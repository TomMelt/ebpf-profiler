cmake_minimum_required(VERSION 3.10)
project(ebpf_profiler)

# Set C++ standard and flags
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} --std=c++17")

# Add argparse subdirectory
add_subdirectory(src/argparse)

# Find source files
set(PROFILER_SOURCES
    src/profiler/perf_profiler.cpp
)

# Create executable
add_executable(perf_profiler ${PROFILER_SOURCES})

# Include directories
target_include_directories(perf_profiler PRIVATE
    ${CMAKE_SOURCE_DIR}/src/profiler
    ${CMAKE_SOURCE_DIR}/src/argparse/include
)

# Link libraries
target_link_libraries(perf_profiler
    PRIVATE
    argparse
    -lbcc
)
