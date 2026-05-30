cmake_minimum_required(VERSION 3.8)

project(kuka_kr16_support)

# Find the required ROS 2 build system
find_package(catkin REQUIRED)

# Enable testing if needed
catkin_package()

# Install configuration files, launch files, meshes, and URDFs
install(DIRECTORY config launch meshes urdf
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)

# Finalize package

