To document a bug report in https://github.com/mesonbuild/meson/issues/13931

Assumed building directory: `build`

At the end install with 
```
DESTDIR=./dist meson install -C build
```

You will see quickjs (cmake project) placed its own library in a different folder compared to tcc (meson project).  
Basically cmake when used via meson is misplacing it.
