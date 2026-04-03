---
layout: default
title: "Home"
permalink: /
---

<style>
  :root {
    --ink:         #1a1a1a;
    --muted:       #888;
    --border:      #e8e8e8;
    --accent:      #c0392b;
    --accent-blue: #2563a8;
    --bg:          #fafaf8;
    --tag-bg:      #f0f0ee;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  .home-page {
    font-family: 'DM Sans', sans-serif;
    color: var(--ink);
    background: var(--bg);
    min-height: 100vh;
  }

  .home-inner {
    max-width: 720px;
    margin: 0 auto;
    padding: 0 clamp(1rem, 3vw, 2rem);
  }

  .hero {
    padding: 4.5rem 0 3.5rem;
    border-bottom: 1px solid var(--border);
  }

  .hero-eyebrow {
    display: flex;
    align-items: center;
    gap: 0.7rem;
    font-size: 0.68rem;
    text-transform: uppercase;
    letter-spacing: 0.14em;
    font-weight: 500;
    color: var(--accent);
    margin-bottom: 1.1rem;
  }

  .hero-eyebrow::before {
    content: '';
    display: inline-block;
    width: 22px;
    height: 1.5px;
    background: var(--accent);
    flex-shrink: 0;
  }

  .hero h1 {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(2.6rem, 7vw, 4rem);
    font-weight: 400;
    letter-spacing: -0.03em;
    line-height: 1.06;
    margin-bottom: 1.25rem;
    color: var(--ink);
  }

  .hero h1 em { font-style: italic; color: var(--accent); }

  .hero-sub {
    font-size: 1rem;
    color: #555;
    font-weight: 300;
    line-height: 1.8;
    max-width: 540px;
    margin-bottom: 2rem;
  }

  .hero-cta { display: flex; gap: 0.75rem; flex-wrap: wrap; }

  .btn {
    font-family: 'DM Sans', sans-serif;
    font-size: 0.82rem;
    font-weight: 400;
    text-decoration: none;
    padding: 0.65rem 1.3rem;
    border-radius: 2px;
    transition: all 0.15s;
    letter-spacing: 0.02em;
    display: inline-block;
  }

  .btn-primary { background: var(--ink); color: #fff; border: 1px solid var(--ink); }
  .btn-primary:hover { background: #333; }
  .btn-secondary { background: transparent; color: var(--ink); border: 1px solid var(--border); }
  .btn-secondary:hover { border-color: var(--ink); }

  .home-section {
    padding: 3rem 0;
    border-bottom: 1px solid var(--border);
  }

  .home-section:last-child { border-bottom: none; }

  .section-head {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 1.5rem;
  }

  .section-label {
    font-size: 0.65rem;
    text-transform: uppercase;
    letter-spacing: 0.13em;
    font-weight: 500;
    color: var(--muted);
    display: flex;
    align-items: center;
    gap: 0.6rem;
  }

  .section-label::after {
    content: '';
    display: inline-block;
    width: 28px;
    height: 1px;
    background: var(--border);
  }

  .section-more {
    font-size: 0.75rem;
    color: var(--muted);
    text-decoration: none;
    font-weight: 300;
    transition: color 0.15s;
  }

  .section-more:hover { color: var(--ink); }

  .post-list { list-style: none; }

  .post-card {
    display: flex;
    gap: 1.1rem;
    border-top: 1px solid var(--border);
    padding: 1.5rem 0;
    opacity: 0;
    transform: translateY(8px);
    animation: fadeUp 0.35s forwards;
  }

  .post-card:last-child { border-bottom: 1px solid var(--border); }
  .post-card:nth-child(1) { animation-delay: 0.06s; }
  .post-card:nth-child(2) { animation-delay: 0.12s; }
  .post-card:nth-child(3) { animation-delay: 0.18s; }

  @keyframes fadeUp { to { opacity: 1; transform: translateY(0); } }

  .post-card-accent {
    width: 3px;
    flex-shrink: 0;
    background: var(--accent);
    border-radius: 2px;
    align-self: stretch;
    min-height: 40px;
  }

  .post-card-accent.accent-blue { background: var(--accent-blue); }
  .post-card-body { flex: 1; min-width: 0; }

  .post-meta-row {
    display: flex;
    align-items: center;
    flex-wrap: wrap;
    gap: 0.3rem;
    margin-bottom: 0.4rem;
  }

  .post-badge {
    font-size: 0.62rem;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    font-weight: 500;
    padding: 0.15rem 0.45rem;
    border-radius: 1px;
    display: inline-block;
  }

  .badge-opinion  { background: #fdecea; color: var(--accent); }
  .badge-research { background: #e8f0fb; color: var(--accent-blue); }

  .post-tag {
    font-size: 0.62rem;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    font-weight: 500;
    background: var(--tag-bg);
    color: var(--muted);
    padding: 0.15rem 0.4rem;
    border-radius: 1px;
  }

  .post-title a {
    font-family: 'DM Serif Display', serif;
    font-size: 1.15rem;
    font-weight: 400;
    color: var(--ink);
    text-decoration: none;
    letter-spacing: -0.01em;
    line-height: 1.3;
    display: block;
    transition: color 0.15s;
  }

  .post-title a:hover { color: var(--accent); }

  .post-excerpt {
    font-size: 0.875rem;
    color: #666;
    margin-top: 0.35rem;
    line-height: 1.65;
    font-weight: 300;
  }

  .post-footer-row {
    display: flex;
    gap: 1rem;
    align-items: center;
    margin-top: 0.6rem;
  }

  .post-date { font-size: 0.72rem; color: var(--muted); font-weight: 300; }
  .post-read-time { font-size: 0.72rem; color: var(--muted); font-weight: 300; }

  .proj-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1rem;
  }

  .proj-mini {
    display: block;
    text-decoration: none;
    background: #fff;
    border: 1px solid var(--border);
    border-radius: 3px;
    padding: 1.25rem 1.1rem;
    transition: border-color 0.15s, box-shadow 0.15s;
  }

  .proj-mini:hover { border-color: #bbb; box-shadow: 0 3px 12px rgba(0,0,0,0.06); }

  .proj-tools {
    font-size: 0.65rem;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    font-weight: 500;
    color: var(--muted);
    margin-bottom: 0.5rem;
  }

  .proj-mini-title {
    font-family: 'DM Serif Display', serif;
    font-size: 0.95rem;
    font-weight: 400;
    color: var(--ink);
    line-height: 1.35;
    letter-spacing: -0.01em;
  }

  .about-strip {
    background: #fff;
    border: 1px solid var(--border);
    border-radius: 3px;
    padding: 1.75rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 1.5rem;
    flex-wrap: wrap;
  }

  .about-strip h2 {
    font-family: 'DM Serif Display', serif;
    font-size: 1.1rem;
    font-weight: 400;
    letter-spacing: -0.01em;
    margin-bottom: 0.3rem;
  }

  .about-strip p { font-size: 0.875rem; color: var(--muted); font-weight: 300; line-height: 1.6; }

  @media (max-width: 520px) {
    .proj-grid { grid-template-columns: 1fr; }
    .about-strip { flex-direction: column; align-items: flex-start; }
    .post-footer-row { flex-direction: column; gap: 0.2rem; }
    .hero { padding: 3rem 0 2.5rem; }
  }
</style>

<div class="home-page">

  <section class="hero" aria-label="Introduction">
    <div class="home-inner">
      <div class="hero-eyebrow">Portfolio</div>
      <h1>Analytics, innovation,<br>and <em>design.</em></h1>
      <p class="hero-sub">
        Exploring the intersection of analytics, innovation, and design.
      </p>
      <div class="hero-cta">
        <a href="/articles/" class="btn btn-primary">Read Articles</a>
        <a href="/projects/" class="btn btn-secondary">View Projects</a>
      </div>
    </div>
  </section>

  <section class="home-section" aria-label="Recent articles">
    <div class="home-inner">
      <div class="section-head">
        <span class="section-label">Recent Writing</span>
        <a href="/articles/" class="section-more">View all →</a>
      </div>
      <ul class="post-list">
        {% for post in site.posts limit:3 %}
        <li class="post-card">
          <div class="post-card-accent{% if post.categories contains 'research' %} accent-blue{% endif %}"></div>
          <div class="post-card-body">
            <div class="post-meta-row">
              {% assign cats = post.categories %}
              {% if cats contains 'opinion' %}
                <span class="post-badge badge-opinion">Opinion</span>
              {% elsif cats contains 'research' %}
                <span class="post-badge badge-research">Research</span>
              {% endif %}
              {% for tag in post.tags %}
                <span class="post-tag">{{ tag }}</span>
              {% endfor %}
            </div>
            <div class="post-title"><a href="{{ post.url }}">{{ post.title }}</a></div>
            {% if post.excerpt %}
            <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 22 }}</p>
            {% endif %}
            <div class="post-footer-row">
              <span class="post-date">{{ post.date | date: "%b %d, %Y" }}</span>
              <span class="post-read-time">
                {% assign wc = post.content | number_of_words %}
                {% assign rt = wc | divided_by: 200 %}
                {% if rt < 1 %}1{% else %}{{ rt }}{% endif %} min read
              </span>
            </div>
          </div>
        </li>
        {% endfor %}
      </ul>
    </div>
  </section>

  <section class="home-section" aria-label="Recent projects">
    <div class="home-inner">
      <div class="section-head">
        <span class="section-label">Recent Work</span>
        <a href="/projects/" class="section-more">View all →</a>
      </div>
      <div class="proj-grid">
        <a href="https://github.com/MantovBiz/NFL-fast-R-Data-Visualizations-and-Breakdowns/tree/main/Chicago-Bears/2025"
           target="_blank" rel="noopener" class="proj-mini">
          <div class="proj-tools">R · nflfastR · ggplot2</div>
          <div class="proj-mini-title">Chicago Bears 2025 — Data Visualizations &amp; Breakdowns</div>
        </a>
      </div>
    </div>
  </section>

  <section class="home-section" aria-label="About">
    <div class="home-inner">
      <div class="about-strip">
        <div>
          <h2>Manuel Tovar</h2>
          <p>MIS &amp; Business Analytics · DePaul University<br>
             I study data because I've always wanted to understand the story behind the numbers.</p>
        </div>
        <a href="/about/" class="btn btn-secondary">About me →</a>
      </div>
    </div>
  </section>

</div>
