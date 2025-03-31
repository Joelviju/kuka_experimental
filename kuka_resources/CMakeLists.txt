cmake_minimum_required(VERSION 3.8)

project(kuka_resources)

# Find the required ROS 2 build system
find_package(ament_cmake REQUIRED)

# Install URDF files
install(DIRECTORY urdf
  DESTINATION share/${PROJECT_NAME}
)

# Finalize package
ament_package()
