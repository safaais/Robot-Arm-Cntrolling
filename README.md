# Robot-Arm-Cntrolling

Controlling the Robot Arm
This comprehensive guide outlines the steps for setting up and managing the robot arm using ROS, including simulations and kinematics with MoveIt.
## Create a ROS Workspace
In terminal, execute the following commands:
```
source /opt/ros/noetic/setup.bash
mkdir -p ~/catkin_ws/src
cd ~/catkin_ws/
catkin_make
source devel/setup.bash
```
Your ROS workspace is now ready for package installation.
## Install the Arduino Robot Arm Package
Navigate to the "src" directory and add the "arduino_robot_arm" package:

```
cd ~/catkin_ws/src/
sudo apt install git
```
## Install Dependencies
In the terminal, run the following commands:

```
cd ~/catkin_ws
sudo apt-get install ros-noetic-moveit
sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui
sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher
sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control
```
## Compile Packages
Compile your packages with:

```
catkin_make
```
## Implementing a Robot Arm Using ROS
Launch the Joint State Publisher in RViz
To initialize RViz, execute:

```
roslaunch robot_arm_pkg check_motors.launch
```

2.	Then, runn Gazebo simulation:

```
roslaunch robot_arm_pkg check_motors_gazebo.launch
```
3.	Finally, Use Moveit for Kinematics

```
roslaunch moveit_pkg demo.launch
```
![image alt](https://github.com/safaais/Robot-Arm-Cntrolling/blob/723a9acaa9d5df11da278915e3657cd36157377c/Screenshot%202024-08-15%20234435.png)

