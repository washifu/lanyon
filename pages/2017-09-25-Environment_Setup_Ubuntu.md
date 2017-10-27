---
layout: page
title: Code Environment Setup
comments: true
---

Install [Ubuntu](https://www.ubuntu.com/download/desktop) 16.04.3 (Any Ubuntu 12+ should be fine)  
  
### Get The Basics  
```
sudo apt-get install git g++ cmake cmake-curses-gui
```  
  
My apt-get also installed the following additional packages:  
`cmake-data git-man liberror-perl libjsoncpp1`  
  
### Dependencies  
This thesis is built using the Point Cloud Library.  
+ PCL  
  
### PCL Dependencies  
Sadly, PCL has a ton of dependencies, so cancel your next meeting and get comfortable.  
+ Boost
+ Eigen
+ FLANN
+ VTK-Qt
+ QHull
+ OpenNI OpenNI2
  
### More PCL Dependencies  
+ pcap
+ GL GLUT GLEW Xmu Xi
+ Open MPI 
+ LibUSB
+ Phonon
+ PROJ  
  
### OpenNI Dependencies  
+ Doxygen
+ LibUSB 1.0
+ Graphviz
+ Mono
+ Java (openjdk)
  
### OpenNI2 Dependencies  
+ LibUDEV  
  
+ libqt-opengl-dev qt-sdk
+ libgtest-dev mono-complete
+ libsuitesparse-dev  
  
  
### OpenNI and OpenNI2 Dependencies  
#### Doxygen LibUSB 1.0 Graphviz LibUDEV  
```
sudo apt-get install doxygen libusb-1.0-0-dev graphviz libudev-dev
```  
Additional Packages:  
`libclang1-3.6 libllvm3.6v5 libobjc-5-dev libobjc4 libusb-1.0-doc libcdt5 libcgraph6 libgvc6 libgvpr2 libpathplan4`  
  
#### Mono  
```
sudo apt-get install mono-complete
```  
Mono Additional Packages:  
`binfmt-support ca-certificates-mono cli-common libgdiplus libglade2-0 libglade2.0-cil libglib2.0-cil libgtk2.0-cil libjavascriptcoregtk-1.0-0 libmono-2.0-1 libmono-2.0-dev libmono-accessibility4.0-cil libmono-c5-1.1-cil libmono-cairo4.0-cil libmono-cecil-private-cil libmono-cil-dev libmono-codecontracts4.0-cil libmono-compilerservices-symbolwriter4.0-cil libmono-corlib4.5-cil libmono-cscompmgd0.0-cil libmono-csharp4.0c-cil libmono-custommarshalers4.0-cil libmono-data-tds4.0-cil libmono-db2-1.0-cil libmono-debugger-soft4.0a-cil libmono-http4.0-cil libmono-i18n-cjk4.0-cil libmono-i18n-mideast4.0-cil libmono-i18n-other4.0-cil libmono-i18n-rare4.0-cil libmono-i18n-west4.0-cil libmono-i18n4.0-all libmono-i18n4.0-cil libmono-ldap4.0-cil libmono-management4.0-cil libmono-messaging-rabbitmq4.0-cil libmono-messaging4.0-cil libmono-microsoft-build-engine4.0-cil libmono-microsoft-build-framework4.0-cil libmono-microsoft-build-tasks-v4.0-4.0-cil libmono-microsoft-build-utilities-v4.0-4.0-cil libmono-microsoft-build4.0-cil libmono-microsoft-csharp4.0-cil libmono-microsoft-visualc10.0-cil libmono-microsoft-web-infrastructure1.0-cil libmono-oracle4.0-cil libmono-parallel4.0-cil libmono-peapi4.0a-cil libmono-posix4.0-cil libmono-profiler libmono-rabbitmq4.0-cil libmono-relaxng4.0-cil libmono-security4.0-cil libmono-sharpzip4.84-cil libmono-simd4.0-cil libmono-smdiagnostics0.0-cil libmono-sqlite4.0-cil libmono-system-componentmodel-composition4.0-cil libmono-system-componentmodel-dataannotations4.0-cil libmono-system-configuration-install4.0-cil libmono-system-configuration4.0-cil libmono-system-core4.0-cil libmono-system-data-datasetextensions4.0-cil libmono-system-data-entity4.0-cil libmono-system-data-linq4.0-cil libmono-system-data-services-client4.0-cil libmono-system-data-services4.0-cil libmono-system-data4.0-cil libmono-system-design4.0-cil libmono-system-drawing-design4.0-cil libmono-system-drawing4.0-cil libmono-system-dynamic4.0-cil libmono-system-enterpriseservices4.0-cil libmono-system-identitymodel-selectors4.0-cil libmono-system-identitymodel4.0-cil libmono-system-io-compression-filesystem4.0-cil libmono-system-io-compression4.0-cil libmono-system-json-microsoft4.0-cil libmono-system-json4.0-cil libmono-system-ldap-protocols4.0-cil libmono-system-ldap4.0-cil libmono-system-management4.0-cil libmono-system-messaging4.0-cil libmono-system-net-http-formatting4.0-cil libmono-system-net-http-webrequest4.0-cil libmono-system-net-http4.0-cil libmono-system-net4.0-cil libmono-system-numerics4.0-cil libmono-system-reactive-core2.2-cil libmono-system-reactive-debugger2.2-cil libmono-system-reactive-experimental2.2-cil libmono-system-reactive-interfaces2.2-cil libmono-system-reactive-linq2.2-cil libmono-system-reactive-observable-aliases0.0-cil libmono-system-reactive-platformservices2.2-cil libmono-system-reactive-providers2.2-cil libmono-system-reactive-runtime-remoting2.2-cil libmono-system-reactive-windows-forms2.2-cil libmono-system-reactive-windows-threading2.2-cil libmono-system-runtime-caching4.0-cil libmono-system-runtime-durableinstancing4.0-cil libmono-system-runtime-serialization-formatters-soap4.0-cil libmono-system-runtime-serialization4.0-cil libmono-system-runtime4.0-cil libmono-system-security4.0-cil libmono-system-servicemodel-activation4.0-cil libmono-system-servicemodel-discovery4.0-cil libmono-system-servicemodel-internals0.0-cil libmono-system-servicemodel-routing4.0-cil libmono-system-servicemodel-web4.0-cil libmono-system-servicemodel4.0a-cil libmono-system-serviceprocess4.0-cil libmono-system-threading-tasks-dataflow4.0-cil libmono-system-transactions4.0-cil libmono-system-web-abstractions4.0-cil libmono-system-web-applicationservices4.0-cil libmono-system-web-dynamicdata4.0-cil libmono-system-web-extensions-design4.0-cil libmono-system-web-extensions4.0-cil libmono-system-web-http-selfhost4.0-cil libmono-system-web-http-webhost4.0-cil libmono-system-web-http4.0-cil libmono-system-web-mvc3.0-cil libmono-system-web-razor2.0-cil libmono-system-web-routing4.0-cil libmono-system-web-services4.0-cil libmono-system-web-webpages-deployment2.0-cil libmono-system-web-webpages-razor2.0-cil libmono-system-web-webpages2.0-cil libmono-system-web4.0-cil libmono-system-windows-forms-datavisualization4.0a-cil libmono-system-windows-forms4.0-cil libmono-system-windows4.0-cil libmono-system-xaml4.0-cil libmono-system-xml-linq4.0-cil libmono-system-xml-serialization4.0-cil libmono-system-xml4.0-cil libmono-system4.0-cil libmono-tasklets4.0-cil libmono-webbrowser4.0-cil libmono-webmatrix-data4.0-cil libmono-windowsbase4.0-cil libmono-xbuild-tasks4.0-cil libmonoboehm-2.0-1 libmonoboehm-2.0-dev libmonosgen-2.0-1 libnunit-cil-dev libnunit-console-runner2.6.3-cil libnunit-core-interfaces2.6.3-cil libnunit-core2.6.3-cil libnunit-framework2.6.3-cil libnunit-mocks2.6.3-cil libnunit-util2.6.3-cil libwebkit1.1-cil libwebkitgtk-1.0-0 libwebkitgtk-1.0-common mono-4.0-gac mono-4.0-service mono-complete mono-csharp-shell mono-devel mono-gac mono-jay mono-mcs mono-runtime mono-runtime-common mono-runtime-sgen mono-utils mono-xbuild monodoc-base monodoc-browser monodoc-manual`  
  
### PCL Dependencies  
#### Boost  
```
sudo apt-get install libboost-all-dev
```  
Boost Additional Packages:  
`autotools-dev icu-devtools libboost-all-dev libboost-atomic-dev libboost-atomic1.58-dev libboost-atomic1.58.0 libboost-chrono-dev libboost-chrono1.58-dev libboost-chrono1.58.0 libboost-context-dev libboost-context1.58-dev libboost-context1.58.0 libboost-coroutine-dev libboost-coroutine1.58-dev libboost-coroutine1.58.0 libboost-date-time-dev libboost-date-time1.58-dev libboost-dev libboost-exception-dev bboost-exception1.58-dev libboost-filesystem-dev libboost-filesystem1.58-dev libboost-graph-dev libboost-graph-parallel-dev libboost-graph1.58.0 libboost-iostreams-dev libboost-iostreams1.58-dev libboost-locale-dev libboost-locale1.58-dev libboost-locale1.58.0 libboost-log-dev libboost-log1.58-dev libboost-log1.58.0 libboost-math-dev libboost-math1.58-dev libboost-math1.58.0 libboost-mpi-dev libboost-mpi-python-dev libboost-mpi-python1.58-dev libboost-mpi-python1.58.0 libboost-mpi1.58-dev libboost-mpi1.58.0 libboost-program-options-dev libboost-program-options1.58-dev libboost-program-options1.58.0 libboost-python-dev libboost-python1.58-dev libboost-python1.58.0 libboost-random-dev libboost-random1.58-dev libboost-random1.58.0 libboost-regex-dev libboost-regex1.58-dev libboost-regex1.58.0 libboost-serialization-dev libboost-serialization1.58-dev libboost-serialization1.58.0 libboost-signals-dev libboost-signals1.58-dev libboost-signals1.58.0 libboost-system-dev libboost-system1.58-dev libboost-test-dev libboost-test1.58-dev libboost-test1.58.0 libboost-thread-dev libboost-thread1.58-dev libboost-thread1.58.0 libboost-timer-dev libboost-timer1.58-dev libboost-timer1.58.0 libboost-tools-dev libboost-wave-dev libboost-wave1.58-dev libboost-wave1.58.0 libboost1.58-dev libboost1.58-tools-dev libexpat1-dev libhwloc-dev libhwloc-plugins libhwloc5 libibverbs-dev libibverbs1 libicu-dev libltdl-dev libnuma-dev libopenmpi-dev libopenmpi1.10 libpython-dev libpython2.7-dev libtool mpi-default-bin mpi-default-dev ocl-icd-libopencl1 openmpi-bin openmpi-common python-dev python2.7-dev`  
  
#### Eigen  
```
sudo apt-get install libeigen3-dev
```    
  
#### FLANN  
```
sudo apt-get install libflann-dev
```  
FLANN Additional Packages:  
`libflann1.8`  
  
#### GL GLUT GLEW XMU XI  
```
sudo apt-get install freeglut3-dev libglew-dev libxmu-dev libxi-dev
```  
Additional Packages:  
`freeglut libxmu-headers`  
  
#### libpcap  
```
sudo apt-get install libpcap-dev
```  
libpcap Additional Packages:  
`libpcap0.8-dev`  
  
#### LibUSB  
```
sudo apt-get install libusb-dev
```  
  
#### PROJ  
```
sudo apt-get install libproj-dev
```  
  
#### Phonon  
```
sudo apt-get install phonon-backend-gstreamer phonon-backend-vlc
```  
Phonon Additional Packages:  
`liba52-0.7.4 libass5 libbasicusageenvironment1 libcddb2 libchromaprint0 libdc1394-22 libdca0 libdirectfb-1.2-9 libdvbpsi10 libdvdnav4 libdvdread4 libebml4v5 libfaad2 libgroupsock8 libiso9660-8 libkate1 liblivemedia50 libmad0 libmatroska6v5 libmpcdec6 libmpeg2-4 libphonon4 libpostproc-ffmpeg53 libproxy-tools libqt4-opengl libqt5x11extras5 libresid-builder0c2a libsdl-image1.2 libsdl1.2debian libsidplay2v5 libssh2-1 libupnp6 libusageenvironment3 libva-drm1 libva-x11-1 libvcdinfo0 libvlc5 libvlccore8 libxcb-composite0 libxcb-xv0 phonon-backend-gstreamer phonon-backend-gstreamer-common phonon-backend-vlc vlc vlc-data vlc-nox vlc-plugin-notify vlc-plugin-samba`  
  
#### Other Dependencies  
```
sudo apt-get install mpi-default-dev
```  
  
### Java  
```
sudo apt-get install openjdk-8-jdk
```  
Java Additional Packages:
`ca-certificates-java fonts-dejavu-extra java-common openjdk-8-jdk-headless openjdk-8-jre openjdk-8-jre-headless`
  
#### VTK-Qt  
```
sudo apt-get install libvtk6-qt-dev
```  
VTK-Qt Additional Packages:  
`comerr-dev hdf5-helpers i965-va-driver javascript-common krb5-multidev libaacs0 libaec-dev libaec0 libarmadillo6 libarpack2 libavcodec-dev libavcodec-ffmpeg56 libavformat-dev libavformat-ffmpeg56 libavutil-dev libavutil-ffmpeg54 libbdplus0 libblas-common libblas3 libbluray1 libcrystalhd3 libcurl4-gnutls-dev libdap-dev libdap17v5 libdapclient6v5 libdapserver7v5 libdrm-dev libegl1-mesa-dev libepsilon1 libfontconfig1-dev libfreetype6-dev libfreexl1 libgdal-dev libgdal1i libgeos-3.5.0 libgeos-c1v5 libgeos-dev libgfortran3 libgif-dev libgif7 libgl1-mesa-dev libgl2ps-dev libgl2ps0 libgles2-mesa libgles2-mesa-dev libglu1-mesa-dev libgme0 libgsm1 libgssrpc4 libhdf4-0-alt libhdf4-alt-dev libhdf5-10 libhdf5-cpp-11 libhdf5-dev libice-dev libjasper-dev libjbig-dev libjpeg-dev libjpeg-turbo8-dev libjpeg8-dev libjs-jquery libjs-sphinxdoc libjs-underscore libjsoncpp-dev libkadm5clnt-mit9 libkadm5srv-mit9 libkdb5-8 libkmlbase1 libkmldom1 libkmlengine1 liblapack3 liblzma-dev libminizip1 libmirclient-dev libmircommon-dev libmircookie-dev libmircookie2 libmircore-dev libmodplug1 libmp3lame0 libmysqlclient-dev libmysqlclient20 libnetcdf-c++4 libnetcdf-cxx-legacy-dev libnetcdf-dev libnetcdf11 libodbc1 libogdi3.2 libogg-dev libopenjp2-7 libopenjpeg5 libpng12-dev libpq-dev libpq5 libproj9 libprotobuf-dev libpthread-stubs0-dev libqt5clucene5 libqt5concurrent5 libqt5designer5 libqt5designercomponents5 libqt5help5 libqt5opengl5-dev libqt5quickparticles5 libqt5quickwidgets5 libqt5webkit5-dev libschroedinger-1.0-0 libshine3 libsm-dev libsnappy1v5 libsoxr0 libspatialite-dev libspatialite7 libsqlite3-dev libssh-gcrypt-4 libssl-dev libssl-doc libsuperlu4 libswresample-dev libswresample-ffmpeg1 libswscale-dev libswscale-ffmpeg3 libsz2 libtheora-dev libtiff5-dev libtiffxx5 libtwolame0 liburiparser1 libva1 libvdpau1 libvtk6-dev libvtk6-java libvtk6-qt-dev libvtk6.2 libvtk6.2-qt libwayland-bin libwayland-dev libwebp-dev libwebpdemux1 libx11-dev libx11-doc libx11-xcb-dev libx264-148 libx265-79 libxau-dev libxcb-dri2-0-dev libxcb-dri3-dev libxcb-glx0-dev libxcb-present-dev libxcb-randr0-dev libxcb-render0-dev libxcb-shape0-dev libxcb-sync-dev libxcb-xfixes0-dev libxcb1-dev libxdamage-dev libxdmcp-dev libxdmf-dev libxdmf2 libxerces-c-dev libxerces-c3.1 libxext-dev libxfixes-dev libxft-dev libxkbcommon-dev libxml2-dev libxrender-dev libxshmfence-dev libxss-dev libxt-dev libxvidcore4 libxxf86vm-dev libzvbi-common libzvbi0 mesa-common-dev mesa-vdpau-drivers mysql-common odbcinst odbcinst1debian2 proj-bin proj-data python-attr python-autobahn python-cffi-backend python-concurrent.futures python-cryptography python-enum34 python-idna python-ipaddress python-lz4 python-mpi4py python-msgpack python-openssl python-pam python-pkg-resources python-pyasn1 python-pyasn1-modules python-serial python-service-identity python-six python-snappy python-trollius python-twisted python-twisted-bin python-twisted-core python-txaio python-vtk6 python-zope.interface qt5-qmake qtbase5-dev qtbase5-dev-tools qtdeclarative5-dev qttools5-dev qttools5-private-dev tcl-dev tcl-vtk6 tcl8.6-dev tk-dev tk8.6-dev unixodbc unixodbc-dev uuid-dev va-driver-all vdpau-driver-all vdpau-va-driver vtk6 x11proto-core-dev x11proto-damage-dev x11proto-dri2-dev x11proto-fixes-dev x11proto-gl-dev x11proto-input-dev x11proto-kb-dev x11proto-render-dev x11proto-scrnsaver-dev x11proto-xext-dev x11proto-xf86vidmode-dev xorg-sgml-doctools xtrans-dev zlib1g-dev`  
  
#### QHull  
```
sudo apt-get install libqhull-dev
```  
QHull Additional Packages:  
`libqhull libqhull7`  
  
### OpenNI OpenNI2  
OpenNI and OpenNI2 cannot be installed via apt-get.  
The sdk binaries and links to git repos may be found at [https://structure.io/openni](https://structure.io/openni).  
  
#### OpenNI  
First, let's tackle OpenNI:  
```
git clone https://github.com/OpenNI/OpenNI.git
cd OpenNI
```  
Create an ```unstable``` branch to save yourself in the future  
```
git checkout -b unstable
```  
Install OpenNI  
```
cd Platform/Linux/CreateRedist/
sudo ./RedistMaker
cd ../Redist/OpenNI-Bin-Dev-Linux-x64-v1.5.8.5
sudo ./install.sh
```  
Note, make sure no upper level directories have spaces in the names.  
`RedistMaker` cannot handle spaces. `RedistMaker` creates an OpenNI distribution in 
OpenNI/Platform/Linux/Redist/. There may exist a distribution already, 
but run `RedistMaker` anyway for a fresh one.  
  
#### OpenNI2  
Second, let's take care of OpenNI2:  
```
git clone https://github.com/occipital/OpenNI2.git
```  
Create an `unstable` branch to save yourself in the future  
```
git checkout -b unstable
make
```  
Install OpenNI2  
```
cd Packaging/Linux/
sudo ./install.sh
```  
Add the definitions of `OPENNI2_INCLUDE` and `OPENNI2_REDIST` from the new 
`OpenNIDevEnvironment` to `~/.bashrc` manually.  
Add the following definitions to `~/.bashr` replace `root` with the address of your 
OpenNI2 directory.  
```
export OPENNI2_INCLUDE=root/OpenNI2/Packaging/Linux/Include
export OPENNI2_REDIST=root/OpenNI2/Packaging/Linux/Redist

export OPENNI2_INCLUDE_DIRS=root/OpenNI2/Packaging/Linux/Include
export OPENNI2_LIBRARY=root/OpenNI2/Packaging/Linux/Include
```  
Lastly,  
```
source ~/.bashrch
```  
  
### Point Cloud Library  
Finally ready to build PCL!  
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
~~~~  
  
```
cmake ..
make -j8
```  
  
Go get some coffee and check your email.  
  
