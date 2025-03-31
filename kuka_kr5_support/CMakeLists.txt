cmake_minimum_required(VERSION 3.8)

project(kuka_kr5_support)

# Find the required ROS 2 packages
find_package(ament_cmake REQUIRED)

# Enable testing if needed
if (BUILD_TESTING)
  find_package(ament_lint_auto REQUIRED)
  ament_lint_auto_find_test_dependencies()
endif()

# Install package files (configurations, launch files, meshes, URDFs)
install(DIRECTORY config launch meshes urdf
  DESTINATION share/${PROJECT_NAME}
)

# Finalize the package
ament_package()
