cmake_minimum_required(VERSION 3.17)
project(gootest)

set(CMAKE_CXX_STANDARD 14)

add_executable(gootest main.cpp Tests/lol.cpp)
add_subdirectory(lib/googletest)
include_directories(lib/googletest/googletest/include)
include_directories(lib/googletest/googlemock/include)
target_link_libraries(gootest gtest gtest_main)