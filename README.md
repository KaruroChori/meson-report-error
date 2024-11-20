Assumed building directory: `build`

At the end install with 
```
DESTDIR=./dist meson install -C build
```

You will see quickjs placed its own library in a different folder compared to tcc. Basically cmake via meson is misplacing it.