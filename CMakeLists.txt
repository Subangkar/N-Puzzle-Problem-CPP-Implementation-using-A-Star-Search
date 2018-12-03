cmake_minimum_required(VERSION 3.12)
project(nPuzzle)

set(CMAKE_CXX_STANDARD 11)

add_executable(nPuzzle Node.h AStarSearch.h main.cpp)