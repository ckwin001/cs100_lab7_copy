CMAKE_MINIMUM_REQUIRED(VERSION 2.8)

ADD_SUBDIRECTORY(googletest)

SET(CMAKE_CXX_STANDARD 11)
#SET(CMAKE_BUILD_TYPE Debug)

ADD_EXECUTABLE(test
    tests/unit_test.cpp
)

ADD_EXECUTABLE(calculator
    src/main.cpp
    src/factory.cpp
)

TARGET_LINK_LIBRARIES(test gtest)
TARGET_COMPILE_DEFINITIONS(test PRIVATE gtest_disable_pthreads=ON)
