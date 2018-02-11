cmake_minimum_required(VERSION 2.8.3)

project(goat_launch)

find_package(catkin REQUIRED COMPONENTS urdf_goat joint_state_publisher
                                        robot_state_publisher)

catkin_package(CATKIN_DEPENDS urdf_goat joint_state_publisher
                              robot_state_publisher)

include_directories(${catkin_INCLUDE_DIRS})

install(DIRECTORY launch/
        DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/launch)
