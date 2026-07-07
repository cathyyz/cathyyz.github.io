---
layout: page
title: Reflect-to-Explore
description: Self-adaptive exploration in RL via dual-layer reflection.
img: assets/img/projects/reflect-to-explore/architecture.png
importance: 1
category: work
---

## Overview

Inspired by human metacognition's **"rapid response + deep reflection"** dual-layer mechanism, I designed a framework that enables RL agents to autonomously identify learning bottlenecks and adjust strategies in dynamic environments—improving task completion rate by **32.7%** without retraining.

## Problem

Traditional RL agents often require retraining from scratch or massive additional data when environments change. I wanted to explore: can we borrow from human "reflect-and-adjust" cognitive patterns to help agents adapt more efficiently?

## Core Innovation: Dual-Layer Reflection Mechanism

| Layer | Trigger Condition | Function |
| --- | --- | --- |
| **Fast Adaptation** | Sudden confidence drop between episodes | Fine-tune parameters for rapid response |
| **Reflection** | Persistent inefficiency or declining performance | Major strategy adjustment + prioritized experience replay |

**Why two layers?** Fast adaptation alone overreacts to noise; reflection alone responds too slowly. The dual-layer design balances stability and adaptability.

**Multi-dimensional Confidence Evaluation:** Single reward signals are too noisy. I designed a composite metric (path efficiency + reward stability + success rate) to provide reliable triggers for reflection.

<div class="row justify-content-sm-center">
  <div class="col-sm-11 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/projects/reflect-to-explore/architecture.png" title="Self-adaptive reinforcement learning agent architecture" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  System architecture: confidence assessment triggers fast adaptation or deep reflection, which updates Q-learning parameters and action selection.
</div>

## Key Challenge & Solution

The hardest part was translating abstract concepts like "reflection" and "confidence" into computable mechanisms.

My approach:

- Defined confidence as a weighted combination of path efficiency, reward stability, and success rate
- Established specific trigger thresholds: confidence drop > 0.25 activates fast adaptation; avg confidence < 0.45 with variance < 0.1 triggers deep reflection

## Results

Tested in a custom dynamic maze environment (10×10 grid, shifting obstacles, moving targets) with 30 independent runs.

- **Task completion rate:** 50.3% vs baseline 37.9% (**+32.7%**)
- **Path efficiency:** improved by **7.8%**
- Consistent performance across different parameter configurations, demonstrating robustness

<style>
  .results-pair {
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
    gap: 1rem;
    align-items: flex-start;
    width: 100%;
    margin-top: 1rem;
  }
  .results-pair .maze-col {
    flex: 0 0 40%;
    width: 40%;
    max-width: 40%;
  }
  .results-pair .chart-col {
    flex: 0 0 55%;
    width: 55%;
    max-width: 55%;
  }
  .results-pair img {
    width: 100%;
    height: auto;
    display: block;
  }
  @media (max-width: 768px) {
    .results-pair {
      flex-direction: column;
    }
    .results-pair .maze-col,
    .results-pair .chart-col {
      flex: 0 0 100%;
      width: 100%;
      max-width: 100%;
    }
  }
</style>

<div class="results-pair">
  <div class="maze-col">
    {% include figure.liquid path="assets/img/projects/reflect-to-explore/maze-environment.png" title="Dynamic maze environment with learned policy" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="chart-col">
    {% include figure.liquid path="assets/img/projects/reflect-to-explore/results-comparison.png" title="Baseline vs reflection agent performance in dynamic maze" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Left: learned policy. Right: performance comparison.
</div>

## What I Learned

This project taught me that cross-disciplinary transfer requires finding the right level of abstraction. "Reflection matters" is too vague to implement; simulating neural circuits is too specific to be practical. The key is identifying quantifiable intermediate concepts (confidence metrics, threshold conditions) that bridge cognitive science insights to actual algorithmic improvements.
