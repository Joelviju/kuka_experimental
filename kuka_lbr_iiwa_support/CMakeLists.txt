cmake_minimum_required(VERSION 3.8)

project(kuka_lbr_iiwa_support)

# Find the required ROS 2 build system
find_package(ament_cmake REQUIRED)

# Install configuration files, launch files, and URDFs
install(DIRECTORY config launch urdf
  DESTINATION share/${PROJECT_NAME}
)

# Temporarily install collision meshes
install(
  DIRECTORY
    meshes/lbr_iiwa_14_r820/collision
  DESTINATION
    share/${PROJECT_NAME}/meshes/lbr_iiwa_14_r820/
)

# Temporarily install visual meshes
install(
  DIRECTORY
    meshes/lbr_iiwa_14_r820/visual
  DESTINATION
    share/${PROJECT_NAME}/meshes/lbr_iiwa_14_r820/
)

# Finalize package
ament_package()
