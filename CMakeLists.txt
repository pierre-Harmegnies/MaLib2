cmake_minimum_required(VERSION 3.10)
project(MaLib2 LANGUAGES CXX)

add_library(MaLib2 SHARED src/lib2.cpp)
target_include_directories(MaLib2 PUBLIC include)

install(TARGETS MaLib2 DESTINATION lib)
install(FILES include/lib2.h DESTINATION include)
