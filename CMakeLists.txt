cmake_minimum_required(VERSION 2.8.4) 

PROJECT(dlib_test) 

SET(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -O2")

IF(CMAKE_CXX_COMPILER_ID STREQUAL "Clang") 
  SET(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Weverything") 
ELSEIF(CMAKE_CXX_COMPILER_ID STREQUAL "GNU") 
  SET(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -Wextra") 
ENDIF() 

INCLUDE(/home/zhoujie/dlib-19.16/dlib/cmake)

ADD_EXECUTABLE(dlib_test dlib_test.cpp) 
TARGET_LINK_LIBRARIES(dlib_test dlib)

