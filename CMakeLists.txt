cmake_minimum_required(VERSION 3.15)
set(projName aStack)

project(${projName})
set(CATCH2DIR /home/rarce/ccom3034)

IF(EXISTS ${CATCH2DIR})   
  include_directories(${CATCH2DIR})
  add_executable(${projName} main.cpp Stack.h AStack.h ${CATCH2DIR}/catch_amalgamated.cpp)
else()
  add_executable(${projName} main.cpp Stack.h AStack.h catch_amalgamated.cpp)
endif()
