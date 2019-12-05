cmake_minimum_required (VERSION 3.5.1)
project(pfs-json CXX)

set(CMAKE_POSITION_INDEPENDENT_CODE TRUE)
option(pfs_json_BUILD_TESTS "Build tests" ON)

if (pfs_json_BUILD_TESTS)
    enable_testing()
    include_directories(${CMAKE_CURRENT_LIST_DIR}/include)
    add_subdirectory(src/tests)
endif()