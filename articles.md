---
layout: default
title: "Articles"
permalink: /articles/
---

<style>
  :root {
    --ink: #1a1a1a; --muted: #888; --border: #e8e8e8;
    --accent: #c0392b; --accent-blue: #2563a8;
    --bg: #fafaf8; --tag-bg: #f0f0ee;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  .articles-page {
    font-family: 'DM Sans', sans-serif;
    color: var(--ink); background: var(--bg);
    min-height: 100vh; padding: 4rem 1.5rem 6rem;
  }

  .page-header { max-width: 720px; margin: 0 auto 2rem; padding-bottom: 2rem; border-bottom: 1px solid var(--border); }

  .page-eyebrow {
    display: flex; align-items: center; gap: 0.6rem;
    font-size: 0.65rem; text-transform: uppercase; letter-spacing: 0.14em;
    font-weight: 500; color: var(--accent); margin-bottom: 0.8rem;
  }
  .page-eyebrow::before { content: ''; display: inline-block; width: 20px; height: 1.5px; background: var(--accent); flex-shrink: 0; }

  .page-header h1 { font-family: 'DM Serif Display', serif; font-size: clamp(2rem,5vw,3rem); font-weight: 400; letter-spacing: -0.02em; margin-bottom: 0.5rem; }
  .page-header p { font-size: 0.9rem; color: var(--muted); font-weight: 300; }

  .search-wrap { max-width: 720px; margin: 0 auto 1.75rem; position: relative; }
  .search-wrap svg { position: absolute; left: 0.9rem; top: 50%; transform: translateY(-50%); color: var(--muted); pointer-events: none; }

  #search-input {
    width: 100%; padding: 0.75rem 1rem 0.75rem 2.6rem;
    font-family: 'DM Sans', sans-serif; font-size: 0.9rem; font-weight: 300;
    border: 1px solid var(--border); border-radius: 2px;
    background: #fff; color: var(--ink); outline: none; transition: border-color 0.2s;
  }
  #search-input:focus { border-color: var(--ink); }
  #search-input::placeholder { color: #bbb; }

  .tabs { max-width: 720px; margin: 0 auto 0.25rem; display: flex; border-bottom: 1px solid var(--border); }
  .tab-btn {
    font-family: 'DM Sans', sans-serif; font-size: 0.8rem; font-weight: 400;
    letter-spacing: 0.04em; text-transform: uppercase; background: none; border: none;
    border-bottom: 2px solid transparent; padding: 0.6rem 1.1rem; margin-bottom: -1px;
    cursor: pointer; color: var(--muted); transition: color 0.15s, border-color 0.15s;
  }
  .tab-btn:hover { color: var(--ink); }
  .tab-btn.active { color: var(--ink); border-bottom-color: var(--ink); }
  .tab-btn:focus-visible { outline: 2px solid var(--accent); outline-offset: 2px; border-radius: 2px; }

  #results-meta { max-width: 720px; margin: 0.75rem auto 0; font-size: 0.75rem; color: var(--muted); font-weight: 300; letter-spacing: 0.03em; min-height: 1.2em; text-transform: uppercase; }

  .posts-list { max-width: 720px; margin: 0 auto; list-style: none; }

  .post-item {
    display: flex; gap: 1rem; border-top: 1px solid var(--border);
    padding: 1.5rem 0; opacity: 0; transform: translateY(6px); animation: fadeUp 0.3s forwards;
  }
  @keyframes fadeUp { to { opacity: 1; transform: translateY(0); } }
  .post-item:last-child { border-bottom: 1px solid var(--border); }

  .card-accent { width: 3px; flex-shrink: 0; background: var(--accent); border-radius: 2px; align-self: stretch; min-height: 36px; }
  .card-accent.accent-blue { background: var(--accent-blue); }
  .card-accent.accent-muted { background: var(--border); }

  .post-content { flex: 1; min-width: 0; }

  .post-meta-row { display: flex; align-items: center; flex-wrap: wrap; gap: 0.3rem; margin-bottom: 0.4rem; }

  .post-badge { font-size: 0.62rem; text-transform: uppercase; letter-spacing: 0.1em; font-weight: 500; padding: 0.15rem 0.45rem; border-radius: 1px; }
  .badge-opinion { background: #fdecea; color: var(--accent); }
  .badge-research { background: #e8f0fb; color: var(--accent-blue); }

  .post-tag { font-size: 0.62rem; letter-spacing: 0.05em; text-transform: uppercase; font-weight: 500; background: var(--tag-bg); color: var(--muted); padding: 0.15rem 0.4rem; border-radius: 1px; }

  .post-title a { font-family: 'DM Serif Display', serif; font-size: 1.15rem; font-weight: 400; color: var(--ink); text-decoration: none; letter-spacing: -0.01em; line-height: 1.3; display: block; transition: color 0.15s; }
  .post-title a:hover { color: var(--accent); }

  .post-excerpt { font-size: 0.875rem; color: #666; margin-top: 0.4rem; line-height: 1.65; font-weight: 300; }

  .post-footer-row { display: flex; gap: 0.75rem; align-items: center; margin-top: 0.55rem; flex-wrap: wrap; }
  .post-date { font-size: 0.72rem; color: var(--muted); font-weight: 300; }
  .post-read-time { font-size: 0.72rem; color: var(--muted); font-weight: 300; }
  .post-read-time::before { content: '· '; color: var(--border); }

  mark { background: #fff3b0; color: inherit; padding: 0 1px; border-radius: 1px; }

  .empty-state { padding: 2.5rem 0; color: var(--muted); font-size: 0.9rem; font-style: italic; font-weight: 300; border-top: 1px solid var(--border); }

  @media (max-width: 480px) { .post-footer-row { flex-direction: column; gap: 0.2rem; } }
</style>

<script>
var allPosts = [
  {% for post in site.posts %}
  {
    "title":      {{ post.title      | jsonify }},
    "url":        {{ post.url        | jsonify }},
    "date":       {{ post.date | date: "%b %d, %Y" | jsonify }},
    "categories": {{ post.categories | jsonify }},
    "tags":       {{ post.tags       | jsonify }},
    "excerpt":    {{ post.excerpt | strip_html | truncatewords: 28 | jsonify }},
    "words":      {{ post.content | number_of_words }}
  }{% unless forloop.last %},{% endunless %}
  {% endfor %}
];
</script>

<div class="articles-page">
  <div class="page-header">
    <div class="page-eyebrow">Writing</div>
    <h1>Articles</h1>
    <p>Research, analysis, and opinion — on anything worth writing about.</p>
  </div>

  <div class="search-wrap">
    <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true">
      <circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/>
    </svg>
    <input type="text" id="search-input" placeholder="Search articles…" autocomplete="off" spellcheck="false" maxlength="120" aria-label="Search articles"/>
  </div>

  <div class="tabs" role="tablist" aria-label="Filter by category">
    <button class="tab-btn active" data-tab="all"      role="tab" aria-selected="true">All</button>
    <button class="tab-btn"        data-tab="opinion"  role="tab" aria-selected="false">Opinion</button>
    <button class="tab-btn"        data-tab="research" role="tab" aria-selected="false">Research</button>
  </div>

  <div id="results-meta" aria-live="polite"></div>
  <ul class="posts-list" id="posts-list" aria-label="Article list"></ul>
</div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/lunr.js/2.3.9/lunr.min.js"></script>
<script>
(function () {
  var idx = lunr(function () {
    this.ref('url');
    this.field('title',      { boost: 10 });
    this.field('tags',       { boost: 5  });
    this.field('categories', { boost: 3  });
    this.field('excerpt');
    allPosts.forEach(function (p) {
      this.add({ url: p.url, title: p.title, tags: (p.tags||[]).join(' '), categories: (p.categories||[]).join(' '), excerpt: p.excerpt });
    }, this);
  });

  function highlightNode(el, terms) {
    if (!el || !terms.length) return;
    if (!el.dataset.orig) el.dataset.orig = el.textContent;
    var text = el.dataset.orig;
    var safeParts = terms.map(function(t){ return t.replace(/[^a-zA-Z0-9]/g,'').toLowerCase(); }).filter(Boolean);
    if (!safeParts.length) { el.textContent = text; return; }
    var re = new RegExp('('+safeParts.join('|')+')','gi');
    while (el.firstChild) el.removeChild(el.firstChild);
    text.split(re).forEach(function(chunk){
      if (re.test(chunk)) { var m=document.createElement('mark'); m.textContent=chunk; el.appendChild(m); re.lastIndex=0; }
      else el.appendChild(document.createTextNode(chunk));
    });
  }

  var currentTab='all', currentQuery='';
  var input=document.getElementById('search-input');
  var list=document.getElementById('posts-list');
  var meta=document.getElementById('results-meta');

  document.querySelectorAll('.tab-btn').forEach(function(btn){
    btn.addEventListener('click', function(){
      document.querySelectorAll('.tab-btn').forEach(function(b){ b.classList.remove('active'); b.setAttribute('aria-selected','false'); });
      btn.classList.add('active'); btn.setAttribute('aria-selected','true');
      currentTab=btn.dataset.tab; render();
    });
  });

  input.addEventListener('input', function(){ currentQuery=this.value.trim(); render(); });

  function render(){
    list.innerHTML=''; meta.textContent='';
    var filtered=allPosts.slice();
    if (currentTab!=='all') filtered=filtered.filter(function(p){ return (p.categories||[]).indexOf(currentTab)>-1; });
    var terms=[];
    if (currentQuery.length>=2){
      try {
        var results=idx.search(currentQuery+'*');
        var urls=results.map(function(r){return r.ref;});
        filtered=filtered.filter(function(p){return urls.indexOf(p.url)>-1;});
        terms=currentQuery.split(/\s+/).filter(Boolean);
      } catch(e){ filtered=[]; }
      meta.textContent=filtered.length+' result'+(filtered.length!==1?'s':'')+' for "'+currentQuery+'"';
    }
    if (filtered.length===0){
      var li=document.createElement('li'); var p=document.createElement('p');
      p.className='empty-state'; p.textContent=currentQuery?'No articles found for "'+currentQuery+'".':'No articles found.';
      li.appendChild(p); list.appendChild(li); return;
    }
    filtered.forEach(function(post,i){
      var cats=post.categories||[];
      var isOpinion=cats.indexOf('opinion')>-1;
      var isResearch=cats.indexOf('research')>-1;
      var rt=post.words?Math.max(1,Math.floor(post.words/200)):null;
      var li=document.createElement('li'); li.className='post-item'; li.style.animationDelay=(i*0.05)+'s';
      var accent=document.createElement('div');
      accent.className='card-accent'+(isResearch?' accent-blue':isOpinion?'':' accent-muted');
      li.appendChild(accent);
      var content=document.createElement('div'); content.className='post-content';
      var metaRow=document.createElement('div'); metaRow.className='post-meta-row';
      if (isOpinion||isResearch){
        var badge=document.createElement('span');
        badge.className='post-badge '+(isOpinion?'badge-opinion':'badge-research');
        badge.textContent=isOpinion?'Opinion':'Research'; metaRow.appendChild(badge);
      }
      (post.tags||[]).forEach(function(t){ var tag=document.createElement('span'); tag.className='post-tag'; tag.textContent=t; metaRow.appendChild(tag); });
      content.appendChild(metaRow);
      var titleDiv=document.createElement('div'); titleDiv.className='post-title';
      var a=document.createElement('a'); a.href=post.url; a.textContent=post.title;
      titleDiv.appendChild(a); content.appendChild(titleDiv);
      if (post.excerpt){ var exc=document.createElement('p'); exc.className='post-excerpt'; exc.textContent=post.excerpt; content.appendChild(exc); highlightNode(exc,terms); }
      var footerRow=document.createElement('div'); footerRow.className='post-footer-row';
      var dateEl=document.createElement('span'); dateEl.className='post-date'; dateEl.textContent=post.date; footerRow.appendChild(dateEl);
      if (rt){ var rtEl=document.createElement('span'); rtEl.className='post-read-time'; rtEl.textContent=rt+' min read'; footerRow.appendChild(rtEl); }
      content.appendChild(footerRow);
      highlightNode(a,terms); li.appendChild(content); list.appendChild(li);
    });
  }
  render();
})();
</script>
