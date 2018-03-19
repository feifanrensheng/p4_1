cmake_minimum_required( VERSION 2.8 )
project( undistort_image )

# 添加c++ 11标准支持
set( CMAKE_CXX_FLAGS "-std=c++11" )

set(CMAKE_MODULE_PATH /home/zn/opencv-3.1.0/release)
# 寻找OpenCV库
find_package( Opencv REQUIRED )
if(Opencv_FOUND)
    message(STATUS "The OpenCV lib is found!")
endif()
 
add_executable( undistort_image undistort_image.cpp)
# 链接OpenCV库
target_link_libraries( undistort_image ${OpenCV_LIBS})

