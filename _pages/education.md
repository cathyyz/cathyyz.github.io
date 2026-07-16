---
layout: page
permalink: /education/
title: Education
description: Academic background and coursework.
nav: true
nav_order: 4
_styles: |
  .post-header {
    display: none !important;
  }
---

<style>
  .post-header {
    display: none !important;
  }
  .edu-page {
    --edu-accent: var(--global-theme-color, #b509ac);
  }
  .edu-page h1 {
    font-size: 2rem;
    font-weight: 700;
    margin-bottom: 1.5rem;
  }
  .edu-school {
    margin-bottom: 2rem;
    padding: 1.15rem 1.25rem;
    border-left: 3px solid var(--edu-accent);
    background: rgba(0, 0, 0, 0.03);
    border-radius: 0 8px 8px 0;
  }
  html[data-theme="dark"] .edu-school {
    background: rgba(255, 255, 255, 0.05);
  }
  .edu-school .school-name {
    font-size: 1.2rem;
    font-weight: 700;
    margin: 0 0 0.35rem;
    line-height: 1.35;
  }
  .edu-school .school-name a {
    color: inherit;
    text-decoration: none;
  }
  .edu-school .school-name a:hover {
    color: var(--edu-accent);
  }
  .edu-school .degree {
    font-size: 1rem;
    margin: 0 0 0.25rem;
  }
  .edu-school .meta {
    font-size: 0.9rem;
    opacity: 0.7;
    margin: 0;
  }
  .edu-section-title {
    font-size: 1.2rem;
    font-weight: 700;
    margin: 0 0 0.35rem;
  }
  .edu-section-note {
    font-size: 0.92rem;
    opacity: 0.7;
    margin: 0 0 1.1rem;
  }
  .edu-courses {
    display: grid;
    grid-template-columns: 1fr;
    gap: 0.85rem;
  }
  .edu-course {
    padding: 0.95rem 1.1rem;
    border: 1px solid rgba(0, 0, 0, 0.08);
    border-radius: 8px;
    background: var(--global-bg-color, #fff);
  }
  html[data-theme="dark"] .edu-course {
    border-color: rgba(255, 255, 255, 0.12);
  }
  .edu-course .course-code {
    font-size: 0.78rem;
    font-weight: 600;
    letter-spacing: 0.03em;
    text-transform: uppercase;
    color: var(--edu-accent);
    margin-bottom: 0.25rem;
  }
  .edu-course .course-name {
    font-size: 1.02rem;
    font-weight: 650;
    margin: 0 0 0.35rem;
    line-height: 1.35;
  }
  .edu-course .course-focus {
    font-size: 0.92rem;
    line-height: 1.5;
    margin: 0;
    opacity: 0.85;
  }
  @media (max-width: 768px) {
    .edu-page h1 {
      font-size: 1.7rem;
    }
  }
</style>

<div class="edu-page">

# Education

<div class="edu-school">
  <p class="school-name"><a href="https://engineering.berkeley.edu/" target="_blank" rel="noopener">University of California, Berkeley</a></p>
  <p class="degree"><strong>B.S.</strong> in Engineering Mathematics · College of Engineering</p>
  <p class="meta">Incoming Freshman · Expected Class of 2030 · Berkeley, CA</p>
</div>

<h2 class="edu-section-title">Current Coursework</h2>
<p class="edu-section-note">Fall 2026 · skill-focused overview for clubs and internship applications</p>

<div class="edu-courses">
  <div class="edu-course">
    <div class="course-code">CS 61A</div>
    <div class="course-name">Structure and Interpretation of Computer Programs</div>
    <p class="course-focus">Python, abstraction, recursion, and functional programming foundations.</p>
  </div>
  <div class="edu-course">
    <div class="course-code">Math 53</div>
    <div class="course-name">Multivariable Calculus</div>
    <p class="course-focus">Multivariable calculus for modeling systems in engineering and data analysis.</p>
  </div>
  <div class="edu-course">
    <div class="course-code">Physics 7A</div>
    <div class="course-name">Physics for Scientists and Engineers</div>
    <p class="course-focus">Classical mechanics and quantitative problem-solving for engineering contexts.</p>
  </div>
</div>

</div>

