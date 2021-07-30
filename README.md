# Robot-Navigation-Using-SLAM-ROS
task2

**PC Setup**

1. first i installed ubuntu 18 on PC
2. install ros melodic
3. Install Dependent ROS 1 Packages
4. Install TurtleBot3 Packages
5. Set TurtleBot3 Model Name
    * Set the default TURTLEBOT3_MODEL name to waffle model
    * echo "export TURTLEBOT3_MODEL=waffle" >> ~/.bashrc
    * https://drive.google.com/file/d/1cYnsStg_ymaqQErtM6xvPYbklXWiDUxz/view?usp=sharing

**Gazebo Simulation**

1. Install Simulation Package
2. Launch Simulation World
   * Three simulation environments are prepared for TurtleBot3. I select TurtleBot3 World to launch Gazebo.
   * $ export TURTLEBOT3_MODEL=waffle
   * $ roslaunch turtlebot3_gazebo turtlebot3_world.launch
3. Operate TurtleBot3
   * and to control the robot I run the following command in new terminal
   * roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch

**SLAM Simulation**

https://drive.google.com/file/d/1VyqiX0mbGUxbafvGGpnrQH1DLp24kiSH/view?usp=sharing
1. Launch Simulation World
   * in new terminal:-
   * $ export TURTLEBOT3_MODEL=waffle
   * $ roslaunch turtlebot3_gazebo turtlebot3_world.launch
2. Run SLAM Node
   * in new terminal:-
   * $ export TURTLEBOT3_MODEL=waffle
   * $ roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping
3. Run Teleoperation Node
   * and to control the robot I run the following command in new terminal
   * roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
4. Save Map
   * in new terminal:-
   * rosrun map_server map_saver -f ~/map
   * https://drive.google.com/file/d/1W0cOhxvqIGMhPVe5xZefh6K0irKVF91X/view?usp=sharing
