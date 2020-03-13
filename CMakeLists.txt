cmake_minimum_required(VERSION 3.10)
project(homework4_kit)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -lpqxx -lpq")

set(PQXX /usr/include/pqxx)

find_library(PQXX_LIB pqxx)
find_library(PQ_LIB pq)

include_directories(.)


add_executable(homework4_kit
        exerciser.cpp
        exerciser.h
        main.cpp
        query_funcs.cpp
        query_funcs.h)

