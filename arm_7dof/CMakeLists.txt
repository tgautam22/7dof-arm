cmake_minimum_required(VERSION 3.8)

project(arm_7dof)

find_package(ament_cmake REQUIRED)

install(DIRECTORY config launch meshes urdf rviz
  DESTINATION share/${PROJECT_NAME}
)

ament_package()
