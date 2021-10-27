# Autonomous-Golf-Cart
![Golf_1](https://user-images.githubusercontent.com/91168380/134340803-c8f8d126-19d8-417f-809b-033782340e08.jpg)
Welcome!!

This project is focused on building an autonomous golf cart with university students as part of my mentorship involvement with Robotics Group. We were donated an old 2009 EZ-Go Golf cart and have recreated the chassis and frame components. We still have a long way to go and during this development process I will be mentoring the students and learning new tools and software’s to develop the autonomy in the golf cart using map-based decision-making capability.

**Goals:**

Develop level 4 autonomy in a dedicated area based on deep-learning and map-based decision-making tools.

**The phases in this project are:**
1.	Golf cart rehab 
2.	Hardware development
3.	Computer and software development
4.	System integration
5.	Map-based decision making

**Golf cart rehab**

Golf Cart Tare down
Fix Frame and Mechanics
Includes rust removal and protection
Order and Replace Parts as needed
Treat parts for rust protection (paint etc)
Order hardware needed for frame reassemble
Reassemble Frame and Basic Mechanics
Determine components and parts needed for manual operation (for later computer control)
Reassemble electrical wiring for basic operation

**Hardware development**

a)	Drive by Wire
Following concept was decided based on the condition of the golf cart and the amount of steering force required to steer the vehicle. Linear actuator with a potentiometer is used to provide position feedback to the computer to make the decision.

![image](https://user-images.githubusercontent.com/91168380/139088064-c8d1cf72-e4c4-46b3-b703-34d55c4ae55d.png)

b)	Brakes
Brake by wire will follow the similar approach as the drive by wire using a linear actuator.

![image](https://user-images.githubusercontent.com/91168380/139088154-2997af85-dea4-40b3-8803-989cea08aceb.png)

**Computer and software development**

a.	Choose control and processing computer/s

b.	Choose and order motor controller (for both manual and computer control)

c.	Decide and order initial sensors and software

      i.	1st and main Camera
      ii.	GPS and IMU
      iii.	Onboard video monitor for driver
      
d.	Create, mount, wire-up test board

e.	Start Programming for simple tracking with just video overlay output telling driver where to go (i.e. cross hair alignment and other data)

f.	Test programming outside on available platforms 

**System Integration**

Finish adding electrical controls and prepare for computer control of them.
Create finish hard mounting, wiring of sensors, electronics, and computer parts to golf cart.
ROS and Arduino will be used as sub-controllers to connect with Nvidia Jetson as shown below.

![image](https://user-images.githubusercontent.com/91168380/139088540-68cc2681-6ffe-4d46-818c-a80f294fc2e0.png)

**Map based decision making**

Studying various software’s available to better integrate with the hardware based on the following strategy.

![image](https://user-images.githubusercontent.com/91168380/139088646-ae8011ad-5b48-4496-9508-0858804beb11.png)





