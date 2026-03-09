---
layout: default
title: "About"
permalink: /about/
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Sans:wght@300;400;500&display=swap');

  :root {
    --ink: #1a1a1a;
    --muted: #888;
    --border: #e8e8e8;
    --accent: #c0392b;
    --bg: #fafaf8;
    --tag-bg: #f0f0ee;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  .about-page {
    font-family: 'DM Sans', sans-serif;
    color: var(--ink);
    background: var(--bg);
    min-height: 100vh;
    padding: 4rem 1.5rem;
  }

  .about-inner {
    max-width: 680px;
    margin: 0 auto;
  }

  .about-header {
    padding-bottom: 2rem;
    border-bottom: 1px solid var(--border);
    margin-bottom: 2.5rem;
  }

  .about-label {
    font-size: 0.7rem;
    text-transform: uppercase;
    letter-spacing: 0.12em;
    font-weight: 500;
    color: var(--accent);
    margin-bottom: 0.75rem;
  }

  .about-header h1 {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(2rem, 5vw, 3rem);
    font-weight: 400;
    letter-spacing: -0.02em;
    margin-bottom: 0.75rem;
    line-height: 1.1;
  }

  .about-header p {
    font-size: 1rem;
    color: #444;
    font-weight: 300;
    line-height: 1.75;
  }

  .about-section {
    margin-bottom: 2.5rem;
  }

  .about-section h2 {
    font-family: 'DM Serif Display', serif;
    font-size: 1.25rem;
    font-weight: 400;
    letter-spacing: -0.01em;
    margin-bottom: 1rem;
    color: var(--ink);
  }

  .skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
    gap: 0.75rem;
  }

  .skill-card {
    border: 1px solid var(--border);
    border-radius: 2px;
    padding: 0.85rem 1rem;
    background: #fff;
  }

  .skill-card-label {
    font-size: 0.68rem;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    font-weight: 500;
    color: var(--muted);
    margin-bottom: 0.4rem;
  }

  .skill-card-tools {
    font-size: 0.875rem;
    font-weight: 300;
    color: var(--ink);
    line-height: 1.5;
  }

  .interests-list {
    list-style: none;
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
  }

  .interests-list li {
    font-size: 0.8rem;
    font-weight: 400;
    background: var(--tag-bg);
    color: var(--ink);
    padding: 0.3rem 0.75rem;
    border-radius: 2px;
    letter-spacing: 0.01em;
  }

  .cta-row {
    display: flex;
    gap: 0.75rem;
    flex-wrap: wrap;
    margin-top: 2rem;
    padding-top: 2rem;
    border-top: 1px solid var(--border);
  }

  .cta-btn {
    font-family: 'DM Sans', sans-serif;
    font-size: 0.82rem;
    font-weight: 400;
    text-decoration: none;
    padding: 0.55rem 1.1rem;
    border-radius: 2px;
    transition: all 0.15s;
    letter-spacing: 0.02em;
  }

  .cta-primary {
    background: var(--ink);
    color: #fff;
    border: 1px solid var(--ink);
  }

  .cta-primary:hover { background: #333; }

  .cta-secondary {
    background: transparent;
    color: var(--ink);
    border: 1px solid var(--border);
  }

  .cta-secondary:hover { border-color: var(--ink); }
</style>

<div class="about-page">
  <div class="about-inner">

    <div class="about-header">
      <div class="about-label">About</div>
      <h1>Manuel Tovar</h1>
      <p>MIS & Business Analytics student at DePaul University, passionate about analytics, data visualization, and research. I enjoy analyzing data, building dashboards, and writing about my findings.</p>
    </div>

    <div class="about-section">
      <h2>Skills & Tools</h2>
      <div class="skills-grid">
        <div class="skill-card">
          <div class="skill-card-label">Data Analysis</div>
          <div class="skill-card-tools">R, Python, SQL</div>
        </div>
        <div class="skill-card">
          <div class="skill-card-label">Visualization</div>
          <div class="skill-card-tools">Tableau, ggplot2, Matplotlib</div>
        </div>
        <div class="skill-card">
          <div class="skill-card-label">Web & Portfolio</div>
          <div class="skill-card-tools">GitHub Pages, Jekyll, Markdown</div>
        </div>
      </div>
    </div>

    <div class="about-section">
      <h2>Interests</h2>
      <ul class="interests-list">
        <li>Sports analytics</li>
        <li>Predictive modeling</li>
        <li>Data visualization</li>
        <li>Music</li>
        <li>Film</li>
        <li>Books</li>
      </ul>
    </div>

    <div class="cta-row">
      <a href="/articles/" class="cta-btn cta-primary">Read Articles</a>
      <a href="/projects/" class="cta-btn cta-secondary">View Projects</a>
    </div>

  </div>
</div>
