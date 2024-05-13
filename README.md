# Puzzlebot --> LiDAR-Problem

# Explanation
* The Problem is that the Jetson Nano Board cant get Data from the conected LiDAR-Sensor. If connected and used trough ros2 with the Standard LiDAR-Node we get the Errors: TIMEOUT or Healthcode 80008002.
    * ros2 launch rplidar_ros rplidar_a1_launch.py serial_baudrate:=115200
    * also tried various baudrates and options we can set trough the launch file
* We also tested the LiDAR trough the node/Implementation from SLAMTEC (the business creating the Sensor) --> same Error
    * https://github.com/Slamtec/sllidar_ros2
* When tested with Robostudio from SLAMTEC the LiDAR works on MACOS, Windows and a Ubuntu-Environment we setup
* The LiDAR also works and starts with the Node, which doesnt work on the Jetson Nano, when used in the Ubuntu-Environment
* We also tried a second Robot to test if the Board has problems but still the same Error.
* --> It works everwhere except on the Jetson Nano 

## Tested Hardware

* Various cabel and power supply units (also a 15W one)
* Various USB Ports
    * We always see that the Sensor is connected (for example to ttyUSB0)
* Various Robots
    * Same configuration (Standard, only used what we got from Manchester to flash)
    * Two Jetson Nano Board
    * Two LiDAR Sensor

## Links --> various Sollutions we tried

* https://github.com/Slamtec/sllidar_ros2
* https://wiki.hshl.de/wiki/index.php/RPLidar_with_ROS2_and_RVIZ
* https://github.com/babakhani/rplidar_ros2
* https://articulatedrobotics.xyz/tutorials/mobile-robot/hardware/lidar/#installing-the-driver

## Annex

* Various Pictures and Videos we took, while doing the tests
   * Error_Message_Timeout.jpeg --> Timeout Error-Message
   * Error_Message_Healthcode.jpeg --> Healthcode 80008002 Error-Message
   * LiDAR_on_rviz_own_ubuntu_env.jpeg --> working LiDAR and node inside own Ubuntu Environment (not Jetson Nano)
   * LiDAR-Data_inside_Robostudio.jpeg --> working LiDAR inside Robostudio (Software from SLAMTEC)
   * Video-LiDAR_inside_own_ubuntu_env.mp4 --> Video of the working LiDAR inside own Ubuntu Environment (not Jetson Nano) 
