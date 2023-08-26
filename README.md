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

