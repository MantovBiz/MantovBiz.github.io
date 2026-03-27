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
    --accent-blue: #2563a8;
    --bg: #fafaf8;
    --tag-bg: #f0f0ee;
    --card-bg: #ffffff;
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

  .about-section { margin-bottom: 3rem; }

  /* ── Hero ─────────────────────────────────────────────────────────────────── */
  .hero {
    display: flex;
    align-items: center;
    gap: 2.5rem;
    padding-bottom: 2.5rem;
    border-bottom: 1px solid var(--border);
    margin-bottom: 3rem;
    flex-wrap: wrap;
  }

  .avatar {
    width: 110px;
    height: 110px;
    border-radius: 50%;
    background: var(--card-bg);
    border: 1px solid var(--border);
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'DM Serif Display', serif;
    font-size: 2rem;
    font-weight: 400;
    color: var(--accent);
    flex-shrink: 0;
    letter-spacing: -1px;
  }

  /*
    To swap in a real photo later, replace the <div class="avatar"> with:
    <img src="/assets/images/profile.jpg" class="avatar-photo" alt="Manuel Tovar">

    And add this rule:
    .avatar-photo { width:110px; height:110px; border-radius:50%; object-fit:cover; border:1px solid var(--border); flex-shrink:0; }
  */

  .hero-text { flex: 1; min-width: 200px; }

  .page-label {
    font-size: 0.68rem;
    text-transform: uppercase;
    letter-spacing: 0.12em;
    font-weight: 500;
    color: var(--accent);
    margin-bottom: 0.6rem;
  }

  .hero-name {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(2rem, 5vw, 3rem);
    font-weight: 400;
    letter-spacing: -0.02em;
    line-height: 1.1;
    margin-bottom: 0.75rem;
  }

  .hero-bio {
    font-size: 1rem;
    color: #444;
    font-weight: 300;
    line-height: 1.75;
    max-width: 540px;
  }

  /* ── Why section ──────────────────────────────────────────────────────────── */
  .why-body {
    font-size: 1rem;
    line-height: 1.8;
    font-weight: 300;
    color: #444;
  }

  .why-body p { margin-bottom: 1.2rem; }
  .why-body p:last-child { margin-bottom: 0; }

  .why-placeholder {
    font-size: 0.875rem;
    color: var(--muted);
    font-style: italic;
    padding: 1.25rem;
    border: 1px dashed var(--border);
    border-radius: 3px;
    line-height: 1.7;
  }

  /* ── Tools grid ───────────────────────────────────────────────────────────── */
  .tools-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
  }

  .tool-card {
    background: var(--card-bg);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 1rem 1.25rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 0.6rem;
    width: 100px;
    opacity: 0;
    transform: translateY(8px);
    transition: opacity 0.4s ease, transform 0.4s ease, border-color 0.15s;
  }

  .tool-card.visible { opacity: 1; transform: translateY(0); }
  .tool-card:hover { border-color: #bbb; transform: translateY(-2px); }

  .tool-logo {
    width: 36px;
    height: 36px;
    object-fit: contain;
    display: block;
  }

  .tool-name {
    font-size: 0.7rem;
    text-transform: uppercase;
    letter-spacing: 0.08em;
    font-weight: 500;
    color: var(--muted);
    text-align: center;
  }

  /* ── Interests ────────────────────────────────────────────────────────────── */
  .interests-wrap {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    margin-bottom: 0.85rem;
  }

  .interest-tag {
    font-size: 0.8rem;
    padding: 0.35rem 0.85rem;
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

  .interest-tip {
    min-height: 1.4rem;
    font-size: 0.82rem;
    color: var(--accent);
    font-style: italic;
    font-weight: 300;
  }

  /* ── CTA ──────────────────────────────────────────────────────────────────── */
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
  }

  .btn-primary  { background: var(--ink); color: #fff; border: 1px solid var(--ink); }
  .btn-primary:hover  { background: #333; }
  .btn-secondary { background: transparent; color: var(--ink); border: 1px solid var(--border); }
  .btn-secondary:hover { border-color: var(--ink); }

  /* ── Fade up on scroll ────────────────────────────────────────────────────── */
  .fade-up {
    opacity: 0;
    transform: translateY(14px);
    transition: opacity 0.5s ease, transform 0.5s ease;
  }
  .fade-up.visible { opacity: 1; transform: translateY(0); }

  /* ── Mobile ───────────────────────────────────────────────────────────────── */
  @media (max-width: 600px) {
    .about-page  { padding: 2rem 1rem 4rem; }
    .hero        { gap: 1.5rem; }
    .avatar      { width: 80px; height: 80px; font-size: 1.5rem; }
    .why-body    { font-size: 0.95rem; }
    .tool-card   { width: 85px; padding: 0.85rem 1rem; }
  }
</style>

<div class="about-page">
  <div class="about-inner">

    <a href="/" class="about-back">← Home</a>

    <!-- ── Hero ───────────────────────────────────────────────────────────── -->
    <div class="hero">
      <div class="avatar">MT</div>
      <div class="hero-text">
        <div class="page-label">About</div>
        <h1 class="hero-name">Manuel Tovar</h1>
        <p class="hero-bio">MIS &amp; Business Analytics student at DePaul University. I write about data, sports, film, and whatever else is worth thinking about — and build projects around the things I find interesting.</p>
      </div>
    </div>

    <!-- ── Why I study what I study ───────────────────────────────────────── -->
    <div class="about-section fade-up" id="why-section">
      <div class="section-label">Why I study what I study</div>
      <div class="why-body">
        <div class="why-placeholder">
          Ever since I was a kid, I loved watching sports and seeing the stats behind the game. Soccer is my passion, and I love the game, so seeing the amount of possession, passes completed vs attempted, heatmaps, and many other visuals. It is all so interesting to me, which is why I wanted to learn more about it. 
          This is why I decided to study Business Analytics, because it would give me the fundamentals of analyzing data. I also love stories, whether it is reading or watching, which is why I decided to get a sports communication minor. Pairing those together would help me get to where I want to be. 
          Now here I am, writing whatever I find in my research or just want to talk about and share with others. Feel free to check out my projects and the articles that I have written. Thank you for taking the time to check out some of my work! 
          
        </div>
      </div>
    </div>

    <!-- ── Tools & skills ─────────────────────────────────────────────────── -->
    <div class="about-section fade-up" id="tools-section">
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

    <!-- ── Interests ──────────────────────────────────────────────────────── -->
    <div class="about-section fade-up" id="interests-section">
      <div class="section-label">Interests</div>
      <div class="interests-wrap">
        <span class="interest-tag" data-tip="Using R and Python to find stories hidden inside sports data.">Sports analytics</span>
        <span class="interest-tag" data-tip="ggplot2, Tableau, Power BI — making numbers mean something visually.">Data visualization</span>
        <span class="interest-tag" data-tip="Kubrick, Scorsese, and anything A24 puts out. Cinema as craft.">Film &amp; cinema</span>
        <span class="interest-tag" data-tip="Everything from jazz and soul to hip-hop. Always something playing.">Music</span>
        <span class="interest-tag" data-tip="Non-fiction mostly — data, business, and the occasional novel.">Books</span>
        <span class="interest-tag" data-tip="From RPGs to strategy games — I love systems with depth.">Video games</span>
        <span class="interest-tag" data-tip="Settlers of Catan to Wingspan — the best way to spend an evening.">Board games</span>
        <span class="interest-tag" data-tip="Die-hard Bears and Cubs fan. Sports never stops being interesting.">Sports</span>
      </div>
      <div class="interest-tip" id="interest-tip"></div>
    </div>

    <!-- ── CTA ────────────────────────────────────────────────────────────── -->
    <div class="cta-row fade-up" id="cta-section">
      <a href="/articles/" class="btn btn-primary">Read articles</a>
      <a href="/projects/" class="btn btn-secondary">View projects</a>
      <a href="/contact/" class="btn btn-secondary">Get in touch →</a>
      <a href="https://www.linkedin.com/in/mantovbiz/" target="_blank" rel="noopener" class="btn btn-secondary">LinkedIn →</a>
    </div>

  </div>
</div>

<script>
  // ── Fade up on scroll ──────────────────────────────────────────────────────
  const fadeObserver = new IntersectionObserver(entries => {
    entries.forEach(e => { if (e.isIntersecting) e.target.classList.add('visible'); });
  }, { threshold: 0.1 });
  document.querySelectorAll('.fade-up').forEach(el => fadeObserver.observe(el));

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
</script>
