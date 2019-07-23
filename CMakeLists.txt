cmake_minimum_required(VERSION 2.8.3)
project(heri_hand_ros)

find_package(catkin REQUIRED COMPONENTS message_generation std_msgs)

###########
## Build ##
###########

add_message_files(
DIRECTORY msgs
FILES
HeriHandControl.msg
)

add_message_files(
DIRECTORY msgs
FILES
HeriHandState.msg
)

add_message_files(
DIRECTORY msgs
FILES
HeriHandFinger.msg
)

add_message_files(
DIRECTORY msgs
FILES
HeriHandFingerAnalogs.msg
)
    
generate_messages(
DEPENDENCIES
std_msgs
)

