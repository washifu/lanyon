---
layout: post
title: Fix Shadows [DONE~]
---

When the openni_grabber demo is run with any VLP-16 data set, two (or more) copies of all the points appear above/below the first set of points. The points are not vertical translations but appear to be angular translations from the LiDAR origin.

It seems that the openni\_grabber demo is designed for HDL-32 data sets as described in [The Velodyne High Definition LiDAR HDL Grabber](http://pointclouds.org/documentation/tutorials/hdl_grabber.php#hdl-grabber "PCL: HDL Grabber") page by PCL.

All the data sets I've collected with the Velodyne VLP-16 have these shadows as do the sample data sets Leo has left behind. <br>
I ran some HDL-32 sample data sets and confirmed no occurence of these shadows, so it seems that the program is calibrated for the HDL-32 and not the VLP-16.

-There doesn't seem to be a calibration file for VLP-16 but- PCL does actually have a *vlp_viewer.cpp* and *vlp_grabber.cpp* in the library.
I have found the VLP-16 and HDL-32 calibration files thanks to Tsukasa Sugiura's comment on his video of [Drawing VLP-16 Data using PCL](https://www.youtube.com/watch?v=7BUFxkyH1r0 "YouTube Video").

*vlp_viewer* <br>
> io/src/vlp_viewer.cpp

*vlp_grabber* <br>
> visualization/tools/vlp_grabber.cpp

### Next Step: 
  * Compile these files. 
  * -If too hasslesome, try to make the HDL Grabber compatible with VLP-16.- [DONE]
  * I am still curious about the other programs, but will leave compiling those as secondary tasks.
