# 🤖 ROS Noetic installation instructions

First of all, there are somethings you need to check before you begain these instructions:
- Check if you have (Ubuntu 20.04) **IT HAS TO BE THE SAME VERSION!**
> You can check your Ubuntu's version by typing the following in the terminal: `lsb_release -a`
- Configure your Ubuntu repositories to allow "restricted," "universe," and "multiverse. [Follow the guide here](https://help.ubuntu.com/community/Repositories/Ubuntu)


## Open your Ubuntu's terminal and follow these instructions:
### 📝**1. Setup your sources.list**
  - *Setup your computer to accept software from packages.ros.org.*
  ```data
  sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'.
  ```
-------------------------------------
### 🔑**2. Set up your keys**
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
### 📥**3. Installation**
First, make sure your Debian package index is up-to-date:
``` sudo apt update```

*Now pick the intended ROS version:*
  - **Desktop-Full Install: (Recommended):** Everything in Desktop plus 2D/3D simulators and 2D/3D perception packages
```
sudo apt install ros-noetic-desktop-full
```

  - **Desktop Install:** Everything in ROS-Base plus tools like rqt and rviz
```
sudo apt install ros-noetic-desktop
```

  - **ROS-Base:** (Bare Bones) ROS packaging, build, and communication libraries. No GUI tools
```
sudo apt install ros-noetic-ros-base 
```
    
-------------------------------------
### 💻**4. Environment Setup**
You must source this script in every bash terminal you use ROS in.
```
source /opt/ros/noetic/setup.bash
```
The following commands will do it for you:

***Bash***
```
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
source ~/.bashrc
```
***zsh***
``` 
echo "source /opt/ros/noetic/setup.zsh" >> ~/.zshrc
source ~/.zshrc
```
-------------------------------------
### ☑️ TO DO
You're done with the installation, now let's check our progress:

- [x] Installing Ubuntu 20.04
- [x] Installing ROS noetic
- [ ] ROS Tutorials

The last step would be to refere you to 🔗 [ROS offical Tutorials](http://wiki.ros.org/ROS/Tutorials). 

***ENJOY***
👾
