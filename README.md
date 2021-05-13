# Line-Follower

# Introduction
This project uses ROS to simulate a line-following Turtlebot robot in the Gazebo environment using a world designed by the authors.

# Setting up the Gazebo
To build the Gazebo world:

 - First, in a terminal, cloning the repository.
```
cd
git clone https://github.com/LuisC2802/Line-Follower.git
```
 - Add the models.tar.gz to the directory .gazebo/models and extract the tar.gz file.
 ```
cd
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
mv FinalHouse.world /usr/share/gazebo-7/worlds
```
# Setting up the .launch file
Now, you should move the FinalHouse.launch to the gazebo directory:
```
mv FinalHouse.launch /opt/ros/kinetic/share/gazebo_ros/launch
