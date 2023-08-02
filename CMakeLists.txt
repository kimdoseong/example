cmake_minimum_required(VERSION 3.0.0)
project(json-cbor VERSION 0.1.0 LANGUAGES C CXX)

include(CTest)
enable_testing()

# find boost
find_package(Boost 1.82.0 REQUIRED COMPONENTS system)
message(STATUS "Boost_INCLUDE_DIR: ${Boost_INCLUDE_DIR}")
include_directories(SYSTEM ${Boost_INCLUDE_DIR})

# find nlohmann
find_path(NLOHMANN_INCLUDE_DIR nlohmann/json.hpp)
message(STATUS "NLOHMANN_INCLUDE_DIR : ${NLOHMANN_INCLUDE_DIR}")

# add_executable(json-cbor main.cpp)
# target_link_directories(json-cbor PRIVATE ${NLOHMANN_INCLUDE_DIR} ${Boost_INCLUDE_DIR})

# json
add_subdirectory(json)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)

