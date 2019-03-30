cmake_minimum_required(VERSION 3.5.1)
project(wsrpc VERSION 0.0.1 LANGUAGES CXX)

enable_testing()

include(cmake/cmake-conan/conan.cmake)

conan_cmake_run(
    REQUIRES Catch2/2.7.0@catchorg/stable
    BASIC_SETUP CMAKE_TARGETS
    BUILD missing
)

add_subdirectory(test)
