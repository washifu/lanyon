---
layout: page
title: Install PCL on macOS
---

### Install PCL ###

[Point Cloud Library's Mac Installation Page](http://pointclouds.org/downloads/macosx.html)

I installed with [Homebrew](http://www.pointclouds.org/documentation/tutorials/installing_homebrew.php):

Prepare Homebrew (if you have not already):

```
brew update
brew tap homebrew/science
```

Install PCL with Homebrew:

```
brew install pcl --with-examples --with-openni --with-openni2 --with-qt5 --with-surface_on_nurbs
```

#### Edit:  
Options `--with-qt5` and `--with-surface_on_nurbs` no longer exist.  
I believe these are now included by default. Also, for me, `--with-openni` and `--with-openni2` no longer work.
Perhaps due to Apple buying OpenNI. In anycase, openni and openni2 are still available in homebrew.
So, technically, these dependency libraries can still be downloaded.  
  
To resolve the installation, install the following dependencies with homebrew (if you don't have them already):
```
brew install cmake pkg-config boost cminpack eigen flann glew libusb qhull vtk openni openni2
```  
  
Then git clone [https://github.com/PointCloudLibrary/pcl](https://github.com/PointCloudLibrary/pcl).  
Build pcl from source:
```
cd pcl
mkdir build && cd build
```
Then you need to enable build with openni and openni2 (since you have these already, it should work fine).
```
ccmake ..
```
Enable `BUILD_examples`, `WITH_OPENNI`, `WITH_OPENNI2` and anything else you want.
Hit `c` to configure, then `g` to build and quit ccmake.  
Finally:
```
cmake ..
make -j8
```
  
Now you will have a working version of PCL. You can make install PCL so CMake can be used to simply find_package
and you can build stand alone PCL dependent programs with CMake.

```
make install -j8
```

Yay~
