cmake_minimum_required(VERSION 3.16)
project(curso_cpp_estudos LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Exemplo simples: ajuste para qualquer arquivo que queira compilar rápido.
add_executable(exemplo_rapido curso-cpp/templates/main-template.cpp)
