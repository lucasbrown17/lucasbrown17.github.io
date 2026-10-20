---
layout: default
title: Projects
permalink: /projects
---
# Rubik's Cube Solver
![image](/RubikCube.gif){: style="float: center"}
Having worked through the beginner's method of solving of the Rubik's Cube, I could tell there were an infinite number of more interesting ways to solve the complex puzzle and not just for a 3x3 cube.

I built a python qt based simulator (shown above), with the cube simulated in 3d space and projected onto the 2d GUI you see above. The application is object orientated, using the observer design pattern for visualisation and the strategy pattern for moves and solvers. 

With the simulation completed, I am building the [Thistlewaite](https://www.jaapsch.net/puzzles/thistle.html) solver algorithm. In parallel, I am building a Reinforcement Q-learning solver.

Skills: Mathematical Modelling; Python; Project Management


# Gas Introduction Module Controllers
<p float="left">
  <img src="/sector8_install(1).jpg" width="350" />
  <img src="/model_comp_102267.png" width="350" /> 
</p>
MAST-U is the largest working Fusion device in the UK. I am upgrading and optimising the system managing the density and heat exhaust of the plasma. The objective is to design bespoke robust and accurate gas flow control systems.

To acquire real-time data, I led a package to design and install diagnostics, working with operations leaders to manage timelines.

To further investigate the system dynamics, I analysed past data. Using Machine Learning techniques, I identified quantitive models for controller development and simulation. 

To build better models and validate control systems, I designed a bench test. I validated the controller through Hardware-in-the-loop testing using a Zynq FPGA-CPU board. 

To benchmark Machine Learning gas flow modelling techniques, I built Bayesian Filters. See the [paper](https://www.sciencedirect.com/science/article/pii/S0920379625001334).

Skills: System Identification/Machine Learning; Python; C++; MATLAB/Simulink; Team Management

Collaborators: Adam Parrott; Dr Charlie Vincent; Hudson Baker (UKAEA)

# ROS2 National Instruments Driver
![image](/comau_aluminium_beam.jpg){: style="float: center"}

Future fusion machines will have bespoke and flexible parts that need frequent replacement due to neutron bombardment. The handling test rig experiments novel control techniques that reduce bending and avoid collisions. I built a configurable real-time ROS2 C++ driver for National Instruments cDAQ equipment. The event driven acquisition node publishes data from instrumentation such as strain gauges, force-torque sensors and load cells up to 500Hz. I also synchronised the acquisition equipment with Precision Time Protocol.

Skills: ROS2; ROS2 Control; Real-Time C++; National Instruments Acquisiton; PTP

Collaborators: Dr Nando Milella; Adam Slater (UKAEA)


# Master's Thesis: NeuroGen
<p float="center">
  <img src="/NeuroGen_top Block.png" height="150" />
  <img src="/Perfboard implementation.jpg" height="350" /> 
</p>
I built a Digital to Analog Converter for biological signal emulation. To simulate bio-signals, the converter required a high dynamic range and large broadband. Using a Sigma Delta converter architecture implemented on an FPGA, I built the NeuroGen bio-emulator. I validated the system in MATLAB/Simulink.

Skills: Electronic Design; FPGA Implementation; MATLAB/Simulink

Collaborators: Prof. Tim Constandinou (Imperial College London)


# Co-operative Handling
![image](/CoopHandling.gif){: style="float: center"}

This research looked at whether dual actuators would solve the problem discussed in the [NI driver section](#ros2-national-instruments-driver). I created the ROS2 application, integrating the Universal Robot, FT sensor and external actuator. We then developed feed forward optimal control schemes and experimented them using a bespoke Graphical User Interface. 

Skills: Python; Julia; C++; Beckhoff PLC; Motor Control; ROS2

Collaborators: Sam Herschmann; Wei Leong; Nando Milella (UKAEA)

# Localisation Gazebo Simulation
<p float="left">
  <img src="/gazebo_snapshot.jpg" width="350" />
  <img src="/WEST2-24072025.JPG" width="350" /> 
</p>
I worked at the flagship French Fusion Research Facility, embedded in the Robotics team. I developed a containerised, configurable simulation platform for controller validation. The project's application was for remote maintenance in highly radioactive environments, making validation critical. The simulation platform could be configured through a GUI, allowing users to move elements and activate camera localisation. 

Skills: ROS2; C++; Gazebo/Ignition; Docker; Project Management

Collaborators: Dr David Busson (CEA IRFM); Matthew Preistly (UKAEA)