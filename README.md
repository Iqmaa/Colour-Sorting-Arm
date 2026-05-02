## About The Project

Used ROS2, gazebo, and Moveit to program an franka panda robot arm model to recognise blocks of different colours and move them to a bin autonomously using opencv.

|     |     |
| :---: | :---: |
| ![panda1](https://github.com/Iqmaa/Colour-Sorting-Arm/blob/main/Media/panda1.png?raw=true)  | ![panda2](https://github.com/Iqmaa/Colour-Sorting-Arm/blob/main/Media/panda2.png?raw=true) /> |


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
   with your desired colour to rerun the operation.

[colour_sorting_arm.webm](https://github.com/user-attachments/assets/4a875368-fbba-408e-9891-9ec3122fc112)


## How it Works(Project Architecture)

## Reference Links
