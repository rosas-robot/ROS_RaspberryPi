# ROS_RaspberryPi
Installing ROS on Raspberry-Pi may sometimes be helpful when one would like to run mobile robot (PR2 or Amigobot) using Raspberry-Pi. By searching online I found a link in ROS-Wiki page, an **.img** file with preinstalled ROS Kinetic in Ubuntu MATE. One just have to download this image and burn it into a formatted SD card. The link where this image is available can be found at http://www.german-robot.com/German-Robot.Com-Image-Pi3-ROS-Kinetic-Ubuntu-Mate.img.zip and its documentation  at http://www.german-robot.com/2016/05/26/raspberry-pi-sd-card-image/.

Afetr burning this image in to SD card, we need to modify language and keyboard settings of Ubuntu MATE as those settings are advantageous for those who knows German language. Next we will talk about the process of changinf language and keyborad layout.

For language change follow, System -> Preferences -> Personal -> Language Support. However *language Support* may not be installed apriori, so I first installed it and then changed settings.

For *keyboard layout settings* change follow, Control center -> Hardware -> Keyboard -> Layout

# Installing ROSARIA
In order to run PR2 or Amigobot, one has to install **ROSARIA** package from Amor robots. Type in the following commands into a terminal to install ROSARIA.

```
# Move to catkin workspace
$ cd ~/catkin_ws/src

# Clone the repository
$ git clone http://github.com/amor-ros-pkg/

# Update ROS dependencies
$ rosdep update

# Install ROSARIA
$ rosdep install rosaria

# catkin_make the workspace
$ cd ~/catkin_ws/
$ catkin_make
```
