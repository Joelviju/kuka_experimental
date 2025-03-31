cmake_minimum_required(VERSION 3.8)

project(kuka_kr3_support)

# Find required ROS 2 packages
find_package(ament_cmake REQUIRED)

# Enable testing if needed
if (BUILD_TESTING)
  find_package(ament_lint_auto REQUIRED)
  ament_lint_auto_find_test_dependencies()
endif()

# Install package files (configuration, launch, meshes, URDFs)
install(DIRECTORY config launch meshes urdf
  DESTINATION share/${PROJECT_NAME}
)

# Finalize package
ament_package()

