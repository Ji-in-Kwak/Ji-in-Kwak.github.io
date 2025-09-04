---
layout: page
title: Scalable Robust Multi-Agent Reinforcement Learning for Model Uncertainty
description: Evolutionary Diversity-maintaining Population Curriculum for Robust MARL
img: assets/img/EDPC_framework.png
importance: 4
category: work
---

This research addresses critical challenges in multi-agent reinforcement learning (MARL) by introducing a novel approach that combines robust attention mechanisms with evolutionary diversity maintenance. Our work focuses on improving MARL performance in uncertain, noisy environments while maintaining scalability with increasing numbers of agents.

# Motivation

Multi-agent reinforcement learning faces several critical challenges that limit its practical applications:

- **Simulation-Reality Gap**: Significant discrepancies exist between simulated training environments and real-world deployment scenarios
- **Reward Uncertainty**: Agents face uncertainty in reward functions, making optimal policy learning difficult
- **Scalability Issues**: Traditional approaches like MADDPG and R-MADDPG show significant performance degradation as the number of agents increases

To address these challenges, we propose two main contributions:

1. **RA-MADDPG**: A robust attention-based multi-agent deep deterministic policy gradient algorithm designed for noisy environments
2. **EDPC**: An evolutionary diversity-maintaining population curriculum (EDPC) framework that enhances training stability and performance

# Methodology

## Robust Attention-based MADDPG (RA-MADDPG)

Our RA-MADDPG algorithm enhances the traditional MADDPG framework with attention mechanisms to:
- Better handle environmental noise and uncertainty
- Improve agent coordination in complex scenarios
- Maintain performance stability in noisy conditions

## Evolutionary Diversity-maintaining Population Curriculum (EDPC)

The EDPC framework introduces two key mechanisms:

1. **Reward-proportionate Parent Selection**
   - Selects parent policies based on their performance
   - Maintains diversity in the policy population
   - Ensures robust learning across different scenarios

2. **Reward-guided Mutation**
   - Adapts mutation rates based on reward signals
   - Optimizes exploration-exploitation trade-off
   - Enhances learning efficiency in complex environments

<div class="row">
    <div class="col-sm-12 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/EDPC_framework.png" title="EDPC Framework" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Overview of the EDPC framework showing the interaction between reward-proportionate parent selection and reward-guided mutation
</div>

# Experimental Results

Our extensive experimentation demonstrated several key advantages of the proposed approach:

## Superior Performance
- EDPC consistently outperformed baseline models across various scenarios
- Showed significant improvements in both training stability and final performance

## Robustness to Uncertainty
- Maintained consistent reward levels across different noise rates
- Demonstrated strong resilience to environmental uncertainties
- Proved effective in handling sim-to-real gaps

## Scalability
- Successfully scaled to larger agent populations
- Average reward increased with the number of agents
- Maintained performance in large-scale MARL scenarios where traditional approaches struggled

These results validate our approach's effectiveness in addressing the core challenges of multi-agent reinforcement learning, particularly in scenarios involving uncertainty and large numbers of agents.

<div class="row">
    <div class="col-sm-12 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/EDPC_result.png" title="Performance Comparison" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Experimental results showing the superior performance of EDPC compared to baseline approaches
</div>

