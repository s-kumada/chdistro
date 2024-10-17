# chdistro

`chdistro`: Change the `ROS_DISTRO` and working space with a single command.

## Install
### Main script
```sh
$ pushd /usr/local/bin && sudo wget https://raw.githubusercontent.com/youtalk/chdistro/master$SHELL/chdistro && sudo chmod 755 chdistro && popd
```
### Tab-completion script
see also: https://hans-robo.hatenablog.com/entry/2020/03/10/121017. 
```sh
$ pushd /etc/bash_completion.d && sudo wget https://gist.githubusercontent.com/HansRobo/38060a841ca6be71181ccc9dcc62c86e/raw/a164c5561605054c6331fe51bcf56c4c199fff22/chdistro-completion.bash && popd
```

## Usage

```sh
$ chdistro --help
chdistro ROS_DISTRO [WORKSPACE_DIR]
```

### ROS 2
***Supported distributions : Kilted Kaiju, Jazzy Jalisco, Iron Irwini, Humble Hawksbill, Galactic Geochelone, Foxy Fitzroy, Eloquent Elusor, Dashing Diademata***

e.g.) If the path to the user workspace is **$HOME/ros/“ROS_DISTRO”**:

```sh
$ chdistro jazzy
ROS_DISTRO=jazzy
ROS_PYTHON_VERSION=3
ROS_VERSION=2
ROS_HOME=/home/$USER/.ros
ROS_LOCALHOST_ONLY=1
ROS_WORKSPACE=/home/$USER/ros/jazzy
```

e.g.) If the path to the user workspace is **$HOME/ros2_ws**:
```sh
$ chdistro jazzy ~/ros2_ws
ROS_DISTRO=jazzy
ROS_PYTHON_VERSION=3
ROS_VERSION=2
ROS_HOME=/home/$USER/.ros
ROS_LOCALHOST_ONLY=1
ROS_WORKSPACE=/home/$USER/ros2_ws
```

### ROS 1
***Supported distributions : Noetic Ninjemys, Melodic Morenia, Kinetic Kame***

e.g.) If the path to the user workspace is **$HOME/ros/“ROS_DISTRO”**:

```sh
$ chdistro noetic
ROS_HOME=/home/$USER/.ros
ROS_WORKSPACE=/home/$USER/ros/noetic
ROS_DISTRO=noetic
ROS_ETC_DIR=/opt/ros/noetic/etc/ros
ROS_PACKAGE_PATH=/opt/ros/noetic/share
ROS_PYTHON_VERSION=3
ROS_VERSION=1
ROS_ROOT=/opt/ros/noetic/share/ros
ROS_MASTER_URI=http://localhost:11311
ROSLISP_PACKAGE_DIRECTORIES=
ROS_WORKSPACE=/home/$USER/ros/noetic
```

e.g.) If the path to the user workspace is **$HOME/catkin_ws**:
```sh
$ chdistro noetic ~/catkin_ws
ROS_DISTRO=noetic
ROS_ETC_DIR=/opt/ros/noetic/etc/ros
ROS_PACKAGE_PATH=/opt/ros/noetic/share
ROS_PYTHON_VERSION=3
ROS_VERSION=1
ROS_ROOT=/opt/ros/noetic/share/ros
ROS_MASTER_URI=http://localhost:11311
ROSLISP_PACKAGE_DIRECTORIES=
ROS_HOME=/home/$USER/.ros
ROS_WORKSPACE=/home/$USER/catkin_ws
```
