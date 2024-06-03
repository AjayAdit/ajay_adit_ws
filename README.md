# Deployment of a custom-defined robot in Rviz and Gazebo with Lidar and camera plugins. Additionally, the feature of teleoperation has been incorporated into the robot-simulated in a custom gazebo world.

This is the readme file for both packages: bot_description and bot_world. To ensure ease of use, each functionality of these packages and the functions can be comprehensively called using launch files.

Thereby, there are 3 launch files, namely rviz.launch, spawn.launch, and control.launch has the capability to carry out all the expected functionalities:

1. rviz.launch: This launch file visualizes the bot in rviz to show the various nuances of the xacro file that described the structure of the robot.
   
   ![Screenshot from 2024-06-03 09-59-17](https://github.com/AjayAdit/ajay_adit_ws/assets/62584240/66ccde08-c036-4649-af93-348370558e9b)

2. spawn.launch: This launch file simulates the robot in a gazebo with camera and Lidar plugins enabled; additionally, this ensures that the robot_state_publisher, and the robot plugin and urdf are working in synergy.
 
   ![Screenshot from 2024-06-03 10-00-40](https://github.com/AjayAdit/ajay_adit_ws/assets/62584240/cab2b9b8-0723-4260-abbb-c4329fc9bd1e)

3. Control.launch: This launch file is the master launch file of the project, encomposing all the functionalities in a single easy-to-use launch file. A few key features added to this launch file are that the robot is spawned in a custom launch file with a variety of objects, and this is the launch file that enables us to carry out teleoperation.To ensure ease of use, this launch file has the teleop node automatically created using a special module named  ### subprocess.Popen.
   ### ScreenShot:

   ![Screenshot from 2024-06-03 10-13-04](https://github.com/AjayAdit/ajay_adit_ws/assets/62584240/38a72351-7d86-4e1c-b5e3-10ba15c0cf32)

   ![Screenshot from 2024-06-03 10-15-17](https://github.com/AjayAdit/ajay_adit_ws/assets/62584240/391d7be4-850d-4ae3-9ea6-ca08046147ff)

   Teleoperation of the bot in a custom Gazebo world with camera and lidar plugins enabled (Gif):

   
  [Screencast from 06-03-2024 10:16:59 AM.webm](https://github.com/AjayAdit/ajay_adit_ws/assets/62584240/265d9e3e-8677-4739-b0cb-222f53348a76)

## How to test my packages:
1. In the home directory, clone this repo using git clone. (The repo is itself a workspace, so source it in bashrc)

2. As mentioned above, all functionality of the packages can be accessed by three launch files, and the ros2 command to run them is given below.
      
          (((ros2 launch bot_description rviz.launch)))

          (((ros2 launch bot_description spawn.launch)))

          (((ros2 launch bot_description control.launch)))
             
