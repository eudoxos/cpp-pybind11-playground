cmake_minimum_required(VERSION 3.4)
project(scripting)

set(PYBIND11_PYTHON_VERSION 3.6)

FIND_PACKAGE(pybind11 CONFIG)

ADD_EXECUTABLE(scripting src/main.cpp)
TARGET_LINK_LIBRARIES(scripting ${PYTHON_LIBRARIES})
TARGET_LINK_LIBRARIES(scripting pybind11::embed)
