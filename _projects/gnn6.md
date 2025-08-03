---
layout: page
title: Graph Neural Networks
description: 
img: assets/img/GNN.png
importance: 2
category: past
---

## Large-scale, decentralized multi-robot coordination through graph neural networks

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/learning_framework.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

For long-term operation in large-scale environments, we need scalable and decentralized algorithms. However, with local communications, these decentralized algorithms typically perform worse than their centralized counterparts. Recently, I have been exploring the use of **graph neural networks (GNNs)** as a tool for automatically synthesizing decentralized planning strategies which are trained to imitate centralized experts. To this end, I developed a **GNN-based imitation learning framework** that learns **decentralized decision-making** for the robots from a **centralized expert** in **small-scale** scenarios and **generalizes well** the learned policies to **larger-scale** scenarios, e.g., larger environments and larger networks of robots.

[Preprint](https://arxiv.org/abs/2105.08601): Graph neural networks for decentralized multi-robot submodular action selection.
