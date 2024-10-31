cmake_minimum_required(VERSION 3.5)
project(nav2_implementation)

find_package(ament_cmake REQUIRED)
find_package(rclcpp REQUIRED)
find_package(rclcpp_action REQUIRED)
find_package(nav2_msgs REQUIRED)

add_executable(waypoint_follow src/waypoint_follow.cpp) 
ament_target_dependencies(waypoint_follow rclcpp std_msgs rclcpp_action nav2_msgs)

install(DIRECTORY
  launch
  params
  maps
  rviz2
  config
  DESTINATION share/${PROJECT_NAME}
)

install(TARGETS waypoint_follow DESTINATION lib/${PROJECT_NAME})

ament_package()
