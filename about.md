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
    --tag-bg: #f0f0ee;
    --card-bg: #ffffff;
    --sidebar-width: 220px;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  .about-page {
    font-family: 'DM Sans', sans-serif;
    color: var(--ink);
    background: var(--bg);
    min-height: 100vh;
    padding: 3rem 1.5rem 6rem;
  }

  .about-inner {
    max-width: 1080px;
    margin: 0 auto;
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
    margin-bottom: 2.5rem;
    transition: color 0.15s;
  }
  .about-back:hover { color: var(--ink); }

  /* ── Two-column layout ─────────────────────────────────────────────────── */
  .about-layout {
    display: grid;
    grid-template-columns: var(--sidebar-width) 1fr;
    gap: 3.5rem;
    align-items: start;
  }

  /* ── Sidebar ───────────────────────────────────────────────────────────── */
  .about-sidebar {
    position: sticky;
    top: 2rem;
  }

  .avatar {
    width: 88px;
    height: 88px;
    border-radius: 50%;
    background: var(--card-bg);
    border: 1px solid var(--border);
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'DM Serif Display', serif;
    font-size: 1.6rem;
    font-weight: 400;
    color: var(--accent);
    margin-bottom: 1rem;
    letter-spacing: -1px;
    transition: border-color 0.2s;
  }
  .avatar:hover { border-color: #bbb; }

  /*
    To swap in a real photo:
    Replace <div class="avatar">MT</div> with:
    <img src="/assets/images/profile.jpg" class="avatar" style="object-fit:cover;" alt="Manuel Tovar">
  */

  .sidebar-name {
    font-family: 'DM Serif Display', serif;
    font-size: 1.25rem;
    font-weight: 400;
    letter-spacing: -0.01em;
    line-height: 1.2;
    margin-bottom: 0.25rem;
  }

  .sidebar-role {
    font-size: 0.78rem;
    color: var(--muted);
    font-weight: 300;
    line-height: 1.6;
    margin-bottom: 1.25rem;
  }

  .sidebar-divider {
    border: none;
    border-top: 1px solid var(--border);
    margin: 1rem 0;
  }

  .sidebar-meta-label {
    font-size: 0.62rem;
    text-transform: uppercase;
    letter-spacing: 0.12em;
    font-weight: 500;
    color: var(--muted);
    margin-bottom: 0.2rem;
  }

  .sidebar-meta-val {
    font-size: 0.8rem;
    color: var(--ink);
    font-weight: 300;
    margin-bottom: 0.85rem;
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
    50% { opacity: 0.35; }
  }

  .sidebar-nav-label {
    font-size: 0.62rem;
    text-transform: uppercase;
    letter-spacing: 0.12em;
    font-weight: 500;
    color: var(--muted);
    margin-bottom: 0.5rem;
  }

  .sidebar-nav {
    list-style: none;
    margin-bottom: 1rem;
  }

  .sidebar-nav li a {
    display: block;
    font-size: 0.8rem;
    color: var(--muted);
    text-decoration: none;
    padding: 0.3rem 0;
    border-bottom: 1px solid var(--border);
    font-weight: 300;
    transition: color 0.15s, padding-left 0.15s;
  }
  .sidebar-nav li:last-child a { border-bottom: none; }
  .sidebar-nav li a:hover { color: var(--ink); padding-left: 0.3rem; }

  .sidebar-links {
    display: flex;
    flex-direction: column;
    gap: 0.4rem;
  }

  .sidebar-link {
    font-size: 0.78rem;
    color: var(--accent-blue);
    text-decoration: none;
    font-weight: 400;
    transition: opacity 0.15s;
  }
  .sidebar-link:hover { opacity: 0.7; }

  /* ── Main content ──────────────────────────────────────────────────────── */
  .about-main { min-width: 0; }

  .page-eyebrow {
    font-size: 0.68rem;
    text-transform: uppercase;
    letter-spacing: 0.12em;
    font-weight: 500;
    color: var(--accent);
    margin-bottom: 0.5rem;
  }

  .page-title {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(2rem, 4vw, 2.75rem);
    font-weight: 400;
    letter-spacing: -0.02em;
    line-height: 1.1;
    margin-bottom: 0.75rem;
  }

  .page-bio {
    font-size: 1rem;
    color: #555;
    font-weight: 300;
    line-height: 1.8;
    max-width: 580px;
    margin-bottom: 2rem;
    padding-bottom: 2rem;
    border-bottom: 1px solid var(--border);
  }

  /* ── Stat cards ────────────────────────────────────────────────────────── */
  .stats-row {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 0.75rem;
    margin-bottom: 2.5rem;
  }

  .stat-card {
    background: var(--card-bg);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 0.9rem 1rem;
    opacity: 0;
    transform: translateY(8px);
    transition: opacity 0.4s ease, transform 0.4s ease, border-color 0.15s;
  }
  .stat-card.visible { opacity: 1; transform: translateY(0); }
  .stat-card:hover { border-color: #bbb; }

  .stat-number {
    font-family: 'DM Serif Display', serif;
    font-size: 1.75rem;
    font-weight: 400;
    letter-spacing: -0.03em;
    color: var(--ink);
    line-height: 1;
    margin-bottom: 0.25rem;
  }

  .stat-label {
    font-size: 0.68rem;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    font-weight: 500;
    color: var(--muted);
  }

  /* ── Section label ─────────────────────────────────────────────────────── */
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

  .about-section {
    margin-bottom: 2.75rem;
    opacity: 0;
    transform: translateY(14px);
    transition: opacity 0.5s ease, transform 0.5s ease;
  }
  .about-section.visible { opacity: 1; transform: translateY(0); }

  /* ── Why section ───────────────────────────────────────────────────────── */
  .why-body {
    font-size: 0.975rem;
    line-height: 1.85;
    font-weight: 300;
    color: #444;
  }
  .why-body p { margin-bottom: 1.1rem; }
  .why-body p:last-child { margin-bottom: 0; }

  /* ── Currently reading / watching strip ────────────────────────────────── */
  .now-strip {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 0.75rem;
  }

  .now-card {
    background: var(--card-bg);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 0.85rem 1rem;
    display: flex;
    flex-direction: column;
    gap: 0.2rem;
    transition: border-color 0.15s;
  }
  .now-card:hover { border-color: #bbb; }

  .now-card-label {
    font-size: 0.62rem;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    font-weight: 500;
    color: var(--accent);
  }

  .now-card-title {
    font-size: 0.88rem;
    font-weight: 400;
    color: var(--ink);
    line-height: 1.4;
  }

  .now-card-sub {
    font-size: 0.75rem;
    color: var(--muted);
    font-weight: 300;
  }

  /* ── Tools grid ────────────────────────────────────────────────────────── */
  .tools-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 0.75rem;
  }

  .tool-card {
    background: var(--card-bg);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 0.85rem 1.1rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 0.5rem;
    width: 90px;
    opacity: 0;
    transform: translateY(8px);
    transition: opacity 0.4s ease, transform 0.4s ease, border-color 0.15s, box-shadow 0.15s;
  }
  .tool-card.visible { opacity: 1; transform: translateY(0); }
  .tool-card:hover { border-color: #bbb; transform: translateY(-2px); box-shadow: 0 4px 12px rgba(0,0,0,0.06); }

  .tool-logo {
    width: 32px;
    height: 32px;
    object-fit: contain;
    display: block;
  }

  .tool-name {
    font-size: 0.65rem;
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
    gap: 0.5rem;
    margin-bottom: 0.85rem;
  }

  .interest-tag {
    font-size: 0.78rem;
    padding: 0.32rem 0.8rem;
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
    font-size: 0.82rem;
    color: var(--accent);
    font-style: italic;
    font-weight: 300;
    transition: opacity 0.2s;
  }

  /* ── CTA ───────────────────────────────────────────────────────────────── */
  .cta-row {
    display: flex;
    gap: 0.75rem;
    flex-wrap: wrap;
    padding-top: 2rem;
    border-top: 1px solid var(--border);
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
    display: inline-flex;
    align-items: center;
    gap: 0.3rem;
  }
  .btn-primary  { background: var(--ink); color: #fff; border: 1px solid var(--ink); }
  .btn-primary:hover  { background: #333; }
  .btn-secondary { background: transparent; color: var(--ink); border: 1px solid var(--border); }
  .btn-secondary:hover { border-color: var(--ink); }

  /* ── Mobile ────────────────────────────────────────────────────────────── */
  @media (max-width: 768px) {
    .about-page { padding: 2rem 1rem 4rem; }

    .about-layout {
      grid-template-columns: 1fr;
      gap: 0;
    }

    /* On mobile, show a condensed hero instead of sidebar */
    .about-sidebar {
      position: static;
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      gap: 1rem;
      padding-bottom: 1.5rem;
      margin-bottom: 1.5rem;
      border-bottom: 1px solid var(--border);
    }

    .sidebar-avatar-wrap { display: flex; align-items: center; gap: 1rem; flex: 1; min-width: 0; }

    .avatar { width: 64px; height: 64px; font-size: 1.25rem; margin-bottom: 0; flex-shrink: 0; }

    .sidebar-name { font-size: 1.15rem; }
    .sidebar-role { margin-bottom: 0; }

    /* Hide nav/meta/links in sidebar on mobile — those are in the CTA row */
    .sidebar-divider,
    .sidebar-meta-label,
    .sidebar-meta-val,
    .sidebar-nav-label,
    .sidebar-nav,
    .sidebar-links { display: none; }

    .stats-row { grid-template-columns: repeat(2, 1fr); }
    .now-strip { grid-template-columns: 1fr; }
    .tool-card { width: 80px; padding: 0.75rem 0.9rem; }
  }

  @media (max-width: 400px) {
    .stats-row { grid-template-columns: repeat(2, 1fr); }
  }
</style>

<div class="about-page">
  <div class="about-inner">

    <a href="/" class="about-back">← Home</a>

    <div class="about-layout">

      <!-- ── Sidebar ────────────────────────────────────────────────────── -->
      <aside class="about-sidebar">
        <div class="sidebar-avatar-wrap">
          <div class="avatar">MT</div>
        </div>
        <div class="sidebar-name">Manuel Tovar</div>
        <div class="sidebar-role">MIS &amp; Business Analytics<br>DePaul University</div>

        <hr class="sidebar-divider">

        <div class="sidebar-meta-label">Location</div>
        <div class="sidebar-meta-val">Chicago, IL</div>

        <div class="sidebar-meta-label">Status</div>
        <div class="sidebar-meta-val"><span class="status-dot"></span> Open to internships</div>

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

      <!-- ── Main ───────────────────────────────────────────────────────── -->
      <main class="about-main">

        <div class="page-eyebrow">About</div>
        <h1 class="page-title">Manuel Tovar</h1>
        <p class="page-bio">MIS &amp; Business Analytics student at DePaul University. I write about data, sports, film, and whatever else is worth thinking about — and build projects around the things I find interesting.</p>

        <!-- Stat cards -->
        <div class="stats-row" id="stats-row">
          <div class="stat-card">
            <div class="stat-number">5</div>
            <div class="stat-label">Tools</div>
          </div>
          <div class="stat-card">
            <div class="stat-number">2</div>
            <div class="stat-label">Degrees</div>
          </div>
          <div class="stat-card">
            <div class="stat-number">8+</div>
            <div class="stat-label">Interests</div>
          </div>
          <div class="stat-card">
            <div class="stat-number">∞</div>
            <div class="stat-label">Curiosity</div>
          </div>
        </div>

        <!-- Why I study what I study -->
        <div class="about-section" id="why-section">
          <div class="section-label">Why I study what I study</div>
          <div class="why-body">
            <p>Ever since I was a kid, I loved watching sports and seeing the stats behind the game. Soccer is my passion, and I love the game — seeing the amount of possession, passes completed vs attempted, heatmaps, and many other visuals is all so interesting to me, which is why I wanted to learn more about it.</p>
            <p>This is why I decided to study Business Analytics, because it would give me the fundamentals of analyzing data. I also love stories, whether it is reading or watching, which is why I decided to get a Sports Communication minor. Pairing those together would help me get to where I want to be.</p>
            <p>Now here I am, writing whatever I find in my research or just want to talk about and share with others. Feel free to check out my projects and the articles that I have written. Thank you for taking the time to check out some of my work!</p>
          </div>
        </div>

        <!-- Currently reading / watching -->
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

        <!-- Tools & skills -->
        <div class="about-section" id="tools-section">
          <div class="section-label">Tools &amp; skills</div>
          <div class="tools-grid" id="tools-grid">

            <div class="tool-card">
              <img class="tool-logo"
                   src="https://upload.wikimedia.org/wikipedia/commons/c/cf/New_Power_BI_Logo.svg"
                   alt="Power BI" />
              <span class="tool-name">Power BI</span>
            </div>

            <div class="tool-card">
              <img class="tool-logo"
                   src="https://upload.wikimedia.org/wikipedia/commons/4/4b/Tableau_Logo.png"
                   alt="Tableau" />
              <span class="tool-name">Tableau</span>
            </div>

            <div class="tool-card">
              <img class="tool-logo"
                   src="https://upload.wikimedia.org/wikipedia/commons/3/34/Microsoft_Office_Excel_%282019%E2%80%93present%29.svg"
                   alt="Excel" />
              <span class="tool-name">Excel</span>
            </div>

            <div class="tool-card">
              <img class="tool-logo"
                   src="https://upload.wikimedia.org/wikipedia/commons/1/1b/R_logo.svg"
                   alt="R" />
              <span class="tool-name">R</span>
            </div>

            <div class="tool-card">
              <img class="tool-logo"
                   src="https://upload.wikimedia.org/wikipedia/commons/8/87/Sql_data_base_with_logo.png"
                   alt="SQL" />
              <span class="tool-name">SQL</span>
            </div>

          </div>
        </div>

        <!-- Interests -->
        <div class="about-section" id="interests-section">
          <div class="section-label">Interests</div>
          <div class="interests-wrap">
              <span class="interest-tag" data-tip="This is the nerdy stuff that sometimes can be fun learning about the data. Not cleaning :(">Sports analytics</span> 

        <span class="interest-tag" data-tip="I love visuals because they can tell a lot with a little. A form of storytelling!">Data visualization</span> 

        <span class="interest-tag" data-tip="I love movies because of the emotions that they can make you feel. My favoire film is Speed Racer. My LeterBoxd is Mantov09">Film &amp; cinema</span> 

        <span class="interest-tag" data-tip="Bad Bunny, Kendrick Lamar, Dave are probably my top 3!.">Music</span> 

        <span class="interest-tag" data-tip="I love Sci-Fi, Greek Mythology. Some of my favorites include Percy Jackson, Project Hail Mary, Micheal Vey.">Books</span> 

        <span class="interest-tag" data-tip="I love single player video games. Some of my favs are The Last of Us, Dispatch, Spider-Man PS4">Video games</span> 

        <span class="interest-tag" data-tip="I don't think there are better moments than spending time with people you enjoy and playing a game together.">Board games</span> 

        <span class="interest-tag" data-tip="Manchester United supporter. As well as Cubs, Bears, Blackhawks">Sports</span> 
          </div>
          <div class="interest-tip" id="interest-tip"></div>
        </div>

        <!-- CTA -->
        <div class="cta-row about-section" id="cta-section">
          <a href="/articles/" class="btn btn-primary">Read articles</a>
          <a href="/projects/" class="btn btn-secondary">View projects</a>
          <a href="/contact/" class="btn btn-secondary">Get in touch →</a>
          <a href="https://www.linkedin.com/in/mantovbiz/" target="_blank" rel="noopener" class="btn btn-secondary">LinkedIn →</a>
        </div>

      </main>
    </div>
  </div>
</div>

<script>
  // ── Fade up on scroll ──────────────────────────────────────────────────────
  const fadeObserver = new IntersectionObserver(entries => {
    entries.forEach(e => { if (e.isIntersecting) e.target.classList.add('visible'); });
  }, { threshold: 0.08 });
  document.querySelectorAll('.about-section').forEach(el => fadeObserver.observe(el));

  // ── Stat cards stagger in ──────────────────────────────────────────────────
  const statCards = document.querySelectorAll('.stat-card');
  const statObserver = new IntersectionObserver(entries => {
    entries.forEach(entry => {
      if (!entry.isIntersecting) return;
      statCards.forEach((card, i) => {
        setTimeout(() => card.classList.add('visible'), i * 80);
      });
      statObserver.disconnect();
    });
  }, { threshold: 0.1 });
  const statsRow = document.getElementById('stats-row');
  if (statsRow) statObserver.observe(statsRow);

  // ── Tool logos stagger in ──────────────────────────────────────────────────
  const toolCards = document.querySelectorAll('.tool-card');
  const toolObserver = new IntersectionObserver(entries => {
    entries.forEach(entry => {
      if (!entry.isIntersecting) return;
      toolCards.forEach((card, i) => {
        setTimeout(() => card.classList.add('visible'), i * 90);
      });
      toolObserver.disconnect();
    });
  }, { threshold: 0.1 });
  const toolSection = document.getElementById('tools-section');
  if (toolSection) toolObserver.observe(toolSection);

  // ── Interest tag tooltips ──────────────────────────────────────────────────
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

  // ── Smooth scroll for sidebar nav links ───────────────────────────────────
  document.querySelectorAll('.sidebar-nav a[href^="#"]').forEach(link => {
    link.addEventListener('click', e => {
      e.preventDefault();
      const target = document.querySelector(link.getAttribute('href'));
      if (target) target.scrollIntoView({ behavior: 'smooth', block: 'start' });
    });
  });
</script>
