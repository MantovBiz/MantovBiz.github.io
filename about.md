---
layout: default
title: "About"
permalink: /about/
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Sans:ital,wght@0,300;0,400;0,500;1,300&display=swap');

  :root {
    --ink: #1a1a1a;
    --muted: #888;
    --border: #e8e8e8;
    --accent: #c0392b;
    --accent-blue: #2563a8;
    --bg: #fafaf8;
    --card-bg: #ffffff;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  .about-page {
    font-family: 'DM Sans', sans-serif;
    color: var(--ink);
    background: var(--bg);
    min-height: 100vh;
    padding: clamp(1.5rem, 3vw, 3rem) clamp(1rem, 4vw, 3rem) 6rem;
    width: 100%;
  }

  .about-back {
    display: inline-flex;
    align-items: center;
    gap: 0.35rem;
    font-size: 0.78rem;
    color: var(--muted);
    text-decoration: none;
    font-weight: 300;
    letter-spacing: 0.02em;
    margin-bottom: 2rem;
    transition: color 0.15s;
  }
  .about-back:hover { color: var(--ink); }

  /* ── 3-zone fluid grid ──────────────────────────────────────────────────
     Left sidebar | Main content | Right panel
     clamp() lets each column breathe on wide screens and shrink on small ones.
  ─────────────────────────────────────────────────────────────────────── */
  .about-grid {
    display: grid;
    grid-template-columns:
      clamp(150px, 17vw, 250px)
      1fr
      clamp(170px, 19vw, 280px);
    grid-template-areas: "sidebar main panel";
    gap: clamp(1.5rem, 3vw, 3rem);
    align-items: start;
    width: 100%;
  }

  /* ── Left sidebar ──────────────────────────────────────────────────────── */
  .about-sidebar {
    grid-area: sidebar;
    position: sticky;
    top: 2rem;
  }

  .avatar {
    width: clamp(68px, 7vw, 92px);
    height: clamp(68px, 7vw, 92px);
    border-radius: 50%;
    background: var(--card-bg);
    border: 1px solid var(--border);
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'DM Serif Display', serif;
    font-size: clamp(1.2rem, 1.8vw, 1.6rem);
    color: var(--accent);
    margin-bottom: 1rem;
    letter-spacing: -1px;
    transition: border-color 0.2s;
  }
  .avatar:hover { border-color: #bbb; }

  .sidebar-name {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(1rem, 1.4vw, 1.25rem);
    letter-spacing: -0.01em;
    line-height: 1.2;
    margin-bottom: 0.25rem;
  }

  .sidebar-role {
    font-size: 0.76rem;
    color: var(--muted);
    font-weight: 300;
    line-height: 1.65;
    margin-bottom: 1.25rem;
  }

  .sidebar-divider {
    border: none;
    border-top: 1px solid var(--border);
    margin: 0.9rem 0;
  }

  .sidebar-meta-label {
    font-size: 0.6rem;
    text-transform: uppercase;
    letter-spacing: 0.12em;
    font-weight: 500;
    color: var(--muted);
    margin-bottom: 0.18rem;
  }

  .sidebar-meta-val {
    font-size: 0.78rem;
    color: var(--ink);
    font-weight: 300;
    margin-bottom: 0.8rem;
    display: flex;
    align-items: center;
    gap: 0.35rem;
  }

  .status-dot {
    width: 6px;
    height: 6px;
    border-radius: 50%;
    background: #27ae60;
    flex-shrink: 0;
    animation: pulse-dot 2.5s ease-in-out infinite;
  }

  @keyframes pulse-dot {
    0%, 100% { opacity: 1; }
    50%       { opacity: 0.3; }
  }

  .sidebar-nav-label {
    font-size: 0.6rem;
    text-transform: uppercase;
    letter-spacing: 0.12em;
    font-weight: 500;
    color: var(--muted);
    margin-bottom: 0.45rem;
  }

  .sidebar-nav { list-style: none; margin-bottom: 1rem; }

  .sidebar-nav li a {
    display: block;
    font-size: 0.78rem;
    color: var(--muted);
    text-decoration: none;
    padding: 0.28rem 0;
    border-bottom: 1px solid var(--border);
    font-weight: 300;
    transition: color 0.15s, padding-left 0.15s;
  }
  .sidebar-nav li:last-child a { border-bottom: none; }
  .sidebar-nav li a:hover { color: var(--ink); padding-left: 0.3rem; }

  .sidebar-links { display: flex; flex-direction: column; gap: 0.4rem; }

  .sidebar-link {
    font-size: 0.75rem;
    color: var(--accent-blue);
    text-decoration: none;
    transition: opacity 0.15s;
  }
  .sidebar-link:hover { opacity: 0.65; }

  /* ── Main content ──────────────────────────────────────────────────────── */
  .about-main {
    grid-area: main;
    min-width: 0;
  }

  .page-eyebrow {
    font-size: 0.66rem;
    text-transform: uppercase;
    letter-spacing: 0.13em;
    font-weight: 500;
    color: var(--accent);
    margin-bottom: 0.45rem;
  }

  .page-title {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(1.9rem, 3.5vw, 2.9rem);
    letter-spacing: -0.02em;
    line-height: 1.08;
    margin-bottom: 0.75rem;
  }

  .page-bio {
    font-size: clamp(0.88rem, 1.1vw, 1rem);
    color: #555;
    font-weight: 300;
    line-height: 1.85;
    margin-bottom: 2rem;
    padding-bottom: 2rem;
    border-bottom: 1px solid var(--border);
  }

  /* ── Stat cards ────────────────────────────────────────────────────────── */
  .stats-row {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 0.7rem;
    margin-bottom: 2.5rem;
  }

  .stat-card {
    background: var(--card-bg);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 0.85rem 1rem;
    opacity: 0;
    transform: translateY(8px);
    transition: opacity 0.4s ease, transform 0.4s ease, border-color 0.15s;
  }
  .stat-card.visible { opacity: 1; transform: translateY(0); }
  .stat-card:hover { border-color: #bbb; }

  .stat-number {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(1.4rem, 2.2vw, 1.9rem);
    letter-spacing: -0.03em;
    line-height: 1;
    margin-bottom: 0.2rem;
  }

  .stat-label {
    font-size: 0.64rem;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    font-weight: 500;
    color: var(--muted);
  }

  /* ── Section label ─────────────────────────────────────────────────────── */
  .section-label {
    font-size: 0.65rem;
    text-transform: uppercase;
    letter-spacing: 0.12em;
    font-weight: 500;
    color: var(--muted);
    margin-bottom: 1.1rem;
    padding-bottom: 0.55rem;
    border-bottom: 1px solid var(--border);
  }

  .about-section {
    margin-bottom: 2.5rem;
    opacity: 0;
    transform: translateY(14px);
    transition: opacity 0.5s ease, transform 0.5s ease;
  }
  .about-section.visible { opacity: 1; transform: translateY(0); }

  /* ── Why body ──────────────────────────────────────────────────────────── */
  .why-body {
    font-size: clamp(0.87rem, 1.05vw, 0.97rem);
    line-height: 1.88;
    font-weight: 300;
    color: #444;
  }
  .why-body p { margin-bottom: 1rem; }
  .why-body p:last-child { margin-bottom: 0; }

  /* ── Currently strip ───────────────────────────────────────────────────── */
  .now-strip {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 0.65rem;
  }

  .now-card {
    background: var(--card-bg);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 0.8rem 1rem;
    display: flex;
    flex-direction: column;
    gap: 0.18rem;
    transition: border-color 0.15s, transform 0.15s;
  }
  .now-card:hover { border-color: #bbb; transform: translateY(-1px); }

  .now-card-label {
    font-size: 0.59rem;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    font-weight: 500;
    color: var(--accent);
  }

  .now-card-title {
    font-size: 0.86rem;
    font-weight: 400;
    color: var(--ink);
    line-height: 1.4;
  }

  .now-card-sub {
    font-size: 0.72rem;
    color: var(--muted);
    font-weight: 300;
  }

  /* ── Tools grid ────────────────────────────────────────────────────────── */
  .tools-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 0.65rem;
  }

  .tool-card {
    background: var(--card-bg);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 0.78rem 0.95rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 0.45rem;
    width: clamp(74px, 8.5vw, 92px);
    opacity: 0;
    transform: translateY(8px);
    transition: opacity 0.4s ease, transform 0.4s ease, border-color 0.15s, box-shadow 0.15s;
  }
  .tool-card.visible { opacity: 1; transform: translateY(0); }
  .tool-card:hover { border-color: #bbb; transform: translateY(-2px); box-shadow: 0 4px 12px rgba(0,0,0,0.06); }

  .tool-logo { width: 28px; height: 28px; object-fit: contain; display: block; }

  .tool-name {
    font-size: 0.61rem;
    text-transform: uppercase;
    letter-spacing: 0.08em;
    font-weight: 500;
    color: var(--muted);
    text-align: center;
  }

  /* ── Interests ─────────────────────────────────────────────────────────── */
  .interests-wrap {
    display: flex;
    flex-wrap: wrap;
    gap: 0.42rem;
    margin-bottom: 0.8rem;
  }

  .interest-tag {
    font-size: 0.75rem;
    padding: 0.28rem 0.72rem;
    border: 1px solid var(--border);
    border-radius: 2px;
    background: var(--card-bg);
    color: var(--muted);
    cursor: pointer;
    transition: all 0.15s;
    font-weight: 300;
    user-select: none;
  }
  .interest-tag:hover, .interest-tag.active {
    background: var(--ink);
    color: #fff;
    border-color: var(--ink);
  }

  .interest-tip {
    min-height: 1.4rem;
    font-size: 0.79rem;
    color: var(--accent);
    font-style: italic;
    font-weight: 300;
  }

  /* ── CTA ───────────────────────────────────────────────────────────────── */
  .cta-row {
    display: flex;
    gap: 0.65rem;
    flex-wrap: wrap;
    padding-top: 2rem;
    border-top: 1px solid var(--border);
  }

  .btn {
    font-family: 'DM Sans', sans-serif;
    font-size: 0.8rem;
    font-weight: 400;
    text-decoration: none;
    padding: 0.5rem 1rem;
    border-radius: 2px;
    transition: all 0.15s;
    letter-spacing: 0.02em;
  }
  .btn-primary  { background: var(--ink); color: #fff; border: 1px solid var(--ink); }
  .btn-primary:hover  { background: #333; }
  .btn-secondary { background: transparent; color: var(--ink); border: 1px solid var(--border); }
  .btn-secondary:hover { border-color: var(--ink); }

  /* ── Right panel ───────────────────────────────────────────────────────── */
  .about-panel {
    grid-area: panel;
    position: sticky;
    top: 2rem;
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }

  .panel-card {
    background: var(--card-bg);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 1rem 1.1rem;
  }

  .panel-card-label {
    font-size: 0.6rem;
    text-transform: uppercase;
    letter-spacing: 0.12em;
    font-weight: 500;
    color: var(--muted);
    margin-bottom: 0.85rem;
    padding-bottom: 0.5rem;
    border-bottom: 1px solid var(--border);
  }

  /* Goals timeline */
  .goal-list { list-style: none; display: flex; flex-direction: column; gap: 0.6rem; }

  .goal-item {
    display: flex;
    align-items: flex-start;
    gap: 0.6rem;
    font-size: 0.79rem;
    font-weight: 300;
    color: #444;
    line-height: 1.5;
  }

  .goal-dot {
    width: 7px;
    height: 7px;
    border-radius: 50%;
    background: var(--border);
    flex-shrink: 0;
    margin-top: 0.38rem;
  }
  .goal-dot.done { background: #27ae60; }
  .goal-dot.now  { background: var(--accent); }
  .goal-dot.next { background: var(--border); border: 1px solid #bbb; }

  .goal-label {
    font-size: 0.58rem;
    text-transform: uppercase;
    letter-spacing: 0.08em;
    font-weight: 500;
    color: var(--muted);
    margin-top: 0.05rem;
  }

  /* Favorites */
  .fav-list { display: flex; flex-direction: column; gap: 0; }

  .fav-row {
    display: flex;
    justify-content: space-between;
    align-items: baseline;
    padding: 0.45rem 0;
    border-bottom: 1px solid var(--border);
  }
  .fav-row:last-child { border-bottom: none; }

  .fav-category {
    font-size: 0.6rem;
    text-transform: uppercase;
    letter-spacing: 0.08em;
    font-weight: 500;
    color: var(--muted);
    flex-shrink: 0;
  }

  .fav-value {
    font-size: 0.76rem;
    font-weight: 300;
    color: var(--ink);
    text-align: right;
    max-width: 58%;
    line-height: 1.3;
  }

  /* Fun facts */
  .fun-fact-text {
    font-size: 0.81rem;
    font-weight: 300;
    color: #444;
    line-height: 1.7;
    min-height: 3.8rem;
    transition: opacity 0.3s ease;
  }

  .fun-fact-controls {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-top: 0.8rem;
  }

  .fun-fact-dots { display: flex; gap: 4px; }

  .fun-fact-dot {
    width: 5px;
    height: 5px;
    border-radius: 50%;
    background: var(--border);
    transition: background 0.2s;
    cursor: pointer;
  }
  .fun-fact-dot.active { background: var(--ink); }

  .fun-fact-btn {
    font-size: 0.68rem;
    color: var(--muted);
    cursor: pointer;
    background: none;
    border: none;
    font-family: 'DM Sans', sans-serif;
    padding: 0;
    transition: color 0.15s;
  }
  .fun-fact-btn:hover { color: var(--ink); }

  /* ── Tablet: right panel moves below, sidebar stays ─────────────────────
     Breakpoint chosen so the 3-col layout doesn't get too cramped
  ─────────────────────────────────────────────────────────────────────── */
  @media (max-width: 900px) {
    .about-grid {
      grid-template-columns: clamp(140px, 21vw, 195px) 1fr;
      grid-template-areas:
        "sidebar main"
        "panel   panel";
      gap: clamp(1rem, 2.5vw, 1.75rem);
    }

    .about-panel {
      position: static;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 0.75rem;
    }
  }

  /* ── Mobile: single column ──────────────────────────────────────────────── */
  @media (max-width: 580px) {
    .about-page { padding: 1.5rem 1rem 4rem; }

    .about-grid {
      grid-template-columns: 1fr;
      grid-template-areas:
        "sidebar"
        "main"
        "panel";
      gap: 1.25rem;
    }

    /* Sidebar becomes a compact inline header strip */
    .about-sidebar {
      position: static;
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      gap: 0.85rem;
      padding-bottom: 1.25rem;
      border-bottom: 1px solid var(--border);
    }

    .avatar { width: 58px; height: 58px; font-size: 1.1rem; margin-bottom: 0; }
    .sidebar-name { font-size: 1rem; }
    .sidebar-role { margin-bottom: 0; }

    /* Hide nav/meta/links — covered by CTA row at bottom */
    .sidebar-divider,
    .sidebar-meta-label,
    .sidebar-meta-val,
    .sidebar-nav-label,
    .sidebar-nav,
    .sidebar-links { display: none; }

    .about-panel { position: static; }
    .stats-row   { grid-template-columns: repeat(2, 1fr); }
    .now-strip   { grid-template-columns: 1fr; }
    .tool-card   { width: 74px; }
  }
</style>

<div class="about-page">

  <a href="/" class="about-back">← Home</a>

  <div class="about-grid">

    <!-- ── Left sidebar ────────────────────────────────────────────────── -->
    <aside class="about-sidebar">
      <div class="avatar">MT</div>
      <div class="sidebar-name">Manuel Tovar</div>
      <div class="sidebar-role">MIS &amp; Business Analytics<br>DePaul University</div>

      <hr class="sidebar-divider">

      <div class="sidebar-meta-label">Location</div>
      <div class="sidebar-meta-val">Chicago, IL</div>

      <div class="sidebar-meta-label">Status</div>
      <div class="sidebar-meta-val"><span class="status-dot"></span>Open to internships</div>

      <div class="sidebar-meta-label">Minor</div>
      <div class="sidebar-meta-val">Sports Communication</div>

      <div class="sidebar-meta-label">Favorite club</div>
      <div class="sidebar-meta-val">Manchester United</div>

      <hr class="sidebar-divider">

      <div class="sidebar-nav-label">On this page</div>
      <ul class="sidebar-nav">
        <li><a href="#why-section">Why I study this</a></li>
        <li><a href="#now-section">Currently</a></li>
        <li><a href="#tools-section">Tools &amp; skills</a></li>
        <li><a href="#interests-section">Interests</a></li>
      </ul>

      <hr class="sidebar-divider">

      <div class="sidebar-links">
        <a href="https://www.linkedin.com/in/mantovbiz/" target="_blank" rel="noopener" class="sidebar-link">LinkedIn →</a>
        <a href="/projects/" class="sidebar-link">View projects →</a>
        <a href="/articles/" class="sidebar-link">Read articles →</a>
        <a href="/contact/" class="sidebar-link">Get in touch →</a>
      </div>
    </aside>

    <!-- ── Main content ─────────────────────────────────────────────────── -->
    <main class="about-main">

      <div class="page-eyebrow">About</div>
      <h1 class="page-title">Manuel Tovar</h1>
      <p class="page-bio">MIS &amp; Business Analytics student at DePaul University. I write about data, sports, film, and whatever else is worth thinking about — and build projects around the things I find interesting.</p>

      <div class="stats-row" id="stats-row">
        <div class="stat-card"><div class="stat-number">5</div><div class="stat-label">Tools</div></div>
        <div class="stat-card"><div class="stat-number">2</div><div class="stat-label">Degrees</div></div>
        <div class="stat-card"><div class="stat-number">8+</div><div class="stat-label">Interests</div></div>
        <div class="stat-card"><div class="stat-number">∞</div><div class="stat-label">Curiosity</div></div>
      </div>

      <div class="about-section" id="why-section">
        <div class="section-label">Why I study what I study</div>
        <div class="why-body">
          <p>Ever since I was a kid, I loved watching sports and seeing the stats behind the game. Soccer is my passion — seeing the amount of possession, passes completed vs attempted, heatmaps, and many other visuals is all so interesting to me, which is why I wanted to learn more about it.</p>
          <p>This is why I decided to study Business Analytics, because it would give me the fundamentals of analyzing data. I also love stories, whether it is reading or watching, which is why I decided to get a Sports Communication minor. Pairing those together would help me get to where I want to be.</p>
          <p>Now here I am, writing whatever I find in my research or just want to talk about and share with others. Feel free to check out my projects and the articles that I have written. Thank you for taking the time to check out some of my work!</p>
        </div>
      </div>

      <div class="about-section" id="now-section">
        <div class="section-label">Currently</div>
        <div class="now-strip">
          <div class="now-card">
            <div class="now-card-label">Reading</div>
            <div class="now-card-title">Project Hail Mary</div>
            <div class="now-card-sub">Andy Weir · Sci-Fi</div>
          </div>
          <div class="now-card">
            <div class="now-card-label">Watching</div>
            <div class="now-card-title">Speed Racer</div>
            <div class="now-card-sub">All-time favorite rewatch</div>
          </div>
          <div class="now-card">
            <div class="now-card-label">Listening to</div>
            <div class="now-card-title">Bad Bunny</div>
            <div class="now-card-sub">Nadie Sabe Lo Que Va a Pasar Mañana</div>
          </div>
          <div class="now-card">
            <div class="now-card-label">Playing</div>
            <div class="now-card-title">The Last of Us</div>
            <div class="now-card-sub">PS4 · Single player</div>
          </div>
        </div>
      </div>

      <div class="about-section" id="tools-section">
        <div class="section-label">Tools &amp; skills</div>
        <div class="tools-grid" id="tools-grid">
          <div class="tool-card">
            <img class="tool-logo" src="https://upload.wikimedia.org/wikipedia/commons/c/cf/New_Power_BI_Logo.svg" alt="Power BI" />
            <span class="tool-name">Power BI</span>
          </div>
          <div class="tool-card">
            <img class="tool-logo" src="https://upload.wikimedia.org/wikipedia/commons/4/4b/Tableau_Logo.png" alt="Tableau" />
            <span class="tool-name">Tableau</span>
          </div>
          <div class="tool-card">
            <img class="tool-logo" src="https://upload.wikimedia.org/wikipedia/commons/3/34/Microsoft_Office_Excel_%282019%E2%80%93present%29.svg" alt="Excel" />
            <span class="tool-name">Excel</span>
          </div>
          <div class="tool-card">
            <img class="tool-logo" src="https://upload.wikimedia.org/wikipedia/commons/1/1b/R_logo.svg" alt="R" />
            <span class="tool-name">R</span>
          </div>
          <div class="tool-card">
            <img class="tool-logo" src="https://upload.wikimedia.org/wikipedia/commons/8/87/Sql_data_base_with_logo.png" alt="SQL" />
            <span class="tool-name">SQL</span>
          </div>
        </div>
      </div>

      <div class="about-section" id="interests-section">
        <div class="section-label">Interests</div>
        <div class="interests-wrap">
          <span class="interest-tag" data-tip="The nerdy stuff — analyzing data behind the game is almost as fun as watching it.">Sports analytics</span>
          <span class="interest-tag" data-tip="Visuals tell a story with a little. Possession maps, heatmaps, pass networks — I love them all.">Data visualization</span>
          <span class="interest-tag" data-tip="Movies move me. My favorite film is Speed Racer. Find me on Letterboxd: Mantov09">Film &amp; cinema</span>
          <span class="interest-tag" data-tip="Bad Bunny, Kendrick Lamar, Dave — probably my top 3.">Music</span>
          <span class="interest-tag" data-tip="Sci-Fi and Greek Mythology. Favorites: Percy Jackson, Project Hail Mary, Michael Vey.">Books</span>
          <span class="interest-tag" data-tip="Single player is my lane. The Last of Us, Dispatch, Spider-Man PS4 are some of my favs.">Video games</span>
          <span class="interest-tag" data-tip="Few things beat playing a game with people you enjoy spending time with.">Board games</span>
          <span class="interest-tag" data-tip="Manchester United supporter. Also Cubs, Bears, Blackhawks.">Sports</span>
        </div>
        <div class="interest-tip" id="interest-tip"></div>
      </div>

      <div class="cta-row about-section" id="cta-section">
        <a href="/articles/" class="btn btn-primary">Read articles</a>
        <a href="/projects/" class="btn btn-secondary">View projects</a>
        <a href="/contact/" class="btn btn-secondary">Get in touch →</a>
        <a href="https://www.linkedin.com/in/mantovbiz/" target="_blank" rel="noopener" class="btn btn-secondary">LinkedIn →</a>
      </div>

    </main>

    <!-- ── Right panel ───────────────────────────────────────────────────── -->
    <aside class="about-panel">

      <div class="panel-card">
        <div class="panel-card-label">Goals &amp; roadmap</div>
        <ul class="goal-list">
          <li class="goal-item">
            <span class="goal-dot done"></span>
            <div><div class="goal-label">Done</div>Declared Business Analytics + Sports Comm minor</div>
          </li>
          <li class="goal-item">
            <span class="goal-dot done"></span>
            <div><div class="goal-label">Done</div>Built this blog &amp; launched first projects</div>
          </li>
          <li class="goal-item">
            <span class="goal-dot now"></span>
            <div><div class="goal-label">Now</div>Deepening SQL, R, and data viz skills</div>
          </li>
          <li class="goal-item">
            <span class="goal-dot next"></span>
            <div><div class="goal-label">Next</div>Land a sports analytics or data internship</div>
          </li>
          <li class="goal-item">
            <span class="goal-dot next"></span>
            <div><div class="goal-label">Future</div>Work at the intersection of sports &amp; data storytelling</div>
          </li>
        </ul>
      </div>

      <div class="panel-card">
        <div class="panel-card-label">Quick favorites</div>
        <div class="fav-list">
          <div class="fav-row"><span class="fav-category">Film</span><span class="fav-value">Speed Racer</span></div>
          <div class="fav-row"><span class="fav-category">Book</span><span class="fav-value">Project Hail Mary</span></div>
          <div class="fav-row"><span class="fav-category">Artist</span><span class="fav-value">Bad Bunny</span></div>
          <div class="fav-row"><span class="fav-category">Game</span><span class="fav-value">The Last of Us</span></div>
          <div class="fav-row"><span class="fav-category">Club</span><span class="fav-value">Manchester United</span></div>
          <div class="fav-row"><span class="fav-category">Letterboxd</span><span class="fav-value">Mantov09</span></div>
        </div>
      </div>

      <div class="panel-card">
        <div class="panel-card-label">Fun facts</div>
        <div class="fun-fact-text" id="fun-fact-text"></div>
        <div class="fun-fact-controls">
          <div class="fun-fact-dots" id="fun-fact-dots"></div>
          <button class="fun-fact-btn" id="fun-fact-next">Next →</button>
        </div>
      </div>

    </aside>

  </div>
</div>

<script>
  /* Smooth scroll */
  document.querySelectorAll('.sidebar-nav a[href^="#"]').forEach(link => {
    link.addEventListener('click', e => {
      e.preventDefault();
      const t = document.querySelector(link.getAttribute('href'));
      if (t) t.scrollIntoView({ behavior: 'smooth', block: 'start' });
    });
  });

  /* Fade up sections */
  const fadeObs = new IntersectionObserver(entries => {
    entries.forEach(e => { if (e.isIntersecting) e.target.classList.add('visible'); });
  }, { threshold: 0.08 });
  document.querySelectorAll('.about-section').forEach(el => fadeObs.observe(el));

  /* Stat cards stagger */
  const statCards = document.querySelectorAll('.stat-card');
  const statObs = new IntersectionObserver(entries => {
    entries.forEach(entry => {
      if (!entry.isIntersecting) return;
      statCards.forEach((c, i) => setTimeout(() => c.classList.add('visible'), i * 80));
      statObs.disconnect();
    });
  }, { threshold: 0.1 });
  const statsRow = document.getElementById('stats-row');
  if (statsRow) statObs.observe(statsRow);

  /* Tool cards stagger */
  const toolCards = document.querySelectorAll('.tool-card');
  const toolObs = new IntersectionObserver(entries => {
    entries.forEach(entry => {
      if (!entry.isIntersecting) return;
      toolCards.forEach((c, i) => setTimeout(() => c.classList.add('visible'), i * 90));
      toolObs.disconnect();
    });
  }, { threshold: 0.1 });
  const toolSection = document.getElementById('tools-section');
  if (toolSection) toolObs.observe(toolSection);

  /* Interest tag tooltips */
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

  /* Fun facts cycler */
  const facts = [
    "I can watch Speed Racer an unlimited number of times and still feel something every single time.",
    "I track every film I watch on Letterboxd. Find me at Mantov09.",
    "Soccer data changed how I watch the game — I can't watch a match without mentally noting possession and pressing patterns.",
    "Percy Jackson got me into Greek mythology before it was cool again.",
    "I genuinely believe The Last of Us has one of the best stories ever written, in any medium.",
    "Bad Bunny, Kendrick, and Dave is a playlist I could run on loop for a full week.",
    "I want to work where sports meets data storytelling — telling the story behind the numbers."
  ];

  let factIndex = 0;
  const factText = document.getElementById('fun-fact-text');
  const factDots = document.getElementById('fun-fact-dots');
  const factNext = document.getElementById('fun-fact-next');

  function buildDots() {
    factDots.innerHTML = '';
    facts.forEach((_, i) => {
      const d = document.createElement('span');
      d.className = 'fun-fact-dot' + (i === factIndex ? ' active' : '');
      d.addEventListener('click', () => showFact(i));
      factDots.appendChild(d);
    });
  }

  function showFact(idx) {
    factText.style.opacity = '0';
    setTimeout(() => {
      factIndex = (idx + facts.length) % facts.length;
      factText.textContent = facts[factIndex];
      factText.style.opacity = '1';
      buildDots();
    }, 250);
  }

  factText.textContent = facts[0];
  buildDots();
  factNext.addEventListener('click', () => showFact(factIndex + 1));
  setInterval(() => showFact(factIndex + 1), 6000);
</script>
