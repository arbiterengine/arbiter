cmake_minimum_required(VERSION 4.2.1)
project(arbiter)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/$<CONFIGURATION>")
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/$<CONFIGURATION>")

add_subdirectory(vendor/sdl EXCLUDE_FROM_ALL)
add_subdirectory(src)

target_link_libraries(arbiter PRIVATE SDL3::SDL3)