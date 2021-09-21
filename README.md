# Mappin-and-SLAM

![alt text](src/sc2.png)

### Dependencies:
#### - RTAB-Map ROS
This package is a ROS wrapper of RTAB-Map (Real-Time Appearance-Based Mapping), a RGB-D SLAM approach based on a global loop closure detector with real-time constraints.

`sudo apt install ros-melodic-rtabmap-ros`

#### - Teleop package
Generic keyboard teleop for twist robots.

`sudo apt install ros-melodic-teleop-twist-keyboard`

### Project build instrctions:
1. Clone this repo inside the `src` folder of a catkin workspace, make sure that you are cloning the saved map as Git LFS file, too:
`https://github.com/Prat33k-dev/Mappin-and-SLAM.git`
2. Build workspace: `catkin_make`
3. Source environment: `source devel/setup.bash` 
4. Start the Gazebo simulation: `roslaunch my_robot world.launch`
5. Start the RTAB-Map SLAM and the visualizer package: `roslaunch my_robot mapping.launch`

### Launching the project
After successfully start the simulation, mapping and teleop packages you should see the following graph after executing `rqt_graph`:
And the following TF tree after executing `rosrun rqt_tf_tree rqt_tf_tree`:

### Mapping
1) After manually driving the robot through the environment we can visualize the map (2D occupancy grid) of the environment and even the robot's path.
2) In the visualizer tool of RTAB-Map we can see the RGBD pointcloud of the environment.
