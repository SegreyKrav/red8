cmake_minimum_required(VERSION 3.10)
project(MathUtils)

set(CMAKE_CXX_STANDARD 17)

add_library(m_utils src/m_utils.cpp)

add_executable(app src/main.cpp)
target_link_libraries(app m_utils)

enable_testing()
add_executable(run_tests tests/test.cpp)
target_link_libraries(run_tests m_utils)

add_test(NAME UnitTests COMMAND run_tests)