---
layout: page
title: VLMs for Air Ground Systems 
description: 
img: assets/img/airground1.jpg
importance: 2
category: current
---

#### *Project Lead: [Bill Cai](https://scholar.google.com/citations?user=9OTtpc8AAAAJ&hl=en)*

## LLM-Land: Large Language Models for Context-Aware Drone Landing

<div class="row">
    <div class="col-sm-7 mt-3 mt-md-0">
        {% include figure.html path="assets/img/land.png" title="example image" class="img-fluid rounded z-depth-1" style="height: 210px; object-fit: cover;" %}
    </div>
    <div class="col-sm-5 mt-3 mt-md-0">
        <iframe width="100%" height="200" src="https://www.youtube.com/embed/9yGEpqmCtdA" frameborder="0" allowfullscreen></iframe>
    </div>    
</div>

Autonomous landing is essential for drones deployed in emergency deliveries, post-disaster response, and other large-scale missions. By enabling self-docking on charging platforms, it facilitates continuous operation and significantly extends mission endurance. However, traditional approaches often fall short in dynamic, unstructured environments due to limited semantic awareness and reliance on fixed, context-insensitive safety margins. To address these limitations, we propose a hybrid framework that integrates large language models (LLMs) with model predictive control (MPC). Our approach begins with a vision–language encoder (VLE) (e.g., BLIP), which transforms real-time images into concise textual scene descriptions. These descriptions are processed by a lightweight LLM (e.g., Qwen 2.5 1.5B  or LLaMA 3.2 1B) equipped with retrieval-augmented generation (RAG) to classify scene elements and infer context-aware safety buffers, such as 3 meters for pedestrians and 5 meters for vehicles. The resulting semantic flags and unsafe regions are then fed into an MPC module, enabling real-time trajectory replanning that avoids collisions while maintaining high landing precision. We validate our framework in the ROS-Gazebo simulator, where it consistently outperforms conventional vision-based MPC baselines. Our results show a significant reduction in near-miss incidents with dynamic obstacles, while preserving accurate landings in cluttered environments. [Preprint](https://arxiv.org/abs/2505.06399).


## An Energy-Aware Routing Algorithm for Mobile Ground-to-Air Charging

<div class="row">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/routing.png" title="example image" class="img-fluid rounded z-depth-1" style="height: 210px; object-fit: cover;" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        <iframe width="100%" height="190" src="https://www.youtube.com/embed/eYPMPYThhKE" frameborder="0" allowfullscreen></iframe>
    </div>    
</div>

We investigate the problem of energy-constrained planning for a cooperative system consisting of an Unmanned Ground Vehicle (UGV) and an Unmanned Aerial Vehicle (UAV). In scenarios where the UGV serves as a mobile base to ferry the UAV and as a charging station to recharge the UAV, we formulate a novel energy-constrained routing problem. To tackle this problem, we design an energy-aware routing algorithm, aiming to minimize the overall mission duration under the energy limitations of both vehicles. The algorithm first solves a Traveling Salesman Problem (TSP) to generate a guided tour. Then, it employs the Monte-Carlo Tree Search (MCTS) algorithm to refine the tour and generate paths for the two vehicles, taking into account multiple physical constraints such as charging speed, total energy expenditure, travel time, and other operational requirements. We evaluate the performance of our algorithm through extensive simulations and a proof-of-concept experiment. The results show that our algorithm consistently achieves near-optimal mission time and maintains fast running time across a wide range of problem instances. [ISRR'24](https://arxiv.org/abs/2310.07729).
