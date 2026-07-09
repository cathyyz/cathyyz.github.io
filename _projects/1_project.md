---
layout: page
title: Self-Adaptive RL Agent for Dynamic Environments
description: A self-adaptive RL agent that uses dual-layer reflection to navigate dynamic environments, improving task completion by 32.7%.
img: assets/img/projects/reflect-to-explore/architecture.png
importance: 1
category: work
portfolio: true
tags: [AI, Research, Python]
cta: "[ View Case Study ]"
---

*Solo Research Project · Python · Reinforcement Learning*

## Overview

Built a reinforcement learning agent that adapts to changing environments in real-time. Standard RL algorithms struggle when obstacles shift and targets move — they either react too slowly or waste time over-exploring. I designed a dual-layer reflection mechanism inspired by human cognition that solves this, improving task completion by **32.7%**.

## The Problem

Traditional RL methods like ε-greedy and DQN work well in static environments but fail when things change. The exploration rate either decays too fast (missing new opportunities) or stays too high (wasting steps on known areas). I wanted to build an agent that knows when to explore more and when to stick with what works — similar to how humans adjust their learning strategies based on feedback.

## My Solution

I designed a dual-layer system inspired by human cognitive regulation:

| Layer | Trigger Condition | Function |
| --- | --- | --- |
| **Fast Adaptation** | Sudden confidence drop between episodes | Fine-tune parameters for rapid response |
| **Reflection** | Persistent inefficiency or declining performance | Major strategy adjustment + prioritized experience replay |

**Why two layers?** Fast adaptation alone overreacts to noise; reflection alone responds too slowly. The dual-layer design balances stability and adaptability.

**Multi-dimensional Confidence Evaluation:** Single reward signals are too noisy. I designed a composite metric (path efficiency + reward stability + success rate) to provide reliable triggers for reflection.

<div style="max-width: 92%; margin: 1.25rem auto;">
  {% include figure.liquid path="assets/img/projects/reflect-to-explore/architecture.png" title="Self-adaptive reinforcement learning agent architecture" class="img-fluid rounded z-depth-1" %}
</div>
<div class="caption">
  System architecture: confidence assessment triggers fast adaptation or deep reflection, which updates Q-learning parameters and action selection.
</div>

## Implementation

I built everything from scratch in Python:

The core algorithm extends Q-learning with adaptive parameter adjustment. The exploration rate responds to both immediate feedback and long-term trends. I implemented priority-based experience replay using Softmax sampling to help the agent learn more from successful episodes.

For testing, I created a custom dynamic maze environment: a 10×10 grid where obstacles randomly shift every 18 steps and the target has a 30% chance of moving each update. This simulates real-world scenarios where conditions change unpredictably.

## Key Challenge & Solution

The hardest part was translating abstract concepts like "reflection" and "confidence" into computable mechanisms.

My approach:

- Defined confidence as a weighted combination of path efficiency, reward stability, and success rate
- Established specific trigger thresholds: confidence drop > 0.25 activates fast adaptation; avg confidence < 0.45 with variance < 0.1 triggers deep reflection

## Results

Tested with 30 independent runs against a confidence-based baseline:

| Metric | Baseline | My Method | Change |
| --- | --- | --- | --- |
| Task Completion | 37.9% | 50.3% | +32.7% |
| Average Steps | 154.9 | 142.8 | -7.8% |

The method showed consistent improvements across different threshold configurations, demonstrating robustness to hyperparameter choices.

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

This project taught me how to translate abstract ideas into working algorithms. The hardest part was finding the right balance — trigger reflection too often and the agent never stabilizes; trigger too rarely and it gets stuck. I ran extensive experiments to find threshold values that worked across different scenarios.

I also learned that evaluation metrics matter as much as the algorithm itself. A single reward number doesn't capture whether an agent is actually learning to navigate efficiently. Building the multi-dimensional confidence score forced me to think carefully about what "good performance" really means in a dynamic environment.
