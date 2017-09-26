---
layout: page
title: Install PCL on wasif in Echidna FULL
---

# Environment Setup  
  
Install Ubuntu 16.04.3 (Any Ubuntu 14.04+ should be fine)
  
### Get The Basics
> sudo apt-get install git g++ cmake cmake-curses-gui  
My apt-get also installed the following additional packages  
`cmake cmake-curses-gui cmake-data git git-man liberror-perl libjsoncpp1`  

### Dependencies
This is the struggle. Best of luck.  
You essentially need the following dependencies:
+ boost
+ eigen
+ flann
+ libusb
+ openni
+ qhull
+ vtk-qt
> sudo apt-get install 

### Point Cloud Library  
Clone the pcl git repo
> git clone https://github.com/PointCloudLibrary/pcl.git  
Create a build directory and compile PCL
```
cd pcl
mkdir build && cd build
ccmake ..
```
Configure the cmake file and set the following options:


Go get some coffee and check your email.


