cmake_minimum_required(VERSION 3.26 FATAL_ERROR)
set(CMAKE_OSX_ARCHITECTURES "arm64")

project(app VERSION 1.0)

add_definitions(-std=c++17)
set(CXX_FLAGS "-Wall")
set(CMAKE_CXX_FLAGS, "${CXX_FLAGS}")
set(CMAKE_BUILD_TYPE Debug)

add_executable(app main.cpp)

find_package(glfw3 3.4 REQUIRED)
find_package(OpenGL REQUIRED)

target_include_directories(app PUBLIC ${OPENGL_INCLUDE_DIR})

target_link_libraries(app "-framework Cocoa")
target_link_libraries(app "-framework OpenGL")
target_link_libraries(app "-framework IOKit")
target_link_libraries(app "-framework QuartzCore")
target_link_libraries(app glfw ${OPENGL_gl_LIBRARY})