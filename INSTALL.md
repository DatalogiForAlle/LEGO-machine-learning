How to get the Swing-robot running
==================================

The project was developed as a student project in the winter
2018-2019. The project is documented in the student report
`Reinforcement_Learning_with_LEGO_Mindstorms.pdf`

Dependencies
------------

As the project was developed in 2018-2019, it depends on Python 3.5.3
and older versions of the used packages. Especially it depends on rpyc
version 3.3.0 (or: alternatively the robots firmware needs to be upgraded!). 

The important thing is that RPYC on the robot and the host computer is
the same version!

To use Python 3.5.3, please install `asdf` and the asdf-plugin for Python.


Installation
------------
When `asdf` is installed the rest of the dependencies are managed by
`pipenv`. To install them, simply run:

 `pipenv install --dev`
 
Preparing the robot
-------------------

 1. Connect through USB. This works well on Ubuntu. Set the Ubuntu machines IP Adress to 10.42.0.1 as the Robot wants to take the 10.42.0.3 IP address (this can be done in the Ubuntu Network manager GUI)
 
 2. Open connection to the robot through `ssh robot@ev3dev.local` or `ssh robot@10.42.0.3`
 
 3. The password to the `robot`-user is `maker`
 
 4. Once logged in, start RPYC through `./rpyc_server.sh`
 
 5. Now the robot is ready and listens for RPYC commands from the host computer
 

Starting the program on the desktop
-----------------------------------

 1. Open jupyter notebook by running `pipenv run jupyter notebook` (You need to stand in the LEGO-machine-learning directory)
 
 2. Open the file `src/swing_robot/CMA_Swing_Robot.ipynb`
 
 3. Run the entire notebook.
 
 4. The robot will start training and will save the training data in a
    `.pickl` file, usually it takes 4-5 hours of training to get a
    good swing.
    
 5. In the last part of the Jupyter file, there's code to read in the
    model from the `.pickl` file and run the trained model.
