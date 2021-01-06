cmake_minimum_required(VERSION 3.0.2)
project(face_plate_msgs)

find_package(catkin REQUIRED COMPONENTS
	roscpp
	std_msgs
	message_generation
)


add_message_files(
	FILES
	Face_pic.msg
	Plate_pic.msg
	Illegal_vehicle_pic.msg
	Face_compare.msg
	Illegal_stop_video.msg
)


generate_messages(
	DEPENDENCIES
	std_msgs
)

catkin_package(
	CATKIN_DEPENDS message_runtime std_msgs
)

include_directories(
	${catkin_INCLUDE_DIRS}
)

