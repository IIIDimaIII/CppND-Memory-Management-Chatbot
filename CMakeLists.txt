cmake_minimum_required(VERSION 3.11.3)
project(Membot)

set(CMAKE_CXX_STANDARD 17)

# Use the vcpkg-provided config package (modern approach)
find_package(wxWidgets CONFIG REQUIRED)

file(GLOB project_SRCS src/*.cpp)

# Tell CMake to build a WIN32 (GUI) executable
add_executable(membot WIN32 ${project_SRCS})

target_link_libraries(membot PRIVATE wx::core wx::base)
