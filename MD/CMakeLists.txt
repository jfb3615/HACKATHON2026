cmake_minimum_required(VERSION 3.16)
set (target MD)
project(${target} LANGUAGES CXX)

set(CMAKE_BUILD_TYPE Release)
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

find_package(Eigen3 REQUIRED)

file(GLOB SOURCES CONFIGURE_DEPENDS "${CMAKE_CURRENT_SOURCE_DIR}/src/*.cpp")

add_library(${target} SHARED ${SOURCES})
target_include_directories(${target} PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/MD")
target_link_libraries(${target} PRIVATE Eigen3::Eigen)
