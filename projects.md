---
layout: default
title: "Projects"
permalink: /projects/
---

<style>
  :root { --ink: #1a1a1a; --muted: #888; --border: #e8e8e8; --accent: #c0392b; --bg: #fafaf8; --tag-bg: #f0f0ee; }
  * { box-sizing: border-box; margin: 0; padding: 0; }

  .projects-page { font-family: 'DM Sans', sans-serif; color: var(--ink); background: var(--bg); min-height: 100vh; padding: 4rem 1.5rem 6rem; }
  .projects-inner { max-width: 720px; margin: 0 auto; }

  .page-header { padding-bottom: 2rem; border-bottom: 1px solid var(--border); margin-bottom: 2rem; }
  .page-eyebrow { display: flex; align-items: center; gap: 0.6rem; font-size: 0.65rem; text-transform: uppercase; letter-spacing: 0.14em; font-weight: 500; color: var(--accent); margin-bottom: 0.8rem; }
  .page-eyebrow::before { content: ''; display: inline-block; width: 20px; height: 1.5px; background: var(--accent); flex-shrink: 0; }
  .page-header h1 { font-family: 'DM Serif Display', serif; font-size: clamp(2rem,5vw,3rem); font-weight: 400; letter-spacing: -0.02em; margin-bottom: 0.5rem; }
  .page-header p { font-size: 0.9rem; color: var(--muted); font-weight: 300; }

  .search-wrap { position: relative; margin-bottom: 0.5rem; }
  .search-wrap svg { position: absolute; left: 0.9rem; top: 50%; transform: translateY(-50%); color: var(--muted); pointer-events: none; }
  #proj-search { width: 100%; padding: 0.75rem 2.8rem 0.75rem 2.6rem; font-family: 'DM Sans', sans-serif; font-size: 0.9rem; font-weight: 300; border: 1px solid var(--border); border-radius: 2px; background: #fff; color: var(--ink); outline: none; transition: border-color 0.2s; }
  #proj-search:focus { border-color: var(--ink); }
  #proj-search::placeholder { color: #bbb; }
  #proj-clear { position: absolute; right: 0.75rem; top: 50%; transform: translateY(-50%); background: none; border: none; cursor: pointer; color: var(--muted); padding: 0.2rem; display: none; line-height: 1; transition: color 0.15s; }
  #proj-clear:hover { color: var(--ink); }
  #proj-meta { font-size: 0.74rem; color: var(--muted); font-weight: 300; letter-spacing: 0.03em; text-transform: uppercase; min-height: 1.1em; margin-bottom: 1.5rem; }

  .project-list { list-style: none; }
  .project-item { background: #fff; border: 1px solid var(--border); border-radius: 4px; padding: 1.6rem; margin-bottom: 1rem; transition: border-color 0.15s, box-shadow 0.15s; opacity: 0; transform: translateY(8px); animation: cardIn 0.35s forwards; }
  .project-item:nth-child(1) { animation-delay: 0.05s; }
  .project-item:nth-child(2) { animation-delay: 0.12s; }
  .project-item:nth-child(3) { animation-delay: 0.19s; }
  @keyframes cardIn { to { opacity: 1; transform: translateY(0); } }
  .project-item:hover { border-color: #bbb; box-shadow: 0 4px 16px rgba(0,0,0,0.06); }
  .project-item[hidden] { display: none; }

  .project-card-top { display: flex; align-items: flex-start; justify-content: space-between; gap: 1rem; margin-bottom: 0.75rem; flex-wrap: wrap; }
  .project-tools { display: flex; flex-wrap: wrap; gap: 0.3rem; }
  .tool-tag { font-size: 0.62rem; letter-spacing: 0.07em; text-transform: uppercase; font-weight: 500; background: var(--tag-bg); color: var(--muted); padding: 0.15rem 0.45rem; border-radius: 1px; }
  .status-badge { font-size: 0.6rem; text-transform: uppercase; letter-spacing: 0.08em; font-weight: 500; padding: 0.2rem 0.5rem; border-radius: 1px; white-space: nowrap; flex-shrink: 0; }
  .status-complete { background: #eaf6ee; color: #27ae60; }
  .status-in-progress { background: #fff8e1; color: #e67e22; }

  .project-title { font-family: 'DM Serif Display', serif; font-size: 1.2rem; font-weight: 400; color: var(--ink); letter-spacing: -0.01em; line-height: 1.3; margin-bottom: 0.5rem; }
  .project-desc { font-size: 0.875rem; color: #555; font-weight: 300; line-height: 1.7; margin-bottom: 1rem; }

  .project-links { display: flex; flex-wrap: wrap; gap: 0.5rem; }
  .project-link { font-size: 0.75rem; color: var(--muted); text-decoration: none; font-weight: 400; padding: 0.4rem 0.8rem; border: 1px solid var(--border); border-radius: 2px; transition: all 0.15s; display: inline-flex; align-items: center; gap: 0.3rem; letter-spacing: 0.01em; }
  .project-link:hover { border-color: var(--ink); color: var(--ink); }

  mark { background: #fff3b0; color: inherit; padding: 0 1px; border-radius: 1px; }
  #proj-empty { padding: 2.5rem 0; color: var(--muted); font-size: 0.9rem; font-style: italic; font-weight: 300; border-top: 1px solid var(--border); display: none; }

  @media (max-width: 480px) {
    .project-card-top { flex-direction: column; }
    .project-links { flex-direction: column; }
    .project-link { justify-content: center; }
  }
</style>

<div class="projects-page">
  <div class="projects-inner">
    <div class="page-header">
      <div class="page-eyebrow">Work</div>
      <h1>Projects</h1>
      <p>Any work I do can be found here with links to documentation!</p>
    </div>

    <div class="search-wrap">
      <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true"><circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/></svg>
      <input type="text" id="proj-search" placeholder="Search projects…" autocomplete="off" spellcheck="false" maxlength="100" aria-label="Search projects"/>
      <button id="proj-clear" aria-label="Clear search">
        <svg width="13" height="13" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true"><line x1="18" y1="6" x2="6" y2="18"/><line x1="6" y1="6" x2="18" y2="18"/></svg>
      </button>
    </div>
    <div id="proj-meta" aria-live="polite"></div>

    <ul class="project-list" id="proj-list">

      <li class="project-item" data-title="Chicago Bears Personnel Coverage Analysis 2025" data-tools="R nflfastR nflreadr gt tidyverse" data-desc="Breakdown of the Bears offensive personnel groupings defensive coverage types man vs zone usage and defensive formations across the 2025 season split by regular season and playoffs">
        <div class="project-card-top">
          <div class="project-tools">
            <span class="tool-tag">R</span><span class="tool-tag">nflfastR</span><span class="tool-tag">nflreadr</span><span class="tool-tag">gt</span><span class="tool-tag">tidyverse</span>
          </div>
          <span class="status-badge status-complete">Complete</span>
        </div>
        <div class="project-title">Chicago Bears Personnel &amp; Coverage Analysis (2025)</div>
        <p class="project-desc">Breakdown of the Bears' offensive personnel groupings, defensive coverage types, man vs zone usage, and defensive formations across the 2025 season — split by regular season and playoffs.</p>
        <div class="project-links">
          <a href="https://github.com/MantovBiz/NFL-fast-R-Data-Visualizations-and-Breakdowns/tree/main/Chicago-Bears/2025" target="_blank" rel="noopener" class="project-link">
            <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true"><path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"/><polyline points="15 3 21 3 21 9"/><line x1="10" y1="14" x2="21" y2="3"/></svg>
            View folder
          </a>
          <a href="https://github.com/MantovBiz/NFL-fast-R-Data-Visualizations-and-Breakdowns" target="_blank" rel="noopener" class="project-link">
            <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"/></svg>
            GitHub repo
          </a>
          <a href="/research/Chicago-Bears-2025-Season-Formations/" class="project-link">
            <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/><polyline points="14 2 14 8 20 8"/><line x1="16" y1="13" x2="8" y2="13"/><line x1="16" y1="17" x2="8" y2="17"/></svg>
            Read article
          </a>
        </div>
      </li>
<li class="project-item" data-title="Steam Game Market Analysis" data-tools="R Power BI SteamSpy API" data-desc="Analysis of the top 100 most played Steam games exploring pricing trends review patterns and ownership distribution across free and paid titles using live API data">
  <div class="project-card-top">
    <div class="project-tools">
      <span class="tool-tag">R</span><span class="tool-tag">Power BI</span><span class="tool-tag">SteamSpy API</span>
    </div>
    <span class="status-badge status-complete">Complete</span>
  </div>
  <div class="project-title">Steam Game Market Analysis</div>
  <p class="project-desc">Analysis of the top 100 most played Steam games, exploring pricing trends, review patterns, and ownership distribution across free and paid titles — built with live SteamSpy API data and visualized in Power BI.</p>
  <div class="project-links">
    <a href="https://github.com/MantovBiz/Steam-Market-Analysis-4-24-26" target="_blank" rel="noopener" class="project-link">
      <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"/></svg>
      GitHub repo
    </a>
  </div>
</li>
