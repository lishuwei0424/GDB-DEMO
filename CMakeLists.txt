CMAKE_MINIMUM_REQUIRED(VERSION 2.8)
PROJECT(GDB)


set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -pthread -g  -O0" )

#OpenCV3.4.3
set(OpenCV_DIR  /usr/local/opencv-3.4.3/share/OpenCV)
find_package(OpenCV 3.4.3   REQUIRED)
include_directories(SYSTEM ${OpenCV_INCLUDE_DIRS}  /usr/local/opencv-3.4.3/include)
link_directories(${OpenCV_LIBRARY_DIRS}  /usr/local/opencv-3.4.3/lib)

add_executable(GBD_DEMO main.cpp)
target_link_libraries(GBD_DEMO ${OpenCV_LIBS})
