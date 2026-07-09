---
layout: page
title: Projects
permalink: /projects/
description:
nav: true
nav_order: 2
_styles: |
  article .post-header {
    display: none;
  }
---

<style>
  .portfolio-projects {
    --portfolio-accent: var(--global-theme-color, #b509ac);
  }
  .portfolio-projects-header h1 {
    font-size: 2rem;
    font-weight: 700;
    margin-bottom: 1.5rem;
  }
  .portfolio-projects-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 1.5rem;
  }
  .portfolio-project-card {
    display: flex;
    flex-direction: column;
    border: 1px solid rgba(0, 0, 0, 0.1);
    border-radius: 10px;
    overflow: hidden;
    background: var(--global-bg-color, #fff);
    height: 100%;
  }
  html[data-theme="dark"] .portfolio-project-card {
    border-color: rgba(255, 255, 255, 0.12);
  }
  .portfolio-project-card .card-image {
    width: 100%;
    aspect-ratio: 16 / 10;
    overflow: hidden;
    background: rgba(0, 0, 0, 0.04);
  }
  .portfolio-project-card .card-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    display: block;
  }
  .portfolio-project-card .card-body {
    display: flex;
    flex-direction: column;
    flex: 1 1 auto;
    padding: 1.1rem 1.15rem 1.15rem;
  }
  .portfolio-project-card .card-title {
    font-size: 1.05rem;
    font-weight: 700;
    line-height: 1.35;
    margin-bottom: 0.65rem;
  }
  .portfolio-project-card .card-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 0.4rem;
    margin-bottom: 0.75rem;
  }
  .portfolio-project-card .card-tag {
    font-size: 0.72rem;
    font-weight: 500;
    padding: 0.2rem 0.55rem;
    border-radius: 999px;
    background: rgba(0, 0, 0, 0.05);
    color: inherit;
    opacity: 0.75;
  }
  html[data-theme="dark"] .portfolio-project-card .card-tag {
    background: rgba(255, 255, 255, 0.08);
  }
  .portfolio-project-card .card-desc {
    font-size: 0.88rem;
    line-height: 1.55;
    opacity: 0.82;
    margin-bottom: 1rem;
    flex: 1 1 auto;
  }
  .portfolio-project-card .card-cta {
    display: block;
    text-align: center;
    padding: 0.55rem 1rem;
    border: 1.5px solid var(--portfolio-accent);
    border-radius: 6px;
    color: var(--portfolio-accent);
    font-size: 0.88rem;
    font-weight: 600;
    text-decoration: none;
    transition: background 0.2s ease, color 0.2s ease;
  }
  .portfolio-project-card .card-cta:hover {
    background: var(--portfolio-accent);
    color: #fff;
    text-decoration: none;
  }
  @media (max-width: 768px) {
    .portfolio-projects-grid {
      grid-template-columns: 1fr;
    }
  }
</style>

<div class="portfolio-projects">

<div class="portfolio-projects-header">
  <h1>{{ page.title }}</h1>
</div>

{% assign portfolio_projects = site.projects | where: "portfolio", true | sort: "importance" %}

<div class="portfolio-projects-grid">
  {% for project in portfolio_projects %}
    <article class="portfolio-project-card">
      {% if project.img %}
        <div class="card-image">
          {% include figure.liquid loading="lazy" path=project.img alt=project.title %}
        </div>
      {% endif %}
      <div class="card-body">
        <h2 class="card-title">{{ project.title }}</h2>
        {% if project.tags %}
          <div class="card-tags">
            {% for tag in project.tags %}
              <span class="card-tag">{{ tag }}</span>
            {% endfor %}
          </div>
        {% endif %}
        {% if project.description %}
          <p class="card-desc">{{ project.description }}</p>
        {% endif %}
        <a class="card-cta" href="{{ project.url | relative_url }}">
          {% if project.cta %}{{ project.cta }}{% else %}[ View Case Study ]{% endif %}
        </a>
      </div>
    </article>
  {% endfor %}
</div>

</div>
