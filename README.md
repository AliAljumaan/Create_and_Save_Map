# Create_and_Save_Map
As part of the project, it will be necessary to provide the robot with a sense of its surroundings and the space around it. With the Turtulebot3, the robot can create a map of the surroundings as it moves. This requires the installation of ross and gazebo; if not, you may refer to the instructions [here](https://github.com/AliAljumaan/Ross_Installation) for setting up ros and [here](https://classic.gazebosim.org/tutorials?tut=ros_installing&cat=connect_ros) for setting up the gazebo.
## Turtlebot3 installation
Open a terminal window and install the dependent packages. Enter the following commands, one right after the other:

```
cd ~/catkin_ws/src/
```

```
git clone https://github.com/ROBOTIS-GIT/turtlebot3_msgs.git
```

```
git clone https://github.com/ROBOTIS-GIT/turtlebot3.git
```

```
cd ~/catkin_ws && catkin_make
```

Type this command to open the bashrc file to add the burger model.
```
gedit ~/.bashrc
```

Add this line at the bottom of the file:

```
export TURTLEBOT3_MODEL=burger
```

Now reload .bashrc so that you do not have to log out and log back in.

```
source ~/.bashrc
```

Now, we need to download the TurtleBot3 simulation files.

```
cd ~/catkin_ws/src/
```

```
git clone https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
```

```
cd ~/catkin_ws && catkin_make
```

## Simulate TurtleBot3 Using Gazebo
To use Gazebo to do the TurtleBot3 simulation Enter the following commands.

```
Simulate TurtleBot3 Using Gazebo
```

## Simulating SLAM With TurtleBot3
Install the SLAM module in a new terminal window.

```
sudo apt install ros-noetic-slam-gmapping
```

Start Gazebo in a new terminal window.

```
roslaunch turtlebot3_gazebo turtlebot3_world.launch

```
Start SLAM in a new terminal tab.

```
roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping

```
Start autonomous navigation in a new terminal tab:

```
roslaunch turtlebot3_gazebo turtlebot3_simulation.launch
```
![image](https://user-images.githubusercontent.com/108624020/183235256-b39de545-0bec-4842-a125-3a7ed9b375fd.png)
