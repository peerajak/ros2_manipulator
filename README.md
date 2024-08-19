# ros2_manipulator The Consturct's material

## How to run

Terminal 1.
ros2 run simple_grasping basic_grasping_perception_node --ros-args -p debug_topics:=true

Terminal 2
ros2 launch my_moveit_config move_group.launch.py

Terminal 3
ros2 launch my_moveit_config moveit_rviz.launch.py

Terminal 4
ros2 run get_pose_client get_pose_client_v2
ros2 launch moveit2_scripts pick_place.launch.py

// stand a block
ros2 run gazebo_ros spawn_entity.py -file ~/ros2_ws/src/grasp_box.urdf -x 0.34 -y 0.13 -z 0.1 -entity grasp_box
ros2 run gazebo_ros spawn_entity.py -file ~/ros2_ws/src/grasp_box.urdf -x 0.5 -y 0.13 -z 0.1 -entity grasp_box

=================================================
ros2 run gazebo_ros spawn_entity.py -file ~/ros2_ws/src/grasp_box.urdf -x 0.34 -y 0.13 -z 0.1 -entity grasp_box
1723807030.349394377] [get_pose_client]: Sending goal
[INFO] [1723807030.353320709] [get_pose_client]: Goal accepted by server, waiting for result
[INFO] [1723807031.901487440] [get_pose_client]: Result received[INFO] [1723807031.901562480] 
                              [get_pose_client]: X: 0.328843
[INFO] [1723807031.901587607] [get_pose_client]: Y: 0.130933
=================================================
ros2 run gazebo_ros spawn_entity.py -file ~/ros2_ws/src/grasp_box.urdf -x 0.5 -y 0.13 -z 0.1 -entity grasp_box
user:~/ros2_ws$ ros2 run get_pose_client get_pose_client_v2
[INFO] [1723807148.989174016] [get_pose_client]: Sending goal
[INFO] [1723807148.989873097] [get_pose_client]: Goal accepted by server, waiting for result
[INFO] [1723807149.097478285] [get_pose_client]: Result received
[INFO] [1723807149.097551100] [get_pose_client]: X: 0.488055
[INFO] [1723807149.097577103] [get_pose_client]: Y: 0.150000

================================================
ros2 run gazebo_ros spawn_entity.py -file ~/ros2_ws/src/grasp_box.urdf -x 0.5 -y 0.1 -z 0.1 -entity grasp_box
O] [1723807778.420359292] [get_pose_client]: Goal accepted by server, waiting for result
[INFO] [1723807778.485656843] [get_pose_client]: Result received
[INFO] [1723807778.485733353] [get_pose_client]: X: 0.488057
[INFO] [1723807778.485760096] [get_pose_client]: Y: 0.120000

===============================================
ros2 run gazebo_ros spawn_entity.py -file ~/ros2_ws/src/grasp_box.urdf -x 0.3 -y 0.11 -z 0.1 -entity grasp_box
FO] [1723808029.147849265] [get_pose_client]: Result received
[INFO] [1723808029.147912525] [get_pose_client]: X: 0.288818
[INFO] [1723808029.147935838] [get_pose_client]: Y: 0.110983

===============================================
ros2 run gazebo_ros spawn_entity.py -file ~/ros2_ws/src/grasp_box.urdf -x 0.38 -y 0.13 -z 0.1 -entity grasp_box
723966102.276489908] [get_pose_client]: Result received[INFO] [1723966102.276568922] [get_pose_client]: X: 0.368854
[INFO] [1723966102.276594695] [get_pose_client]: Y: 0.130228


ax + b = x*
cy + d = y*
where x*,y* is real position of red block

a(0.328843) + b = 0.34
a(0.488055) + b = 0.5
a(0.288818) + b = 0.3
a(0.368854) + b = 0.38
Result: a=1.004949376, b = 0.0095294324
a=0.999725, b=0.011247
a=0.999550, b=0.0011311
Least square solution a = 1.004, b=0.009829

#c(0.130933) + d = 0.13
c(0.15) + d = 0.13
c(0.12) + d = 0.1
c(0.110983)  + d = 0.11
c(0.130228) + d = 0.13
Result c=1, d=-0.02
c =1.03823, d= -0.0053369
Least square solution c = 1.081, d=-0.01687
 



