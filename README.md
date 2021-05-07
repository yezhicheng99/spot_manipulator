
# Boston dynamics spot robot with open manipulator

## Simulation
<img src="https://github.com/yezhicheng99/spot_manipulator/blob/master/readme/env.png" width="900">


Tested on:
- Ubuntu 18.04 (ROS Melodic)

## 1. Installation

### 1.1 Clone and install all dependencies:

    sudo apt install -y python-rosdep
    cd <your_ws>/src
    git clone https://github.com/yezhicheng99/spot_manipulator.git
    git clone https://github.com/yezhicheng99/spot_manipulator_gui.git
    git clone https://github.com/chvmp/champ_teleop
    cd ..
    rosdep install --from-paths src --ignore-src -r -y

### 1.2 Build your workspace:

    cd <your_ws>
    catkin_make
    source <your_ws/>/devel/setup.bash

## 2. Quick Start

### 2.1 Start gazebo simulation:
    roslaunch spot_manipulator gazebo.launch

### 2.2 Control open manipulator:
    roslaunch spot_manipulator move_group.launch
    roslaunch spot_manipulator_gui spot_manipulator_gui.launch

### 2.3 Run the teleop node:
    roslaunch champ_teleop teleop.launch