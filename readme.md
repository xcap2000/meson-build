# Meson Build

Create a meson.build file with the following contents:

```meson
project('foo', 'c', 'vala')

glib_dep = dependency('glib-2.0')
gobject_dep = dependency('gobject-2.0')

executable('foo', 'foo.vala', dependencies: [glib_dep, gobject_dep])
```

Create a foo.vala file with the following contents:

```vala
int main (string[] args) {
    stdout.printf ("hello, world\n");
    return 0;
}
```

Create a build folder and build the project:

```bash
$ mkdir build
$ cd build
$ meson ..
$ ninja # sudo ninja install
$ ./foo
```

If install: true

```bash
$ meson build --prefix=/usr # same folder
$ cd build
$ ninja # sudo ninja install
$ ./foo
```

## References

```
https://wiki.gnome.org/Projects/Vala/Documentation
https://wiki.gnome.org/Projects/Vala/Tools/Meson
https://github.com/mesonbuild/meson/blob/master/docs/markdown/FAQ.md
```