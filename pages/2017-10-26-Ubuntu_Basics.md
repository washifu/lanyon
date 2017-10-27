---
layout: page
title: Ubuntu Basics
comments: true
---

Install [Ubuntu](https://www.ubuntu.com/download/desktop)  
  
This guide is for 16.04.3  
  
## The Basics  
  
### Shared Folders
On the VMware menu select Virtual Machine->Reinstall VMware Tools.  
Once the cd for the installation is available, copy the VMwareTools tar.gz file to a Downloads 
(or your preferred directory on your Ubuntu VM). Unzip, change directory into ```vmware-tools-distrib``` 
and in terminal, run  
```
sudo ./vmware-install.pl
```  
Hit enter for all the default options.  
Restart the VM.  
The shared directory is located in ```/mnt/hgfs/```.
Setup a shared directory in host computer in the ```Sharing``` settings for the VM in VMware.  
  
### Git
```
sudo apt-get install git
```  
  
### [Google Chrome](https://askubuntu.com/a/510186)  
Add Key  
```
wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
```
Setup Repo  
```
echo 'deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main' | sudo tee /etc/apt/sources.list.d/google-chrome.list
```
Install Package  
```
sudo apt-get update 
sudo apt-get install google-chrome-stable
```  
  
### [Sublime](https://askubuntu.com/a/227617)
Add Repo  
```
sudo add-apt-repository ppa:webupd8team/sublime-text-3
```  
Install Package  
```
sudo apt-get update
sudo apt-get install sublime-text-installer
```  
  
### ~/.bashrc
Open ```~/.bashrc``` with Sublime  
```
subl ~/.bashrc
```  
Add to end of ```~/.bashrc``` file  
```
#----------------------#
#---   USER ADDED   ---#
#----------------------#
alias rebuild='cd .. && rm -r build && mkdir build && cd build && cmake ..'
```
