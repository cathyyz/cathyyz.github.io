---
layout: page
title: AI Art Perception Study — Statistical Mediation Analysis
description: Investigating how perceived creativity mediates emotional responses to AI-generated vs. human-created artwork (672 samples).
img: assets/img/projects/ai-art-perception/cover.png
importance: 4
category: work
portfolio: true
tags: [Statistics, Research, Psychology]
cta: "[ View Case Study ]"
---

<style>
  .aiart-meta {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1rem;
    margin: 1.25rem 0 1.5rem;
  }
  .aiart-meta .meta-item {
    padding: 0.85rem 1rem;
    border-left: 3px solid var(--global-theme-color, #2698ba);
    background: rgba(0, 0, 0, 0.03);
    border-radius: 0 4px 4px 0;
  }
  html[data-theme="dark"] .aiart-meta .meta-item {
    background: rgba(255, 255, 255, 0.05);
  }
  .aiart-meta .meta-label {
    font-size: 0.75rem;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.04em;
    opacity: 0.65;
    margin-bottom: 0.35rem;
  }
  .aiart-meta .meta-value {
    font-size: 0.92rem;
    line-height: 1.45;
  }
  .aiart-methods {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1rem;
    margin: 1.25rem 0 0.5rem;
  }
  .aiart-methods .method-card {
    padding: 0.95rem 1.05rem;
    border-left: 2px solid var(--global-theme-color, #2698ba);
    background: rgba(0, 0, 0, 0.03);
    border-radius: 0 6px 6px 0;
  }
  html[data-theme="dark"] .aiart-methods .method-card {
    background: rgba(255, 255, 255, 0.05);
  }
  .aiart-methods .method-title {
    font-size: 0.98rem;
    font-weight: 650;
    margin: 0 0 0.4rem;
    line-height: 1.35;
  }
  .aiart-methods .method-card p {
    margin: 0;
    font-size: 0.92rem;
    line-height: 1.5;
  }
  .aiart-full {
    margin: 1.1rem 0 0.35rem;
  }
  .aiart-full img {
    width: 100%;
    height: auto;
    display: block;
  }
  .aiart-finding {
    margin: 1.75rem 0 0;
    padding: 0 0 0 1.15rem;
    border-left: 2px solid var(--global-theme-color, #2698ba);
  }
  .aiart-finding .finding-title {
    font-size: 1.05rem;
    font-weight: 700;
    line-height: 1.35;
    margin: 0 0 0.65rem;
  }
  .aiart-split {
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
    gap: 1.4rem;
    align-items: center;
    margin: 0.35rem 0 0.25rem;
  }
  .aiart-split .split-text {
    flex: 1 1 48%;
  }
  .aiart-split .split-img {
    flex: 0 0 48%;
    max-width: 48%;
  }
  .aiart-split img {
    width: 100%;
    height: auto;
    display: block;
  }
  .aiart-split.split-wide-img .split-text {
    flex: 1 1 42%;
  }
  .aiart-split.split-wide-img .split-img {
    flex: 0 0 55%;
    max-width: 55%;
  }
  .aiart-caption {
    font-size: 0.88rem;
    opacity: 0.75;
    margin: 0.35rem 0 0;
    line-height: 1.45;
  }
  @media (max-width: 768px) {
    .aiart-meta {
      grid-template-columns: 1fr;
    }
    .aiart-methods {
      grid-template-columns: 1fr;
    }
    .aiart-split,
    .aiart-split.split-wide-img {
      flex-direction: column;
    }
    .aiart-split .split-img,
    .aiart-split.split-wide-img .split-img {
      flex: 0 0 100%;
      max-width: 100%;
    }
  }
</style>

## Overview

Do AI-generated artworks elicit the same perceived creativity and emotional responses as human-created pieces when viewers are unaware of the source? This project employed a double-blind experiment with 672 observations, applying reliability testing, correlation analysis, and regression modeling to examine how perceived creativity mediates the relationship between creation source and aesthetic experience.

**Key finding:** after removing labeling effects, AI and human artworks showed no significant differences in perceived creativity; originality emerged as the strongest predictor of aesthetic experience (β=0.63, R²=0.427).

<div class="aiart-meta">
  <div class="meta-item">
    <div class="meta-label">Focus</div>
    <div class="meta-value">Mediation analysis · Perceived creativity · Aesthetic experience</div>
  </div>
  <div class="meta-item">
    <div class="meta-label">Sample</div>
    <div class="meta-value">56 participants · 12 artworks · 672 valid observations</div>
  </div>
  <div class="meta-item">
    <div class="meta-label">Core Result</div>
    <div class="meta-value">Originality → aesthetic experience (β=0.63, R²=0.427)</div>
  </div>
</div>

## Data Collection

This study recruited 56 participants aged from under 18 to over 50, with 66% having no art background and 34% with art-related experience. Each participant rated 12 artworks—6 AI-generated via Midjourney and 6 human-created from Wikimedia Commons/WikiArt, covering both abstract and representational styles—yielding 672 valid observations (336 per group). A double-blind design ensured participants were unaware of creation sources, with randomized presentation order. Perceived creativity (novelty, originality, thought-provoking) and emotional response (aesthetic experience) were measured using 7-point Likert scales.

<div class="aiart-full">
  {% include figure.liquid path="assets/img/projects/ai-art-perception/stimuli-grid.png" title="Stimulus set — 12 artworks used in the double-blind rating study" class="img-fluid rounded z-depth-1" %}
</div>
<div class="caption">
  Figure 1. The 12 stimulus artworks (6 AI-generated via Midjourney, 6 human-created), spanning abstract and representational styles.
</div>

## Data Preprocessing

Exported survey responses to CSV format and restructured data from wide to long format (one row per participant-artwork observation) for analysis in Stata. Added creation source labels (AI/Human) to each observation.

## Analytical Methods

<div class="aiart-methods">
  <div class="method-card">
    <div class="method-title">Reliability & Validity Testing</div>
    <p>Overall Cronbach's Alpha of 0.8955, with all dimensions exceeding 0.80, indicating strong internal consistency. Inter-dimension correlation matrix confirmed discriminant validity (within perceived creativity r=0.737–0.812; with aesthetic experience r=0.594).</p>
  </div>
  <div class="method-card">
    <div class="method-title">Descriptive Statistics</div>
    <p>Calculated means and standard deviations for AI and human groups across all dimensions to compare between-group differences.</p>
  </div>
  <div class="method-card">
    <div class="method-title">Regression Modeling</div>
    <p>Built simple linear regression models to test predictive effects of novelty and originality on aesthetic experience, reporting β, SE, t, p, 95% CI, and R².</p>
  </div>
  <div class="method-card">
    <div class="method-title">Mediation Pathway Analysis</div>
    <p>Examined the proposed mediation model by comparing perceived creativity scores between AI and human groups, and testing whether perceived creativity dimensions significantly predict aesthetic experience.</p>
  </div>
</div>

## Key Findings

<div class="aiart-finding">

<div class="finding-title">1. Minimal Perceptual Differences Between AI and Human Works</div>

<div class="aiart-split split-wide-img">
  <div class="split-text" markdown="1">

Descriptive statistics revealed small mean differences across all perceived creativity dimensions. For originality, AI artworks (M=4.99, SD=1.40) scored slightly higher than human works (M=4.92, SD=1.56). For novelty, human works (M=4.63, SD=1.62) scored slightly higher than AI (M=4.56, SD=1.54). The thought-provoking dimension showed the largest gap, with AI (M=4.30, SD=1.54) scoring lower than human works (M=4.54, SD=1.64).

The correlation matrix further confirmed coherent but distinct constructs: perceived-creativity dimensions were strongly related to each other, while still showing moderate links to aesthetic experience.

  </div>
  <div class="split-img">
    {% include figure.liquid path="assets/img/projects/ai-art-perception/correlation-heatmap.png" title="Correlation heatmap of perceived creativity and emotional response indicators" class="img-fluid rounded z-depth-1" %}
    <p class="aiart-caption">Figure 2. Correlation heatmap of originality, novelty, inspiration, and aesthetic response.</p>
  </div>
</div>

</div>

<div class="aiart-finding">

<div class="finding-title">2. Originality as the Strongest Predictor</div>

<div class="aiart-split">
  <div class="split-img">
    {% include figure.liquid path="assets/img/projects/ai-art-perception/originality-regression.png" title="Regression of originality on aesthetic experience" class="img-fluid rounded z-depth-1" %}
    <p class="aiart-caption">Figure 3. Positive relationship between originality and aesthetic experience.</p>
  </div>
  <div class="split-text" markdown="1">

Regression analysis showed originality had a significant positive effect on aesthetic experience, explaining 42.72% of variance (R²=0.4272). Novelty also showed significant predictive power, explaining 38.5% of variance (R²=0.385).

Among all measured dimensions, originality was the clearest driver of how viewers evaluated aesthetic quality — more so than novelty alone.

  </div>
</div>

</div>

<div class="aiart-finding">

<div class="finding-title">3. Perceived Creativity Serves as Mediator</div>

<div class="aiart-split">
  <div class="split-text" markdown="1">

Mediation analysis indicated that all perceived creativity dimensions significantly predicted aesthetic experience, supporting the theoretical model that perceived creativity mediates the relationship between creation source and emotional response.

In other words, once labeling effects are removed, what matters most is not whether a work was made by AI or a human, but how creative viewers perceive it to be.

  </div>
</div>

</div>

## What I Learned

This project challenged my assumption that human perception and emotion are too subjective to measure. Through designing Likert scales and validating them with reliability and validity tests, I learned that subjective experiences can be systematically quantified and analyzed.

Additionally, I self-taught Stata to conduct the statistical analysis, which expanded my technical toolkit and my skill of self learning in a short period of time.


