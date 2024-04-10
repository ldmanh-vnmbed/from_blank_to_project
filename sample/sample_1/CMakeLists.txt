cmake_minimum_required(VERSION 3.12)
project(sample_1 CXX)

include_directories(${CMAKE_SOURCE_DIR})
# Note:
# - include_directories means include the directory where the include files locate
# - CMAKE_SOURCE_DIR means the current directory of CMakeLists.txt file you are running
# - You can debug CMakeLists.txt by print the value of variable like this

message("Directory: ${CMAKE_SOURCE_DIR}")

add_executable(${PROJECT_NAME} main.cpp someFunc.cpp)
# Note:
# add_executable will build the main.cpp -> main.cpp.o, someFunc.cpp -> someFunc.cpp.o. That means build the source file to object file
# and like them to ${PROJECT_NAME} which PROJECT_NAME set by function project(sample_1 CXX)