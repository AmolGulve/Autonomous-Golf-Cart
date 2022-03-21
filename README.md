# Autonomous-Golf-Cart
![Golf_1](https://user-images.githubusercontent.com/91168380/134340803-c8f8d126-19d8-417f-809b-033782340e08.jpg)
Welcome!!

I am leading this project to focus on building an autonomous golf cart as part of my mentorship involvement with Robotics Group. We were donated an old 2009 EZ-Go Golf cart and have refurbished the chassis and frame components. We still have a long way to go and during this development process I will be mentoring the students and learning new tools and software’s to develop the autonomy in the golf cart using map-based decision-making capability.

**Goals:**

Develop level 4 autonomy in a dedicated area based on deep-learning and map-based decision-making tools.

**The phases in this project are:**
1.	Golf cart rehab 
2.	Hardware development
3.	Computer and software development
4.	System integration
5.	Map-based decision making
6.	Yolo Object detection with ROS

**Golf cart rehab**

- Golf Cart Tare down

- Fix Frame and Mechanics

- Includes rust removal and protection

- Order and Replace Parts as needed

- Treat parts for rust protection (paint etc)

- Order hardware needed for frame reassemble

- Reassemble Frame and Basic Mechanics

- Determine components and parts needed for manual operation (for later computer control)

- Reassemble electrical wiring for basic operation

**Hardware development**

a)	Drive by Wire:

Following concept was decided based on the condition of the golf cart and the amount of steering force required to steer the vehicle. Linear actuator with a potentiometer is used to provide position feedback to the computer to make the decision.

![image](https://user-images.githubusercontent.com/91168380/139088064-c8d1cf72-e4c4-46b3-b703-34d55c4ae55d.png)

b)	Brakes:

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

![image](https://user-images.githubusercontent.com/91168380/139088540-68cc2681-6ffe-4d46-818c-a80f294fc2e0.png)

ROS and Arduino will be used as sub-controllers to connect with Nvidia Jetson as shown below.

![Ros_arduino](https://user-images.githubusercontent.com/91168380/139174847-611eed5d-9777-4c33-97f9-f3e52ef59292.png)

**Map based decision making**

Studying various software’s available to better integrate with the hardware based on the following strategy.

![image](https://user-images.githubusercontent.com/91168380/139088646-ae8011ad-5b48-4496-9508-0858804beb11.png)


**About ROS**

ROS Information
Below you will find information about all the ROS packages, nodes, topics planned to be used in this project.

Packages & Nodes
Here is a list of packages. Underneath each package are nodes in that package.

**autopilot**
The autopilot node is the brain of the self-driving car. It uses end-to-end deep learning to predict the steering, acceleration and braking commands of the vehicle. while subscribes to the camera feed. (Node currently functioning) The Arduino subsribes to the steering_cmds and controls the steering accordingly.

Nodes:
autopilot
visualization
Publishes
/vehicle/dbw/steering_cmds/
/vehicle/dbw/cruise_cmds/
Subscribes
/camera_node/image_raw
/camera_node/image_sim

**object_detection**
YOLO (You Only Look Once) realtime object detection system.
The golf cart uses Python and the machine learning library Python. The first step is to convert the latest version of YOLO (v3) to Keras. 
I created an object detection node in ROS. This node listens to the camera input and performs object detection. Also, the node publishes the detection results with a specific message type, and it can also publish detection visualization. The result looks something like this: 
![image](https://user-images.githubusercontent.com/91168380/159380264-145689eb-5aa0-40de-a275-01102133f5b9.png)

Nodes:
object_detection_node
Publishes
/detection/object/detection_visualization/
/detection/object/detection_result
Subscribes:
/camera_node/image_raw

**gps**
Used for localization. Currently using the Adafruit GPS module, serial communication.

Nodes:
gps_receiver
nmea_topic_driver
nmea_topic_serial_reader
The GPS package manages and publishes the data received from a GPS module connected via serial. The package

Publishes:
/sensor/gps/fix
/sensor/gps/vel
data_logger




