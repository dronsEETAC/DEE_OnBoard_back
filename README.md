# On Board
## 1. General description
The modules in this block run in the on board computer (Raspberry Pi) to control different devices in the drone platform (autopilot, camera, leds, etc.). All on board modules are developed in Python. 
Each of the modules in this block has a GitHub repo where you can find the code together with a description, installation instructions and demos. These are the repos:
* *Autopilot service*:
[![DroneEngineeringEcosystem Badge](https://img.shields.io/badge/DEE-AutopilotService-brightgreen.svg)](https://github.com/dronsEETAC/DroneAutopilotDEE) an on-board module that controls the autopilot to execute the commands coming from other modules (arm, takeoff, go to position, etc.).    

* *Camera service*:
[![DroneEngineeringEcosystem Badge](https://img.shields.io/badge/DEE-CameraService-brightgreen.svg)](https://github.com/dronsEETAC/CameraControllerDEE) an on-board module that controls the on-board camera to execute the commands coming from other modules (take a picture, get the video stream, etc.)       
   
* *LEDs service*:
[![DroneEngineeringEcosystem Badge](https://img.shields.io/badge/DEE-LEDsService-brightgreen.svg)](https://github.com/dronsEETAC/LEDsControllerDEE) an on-board module that controls the LEDs of the drone platform to inform of the status of the drone platform, or a servo installed in the platform, as required by other modules.  
    
* *Monitor*:
[![DroneEngineeringEcosystem Badge](https://img.shields.io/badge/DEE-Monitor-brightgreen.svg)](https://github.com/dronsEETAC/MonitorDEE) records on board data for future analysis (for instance, all the messages send through the brokers.    
## 2. Python and PyCharm
In order to run and contribute to the modules in this block you need to install versión 3.7 of Python. We recomend you to use PyCharm as IDE for development in Python.
## 3. Operation modes
All services in this block can be run in simulation mode and also in production mode. To use the service in simulation mode, clone the repo in your computer and install de requirements. Be also sure that you have running the internal broker at "localhost:1884". When running the service you must specify the communication and operation mode and also which broker must be used as external broker. To do that you must edit the run/debug configuration in PyCharm, as shown in the image, in order to pass the required arguments to the script implementing the service. At least two parameters are required: connection_mode (global or local) and operation_mode (simulation or production). In case of global communication mode, a third argument is requiered indicating the external broker to be used. The different options for ths third argument are shown in this table:
options for external broker (third argument) |    
--- | ---
hivemq | broker.hivemq.com:8000 with websockets    
hivemq_cert | broker.hivemq.com:8884 with secure websockets    
classpip-cred |classpip.upc.edu:8000 with websockets and credentials (in the fourth and fifth arguments)   
classpip_cert | classpip.upc.edu:8883 with secure websockets and credentials (in the fourth and fifth arguments)   
localhost | localhost:8000 with websockets   
localhost_cert | localhost:8883 with secure websockets   

options for external broker (third argument) | #1 | #2 | #3 | #4 | #5 | #6 | #7 | #8 | #9 | #10 | #11
--- | --- | --- | --- |--- |--- |--- |--- |--- |--- |--- |---
Seconds | 301 | 283 | 290 | 286 | 289 | 285 | 287 | 287 | 272 | 276 | 269

In case the external broker requieres credentials, two additional parameters must be includes (username and password). The figure shows and example where the external broker does not requires credentials.   
![autopilotServiceConfiguration](https://user-images.githubusercontent.com/100842082/212955034-2a9fdd8d-e654-405e-951d-605479ba9928.png)
   
MODIFICAR LO SIGUIENTE CUANDO EL SOFTWARE ON BOARD ESTE EN DOCKER
To run the autopilot service in production mode you will need the boot.py script that you will find in the main repo of the Drone Engineering Ecosystem. Follow the instruction that you will find in that repo.
[![DroneEngineeringEcosystem Badge](https://img.shields.io/badge/DEE-MainRepo-brightgreen.svg)](https://github.com/dronsEETAC/DroneEngineeringEcosystemDEE)

