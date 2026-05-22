add_library (nl STATIC nl_single_file.c)
target_include_directories(nl PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}")
set_target_properties(nl PROPERTIES POSITION_INDEPENDENT_CODE TRUE)
