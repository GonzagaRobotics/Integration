# Integration
Integrating communications and control between the rover, control methods/models, and microcontrollers. Using ROS2 and MicroROS.

These instructions assume the micro_ros_agent is already created. To do this, follow the instructions on this link under **Creating the micro-ROS agent** https://micro.ros.org/docs/tutorials/core/first_application_linux/

Steps to connect microcontroller to ROS2:
1. Plug microcontroller into Jetson over USB
2. (Optional) You might need to change the permissions on the USB to allow it to communicate. If so, figure out what the connection is by entering lsusb -l /dev/tty* Then, sudo chmod 666 /dev/'connection name'
3. source install/local_setup.bash
4. ros2 run micro_ros_agent micro_ros_agent serial --dev /dev/'connection name'
5. Press the enable button on the microcontroller

You should now be able to see the microcontroller's nodes and topics using ros2 topic list and ros2 node list. 


