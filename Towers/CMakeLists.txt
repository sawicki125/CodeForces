cmake_minimum_required(VERSION 3.7)
project(Towers)

set(CMAKE_CXX_STANDARD 11)

set(SOURCE_FILES src/main.cpp src/UT/Towers_test.cpp src/UT/Towers_test.hpp src/Towers.cpp src/Towers.hpp)
add_executable(Towers ${SOURCE_FILES})

add_subdirectory(googletest)

include_directories(googletest/googletest/include)

include_directories(googletest/googlemock/include)

target_link_libraries(Towers gtest gtest_main)