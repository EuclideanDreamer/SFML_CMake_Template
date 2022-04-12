

project(proj)

cmake_minimum_required(VERSION 3.8)

set(CMAKE_CXX_COMPILER_ID "GNU")
set(CMAKE_CXX_COMPILER_VERSION "4.6.3")


add_executable(proj "Source/main.cpp" )
target_include_directories(proj PUBLIC "/usr/include")
target_include_directories(proj PUBLIC "/home/booboo/Desktop/SFML/SFML_Project_Template/Headers")
target_include_directories(proj PUBLIC "/home/booboo/Desktop/SFML/SFML_Project_Template/Source")

target_precompile_headers(proj PUBLIC "Headers/header.h")
target_link_libraries(proj sfml-graphics sfml-window sfml-system )


# all this to do below essentally
# $g++ -c main.cpp
# $g++ main.o -o p -lsfml-graphics -lsfml-window -lsfml-system
