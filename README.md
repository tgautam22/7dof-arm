# 7-DOF Robot Arm

A 7-degree-of-freedom robot arm designed in SolidWorks and simulated in ROS 2 with MoveIt 2 for motion planning.

## Overview

- 7 revolute joints using CubeMars AK60-39 and AK45-36 actuators
- 6061-T6 aluminum links
- Rated for a 1 kg payload, with a maximum static payload of 2.43 kg

## Repo Structure

```
arm_7dof/                 URDF, meshes, and RViz launch file
arm_7dof_moveit_config/   MoveIt 2 configuration
```

## Running It

Requires Ubuntu 24.04 and ROS 2 Jazzy with MoveIt 2.

```bash
mkdir -p ~/ros2_ws/src && cd ~/ros2_ws/src
git clone https://github.com/tgautam22/7dof-arm.git
cd ~/ros2_ws && colcon build --symlink-install
source install/setup.bash
ros2 launch arm_7dof_moveit_config demo.launch.py
```