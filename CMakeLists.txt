cmake_minimum_required(VERSION 3.16)
project(cello_project C)

set(CMAKE_C_STANDARD 99)

# First, install the library
# https://libcello.org/learn/installation
link_libraries(libCello.a)

# Enable threads
set(THREADS_PREFER_PTHREAD_FLAG ON)
find_package(Threads REQUIRED)

add_executable(cello_project main.c)

target_link_libraries(cello_project PRIVATE Threads::Threads)
