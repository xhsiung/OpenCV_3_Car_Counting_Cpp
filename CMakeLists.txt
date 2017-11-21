cmake_minimum_required(VERSION 2.8)
project( main )
add_compile_options(-std=c++11)

find_package( OpenCV REQUIRED )
include_directories( ${OpenCV_INCLUDE_DIRS} )
add_executable( main main.cpp Blob.cpp Blob.h )
target_link_libraries( main ${OpenCV_LIBS} )
