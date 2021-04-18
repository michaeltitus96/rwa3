# rwa3

Before beginning, place room_recorder.py in your location_recorder/nodes folder. Update line 13 to match the path to the records folder. No need to create the .yaml file before beginning, the service script will do that if it doesn't already exist.

1. In new terminal tab, start "roscore"
2. In new terminal tab, go to your worksapce (cd rwa), then do catkin_make (or "catkin build"), then source.
3. Start robot navigation with "roslaunch mapping start_navigation.launch"
4. In new terminal tab, again build/source workspace (sometimes this isn't necessary but I always do it just in case). Begin room_recorder.py with "rosrun location_recorder room_recorder.py"
5. In new termianl (again build/source), make sure robot is in living room and type ' rosservice call room_service "livingroom" '. There should be confirmation that the entry was saved.
6. Using 2D Nav Goal in Rviz, move the robot to the next room. 
7. Once the robot has stopped moving, again type ' rosservice call room_service "kitchen" ' (or whatever room it is in).
8. Continue for each room, then go to the rosrun terminal and CTRL+C.
9. Check that the .yaml file in the records folder is accurate.
