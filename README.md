```bash
# Python3 trouble shooting for Jetson board
export OPENBLAS_CORETYPE=ARMV8 python3

# CUDA Setting
export PATH=/usr/local/cuda-10.2/bin:$PATH
export LD_LIBRARY_PATH=/usr/local/cuda-10.2/lib64:$LD_LIBRARY_PATH

# bashrc aliases
alias gb='gedit ~/.bashrc'
alias sb='source ~/.bashrc'

# ROS aliases
alias cw='cd ~/catkin_ws'
alias cs='cd ~/catkin_ws/src'
alias cm='cd ~/catkin_ws && catkin_make'

# ROS Setting
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
