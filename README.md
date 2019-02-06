
# Simulating Adaptive Monte Carlo Localization

This repository contains a ROS package which simultaneously localizes and maps a robot in an unknown environment. This is done with the use of a 2D LiDAR and an RGB-D Camera (Kinect)

![start_goal](/images/intro.png)


## Installation
An installation of the [Robot Operating System (ROS)](http://wiki.ros.org/ROS/Installation) is required to run this package. This package has only been tested on the Kinetic and Melodic distributions of ROS.

Clone this repository into a catkin workspace src directory, and build the package.
```
$ git clone https://github.com/kenkangg/ROS_SLAM
$
$ cd ~/catkin_ws
$ catkin_make
$ source devel/setup.bash
```

## Usage
In order to use this package, you will need to launch 4 nodes. Once these nodes are turned on, live visualization of the SLAM algorithm can be seen through both the RTAB-Map and RViz Windows as you move around the environment.

#### Gazebo Simulation
```
$ roslaunch slam_bot world.launch
```

#### Mapping
```
$ roslaunch slam_bot mapping.launch
```

#### Rviz Visualization
```
$ roslaunch slam_bot rviz.launch
```


#### Manual Movement
```
$ roslaunch slam_bot teleop.launch
```
