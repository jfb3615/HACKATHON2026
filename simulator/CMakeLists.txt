cmake_minimum_required(VERSION 3.16)
set (target simulator)
project(${target} LANGUAGES CXX)

set(CMAKE_BUILD_TYPE Release)
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

file(GLOB SOURCES CONFIGURE_DEPENDS "${CMAKE_CURRENT_SOURCE_DIR}/src/*.cpp")

add_executable(${target} ${SOURCES})
target_link_libraries(${target} PRIVATE MC MD Model PostProcess Visualization)