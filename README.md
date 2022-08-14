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
       roslaunch turtlebot3_gazebo turtlebot3_world.launch
        
 second- run a new terminal with these commands: 
 
     source /home/%username%/catkin_%WorkspaceName%/devel/setup.bash
     export TURTLEBOT3_MODEL=burger
     roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping
    
    
 third-  run a new terminal with these commands: 
 
     source /home/%username%/catkin_%WorkspaceName%/devel/setup.bash
     export TURTLEBOT3_MODEL=burger
     roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
  
 
 
 fourth- now you can control the robot through the 3rd terminal using the  W S A D X and start mapping.
 
 ![Screenshot_3](https://user-images.githubusercontent.com/91455733/184547764-7a5d17da-3462-4cff-a942-539f11695515.png)
 
 
 fifth- you can see i mapped the whole world, and only thing left is to save it.
 
 ![Screenshot_1](https://user-images.githubusercontent.com/91455733/184548026-eb32a679-40e0-4696-8aa6-ff34a38cde8c.png)


 sixth- to save the map, in a new terminal run this command: 

    rosrun map_server map_saver -f ~/map
    
   ![Screenshot_2](https://user-images.githubusercontent.com/91455733/184548192-716cb273-d936-4cad-be75-c40b4c3c2c35.png)

   will be saved as .pgm file.    
    
    

