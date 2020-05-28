cmake_minimum_required(VERSION 3.15)
project(COMEN)

set(VERSION 0.3.2)
set(CMAKE_CXX_STANDARD 14)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -O3")
#set(LDFLAGS -g -lm -flto -no-pie)
set(SOURCE_FILES src/errorHandler.c src/errorHandler.h src/common.h src/common.c src/smoothing.c src/smoothing.h src/commonStructs.c src/commonStructs.h src/nGramReader.c src/nGramReader.h)
add_executable(createNG src/createNG.c src/createNG.h src/cmdlineCreateNG.c src/cmdlineCreateNG.h ${SOURCE_FILES})
add_executable(enumNG src/enumNG.c src/enumNG.h src/boosting.c src/boosting.h src/cmdlineEnumNG.c src/cmdlineEnumNG.h src/attackSimulator.c src/attackSimulator.h ${SOURCE_FILES})
#add_executable(evalPW src/evalPW.c src/evalPW.h)
add_executable(test src/test.cpp src/test.h src/createNG.c src/createNG.h src/cmdlineCreateNG.c src/cmdlineCreateNG.h ${SOURCE_FILES})