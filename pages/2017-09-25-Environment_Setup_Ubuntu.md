---
layout: page
title: Environment Setup
---

# Environment Setup  
  
Install Ubuntu 16.04.3 (Any Ubuntu 14.04+ should be fine)
  
### Get The Basics
```
sudo apt-get install git g++ cmake cmake-curses-gui
```
  
My apt-get also installed the following additional packages  
`cmake-data git-man liberror-perl libjsoncpp1`  

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

#### Boost
```
sudo apt-get install libboost-all-dev
```

Boost Additional Packages:  
```autotools-dev icu-devtools libboost-all-dev libboost-atomic-dev libboost-atomic1.58-dev libboost-atomic1.58.0 libboost-chrono-dev libboost-chrono1.58-dev libboost-chrono1.58.0 libboost-context-dev libboost-context1.58-dev libboost-context1.58.0 libboost-coroutine-dev libboost-coroutine1.58-dev libboost-coroutine1.58.0 libboost-date-time-dev libboost-date-time1.58-dev libboost-dev libboost-exception-dev bboost-exception1.58-dev libboost-filesystem-dev libboost-filesystem1.58-dev libboost-graph-dev libboost-graph-parallel-dev libboost-graph1.58.0 libboost-iostreams-dev libboost-iostreams1.58-dev libboost-locale-dev libboost-locale1.58-dev libboost-locale1.58.0 libboost-log-dev libboost-log1.58-dev libboost-log1.58.0 libboost-math-dev libboost-math1.58-dev libboost-math1.58.0 libboost-mpi-dev libboost-mpi-python-dev libboost-mpi-python1.58-dev libboost-mpi-python1.58.0 libboost-mpi1.58-dev libboost-mpi1.58.0 libboost-program-options-dev libboost-program-options1.58-dev libboost-program-options1.58.0 libboost-python-dev libboost-python1.58-dev libboost-python1.58.0 libboost-random-dev libboost-random1.58-dev libboost-random1.58.0 libboost-regex-dev libboost-regex1.58-dev libboost-regex1.58.0 libboost-serialization-dev libboost-serialization1.58-dev libboost-serialization1.58.0 libboost-signals-dev libboost-signals1.58-dev libboost-signals1.58.0 libboost-system-dev libboost-system1.58-dev libboost-test-dev libboost-test1.58-dev libboost-test1.58.0 libboost-thread-dev libboost-thread1.58-dev libboost-thread1.58.0 libboost-timer-dev libboost-timer1.58-dev libboost-timer1.58.0 libboost-tools-dev libboost-wave-dev libboost-wave1.58-dev libboost-wave1.58.0 libboost1.58-dev libboost1.58-tools-dev libexpat1-dev libhwloc-dev libhwloc-plugins libhwloc5 libibverbs-dev libibverbs1 libicu-dev libltdl-dev libnuma-dev libopenmpi-dev libopenmpi1.10 libpython-dev libpython2.7-dev libtool mpi-default-bin mpi-default-dev ocl-icd-libopencl1 openmpi-bin openmpi-common python-dev python2.7-dev```

#### Eigen
```
sudo apt-get install libeigen3-dev
```

#### FLANN
```
sudo apt-get install libflann-dev libflann1.8
```

### Point Cloud Library  
Clone the pcl git repo
```
git clone https://github.com/PointCloudLibrary/pcl.git
```
Create a build directory and compile PCL
```
cd pcl
mkdir build && cd build
ccmake ..
```
Configure the cmake file and set the following options:


Go get some coffee and check your email.


