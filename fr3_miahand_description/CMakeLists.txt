cmake_minimum_required(VERSION 3.0.2)
project(fr3_miahand_description)

## Compile as C++11, supported in ROS Kinetic and newer
add_compile_options(-std=c++17)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS
  franka_description
  mia_hand_description
)

catkin_package(
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

install(DIRECTORY
  launch
  meshes
  robots
  rviz
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)


