add_executable(OpenGLDemo OpenGLDemo.cpp glad.c)
find_package(OpenGL REQUIRED COMPONENTS OpenGL)
find_package(X11 REQUIRED)
find_package(Threads REQUIRED)

message(STATUS "X11_FOUND = ${X11_FOUND}")
message(STATUS "X11_INCLUDE_DIR = ${X11_INCLUDE_DIR}")
message(STATUS "X11_LIBRARIES = ${X11_LIBRARIES}")

target_link_libraries(OpenGLDemo PUBLIC glfw3 ${CMAKE_DL_LIBS}  OpenGL::OpenGL  ${X11_LIBRARIES} Threads::Threads)

target_include_directories(OpenGLDemo PUBLIC
                                "${PROJECT_BINARY_DIR}"
                                )
