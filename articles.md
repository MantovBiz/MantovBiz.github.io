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
    --accent: #c0392b;
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
    padding: 4rem 1.5rem 6rem;
  }

  .page-header {
    max-width: 680px;
    margin: 0 auto 2rem;
    padding-bottom: 2rem;
    border-bottom: 1px solid var(--border);
  }

  .page-header h1 {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(2rem, 5vw, 3rem);
    font-weight: 400;
    letter-spacing: -0.02em;
    margin-bottom: 0.5rem;
  }

  .page-header p { font-size: 0.9rem; color: var(--muted); font-weight: 300; }

  .search-wrap {
    max-width: 680px;
    margin: 0 auto 1.75rem;
    position: relative;
  }

  .search-wrap svg {
    position: absolute;
    left: 0.9rem;
    top: 50%;
    transform: translateY(-50%);
    color: var(--muted);
    pointer-events: none;
  }

  #search-input {
    width: 100%;
    padding: 0.75rem 1rem 0.75rem 2.6rem;
    font-family: 'DM Sans', sans-serif;
    font-size: 0.9rem;
    font-weight: 300;
    border: 1px solid var(--border);
    border-radius: 2px;
    background: #fff;
    color: var(--ink);
    outline: none;
    transition: border-color 0.2s;
  }

  #search-input:focus { border-color: var(--ink); }
  #search-input::placeholder { color: #bbb; }

  .tabs {
    max-width: 680px;
    margin: 0 auto 0.25rem;
    display: flex;
    border-bottom: 1px solid var(--border);
  }

  .tab-btn {
    font-family: 'DM Sans', sans-serif;
    font-size: 0.8rem;
    font-weight: 400;
    letter-spacing: 0.04em;
    text-transform: uppercase;
    background: none;
    border: none;
    border-bottom: 2px solid transparent;
    padding: 0.6rem 1.1rem;
    margin-bottom: -1px;
    cursor: pointer;
    color: var(--muted);
    transition: color 0.15s, border-color 0.15s;
  }

  .tab-btn:hover { color: var(--ink); }
  .tab-btn.active { color: var(--ink); border-bottom-color: var(--ink); }

  #results-meta {
    max-width: 680px;
    margin: 0.75rem auto 0;
    font-size: 0.75rem;
    color: var(--muted);
    font-weight: 300;
    letter-spacing: 0.03em;
    min-height: 1.2em;
    text-transform: uppercase;
  }

  .posts-list { max-width: 680px; margin: 0 auto; list-style: none; }

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
  .post-item:last-child { border-bottom: 1px solid var(--border); }

  .post-meta-row {
    display: flex;
    align-items: center;
    flex-wrap: wrap;
    gap: 0.3rem;
    margin-bottom: 0.4rem;
  }

  .post-badge {
    font-size: 0.65rem;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    font-weight: 500;
    padding: 0.15rem 0.45rem;
    border-radius: 1px;
  }

  .badge-opinion  { background: #fdecea; color: var(--accent); }
  .badge-research { background: #e8f0fb; color: var(--accent-blue); }

  .post-tag {
    font-size: 0.65rem;
    letter-spacing: 0.05em;
    text-transform: uppercase;
    font-weight: 500;
    background: var(--tag-bg);
    color: var(--muted);
    padding: 0.15rem 0.4rem;
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
    display: block;
  }

  .post-title a:hover { color: var(--accent); }

  .post-excerpt {
    font-size: 0.875rem;
    color: #666;
    margin-top: 0.4rem;
    line-height: 1.65;
    font-weight: 300;
  }

  .post-date {
    font-size: 0.72rem;
    color: var(--muted);
    font-weight: 300;
    white-space: nowrap;
    padding-top: 0.25rem;
  }

  mark { background: #fff3b0; color: inherit; padding: 0 1px; border-radius: 1px; }

  .empty-state {
    padding: 2.5rem 0;
    color: var(--muted);
    font-size: 0.9rem;
    font-style: italic;
    font-weight: 300;
    border-top: 1px solid var(--border);
  }

  @media (max-width: 480px) {
    .post-item { grid-template-columns: 1fr; }
    .post-date { padding-top: 0; }
  }
</style>

<script>
var allPosts = [
  {% for post in site.posts %}
  {
    "title": {{ post.title | jsonify }},
    "url": {{ post.url | jsonify }},
    "date": {{ post.date | date: "%b %d, %Y" | jsonify }},
    "categories": {{ post.categories | jsonify }},
    "tags": {{ post.tags | jsonify }},
    "excerpt": {{ post.excerpt | strip_html | truncatewords: 28 | jsonify }}
  }{% unless forloop.last %},{% endunless %}
  {% endfor %}
];
</script>

<div class="articles-page">
  <div class="page-header">
    <h1>Articles</h1>
    <p>Research, analysis, and opinion — on anything worth writing about.</p>
  </div>

  <div class="search-wrap">
    <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
      <circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/>
    </svg>
    <input type="text" id="search-input" placeholder="Search articles…" autocomplete="off" />
  </div>

  <div class="tabs">
    <button class="tab-btn active" data-tab="all">All</button>
    <button class="tab-btn" data-tab="opinion">Opinion</button>
    <button class="tab-btn" data-tab="research">Research</button>
  </div>

  <div id="results-meta"></div>
  <ul class="posts-list" id="posts-list"></ul>
</div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/lunr.js/2.3.9/lunr.min.js"></script>
<script>
  var idx = lunr(function () {
    this.ref('url');
    this.field('title', { boost: 10 });
    this.field('tags', { boost: 5 });
    this.field('categories', { boost: 3 });
    this.field('excerpt');
    allPosts.forEach(function(p) {
      this.add({
        url: p.url,
        title: p.title,
        tags: (p.tags || []).join(' '),
        categories: (p.categories || []).join(' '),
        excerpt: p.excerpt
      });
    }, this);
  });

  var currentTab = 'all', currentQuery = '';
  var input = document.getElementById('search-input');
  var list  = document.getElementById('posts-list');
  var meta  = document.getElementById('results-meta');

  document.querySelectorAll('.tab-btn').forEach(function(btn) {
    btn.addEventListener('click', function() {
      document.querySelectorAll('.tab-btn').forEach(function(b) { b.classList.remove('active'); });
      btn.classList.add('active');
      currentTab = btn.dataset.tab;
      render();
    });
  });

  input.addEventListener('input', function() {
    currentQuery = this.value.trim();
    render();
  });

  function highlight(text, query) {
    if (!query || !text) return text;
    var esc = query.replace(/[.*+?^${}()|[\]\\]/g, '\\$&');
    return text.replace(new RegExp('(' + esc + ')', 'gi'), '<mark>$1</mark>');
  }

  function render() {
    list.innerHTML = '';
    meta.textContent = '';

    var filtered = allPosts.slice();

    if (currentTab !== 'all') {
      filtered = filtered.filter(function(p) {
        return (p.categories || []).indexOf(currentTab) > -1;
      });
    }

    if (currentQuery.length >= 2) {
      var results = idx.search(currentQuery + '*');
      var urls = results.map(function(r) { return r.ref; });
      filtered = filtered.filter(function(p) { return urls.indexOf(p.url) > -1; });
      meta.textContent = filtered.length + ' result' + (filtered.length !== 1 ? 's' : '') + ' for "' + currentQuery + '"';
    }

    if (filtered.length === 0) {
      list.innerHTML = '<li><p class="empty-state">No articles found' + (currentQuery ? ' for "' + currentQuery + '"' : '') + '.</p></li>';
      return;
    }

    filtered.forEach(function(post, i) {
      var cats = post.categories || [];
      var isOpinion  = cats.indexOf('opinion') > -1;
      var isResearch = cats.indexOf('research') > -1;
      var badge = isOpinion
        ? '<span class="post-badge badge-opinion">Opinion</span>'
        : isResearch
          ? '<span class="post-badge badge-research">Research</span>'
          : '';
      var tags = (post.tags || []).map(function(t) {
        return '<span class="post-tag">' + t + '</span>';
      }).join('');

      var li = document.createElement('li');
      li.className = 'post-item';
      li.style.animationDelay = (i * 0.05) + 's';
      li.innerHTML =
        '<div class="post-content">' +
          '<div class="post-meta-row">' + badge + tags + '</div>' +
          '<div class="post-title"><a href="' + post.url + '">' + highlight(post.title, currentQuery) + '</a></div>' +
          (post.excerpt ? '<p class="post-excerpt">' + highlight(post.excerpt, currentQuery) + '</p>' : '') +
        '</div>' +
        '<div class="post-date">' + post.date + '</div>';
      list.appendChild(li);
    });
  }

  render();
</script>
