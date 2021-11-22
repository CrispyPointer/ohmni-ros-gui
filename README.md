# ohmni-ros-gui
 # ohmni-ros-gui
# **The required packages to build the control GUI for Ohmnibot**

These packages alow us to perfrom certain tasks on OHmnibot:

## Prequisite setting:

**#mounting a directory inside the Ohmnibot ROS docker environment**
```
In bot cli> docker run -it --network host --privileged -v /data/data/com.ohmnilabs.telebot_rtc/files:/app -v /dev:/dev -e ROS_IP=[bot_ip] [tb_control_docker_image]
```
**#Create the ohmni_ws directory to contain the developing source code.**

Clone the rplidar_ros package inside the ohmni_ws/src directory and run catkin_make to build the package.

Note: 

The Lidar port might changes when we restart the bot so follow this step to redirect the port:
```
Ohmni_ws> cd src/rplidar_ros/launch
```
Using vim to edit the file rplidar.launch - Change the serial port value accordingly (Usually /dev/ttyUSB0 or /dev/ttyUSB1)

1. Using RPLidar to map the working environment and perform SLAM on Ohmnibot.



2. Building a websocket API to connect the Ohmni's ROS topics with other webAPIs by using Rosbridge.



