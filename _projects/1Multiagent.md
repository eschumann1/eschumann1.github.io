---
title: "Resilient Multi-Agent Clustering and Formation"
excerpt: "Potential Field based methods for resilient multi-agent clustering and formation simulations <br/><img src='/images/multiagent.PNG'>"
collection: portfolio
---

For my MS in Computational Science and Engineering at Harvard, I designed and tested simulations in Python for clustering and formation in a multi-agent systems control course. I then proceeded to test the robustness of these methods against the presence of malfunctioning or malicious agents.

I was motivated by bio-inspired swarms to consider the formation problem based on the work by Guzel et al. in “A Novel Framework for Multi-Agent Systems Using a Decentralized Strategy” where a clustering behavior is defined for individual agents to aggregate, allocate a leader for pattern formation, and navigate a messy environment containing obstacles. 

The first problem unique to swarm robotics considered is the problem of aggregation or clustering, where early works implemented a procedure to send robots moving towards local centroids calculated based on the position of sensed neighboring robots. In my baseline simulation, clustering of a single swarm from random initial locations will require a force analysis and force based clustering algorithm to form a cluster as agents impose an attractive gravitational force on each other.

Once a leader is chosen, a circular pattern formation algorithm is implemented prior to moving the swarm. Obstacle avoidance will handled using the potential field algorithm to set a repulsive force on obstacles. Re-implementing the pattern formation algorithm will ensure the formation is adaptive and reformed after obstacle avoidance. This pattern formation algorithm for clustering utilizes the center of gravity (COG) of the group to estimate member locations. When any individual maneuvers to avoid obstacles, this causes others to adapt in order to keep formation.

<video  style="display:block; width:100%; height:auto;" autoplay muted controls loop="loop">
    <source src="{{ site.baseurl }}/media/formation.mp4" type="video/mp4" />
</video>

<br/>

Whenever the leader observes an agent too far away from its formation position, it must check that the agent is legitimate. The leader will check for an obstacle causing the distance and if the obstacle produces the necessary exertion of force on the agent to satisfy the distance. In the case of a stationary agent, that agent is promptly rejected from the swarm.

<video  style="display:block; width:100%; height:auto;" autoplay muted controls loop="loop">
    <source src="{{ site.baseurl }}/media/formation_malicious.mp4" type="video/mp4" />
</video>

<br/>

A basic obstacle avoidance scenario is tested where obstacles are assumed to remain stationary. The simplest approach is to turn a random direction and proceed. However, this does not ensure efficient behavior that leads towards reaching a goal. Instead, a potential field approach is used to explore locally optimum solutions by setting a repulsive force on obstacles and an attractive force on neighboring robots.

<video  style="display:block; width:100%; height:auto;" autoplay muted controls loop="loop">
    <source src="{{ site.baseurl }}/media/formation_malicious_obs.mp4" type="video/mp4" />
</video>

<br/>

Within the realm of swarm robotics, this framework attempts to perform navigation autonomously through networked robots that utilize sensing within an effective range to communicate and coordinate various activities such as obstacle avoidance or pursing a goal. There are numerous applications for these capabilities in the real world such as environmental monitoring and search and rescue.
