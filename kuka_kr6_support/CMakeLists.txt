cmake_minimum_required(VERSION 3.8)

project(kuka_kr6_support)

# Find the required ROS 2 build system
find_package(ament_cmake REQUIRED)

# Enable testing if needed
if (BUILD_TESTING)
  find_package(ament_lint_auto REQUIRED)
  ament_lint_auto_find_test_dependencies()
endif()

# Install configuration files, launch files, meshes, and URDFs
install(DIRECTORY config launch meshes urdf
  DESTINATION share/${PROJECT_NAME}
)

# Finalize package
ament_package()
