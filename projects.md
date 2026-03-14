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
    padding: 4rem 1.5rem 6rem;
  }

  .projects-inner { max-width: 680px; margin: 0 auto; }

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

  .page-header p { font-size: 0.9rem; color: var(--muted); font-weight: 300; }

  .project-list { list-style: none; }

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

  .project-desc {
    font-size: 0.9rem;
    color: #555;
    font-weight: 300;
    line-height: 1.65;
  }

  .project-links {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
    padding-top: 0.2rem;
  }

  .project-link {
    font-size: 0.75rem;
    color: var(--muted);
    text-decoration: none;
    white-space: nowrap;
    font-weight: 300;
    padding: 0.4rem 0.8rem;
    border: 1px solid var(--border);
    border-radius: 2px;
    transition: all 0.15s;
    display: flex;
    align-items: center;
    gap: 0.3rem;
    letter-spacing: 0.01em;
  }

  .project-link:hover { border-color: var(--ink); color: var(--ink); }

  @media (max-width: 480px) {
    .project-item { grid-template-columns: 1fr; }
    .project-links { flex-direction: row; flex-wrap: wrap; padding-top: 0.75rem; }
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
            <span class="tool-tag">nflfastR</span>
            <span class="tool-tag">nflreadr</span>
            <span class="tool-tag">gt</span>
            <span class="tool-tag">tidyverse</span>
          </div>
          <div class="project-title">Chicago Bears Personnel & Coverage Analysis (2025)</div>
          <p class="project-desc">Breakdown of the Bears' offensive personnel groupings, defensive coverage types, man vs zone usage, and defensive formations across the 2025 season — split by regular season and playoffs. Tables built with gt and data sourced via nflverse.</p>
        </div>
        <div class="project-links">
          <a href="https://github.com/MantovBiz/NFL-fast-R-Data-Visualizations-and-Breakdowns/tree/main/Chicago-Bears/2025" target="_blank" rel="noopener" class="project-link">
            <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"/><polyline points="15 3 21 3 21 9"/><line x1="10" y1="14" x2="21" y2="3"/></svg>
            View folder
          </a>
          <a href="https://github.com/MantovBiz/NFL-fast-R-Data-Visualizations-and-Breakdowns" target="_blank" rel="noopener" class="project-link">
            <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"/></svg>
            GitHub repo
          </a>
        </div>
      </li>

      <li class="project-item">
        <div class="project-content">
          <div class="project-tools">
            <span class="tool-tag">R</span>
            <span class="tool-tag">ggplot2</span>
          </div>
          <div class="project-title">NFL Running Back Analysis</div>
          <p class="project-desc">Analyzed usage trends for NFL running backs over the last four seasons, examining how carry distribution, efficiency, and role have shifted across teams and schemes.</p>
        </div>
        <div class="project-links">
          <a href="https://github.com/MantovBiz" target="_blank" rel="noopener" class="project-link">
            <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"/></svg>
            GitHub repo
          </a>
        </div>
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
        <div class="project-links">
          <a href="https://github.com/MantovBiz" target="_blank" rel="noopener" class="project-link">
            <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"/></svg>
            GitHub repo
          </a>
        </div>
      </li>

    </ul>

  </div>
</div>
