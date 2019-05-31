# Simple example using mod.io in Godot

This is a small example using modio.io's SDK C interface to create a GDNative script that just showcases some very simple bare bones calls

## Compiling

Dependencies:

 * You need [Godot headers](https://github.com/GodotNativeTools/godot_headers)
 * clang or any decent C compiler that's C11 or C99 compatible

### Linux
To compile the library on Linux, do

```
clang -std=c11 -fPIC -c -I./godot_headers src/modio_wrapper.c -o src/modio_wrapper.os
clang -shared src/modio_wrapper.os -L. -lmodio -o ./bin/libmodio_wrapper.so
```

This creates the file `libmodio_wrapper.so` in your `bin/` directory.

### Mac OS X

Todo: Test Mac Os compilation.

### Windows

Todo: Test Windows compilation.

## Usage

Create a new object using `preload("res://bin/modio_wrapper.gdns").new()`

## References

 * [GDNative is here!](https://godotengine.org/article/dlscript-here)
 * [GDNative tutorial](https://docs.godotengine.org/en/3.1/tutorials/plugins/gdnative/gdnative-c-example.html)
 * [GDNative C demo](https://github.com/GodotNativeTools/GDNative-demos/tree/master/c/SimpleDemo) 
