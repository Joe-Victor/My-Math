cmake_minimum_required(VERSION 3.21)
project(Test)

### Uncomment this ONCE to generate a libmy_math.a file
 add_library(my_math STATIC my_math.cpp my_math.h)

add_executable(Test main.cpp)

find_library(MY_MATH_LIB my_math HINTS ./lib)
target_link_libraries(Test PUBLIC ${MY_MATH_LIB})

