# RoboND-Localization-Project

 In this project two robot models are created using URDF in a Gazebo/RViz environment, and are assigned to navigate within a given map to reach a predefined goal position. Robots have two sensors: a camera and a laser scanner, to process data from sensors and move the robot models ROS navigation stack is used.Both robots use AMCL (Adaptive Monte Carlo Localiation) ROS package to perform localization . Please refer to [project writeup](https://github.com/Zerde/RoboND-Localization-Project/blob/master/writeup%20and%20screenshots/localization-project-writeup.pdf) for more information.

## Project Setup and run

Create catkin workspace, if you haven't already.For this project catkin_ws is used, if your workspace name is different, change the commands accordingly. 

```sh
$ mkdir -p ~/catkin_ws/src
$ cd ~/catkin_ws/src
$ catkin_init_workspace
$ cd ~/catkin_ws
$ catkin_make
```
Create package called "udacity_bot":
```sh
$ cd ~/catkin_ws/src
$ catkin_create_pkg udacity_bot
```
Copy this repo into udacity_bot folder, source and build the project:
```sh
$ cd ~/catkin_ws
$ source devel/setup.bash
$ catkin_make
```
To run with udacity_bot model:
```sh
$ cd ~/catkin_ws
$ roslaunch udacity_bot udacity_world.launch
$ roslaunch udacity_bot amcl.launch
$ rosrun udacity_bot navigation_goal
```
To run with ziz_bot model:
```sh
$ cd ~/catkin_ws
$ roslaunch udacity_bot ziz_world.launch
$ roslaunch udacity_bot amcl_ziz.launch
$ rosrun udacity_bot navigation_goal
```
