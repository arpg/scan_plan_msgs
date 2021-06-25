cmake_minimum_required(VERSION 3.0.2)
project(scan_plan_msgs)

find_package(catkin REQUIRED COMPONENTS
  geometry_msgs
  std_msgs
  message_generation
)

add_message_files(
  FILES
  PointArray.msg
  PointArrays.msg
)

generate_messages(
  DEPENDENCIES
  std_msgs
  geometry_msgs
)

catkin_package( CATKIN_DEPENDS message_runtime )

