cmake_minimum_required(VERSION 3.0.0)
project(client VERSION 0.1.0 LANGUAGES C CXX)

include(CTest)
enable_testing()

add_executable(client client.cpp)
target_link_directories(client PRIVATE ${NLOHMANN_INCLUDE_DIR} ${Boost_INCLUDE_DIR})

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)