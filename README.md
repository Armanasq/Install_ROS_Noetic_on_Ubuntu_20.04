This repository provides step-by-step instructions on how to install ROS Noetic on Ubuntu 20.04.

# Prerequisites
Before you begin, ensure that you have the following:

* Ubuntu 20.04 installed on your system.
* A stable internet connection.

## Installation
1. First, add the ROS Noetic repository to your sources list

```
sudo apt update
sudo apt install -y curl
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
```

2. Next, update your package list and install ROS Noetic:

```
sudo apt update
sudo apt install -y ros-noetic-desktop-full
```

3. Add the ROS environment variables to your bash session:

```
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
source ~/.bashrc
```

4. Install dependencies for building ROS packages:
```
sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential
```

5. Initialize rosdep:

```
sudo rosdep init
rosdep update
```


## Usage

You can start using ROS Noetic by opening a terminal window and typing:
```
roscore
```

This will start the ROS master node.

To test your installation, you can run one of the ROS demo nodes:

```
rosrun turtlesim turtlesim_node
```
This will start the turtlesim_node, which displays a simple simulation of a turtle that you can control using ROS commands.


