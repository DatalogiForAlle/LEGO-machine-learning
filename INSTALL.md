Dependencies
------------

This was developed in 2018-2019, and depends on Python 3.5.3 and older versions of the used packages. Especially it depends on rpyc version 3.3.0 (alternatively the robots needs to be upgraded)

To use Python 3.5.3, please install `asdf` and the asdf-plugin for Python.


Installation
------------
When `asdf` is installed the rest of the dependencies are managed by `pipenv`. To install them, simply run:

 `pipenv install --dev`
 
Connecting to the robot
-----------------------

 - Connect through USB. This works well on Ubuntu. Set the Ubuntu machines IP Adress to 10.42.0.1 as the Robot wants to take the 10.42.0.3 IP address (this can be done in the GUI)
 
 - Open connection to the robot through `ssh robot@ev3dev.local` or `ssh robot@10.42.0.3`
 
 - The password is `maker`
 
 - Once logged in, start RPYC through `./rpyc_server.sh`
 
 
Starting the program on the desktop
-----------------------------------

 - Open jupyter notebook by running `pipenv run jupyter notebook` (You need to stand in the LEGO-machine-learning directory)
 
 - Open the file `src/swing_robot/CMA_Swing_Robot.ipynb`
 
 - Run it >>
