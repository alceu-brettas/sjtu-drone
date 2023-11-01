# About sjtu_drone #
sjtu_drone is a quadrotor simulation program forked from ['tum_simulator'] (http://wiki.ros.org/tum_simulator) , which is developed with ROS + Gazebo. It is used for testing visual SLAM algorithms aiding with different sensors, such as IMU, sonar range finder and laser range finder. Here by 'sjtu', it means Shanghai Jiao Tong University. Currently, this program is used for testing algorithms for [UAV contest in SJTU](http://mediasoc.sjtu.edu.cn/wordpress)

This repository is just a adapatation of the original SJTU Drone for Noetic. All Credits for [Original Repositories](https://github.com/tahsinkose/sjtu-drone)

# Requirements #
This package is compatible with ROS Noetic version (Ubuntu 20.04). Existing versions on the internet support at most until Gazebo 11.

# Download and Compiling #
```
$ cd <catkin_ws>/src
$ git clone https://github.com/alceu-brettas/sjtu-drone.git
$ cd <catkin_ws>
$ catkin_make
```

Here <catkin_ws> is the path of the catkin workspace. Please refer to the [tutorial](http://wiki.ros.org/ROS/Tutorials) about how to create a catkin workspace in ROS.

# Run
The simplest way is calling after you have built the workspace successfully.

```
$ cd <where you check out the code>
$ source devel/setup.bash
$ roslaunch sjtu-drone sjtu.launch
```
# Running with keyboard
In second terminal, if the controller don't open:

```
$ rosrun sjtu-drone drone_keyboard
```

```
$ roslaunch sjtu-drone sjtu.launch
```


# Read sensor data from ROS topics #
One can use [rqt_gui](http://wiki.ros.org/rqt_gui) to have an extensive amount of utilities for topic visualization and manipulation. Some of the useful topics reside below.
```
forward looking camera :  /drone/front_camera/image_raw
downward looking camera: /drone/down_camera/image_raw
sonar data:  /drone/sonar
laser range data: /drone/laser
```
