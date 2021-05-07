project('foo', 'c', 'vala')

glib_dep = dependency('glib-2.0')
gobject_dep = dependency('gobject-2.0')

executable(
    meson.project_name(),
    'foo.vala',
    dependencies: [
        glib_dep,
        gobject_dep
    ]
    # ,install: true
)

