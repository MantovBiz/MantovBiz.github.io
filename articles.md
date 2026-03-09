---
layout: default
title: "Articles"
permalink: /articles/
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Sans:wght@300;400;500&display=swap');

  :root {
    --ink: #1a1a1a;
    --muted: #888;
    --border: #e8e8e8;
    --accent-red: #c0392b;
    --accent-blue: #2563a8;
    --bg: #fafaf8;
    --tag-bg: #f0f0ee;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  .articles-page {
    font-family: 'DM Sans', sans-serif;
    color: var(--ink);
    background: var(--bg);
    min-height: 100vh;
    padding: 4rem 1.5rem;
  }

  .page-header {
    max-width: 680px;
    margin: 0 auto 3rem;
    padding-bottom: 2rem;
    border-bottom: 1px solid var(--border);
  }

  .page-header h1 {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(2rem, 5vw, 3rem);
    font-weight: 400;
    letter-spacing: -0.02em;
    margin-bottom: 0.6rem;
  }

  .page-header p {
    font-size: 0.9rem;
    color: var(--muted);
    font-weight: 300;
    line-height: 1.6;
  }

  /* Nav pills */
  .nav-pills {
    max-width: 680px;
    margin: 0 auto 2.5rem;
    display: flex;
    gap: 0.5rem;
    flex-wrap: wrap;
  }

  .nav-pills a {
    font-size: 0.8rem;
    font-weight: 400;
    text-decoration: none;
    padding: 0.35rem 0.85rem;
    border: 1px solid var(--border);
    border-radius: 2px;
    color: var(--muted);
    transition: all 0.15s;
    letter-spacing: 0.02em;
  }

  .nav-pills a:hover { border-color: var(--ink); color: var(--ink); }
  .nav-pills a.active { border-color: var(--ink); background: var(--ink); color: #fff; }

  .nav-pills .search-link {
    margin-left: auto;
    display: flex;
    align-items: center;
    gap: 0.3rem;
  }

  /* Section headers */
  .section-head {
    max-width: 680px;
    margin: 2.5rem auto 0.5rem;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .section-label {
    font-size: 0.7rem;
    text-transform: uppercase;
    letter-spacing: 0.12em;
    font-weight: 500;
  }

  .section-label.opinion { color: var(--accent-red); }
  .section-label.research { color: var(--accent-blue); }

  .section-more {
    font-size: 0.75rem;
    color: var(--muted);
    text-decoration: none;
    font-weight: 300;
    transition: color 0.15s;
  }

  .section-more:hover { color: var(--ink); }

  /* Posts list */
  .posts-list {
    max-width: 680px;
    margin: 0 auto;
    list-style: none;
  }

  .post-item {
    border-top: 1px solid var(--border);
    padding: 1.5rem 0;
    display: grid;
    grid-template-columns: 1fr auto;
    gap: 1rem;
    opacity: 0;
    transform: translateY(6px);
    animation: fadeUp 0.3s forwards;
  }

  @keyframes fadeUp { to { opacity: 1; transform: translateY(0); } }

  .post-item:nth-child(1) { animation-delay: 0.05s; }
  .post-item:nth-child(2) { animation-delay: 0.1s; }
  .post-item:nth-child(3) { animation-delay: 0.15s; }
  .post-item:nth-child(4) { animation-delay: 0.2s; }
  .post-item:nth-child(5) { animation-delay: 0.25s; }

  .post-item:last-child { border-bottom: 1px solid var(--border); }

  .post-content { min-width: 0; }

  .post-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 0.3rem;
    margin-bottom: 0.4rem;
  }

  .post-tag {
    font-size: 0.68rem;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    font-weight: 500;
    background: var(--tag-bg);
    color: var(--muted);
    padding: 0.15rem 0.45rem;
    border-radius: 1px;
  }

  .post-title a {
    font-family: 'DM Serif Display', serif;
    font-size: 1.2rem;
    font-weight: 400;
    color: var(--ink);
    text-decoration: none;
    letter-spacing: -0.01em;
    line-height: 1.3;
    transition: color 0.15s;
  }

  .post-title a:hover { color: var(--accent-red); }

  .post-excerpt {
    font-size: 0.875rem;
    color: #666;
    margin-top: 0.4rem;
    line-height: 1.65;
    font-weight: 300;
  }

  .post-date {
    font-size: 0.75rem;
    color: var(--muted);
    font-weight: 300;
    white-space: nowrap;
    padding-top: 0.2rem;
  }

  @media (max-width: 480px) {
    .post-item { grid-template-columns: 1fr; }
    .post-date { padding-top: 0; }
    .nav-pills .search-link { margin-left: 0; }
  }
</style>

<div class="articles-page">

  <div class="page-header">
    <h1>Articles</h1>
    <p>Sports analytics writing — research, data analysis, and opinion.</p>
  </div>

  <nav class="nav-pills">
    <a href="/articles/" class="active">All</a>
    <a href="/opinion/">Opinion</a>
    <a href="/research/">Research</a>
    <a href="/search/" class="search-link">
      <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5">
        <circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/>
      </svg>
      Search
    </a>
  </nav>

  <!-- OPINION SECTION -->
  {% assign opinion_posts = site.categories.opinion %}
  {% if opinion_posts.size > 0 %}
  <div class="section-head">
    <span class="section-label opinion">Opinion</span>
    <a href="/opinion/" class="section-more">View all →</a>
  </div>
  <ul class="posts-list">
    {% for post in opinion_posts limit:3 %}
    <li class="post-item">
      <div class="post-content">
        {% if post.tags and post.tags.size > 0 %}
        <div class="post-tags">
          {% for tag in post.tags %}<span class="post-tag">{{ tag }}</span>{% endfor %}
        </div>
        {% endif %}
        <div class="post-title"><a href="{{ post.url }}">{{ post.title }}</a></div>
        {% if post.excerpt %}<p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 20 }}</p>{% endif %}
      </div>
      <div class="post-date">{{ post.date | date: "%b %d, %Y" }}</div>
    </li>
    {% endfor %}
  </ul>
  {% endif %}

  <!-- RESEARCH SECTION -->
  {% assign research_posts = site.categories.research %}
  {% if research_posts.size > 0 %}
  <div class="section-head">
    <span class="section-label research">Research</span>
    <a href="/research/" class="section-more">View all →</a>
  </div>
  <ul class="posts-list">
    {% for post in research_posts limit:3 %}
    <li class="post-item">
      <div class="post-content">
        {% if post.tags and post.tags.size > 0 %}
        <div class="post-tags">
          {% for tag in post.tags %}<span class="post-tag">{{ tag }}</span>{% endfor %}
        </div>
        {% endif %}
        <div class="post-title"><a href="{{ post.url }}">{{ post.title }}</a></div>
        {% if post.excerpt %}<p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 20 }}</p>{% endif %}
      </div>
      <div class="post-date">{{ post.date | date: "%b %d, %Y" }}</div>
    </li>
    {% endfor %}
  </ul>
  {% endif %}

  <!-- FALLBACK: show all posts if no categories assigned yet -->
  {% if opinion_posts.size == 0 and research_posts.size == 0 %}
  <ul class="posts-list">
    {% for post in site.posts %}
    <li class="post-item">
      <div class="post-content">
        {% if post.tags and post.tags.size > 0 %}
        <div class="post-tags">
          {% for tag in post.tags %}<span class="post-tag">{{ tag }}</span>{% endfor %}
        </div>
        {% endif %}
        <div class="post-title"><a href="{{ post.url }}">{{ post.title }}</a></div>
        {% if post.excerpt %}<p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 20 }}</p>{% endif %}
      </div>
      <div class="post-date">{{ post.date | date: "%b %d, %Y" }}</div>
    </li>
    {% endfor %}
  </ul>
  {% endif %}

</div>
