cmake_minimum_required(VERSION 3.12)
project(sample_2 CXX)

set(LIBS_DIR ${CMAKE_CURRENT_SOURCE_DIR}/libs)
# The set function basiclly set a value to a variable. Same like LIBS_DIR = ${CMAKE_CURRENT_SOURCE_DIR}/libs

add_executable(${PROJECT_NAME} main.cpp)

target_include_directories(${PROJECT_NAME} PUBLIC ${LIBS_DIR})
# Same with include_directory but need 1 more parameter is PUBLIC or PRIVATE ....It not basic, it's advance CMake. So just dont care about it. Just use PUBLIC

target_link_libraries(${PROJECT_NAME} ${LIBS_DIR}/libjustPrint.so)
# To link the static libraries and dynamic libraries to your project
# Use the function target_link_libraries which tell the cmake like the .so file to ${PROJECT_NAME}
# Try to build this with .a file