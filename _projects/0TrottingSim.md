---
title: "Trotting Simulation"
excerpt: "MPC based torque control simulation of a quadrupedal robot<br/><img src='/images/spiritsim.png'>"
collection: portfolio
order: 1
---

At Carnegie Mellon University's Robomechanics Lab, I developed trotting simulations of a quadrupedal robot based on Ghost Robotics’ Spirit 40 quadruped. In a linux environment, I used Bullet for the simulation and Python for the control algorithms. Inspired by desirable results from the MIT Cheetah 3 quadruped, I investigated the viability of using model predictive control (MPC) as a low-level controller for legged locomotion. Within the general control framework, I assumed the footstep planner inputs and state estimation allowed a steady gait cycle and low contact forces on touchdown of the feet.

<p align="center">
<br/><img src='/images/controlframework.PNG'>
</p>

MPC predicts the effect of control actions on the future system state, subject to constraints, and selects the course of actions which return the optimal future states. This is powerful because it allows the robot to think ahead and predict the future rather than only reacting, which is vital for executing dynamic movements. 

<p align="center">
<br/><img src='/images/MPC.png'>
</p>

I gradually progressed the robot simulation in PyBullet from standing to trotting the robot by developing controllers for stance and swing phases of the respective legs during the gait cycle. To stand, I implemented torque control using model predictive control to optimize for desired ground reaction forces during the stance phase. This required calculating the leg jacobians based off the URDF file for Spirit 40. For trotting, a leg swing trajectory was generated using parabolic and Bézier curves and implemented with position control. The parabolic trajectory appeared more stable for trotting at low speed.


<video  style="display:block; width:100%; height:auto;" autoplay controls loop="loop">
    <source src="{{ site.baseurl }}/media/spiritsimwalk.mp4" type="video/mp4" />
</video>

<br/>

Since demonstrating stable trotting on a flat, level surface without optimizing the leg swing trajectory, I am interested in reformulating the MPC problem in the context of obstacle navigation such as leaping over a large boulder. A further improvement in the long run could involve the swing leg controller and foot step planner in terms of having the MPC controller inform foot placement decisions rather than having these modules isolated.
