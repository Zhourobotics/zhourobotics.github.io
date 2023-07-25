---
layout: page
title: Selective Comms
description: "Photo source: ohm-advisors"
img: assets/img/select_comms.png
importance: 9
category: past
---

## Reducing communication by self-triggered control and forming subteams

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <iframe width="370" height="210" src="https://www.youtube.com/embed/UcsRCc9cfns" frameborder="0" allowfullscreen></iframe> &nbsp;&nbsp;
        <iframe width="370" height="210" src="https://www.youtube.com/embed/YHz-NRubaAA" frameborder="0" allowfullscreen></iframe>
    </div>    
</div>



Many challenges exist in the long-term autonomy of multi-robot systems, such as limited onboard battery capacity, heavy computation and communication load, and dangerous and uncertain outer environments. Among these challenges, our research focuses on **reducing communication costs** during coordination. Particularly, leveraging **self-triggered control**, we designed a **"when to communicate"** strategy that decides when a robot in the team should communicate to seek up-to-date information and when it is safe to operate with possibly outdated information. Even though the communication is restricted, this self-triggered strategy achieves similar performance to the all-time communication strategy, in theory, simulations, and a proof-of-concept experiment. To further reduce communication costs, we devised a **"who to communicate with"** strategy by forming robot subteams. We proposed a **polynomial-time assignment algorithm** that provides a provably **near-optimal performance** even though the robots can only communicate within subteams.

[ICRA'17](https://ieeexplore.ieee.org/abstract/document/7989244), [T-ASE'18](https://ieeexplore.ieee.org/abstract/document/8466114): Active target tracking with self-triggered communications in multi-robot teams (left video). <br>
[ICRA'20+T-RO'19](https://ieeexplore.ieee.org/abstract/document/8747443): Sensor assignment algorithms to improve observability while tracking targets (right video).
