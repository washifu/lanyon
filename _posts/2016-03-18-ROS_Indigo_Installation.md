---
layout: post
title: ROS Indigo Installation
---

Bad News: ROS [velodyne stack](http://wiki.ros.org/velodyne "ROS") is only supported in indigo and not yet in jade (likely this will change) <br>
So, here is the ROS Indigo Install. It's fairly straight forward and much like the jade install but with fewer steps. <br>
Note that with two ROS distros, sourcing the setup.bash should be done manually when using each distro.

Bootstrap dependencies and rosdep has already been installed.

Make a new directory for Indigo. 

```
$ mkdir ~/ros_catkin_ws_indigo
$ cd ~/ros_catkin_ws_indigo
```

Desktop-Full Install

```
$ rosinstall_generator desktop_full --rosdistro indigo --deps --wet-only --tar > indigo-desktop-full-wet.rosinstall
$ wstool init -j8 src indigo-desktop-full-wet.rosinstall
```

