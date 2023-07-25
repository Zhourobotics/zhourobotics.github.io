---
layout: page
title: Risk-Aware Planning
description: 
img: assets/img/simple_mod_exp1.jpg
importance: 2
category: current
---

## Managing risk by stochastic submodular optimization


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/simple_mod_exp.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <iframe width="370" height="250" src="https://www.youtube.com/embed/atyBxxpqmCI" frameborder="0" allowfullscreen></iframe>
    </div>
</div>

In addition to failures caused by DoS attacks, robots can fail randomly, which adds **uncertainty** to their performance. More broadly, the uncertainty comes from noisy robot sensing, imperfect robot motion, and unknown environmental conditions. The uncertainty usually puts robots' performance at risk.

A standard strategy to deal with uncertainty is to optimize either the worst-case or the average of the stochastic performance. Both measures only consider a specific point of the distribution while not sufficiently utilizing the spread of the distribution. Instead, we utilized a risk measure, **Conditional-Value-at-Risk (CVaR)**, commonly used for risk management in stocks portfolio optimization. CVaR is calculated based on the distribution of performance outcomes. By optimizing CVaR, the robots can _manage the trustworthiness_ of their decision-making by tuning a risk parameter. For example, with a high risk level, the robots make more _adventurous_ decisions to gain more rewards (one average) but with higher uncertainty. Instead, if robots choose a low risk level, they are more conservative and achieve fewer rewards but with lower uncertainty. To this end, we proposed **the first polynomial-time algorithm that gives a bounded approximation for CVaR-based combinatorial optimization**. This trustworthy algorithm has been used for enabling **risk-aware multi-robot planning** in environmental monitoring and mobility-on-demand, stochastic traveling salesman problem, and for handling uncertainty extractions from **Bayesian deep learning models**.

Along with optimizing CVaR for trustworthy decision-making, we designed a **Pareto optimization scheme** that adaptively balances maximizing team performance and minimizing risk of failures based on the abundance of **heterogeneous** team resources.

[WAFR'18](https://link.springer.com/chapter/10.1007/978-3-030-44051-0_9), [T-RO](https://ieeexplore.ieee.org/document/9750919): Risk-aware submodular optimization to deal with uncertainties for multi-robot coordination (left figure). <br>
[IROS'20](https://ieeexplore.ieee.org/abstract/document/9341075): Risk-aware planning and assignment for ground vehicles using uncertain perception from aerial vehicles; dealing with uncertain extractions from Bayesian deep learning. <br>
[IROS'21](https://ieeexplore.ieee.org/abstract/document/9635957): Risk-aware submodular optimization for stochastic traveling salesperson problem. <br>
[RA-L+ICRA'22](https://ieeexplore.ieee.org/document/9726858): Adaptive and risk-aware target tracking for robot teams with heterogeneous sensors (right video).