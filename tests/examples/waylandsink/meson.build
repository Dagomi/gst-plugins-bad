gtk_dep = dependency('gtk+-3.0', required : false)
gtk_wayland_dep = dependency('gtk+-wayland-3.0', required : false)

if use_wayland and gtk_dep.found() and gtk_wayland_dep.found()
  executable('waylandsink',
    'main.c',
    extra_files: ['window.ui'],
    install: false,
    include_directories : [configinc],
    dependencies : [gtk_dep, gtk_wayland_dep, gst_dep, gstwayland_dep],
    c_args : ['-DHAVE_CONFIG_H=1', '-DGST_USE_UNSTABLE_API=1'],
  )
endif
