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
    margin-bottom: 2rem;
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

  /* ── Search bar ──────────────────────────────────────────────────────────── */
  .search-wrap {
    position: relative;
    margin-bottom: 0.5rem;
  }

  .search-wrap svg {
    position: absolute;
    left: 0.9rem;
    top: 50%;
    transform: translateY(-50%);
    color: var(--muted);
    pointer-events: none;
  }

  #proj-search {
    width: 100%;
    padding: 0.75rem 2.8rem 0.75rem 2.6rem;
    font-family: 'DM Sans', sans-serif;
    font-size: 0.9rem;
    font-weight: 300;
    border: 1px solid var(--border);
    border-radius: 2px;
    background: #fff;
    color: var(--ink);
    outline: none;
    transition: border-color 0.2s;
    /* Prevent browser autocomplete from injecting unexpected values */
    autocomplete: off;
  }

  #proj-search:focus { border-color: var(--ink); }
  #proj-search::placeholder { color: #bbb; }

  /* Clear button */
  #proj-clear {
    position: absolute;
    right: 0.75rem;
    top: 50%;
    transform: translateY(-50%);
    background: none;
    border: none;
    cursor: pointer;
    color: var(--muted);
    padding: 0.2rem;
    display: none;
    line-height: 1;
    transition: color 0.15s;
  }
  #proj-clear:hover { color: var(--ink); }

  #proj-meta {
    font-size: 0.74rem;
    color: var(--muted);
    font-weight: 300;
    letter-spacing: 0.03em;
    text-transform: uppercase;
    min-height: 1.1em;
    margin-bottom: 1.5rem;
  }

  /* ── Project list ──────────────────────────────────────────────────────── */
  .project-list { list-style: none; }

  .project-item {
    border-top: 1px solid var(--border);
    padding: 1.75rem 0;
    display: grid;
    grid-template-columns: 1fr auto;
    gap: 1rem;
    align-items: start;
  }

  .project-item:last-child { border-bottom: 1px solid var(--border); }

  .project-item[hidden] { display: none; }

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

  /* ── Highlight matched text ──────────────────────────────────────────────── */
  mark { background: #fff3b0; color: inherit; padding: 0 1px; border-radius: 1px; }

  /* ── Empty state ─────────────────────────────────────────────────────────── */
  #proj-empty {
    padding: 2.5rem 0;
    color: var(--muted);
    font-size: 0.9rem;
    font-style: italic;
    font-weight: 300;
    border-top: 1px solid var(--border);
    display: none;
  }

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

    <!-- Safe search: plain text filter, no eval, no innerHTML from input -->
    <div class="search-wrap">
      <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
        <circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/>
      </svg>
      <input
        type="text"
        id="proj-search"
        placeholder="Search projects…"
        autocomplete="off"
        spellcheck="false"
        maxlength="100"
        aria-label="Search projects"
      />
      <button id="proj-clear" aria-label="Clear search">
        <svg width="13" height="13" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
          <line x1="18" y1="6" x2="6" y2="18"/><line x1="6" y1="6" x2="18" y2="18"/>
        </svg>
      </button>
    </div>
    <div id="proj-meta"></div>

    <ul class="project-list" id="proj-list">

      <li class="project-item"
          data-title="Chicago Bears Personnel Coverage Analysis 2025"
          data-tools="R nflfastR nflreadr gt tidyverse"
          data-desc="Breakdown of the Bears offensive personnel groupings defensive coverage types man vs zone usage and defensive formations across the 2025 season split by regular season and playoffs">
        <div class="project-content">
          <div class="project-tools">
            <span class="tool-tag">R</span>
            <span class="tool-tag">nflfastR</span>
            <span class="tool-tag">nflreadr</span>
            <span class="tool-tag">gt</span>
            <span class="tool-tag">tidyverse</span>
          </div>
          <div class="project-title">Chicago Bears Personnel &amp; Coverage Analysis (2025)</div>
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
          <a href="https://mantovbiz.github.io/research/2026/03/13/Chicago-Bears-2025-Season-Formations.html" class="project-link">
            <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/><polyline points="14 2 14 8 20 8"/><line x1="16" y1="13" x2="8" y2="13"/><line x1="16" y1="17" x2="8" y2="17"/><polyline points="10 9 9 9 8 9"/></svg>
            Read article
          </a>
        </div>
      </li>

      <li class="project-item"
          data-title="NFL Running Back Analysis"
          data-tools="R ggplot2"
          data-desc="Analyzed usage trends for NFL running backs over the last four seasons examining carry distribution efficiency and role shifts across teams and schemes">
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

      <li class="project-item"
          data-title="NBA Salary Efficiency"
          data-tools="Python Pandas"
          data-desc="Evaluated team payroll efficiency across NBA teams comparing salary spend against on-court production to identify over and underperforming contracts">
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

    <p id="proj-empty">No projects match your search.</p>

  </div>
</div>

<script>
(function () {
  var input   = document.getElementById('proj-search');
  var clearBtn = document.getElementById('proj-clear');
  var metaEl  = document.getElementById('proj-meta');
  var emptyEl = document.getElementById('proj-empty');
  var items   = Array.prototype.slice.call(
    document.querySelectorAll('#proj-list .project-item')
  );

  /* Pre-compute searchable text per item from data attributes only —
     never from user input, so there is no injection surface. */
  var searchData = items.map(function (li) {
    return (
      (li.dataset.title  || '') + ' ' +
      (li.dataset.tools  || '') + ' ' +
      (li.dataset.desc   || '')
    ).toLowerCase();
  });

  function sanitizeQuery(raw) {
    /* Strip everything that isn't letters, numbers, spaces, or hyphens.
       This prevents any CSS/HTML/JS injection from ever reaching the DOM. */
    return raw.replace(/[^a-zA-Z0-9 \-]/g, '').trim().toLowerCase();
  }

  function setHighlight(titleEl, descEl, terms) {
    /* We use textContent to read and a Text node to write — never innerHTML
       from user input. Highlights are added safely via DOM manipulation. */
    if (!terms.length) {
      titleEl.childNodes[0] && (titleEl.textContent = titleEl.dataset.orig || titleEl.textContent);
      descEl  && (descEl.textContent  = descEl.dataset.orig  || descEl.textContent);
      return;
    }

    [titleEl, descEl].forEach(function (el) {
      if (!el) return;
      if (!el.dataset.orig) el.dataset.orig = el.textContent;
      var text = el.dataset.orig;
      /* Build a safe regex from sanitized terms */
      var pattern = terms.map(function (t) {
        return t.replace(/[-]/g, '\\-');
      }).join('|');
      var re = new RegExp('(' + pattern + ')', 'gi');

      /* Clear and rebuild with <mark> nodes — no innerHTML from user input */
      while (el.firstChild) el.removeChild(el.firstChild);
      text.split(re).forEach(function (chunk) {
        if (re.test(chunk)) {
          var mark = document.createElement('mark');
          mark.textContent = chunk;
          el.appendChild(mark);
          re.lastIndex = 0;
        } else {
          el.appendChild(document.createTextNode(chunk));
        }
      });
    });
  }

  function render() {
    var raw   = input.value;
    var query = sanitizeQuery(raw);
    var terms = query ? query.split(/\s+/).filter(Boolean) : [];

    clearBtn.style.display = raw.length ? 'block' : 'none';

    var visible = 0;

    items.forEach(function (li, i) {
      var titleEl = li.querySelector('.project-title');
      var descEl  = li.querySelector('.project-desc');
      var match   = !terms.length || terms.every(function (t) {
        return searchData[i].indexOf(t) > -1;
      });

      if (match) {
        li.removeAttribute('hidden');
        setHighlight(titleEl, descEl, terms);
        visible++;
      } else {
        li.setAttribute('hidden', '');
      }
    });

    emptyEl.style.display = visible === 0 ? 'block' : 'none';

    if (terms.length) {
      metaEl.textContent = visible + ' project' + (visible !== 1 ? 's' : '') + ' found';
    } else {
      metaEl.textContent = '';
    }
  }

  input.addEventListener('input', render);

  clearBtn.addEventListener('click', function () {
    input.value = '';
    render();
    input.focus();
  });

  render();
})();
</script>
