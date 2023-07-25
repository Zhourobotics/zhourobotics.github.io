---
layout: page
title: Formation Control
description: "Photo source: grahamowengallery"
img: assets/img/canada-geese.jpg 
importance: 10
category: past
---

## Saving energy in team formation by distributed model predictive control


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/flocking1.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/flocking2.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/flocking3.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

We design a **distributed model predictive control (MPC)** strategy to achieve flocking of multi-agent systems. Based on the relative motion between each pair of neighboring agents, we introduce a **neighbor screening protocol**, by which each agent only focuses on its neighbors, which have the relative motion that violates the formation of flocks. Then, a truly distributed MPC flocking algorithm is designed with consideration of neighbor screening mechanism. Specifically, at each sampling instant, each agent monitors the information in the networked system, finds its neighbors to form its subsystem, determines the screened neighbor set, and optimizes its plan by collecting the position states within the screened subsystem. Geometric properties of the optimal path are used to guarantee the formation of the flock without inter-agent collision. Finally, the performance and advantage of the proposed distributed MPC flocking strategy are vividly verified by the simulation results.

[IJRNC'17](https://onlinelibrary.wiley.com/doi/abs/10.1002/rnc.3606): Distributed model predictive control for multi-agent flocking via neighbor screening optimization (figures above). <br>
[IET'15](https://ietresearch.onlinelibrary.wiley.com/doi/full/10.1049/iet-cta.2014.1357): Distributed model predictive control for consensus of sampled-data multi-agent systems with double-integrator dynamics. <br>
[CCC'15](https://ieeexplore.ieee.org/document/7260840): Cooperative control of linear systems with coupled constraints via distributed model predictive control.

