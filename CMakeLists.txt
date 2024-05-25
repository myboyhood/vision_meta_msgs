cmake_minimum_required(VERSION 2.8.3)
project(vision_meta_msgs)

## Compile as C++11, supported in ROS Kinetic and newer
# add_compile_options(-std=c++11)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS
  std_msgs
  geometry_msgs
  message_generation
  nav_msgs
  sensor_msgs
  roscpp
  rosmsg
  rospy
)

## Generate messages in the 'msg' folder
add_message_files(
  FILES
  UV_AB.msg
  UVD_AB.msg
  Point.msg
  UV_float32.msg
  UV_uint16.msg
  UVSets.msg
  Instance.msg
  Instances.msg
  MKPTS.msg
  LinesUV.msg
  LineUVUnit.msg
)

## Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  std_msgs
  nav_msgs 
  geometry_msgs
  sensor_msgs
)


catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES swarmtal_msgs
#  CATKIN_DEPENDS geometry_msgs messag_generation nav_msgs roscpp rosmsg rospy
#  DEPENDS system_lib
)

###########
## Build ##
###########

## Specify additional locations of header files
## Your package locations should be listed before other locations
include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)