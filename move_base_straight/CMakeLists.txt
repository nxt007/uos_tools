# Catkin User Guide: http://www.ros.org/doc/groovy/api/catkin/html/user_guide/user_guide.html
# Catkin CMake Standard: http://www.ros.org/doc/groovy/api/catkin/html/user_guide/standards.html
cmake_minimum_required(VERSION 2.8.3)
project(move_base_straight)

# Load catkin and all dependencies required for this package
find_package(catkin REQUIRED COMPONENTS)

catkin_package(
    CATKIN_DEPENDS
)

install(PROGRAMS
    nodes/move_base_straight.py
    DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)

install(DIRECTORY
    launch/
    DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/launch
)
