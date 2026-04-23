cmake_minimum_required(VERSION 3.10)
project(MaLib2 LANGUAGES CXX)

add_library(MaLib2 SHARED src/lib2.cpp)
target_include_directories(MaLib2 PUBLIC 
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
    $<INSTALL_INTERFACE:include>
)

install(TARGETS MaLib2 
    EXPORT MaLib2Targets
    DESTINATION lib
    INCLUDES DESTINATION include
)

install(FILES include/lib2.h DESTINATION include)

install(EXPORT MaLib2Targets
    FILE MaLib2Config.cmake
    DESTINATION lib/cmake/MaLib2
)
