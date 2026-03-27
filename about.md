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
    --card-bg: #ffffff;
    --terminal-bg: #1a1a1a;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  .about-page {
    font-family: 'DM Sans', sans-serif;
    color: var(--ink);
    background: var(--bg);
    min-height: 100vh;
    padding: 4rem 1.5rem 6rem;
  }

  .about-inner { max-width: 960px; margin: 0 auto; }

  /* ── Back link ────────────────────────────────────────────────────────────── */
  .about-back {
    display: inline-flex;
    align-items: center;
    gap: 0.35rem;
    font-size: 0.78rem;
    color: var(--muted);
    text-decoration: none;
    font-weight: 300;
    letter-spacing: 0.02em;
    margin-bottom: 3rem;
    transition: color 0.15s;
  }
  .about-back:hover { color: var(--ink); }

  /* ── Section label ────────────────────────────────────────────────────────── */
  .section-label {
    font-size: 0.68rem;
    text-transform: uppercase;
    letter-spacing: 0.12em;
    font-weight: 500;
    color: var(--muted);
    margin-bottom: 1.25rem;
    padding-bottom: 0.6rem;
    border-bottom: 1px solid var(--border);
  }

  /* ── Terminal hero ────────────────────────────────────────────────────────── */
  .terminal-hero {
    background: var(--terminal-bg);
    border-radius: 6px;
    padding: 2rem 2rem 1.75rem;
    margin-bottom: 3rem;
    position: relative;
    overflow: hidden;
  }

  .terminal-titlebar {
    display: flex;
    align-items: center;
    gap: 0.4rem;
    margin-bottom: 1.5rem;
  }

  .terminal-dot {
    width: 10px;
    height: 10px;
    border-radius: 50%;
  }

  .dot-red    { background: #ff5f57; }
  .dot-yellow { background: #ffbd2e; }
  .dot-green  { background: #28ca41; }

  .terminal-body {
    font-family: 'Courier New', monospace;
    font-size: 0.88rem;
    line-height: 2;
    color: #555;
  }

  .t-line {
    display: flex;
    gap: 1rem;
    opacity: 0;
    transform: translateY(4px);
    transition: opacity 0.3s ease, transform 0.3s ease;
  }

  .t-line.show { opacity: 1; transform: translateY(0); }

  .t-prompt { color: var(--accent); user-select: none; }
  .t-key    { color: #555; min-width: 90px; }
  .t-arrow  { color: #333; }
  .t-val    { color: #e8e8e4; }
  .t-val.name-val {
    font-family: 'DM Serif Display', serif;
    font-size: 1.5rem;
    color: #ffffff;
    letter-spacing: -0.02em;
    line-height: 1.2;
  }

  .t-cursor {
    display: inline-block;
    width: 8px;
    height: 1em;
    background: var(--accent);
    vertical-align: middle;
    margin-left: 2px;
    animation: blink 1s step-end infinite;
  }

  @keyframes blink { 50% { opacity: 0; } }

  /* ── Animated stats ───────────────────────────────────────────────────────── */
  .stats-section { margin-bottom: 3rem; }

  .stats-row {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
    gap: 1px;
    background: var(--border);
    border: 1px solid var(--border);
    border-radius: 4px;
    overflow: hidden;
  }

  .stat-box {
    background: var(--card-bg);
    padding: 1.5rem 1.25rem;
    text-align: center;
  }

  .stat-number {
    font-family: 'DM Serif Display', serif;
    font-size: 2.5rem;
    font-weight: 400;
    color: var(--ink);
    line-height: 1;
    letter-spacing: -0.03em;
  }

  .stat-number sup {
    font-family: 'DM Sans', sans-serif;
    font-size: 1rem;
    color: var(--accent);
    vertical-align: super;
  }

  .stat-label {
    font-size: 0.68rem;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    color: var(--muted);
    margin-top: 0.4rem;
    font-weight: 400;
  }

  /* ── Skills ───────────────────────────────────────────────────────────────── */
  .skills-section { margin-bottom: 3rem; }

  .skill-row {
    display: flex;
    align-items: center;
    gap: 1rem;
    margin-bottom: 0.85rem;
  }

  .skill-name {
    font-size: 0.82rem;
    color: var(--ink);
    font-weight: 400;
    width: 100px;
    flex-shrink: 0;
  }

  .skill-track {
    flex: 1;
    height: 2px;
    background: var(--border);
    border-radius: 1px;
    overflow: hidden;
  }

  .skill-fill {
    height: 100%;
    background: var(--ink);
    border-radius: 1px;
    width: 0;
    transition: width 1.2s cubic-bezier(0.4, 0, 0.2, 1);
  }

  .skill-fill.accent { background: var(--accent); }

  .skill-pct {
    font-size: 0.72rem;
    color: var(--muted);
    width: 32px;
    text-align: right;
    font-weight: 300;
  }

  /* ── Interests ────────────────────────────────────────────────────────────── */
  .interests-section { margin-bottom: 3rem; }

  .interests-wrap { display: flex; flex-wrap: wrap; gap: 0.5rem; margin-bottom: 1rem; }

  .interest-tag {
    font-size: 0.78rem;
    padding: 0.4rem 0.9rem;
    border: 1px solid var(--border);
    border-radius: 2px;
    background: var(--card-bg);
    color: var(--muted);
    cursor: pointer;
    transition: all 0.15s;
    font-weight: 300;
    user-select: none;
  }

  .interest-tag:hover,
  .interest-tag.active {
    background: var(--ink);
    color: #fff;
    border-color: var(--ink);
  }

  .interest-tooltip {
    min-height: 1.4rem;
    font-size: 0.82rem;
    color: var(--accent);
    font-style: italic;
    font-weight: 300;
    padding-top: 0.25rem;
    transition: opacity 0.2s;
  }

  /* ── CTA ──────────────────────────────────────────────────────────────────── */
  .cta-section {
    padding-top: 2rem;
    border-top: 1px solid var(--border);
    display: flex;
    gap: 0.75rem;
    flex-wrap: wrap;
  }

  .btn {
    font-family: 'DM Sans', sans-serif;
    font-size: 0.82rem;
    font-weight: 400;
    text-decoration: none;
    padding: 0.55rem 1.1rem;
    border-radius: 2px;
    transition: all 0.15s;
    letter-spacing: 0.02em;
  }

  .btn-primary { background: var(--ink); color: #fff; border: 1px solid var(--ink); }
  .btn-primary:hover { background: #333; }
  .btn-secondary { background: transparent; color: var(--ink); border: 1px solid var(--border); }
  .btn-secondary:hover { border-color: var(--ink); }

  /* ── Fade in on scroll ────────────────────────────────────────────────────── */
  .fade-up {
    opacity: 0;
    transform: translateY(16px);
    transition: opacity 0.55s ease, transform 0.55s ease;
  }

  .fade-up.visible { opacity: 1; transform: translateY(0); }

  /* ── Mobile ───────────────────────────────────────────────────────────────── */
  @media (max-width: 600px) {
    .about-page   { padding: 2rem 1rem 4rem; }
    .terminal-hero { padding: 1.25rem; }
    .terminal-body { font-size: 0.78rem; }
    .t-val.name-val { font-size: 1.2rem; }
    .stat-number  { font-size: 2rem; }
    .skill-name   { width: 80px; font-size: 0.78rem; }
  }
</style>

<div class="about-page">
  <div class="about-inner">

    <a href="/" class="about-back">← Home</a>

    <!-- ── Terminal Hero ──────────────────────────────────────────────────── -->
    <div class="terminal-hero" id="terminal-hero">
      <div class="terminal-titlebar">
        <div class="terminal-dot dot-red"></div>
        <div class="terminal-dot dot-yellow"></div>
        <div class="terminal-dot dot-green"></div>
      </div>
      <div class="terminal-body" id="terminal-body"></div>
    </div>

    <!-- ── Animated Stats ────────────────────────────────────────────────── -->
    <div class="stats-section fade-up" id="stats-section">
      <div class="section-label">By the numbers</div>
      <div class="stats-row">
        <div class="stat-box">
          <div class="stat-number" id="stat-projects">0<sup>+</sup></div>
          <div class="stat-label">Projects built</div>
        </div>
        <div class="stat-box">
          <div class="stat-number" id="stat-articles">0<sup>+</sup></div>
          <div class="stat-label">Articles written</div>
        </div>
        <div class="stat-box">
          <div class="stat-number" id="stat-tools">0<sup>+</sup></div>
          <div class="stat-label">Tools mastered</div>
        </div>
        <div class="stat-box">
          <div class="stat-number" id="stat-years">0<sup>yrs</sup></div>
          <div class="stat-label">Years studying</div>
        </div>
      </div>
    </div>

    <!-- ── Skills ────────────────────────────────────────────────────────── -->
    <div class="skills-section fade-up" id="skills-section">
      <div class="section-label">Skills & tools</div>
      <div id="skill-bars">
        <div class="skill-row">
          <div class="skill-name">R</div>
          <div class="skill-track"><div class="skill-fill" data-pct="88"></div></div>
          <div class="skill-pct">88%</div>
        </div>
        <div class="skill-row">
          <div class="skill-name">Python</div>
          <div class="skill-track"><div class="skill-fill" data-pct="75"></div></div>
          <div class="skill-pct">75%</div>
        </div>
        <div class="skill-row">
          <div class="skill-name">SQL</div>
          <div class="skill-track"><div class="skill-fill" data-pct="70"></div></div>
          <div class="skill-pct">70%</div>
        </div>
        <div class="skill-row">
          <div class="skill-name">Tableau</div>
          <div class="skill-track"><div class="skill-fill accent" data-pct="65"></div></div>
          <div class="skill-pct">65%</div>
        </div>
        <div class="skill-row">
          <div class="skill-name">ggplot2</div>
          <div class="skill-track"><div class="skill-fill accent" data-pct="85"></div></div>
          <div class="skill-pct">85%</div>
        </div>
        <div class="skill-row">
          <div class="skill-name">Matplotlib</div>
          <div class="skill-track"><div class="skill-fill" data-pct="68"></div></div>
          <div class="skill-pct">68%</div>
        </div>
      </div>
    </div>

    <!-- ── Interests ─────────────────────────────────────────────────────── -->
    <div class="interests-section fade-up" id="interests-section">
      <div class="section-label">Interests</div>
      <div class="interests-wrap">
        <span class="interest-tag" data-tip="I use R and Python to find stories hidden inside sports data.">Sports analytics</span>
        <span class="interest-tag" data-tip="ggplot2, Tableau, and D3 — making numbers actually mean something visually.">Data visualization</span>
        <span class="interest-tag" data-tip="Building models that predict game outcomes and player performance.">Predictive modeling</span>
        <span class="interest-tag" data-tip="Kubrick, Scorsese, and anything A24 puts out. Cinema as craft.">Film & cinema</span>
        <span class="interest-tag" data-tip="Everything from jazz and soul to hip-hop. Always something playing.">Music</span>
        <span class="interest-tag" data-tip="Non-fiction mostly — data, business, and the occasional novel.">Books</span>
      </div>
      <div class="interest-tooltip" id="interest-tip"></div>
    </div>

    <!-- ── CTA ───────────────────────────────────────────────────────────── -->
    <div class="cta-section fade-up" id="cta-section">
      <a href="/articles/" class="btn btn-primary">Read articles</a>
      <a href="/projects/" class="btn btn-secondary">View projects</a>
      <a href="/contact/" class="btn btn-secondary">Get in touch →</a>
      <a href="https://www.linkedin.com/in/mantovbiz/" target="_blank" rel="noopener" class="btn btn-secondary">LinkedIn →</a>
    </div>

  </div>
</div>

<script>
  // ── Terminal animation ────────────────────────────────────────────────────
  const lines = [
    { prompt: true, key: null,       val: 'whoami',                         cls: 'val' },
    { prompt: false, key: 'name',    val: 'Manuel Tovar',                   cls: 'val name-val' },
    { prompt: false, key: 'role',    val: 'MIS & Business Analytics @ DePaul University', cls: 'val' },
    { prompt: false, key: 'location',val: 'Chicago, IL',                    cls: 'val' },
    { prompt: false, key: 'stack',   val: 'R · Python · SQL · Tableau',     cls: 'val' },
    { prompt: false, key: 'writing', val: 'sports analytics · data · film', cls: 'val' },
    { prompt: false, key: 'status',  val: 'open to opportunities',          cls: 'val', cursor: true },
  ];

  const body = document.getElementById('terminal-body');

  function buildLine(line) {
    const div = document.createElement('div');
    div.className = 't-line';
    if (line.prompt) {
      div.innerHTML = `<span class="t-prompt">$</span><span class="t-val">&nbsp;${line.val}</span>`;
    } else {
      const cursor = line.cursor ? '<span class="t-cursor"></span>' : '';
      div.innerHTML = `<span class="t-key">${line.key}</span><span class="t-arrow">→</span><span class="${line.cls}">${line.val}${cursor}</span>`;
    }
    return div;
  }

  function runTerminal() {
    lines.forEach((line, i) => {
      const el = buildLine(line);
      body.appendChild(el);
      setTimeout(() => el.classList.add('show'), 300 + i * 220);
    });
  }

  // ── Stat counter ──────────────────────────────────────────────────────────
  const statTargets = [
    { id: 'stat-projects', val: 12, suffix: '<sup>+</sup>' },
    { id: 'stat-articles', val: 8,  suffix: '<sup>+</sup>' },
    { id: 'stat-tools',    val: 6,  suffix: '<sup>+</sup>' },
    { id: 'stat-years',    val: 3,  suffix: '<sup>yrs</sup>' },
  ];

  function animateStats() {
    statTargets.forEach(({ id, val, suffix }) => {
      const el = document.getElementById(id);
      let cur = 0;
      const step = Math.max(1, Math.ceil(val / 40));
      const iv = setInterval(() => {
        cur = Math.min(cur + step, val);
        el.innerHTML = cur + suffix;
        if (cur >= val) clearInterval(iv);
      }, 35);
    });
  }

  // ── Skill bars ────────────────────────────────────────────────────────────
  function animateBars() {
    document.querySelectorAll('.skill-fill').forEach(bar => {
      bar.style.width = bar.dataset.pct + '%';
    });
  }

  // ── Interest tags ─────────────────────────────────────────────────────────
  const tags = document.querySelectorAll('.interest-tag');
  const tip  = document.getElementById('interest-tip');

  tags.forEach(tag => {
    tag.addEventListener('mouseenter', () => {
      tags.forEach(t => t.classList.remove('active'));
      tag.classList.add('active');
      tip.textContent = tag.dataset.tip;
    });
    tag.addEventListener('mouseleave', () => {
      tag.classList.remove('active');
      tip.textContent = '';
    });
  });

  // ── Scroll observer ───────────────────────────────────────────────────────
  let statsAnimated = false;
  let barsAnimated  = false;

  const observer = new IntersectionObserver(entries => {
    entries.forEach(entry => {
      if (!entry.isIntersecting) return;
      entry.target.classList.add('visible');
      if (entry.target.id === 'stats-section' && !statsAnimated) {
        statsAnimated = true;
        setTimeout(animateStats, 200);
      }
      if (entry.target.id === 'skills-section' && !barsAnimated) {
        barsAnimated = true;
        setTimeout(animateBars, 200);
      }
    });
  }, { threshold: 0.15 });

  document.querySelectorAll('.fade-up').forEach(el => observer.observe(el));

  // ── Kick off terminal on load ─────────────────────────────────────────────
  window.addEventListener('DOMContentLoaded', () => {
    setTimeout(runTerminal, 200);
  });
</script>
