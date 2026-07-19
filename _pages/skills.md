---
layout: page
permalink: /skills/
title: Skills
description:
nav: true
nav_order: 3
_styles: |
  .post-header {
    display: none !important;
  }
---

<style>
  .post-header {
    display: none !important;
  }
  .skills-page {
    --skills-accent: var(--global-theme-color, #b509ac);
  }
  .skills-section-title {
    font-size: 1.15rem;
    font-weight: 700;
    margin: 0 0 0.85rem;
  }
  .skills-section-title.spaced {
    margin-top: 2rem;
  }
  .skills-stack {
    display: grid;
    grid-template-columns: 1fr;
    gap: 0.85rem;
  }
  .skill-row {
    display: grid;
    grid-template-columns: 180px 1fr;
    gap: 1rem;
    align-items: start;
    padding: 1rem 1.15rem;
    border: 1px solid rgba(0, 0, 0, 0.08);
    border-radius: 10px;
    background: var(--global-bg-color, #fff);
  }
  html[data-theme="dark"] .skill-row {
    border-color: rgba(255, 255, 255, 0.12);
  }
  .skill-row .skill-label {
    font-size: 0.95rem;
    font-weight: 700;
    line-height: 1.35;
    color: var(--skills-accent);
  }
  .skill-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 0.45rem;
  }
  .skill-tag {
    font-size: 0.82rem;
    font-weight: 500;
    padding: 0.3rem 0.7rem;
    border-radius: 999px;
    background: rgba(0, 0, 0, 0.05);
    line-height: 1.3;
  }
  html[data-theme="dark"] .skill-tag {
    background: rgba(255, 255, 255, 0.08);
  }
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 1rem;
  }
  .skill-card {
    padding: 1.05rem 1.15rem 1.1rem;
    border: 1px solid rgba(0, 0, 0, 0.08);
    border-radius: 10px;
    background: var(--global-bg-color, #fff);
  }
  html[data-theme="dark"] .skill-card {
    border-color: rgba(255, 255, 255, 0.12);
  }
  .skill-card .skill-category {
    font-size: 1.02rem;
    font-weight: 700;
    line-height: 1.35;
    margin: 0 0 0.3rem;
  }
  .skill-card .skill-context {
    font-size: 0.84rem;
    line-height: 1.45;
    opacity: 0.65;
    margin: 0 0 0.8rem;
  }
  .skills-lang {
    margin-top: 1.25rem;
    padding: 0.95rem 1.1rem;
    border-left: 3px solid var(--skills-accent);
    border-radius: 0 8px 8px 0;
    background: rgba(0, 0, 0, 0.03);
  }
  html[data-theme="dark"] .skills-lang {
    background: rgba(255, 255, 255, 0.05);
  }
  .skills-lang .lang-title {
    font-size: 0.95rem;
    font-weight: 700;
    margin: 0 0 0.55rem;
  }
  @media (max-width: 768px) {
    .skill-row {
      grid-template-columns: 1fr;
      gap: 0.55rem;
    }
    .skills-grid {
      grid-template-columns: 1fr;
    }
  }
</style>

<div class="skills-page">

<h2 class="skills-section-title">Core Skills</h2>

<div class="skills-stack">
  <div class="skill-row">
    <div class="skill-label">Programming Languages</div>
    <div class="skill-tags">
      <span class="skill-tag">Python</span>
      <span class="skill-tag">Java</span>
      <span class="skill-tag">HTML</span>
    </div>
  </div>

  <div class="skill-row">
    <div class="skill-label">Frameworks & Libraries</div>
    <div class="skill-tags">
      <span class="skill-tag">PyTorch</span>
      <span class="skill-tag">Pandas</span>
      <span class="skill-tag">NumPy</span>
      <span class="skill-tag">Matplotlib</span>
      <span class="skill-tag">Arduino</span>
    </div>
  </div>

  <div class="skill-row">
    <div class="skill-label">Tools</div>
    <div class="skill-tags">
      <span class="skill-tag">Google Workspace</span>
      <span class="skill-tag">Git</span>
      <span class="skill-tag">Stata</span>
      <span class="skill-tag">Data Visualization</span>
    </div>
  </div>
</div>

<h2 class="skills-section-title spaced">From Projects</h2>

<div class="skills-grid">
  <div class="skill-card">
    <div class="skill-category">AI & Machine Learning</div>
    <p class="skill-context">Self-adaptive RL agent · PKU-Stanford Gen-AI Program</p>
    <div class="skill-tags">
      <span class="skill-tag">Reinforcement Learning</span>
      <span class="skill-tag">Q-Learning</span>
      <span class="skill-tag">Experience Replay</span>
      <span class="skill-tag">Feature Extraction</span>
    </div>
  </div>

  <div class="skill-card">
    <div class="skill-category">Data & Statistics</div>
    <p class="skill-context">AI Art Perception Study · 672 observations</p>
    <div class="skill-tags">
      <span class="skill-tag">Regression Analysis</span>
      <span class="skill-tag">Mediation Analysis</span>
      <span class="skill-tag">Survey Design</span>
      <span class="skill-tag">Reliability Testing</span>
    </div>
  </div>

  <div class="skill-card">
    <div class="skill-category">Hardware & Engineering</div>
    <p class="skill-context">Cymatics exhibition installation</p>
    <div class="skill-tags">
      <span class="skill-tag">Hardware Prototyping</span>
      <span class="skill-tag">Optical Engineering</span>
      <span class="skill-tag">Wave Physics</span>
      <span class="skill-tag">System Calibration</span>
    </div>
  </div>

  <div class="skill-card">
    <div class="skill-category">Signal Processing</div>
    <p class="skill-context">Project Echo · sound localization</p>
    <div class="skill-tags">
      <span class="skill-tag">Digital Signal Processing</span>
      <span class="skill-tag">TDoA</span>
      <span class="skill-tag">Microphone Arrays</span>
      <span class="skill-tag">Audio Feature Extraction</span>
    </div>
  </div>
</div>

<div class="skills-lang">
  <div class="lang-title">Languages</div>
  <div class="skill-tags">
    <span class="skill-tag">English — Fluent</span>
    <span class="skill-tag">Mandarin — Native</span>
  </div>
</div>

</div>
