This project is a self balanced robot. The following hardware is used: Arduino Nano, MPU6050, BT module, Nema 17 stepper motors, A4988 stepper drivers, V4 CNC shield, 5v step-down converter, 3S LiPo batteries, 3S protection board.

In case you are interested in this project here are the list to parts needed (except the battery! - that's a separate talk):
Arduino Nano + V4 Shield + Stepper Drivers - https://bit.ly/2UT20Mf
OR items separately 
Arduino Nano soldered pins with cable - https://bit.ly/2rRCKJ7
Arduino Nano pins not soldered - https://bit.ly/2Cjfr0u
V4 Shield only - https://bit.ly/2CiQuST
A4988 drivers (2 pieces) - https://bit.ly/2BqmnaL

Stepper Motors (2 pieces) - https://bit.ly/2rKPd0N
MPU6050 - https://bit.ly/2SXwivy
Bluetooth module - https://bit.ly/2Grtjdo
Dupont wires - https://bit.ly/2LlYHsq
Step Down Voltage Regulator - https://bit.ly/2R8iUHO
Switch - https://bit.ly/2Evlh0f
Some more wires - https://bit.ly/2EuaaFa
Connector for the Shield - https://bit.ly/2R2s0FD or https://bit.ly/2PJ4KrG

You will also need soldering iron and all related, plywood or something else,  bolts, etc.

The source code used is taken from here http://86.84.251.44/cgi-bin/yabr.cgi  (another open source similar project).

The mobile app used to control it is called Bluetooth RC Controller.

The very first thing to check is the MPU6050 address. It could be 0x68 or 0x69. You have to adapt the following line int gyro_address = 0x68; to correct value.

Then you need to adapt int acc_calibration_value = -235; . To get your value you can use YABR_hardware_test code. Upload it to your robot, place it vertically on the table. It should not move at all - don't hold it with your hands. I used to place it on the corner of the table resting on the frame between the wheels. Run the code YABR_hardware_test, it will do a hardware check, and will display calibration value if your gyro has been found. Remember that value and put it into robot code before uploading it.