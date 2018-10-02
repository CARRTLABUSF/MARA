# MARA
MARA ROS Files-

Steps to install---

1. catkin_make
2. add setup.bash location to your ~/.bashrc
	Go to the end of that file and add
	# source <path to your directory>/devel/setup.bash
3. Instal dependencies. To find out the dependencies, run:

		# rosrun mara joint_trajectory_server.py r 0
	Then, install dependencies with 
	
		# sudo apt-get install python-DEPENDENCYNAME
	for example: 
	
		#sudo apt-get install python-sklearn
4. Run roscore

		# roscore
5. 
 1: run the trajectory servers for each arm:

		# rosrun mara joint_trajectory_server.py r 0
		# rosrun mara joint_trajectory_server.py l 1

 2: launch moveit:
		# roslaunch mara_moveit_config demo_mara.launch

 3: run the controller


		# rosrun mara mara_controller.py   
