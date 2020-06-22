# ROS Noetic installation instructions

First of all, there are somethings you need to check before you begain these instructions:
- Check if you have (Ubuntu 20.04) **IT HAS TO BE THE SAME VERSION!**
> You can check your Ubuntu's version by typing the following in the terminal: `lsb_release -a`
- Configure your Ubuntu repositories to allow "restricted," "universe," and "multiverse. [Follow the guide here](https://help.ubuntu.com/community/Repositories/Ubuntu)


## Open your Ubuntu's terminal and follow these instructions:
### **1. Setup your sources.list**
  - *Setup your computer to accept software from packages.ros.org.*
  ```data
  sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'.
  ```
-------------------------------------
### **2. Set up your keys**
```
sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
```
> If you experience issues connecting to the keyserver, you can try substituting `hkp://pgp.mit.edu:80` or `hkp://keyserver.ubuntu.com:80` in the previous command.
> Alternatively, you can use curl instead of the apt-key command, which can be helpful if you are behind a proxy server:
```
curl -sSL 'http://keyserver.ubuntu.com/pks/lookup?op=get&search=0xC1CF6E31E6BADE8868B172B4F42ED6FBAB17C654' | sudo apt-key add -
```
> If you get an error saying _**bash: curl: command not found**_ you may not have `curl` command installed, follow this:
> - Update your `Ubuntu` box, run: `sudo apt update && sudo apt upgrade`
> - Next, install `curl`, execute: `sudo apt install curl`
> - Verify install of `cur`l on `Ubuntu` by running: `curl --version`
-------------------------------------
### **3. Installation**
First, make sure your Debian package index is up-to-date:
    ``` sudo apt update```
