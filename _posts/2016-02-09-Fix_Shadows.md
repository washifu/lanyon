---
layout: post
title: Fix Shadows
---

When the openni_grabber demo is run with any VLP-16 data set, there appears 2 more copies of all the points below the first set of points. 
The points are not vertical translations but appear to be angular translations from the LiDAR origin.
It seems that the openni\_grabber demo is designed for HDL-32 data sets as described on [The Velodyne High Definition LiDAR HDL Grabber](http://pointclouds.org/documentation/tutorials/hdl_grabber.php#hdl-grabber "PCL: HDL Grabber") page by PCL.

I ran some HDL-32 sample data sets and confirmed no occurence of these shadows.
All the data sets I've collected with the Velodyne VLP-16 have these shadows as do the sample data sets Leo has left behind.

There doesn't seem to be a calibration file for VLP-16 but PCL does actually have a *vlp_viewer.cpp* and *vlp_grabber.cpp* in the library.
*vlp_viewer* 
> io/src/vlp_viewer.cpp
*vlp_grabber* 
> visualization/tools/vlp_grabber.cpp

Next Step: Compile these files. If too hasslesome, try to make the HDL Grabber compatible with VLP-16.
