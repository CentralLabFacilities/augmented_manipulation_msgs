cmake_minimum_required(VERSION 2.8.3)
project(augmented_manipulation_msgs)

find_package(catkin REQUIRED
  COMPONENTS
    actionlib
    message_generation
    std_msgs
    moveit_msgs
)

link_directories(${catkin_LIBRARY_DIRS}})


add_message_files(
  FILES
  GraspConfigSet.msg
  AugmentedPickupQuery.msg
)

add_action_files(
  FILES
  AugmentedPickup.action
)

generate_messages(DEPENDENCIES actionlib_msgs std_msgs moveit_msgs)

catkin_package()
