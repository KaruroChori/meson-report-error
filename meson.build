project(
    'meson-bugreport',
    ['c', 'cpp'],
    version: '1.0.0',
    default_options: ['c_std=c11', 'cpp_std=c++11'],
)

cmake = import('cmake')

libtcc_proj = subproject('libtcc')
libtcc_dep = libtcc_proj.get_variable('libtcc_dep')


opt_quickjs = cmake.subproject_options()
opt_quickjs.add_cmake_defines(
    {
        'CMAKE_POSITION_INDEPENDENT_CODE': true,
    },
)

quickjs_proj = cmake.subproject('quickjs', options: opt_quickjs)
quickjs_dep = quickjs_proj.dependency('qjs')