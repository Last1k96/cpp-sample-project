cmake_minimum_required(VERSION 3.23)
project(sample_project)

set(CMAKE_CXX_STANDARD 11)

# strongly encouraged to enable this globally to avoid conflicts between
# -Wpedantic being enabled and -std=c++20 and -std=gnu++20 for example
# when compiling with PCH enabled
set(CMAKE_CXX_EXTENSIONS OFF)

add_executable(${PROJECT_NAME} main.cpp)

find_package(fmt REQUIRED)

target_link_libraries(
    ${PROJECT_NAME} 
    PRIVATE fmt::fmt)


