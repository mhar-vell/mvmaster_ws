cmake_minimum_required(VERSION 3.5)
# cmake_minimum_required(VERSION 2.8.3)
project(movemaster_msg)

find_package(catkin REQUIRED COMPONENTS
	message_generation
	std_msgs
)

add_message_files(
  FILES
  setpoint.msg
  status.msg
)

generate_messages(
  DEPENDENCIES
  std_msgs
)

catkin_package(
  CATKIN_DEPENDS message_runtime
)