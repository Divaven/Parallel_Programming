cmake_minimum_required(VERSION 3.16)
project(untitled)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# --- OpenMP ---
find_package(OpenMP REQUIRED)

# --- MPI ---
find_package(MPI REQUIRED)

add_executable(untitled main.cpp)

# Подключаем библиотеки
target_link_libraries(untitled
        PRIVATE
        OpenMP::OpenMP_CXX
        MPI::MPI_CXX
)
