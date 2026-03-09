---
layout: default
title: "Home"
permalink: /
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

  .home-page {
    font-family: 'DM Sans', sans-serif;
    color: var(--ink);
    background: var(--bg);
    min-height: 100vh;
    padding: 4rem 1.5rem 6rem;
  }

  .home-inner { max-width: 680px; margin: 0 auto; }

  /* Hero */
  .hero {
    padding-bottom: 3rem;
    border-bottom: 1px solid var(--border);
    margin-bottom: 3rem;
  }

  .hero-label {
    font-size: 0.7rem;
    text-transform: uppercase;
    letter-spacing: 0.14em;
    font-weight: 500;
    color: var(--accent);
    margin-bottom: 1rem;
  }

  .hero h1 {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(2.4rem, 6vw, 3.75rem);
    font-weight: 400;
    letter-spacing: -0.03em;
    line-height: 1.08;
    margin-bottom: 1.25rem;
  }

  .hero h1 em { font-style: italic; color: var(--accent); }

  .hero p {
    font-size: 1rem;
    color: #555;
    font-weight: 300;
    line-height: 1.75;
    max-width: 520px;
    margin-bottom: 2rem;
  }

  .hero-cta { display: flex; gap: 0.75rem; flex-wrap: wrap; }

  .btn {
    font-family: 'DM Sans', sans-serif;
    font-size: 0.82rem;
    font-weight: 400;
    text-decoration: none;
    padding: 0.6rem 1.2rem;
    border-radius: 2px;
    transition: all 0.15s;
    letter-spacing: 0.02em;
  }

  .btn-primary { background: var(--ink); color: #fff; border: 1px solid var(--ink); }
  .btn-primary:hover { background: #333; }
  .btn-secondary { background: transparent; color: var(--ink); border: 1px solid var(--border); }
  .btn-secondary:hover { border-color: var(--ink); }

  /* Recent posts */
  .section-head {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 0.25rem;
  }

  .section-label {
    font-size: 0.7rem;
    text-transform: uppercase;
    letter-spacing: 0.12em;
    font-weight: 500;
    color: var(--muted);
  }

  .section-more {
    font-size: 0.75rem;
    color: var(--muted);
    text-decoration: none;
    font-weight: 300;
    transition: color 0.15s;
  }

  .section-more:hover { color: var(--ink); }

  .post-list { list-style: none; margin-bottom: 3rem; }

  .post-item {
    border-top: 1px solid var(--border);
    padding: 1.4rem 0;
    display: grid;
    grid-template-columns: 1fr auto;
    gap: 1rem;
    align-items: start;
    opacity: 0;
    transform: translateY(6px);
    animation: fadeUp 0.3s forwards;
  }

  .post-item:nth-child(1) { animation-delay: 0.08s; }
  .post-item:nth-child(2) { animation-delay: 0.14s; }
  .post-item:nth-child(3) { animation-delay: 0.20s; }
  @keyframes fadeUp { to { opacity: 1; transform: translateY(0); } }
  .post-item:last-child { border-bottom: 1px solid var(--border); }

  .post-badge {
    font-size: 0.65rem;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    font-weight: 500;
    padding: 0.15rem 0.45rem;
    border-radius: 1px;
    margin-bottom: 0.4rem;
    display: inline-block;
  }

  .badge-opinion  { background: #fdecea; color: #c0392b; }
  .badge-research { background: #e8f0fb; color: #2563a8; }

  .post-title a {
    font-family: 'DM Serif Display', serif;
    font-size: 1.15rem;
    font-weight: 400;
    color: var(--ink);
    text-decoration: none;
    letter-spacing: -0.01em;
    line-height: 1.3;
    transition: color 0.15s;
    display: block;
  }

  .post-title a:hover { color: var(--accent); }

  .post-excerpt {
    font-size: 0.875rem;
    color: #666;
    margin-top: 0.35rem;
    line-height: 1.65;
    font-weight: 300;
  }

  .post-date {
    font-size: 0.72rem;
    color: var(--muted);
    font-weight: 300;
    white-space: nowrap;
    padding-top: 0.2rem;
  }

  /* About strip */
  .about-strip {
    border: 1px solid var(--border);
    border-radius: 2px;
    padding: 1.75rem;
    background: #fff;
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 1.5rem;
    flex-wrap: wrap;
  }

  .about-strip h2 {
    font-family: 'DM Serif Display', serif;
    font-size: 1.15rem;
    font-weight: 400;
    margin-bottom: 0.3rem;
    letter-spacing: -0.01em;
  }

  .about-strip p {
    font-size: 0.875rem;
    color: var(--muted);
    font-weight: 300;
    line-height: 1.5;
  }

  @media (max-width: 480px) {
    .post-item { grid-template-columns: 1fr; }
    .post-date { padding-top: 0; }
    .about-strip { flex-direction: column; align-items: flex-start; }
  }
</style>

<div class="home-page">
  <div class="home-inner">

    <div class="hero">
      <div class="hero-label">Mantov's Portfolio</div>
      <h1>Writing, research,<br>and <em>curiosity.</em></h1>
      <p>A space for analytics, projects, and opinions — from sports and data to film and culture. By Manuel Tovar, MIS & Business Analytics student at DePaul University.</p>
      <div class="hero-cta">
        <a href="/articles/" class="btn btn-primary">Read Articles</a>
        <a href="/projects/" class="btn btn-secondary">View Projects</a>
      </div>
    </div>

    <div class="section-head">
      <span class="section-label">Recent Articles</span>
      <a href="/articles/" class="section-more">View all →</a>
    </div>

    <ul class="post-list">
      {% for post in site.posts limit:3 %}
      <li class="post-item">
        <div>
          {% assign cats = post.categories %}
          {% if cats contains 'opinion' %}
            <span class="post-badge badge-opinion">Opinion</span>
          {% elsif cats contains 'research' %}
            <span class="post-badge badge-research">Research</span>
          {% endif %}
          <div class="post-title"><a href="{{ post.url }}">{{ post.title }}</a></div>
          {% if post.excerpt %}
          <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 20 }}</p>
          {% endif %}
        </div>
        <div class="post-date">{{ post.date | date: "%b %d, %Y" }}</div>
      </li>
      {% endfor %}
    </ul>

    <div class="about-strip">
      <div>
        <h2>Manuel Tovar</h2>
        <p>MIS & Business Analytics · DePaul University<br>R, Python, SQL, Tableau</p>
      </div>
      <a href="/about/" class="btn btn-secondary">About me →</a>
    </div>

  </div>
</div>
