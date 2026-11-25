cmake_minimum_required(VERSION 3.16)

project(HACKATHON2026 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)


add_subdirectory(MC)
add_subdirectory(MD)
add_subdirectory(PostProcess)
add_subdirectory(Model)
add_subdirectory(Visualization)
add_subdirectory(simulator)
