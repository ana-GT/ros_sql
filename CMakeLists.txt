cmake_minimum_required(VERSION 2.8.3)
project(ros_sql)

add_compile_options(-std=c++11)

find_package(catkin REQUIRED COMPONENTS
  roscpp rospy rosmsg rosbag rostopic std_msgs geometry_msgs message_generation
)

add_message_files(
  DIRECTORY msg
  FILES TestComplex.msg
)

## Generate messages
generate_messages(
  DEPENDENCIES
  geometry_msgs
  std_msgs
)

catkin_package(
    #INCLUDE_DIRS include
    CATKIN_DEPENDS roscpp rospy rosmsg rosbag rostopic std_msgs geometry_msgs message_runtime
    #LIBRARIES ${PROJECT_NAME}
    #DEPENDS  
)


