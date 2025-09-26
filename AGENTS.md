# Project Overview
This repository contains an ebpf based sampling profile. It is designed to collect performance data from applications running on Linux systems. The profile captures stack traces at regular intervals, allowing developers to analyze application performance and identify bottlenecks.

# Important libraries
- libbpf: A library for loading and interacting with eBPF programs (https://github.com/libbpf/libbpf).
- argparse: A library for parsing command-line arguments in C++ (https://github.com/p-ranav/argparse).

# Build and Test Commands
To build and test the project, use the following commands:
- Build: `make`
- Test: `make test`

# Code Style Guidelines
The main code is written in C++. Please follow these style guidelines:
- `clang-format` is used for code formatting.

# Testing Instructions
To run tests, use the command `make test`.