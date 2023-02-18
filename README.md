# ROS Kalman Filters

## Using the library:

```
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

roslaunch turtlebot3_gazebo turtlebot3_world.launch
```

## Troubleshooting:

- gazebo can't be opened:
Could be that the X11 is not set correctly:
```
xhost local:root
xhost +local:docker
docker exec -it <container name> /bin/bash
```

