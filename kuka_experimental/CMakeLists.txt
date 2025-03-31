cmake_minimum_required(VERSION 3.8)  # ROS 2 requires CMake 3.8+
project(kuka_experimental)

# Find ament_cmake (ROS 2 build system)
find_package(ament_cmake REQUIRED)

# No equivalent to catkin_metapackage() needed in ROS 2
# Metapackage configuration is handled in package.xml via:
# <export><metapackage/></export>

# Finalize package
ament_package()