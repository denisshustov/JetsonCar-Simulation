cmake_minimum_required(VERSION 2.8.3)
project(jetson_hw)

## Compile as C++11, supported in ROS Kinetic and newer
# add_compile_options(-std=c++11)

find_package(catkin REQUIRED COMPONENTS
  controller_manager
  hardware_interface
  roscpp
)
catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES jetson_hw
#  CATKIN_DEPENDS controller_manager hardware_interface roscpp
#  DEPENDS system_lib
)

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)

add_executable(jetson_hw src/jetson_hw.cpp)


target_link_libraries(jetson_hw
   ${catkin_LIBRARIES}
)
