---
layout: default
title: "Projects"
permalink: /projects/
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

  .projects-page {
    font-family: 'DM Sans', sans-serif;
    color: var(--ink);
    background: var(--bg);
    min-height: 100vh;
    padding: 4rem 1.5rem;
  }

  .projects-inner {
    max-width: 680px;
    margin: 0 auto;
  }

  .page-header {
    padding-bottom: 2rem;
    border-bottom: 1px solid var(--border);
    margin-bottom: 2.5rem;
  }

  .page-label {
    font-size: 0.7rem;
    text-transform: uppercase;
    letter-spacing: 0.12em;
    font-weight: 500;
    color: var(--accent);
    margin-bottom: 0.75rem;
  }

  .page-header h1 {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(2rem, 5vw, 3rem);
    font-weight: 400;
    letter-spacing: -0.02em;
    margin-bottom: 0.5rem;
  }

  .page-header p {
    font-size: 0.9rem;
    color: var(--muted);
    font-weight: 300;
  }

  .project-list {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 0;
  }

  .project-item {
    border-top: 1px solid var(--border);
    padding: 1.75rem 0;
    display: grid;
    grid-template-columns: 1fr auto;
    gap: 1rem;
    align-items: start;
    opacity: 0;
    transform: translateY(6px);
    animation: fadeUp 0.3s forwards;
  }

  .project-item:nth-child(1) { animation-delay: 0.05s; }
  .project-item:nth-child(2) { animation-delay: 0.10s; }
  .project-item:nth-child(3) { animation-delay: 0.15s; }
  .project-item:nth-child(4) { animation-delay: 0.20s; }

  @keyframes fadeUp { to { opacity: 1; transform: translateY(0); } }

  .project-item:last-child { border-bottom: 1px solid var(--border); }

  .project-content { min-width: 0; }

  .project-tools {
    display: flex;
    flex-wrap: wrap;
    gap: 0.3rem;
    margin-bottom: 0.5rem;
  }

  .tool-tag {
    font-size: 0.65rem;
    letter-spacing: 0.07em;
    text-transform: uppercase;
    font-weight: 500;
    background: var(--tag-bg);
    color: var(--muted);
    padding: 0.15rem 0.45rem;
    border-radius: 1px;
  }

  .project-title {
    font-family: 'DM Serif Display', serif;
    font-size: 1.3rem;
    font-weight: 400;
    color: var(--ink);
    letter-spacing: -0.01em;
    line-height: 1.3;
    margin-bottom: 0.5rem;
  }

  .project-title a {
    color: inherit;
    text-decoration: none;
    transition: color 0.15s;
  }

  .project-title a:hover { color: var(--accent); }

  .project-desc {
    font-size: 0.9rem;
    color: #555;
    font-weight: 300;
    line-height: 1.65;
  }

  .project-link {
    font-size: 0.75rem;
    color: var(--muted);
    text-decoration: none;
    white-space: nowrap;
    font-weight: 300;
    padding-top: 0.25rem;
    transition: color 0.15s;
    display: flex;
    align-items: center;
    gap: 0.25rem;
  }

  .project-link:hover { color: var(--ink); }

  @media (max-width: 480px) {
    .project-item { grid-template-columns: 1fr; }
  }
</style>

<div class="projects-page">
  <div class="projects-inner">

    <div class="page-header">
      <div class="page-label">Work</div>
      <h1>Projects</h1>
      <p>Data analysis, visualization, and sports analytics projects.</p>
    </div>

    <ul class="project-list">

      <li class="project-item">
        <div class="project-content">
          <div class="project-tools">
            <span class="tool-tag">R</span>
            <span class="tool-tag">ggplot2</span>
          </div>
          <div class="project-title">NFL Running Back Analysis</div>
          <p class="project-desc">Analyzed usage trends for NFL running backs over the last four seasons, examining how carry distribution, efficiency, and role have shifted across teams and schemes.</p>
        </div>
        <!-- Optional: add a link below if you have a GitHub repo or article
        <a href="#" class="project-link">
          <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"/><polyline points="15 3 21 3 21 9"/><line x1="10" y1="14" x2="21" y2="3"/></svg>
          View
        </a>
        -->
      </li>

      <li class="project-item">
        <div class="project-content">
          <div class="project-tools">
            <span class="tool-tag">Python</span>
            <span class="tool-tag">Pandas</span>
          </div>
          <div class="project-title">NBA Salary Efficiency</div>
          <p class="project-desc">Evaluated team payroll efficiency across NBA teams, comparing salary spend against on-court production to identify over- and underperforming contracts.</p>
        </div>
      </li>

    </ul>

  </div>
</div>
