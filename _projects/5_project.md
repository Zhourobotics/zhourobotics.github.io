---
layout: page
title: Adversarial Planning
description: 
img: assets/img/adver_plan.png
importance: 5
category: current
---

## Tree search application in robot-target game

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/tree_search.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

We introduce and study the problem of planning a trajectory for an agent to carry out a scouting mission while avoiding being detected by an adversarial guard. This introduces a multi-objective version of classical visibility-based target search and pursuit-evasion problem. In our formulation, the agent receives a positive reward for increasing its visibility (by exploring new regions) and a negative penalty every time it is detected by the guard. The objective is to find a finite-horizon path for the agent that balances the trade off between maximizing visibility and minimizing detectability.

We model this problem as a **discrete, sequential, two-player, zero-sum game**. We use two types of game tree search algorithms to solve this problem: **minimax search tree and Monte-Carlo search tree**. Both search trees can yield the optimal policy but may require possibly exponential computational time and space. We propose several pruning techniques to reduce the computational cost while still preserving optimality guarantees. Simulation results show that the proposed strategy prunes approximately three orders of magnitude nodes as compared to the brute-force strategy. We also find that the Monte-Carlo search tree saves approximately one order of computational time as compared to the minimax search tree.

[ICRA'19](https://ieeexplore.ieee.org/document/8794305), [AURO'21](https://link.springer.com/article/10.1007/s10514-020-09963-4): Game tree search for minimizing detectability and maximizing visibility.

## Spoofing strategy in robot-target game

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/spoof1.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/spoof2.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

We study the problem of **designing spoofing signals to corrupt and mislead the output of a Kalman filter**. Unlike existing works that focus on detection and filtering algorithms for the observer, we study the problem from the attacker’s point-of-view. In our model, the attacker can corrupt the measurements by adding spoofing signals. The attacker seeks to create a separation between the estimate of the Kalman filter with and without spoofing signals. We present a number of results on how to generate such spoofing signals, while minimizing the signal magnitude. The resulting algorithms are evaluated through simulations along with theoretical proofs.

[ACC'18](https://ieeexplore.ieee.org/document/8430817), [full version](https://arxiv.org/abs/1710.02442): Strategies to inject spoofed measurement data to mislead Kalman filter.
