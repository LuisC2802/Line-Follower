# Line-Follower

# Introduction
This project uses ROS to simulate a line-following Turtlebot robot in the Gazebo environment using a world designed by the authors.

# Creating a work space
To build the project run the following steps in a terminal:
- Creating a catkin workspace:
```
mkdir catkin_ws
cd catkin_ws
mkdir src
catkin_make
```
- Cloning the repository.
```
cd ~/catkin_ws/src
git clone https://github.com/LuisC2802/Line-Follower.git
```

# Setting up the Gazebo
To build the Gazebo world:
 - Add the models.tar.gz to the directory .gazebo/models and extract the tar.gz file.
 ```
cd ~/catkin_ws/src
mv models.tar.gz .gazebo/models
cd .gazebo/models
tar --extract --file models.tar.gz
```
 To validate the correct process, in a terminal, start Gazebo
```
gazebo
```
 You should see in Insert /home/user/.gazebo/models, the current directories in the tar.gz file (Bed, Bathroom, stove).
 
# Setting up the .world file
Now, you should move the FinalHouse.world to the gazebo directory:
```
cd ~/catkin_ws/src
mv FinalHouse.world /usr/share/gazebo-7/worlds
```
# Setting up the .launch file
Now, you should move the FinalHouse.launch to the gazebo directory:
```
~/catkin_ws/src
mv FinalHouse.launch /opt/ros/kinetic/share/gazebo_ros/launch
```
# Run the world launch
To validate the correct set up of the world, run the world launch in the Gazebo.
```
cd
roslaunch gazebo_ros FinalHouse.launch
```
# To run
To run the project and see the output in the gazebo world , execute the following steps:
```
cd ~/catkin_ws
catkin_make
source devel/setup.bash
roslaunch line_follower_turtlebot Lfmw.launch
```
