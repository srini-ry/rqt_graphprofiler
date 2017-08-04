cmake_minimum_required(VERSION 2.8.3)
project(ros_topology_msgs)

find_package(catkin REQUIRED COMPONENTS message_generation std_msgs)

add_message_files(DIRECTORY msg
  FILES
    Connection.msg
    Graph.msg
    Node.msg
    Service.msg
    Topic.msg
)

generate_messages(DEPENDENCIES std_msgs)
catkin_package(CATKIN_DEPENDS message_runtime std_msgs)
