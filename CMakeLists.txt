ask_build_sourcey_module(pacm)
if(BUILD_MODULES AND BUILD_MODULE_pacm) 
  #include_dependency(OpenSSL REQUIRED)
  #include_dependency(JsonCpp REQUIRED)
  #include_dependency(LibUV REQUIRED)
  #include_dependency(HttpParser REQUIRED)
  #include_dependency(ZLIB REQUIRED)
  #include_dependency(Minizip REQUIRED)

  define_sourcey_module(pacm base uv net json http archo crypto)
  
  add_subdirectory(applications)
endif()
