---
layout: page
title: VLAs and WAMs for Manipulation
description: 
img: assets/img/roboticarm2026.jpg
importance: 4
category: current
---

#### *Project Lead: [Zijian An](https://scholar.google.com/citations?user=zOA9WhsAAAAJ&hl=en)*

We deploy **vision-language-action (VLA) models** on accessible, low-cost hardware to advance robotic manipulation, with a focus on **food processing, packaging, and smart agriculture**. Our work studies how to make VLA policies satisfy precise task constraints, execute long-horizon sequences reliably, run in real time, and plan with vision-language models.

## CLAW: A Vision-Language-Action Framework for Weight-Aware Robotic Grasping

<div class="row">
    <div class="col-sm-7 mt-3 mt-md-0">
        {% include figure.html path="assets/img/research/claw.png" title="CLAW" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-5 mt-3 mt-md-0">
        <iframe width="100%" height="200" src="https://www.youtube.com/embed/MuMYj2QgReI" frameborder="0" allowfullscreen></iframe>
    </div>
</div>

Vision-language-action (VLA) models have recently emerged as a promising paradigm for robotic control, enabling end-to-end policies that ground natural language instructions into visuomotor actions. However, current VLAs often struggle to satisfy precise task constraints, such as stopping based on numeric thresholds, since their observation-to-action mappings are implicitly shaped by training data and lack explicit mechanisms for condition monitoring. In this work, we propose CLAW (CLIP-Language-Action for Weight), a framework that decouples condition evaluation from action generation. CLAW leverages a fine-tuned CLIP model as a lightweight prompt generator, which continuously monitors the digital readout of a scale and produces discrete directives based on task-specific weight thresholds. These prompts are then consumed by π<sub>0</sub>, a flow-based VLA policy, which integrates the prompts with multi-view camera observations to produce continuous robot actions. This design enables CLAW to combine symbolic weight reasoning with high-frequency visuomotor control. We validate CLAW on three experimental setups: single-object grasping and mixed-object tasks requiring dual-arm manipulation. Across all conditions, CLAW reliably executes weight-aware behaviors and outperforms both raw-π<sub>0</sub> and fine-tuned π<sub>0</sub> models. [CASE'26](https://arxiv.org/abs/2509.14143).

## VILAS: A VLA-Integrated Low-cost Architecture with Soft Grasping for Robotic Manipulation

<div class="row">
    <div class="col-sm-7 mt-3 mt-md-0">
        {% include figure.html path="assets/img/research/vilas.jpg" title="VILAS" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-5 mt-3 mt-md-0">
        <iframe width="100%" height="200" src="https://www.youtube.com/embed/Z7g6pS-ULDk" frameborder="0" allowfullscreen></iframe>
    </div>
</div>

We present VILAS, a fully low-cost, modular robotic manipulation platform designed to support end-to-end vision-language-action (VLA) policy learning and deployment on accessible hardware. The system integrates a Fairino FR5 collaborative arm, a Jodell RG52-50 electric gripper, and a dual-camera perception module, unified through a ZMQ-based communication architecture that seamlessly coordinates teleoperation, data collection, and policy deployment within a single framework. To enable safe manipulation of fragile objects without relying on explicit force sensing, we design a kirigami-based soft compliant gripper extension that induces predictable deformation under compressive loading, providing gentle and repeatable contact with delicate targets. We deploy and evaluate three state-of-the-art VLA models on the VILAS platform: π<sub>0</sub>, π<sub>0.5</sub>, and GR00T N1.6. All models are fine-tuned from publicly released pretrained checkpoints using an identical demonstration dataset collected via our teleoperation pipeline. Experiments on a grape grasping task validate the effectiveness of the proposed system, confirming that capable manipulation policies can be successfully trained and deployed on low-cost modular hardware, and provide practical insights into the deployment characteristics of current VLA models in real-world settings. [DARS'26](https://arxiv.org/abs/2605.02037).

## SeqVLA: Sequential Task Execution for Long-Horizon Manipulation with Completion-Aware Vision-Language-Action Model

<div class="row">
    <div class="col-sm-7 mt-3 mt-md-0">
        {% include figure.html path="assets/img/research/seqvla.png" title="SeqVLA" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-5 mt-3 mt-md-0">
        <iframe width="100%" height="200" src="https://www.youtube.com/embed/ee0Zlf_BNtU" frameborder="0" allowfullscreen></iframe>
    </div>
</div>

Long-horizon robotic manipulation tasks require executing multiple interdependent subtasks in strict sequence, where errors in detecting subtask completion can cascade into downstream failures. Existing Vision-Language-Action (VLA) models such as π<sub>0</sub> excel at continuous low-level control but lack an internal signal for identifying when a subtask has finished, making them brittle in sequential settings. We propose SeqVLA, a completion-aware extension of π<sub>0</sub> that augments the base architecture with a lightweight detection head perceiving whether the current subtask is complete. This dual-head design enables SeqVLA not only to generate manipulation actions but also to autonomously trigger transitions between subtasks. We investigate four finetuning strategies that vary in how the action and detection heads are optimized (joint vs. sequential finetuning) and how pretrained knowledge is preserved (full finetuning vs. frozen backbone). Experiments are performed on two multi-stage tasks: salad packing with seven distinct subtasks and candy packing with four distinct subtasks. Results show that SeqVLA significantly outperforms the baseline π<sub>0</sub> and other strong baselines in overall success rate. In particular, joint finetuning with an unfrozen backbone yields the most decisive and statistically reliable completion predictions, eliminating sequence-related failures and enabling robust long-horizon execution. [ISRR'26](https://arxiv.org/abs/2509.14138).

## ROG-Grasp: Root-Oriented Geometry for Robotic Grasping and Placement

<div class="row">
    <div class="col-sm-7 mt-3 mt-md-0">
        {% include figure.html path="assets/img/research/roggrasp.png" title="ROG-Grasp" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-5 mt-3 mt-md-0">
        <iframe width="100%" height="200" src="https://www.youtube.com/embed/Ir2UtGODdMo" frameborder="0" allowfullscreen></iframe>
    </div>
</div>

Orientation-aware manipulation is essential in post-harvest agricultural processing, where produce must be grasped and placed in consistent configurations. This paper presents ROG-Grasp, a geometry-based robotic grasping and placement framework that estimates the produce orientation from root surface geometry using RGB-D perception. A YOLO-based root detector and point cloud plane fitting are used to infer the root normal, enabling stable grasp pose generation and orientation-constrained Cartesian motion planning. Experiments on tomatoes and onions demonstrate high success rates and stable execution time in both isolated and cluttered scenarios. Compared with vision-language-action (VLA) policies, the proposed method achieves more reliable and accurate grasp completion with faster execution. These results highlight the effectiveness of geometry-driven perception for practical orientation-controlled manipulation tasks. [CASE'26](https://arxiv.org/abs/2606.00449).

## Threading Optimization for Vision-Language-Action Model Inference in Low-Cost Smart Agricultural Manipulation

<div class="row">
    <div class="col-sm-7 mt-3 mt-md-0">
        {% include figure.html path="assets/img/research/threading.png" title="Threading optimization" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-5 mt-3 mt-md-0">
        <iframe width="100%" height="200" src="https://www.youtube.com/embed/Ryvi5j6MjXY" frameborder="0" allowfullscreen></iframe>
    </div>
</div>

Vision-Language-Action (VLA) models continue to face challenges such as slow inference speed and difficulty performing fine-grained motion adjustments, limiting their widespread adoption in industry. While the Real-Time Action Chunking (RTAC) algorithm has been proposed to address these bottlenecks, bridging the gap between the algorithm provided in pseudocode to a stable, real-world deployment on a low-cost robotic arm remains a challenge. In this work, we present a complete system-level implementation of RTAC tailored for a low-cost robotic manipulation system. We advance beyond the original high-level pseudocode by optimizing the threading implementation for the policy inference and control pipeline, reducing end-to-end latency and improving responsiveness without modifying the underlying policy. We evaluate this system on tasks involving the manipulation of agricultural produce, specifically garlic bulbs and walnuts. Experimental results demonstrate that our custom threading implementation significantly improves control stability and speed compared to the base implementation of RTAC. [CASE'26](https://arxiv.org/abs/2606.00966).

## Vision Language Models Cannot Plan, but Can They Formalize?

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/research/vlmformalize.png" title="VLM-as-formalizer" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

The advancement of vision language models (VLMs) has empowered embodied agents to accomplish simple multimodal planning tasks, but not long-horizon ones requiring long sequences of actions. In text-only simulations, long-horizon planning has seen significant improvement brought by repositioning the role of LLMs. Instead of directly generating action sequences, LLMs translate the planning domain and problem into a formal planning language like the Planning Domain Definition Language (PDDL), which can call a formal solver to derive the plan in a verifiable manner. In multimodal environments, research on VLM-as-formalizer remains scarce, usually involving gross simplifications such as predefined object vocabulary or overly similar few-shot examples. In this work, we present a suite of five VLM-as-formalizer pipelines that tackle one-shot, open-vocabulary, and multimodal PDDL formalization. We evaluate those on an existing benchmark while presenting another two that for the first time account for planning with authentic, multi-view, and low-quality images. We conclude that VLM-as-formalizer greatly outperforms end-to-end plan generation. We find that visual grounding of object relations remains the primary bottleneck for weaker VLMs, while stronger models have largely overcome this limitation. [ECCV'26 WMEAI Workshop, Best Paper Award](https://arxiv.org/abs/2509.21576).

## GlanceWAM: Sparse Test-Time Imagination for World-Action Models

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/research/glancewam.png" title="GlanceWAM" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

Video generative models provide rich physical priors for robot learning, yet existing world-action models (WAMs) face a fundamental trade-off: synchronous video generation at control rate is latency-prohibitive, while abandoning test-time visual imagination sacrifices task success. We show that visual imagination achieves both real-time inference and superior success rates when generated asynchronously off the critical path and consumed directly in latent space. We introduce GlanceWAM, which decouples imagination from control within a single video DiT: an asynchronous proposer glances ahead on a slow clock to imagine a single lookahead frame seconds into the future in the background, while an action head decodes action chunks at control rate (48 ms) purely in latent space without blocking. Enabled by a non-interfering attention mask that isolates video representations and staleness-robust horizon training that accommodates asynchronous lookahead aging, GlanceWAM breaks the speed-success dilemma. Trained purely on demonstrations, it attains 72.2% on the 24-task RoboCasa kitchen benchmark (surpassing synchronous Cosmos Policy at 67.1% and imagination-free co-training at 64.4%) and 99.0% on LIBERO, executing at 48 ms per chunk on an NVIDIA A100 GPU (24x faster than synchronous baselines). [IROS'26 RoBoWoMo Workshop](https://arxiv.org/abs/2608.23927) & [GitHub](https://github.com/linhanwang/GlanceWAM).

## Related Publications

- R. Yang, Z. An, L. Zhou, and Y. Feng, "Process-Aware Robotic Food Assembly: Closed-Loop Visual Monitoring Across Heterogeneous Ingredients," *Journal of Agriculture and Food Research*, 2026. [Paper](https://www.sciencedirect.com/science/article/pii/S2666154326006575).
- R. Yang, S. Cai, L. Zhou, and Y. Feng, "Intelligent Food Portioning System Using Vision-Language-Action (VLA) Models for Small-Scale Food Operations," *Journal of Future Foods*, 2026. [Paper](https://doi.org/10.1016/j.jfutfo.2025.12.047).
