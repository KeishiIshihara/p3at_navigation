cmake_minimum_required(VERSION 2.8.3)
project(p3at_navigation)

# Find all required modules for compilation
find_package(catkin REQUIRED COMPONENTS
    roscpp
    tf
    geometry_msgs
    nav_msgs
    std_srvs
    costmap_2d
    clear_costmap_recovery
)


generate_messages(DEPENDENCIES std_msgs )

# Nothing that can be imported by other modules
catkin_package()

include_directories(
  ${catkin_INCLUDE_DIRS}
)


# Instructions to install launch files
install(DIRECTORY launch/
    DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/launch )

# Instructions to install configuration files
install(DIRECTORY navigation_conf/
    DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/nav_conf )
install(DIRECTORY maps/
    DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/maps )

# Executable files






