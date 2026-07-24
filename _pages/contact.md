---
layout: page
permalink: /contact/
title: Contact
description:
nav: true
nav_order: 6
_styles: |
  .post-header {
    display: none !important;
  }
---

<style>
  .post-header,
  header.post-header,
  .post .post-title,
  article .post-title,
  h1.post-title {
    display: none !important;
  }
  .contact-page {
    --contact-accent: var(--global-theme-color, #b509ac);
  }
  .contact-intro {
    margin: 0 0 1.5rem;
    font-size: 1rem;
    line-height: 1.6;
    opacity: 0.85;
  }
  .contact-list {
    display: grid;
    grid-template-columns: 1fr;
    gap: 0.85rem;
    max-width: 520px;
  }
  .contact-item {
    display: flex;
    align-items: center;
    gap: 1rem;
    padding: 1rem 1.15rem;
    border: 1px solid rgba(0, 0, 0, 0.08);
    border-radius: 10px;
    background: var(--global-bg-color, #fff);
    text-decoration: none;
    color: inherit;
    transition: box-shadow 0.2s ease, border-color 0.2s ease, transform 0.2s ease;
  }
  html[data-theme="dark"] .contact-item {
    border-color: rgba(255, 255, 255, 0.12);
  }
  .contact-item:hover {
    border-color: rgba(181, 9, 172, 0.3);
    box-shadow: 0 4px 16px rgba(0, 0, 0, 0.06);
    transform: translateY(-1px);
    color: inherit;
    text-decoration: none;
  }
  .contact-item .contact-icon {
    flex: 0 0 auto;
    width: 2.4rem;
    height: 2.4rem;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 8px;
    background: rgba(181, 9, 172, 0.08);
    color: var(--contact-accent);
    font-size: 1.15rem;
  }
  .contact-item .contact-text {
    flex: 1 1 auto;
    min-width: 0;
  }
  .contact-item .contact-label {
    font-size: 0.75rem;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.04em;
    opacity: 0.6;
    margin-bottom: 0.2rem;
  }
  .contact-item .contact-value {
    font-size: 0.98rem;
    font-weight: 550;
    line-height: 1.35;
    word-break: break-word;
  }
</style>

<div class="contact-page">

<p class="contact-intro">Feel free to reach out about research opportunities, project collaborations, or just to connect.</p>

<div class="contact-list">
  <a class="contact-item" href="mailto:zcy2026@berkeley.edu">
    <div class="contact-icon"><i class="fa-solid fa-envelope"></i></div>
    <div class="contact-text">
      <div class="contact-label">Email</div>
      <div class="contact-value">zcy2026@berkeley.edu</div>
    </div>
  </a>

  <a class="contact-item" href="https://www.linkedin.com/in/chenyu-zhou-993755336" target="_blank" rel="noopener">
    <div class="contact-icon"><i class="fa-brands fa-linkedin"></i></div>
    <div class="contact-text">
      <div class="contact-label">LinkedIn</div>
      <div class="contact-value">linkedin.com/in/chenyu-zhou-993755336</div>
    </div>
  </a>

  <a class="contact-item" href="https://github.com/cathyyz" target="_blank" rel="noopener">
    <div class="contact-icon"><i class="fa-brands fa-github"></i></div>
    <div class="contact-text">
      <div class="contact-label">GitHub</div>
      <div class="contact-value">github.com/cathyyz</div>
    </div>
  </a>
</div>

</div>
