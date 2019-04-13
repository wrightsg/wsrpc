add_executable(catch_test catch_test.cpp)
target_compile_features(catch_test PRIVATE cxx_std_11)
target_link_libraries(catch_test PRIVATE CONAN_PKG::Catch2)
add_test(NAME catch_test COMMAND catch_test)
