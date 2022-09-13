# Setup project
cmake_minimum_required(VERSION 3.10 FATAL_ERROR)
project(viogsf)

set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

# add sources and headers
file(GLOB sources ${PROJECT_SOURCE_DIR}/vbam/apu/*.cpp ${PROJECT_SOURCE_DIR}/vbam/gba/*.cpp)
file(GLOB headers ${PROJECT_SOURCE_DIR}/vbam/apu/*.h ${PROJECT_SOURCE_DIR}/vbam/gba/*.h ${PROJECT_SOURCE_DIR}/vbam/common/*.h)

# build library
add_library(viogsf STATIC ${sources} ${headers})
set_property(TARGET viogsf PROPERTY POSITION_INDEPENDENT_CODE ON)

