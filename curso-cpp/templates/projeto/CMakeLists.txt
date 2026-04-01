cmake_minimum_required(VERSION 3.16)
project(projeto_exemplo LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

add_executable(projeto_exemplo src/main.cpp)
