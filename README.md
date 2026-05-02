## About The Project

Used ROS2, gazebo, and Moveit to program an franka panda robot arm model to recognise blocks of different colours and move them to a bin autonomously using opencv.

### How to Run

1. Clone the repo
   
2. Install all necessary packages and dependencies
   
3. Run the following commands in terminal to start the gazebo simulation, RViz, camera and colour detection, Moveit, and the Robot controllers
   
   ```
   colcon build
   source install/setup.bash
   ros2 launch panda_bringup pick_and_place.launch.py
   ```
   open another terminal to run
   
   ```
   source install/setup.bash
   ros2 run pymoveit2 pick_and_place.py --ros-args -p target_color:=R
   ```
   Target colour can be R, B, or G. Which stand for Red, Green, and Blue respectively.

   To pick another colour after the first one, press ```ctrl+c``` in the second terminal then run
   ```
   ros2 run pymoveit2 pick_and_place.py --ros-args -p target_color:=B
   ```
   with your desured colour to rerun the operation.


## How it Works(Project Architecture)

## Reference Links
