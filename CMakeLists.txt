cmake_minimum_required(VERSION 3.0.2)
project(led_circuit_msgs)

find_package(catkin REQUIRED COMPONENTS
  message_generation
  std_msgs
)

add_message_files(
  FILES
  Pattern.msg
  Command.msg
)

generate_messages(
  DEPENDENCIES
  std_msgs
)

catkin_package(
  CATKIN_DEPENDS 
  message_runtime
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)
