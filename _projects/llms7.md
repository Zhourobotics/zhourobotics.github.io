---
layout: page
title: LLMs for Multi-Robot Coordination
description: 
img: assets/img/drones.jpg
importance: 1
category: current
---

#### *Project Lead: [Peihan Li](https://scholar.google.com/citations?user=Qg7-Gr0AAAAJ&hl=en)*

## Large Language Models for Multi-Robot Systems: A Survey

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/LLMMRS.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

The rapid advancement of Large Language Models (LLMs) has opened new possibilities in Multi-Robot Systems (MRS), enabling enhanced communication, task planning, and human-robot interaction. Unlike traditional single-robot and multi-agent systems, MRS poses unique challenges, including coordination, scalability, and real-world adaptability. This survey provides the first comprehensive exploration of LLM integration into MRS. It systematically categorizes their applications across high-level task allocation, mid-level motion planning, low-level action generation, and human intervention. We highlight key applications in diverse domains, such as household robotics, construction, formation control, target tracking, and robot games, showcasing the versatility and transformative potential of LLMs in MRS.
Furthermore, we examine the challenges that limit adapting LLMs in MRS, including mathematical reasoning limitations, hallucination, latency issues, and the need for robust benchmarking systems. Finally, we outline opportunities for future research, emphasizing advancements in fine-tuning, reasoning techniques, and task-specific models. This survey aims to guide researchers in the intelligence and real-world deployment of MRS powered by LLMs. Based on the fast-evolving nature of research in the field, we keep updating the papers in the open-source [Github repository](https://github.com/Zhourobotics/LLM-MRS-survey). [Preprint](https://arxiv.org/abs/2502.03814).

## LLM-Flock: Decentralized Multi-Robot Flocking via LLMs and Influence-Based Consensus

<div class="row">
    <div class="col-sm-7 mt-3 mt-md-0">
        {% include figure.html path="assets/img/LLMFlockv2.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-5 mt-3 mt-md-0">
        <iframe width="100%" height="200" src="https://www.youtube.com/embed/8zcPYqjWzYo" frameborder="0" allowfullscreen></iframe>
    </div>    
</div>

Large Language Models (LLMs) have advanced rapidly in recent years, demonstrating strong capabilities in problem comprehension and reasoning. Inspired by these developments, researchers have begun exploring the use of LLMs as decentralized decision-makers for multi-robot formation control. However, prior studies reveal that directly applying LLMs to such tasks often leads to unstable and inconsistent behaviors—robots may collapse to the centroid of their positions or diverge entirely—due to hallucinated reasoning, logical inconsistencies, and limited coordination awareness. To overcome these limitations, we propose a novel framework that integrates LLMs with an influence-based plan consensus protocol. In this framework, each robot independently generates a local plan toward the desired formation using its own LLM. The robots then iteratively refine their plans through a decentralized consensus protocol that accounts for their influence on neighboring robots. This process drives the system toward a coherent and stable flocking formation in a fully decentralized manner. We evaluate our approach through comprehensive simulations involving both state-of-the-art closed-source LLMs (e.g., o3-mini, Claude 3.5) and open-source models (e.g., Llama3.1-405b, Qwen-Max, DeepSeek-R1). The results show notable improvements in stability, convergence, and adaptability over previous LLM-based methods. We further validate our framework on a physical team of Crazyflie drones, demonstrating its practical viability and effectiveness in real-world multi-robot systems. [Preprint](https://arxiv.org/abs/2505.06513).

## Challenges Faced By Large Language Models In Solving Multi-Agent Flocking

<div class="row">
    <div class="col-sm-8 mt-3 mt-md-0">
        <iframe width="100%" height="285" src="https://www.youtube.com/embed/Oqa_F1TSitc" frameborder="0" allowfullscreen></iframe>
    </div>    
</div>
Flocking is a behavior where multiple agents in a system attempt to stay close to each other while avoiding collision and maintaining a desired formation. This is observed in the natural world and has applications in robotics, including search and rescue, wild animal tracking, and perimeter surveillance. Recently, large language models (LLMs) have displayed an impressive ability to solve various collaboration tasks as individual decision-makers. Solving multi-agent flocking with LLMs would demonstrate their usefulness in situations requiring spatial and decentralized decision-making. Yet, when LLM-powered agents are tasked with implementing multi-agent flocking, they fall short of the desired behavior. After extensive testing, we find that agents with LLMs as individual decision-makers typically opt to converge on the average of their initial positions or diverge from each other. After breaking the problem down, we discover that LLMs cannot understand maintaining a shape or keeping a distance in a meaningful way. Solving multi-agent flocking with LLMs would enhance their ability to understand collaborative spatial reasoning and lay a foundation for addressing more complex multi-agent tasks. This paper discusses the challenges LLMs face in multi-agent flocking and suggests areas for future improvement and research. [DARS'24](https://arxiv.org/abs/2404.04752) & [GitHub](https://github.com/Zhourobotics/llms-for-flocking-pub).


## Hierarchical LLMs In-the-loop Optimization for Real-time  Multi-Robot Target Tracking under Unknown Hazards

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/llmtrack.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

Real-time multi-robot coordination in hazardous and adversarial environments requires fast, reliable adaptation to dynamic threats. While Large Language Models (LLMs) offer strong high-level reasoning capabilities, the lack of safety guarantees limits their direct use in critical decision-making. In this paper, we propose a hierarchical optimization framework that integrates LLMs into the decision loop for multi-robot target tracking in dynamic and hazardous environments. Rather than generating control actions directly, LLMs are used to generate task configuration and adjust parameters in a bi-level task allocation and planning problem. We formulate multi-robot coordination for tracking tasks as a bi-level optimization problem, with LLMs to reason about potential hazards in the environment and the status of the robot team and modify both the inner and outer levels of the optimization. This hierarchical approach enables real-time adjustments to the robots' behavior. Additionally, a human supervisor can offer broad guidance and assessments to address unexpected dangers, model mismatches, and performance issues arising from local minima. We validate our proposed framework in both simulation and real-world experiments with comprehensive evaluations, demonstrating its effectiveness and showcasing its capability for safe LLM integration for multi-robot systems. [Preprint](https://arxiv.org/abs/2409.12274).