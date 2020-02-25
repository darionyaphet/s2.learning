cmake_minimum_required(VERSION 3.15)
project(s2_learning)

set(CMAKE_CXX_STANDARD 14)

set(INC_DIR /usr/local/Cellar/s2geometry/0.9.0_1/include/s2)
set(LINK_DIR /usr/local/Cellar/s2geometry/0.9.0_1/lib)
link_libraries(s2)

add_executable(point_index point_index.cpp)
add_executable(term_index  term_index.cpp)

include_directories(${INC_DIR})
link_directories(${LINK_DIR})

target_link_libraries(point_index s2testing s2)
target_link_libraries(term_index  s2testing s2)