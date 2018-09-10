ros-course-exercise-1
======================

ROS course based on Programming for Robotics (http://www.rsl.ethz.ch/education-students/lectures/ros.html)

# Exercise 1

In order to solve the first exercise of this course, it is necessary to understand the .launch file which is located in your husky_gazebo/launch. 
The command line is:
```
$ roscd husky_gazebo/launch/

```

Create a new launch file:
```
$ gedit husky_empty_world2.launch

```

Instructions
------------
```
$ <launch>
$ <include file="$(find husky_gazebo)/launch/husky_empty_world.launch">
$    <arg name="world_name" value="worlds/robocup14_spl_field.world"/>
$  </include>
$ </launch>
```
### Now it is necessary to implement the teleop_keyboard_twist

In the same launch file created you need to add this command line in your script.

```
$ <node name="teleop_twist_keyboard" pkg="teleop_twist_keyboard" type="teleop_twist_keyboard.py" output="screen">
$  </node>
```  
### Execute the modified launch file and done!

In my case: ``` $ roslaunch husky_gazebo husky_empty_world2.launch ```