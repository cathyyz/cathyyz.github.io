---
layout: page
title: Cymatics — Visualizing the Invisible
description: An interactive installation engineered to visualize sound through cymatics — transforming acoustic frequencies into real-time water patterns for public exhibition.
img: assets/img/projects/cymatics/cover.png
importance: 2
category: work
portfolio: true
tags: [Hardware, Accessibility, Arduino]
cta: "[ View Case Study ]"
---

<style>
  .cymatics-meta {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1rem;
    margin: 1.25rem 0 1.5rem;
  }
  .cymatics-meta .meta-item {
    padding: 0.85rem 1rem;
    border-left: 3px solid var(--global-theme-color, #2698ba);
    background: rgba(0, 0, 0, 0.03);
    border-radius: 0 4px 4px 0;
  }
  html[data-theme="dark"] .cymatics-meta .meta-item {
    background: rgba(255, 255, 255, 0.05);
  }
  .cymatics-meta .meta-label {
    font-size: 0.75rem;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.04em;
    opacity: 0.65;
    margin-bottom: 0.35rem;
  }
  .cymatics-meta .meta-value {
    font-size: 0.92rem;
    line-height: 1.45;
  }
  .cymatics-hero {
    max-width: 96%;
    margin: 0 auto 0.5rem;
  }
  .cymatics-split {
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
    gap: 1.5rem;
    align-items: center;
    margin: 1.25rem 0;
  }
  .cymatics-split .split-text {
    flex: 1 1 55%;
  }
  .cymatics-split .split-img {
    flex: 0 0 42%;
    max-width: 42%;
  }
  .cymatics-split img {
    width: 100%;
    height: auto;
    display: block;
  }
  .cymatics-pair {
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
    gap: 1rem;
    align-items: stretch;
    margin: 1.25rem 0 0.5rem;
  }
  .cymatics-pair .pair-col {
    flex: 1 1 50%;
    display: flex;
    flex-direction: column;
  }
  .cymatics-pair .pair-col figure {
    flex: 1 1 auto;
    height: 300px;
    margin: 0;
    overflow: hidden;
    border-radius: 4px;
  }
  .cymatics-pair .pair-col figure img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: center;
    display: block;
  }
  .cymatics-pair .pair-label {
    font-size: 0.8rem;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.03em;
    opacity: 0.6;
    margin-bottom: 0.5rem;
  }
  .cymatics-full {
    max-width: 96%;
    margin: 1.25rem auto 0.5rem;
  }
  .cymatics-exhibition-text {
    max-width: 96%;
    margin: 1rem auto 0;
    font-size: 0.98rem;
    line-height: 1.65;
  }
  .cymatics-phase-sub {
    margin: 1.5rem 0 0;
    padding: 0 0 0 1.25rem;
    border-left: 2px solid var(--global-theme-color, #2698ba);
  }
  .cymatics-phase-sub .phase-sub-title {
    font-size: 1.05rem;
    font-weight: 700;
    line-height: 1.35;
    margin: 0 0 0.75rem;
  }
  @media (max-width: 768px) {
    .cymatics-meta {
      grid-template-columns: 1fr;
    }
    .cymatics-split {
      flex-direction: column;
    }
    .cymatics-split .split-img {
      flex: 0 0 100%;
      max-width: 100%;
    }
    .cymatics-pair {
      flex-direction: column;
    }
    .cymatics-pair .pair-col figure {
      height: auto;
    }
    .cymatics-pair .pair-col figure img {
      height: auto;
      object-fit: contain;
    }
  }
</style>

## Project Overview

<div class="cymatics-meta">
  <div class="meta-item">
    <div class="meta-label">Core Technologies</div>
    <div class="meta-value">Wave Physics · Optical Engineering · Hardware Prototyping · Arduino</div>
  </div>
  <div class="meta-item">
    <div class="meta-label">Timeline</div>
    <div class="meta-value">4 years</div>
  </div>
  <div class="meta-item">
    <div class="meta-label">Outcome</div>
    <div class="meta-value">Public exhibition installation where visitors experience music transformed into dynamic ceiling projections in real-time</div>
  </div>
</div>

<div class="cymatics-hero">
  {% include figure.liquid path="assets/img/projects/cymatics/overview.png" title="Cymatics installation — sound visualized through water ripple patterns" class="img-fluid rounded z-depth-1" %}
</div>
<div class="caption">
  A visitor observes cymatic patterns forming on the water surface as sound vibrations pass through the resonance chamber.
</div>

## Context

In 7th grade, I watched a documentary about hearing-impaired children rehearsing for a musical. It struck me that something as fundamental as "listening to music" simply doesn't exist for an entire community of people.

This sparked a question: **Can sound be seen?** Could visual experience allow hearing-impaired individuals to feel the rhythm and emotion of music?

### Phase 1: Laser Harp Prototype

<div class="cymatics-split">
  <div class="split-text" markdown="1">

**Goal:** Design an interactive sound device for hearing-impaired children.

**Approach:** Built an "invisible harp" using Arduino and laser sensors. Hand movements triggered different notes, and the sound traveled through a speaker into a water surface, creating ripple patterns.

**Result:** Successfully observed different frequencies producing distinct geometric patterns. Achieved a small-scale interactive demonstration of cymatics principles.

  </div>
  <div class="split-img">
    {% include figure.liquid path="assets/img/projects/cymatics/laser-harp-prototype.png" title="Phase 1 laser harp prototype with Arduino and laser sensors" class="img-fluid rounded z-depth-1" %}
  </div>
</div>

### Phase 2: Exhibition Installation — Redesigning for Public Space

The original prototype was designed for single-user viewing, but a public exhibition serves dozens of simultaneous viewers. Simply scaling up the water container would make acoustic resonance exponentially harder to achieve. Therefore, I decided to project the patterns onto the ceiling, allowing comfortable viewing for large audiences while keeping the resonance system compact. But how did I achieve this?

<div class="cymatics-phase-sub">

<div class="phase-sub-title">Engineering Design — Solving the Clear Magnification Problem</div>

<div markdown="1">

Magnified projection creates an inherent tension: higher magnification means blurrier images. Water ripple patterns are dynamic and detail-rich, demanding high optical clarity.

**Solution:** I figured that I can use the concave mirror itself to hold water. This way, the water surface sits directly on a focusing reflector. And by fitting the concave mirror directly into the concave surface of the sound box, I can maximize efficiency and minimize space.

**Structure:**

- Speaker at the base generates vibrations
- Concave mirror mounted above, filled with a thin layer of water; vibrations transfer through the frame to the water surface, forming patterns
- Light source illuminates the water from above
- The concave mirror reflects and focuses the patterned light upward
- A convex lens in the shade plate provides further magnification control

</div>
<div class="cymatics-pair">
  <div class="pair-col">
    <div class="pair-label">Initial exhibition setup</div>
    {% include figure.liquid path="assets/img/projects/cymatics/engineering-v2.png" title="Initial exhibition installation setup" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="pair-col">
    <div class="pair-label">Customized design</div>
    {% include figure.liquid path="assets/img/projects/cymatics/engineering-v1.png" title="Customized exhibition installation with optimized optical system" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Left: initial exhibition setup. Right: customized design after lens and resonance chamber optimization.
</div>

</div>

## Exhibition & Execution

<div class="cymatics-full">
  {% include figure.liquid path="assets/img/projects/cymatics/exhibition-experience.png" title="Public exhibition — cymatic patterns projected onto the ceiling" class="img-fluid rounded z-depth-1" %}
</div>

<div class="cymatics-exhibition-text" markdown="1">

In 2024, the installation was showcased at the Sound Visualization Exhibition at the China Academy of Art. As the technical demonstrator, I was fully responsible for the hands-on booth setup, testing lens positions and focal lengths to balance magnification against clarity. I conducted real-time technical demonstrations for diverse visitors and actively facilitated audience interaction. Many visitors reported that simultaneously "hearing" and "seeing" music created a meditative, calming effect.

</div>

## Reflection

This project taught me what it truly means to engineer something from zero to one. To achieve clear projection of water ripples, I had to simultaneously consider wave physics, geometric optics, and mechanical structure. During calibration, I continuously adjusted lens focal lengths, light source angles, and water depth; every variable affected the final projection quality, which instilled a habit of systematic testing and documentation.

Over four years — from an 8th-grade Arduino prototype to a 10th-grade exhibition piece — I learned to keep pushing forward under ambiguous goals rather than waiting for a perfect plan. Most importantly, I understood that technology's value lies not in its complexity, but in **whose problem it solves**.

The exhibition also taught me the importance of communication in technology. During the public exhibition, I guided visitors of all ages and backgrounds through the installation. I learned to translate concepts like "acoustic resonance" and "optical magnification" into intuitive explanations. This experience showed me that the ability to bridge technical depth and accessible communication is essential, whether explaining findings to stakeholders, collaborating across teams, or supporting others in understanding data.
