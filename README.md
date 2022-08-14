# TurtleBot3_SLAM_Simulation_guide




# Installing TurtleBot3: 

run these commands in cmd: 

      sudo apt-get install ros-noetic-joy ros-noetic-teleop-twist-joy \
      ros-noetic-teleop-twist-keyboard ros-noetic-laser-proc \
      ros-noetic-rgbd-launch ros-noetic-rosserial-arduino \
      ros-noetic-rosserial-python ros-noetic-rosserial-client \
      ros-noetic-rosserial-msgs ros-noetic-amcl ros-noetic-map-server \
      ros-noetic-move-base ros-noetic-urdf ros-noetic-xacro \
      ros-noetic-compressed-image-transport ros-noetic-rqt* ros-noetic-rviz \
      ros-noetic-gmapping ros-noetic-navigation ros-noetic-interactive-markers

      sudo apt install ros-noetic-dynamixel-sdk
    
      sudo apt install ros-noetic-turtlebot3-msgs
    
      sudo apt install ros-noetic-turtlebot3


# starting Simulation: 
  
  
 first- run a terminal with these commands:  
  
       source /home/%username%/catkin_%workspace name%/devel/setup.bash
       export TURTLEBOT3_MODEL=burger
       roslaunch turtlebot3_gazebo turtlebot3_house.launch
        
 second- run a new terminal with these commands: 
 
     source /home/*username*/catkin_*workspace name*/devel/setup.bash
     export TURTLEBOT3_MODEL=burger
     roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping
    
    
 third-  run a new terminal with these commands: 
 
     source /home/*username*/catkin_*workspace name*/devel/setup.bash
     export TURTLEBOT3_MODEL=burger
     roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
  
 
 
 fourth- now you can control the robot through the 3rd terminal using the  W S A D X and start mapping.
 

 fifth- to save the map, in a new terminal run these commands: 

    rosrun map_server map_saver -f ~/map
    
    
    

