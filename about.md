---
layout: default
title: "About"
permalink: /about/
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Sans:ital,wght@0,300;0,400;0,500;1,300&display=swap');

  #ab, #ab * { box-sizing: border-box; margin: 0; padding: 0; }

  #ab {
    all: initial;
    display: block;
    font-family: 'DM Sans', sans-serif;
    font-size: 15px;
    line-height: 1.6;
    color: #1a1a1a;
    background: #fafaf8;
    width: 100%;
    min-height: 100vh;
    padding: 2.5rem 1.25rem 5rem;
  }

  #ab .wrap {
    max-width: 640px;
    margin: 0 auto;
  }

  #ab .bk {
    display: inline-flex;
    align-items: center;
    gap: 0.3rem;
    font-size: 0.78rem;
    color: #888;
    text-decoration: none;
    font-weight: 300;
    letter-spacing: 0.02em;
    margin-bottom: 2rem;
  }
  #ab .bk:hover { color: #1a1a1a; }

  /* ── HEADER ── */
  #ab .hd {
    display: flex;
    align-items: center;
    gap: 1rem;
    margin-bottom: 1.5rem;
    padding-bottom: 1.5rem;
    border-bottom: 1px solid #e8e8e8;
  }

  #ab .av {
    width: 56px;
    height: 56px;
    border-radius: 50%;
    background: #fff;
    border: 1px solid #e8e8e8;
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'DM Serif Display', serif;
    font-size: 1.1rem;
    color: #c0392b;
    flex-shrink: 0;
  }

  #ab .hd-txt { flex: 1; min-width: 0; }

  #ab .hd-name {
    font-family: 'DM Serif Display', serif;
    font-size: 1.4rem;
    line-height: 1.15;
    color: #1a1a1a;
    display: block;
  }

  #ab .hd-role {
    font-size: 0.78rem;
    color: #888;
    font-weight: 300;
    display: block;
    margin-top: 0.1rem;
  }

  /* ── META ROW ── */
  #ab .meta {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem 2rem;
    margin-bottom: 1.75rem;
  }

  #ab .meta-item { display: flex; flex-direction: column; }

  #ab .ml {
    font-size: 0.56rem;
    text-transform: uppercase;
    letter-spacing: 0.12em;
    font-weight: 500;
    color: #bbb;
    margin-bottom: 0.1rem;
  }

  #ab .mv {
    font-size: 0.8rem;
    color: #1a1a1a;
    font-weight: 300;
    display: flex;
    align-items: center;
    gap: 0.3rem;
  }

  #ab .dot {
    width: 6px;
    height: 6px;
    border-radius: 50%;
    background: #27ae60;
    flex-shrink: 0;
    animation: pulse 2.5s ease-in-out infinite;
  }
  @keyframes pulse { 0%,100%{opacity:1} 50%{opacity:0.3} }

  /* ── BIO ── */
  #ab .bio {
    font-size: 0.92rem;
    color: #555;
    font-weight: 300;
    line-height: 1.85;
    margin-bottom: 2rem;
    padding-bottom: 2rem;
    border-bottom: 1px solid #e8e8e8;
    display: block;
  }

  /* ── SECTION ── */
  #ab .sec {
    margin-bottom: 2rem;
    padding-bottom: 2rem;
    border-bottom: 1px solid #e8e8e8;
    opacity: 0;
    transform: translateY(10px);
    transition: opacity 0.45s ease, transform 0.45s ease;
    display: block;
  }
  #ab .sec.on { opacity: 1; transform: translateY(0); }
  #ab .sec:last-child { border-bottom: none; }

  #ab .sc-lbl {
    font-size: 0.6rem;
    text-transform: uppercase;
    letter-spacing: 0.12em;
    font-weight: 500;
    color: #888;
    display: block;
    margin-bottom: 0.85rem;
  }

  /* ── WHY ── */
  #ab .why p {
    font-size: 0.91rem;
    line-height: 1.88;
    font-weight: 300;
    color: #444;
    margin-bottom: 0.8rem;
    display: block;
  }
  #ab .why p:last-child { margin-bottom: 0; }

  /* ── TOOLS ── */
  #ab .tools { display: flex; flex-wrap: wrap; gap: 0.5rem; }

  #ab .tool {
    background: #fff;
    border: 1px solid #e8e8e8;
    border-radius: 4px;
    padding: 0.6rem 0.75rem;
    display: flex;
    align-items: center;
    gap: 0.5rem;
    opacity: 0;
    transform: translateY(6px);
    transition: opacity 0.35s ease, transform 0.35s ease, border-color 0.15s, box-shadow 0.15s;
  }
  #ab .tool.on { opacity: 1; transform: translateY(0); }
  #ab .tool:hover { border-color: #bbb; box-shadow: 0 3px 10px rgba(0,0,0,0.05); }
  #ab .tool img { width: 20px; height: 20px; object-fit: contain; display: block; }
  #ab .tool span {
    font-size: 0.75rem;
    font-weight: 400;
    color: #555;
  }

  /* ── INTERESTS ── */
  #ab .tags { display: flex; flex-wrap: wrap; gap: 0.38rem; margin-bottom: 0.6rem; }

  #ab .tag {
    font-size: 0.73rem;
    padding: 0.24rem 0.68rem;
    border: 1px solid #e8e8e8;
    border-radius: 2px;
    background: #fff;
    color: #888;
    cursor: pointer;
    font-weight: 300;
    user-select: none;
    transition: all 0.15s;
  }
  #ab .tag:hover, #ab .tag.on { background: #1a1a1a; color: #fff; border-color: #1a1a1a; }

  #ab .tip {
    font-size: 0.76rem;
    color: #c0392b;
    font-style: italic;
    font-weight: 300;
    min-height: 1.2rem;
    display: block;
  }

  /* ── FAVORITES ── */
  #ab .favs {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(160px, 1fr));
    gap: 0;
  }

  #ab .fav {
    display: flex;
    flex-direction: column;
    padding: 0.6rem 0;
    border-bottom: 1px solid #f0f0ee;
    padding-right: 1rem;
  }

  #ab .fcat {
    font-size: 0.56rem;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    font-weight: 500;
    color: #bbb;
    margin-bottom: 0.1rem;
  }

  #ab .fval {
    font-size: 0.82rem;
    font-weight: 300;
    color: #1a1a1a;
  }

  /* ── LINKS ── */
  #ab .lks {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
  }

  #ab a.btn {
    font-family: 'DM Sans', sans-serif;
    font-size: 0.77rem;
    font-weight: 400;
    text-decoration: none;
    padding: 0.46rem 0.9rem;
    border-radius: 2px;
    transition: all 0.15s;
    letter-spacing: 0.02em;
    display: inline-block;
  }
  #ab a.btn-p { background: #1a1a1a; color: #fff; border: 1px solid #1a1a1a; }
  #ab a.btn-p:hover { background: #333; }
  #ab a.btn-s { background: transparent; color: #1a1a1a; border: 1px solid #e8e8e8; }
  #ab a.btn-s:hover { border-color: #1a1a1a; }
</style>

<div id="ab">
  <div class="wrap">

    <a href="/" class="bk">← Home</a>

    <!-- HEADER -->
    <div class="hd">
      <div class="av">MT</div>
      <div class="hd-txt">
        <span class="hd-name">Manuel Tovar</span>
        <span class="hd-role">MIS &amp; Business Analytics · DePaul University</span>
      </div>
    </div>

    <!-- META -->
    <div class="meta">
      <div class="meta-item">
        <span class="ml">Location</span>
        <span class="mv">Chicago, IL</span>
      </div>
      <div class="meta-item">
        <span class="ml">Status</span>
        <span class="mv"><span class="dot"></span>Open to internships</span>
      </div>
      <div class="meta-item">
        <span class="ml">Minor</span>
        <span class="mv">Sports Communication</span>
      </div>
      <div class="meta-item">
        <span class="ml">Favorite club</span>
        <span class="mv">Manchester United</span>
      </div>
    </div>

    <!-- BIO -->
    <span class="bio">MIS &amp; Business Analytics student at DePaul University. I write about data, sports, film, and whatever else is worth thinking about — and build projects around the things I find interesting.</span>

    <!-- WHY -->
    <div class="sec" id="s-why">
      <span class="sc-lbl">Why I study what I study</span>
      <div class="why">
        <p>Ever since I was a kid, I loved watching sports and seeing the stats behind the game. Soccer is my passion — seeing possession data, heatmaps, and pass networks captivated me early. That curiosity is what pushed me toward Business Analytics.</p>
        <p>I also love stories — reading, watching, telling them. That's why I paired my analytics degree with a Sports Communication minor. Data and storytelling together is exactly where I want to be.</p>
      </div>
    </div>

    <!-- TOOLS -->
    <div class="sec" id="s-tools">
      <span class="sc-lbl">Tools &amp; skills</span>
      <div class="tools" id="js-tools">
        <div class="tool">
          <img src="https://upload.wikimedia.org/wikipedia/commons/c/cf/New_Power_BI_Logo.svg" alt="Power BI">
          <span>Power BI</span>
        </div>
        <div class="tool">
          <img src="https://upload.wikimedia.org/wikipedia/commons/4/4b/Tableau_Logo.png" alt="Tableau">
          <span>Tableau</span>
        </div>
        <div class="tool">
          <img src="https://upload.wikimedia.org/wikipedia/commons/3/34/Microsoft_Office_Excel_%282019%E2%80%93present%29.svg" alt="Excel">
          <span>Excel</span>
        </div>
        <div class="tool">
          <img src="https://upload.wikimedia.org/wikipedia/commons/1/1b/R_logo.svg" alt="R">
          <span>R</span>
        </div>
        <div class="tool">
          <img src="https://upload.wikimedia.org/wikipedia/commons/8/87/Sql_data_base_with_logo.png" alt="SQL">
          <span>SQL</span>
        </div>
      </div>
    </div>

    <!-- INTERESTS -->
    <div class="sec" id="s-int">
      <span class="sc-lbl">Interests</span>
      <div class="tags">
        <span class="tag" data-tip="Analyzing data behind the game is almost as fun as watching it.">Sports analytics</span>
        <span class="tag" data-tip="Possession maps, heatmaps, pass networks — visuals that tell the story.">Data visualization</span>
        <span class="tag" data-tip="Favorite film: Speed Racer. Find me on Letterboxd: Mantov09">Film &amp; cinema</span>
        <span class="tag" data-tip="Bad Bunny, Kendrick Lamar, Dave — my top 3.">Music</span>
        <span class="tag" data-tip="Sci-Fi and Greek Mythology. Percy Jackson, Project Hail Mary, Michael Vey.">Books</span>
        <span class="tag" data-tip="The Last of Us, Dispatch, Spider-Man PS4.">Video games</span>
        <span class="tag" data-tip="Few things beat a good game with good people.">Board games</span>
        <span class="tag" data-tip="Manchester United. Also Cubs, Bears, Blackhawks.">Sports</span>
      </div>
      <span class="tip" id="js-tip"></span>
    </div>

    <!-- FAVORITES -->
    <div class="sec" id="s-favs">
      <span class="sc-lbl">Quick favorites</span>
      <div class="favs">
        <div class="fav"><span class="fcat">Film</span><span class="fval">Speed Racer</span></div>
        <div class="fav"><span class="fcat">Book</span><span class="fval">Project Hail Mary</span></div>
        <div class="fav"><span class="fcat">Artist</span><span class="fval">Bad Bunny</span></div>
        <div class="fav"><span class="fcat">Game</span><span class="fval">The Last of Us</span></div>
        <div class="fav"><span class="fcat">Club</span><span class="fval">Manchester United</span></div>
        <div class="fav"><span class="fcat">Letterboxd</span><span class="fval">Mantov09</span></div>
      </div>
    </div>

    <!-- CTA -->
    <div class="sec" id="s-cta" style="border-bottom:none; padding-bottom:0;">
      <div class="lks">
        <a href="/articles/" class="btn btn-p">Read articles</a>
        <a href="/projects/" class="btn btn-s">View projects</a>
        <a href="/contact/" class="btn btn-s">Get in touch →</a>
        <a href="https://www.linkedin.com/in/mantovbiz/" target="_blank" rel="noopener" class="btn btn-s">LinkedIn →</a>
      </div>
    </div>

  </div>
</div>

<script>
(function() {
  /* Fade-up sections */
  var fo = new IntersectionObserver(function(entries) {
    entries.forEach(function(e) { if (e.isIntersecting) e.target.classList.add('on'); });
  }, { threshold: 0.07 });
  document.querySelectorAll('#ab .sec').forEach(function(el) { fo.observe(el); });

  /* Tool cards stagger */
  var tc = document.querySelectorAll('#ab .tool');
  var to = new IntersectionObserver(function(entries) {
    entries.forEach(function(e) {
      if (!e.isIntersecting) return;
      tc.forEach(function(c, i) { setTimeout(function() { c.classList.add('on'); }, i * 80); });
      to.disconnect();
    });
  }, { threshold: 0.1 });
  var tg = document.getElementById('js-tools');
  if (tg) to.observe(tg);

  /* Interest tooltips */
  var tags = document.querySelectorAll('#ab .tag');
  var tip  = document.getElementById('js-tip');
  tags.forEach(function(tag) {
    tag.addEventListener('mouseenter', function() {
      tags.forEach(function(t) { t.classList.remove('on'); });
      tag.classList.add('on');
      tip.textContent = tag.dataset.tip;
    });
    tag.addEventListener('mouseleave', function() {
      tag.classList.remove('on');
      tip.textContent = '';
    });
  });
})();
</script>
