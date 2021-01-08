add_library(glfw3 STATIC IMPORTED GLOBAL)
target_include_directories(glfw3 INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/include)
set_target_properties(glfw3 PROPERTIES
    IMPORTED_LOCATION ${CMAKE_CURRENT_SOURCE_DIR}/libglfw3.a
)
