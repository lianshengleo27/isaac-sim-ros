# isaac-sim-ros

ROS2 packages for controlling robots in isaac sim
## 1. Installation
install depenencies:
```bash
sudo apt update
rosdep install -i --from-path src --rosdistro $ROS_DISTRO -y
```
## 2. Build the package
```bash
colcon build --symlink-install
```
