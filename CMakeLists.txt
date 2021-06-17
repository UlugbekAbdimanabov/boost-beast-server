cmake_minimum_required(VERSION 3.12)

#set(BOOST_ROOT "C:/local/boost_1_70_0")

#ADD_DEFINITIONS("-DBOOST_ALL_NO_LIB")

set(CMAKE_CXX_STANDARD 11)

find_package(Boost 1.70.0 COMPONENTS program_options REQUIRED)

#set(Boost_USE_STATIC_LIBS ON)

add_executable(anyExecutable servak.cpp)

target_link_libraries(anyExecutable Boost::program_options pthread)