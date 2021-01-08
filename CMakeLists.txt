cmake_minimum_required(VERSION 3.10)
project(OpenGLDemo VERSION 1.0)



configure_file(OpenGLDemoConfig.h.in OpenGLDemoConfig.h)
add_subdirectory(src)
add_subdirectory(third_party)
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)
