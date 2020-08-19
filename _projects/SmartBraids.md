---
title: "Trotting Simulation"
excerpt: "MPC Based Torque Control Simulation of a Quadrupedal Robot<br/><img src='/images/smartBraid500.png'>"
collection: portfolio
---

At Carnegie Mellon University's Robomechanics Lab, I helped create trotting simulations of a quadrupedal robot in Pybullet based on Ghost Robotics’ Spirit 40 quadruped. Inspired by desirable results from the MIT Cheetah 3 quadruped, I investigated the viability of using model predictive control as a low-level controller for legged locomotion. I gradually progressed the robot simulation in PyBullet from standing to trotting the robot by developing controllers for stance and swing phases of the respective legs during the gait cycle. 

To stand, I implemented torque control using model predictive control to optimize for desired ground reaction forces during the stance phase. This required calculating the leg jacobians which was not available through Ghost Robotics. Instead, I consulted values from the URDF file and generated the values through Matlab. For trotting, a leg swing trajectory was generated using parabolic and Bézier curves and implemented with position control. The parabolic trajectory appeared more stable for trotting at low speed.

# <iframe width="560" height="315" src="https://www.youtube.com/embed/47T9I_wnEE4" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
# <img src='/images/smartBraidDiagram.png'>

<video  style="display:block; width:100%; height:auto;" autoplay controls loop="loop">
    <source src="{{ site.baseurl }}/media/smartBraids/spiritsimwalk.mp4" type="video/mp4" />
    # <source src="{{ site.baseurl }}/media/smartBraids/SmartBraidGuide.ogv" type="video/ogg" />
    # <source src="{{ site.baseurl }}/media/smartBraids/SmartBraidGuide.webm" type="video/webm" />
</video>

<!-- [Picture of jig in CAD] -->
