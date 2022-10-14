# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

### Step1:
Import the required packages
### Step2:
Assign the value for X axis and Y axis 
### Step3:
write the program to move the Robot
### Step4:
Write the program to record video
### Step5:
Run the program to move the robot

## Program:
```python
#Developed by: Naveenaa A.K
#Register number: 22003091

from robomaster import robot
import time
from robomaster import camera


if _name_ == '_main_':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_led = ep_robot.led

for i in range(10):
    ep_led.set_led(comp="all",r=255,g=0,b=0,effect="on")   
    time.sleep(2)

    ep_led.set_led(comp="all",r=0,g=255,b=100,effect="on")   
    time.sleep(2)

    ep_led.set_led(comp="all",r=0,g=0,b=255,effect="on")   
    time.sleep(2)

    ep_chassis = ep_robot.chassis 

    ep_camera = ep_robot.camera

     
 
    ep_chassis.move(x=3.9, y=0, z=0, xy_speed=0.75).wait_for_completed()

    ep_chassis.drive_speed(x=0.2,y=0,z=20)
    time.sleep(7)

    ep_chassis.move(x=2.5, y=0, z=0, xy_speed=0.75).wait_for_completed()

    ep_chassis.move(x=0, y=0.1, z=0, xy_speed=0.75).wait_for_completed()

    ep_chassis.drive_speed(x=1,y=0,z=40)
    time.sleep(7)

    ep_chassis.move(x=0, y=0.1, z=0, xy_speed=0.75).wait_for_completed()



    ep_robot.close()
```
## Initial Position:
![WhatsApp Image 2022-10-14 at 11 19 38 AM](https://user-images.githubusercontent.com/113497406/195772390-0bede9ec-8445-4014-939c-c0efd71de6c0.jpeg)


## Final Position:
![WhatsApp Image 2022-10-14 at 11 19 38 AM (1)](https://user-images.githubusercontent.com/113497406/195772473-879fa271-9d3a-4a8d-be34-4ffe0740ee53.jpeg)


## Output:
https://user-images.githubusercontent.com/113497406/193526046-881d0737-b291-4685-8568-2e78887d379a.mp4


    
### Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.
