

cmake_minimum_required(VERSION 3.30)
project(dijkstra_algoritme)

set(CMAKE_CXX_STANDARD 23)
include_directories(src/include)
add_executable(dijkstra_algoritme
        src/main.cpp
)
