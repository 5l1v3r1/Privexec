# bela win libaray

add_library(belawin STATIC
  appexeclink.cc
  env.cc
  io.cc
  path.cc
  peimage.cc
  process.cc
  realpath.cc
  reparsepoint.cc
  version.cc
)

target_link_libraries(belawin
  bela
  version
)


if(BELA_ENABLE_LTO)
  set_property(TARGET belawin PROPERTY INTERPROCEDURAL_OPTIMIZATION TRUE)
endif()
