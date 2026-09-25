---
layout: page
title: VLMs for Driving and Navigation
description: 
img: assets/img/autodrive.jpg
importance: 3
category: current
---

#### *Project Lead: [Amirhosein Chahe](https://scholar.google.com/citations?user=MeK_1LUAAAAJ&hl=en)*

## What's Hidden Matters: Identifying Planning-Critical Occluded Agents using Vision-Language Models

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/research/occluded.jpg" title="Planning-critical occlusions" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

Autonomous vehicles must safely navigate complex environments where planning-critical agents may be hidden from view. Current approaches often treat all occlusions with uniform conservatism, yielding needlessly defensive driving, or they infer hidden spaces without estimating the impact on the planner. This work bridges the critical gap between perception and planning by enabling Vision-Language Models (VLMs) to identify and reason about the specific hidden agents that are most critical to the ego-vehicle's trajectory. We introduce a novel framework that uses Planning KL-divergence (PKL), an information-theoretic metric, to systematically identify and rank occluded agents based on their impact on the ego vehicle's plan. Using this planning-aware ranking, we employ an expert VLM (GPT-5) to generate rich, structured annotations that capture the visual evidence and reasoning required for this task. We apply this framework to the nuScenes dataset to create a new benchmark focused on high-impact scenarios. We conduct comprehensive experiments on a wide range of general-purpose and domain-adapted VLMs, demonstrating that fine-tuning on our PKL-guided data yields dramatic performance improvements across all models. Notably, smaller, fine-tuned models significantly outperform their much larger zero-shot counterparts, and our PKL-guided data selection strategy improves performance by approximately 30% over random sampling. Our work presents the first systematic approach for training VLMs to focus on planning-critical occlusions, enabling more semantically grounded and efficient risk assessment in autonomous driving. [IROS'26](https://arxiv.org/abs/2607.00283).

## Policy-Guided World Model Planning for Language-Conditioned Visual Navigation

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/research/pijepa.png" title="PiJEPA trajectories" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

Navigating to a visually specified goal given natural language instructions remains a fundamental challenge in embodied AI. Existing approaches either rely on reactive policies that struggle with long-horizon planning, or employ world models that suffer from poor action initialization in high-dimensional spaces. We present PiJEPA, a two-stage framework that combines the strengths of learned navigation policies with latent world model planning for instruction-conditioned visual navigation. In the first stage, we finetune an Octo-based generalist policy, augmented with a frozen pretrained vision encoder (DINOv2 or V-JEPA-2), on the CAST navigation dataset to produce an informed action distribution conditioned on the current observation and language instruction. In the second stage, we use this policy-derived distribution to warm-start Model Predictive Path Integral (MPPI) planning over a separately trained JEPA world model, which predicts future latent states in the embedding space of the same frozen encoder. By initializing the MPPI sampling distribution from the policy prior rather than from an uninformed Gaussian, our planner converges faster to high-quality action sequences that reach the goal. We systematically study the effect of the vision encoder backbone, comparing DINOv2 and V-JEPA-2, across both the policy and world model components. Experiments on real-world navigation tasks demonstrate that PiJEPA significantly outperforms both standalone policy execution and uninformed world model planning, achieving improved goal-reaching accuracy and instruction-following fidelity. [CVPR'26 WDFM-EAI Workshop](https://openaccess.thecvf.com/content/CVPR2026W/WDFM-EAI/html/Chahe_Policy-Guided_World_Model_Planning_for_Language-Conditioned_Visual_Navigation_CVPRW_2026_paper.html) & [arXiv](https://arxiv.org/abs/2603.25981).

## ReasonDrive: Efficient Visual Question Answering for Autonomous Vehicles with Reasoning-Enhanced Small Vision-Language Models

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/reasondrive.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

Vision-language models (VLMs) show promise for autonomous driving but often lack transparent reasoning capabilities that are critical for safety. We investigate whether explicitly modeling reasoning during fine-tuning enhances VLM performance on driving decision tasks. Using GPT-4o, we generate structured reasoning chains for driving scenarios from the DriveLM benchmark with category-specific prompting strategies. We compare reasoning-based fine-tuning, answer-only fine-tuning, and baseline instruction-tuned models across multiple small VLM families (Llama 3.2, Llava 1.5, and Qwen 2.5VL). Our results demonstrate that reasoning-based fine-tuning consistently outperforms alternatives, with Llama3.2-11B-reason achieving the highest performance. Models fine-tuned with reasoning show substantial improvements in accuracy and text generation quality, suggesting explicit reasoning enhances internal representations for driving decisions. These findings highlight the importance of transparent decision processes in safety-critical domains and offer a promising direction for developing more interpretable autonomous driving systems. [CVPR'25 WDFM-AD Workshop](https://openaccess.thecvf.com/content/CVPR2025W/WDFM-AD/html/Chahe_ReasonDrive_Efficient_Visual_Question_Answering_for_Autonomous_Vehicles_with_Reasoning-Enhanced_CVPRW_2025_paper.html) & [GitHub](https://github.com/Zhourobotics/ReasonDrive).


## Query3D: LLM-Powered Open-Vocabulary Scene Segmentation with Language Embedded 3D Gaussians

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/query3d.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

This paper introduces a novel method for open-vocabulary 3D scene querying in autonomous driving by combining Language Embedded 3D Gaussians with Large Language Models (LLMs). We propose utilizing LLMs to generate both contextually canonical phrases and helping positive words for enhanced segmentation and scene interpretation. Our method leverages GPT-3.5 Turbo as an expert model to create a high-quality text dataset, which we then use to fine-tune smaller, more efficient LLMs for on-device deployment.
Our comprehensive evaluation on the WayveScenes101 dataset demonstrates that LLM-guided segmentation significantly outperforms traditional approaches based on predefined canonical phrases. Notably, our fine-tuned smaller models achieve performance comparable to larger expert models while maintaining faster inference times. Through ablation studies, we discover that the effectiveness of helping positive words correlates with model scale, with larger models better equipped to leverage additional semantic information.
This work represents a significant advancement towards more efficient, context-aware autonomous driving systems, effectively bridging 3D scene representation with high-level semantic querying while maintaining practical deployment considerations. [WACV'25 LLVM-AD Workshop, Best Paper Award](https://openaccess.thecvf.com/content/WACV2025W/LLVMAD/html/Chahe_Query3D_LLM-Powered_Open-Vocabulary_Scene_Segmentation_with_Language_Embedded_3D_Gaussians_WACVW_2025_paper.html) & [GitHub](https://github.com/Zhourobotics/Query-3DGS-LLM).


## Dynamic Adversarial Attacks on Autonomous Driving Systems

<div class="row">
    <div class="col-sm-7 mt-3 mt-md-0">
        {% include figure.html path="assets/img/rssadversiral.png" title="example image" class="img-fluid rounded z-depth-1" style="height: 210px; object-fit: cover;" %}
    </div>
    <div class="col-sm-5 mt-3 mt-md-0">
        <iframe width="100%" height="165" src="https://www.youtube.com/embed/Wh2sPYpWczQ" frameborder="0" allowfullscreen></iframe>
    </div>    
</div>

This paper introduces an attacking mechanism to challenge the resilience of autonomous driving systems. Specifically, we manipulate the decision-making processes of an autonomous vehicle by dynamically displaying adversarial patches on a screen mounted on another moving vehicle. These patches are optimized to deceive the object detection models into misclassifying targeted objects, e.g., traffic signs. Such manipulation has significant implications for critical multi-vehicle interactions such as intersection crossing, which are vital for safe and efficient autonomous driving systems. 
Particularly, we make four major contributions. First, we introduce a novel adversarial attack approach where the patch is not co-located with its target, enabling more versatile and stealthy attacks. Moreover, our method utilizes dynamic patches displayed on a screen, allowing for adaptive changes and movements, enhancing the flexibility and performance of the attack. To do so, we design a Screen Image Transformation Network (SIT-Net), which simulates environmental effects on the displayed images, narrowing the gap between simulated and real-world scenarios. Further, we integrate a positional loss term into the adversarial training process to increase the success rate of the dynamic attack. Finally, we shift the focus from merely attacking perceptual systems to influencing the decision-making algorithms of self-driving systems. Our experiments demonstrate the first successful implementation of such dynamic adversarial attacks in real-world autonomous driving scenarios, paving the way for advancements in the field of robust and secure autonomous driving. [RSS'24](https://www.roboticsproceedings.org/rss20/p076.pdf) & [GitHub](https://github.com/amirhoseinch/dynamicpatch). 
