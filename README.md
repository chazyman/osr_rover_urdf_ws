# Install & Run
## Install & Build ROS2 workspace
Open a Terminal window  
cd ~  
git clone https://github.com/chazyman/osr_rover_urdf_ws.git  
cd osr_rover_urdf_ws  
source /opt/ros/humble/setup.sh  
rosdep install --from-paths src --ignore-src -r -y  
colcon build --symlink-install  
source install/setup.sh  

## Launch Rover URDF
ros2 launch osr_description perseverance_rover_with_params.launch.py urdf_model:=\`ros2 pkg prefix --share osr_description\`/urdf/rover/m2020_all.urdf  
  
-- or --  
ros2 launch osr_description perseverance_rover_with_params.launch.py urdf_model:=\`ros2 pkg prefix --share osr_description\`/urdf/rover/m2020_rover_flipped.urdf  

