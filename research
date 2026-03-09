---
layout: default
title: "Research"
permalink: /research/
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Sans:wght@300;400;500&display=swap');

  :root {
    --ink: #1a1a1a;
    --muted: #888;
    --border: #e8e8e8;
    --accent: #2563a8;
    --bg: #fafaf8;
    --tag-bg: #f0f0ee;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  .category-page {
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
    margin-bottom: 0.6rem;
    line-height: 1.1;
  }

  .page-header p {
    font-size: 0.9rem;
    color: var(--muted);
    font-weight: 300;
    line-height: 1.6;
  }

  .nav-pills {
    max-width: 680px;
    margin: 0 auto 2.5rem;
    display: flex;
    gap: 0.5rem;
    flex-wrap: wrap;
  }

  .nav-pills a {
    font-family: 'DM Sans', sans-serif;
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

  .posts-list {
    max-width: 680px;
    margin: 0 auto;
    list-style: none;
  }

  .post-item {
    border-top: 1px solid var(--border);
    padding: 1.75rem 0;
    display: grid;
    grid-template-columns: 1fr auto;
    gap: 1rem;
    align-start: start;
    opacity: 0;
    transform: translateY(8px);
    animation: fadeUp 0.35s forwards;
  }

  @keyframes fadeUp {
    to { opacity: 1; transform: translateY(0); }
  }

  {% for post in site.categories.research %}
  .post-item:nth-child({{ forloop.index }}) { animation-delay: {{ forloop.index | times: 0.06 }}s; }
  {% endfor %}

  .post-item:last-child { border-bottom: 1px solid var(--border); }

  .post-content { min-width: 0; }

  .post-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 0.3rem;
    margin-bottom: 0.5rem;
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
    font-size: 1.3rem;
    font-weight: 400;
    color: var(--ink);
    text-decoration: none;
    letter-spacing: -0.01em;
    line-height: 1.3;
    transition: color 0.15s;
  }

  .post-title a:hover { color: var(--accent); }

  .post-excerpt {
    font-size: 0.875rem;
    color: #666;
    margin-top: 0.5rem;
    line-height: 1.65;
    font-weight: 300;
  }

  .post-date {
    font-size: 0.75rem;
    color: var(--muted);
    font-weight: 300;
    white-space: nowrap;
    padding-top: 0.2rem;
    letter-spacing: 0.01em;
  }

  .empty-state {
    padding: 3rem 0;
    color: var(--muted);
    font-size: 0.95rem;
    font-style: italic;
    font-weight: 300;
  }

  @media (max-width: 480px) {
    .post-item { grid-template-columns: 1fr; }
    .post-date { padding-top: 0; }
  }
</style>

<div class="category-page">
  <div class="page-header">
    <div class="page-label">Category</div>
    <h1>Research</h1>
    <p>Data-driven analysis, methodology breakdowns, and deep dives into sports analytics.</p>
  </div>

  <nav class="nav-pills">
    <a href="/articles/">All</a>
    <a href="/opinion/">Opinion</a>
    <a href="/research/" class="active">Research</a>
    <a href="/search/">Search</a>
  </nav>

  <ul class="posts-list">
    {% assign research_posts = site.categories.research %}
    {% if research_posts.size > 0 %}
      {% for post in research_posts %}
      <li class="post-item">
        <div class="post-content">
          {% if post.tags and post.tags.size > 0 %}
          <div class="post-tags">
            {% for tag in post.tags %}
            <span class="post-tag">{{ tag }}</span>
            {% endfor %}
          </div>
          {% endif %}
          <div class="post-title">
            <a href="{{ post.url }}">{{ post.title }}</a>
          </div>
          {% if post.excerpt %}
          <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 25 }}</p>
          {% endif %}
        </div>
        <div class="post-date">{{ post.date | date: "%b %d, %Y" }}</div>
      </li>
      {% endfor %}
    {% else %}
      <li><p class="empty-state">No research articles yet. Check back soon.</p></li>
    {% endif %}
  </ul>
</div>
