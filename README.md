#Pick-n-Place-Masters-Research

This repository is complimentry to Masters Research of Taha Al Lawati

This project have focused on UR5e and Robotiq 2F-85 gripper.


We are building the UR ROS 2 Driver from source which can be found here.
[UR ROS 2 Driver](https://docs.universal-robots.com/Universal_Robots_ROS2_Documentation/doc/ur_robot_driver/ur_robot_driver/doc/installation/installation.html)

I have edited the files which is not ideal. Ideally we wound want to create a new package that calls files from driver packages and modify the files in the new package. 
This change I would do if the time allowed.

For the gripper, since I have encounted many issues with configuring the gripper, I have used multiple of repositories for the gripper.

This repository is how I managed to turn on the gripper and send commands to it from ROS 2. However, it would lose connection as soon as I establish the connection through external control by running the external control program from the teaching pendent.
[UR Robotiq Inegrated Driver](https://github.com/robotic-vision-lab/UR-Robotiq-Integrated-Driver/tree/public-release)
note: I was not using docker as they specify in the repo.


The repo with full files for the Robotiq gripper
[ROS 2 Robotiq Gripper by PickNikRobotics](https://github.com/PickNikRobotics/ros2_robotiq_gripper/tree/main)

### we have to use these commands as they are not mentioned in the readme.md
```bash
git clone -b humble https://github.com/PickNikRobotics/ros2_robotiq_gripper.git src/robotiq

vcs import src --skip-existing --input src/robotiq/ros2_robotiq_gripper-not-released.humble.repos
