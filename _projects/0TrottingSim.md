---
title: "Trotting Simulation"
excerpt: "MPC based torque control simulation of a quadrupedal robot<br/><img src='/images/spiritsim.png'>"
collection: portfolio
order: 1
---

At Carnegie Mellon University's Robomechanics Lab, I developed trotting simulations of a quadrupedal robot in Pybullet based on Ghost Robotics’ Spirit 40 quadruped. Inspired by desirable results from the MIT Cheetah 3 quadruped, I investigated the viability of using model predictive control (MPC) as a low-level controller for legged locomotion. MPC predicts the effect of control actions on the future system state, subject to constraints, and selects the course of actions which return the optimal future states. This is powerful because it allows the robot to think ahead and predict the future rather than only reacting, which is vital for executing dynamic movements. I implemented torque control using MPC to optimize for desired ground reaction forces and generated joint torques by calculating leg jacobians based off the URDF file for Spirit 40. 

<p align="center">
<br/><img src='/images/controlframework.PNG'>
</p>

I gradually progressed the robot simulation in PyBullet from standing to trotting the robot by developing controllers for stance and swing phases of the respective legs during the gait cycle. 

<video  style="display:block; width:100%; height:auto;" autoplay controls loop="loop">
    <source src="{{ site.baseurl }}/media/spiritsimwalk.mp4" type="video/mp4" />
</video>

<!-- [Picture of jig in CAD] -->
