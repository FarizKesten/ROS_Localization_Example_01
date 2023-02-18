# ROS Kalman Filters

## Using the library:

```
set turtlebot type: 
export TURTLEBOT3_MODEL=burger

# fetch submodule
apt-get update
apt-get upgrade -y

git submodule update --init

catkin_make
source devel/setup.bash

# in case not installed yet:
rosdep -i install turtlebot3_gazebo
catkin_make
source devel/setup.bash

# launch turtlebot3 simulation in gazebo
roslaunch turtlebot3_gazebo turtlebot3_world.launch

# control turtlebot3 motion via keyboard
launch turtlebot3_teleop turtlebot3_teleop_key.launch

```
### Running rviz:

```
rosrun rviz rviz

```


## Troubleshooting:

- gazebo can't be opened:
Could be that the X11 is not set correctly:
```
xhost local:root
xhost +local:docker
docker exec -it <container name> /bin/bash
```

## TODO:

- Continue from: Rviz package 19.02.23)
