This repository contains the ROS 2 packages used to visualize the `USF Robot` in **RViz2** and **MoveIt2**.

# Requirements:
* **Ubuntu 22.04 LTS**
* ROS 2 **Humble Hawksbill**
* **RViz2** and **MoveIt2** (`ws_moveit2`)

# Before Launching RViz2/MoveIt2:
1. **Build the Package**: 
    colcon build
2. **Source the ROS 2 Humble Environment**: 
    source /opt/ros/humble/setup.bash
3. **Source the Workspace**: 
    source install/setup.bash

# Launch RViz2/MoveIt2 with the USF Robot: 
    ros2 launch usf_robot_moveit_config demo.launch.py

- When you launch the `demo.launch.py`, click on "Add" on **RViz2** under **Displays**, then scroll down and select `RobotModel`. Click "OK" to add it.
- Under **Displays**, click on the arrow to the left of `RobotModel` then scroll down to `Description Topic`. Click on the empty space to the right of it, then click the down arrow and select `/robot_descriptio>

# Planning Movements:
1. Under **MotionPlanning**, select the __Planning__ tab. There is a planning group called `usf_arm` which consists of the robot arm plus the claws. 
2. Keep the current state as <current>, and select your goal state.
3. Click on `Plan & Execute`.


**Notes**:
- Under **MotionPlanning**, you can change the velocity by adjusting the `Velocity Scaling` value.
- You can also adjust the robot's joints with sliders by navigating to the __Joints__ tab.
- After you adjust the joint positions with the sliders, click on `Plan & Execute` under the __Planning__ tab.
