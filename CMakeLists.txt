cmake_minimum_required(VERSION 2.27)
 
project(honda)

# Locate GTest

find_package(GTest REQUIRED)

include_directories(${GTEST_INCLUDE_DIRS})
 
# Link unit_tests with what we want to test and the GTest and pthread library

add_executable(Test.cpp )
 
target_link_libraries(unit_tests ${GTEST_LIBRARIES} pthread)

find_package(Threads REQUIRED)
