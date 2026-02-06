cmake_minimum_required(VERSION 3.30)

project(boids CXX)

set(target entt_boids)
add_executable(${target})

# dependencies

find_package(EnTT CONFIG REQUIRED)
target_link_libraries(${target} PRIVATE EnTT::EnTT)
find_package(raylib CONFIG REQUIRED)
target_link_libraries(${target} PRIVATE raylib)
find_package(glfw3 REQUIRED)
target_link_libraries(${target} PRIVATE glfw)


add_subdirectory(boids)
