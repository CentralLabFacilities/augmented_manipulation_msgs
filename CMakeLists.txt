cmake_minimum_required(VERSION 2.8.3)
project(augmented_manipulation_msgs)

find_package(catkin REQUIRED
  COMPONENTS
    actionlib
    message_generation
    std_msgs
)

link_directories(${catkin_LIBRARY_DIRS}})

add_action_files(
  FILES
  AugmentedPickup.action
)

add_message_files(
  FILES
  GroupConfig.msg
)

generate_messages(DEPENDENCIES actionlib_msgs std_msgs)

catkin_package()
