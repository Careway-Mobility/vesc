# vesc

Fork of https://github.com/erwincoumans/vesc.

# Installation

Add yourself to the dialout group: sudo usermod -a -G dialout args-xaviar

Add udev rules: 
cd /etc/udev/rules.d

Make file 99-ttyACM.rule with below lines:
SUBSYSTEM=="tty", KERNEL=="ttyACM0", GROUP="dialout", MODE="0660"
SUBSYSTEM=="tty", KERNEL=="ttyACM1", GROUP="dialout", MODE="0660"

## Dependencies
ROS Packages
- [ackermann_msgs](http://wiki.ros.org/ackermann_msgs) (via `ros-melodic-ackermann-msgs` apt package for example)
- [serial](http://wiki.ros.org/serial) (via `ros-melodic-serial` apt package for example)
- [tf](http://wiki.ros.org/tf) (via `ros-melodic-tf` apt package for example)
