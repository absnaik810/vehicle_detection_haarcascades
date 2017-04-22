cmake_minimum_required(VERSION 2.8)

project(vehicle_detection_haarcascades)

set(OpenCV_FOUND 1)

set(OpenCV_DIR ~/downloads/opencv-2.4.13.2/build)

find_package(OpenCV REQUIRED)

set(vehicle_detection_src vehicle_detection.cpp)

include_directories(${CMAKE_SOURCE_DIR})

add_executable(vehicle_detection_haarcascades ${vehicle_detection_src})

target_link_libraries(vehicle_detection_haarcascades ${OpenCV_LIBS})

