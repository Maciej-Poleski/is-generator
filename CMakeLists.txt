cmake_minimum_required(VERSION 2.8.8 FATAL_ERROR)
project(is-generator)

set(Boost_USE_STATIC_RUNTIME OFF)

find_package(Boost 1.49.0 REQUIRED)
include_directories(${Boost_INCLUDE_DIRS})

add_executable(is-generator main.cpp)
target_link_libraries(is-generator ${Boost_LIBRARIES})

install(TARGETS is-generator RUNTIME DESTINATION bin)
