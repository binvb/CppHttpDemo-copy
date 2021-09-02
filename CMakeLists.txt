cmake_minimum_required(VERSION 3.5)

project (httpserver CXX C)

SET (CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")
SET (CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -std=c99")

aux_source_directory(./httpserver dir_src)

include_directories(./common)

add_subdirectory(common)

add_executable(httpserver ${dir_src})
target_link_libraries(httpserver common)
