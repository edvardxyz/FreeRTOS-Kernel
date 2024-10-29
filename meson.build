project('start', 'c')

freertos_sources = files(
  'croutine.c',
  'event_groups.c',
  'list.c',
  'queue.c',
  'tasks.c',
  'timers.c',
  'portable/ThirdParty/GCC/ATmega/port.c',
  #'portable/MemMang/heap_1.c',
)

freertos_include_dirs = include_directories(
  'include',
  'portable/ThirdParty/GCC/ATmega',
)

freertos_lib = static_library(
  'freertos',
  freertos_sources,
  include_directories: freertos_include_dirs
)

freertos_dep = declare_dependency(
  link_with: freertos_lib,
  include_directories: freertos_include_dirs
)
