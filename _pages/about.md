---
layout: page
title: About
permalink: /
description:
profile:
  align: right
  image: prof_pic.jpg
  image_circular: false
  more_info: >
    <p>Engineering Math & Statistics @ UC Berkeley</p>
subtitle: <a href="#">Affiliations</a>

selected_papers: false
social: true

announcements:
  enabled: false

latest_posts:
  enabled: true
  scrollable: true
  limit: 3

featured_projects_limit: 2
_styles: |
  .post-header {
    display: none !important;
  }
---

<style>
  .post-header {
    display: none !important;
  }
  .portfolio-about {
    --portfolio-accent: var(--global-theme-color, #b509ac);
  }
  .portfolio-about-header {
    margin-bottom: 1.75rem;
  }
  .portfolio-about-header h1 {
    font-size: 2rem;
    font-weight: 700;
    margin-bottom: 0.35rem;
  }
  .portfolio-about-header .subtitle {
    font-size: 1rem;
    opacity: 0.85;
  }
  .portfolio-about-header .subtitle a {
    color: var(--portfolio-accent);
    text-decoration: none;
  }
  .portfolio-about-intro {
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
    gap: 2rem;
    align-items: flex-start;
    margin-bottom: 2.5rem;
  }
  .portfolio-about-intro .intro-text {
    flex: 1 1 62%;
    font-size: 0.98rem;
    line-height: 1.65;
  }
  .portfolio-about-intro .intro-text h2 {
    font-size: 1.15rem;
    font-weight: 700;
    margin: 1.5rem 0 0.75rem;
  }
  .portfolio-about-intro .intro-profile {
    flex: 0 0 30%;
    max-width: 30%;
    text-align: center;
  }
  .portfolio-about-intro .intro-profile img {
    width: 100%;
    height: auto;
    border-radius: 6px;
  }
  .portfolio-about-intro .intro-profile .profile-info {
    margin-top: 0.75rem;
    font-size: 0.9rem;
    line-height: 1.5;
    opacity: 0.85;
  }
  .portfolio-section-title {
    font-size: 1.35rem;
    font-weight: 700;
    margin: 0 0 1rem;
  }
  .portfolio-featured-row {
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
    gap: 1rem;
    margin-bottom: 2.5rem;
  }
  .portfolio-featured-card {
    flex: 1 1 50%;
    text-decoration: none;
    color: inherit;
    border: 1px solid rgba(0, 0, 0, 0.08);
    border-radius: 8px;
    overflow: hidden;
    background: var(--global-bg-color, #fff);
    transition: box-shadow 0.2s ease, transform 0.2s ease;
  }
  html[data-theme="dark"] .portfolio-featured-card {
    border-color: rgba(255, 255, 255, 0.12);
  }
  .portfolio-featured-card:hover {
    box-shadow: 0 6px 20px rgba(0, 0, 0, 0.08);
    transform: translateY(-2px);
    color: inherit;
    text-decoration: none;
  }
  .portfolio-featured-card img {
    width: 100%;
    height: 180px;
    object-fit: cover;
    display: block;
  }
  .portfolio-featured-card .card-title {
    padding: 0.85rem 1rem 1rem;
    font-size: 0.95rem;
    font-weight: 600;
    line-height: 1.4;
  }
  .portfolio-posts-list {
    list-style: none;
    padding: 0;
    margin: 0;
  }
  .portfolio-posts-list li {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: baseline;
    gap: 1rem;
    padding: 0.55rem 0;
    border-bottom: 1px solid rgba(0, 0, 0, 0.06);
    font-size: 0.92rem;
  }
  html[data-theme="dark"] .portfolio-posts-list li {
    border-bottom-color: rgba(255, 255, 255, 0.08);
  }
  .portfolio-posts-list .post-date {
    flex: 0 0 auto;
    opacity: 0.55;
    white-space: nowrap;
  }
  .portfolio-posts-list .post-title {
    flex: 1 1 auto;
    text-align: right;
    color: var(--portfolio-accent);
    text-decoration: none;
    font-weight: 500;
  }
  .portfolio-posts-list .post-title:hover {
    text-decoration: underline;
  }
  .portfolio-social {
    margin-top: 2rem;
    padding-top: 1.5rem;
    border-top: 1px solid rgba(0, 0, 0, 0.06);
  }
  .portfolio-social img {
    max-width: 1.25rem;
    max-height: 1.25rem;
    object-fit: contain;
  }
  html[data-theme="dark"] .portfolio-social {
    border-top-color: rgba(255, 255, 255, 0.08);
  }
  @media (max-width: 768px) {
    .portfolio-about-intro {
      flex-direction: column-reverse;
    }
    .portfolio-about-intro .intro-profile {
      flex: 0 0 100%;
      max-width: 220px;
      margin: 0 auto;
    }
    .portfolio-featured-row {
      flex-direction: column;
    }
    .portfolio-posts-list li {
      flex-direction: column;
      align-items: flex-start;
      gap: 0.25rem;
    }
    .portfolio-posts-list .post-title {
      text-align: left;
    }
  }
</style>

<div class="portfolio-about">

<div class="portfolio-about-header">
  <h1>{{ site.title }}</h1>
  <div class="subtitle">{{ page.subtitle }}</div>
</div>

<div class="portfolio-about-intro">
  <div class="intro-text" markdown="1">

Hi, I'm Cathy Zhou, an incoming freshman studying Engineering Math & Statistics at UC Berkeley.

I'm interested in data analysis, artificial intelligence, and engineering — how we can apply data and machine learning to build systems and functional products that solve real-world problems. I'm also curious about human-computer interaction and designing technology that people actually want to use. 

I'm currently teaching myself Verilog and SQL, and building this portfolio to document my learning journey. I'm looking forward to exploring courses in statistics, computer science, and machine learning this year.

I'm open to research opportunities, project collaborations, or just connecting with others interested in AI, data, and engineering. Feel free to reach out!

  </div>
  <div class="intro-profile">
    {% if page.profile.image %}
      {% assign profile_image_path = page.profile.image | prepend: 'assets/img/' %}
      {% include figure.liquid loading="eager" path=profile_image_path class="img-fluid z-depth-1 rounded" alt=page.profile.image cache_bust=true %}
    {% endif %}
    {% if page.profile.more_info %}
      <div class="profile-info">{{ page.profile.more_info }}</div>
    {% endif %}
  </div>
</div>

<h2 class="portfolio-section-title">Featured Projects</h2>

{% assign featured_projects = site.projects | where: "portfolio", true | sort: "importance" %}
{% if page.featured_projects_limit %}
  {% assign featured_projects_limit = page.featured_projects_limit %}
{% else %}
  {% assign featured_projects_limit = featured_projects.size %}
{% endif %}

<div class="portfolio-featured-row">
  {% for project in featured_projects limit: featured_projects_limit %}
    <a class="portfolio-featured-card" href="{{ project.url | relative_url }}">
      {% if project.img %}
        {% include figure.liquid loading="lazy" path=project.img alt=project.title class="card-img-top" %}
      {% endif %}
      <div class="card-title">{{ project.title }}</div>
    </a>
  {% endfor %}
</div>

{% if page.latest_posts.enabled %}
  <h2 class="portfolio-section-title">latest posts</h2>
  <ul class="portfolio-posts-list">
    {% assign latest_posts = site.posts %}
    {% if page.latest_posts.limit %}
      {% assign latest_posts_limit = page.latest_posts.limit %}
    {% else %}
      {% assign latest_posts_limit = latest_posts.size %}
    {% endif %}
    {% for item in latest_posts limit: latest_posts_limit %}
      <li>
        <span class="post-date">{{ item.date | date: '%b %d, %Y' }}</span>
        {% if item.redirect == blank %}
          <a class="post-title" href="{{ item.url | relative_url }}">{{ item.title }}</a>
        {% elsif item.redirect contains '://' %}
          <a class="post-title" href="{{ item.redirect }}" target="_blank">{{ item.title }}</a>
        {% else %}
          <a class="post-title" href="{{ item.redirect | relative_url }}">{{ item.title }}</a>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
{% endif %}

{% if page.social %}
  <div class="portfolio-social">
    {% social_links %}
    {% if site.contact_note %}
      <p class="text-muted mt-2">{{ site.contact_note }}</p>
    {% endif %}
  </div>
{% endif %}

</div>



