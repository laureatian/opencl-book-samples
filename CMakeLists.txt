# This is an example project to show and test the usage of the FindOpenCL
# script.

cmake_minimum_required( VERSION 2.6 )
project( CL_Book )

set(CMAKE_MODULE_PATH "${CMAKE_SOURCE_DIR}/cmake")
#TODO: Need more friendly method
#find_package( OpenCL REQUIRED )
find_package( GLEW REQUIRED)

#include_directories( ${OPENCL_INCLUDE_DIRS} )
#include_directories( "${CMAKE_SOURCE_DIR}/khronos" )
set(OPENCL_LIBRARIES cl)

link_directories(/usr/local/lib/x86_64-linux-gnu/beignet)

SUBDIRS(src)

