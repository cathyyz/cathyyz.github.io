---
layout: page
title: Project Echo — Desktop Sound Localization Array
description: A desktop accessibility device for the hearing-impaired — combining 360° directional feedback for critical sounds with real-time audio visualization, helping users both locate and experience sound.
img: assets/img/projects/project-echo/cover.png
importance: 3
category: work
portfolio: true
tags: [DSP, Accessibility, Python]
cta: "[ View Case Study ]"
---

<style>
  .echo-meta {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1rem;
    margin: 1.25rem 0 1.5rem;
  }
  .echo-meta .meta-item {
    padding: 0.85rem 1rem;
    border-left: 3px solid var(--global-theme-color, #2698ba);
    background: rgba(0, 0, 0, 0.03);
    border-radius: 0 4px 4px 0;
  }
  html[data-theme="dark"] .echo-meta .meta-item {
    background: rgba(255, 255, 255, 0.05);
  }
  .echo-meta .meta-label {
    font-size: 0.75rem;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.04em;
    opacity: 0.65;
    margin-bottom: 0.35rem;
  }
  .echo-meta .meta-value {
    font-size: 0.92rem;
    line-height: 1.45;
  }
  .echo-hero {
    max-width: 96%;
    margin: 0 auto 0.5rem;
  }
  .echo-split {
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
    gap: 1.5rem;
    align-items: center;
    margin: 1.25rem 0;
  }
  .echo-split .split-text {
    flex: 1 1 55%;
  }
  .echo-split .split-img {
    flex: 0 0 42%;
    max-width: 42%;
  }
  .echo-split img {
    width: 100%;
    height: auto;
    display: block;
  }
  .echo-phase-sub {
    margin: 1.5rem 0 0;
    padding: 0 0 0 1.25rem;
    border-left: 2px solid var(--global-theme-color, #2698ba);
  }
  .echo-phase-sub .phase-sub-title {
    font-size: 1.05rem;
    font-weight: 700;
    line-height: 1.35;
    margin: 0 0 0.75rem;
  }
  .echo-formula {
    text-align: center;
    font-size: 1.1rem;
    font-weight: 600;
    padding: 0.85rem;
    margin: 0.75rem 0;
    background: rgba(0, 0, 0, 0.03);
    border-radius: 6px;
    border: 1px solid rgba(0, 0, 0, 0.06);
  }
  html[data-theme="dark"] .echo-formula {
    background: rgba(255, 255, 255, 0.04);
    border-color: rgba(255, 255, 255, 0.08);
  }
  .echo-next-steps {
    margin: 0.75rem 0 0;
  }
  .echo-next-steps .next-step-item {
    margin: 1rem 0 0;
    padding: 0 0 0 1.25rem;
    border-left: 2px solid var(--global-theme-color, #2698ba);
  }
  .echo-next-steps .next-step-title {
    font-size: 1rem;
    font-weight: 600;
    line-height: 1.4;
    margin: 0 0 0.35rem;
  }
  .echo-next-steps .next-step-item p {
    margin: 0;
    font-size: 0.95rem;
    line-height: 1.55;
  }
  @media (max-width: 768px) {
    .echo-meta {
      grid-template-columns: 1fr;
    }
    .echo-split {
      flex-direction: column;
    }
    .echo-split .split-img {
      flex: 0 0 100%;
      max-width: 100%;
    }
  }
</style>

## Project Overview

<div class="echo-meta">
  <div class="meta-item">
    <div class="meta-label">Focus Area</div>
    <div class="meta-value">Digital Signal Processing (DSP) · Microphone Arrays · Python</div>
  </div>
  <div class="meta-item">
    <div class="meta-label">Current Stage</div>
    <div class="meta-value">Proof of Concept & Algorithm Prototyping · Work in Progress</div>
  </div>
  <div class="meta-item">
    <div class="meta-label">Target Application</div>
    <div class="meta-value">Desktop accessibility for the hearing-impaired</div>
  </div>
</div>

<div class="echo-hero">
  {% include figure.liquid path="assets/img/projects/project-echo/device-render.png" title="Project Echo — sound localization device concept render" class="img-fluid rounded z-depth-1" %}
</div>
<div class="caption">
  Concept render of the desktop sound localization array with 8-microphone circular array and directional LED feedback.
</div>

## Context

Following the Cymatics exhibition, I conducted a survey on social media platforms targeting hearing-impaired individuals and their families, asking them about the difficulties they want the most help with in their daily lives. An overwhelming majority of participants reported that the inability to determine the direction of sounds greatly bothered them in their daily lives.

This goes beyond mere inconvenience as it fundamentally affects their sense of control over their living environment. Not being able to locate a car horn while crossing the street, or know which direction a call for attention is coming from, creates persistent anxiety in daily navigation. While some assistive devices on the market do offer directional audio features, they often come with high price points, putting them out of reach for many who need them most.

**The Goal:** Design a compact, accessible desktop device that identifies critical sounds and instantly indicates their direction through intuitive visual cues while also allowing users to experience the beauty of sound itself, provide a calming, aesthetic presence that helps reduce the stress associated with auditory uncertainty.

## Proposed Architecture

The current theoretical model is built around an 8-microphone circular array to capture 360° audio data.

- **Hardware Layer:** A high-performance DSP chip handles real-time audio sampling, while a dedicated visualization module translates audio waveforms into dynamic visual patterns, extending the cymatics principles from my earlier project into a digital medium.
- **Software Layer:** Algorithms trained to recognize specific sound signatures.
- **Visual Feedback:** The interface serves a dual purpose. A segmented LED ring on top instantly illuminates to indicate the sound's origin direction. Simultaneously, an integrated display renders real-time visualizations of the sound's frequency and amplitude that allows users not only to locate sounds but to experience them aesthetically.

<div class="echo-phase-sub">

<div class="phase-sub-title">Core Spatial Algorithm</div>

<div markdown="1">

The algorithm relies on Time Difference of Arrival (TDoA) between microphone pairs, utilizing the geometric relationship:

</div>

<div class="echo-formula">Δt = (d · cos θ) / v</div>

<div markdown="1">

Where *d* = distance between mics, *v* = speed of sound, and *θ* = angle of arrival.

</div>

</div>

<div class="echo-split">
  <div class="split-text" markdown="1">

The device integrates microphone input, on-board signal processing, and a visual LED ring into a single desktop form factor — translating spatial audio data into immediate directional feedback for the user.

  </div>
  <div class="split-img">
    {% include figure.liquid path="assets/img/projects/project-echo/cover.png" title="Project Echo hardware prototype" class="img-fluid rounded z-depth-1" %}
  </div>
</div>

## Current Progress

As a software-first proof of concept, I have successfully developed and tested Python-based audio processing scripts on a Raspberry Pi. The system is capable of extracting audio features and recognizing specific critical sound signatures, such as standard fire alarm frequencies, from raw audio inputs. Additionally, I implemented basic directional detection using a two-microphone setup, applying Time Difference of Arrival (TDoA) calculations to determine whether a sound originates from the left or right side of the device.

The system is currently functional for binary directional output. I am now in the process of refining the detection accuracy before scaling up to a full 360° microphone array.

## Next Steps

<div class="echo-next-steps">

<div class="next-step-item">
<div class="next-step-title">Full 360° Directional Detection</div>
<p>Expanding from the current two-microphone setup to a circular array configuration.</p>
</div>

<div class="next-step-item">
<div class="next-step-title">Hardware Miniaturization</div>
<p>Once the prototype is finished, I'll focus on developing it into a custom compact form.</p>
</div>

<div class="next-step-item">
<div class="next-step-title">User Testing & Validation</div>
<p>I plan to recruit volunteers from the deaf and hard-of-hearing community to conduct small-scale usability testing to ensure the device's real-world effectiveness.</p>
</div>

</div>

## Reflection

Before this project, I assumed the hearing-impaired population's main difficulty was understanding and enjoying sounds. But the survey taught me otherwise, that their deeper struggle is not knowing where sounds come from, which creates a constant sense of unease in daily navigation. This reminded me to always start from real user needs rather than assumptions.

Looking ahead, I'm hoping to collaborate with others who share an interest in assistive technology, particularly in hardware and acoustic engineering, to bring this concept to a functional product.


