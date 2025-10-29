# TurtleBot3
First, we copy the required commands from the TurtleBot3 website, specifically from the Quick Start Guide section, as follows:
$sudo apt install ros-humble-gazebo-*
$sudo apt install ros-humble-cartographer
$ sudo apt install ros-humble-cartographer-ros
sudo apt install ros-humble-navigation2
$ sudo apt install ros-humble-nav2-bringup
source /opt/ros/humble/setup.bash
$ mkdir -p ~/turtlebot3_ws/src
$ cd ~/turtlebot3_ws/src/
$ git clone -b humble https://github.com/ROBOTIS-GIT/DynamixelSDK.git
$ git clone -b humble https://github.com/ROBOTIS-GIT/turtlebot3_msgs.git
$ git clone -b humble https://github.com/ROBOTIS-GIT/turtlebot3.git
$ sudo apt install python3-colcon-common-extensions
$ cd ~/turtlebot3_ws
$ colcon build --symlink-install
$ echo 'source ~/turtlebot3_ws/install/setup.bash' >> ~/.bashrc
$ source ~/.bashrc
Then, from the Simulation section, we select SLAM Simulation.
$export TURTLEBOT3_MODEL=burger
$ ros2 launch turtlebot3_gazebo turtlebot3_world.launch.py
$export TURTLEBOT3_MODEL=burger
$ ros2 launch turtlebot3_cartographer cartographer.launch.py use_sim_time:=True
$export TURTLEBOT3_MODEL=burger
$ ros2 run turtlebot3_teleop teleop_keyboard
$ros2 run nav2_map_server map_saver_cli -f ~/map
