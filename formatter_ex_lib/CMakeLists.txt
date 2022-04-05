cmake_minimum_required(VERSION 3.16)
 
set(CMAKE_CXX_STANDARD 20)
 
project(formatter_ex)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../formatter_lib)
add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/../formatter_lib formatter_lib)

add_library(${PROJECT_NAME} STATIC formatter_ex.h formatter_ex.cpp)

target_link_libraries(${PROJECT_NAME} formatter)
