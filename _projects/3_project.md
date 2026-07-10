---
layout: page
title: Project Echo — Desktop Sound Localization Array
description: A conceptual desktop array providing 360° visual feedback for critical environmental sounds.
img: assets/img/projects/project-echo/device-render.png
importance: 3
category: work
portfolio: true
tags: [DSP, Accessibility, Python]
cta: "[ View Case Study ]"
_styles: |
  .post-header {
    display: none !important;
  }
---

<style>
  .post-header {
    display: none !important;
  }
  .echo-page {
    --echo-navy: #0f172a;
    --echo-orange: #f59e0b;
    --echo-accent: var(--global-theme-color, #2698ba);
  }
  .echo-hero {
    background: var(--echo-navy);
    color: #f8fafc;
    margin: 0 -15px 2rem;
    padding: 2.5rem 1.5rem 0;
    text-align: center;
    border-radius: 0 0 12px 12px;
  }
  .echo-hero .wip-badge {
    display: inline-flex;
    align-items: center;
    gap: 0.4rem;
    font-size: 0.68rem;
    font-weight: 700;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: var(--echo-orange);
    border: 1px solid rgba(245, 158, 11, 0.45);
    border-radius: 999px;
    padding: 0.3rem 0.75rem;
    margin-bottom: 1rem;
  }
  .echo-hero h1 {
    font-size: clamp(1.5rem, 4vw, 2rem);
    font-weight: 800;
    line-height: 1.25;
    margin: 0 0 0.75rem;
    color: #fff;
  }
  .echo-hero .hero-subtitle {
    max-width: 36rem;
    margin: 0 auto 1.5rem;
    font-size: 0.95rem;
    line-height: 1.55;
    opacity: 0.78;
  }
  .echo-hero-image {
    max-width: 520px;
    margin: 0 auto -3rem;
    padding: 0 1rem;
    position: relative;
    z-index: 2;
  }
  .echo-hero-image figure {
    margin: 0;
    background: #1e293b;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.35);
  }
  .echo-hero-image img {
    width: 100%;
    height: auto;
    display: block;
  }
  .echo-meta {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.5rem;
    margin: 4rem 0 2.5rem;
    padding-top: 0.5rem;
  }
  .echo-meta .meta-label {
    font-size: 0.68rem;
    font-weight: 700;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    color: var(--echo-accent);
    margin-bottom: 0.35rem;
  }
  .echo-meta .meta-value {
    font-size: 0.92rem;
    font-weight: 600;
    line-height: 1.45;
  }
  .echo-section-title {
    display: flex;
    align-items: center;
    gap: 0.65rem;
    font-size: 1.35rem;
    font-weight: 800;
    margin: 2rem 0 1rem;
  }
  .echo-section-title::before {
    content: "";
    width: 2rem;
    height: 4px;
    background: var(--echo-orange);
    border-radius: 2px;
    flex-shrink: 0;
  }
  .echo-vision-text {
    font-size: 0.98rem;
    line-height: 1.65;
    margin-bottom: 1rem;
  }
  .echo-goal-box {
    padding: 1rem 1.15rem;
    border-left: 4px solid var(--echo-orange);
    background: rgba(245, 158, 11, 0.08);
    border-radius: 0 8px 8px 0;
    font-size: 0.95rem;
    line-height: 1.6;
  }
  html[data-theme="dark"] .echo-goal-box {
    background: rgba(245, 158, 11, 0.12);
  }
  .echo-arch-intro {
    font-size: 0.95rem;
    line-height: 1.6;
    margin-bottom: 1.25rem;
    opacity: 0.85;
  }
  .echo-layers {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    margin-bottom: 1.5rem;
  }
  .echo-layer {
    display: flex;
    gap: 0.85rem;
    align-items: flex-start;
  }
  .echo-layer-icon {
    flex: 0 0 2rem;
    width: 2rem;
    height: 2rem;
    border-radius: 8px;
    background: rgba(0, 0, 0, 0.05);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 0.85rem;
    opacity: 0.7;
  }
  html[data-theme="dark"] .echo-layer-icon {
    background: rgba(255, 255, 255, 0.08);
  }
  .echo-layer-title {
    font-weight: 700;
    font-size: 0.92rem;
    margin-bottom: 0.15rem;
  }
  .echo-layer-desc {
    font-size: 0.88rem;
    line-height: 1.5;
    opacity: 0.8;
  }
  .echo-algorithm-box {
    padding: 1.25rem;
    border-radius: 10px;
    background: rgba(0, 0, 0, 0.04);
    border: 1px solid rgba(0, 0, 0, 0.06);
  }
  html[data-theme="dark"] .echo-algorithm-box {
    background: rgba(255, 255, 255, 0.04);
    border-color: rgba(255, 255, 255, 0.08);
  }
  .echo-algorithm-box .algo-label {
    font-size: 0.68rem;
    font-weight: 700;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    color: var(--echo-accent);
    margin-bottom: 0.5rem;
  }
  .echo-formula {
    text-align: center;
    font-size: 1.15rem;
    font-weight: 600;
    padding: 0.85rem;
    margin: 0.75rem 0;
    background: var(--global-bg-color, #fff);
    border-radius: 6px;
    border: 1px solid rgba(0, 0, 0, 0.06);
  }
  html[data-theme="dark"] .echo-formula {
    border-color: rgba(255, 255, 255, 0.1);
  }
  .echo-algorithm-box .algo-note {
    font-size: 0.82rem;
    opacity: 0.75;
    line-height: 1.5;
  }
  .echo-progress-box {
    padding: 1.25rem;
    border-radius: 10px;
    border: 1px solid rgba(0, 0, 0, 0.08);
    background: rgba(0, 0, 0, 0.02);
    font-size: 0.95rem;
    line-height: 1.65;
  }
  html[data-theme="dark"] .echo-progress-box {
    border-color: rgba(255, 255, 255, 0.1);
    background: rgba(255, 255, 255, 0.03);
  }
  .echo-roadmap {
    background: var(--echo-navy);
    color: #e2e8f0;
    margin: 2.5rem -15px 0;
    padding: 2rem 1.5rem 2.5rem;
    border-radius: 12px 12px 0 0;
  }
  .echo-roadmap .echo-section-title {
    color: #fff;
  }
  .echo-roadmap-intro {
    font-size: 0.92rem;
    line-height: 1.6;
    opacity: 0.85;
    margin-bottom: 1.25rem;
  }
  .echo-roadmap-card {
    padding: 1.15rem 1.25rem;
    border-radius: 10px;
    background: rgba(255, 255, 255, 0.06);
    border: 1px solid rgba(255, 255, 255, 0.08);
  }
  .echo-roadmap-card .card-index {
    font-size: 0.72rem;
    font-weight: 700;
    letter-spacing: 0.04em;
    color: var(--echo-orange);
    margin-bottom: 0.35rem;
  }
  .echo-roadmap-card .card-title {
    font-size: 1rem;
    font-weight: 700;
    color: #fff;
    margin-bottom: 0.35rem;
  }
  .echo-roadmap-card .card-desc {
    font-size: 0.88rem;
    line-height: 1.55;
    opacity: 0.78;
  }
  @media (max-width: 768px) {
    .echo-meta {
      grid-template-columns: 1fr;
      margin-top: 3rem;
    }
    .echo-hero {
      margin-left: 0;
      margin-right: 0;
    }
    .echo-roadmap {
      margin-left: 0;
      margin-right: 0;
    }
  }
</style>

<div class="echo-page">

<div class="echo-hero">
  <div class="wip-badge">⚠ Work in Progress / Concept</div>
  <h1>Project Echo: Desktop Sound Localization Array</h1>
  <p class="hero-subtitle">A conceptual hardware array designed to provide 360° visual feedback for critical environmental sounds.</p>
  <div class="echo-hero-image">
    {% include figure.liquid path="assets/img/projects/project-echo/device-render.png" title="Project Echo — sound localization device render" class="img-fluid rounded" %}
  </div>
</div>

<div class="echo-meta">
  <div class="meta-item">
    <div class="meta-label">Focus Area</div>
    <div class="meta-value">Digital Signal Processing (DSP), Microphone Arrays, Python</div>
  </div>
  <div class="meta-item">
    <div class="meta-label">Current Stage</div>
    <div class="meta-value">Proof of Concept & Algorithm Prototyping</div>
  </div>
  <div class="meta-item">
    <div class="meta-label">Target Application</div>
    <div class="meta-value">Desktop accessibility for the hearing-impaired</div>
  </div>
</div>

<h2 class="echo-section-title">The Vision</h2>

<div class="echo-vision-text" markdown="1">

Following the Cymatics exhibition, I conducted a survey on social media platforms targeting hearing-impaired individuals and their families, asking them about the difficulties they want the most help with in their daily lives. An overwhelming majority of participants reported that the inability to determine the direction of sounds greatly bothered them in their daily lives. And this wasn't just an inconvenience as well, it posed real safety risks. Critical alerts like fire alarms, doorbells, car horns, or someone calling for attention all require not just detection, but directional awareness to respond appropriately.

</div>

<div class="echo-goal-box">

**The Goal:** Design a compact desktop device that not only identifies specific critical sounds but also instantly indicates their angle of arrival (AoA) through intuitive visual cues.

</div>

<h2 class="echo-section-title">Proposed Architecture</h2>

<p class="echo-arch-intro">The current theoretical model is built around an 8-microphone circular array to capture 360° audio data.</p>

<div class="echo-layers">
  <div class="echo-layer">
    <div class="echo-layer-icon">◈</div>
    <div>
      <div class="echo-layer-title">Hardware Layer</div>
      <div class="echo-layer-desc">A high-performance DSP chip handles real-time audio sampling.</div>
    </div>
  </div>
  <div class="echo-layer">
    <div class="echo-layer-icon">&lt;/&gt;</div>
    <div>
      <div class="echo-layer-title">Software Layer</div>
      <div class="echo-layer-desc">Algorithms trained to recognize specific sound signatures.</div>
    </div>
  </div>
  <div class="echo-layer">
    <div class="echo-layer-icon">⚡</div>
    <div>
      <div class="echo-layer-title">Visual Feedback</div>
      <div class="echo-layer-desc">A segmented LED ring on top instantly illuminates to show the sound's origin.</div>
    </div>
  </div>
</div>

<div class="echo-algorithm-box">
  <div class="algo-label">Core Spatial Algorithm</div>
  <p style="margin:0 0 0.5rem;font-size:0.9rem;line-height:1.55;">The algorithm relies on Time Difference of Arrival (TDoA) between microphone pairs, utilizing the geometric relationship:</p>
  <div class="echo-formula">Δt = (d · cos θ) / v</div>
  <p class="algo-note">Where <em>d</em> = distance between mics, <em>v</em> = speed of sound, and <em>θ</em> = angle of arrival.</p>
</div>

<h2 class="echo-section-title">Current Progress</h2>

<div class="echo-progress-box" markdown="1">

As a software-first proof of concept, I have successfully developed and tested Python-based audio processing scripts on a Raspberry Pi. The system is capable of extracting audio features and recognizing specific critical sound signatures, such as standard fire alarm frequencies, from raw audio inputs. Additionally, I implemented basic directional detection using a two-microphone setup, applying Time Difference of Arrival (TDoA) calculations to determine whether a sound originates from the left or right side of the device.

The system is currently functional for binary directional output. I am now in the process of refining the detection accuracy before scaling up to a full 360° microphone array.

</div>

<div class="echo-roadmap">
  <h2 class="echo-section-title">Roadmap & Next Steps</h2>
  <p class="echo-roadmap-intro">Transitioning this concept into a functional physical prototype is my primary technical goal for the near future. As I dive deeper into engineering mathematics and core engineering principles, my roadmap includes:</p>
  <div class="echo-roadmap-card">
    <div class="card-index">01 //</div>
    <div class="card-title">Algorithm Upgrade</div>
    <div class="card-desc">Moving beyond simple recognition to implement robust TDoA algorithms for precise directional calculation.</div>
  </div>
</div>

</div>
