|||
|--|--|
|OS|Ubuntu 18.04 / Jetpack 4.4~5|
|ROS|Melodic|

```bash
# Python3 trouble shooting for Jetson board
export OPENBLAS_CORETYPE=ARMV8 python3

# CUDA setting
export PATH=/usr/local/cuda-10.2/bin:$PATH
export LD_LIBRARY_PATH=/usr/local/cuda-10.2/lib64:$LD_LIBRARY_PATH

# bashrc aliases
alias gb='gedit ~/.bashrc'
alias sb='source ~/.bashrc'

# ROS aliases
alias cw='cd ~/catkin_ws'
alias cs='cd ~/catkin_ws/src'
alias cm='cd ~/catkin_ws && catkin_make'

# ROS setting
source /opt/ros/melodic/setup.bash
source ~/catkin_ws/devel/setup.bash
source ~/carto_ws/install_isolated/setup.bash	# Cartographer
source ~/cvbridge_build_ws/devel/setup.bash	# CvBridge for python3

# ROS Network
export ROS_IP=localhost     # My IP address
export ROS_HOSTNAME=${ROS_IP}
export ROS_MASTER_URI=http://${ROS_IP}:11311

# Cartographer alias
alias ccw='cd ~/carto_ws'
alias ccs='cd ~/carto_ws/src'
alias ccm='cd ~/carto_ws && catkin_make_isolated --install --use-ninja'
```

---

|||
|--|--|
|OS|Ubuntu 20.04|
|ROS|Foxy|

```bash
# bashrc aliases
alias gb='gedit ~/.bashrc'
alias sb='source ~/.bashrc'
alias cb='cat ~/.bashrc'

# ROS aliases
alias cw='cd ~/colcon_ws'
alias cs='cd ~/colcon_ws/src'
alias cm='cd ~/colcon_ws && colcon build'

# ROS setting
source /opt/ros/foxy/setup.bash
source ~/colcon_ws/install/setup.bash		# Main ROS workspace
source ~/turtlebot3_ws/install/setup.bash	# Turtlebot3 workspace

# colcon setting
source /usr/share/colcon_cd/function/colcon_cd.sh
export _colcon_cd_root=/opt/ros/foxy/
source /usr/share/colcon_argcomplete/hook/colcon-argcomplete.bash

# Tutlebot3 setting
export ROS_DOMAIN_ID=30 #TURTLEBOT3
export TURTLEBOT3_MODEL=burger
```
