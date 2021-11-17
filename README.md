# ROS_self_navigating_bot

This is a demo of a self-navigating robot with global and local map planning using Rviz, gazebo and ROS

The commands required to run the package are the following:

![](images/commands%20required.PNG)

Your Rviz should look like this:

![](images/rviz.PNG)

The little robot you see is a Differential Drive robot designed in Fushion 360 and transformed into a URDF to be used in gazebo

It was designed as simple as posible for demonstration purposes

In order to make this the navigation ros package was used along side with: Gmapping, Map_server, AMCL, Move_base, Navigation, Control, Slam

The result is the following robot that can navigate itself to a 2D goal given through Rviz by the user in a map that is being published by the mas_server package and it can create 

local and global paths to navigate through the map. This is demonstrated well if an object is placed in front of it(through gazebo) after the goal destinations has been set, it 

will automatically change it's local path in order to avoid the obstacle and reach it's goal. The following is possible as the robot carries a laser scanner that can give real 

time feedback from it's soroundings and it can as a result use and share that information throught the /laser/scan topic in order to plan a new path.  
