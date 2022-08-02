# install-Ros2-on-Jetson-nano
**Step 1>>**download Xubunto20.4

**Step 2>>**oppen virtualbox and click

**Step 3>>**upload xupunto file

**Step 4>>**cuntinio setting

oppen terminal and install ROS2

1>>locale # check for UTF-8

sudo apt update && sudo apt install locales sudo locale-gen en_US en_US.UTF-8 sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8 export LANG=en_US.UTF-8

locale # verify settings

2>>apt-cache policy | grep universe

3>>500 http://us.archive.ubuntu.com/ubuntu focal/universe amd64 Packages release v=20.04,o=Ubuntu,a=focal,n=focal,l=Ubuntu,c=universe,b=amd64

4>>sudo apt install software-properties-common sudo add-apt-repository universe

5>>udo apt update && sudo apt install curl gnupg2 lsb-release sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key -o /usr/share/keyrings/ros-archive-keyring.gpg

6>>echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(source /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null

7>>sudo apt update

8>>sudo apt upgrade

9>>sudo apt install ros-foxy-desktop
