# AI_Robotics_Turtlebot3_Task2

**Turtlebot3_Task2**

**1- PC-SetUp**

**First I Installed Dependent ROS 1 Packages using the following code**

$ sudo apt-get install ros-melodic-joy ros-melodic-teleop-twist-joy \
  ros-melodic-teleop-twist-keyboard ros-melodic-laser-proc \
  ros-melodic-rgbd-launch ros-melodic-depthimage-to-laserscan \
  ros-melodic-rosserial-arduino ros-melodic-rosserial-python \
  ros-melodic-rosserial-server ros-melodic-rosserial-client \
  ros-melodic-rosserial-msgs ros-melodic-amcl ros-melodic-map-server \
  ros-melodic-move-base ros-melodic-urdf ros-melodic-xacro \
  ros-melodic-compressed-image-transport ros-melodic-rqt* \
  ros-melodic-gmapping ros-melodic-navigation ros-melodic-interactive-markers

**Then I Installed the TurtleBot3 Packages**

$ sudo apt-get install ros-melodic-dynamixel-sdk
$ sudo apt-get install ros-melodic-turtlebot3-msgs
$ sudo apt-get install ros-melodic-turtlebot3

**I chose the robot waffle_pi**

$ echo "export TURTLEBOT3_MODEL=waffle_pi" >> ~/.bashrc


**2- Gazebo Simulation**

**First Install Simulation Package**

$ cd ~/catkin_ws/src/
$ git clone -b melodic-devel https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
$ cd ~/catkin_ws && catkin_make

**Launch Simulation World for waffle_pi**

**New terminal**

$ export TURTLEBOT3_MODEL=waffle_pi
$ roslaunch turtlebot3_gazebo turtlebot3_world.launch

**Operate TurtleBot3**

$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch


**3- SLAM Simulation**

**Launch Simulation World**

**New terminal**

$ export TURTLEBOT3_MODEL=waffle_pi
$ roslaunch turtlebot3_gazebo turtlebot3_world.launch

**Run SLAM Node**
**New terminal**

$ export TURTLEBOT3_MODEL=waffle_pi
$ roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping

**Run Teleoperation Node**
**New terminal**

$ export TURTLEBOT3_MODEL=waffle_pi
$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch

**After I Run the codes i can finally move my robot waffle_pi while the sensor is exploring the maze"room".**

**Lastly I saved the map using the following code**
**New terminal**

$ rosrun map_server map_saver -f ~/map

**Note:please check the uploaded documents **

**Thank you for reading :)!**
