cmake_minimum_required(VERSION 2.8.3)
project(r4d_2_multimarker)

add_definitions(-std=c++11)

find_package(catkin REQUIRED COMPONENTS
  r4d_common
)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES r4d_2_tracking
#  CATKIN_DEPENDS r4d_common
#  DEPENDS system_lib
)

include_directories(
  include
  ${catkin_INCLUDE_DIRS}
)

add_executable(multimarker_node src/multimarker_node.cpp)

target_link_libraries(multimarker_node
  ${catkin_LIBRARIES}
)
