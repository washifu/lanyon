---
layout: post
title: ROS Installation on Echidna
---

## Instructions for ROS Jade
[Install ROS from source](http://wiki.ros.org/jade/Installation/Source "ROS")
Bootstrap Dependencies to facilitate the download and management of ROS

Making sure to have buid tools like compiler, CMake, etc.
```
$ sudo pip install -U rosdep rosinstall_generator wstool rosinstall
```
```
$ sudo pip install --upgrade setuptools
```
 Initialize rosdep
```
$ sudo rosdep init
$ rosdep update
```

Installing core ROS packages
Create a catkin workspace
```
mkdir ~/ros_catkin_ws
cd ~/ros_catkin_ws
```
Desktop-Full Install: ROS, rqt, rviz, robot-generic libraries, 2D/3D simulators, navigation and 2D/3D perception
```
rosinstall_generator desktop_full --rosdistro jade --deps --wet-only --tar > jade-desktop-full-wet.rosinstall
wstool init -j8 src jade-desktop-full-wet.rosinstall
```
Making sure to have all the required dependencies
```
$ rosdep install --from-paths src --ignore-src --rosdistro jade -y
```
ERROR
```
Reading state information... Done
E: Unable to locate package ros-jade-rviz
ERROR: the following rosdeps failed to install
  apt: command [sudo -H apt-get install -y ros-jade-rviz] failed
```
Build the catkin workspace
Invoke catkin_make_isolated
```
$ ./src/catkin/bin/catkin_make_isolated --install -DCMAKE_BUILD_TYPE=Release
```
ERROR
```
==> Processing catkin package: 'catkin'
==> cmake /home/wasif/ros_catkin_ws/src/catkin -DCATKIN_DEVEL_PREFIX=/home/wasif/ros_catkin_ws/devel_isolated/catkin -DCMAKE_INSTALL_PREFIX=/home/wasif/ros_catkin_ws/install_isolated -DCMAKE_BUILD_TYPE=Release -G Unix Makefiles in '/home/wasif/ros_catkin_ws/build_isolated/catkin'
-- Using CATKIN_DEVEL_PREFIX: /home/wasif/ros_catkin_ws/devel_isolated/catkin
-- Using CMAKE_PREFIX_PATH: 
-- Using PYTHON_EXECUTABLE: /usr/bin/python
-- Using Debian Python package layout
-- Could NOT find PY_em (missing:  PY_EM) 
CMake Error at cmake/empy.cmake:29 (message):
  Unable to find either executable 'empy' or Python module 'em'...  try
  installing the package 'python-empy'
Call Stack (most recent call first):
  cmake/all.cmake:147 (include)
  CMakeLists.txt:8 (include)


-- Configuring incomplete, errors occurred!
See also "/home/wasif/ros_catkin_ws/build_isolated/catkin/CMakeFiles/CMakeOutput.log".
<== Failed to process package 'catkin': 
  Command '['cmake', '/home/wasif/ros_catkin_ws/src/catkin', '-DCATKIN_DEVEL_PREFIX=/home/wasif/ros_catkin_ws/devel_isolated/catkin', '-DCMAKE_INSTALL_PREFIX=/home/wasif/ros_catkin_ws/install_isolated', '-DCMAKE_BUILD_TYPE=Release', '-G', 'Unix Makefiles']' returned non-zero exit status 1

Reproduce this error by running:
==> cd /home/wasif/ros_catkin_ws/build_isolated/catkin && cmake /home/wasif/ros_catkin_ws/src/catkin -DCATKIN_DEVEL_PREFIX=/home/wasif/ros_catkin_ws/devel_isolated/catkin -DCMAKE_INSTALL_PREFIX=/home/wasif/ros_catkin_ws/install_isolated -DCMAKE_BUILD_TYPE=Release -G 'Unix Makefiles'

Command failed, exiting.
```
Resolve error by installing python-empy
```
$ sudo apt-get install python-empy
```
ERROR
```
CMake Error at CMakeLists.txt:6 (find_package):
  By not providing "Findconsole_bridge.cmake" in CMAKE_MODULE_PATH this
  project has asked CMake to find a package configuration file provided by
  "console_bridge", but CMake did not find one.

  Could not find a package configuration file provided by "console_bridge"
  with any of the following names:

    console_bridgeConfig.cmake
    console_bridge-config.cmake

  Add the installation prefix of "console_bridge" to CMAKE_PREFIX_PATH or set
  "console_bridge_DIR" to a directory containing one of the above files.  If
  "console_bridge" provides a separate development package or SDK, be sure it
  has been installed.


-- Configuring incomplete, errors occurred!
See also "/home/wasif/ros_catkin_ws/build_isolated/class_loader/CMakeFiles/CMakeOutput.log".
See also "/home/wasif/ros_catkin_ws/build_isolated/class_loader/CMakeFiles/CMakeError.log".
<== Failed to process package 'class_loader': 
  Command '['/home/wasif/ros_catkin_ws/install_isolated/env.sh', 'cmake', '/home/wasif/ros_catkin_ws/src/class_loader', '-DCATKIN_DEVEL_PREFIX=/home/wasif/ros_catkin_ws/devel_isolated/class_loader', '-DCMAKE_INSTALL_PREFIX=/home/wasif/ros_catkin_ws/install_isolated', '-DCMAKE_BUILD_TYPE=Release', '-G', 'Unix Makefiles']' returned non-zero exit status 1

Reproduce this error by running:
==> cd /home/wasif/ros_catkin_ws/build_isolated/class_loader && /home/wasif/ros_catkin_ws/install_isolated/env.sh cmake /home/wasif/ros_catkin_ws/src/class_loader -DCATKIN_DEVEL_PREFIX=/home/wasif/ros_catkin_ws/devel_isolated/class_loader -DCMAKE_INSTALL_PREFIX=/home/wasif/ros_catkin_ws/install_isolated -DCMAKE_BUILD_TYPE=Release -G 'Unix Makefiles'

Command failed, exiting.
```
Resolve error by installing python-nose
```
sudo apt-get install python-nose
```
The "console_bridge" error persists. I am at a loss here.
