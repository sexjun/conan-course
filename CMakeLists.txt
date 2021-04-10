cmake_minimum_required(VERSION 3.0.0)
project(md5 VERSION 0.1.0)

add_definitions("-std=c++11")

include(CTest)
enable_testing()

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup()

add_executable(md5 md5.cpp)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)

target_link_libraries(md5 ${CONAN_LIBS})



