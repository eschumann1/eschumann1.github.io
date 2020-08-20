---
title: "Trotting Simulation"
excerpt: "MPC Based Torque Control Simulation of a Quadrupedal Robot<br/><img src='/images/spiritsim.png'>"
collection: portfolio
order = 1
---

At Carnegie Mellon University's Robomechanics Lab, I developed trotting simulations of a quadrupedal robot in Pybullet based on Ghost Robotics’ Spirit 40 quadruped. Inspired by desirable results from the MIT Cheetah 3 quadruped, I investigated the viability of using model predictive control as a low-level controller for legged locomotion. I gradually progressed the robot simulation in PyBullet from standing to trotting the robot by developing controllers for stance and swing phases of the respective legs during the gait cycle. I implemented torque control using model predictive control to optimize for desired ground reaction forces during the stance phase. 

<video  style="display:block; width:100%; height:auto;" autoplay controls loop="loop">
    <source src="{{ site.baseurl }}/media/spiritsimwalk.mp4" type="video/mp4" />
</video>

<!-- [Picture of jig in CAD] -->
