cmake_minimum_required(VERSION 3.0)
project(drone_ros_msgs)

SET(CMAKE_BUILD_TYPE Release)

find_package(catkin REQUIRED COMPONENTS roscpp tf2_ros geometry_msgs sensor_msgs std_msgs genmsg message_generation)

add_message_files(
  FILES
  Planes.msg
  PlanesInliers.msg
  PlanesInliersArr.msg
  PoseCost.msg
)
generate_messages(
  DEPENDENCIES
  std_msgs
  geometry_msgs
)
catkin_package(
  CATKIN_DEPENDS message_runtime
)
