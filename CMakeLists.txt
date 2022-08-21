cmake_minimum_required(VERSION 3.23)
project(cpp_bouncy_balls)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++17")

set(SOURCE_FILES main.cpp)
add_executable(cpp_bouncy_balls ${SOURCE_FILES})

include_directories(CMAKE_SOURCE_DIR/ExternalLibraries/SFML/include)

find_package(SFML 2.5 COMPONENTS system window graphics network audio REQUIRED)
include_directories(${SFML_INCLUDE_DIRS})
target_link_libraries(cpp_bouncy_balls sfml-system sfml-window sfml-graphics sfml-audio sfml-network)