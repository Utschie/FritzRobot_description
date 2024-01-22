# Fritzrobot_description

## Description
Model files
##
### 2024-01-21 update
Enabled the movement in gazebo with [`gazebo_mecanum_plugins`](https://github.com/qaz9517532846/gazebo_mecanum_plugins).


Simulated the LIDAR in gazebo with [`robosense_simulator`](https://github.com/tomlogan501/robosense_simulator) and [`velodyne_gazebo_plugins`](https://wiki.ros.org/velodyne_gazebo_plugins).

**Notice：**

*The meaning of **collision_range** is how far the laser will be blocked at the nearest distance, which must be larger than the radius of the LIDAR, because the laser is emitted from the center of the LIDAR's body, so if the **collision_range** is smaller than the radius of the LIDAR, then the laser will be blocked by the LIDAR‘s shell.* 

*Also the **collision_range** should preferably not be set too large (preferably not the default value of 0.3m), if the value is set too large then gazebo will not be able to simulate the scenario where the LIDAR is occluded in front of its eyes. For example, in this simulation, the two LIDARs are occluded from each other, which should result in part of the field of view being missing.*

*The ideal value of **collision_range** is just a bit bigger than LIDAR'S radius*

The simulation shown below

https://github.com/Utschie/FritzRobot_description/assets/33782458/288423f4-e0bd-438e-a80e-16457b35217d

### 2023-12-26 update
modified the models in gazebo and rviz, fixed the issue of the joint_state_publisher through changed python to v3.8
![avatar](./pictures/gazebo&rviz.png)
### 2023-12-22 update

modified the models based on wheeltec's models. 

changed the types of wheel_shaft_joints and wheel_roll_joints because the joint_state_pulisher can't start(don't know why), so that the continous joint can't be transformed. 
