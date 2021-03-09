cmake_minimum_required(VERSION 3.0.2)
project(husky_planning)

find_package(catkin REQUIRED COMPONENTS
  global_planner
  husky_gazebo
  husky_navigation
  husky_viz
)

catkin_package()

include_directories(
  ${catkin_INCLUDE_DIRS}
)

install(
  DIRECTORY launch rviz
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
