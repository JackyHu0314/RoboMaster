cmake_minimum_required(VERSION 3.16)

project(RoboMasterHelloWorld VERSION 1.0 LANGUAGES CXX)

add_executable(hello src/main.cpp)
target_compile_features(hello PRIVATE cxx_std_17)

enable_testing()
add_test(NAME hello_output COMMAND hello)
set_tests_properties(hello_output PROPERTIES
    PASS_REGULAR_EXPRESSION "^Hello, RoboMaster!"
)
