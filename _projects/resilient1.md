---
layout: page
title: Resilient Coordination 
description: 
img: assets/img/resilient_drone.png
importance: 5
category: current
---

## Countering attacks and failures through resilient coordination

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <iframe width="370" height="210" src="https://www.youtube.com/embed/T0Hb0UURCLM" frameborder="0" allowfullscreen></iframe> &nbsp;&nbsp;
        <iframe width="370" height="210" src="https://youtube.com/embed/hKOrFYUVjlo" frameborder="0" allowfullscreen></iframe>
    </div>    
</div>

Most of the research on robot resiliency focuses on countering deceptive attacks that mislead the robot team. Instead, we have so far focused against _denial-of-service (DoS)_ attacks and failures that can make robots fail or compromise their sensors. We aimed at guaranteeing team performance even if some robots in the team get DoS attacks. To this end, we formulated **game-theoretic problems** between the robots and the adversary, and designed **the first provably near-optimal approximation algorithms for robust combinatorial optimization** in various settings including centralized, decentralized communication and short-horizon, long-horizon planning. These algorithms enabled **DoS-resilient multi-robot planning** in data collection scenarios such as target tracking and environmental exploration. Apart from sensor attacks, the communications among robots can be easily jammed and disrupted by the adversary. Thus, we have recently investigated **near-optimal resilient algorithms** to protect the team performance from both _sensor and communication attacks/failures_.

Besides the aforementioned resilient algorithms that can **withstand** attacks/failures, I am also interested in how robots should react to and recover from attacks/failures. To this end, we developed a resilient coordination framework that enables robots to **adapt and recover** by reconfiguring team resources to compensate for the performance loss induced by robot failures.

[RA-L+ICRA'19](https://ieeexplore.ieee.org/abstract/document/8534468): Robust submodular maximization against robot/sensor attacks/failures; <br>
[ICRA'20](https://ieeexplore.ieee.org/document/9197243), [T-RO](https://ieeexplore.ieee.org/abstract/document/9763059): Decentralized (clique-based) robust submodular maximization against robot/sensor attacks/failures (left video);  <br>
[RA-L'21](https://ieeexplore.ieee.org/abstract/document/9431677): Distributed (consensus-based) robust submodular maximization against robot/sensor attacks/failures;  <br>
[RSS'20](https://roboticsconference.org/2020/program/papers/95.html), [full version](https://arxiv.org/abs/2003.13896): Robust team orienteering over a longer planning time against robot/sensor attacks/failures;  <br>
[ACC'22 invited paper, full version](https://arxiv.org/abs/2109.09838): Robust monotone maximization against robot/sensor and communication attacks/failures; <br>
[IROS'20](https://ieeexplore.ieee.org/document/9340871): Resilient coordination to adapt to and recover from robot/sensor failures (right video).