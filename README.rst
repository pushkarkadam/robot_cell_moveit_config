Robot Cell MoveIt Config
========================

This repository uses moveit to plan the robot movement.

Usage
-----

First source the workspace.

Driver 
^^^^^^

Make sure to download and install `robot_cell_control`_  and `robot_cell_description`_ packages.

.. _robot_cell_control: https://github.com/pushkarkadam/robot_cell_control 
.. _robot_cell_description: https://github.com/pushkarkadam/robot_cell_description 

The first step includes starting driver for UR10e robot as follows::

    ros2 launch robot_cell_control start_robot.launch.py use_fake_hardware:='True' use_fake_sensor:='True'

MoveIt2 
^^^^^^^

Start the ``move_group`` node by running the following::

    ros2 launch robot_cell_moveit_config move_group.launch.py

If everything went well, you should see the output: **You can start planning now!**.

To interact with the MoveIt! setup, you can start Rviz with the correct setup file::

    ros2 launch robot_cell_moveit_config moveit_rviz.launch.py