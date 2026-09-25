---
layout: page
title: Foundation Models for Air-Ground Systems
description: 
img: assets/img/airground1.jpg
importance: 2
category: current
---

#### *Project Lead: [Bill Cai](https://scholar.google.com/citations?user=9OTtpc8AAAAJ&hl=en)*

## AGT-CV: An Aerial-Ground Team Cross-View Dataset for Heterogeneous Robot Teams in Unstructured Environments

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/research/agtcv.jpg" title="AGT-CV dataset" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

Heterogeneous air-ground robot teams combine complementary sensing modalities, mobility characteristics, and spatial viewpoints that can significantly enhance perception in complex outdoor environments. However, progress in multi-robot collaborative perception has been constrained by the lack of real-world datasets featuring overlapping multi-modal observations from platforms operating in unstructured terrain. We present a real-world multi-robot collaborative perception dataset collected using a Clearpath Husky UGV and an Autel EVO II UAV across diverse unstructured environments, including forest trails, rocky paths, muddy terrain, snow piles, and grass-covered fields. The ground platform provides 3D LiDAR, stereo camera, IMU, and GPS data, while the aerial platform contributes RGB imagery, thermal/infrared observations, and GPS from a complementary overhead viewpoint, allowing for rich cross-modal and cross-view perception. The dataset is collected in 4 unique environments, with over 13,000 synchronized frames across approximately 29 minutes of operation, and includes both SAM 3-based zero-shot segmentation and over 8,000 manually labeled images. A unique aspect of the dataset is its early-spring collection period, during which sparse tree canopies allow the aerial robot to partially observe the ground robot and terrain through the trees, allowing for occlusion-aware collaborative perception. Unlike prior multi-robot datasets that focus on SLAM or simulated cooperative driving, our dataset is specifically designed to support research on cross-view perception, air-ground viewpoint fusion, traversability estimation, and collaborative scene understanding in real off-road environments. [ECCV'26 CDEL Workshop (Oral)](https://arxiv.org/abs/2605.06478).

## Project SCOUT: Interceptor Drone for Perimeter Defense

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/research/scout.png" title="SCOUT perception pipeline" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="row justify-content-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        <iframe width="100%" height="285" src="https://www.youtube.com/embed/OxrbMOGu-Kg" frameborder="0" allowfullscreen></iframe>
    </div>
</div>

The rapid proliferation of unauthorized unmanned aerial vehicles (UAVs) has created a growing need for robust, jamming-resistant counter-UAV systems for perimeter defense. This paper presents SCOUT (Spatial Computation for Optimized UAV Tracking), a ROS-integrated onboard perception and control framework for real-time aerial defense against incoming UAVs. SCOUT performs visual detection, target association, track filtering, and control command generation directly onboard the defender UAV, without relying on external sensing infrastructure or ground-station computation. To provide stable control inputs, the perception pipeline combines TensorRT-accelerated drone detection with ByteTrack-based association and a lightweight track-retention state machine. The state machine rejects abrupt target jumps and maintains short-term target continuity during temporary detection degradation, reducing unstable control responses caused by false detections or target switching. We evaluate the proposed architecture through an integrated hardware deployment executing a planar "goalkeeping" interception strategy, in which the defender UAV tracks the incoming target and adjusts its motion to maintain a blocking configuration near the protected boundary. Real-world flight results show that SCOUT maintains valid target detections for 92.2% of frames while operating at real-time onboard detection rates, demonstrating the feasibility of visual tracking and closed-loop control for UAV perimeter defense. [SSRR'26](https://arxiv.org/abs/2609.21005).

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
