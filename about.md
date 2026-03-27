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
    padding: 2.5rem 2rem 6rem;
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
    margin-bottom: 1.75rem;
  }
  #ab .bk:hover { color: #1a1a1a; }

  /* ── 3-column flex row ── */
  #ab .row {
    display: flex;
    flex-direction: row;
    align-items: flex-start;
    gap: 2.5rem;
    width: 100%;
  }

  /* ── LEFT SIDEBAR ── */
  #ab .sb {
    flex: 0 0 190px;
    width: 190px;
    position: sticky;
    top: 1.5rem;
    align-self: flex-start;
  }

  #ab .av {
    width: 72px;
    height: 72px;
    border-radius: 50%;
    background: #fff;
    border: 1px solid #e8e8e8;
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'DM Serif Display', serif;
    font-size: 1.3rem;
    color: #c0392b;
    margin-bottom: 0.75rem;
    letter-spacing: -1px;
    flex-shrink: 0;
  }

  #ab .sb-name {
    font-family: 'DM Serif Display', serif;
    font-size: 1.05rem;
    line-height: 1.2;
    color: #1a1a1a;
    display: block;
    margin-bottom: 0.18rem;
  }

  #ab .sb-role {
    font-size: 0.73rem;
    color: #888;
    font-weight: 300;
    line-height: 1.6;
    display: block;
    margin-bottom: 0.9rem;
  }

  #ab .div {
    border: none;
    border-top: 1px solid #e8e8e8;
    margin: 0.75rem 0;
    display: block;
  }

  #ab .ml {
    font-size: 0.56rem;
    text-transform: uppercase;
    letter-spacing: 0.12em;
    font-weight: 500;
    color: #bbb;
    display: block;
    margin-bottom: 0.12rem;
  }

  #ab .mv {
    font-size: 0.74rem;
    color: #1a1a1a;
    font-weight: 300;
    display: flex;
    align-items: center;
    gap: 0.3rem;
    margin-bottom: 0.6rem;
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

  #ab .nl {
    font-size: 0.56rem;
    text-transform: uppercase;
    letter-spacing: 0.12em;
    font-weight: 500;
    color: #bbb;
    display: block;
    margin-bottom: 0.38rem;
  }

  #ab .nav { list-style: none; margin-bottom: 0.75rem; }
  #ab .nav li a {
    display: block;
    font-size: 0.74rem;
    color: #888;
    text-decoration: none;
    padding: 0.22rem 0;
    border-bottom: 1px solid #e8e8e8;
    font-weight: 300;
    transition: color 0.15s, padding-left 0.15s;
  }
  #ab .nav li:last-child a { border-bottom: none; }
  #ab .nav li a:hover { color: #1a1a1a; padding-left: 0.3rem; }

  #ab .lks { display: flex; flex-direction: column; gap: 0.3rem; }
  #ab .lk {
    font-size: 0.72rem;
    color: #2563a8;
    text-decoration: none;
    display: block;
  }
  #ab .lk:hover { opacity: 0.65; }

  /* ── MAIN CONTENT ── */
  #ab .mn {
    flex: 1 1 0;
    min-width: 0;
  }

  #ab .ey {
    font-size: 0.61rem;
    text-transform: uppercase;
    letter-spacing: 0.13em;
    font-weight: 500;
    color: #c0392b;
    display: block;
    margin-bottom: 0.35rem;
  }

  #ab h1 {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(1.75rem, 2.8vw, 2.5rem);
    letter-spacing: -0.02em;
    line-height: 1.08;
    color: #1a1a1a;
    font-weight: 400;
    margin-bottom: 0.55rem;
    display: block;
  }

  #ab .bio {
    font-size: 0.92rem;
    color: #555;
    font-weight: 300;
    line-height: 1.85;
    display: block;
    margin-bottom: 2rem;
    padding-bottom: 2rem;
    border-bottom: 1px solid #e8e8e8;
  }

  /* Section label */
  #ab .sc-lbl {
    font-size: 0.6rem;
    text-transform: uppercase;
    letter-spacing: 0.12em;
    font-weight: 500;
    color: #888;
    display: block;
    margin-bottom: 0.9rem;
    padding-bottom: 0.42rem;
    border-bottom: 1px solid #e8e8e8;
  }

  /* Fade-up section */
  #ab .sec {
    margin-bottom: 2.25rem;
    opacity: 0;
    transform: translateY(12px);
    transition: opacity 0.5s ease, transform 0.5s ease;
    display: block;
  }
  #ab .sec.on { opacity: 1; transform: translateY(0); }

  /* Why body */
  #ab .why p {
    font-size: 0.91rem;
    line-height: 1.88;
    font-weight: 300;
    color: #444;
    margin-bottom: 0.85rem;
    display: block;
  }
  #ab .why p:last-child { margin-bottom: 0; }

  /* Tools */
  #ab .tools { display: flex; flex-wrap: wrap; gap: 0.55rem; }

  #ab .tool {
    background: #fff;
    border: 1px solid #e8e8e8;
    border-radius: 4px;
    padding: 0.68rem 0.8rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 0.4rem;
    width: 82px;
    opacity: 0;
    transform: translateY(8px);
    transition: opacity 0.4s ease, transform 0.4s ease, border-color 0.15s, box-shadow 0.15s;
  }
  #ab .tool.on { opacity: 1; transform: translateY(0); }
  #ab .tool:hover { border-color: #bbb; transform: translateY(-2px); box-shadow: 0 4px 12px rgba(0,0,0,0.05); }
  #ab .tool img { width: 26px; height: 26px; object-fit: contain; display: block; }
  #ab .tool span {
    font-size: 0.57rem;
    text-transform: uppercase;
    letter-spacing: 0.08em;
    font-weight: 500;
    color: #888;
    text-align: center;
    display: block;
  }

  /* Interests */
  #ab .tags { display: flex; flex-wrap: wrap; gap: 0.38rem; margin-bottom: 0.65rem; }

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
    display: inline-block;
  }
  #ab .tag:hover, #ab .tag.on { background: #1a1a1a; color: #fff; border-color: #1a1a1a; }

  #ab .tip {
    font-size: 0.76rem;
    color: #c0392b;
    font-style: italic;
    font-weight: 300;
    min-height: 1.25rem;
    display: block;
  }

  /* CTA */
  #ab .cta {
    display: flex;
    gap: 0.55rem;
    flex-wrap: wrap;
    padding-top: 1.75rem;
    border-top: 1px solid #e8e8e8;
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

  /* ── RIGHT PANEL — quick favorites only ── */
  #ab .pn {
    flex: 0 0 200px;
    width: 200px;
    position: sticky;
    top: 1.5rem;
    align-self: flex-start;
  }

  #ab .pc {
    background: #fff;
    border: 1px solid #e8e8e8;
    border-radius: 4px;
    padding: 0.9rem 1rem;
    display: block;
  }

  #ab .pc-lbl {
    font-size: 0.57rem;
    text-transform: uppercase;
    letter-spacing: 0.12em;
    font-weight: 500;
    color: #bbb;
    display: block;
    margin-bottom: 0.75rem;
    padding-bottom: 0.42rem;
    border-bottom: 1px solid #e8e8e8;
  }

  #ab .favs { display: flex; flex-direction: column; }

  #ab .fav {
    display: flex;
    justify-content: space-between;
    align-items: baseline;
    padding: 0.42rem 0;
    border-bottom: 1px solid #f0f0ee;
    gap: 0.5rem;
  }
  #ab .fav:last-child { border-bottom: none; }

  #ab .fcat {
    font-size: 0.57rem;
    text-transform: uppercase;
    letter-spacing: 0.08em;
    font-weight: 500;
    color: #bbb;
    flex-shrink: 0;
  }

  #ab .fval {
    font-size: 0.74rem;
    font-weight: 300;
    color: #1a1a1a;
    text-align: right;
    line-height: 1.3;
  }

  /* ── RESPONSIVE ── */
  @media (max-width: 900px) {
    #ab .row { flex-wrap: wrap; }
    #ab .sb  { flex: 0 0 170px; width: 170px; }
    #ab .mn  { flex: 1 1 0; min-width: 0; }
    #ab .pn  { flex: 1 1 100%; width: 100%; position: static; }
    #ab .pc  { max-width: 320px; }
  }

  @media (max-width: 580px) {
    #ab { padding: 1.25rem 1rem 4rem; }
    #ab .row { flex-direction: column; gap: 1.25rem; }

    #ab .sb {
      position: static;
      width: 100%;
      flex: none;
      display: flex;
      align-items: center;
      gap: 0.85rem;
      padding-bottom: 1rem;
      border-bottom: 1px solid #e8e8e8;
    }

    #ab .av { width: 52px; height: 52px; font-size: 1rem; margin-bottom: 0; }
    #ab .sb-name { font-size: 0.95rem; }
    #ab .sb-role { margin-bottom: 0; }
    #ab .div, #ab .ml, #ab .mv, #ab .nl, #ab .nav, #ab .lks { display: none; }

    #ab .mn { flex: none; width: 100%; }
    #ab .pn { position: static; width: 100%; flex: none; }
    #ab .pc { max-width: 100%; }
  }
</style>

<div id="ab">

  <a href="/" class="bk">← Home</a>

  <div class="row">

    <!-- LEFT SIDEBAR -->
    <aside class="sb">
      <div class="av">MT</div>
      <span class="sb-name">Manuel Tovar</span>
      <span class="sb-role">MIS &amp; Business Analytics<br>DePaul University</span>

      <hr class="div">

      <span class="ml">Location</span>
      <div class="mv">Chicago, IL</div>

      <span class="ml">Status</span>
      <div class="mv"><span class="dot"></span>Open to internships</div>

      <span class="ml">Minor</span>
      <div class="mv">Sports Communication</div>

      <span class="ml">Favorite club</span>
      <div class="mv">Manchester United</div>

      <hr class="div">

      <span class="nl">On this page</span>
      <ul class="nav">
        <li><a href="#s-why">Why I study this</a></li>
        <li><a href="#s-tools">Tools &amp; skills</a></li>
        <li><a href="#s-int">Interests</a></li>
      </ul>

      <hr class="div">

      <div class="lks">
        <a href="https://www.linkedin.com/in/mantovbiz/" target="_blank" rel="noopener" class="lk">LinkedIn →</a>
        <a href="/projects/" class="lk">View projects →</a>
        <a href="/articles/" class="lk">Read articles →</a>
        <a href="/contact/" class="lk">Get in touch →</a>
      </div>
    </aside>

    <!-- MAIN CONTENT -->
    <main class="mn">

      <span class="ey">About</span>
      <h1>Manuel Tovar</h1>
      <span class="bio">MIS &amp; Business Analytics student at DePaul University. I write about data, sports, film, and whatever else is worth thinking about — and build projects around the things I find interesting.</span>

      <div class="sec" id="s-why">
        <span class="sc-lbl">Why I study what I study</span>
        <div class="why">
          <p>Ever since I was a kid, I loved watching sports and seeing the stats behind the game. Soccer is my passion — seeing possession data, heatmaps, and pass networks captivated me early. That curiosity is what pushed me toward Business Analytics.</p>
          <p>I also love stories — reading, watching, telling them. That's why I paired my analytics degree with a Sports Communication minor. Data and storytelling together is exactly where I want to be.</p>
        </div>
      </div>

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

      <div class="sec cta" id="s-cta">
        <a href="/articles/" class="btn btn-p">Read articles</a>
        <a href="/projects/" class="btn btn-s">View projects</a>
        <a href="/contact/" class="btn btn-s">Get in touch →</a>
        <a href="https://www.linkedin.com/in/mantovbiz/" target="_blank" rel="noopener" class="btn btn-s">LinkedIn →</a>
      </div>

    </main>

    <!-- RIGHT PANEL — quick favorites only -->
    <aside class="pn">
      <div class="pc">
        <span class="pc-lbl">Quick favorites</span>
        <div class="favs">
          <div class="fav"><span class="fcat">Film</span><span class="fval">Speed Racer</span></div>
          <div class="fav"><span class="fcat">Book</span><span class="fval">Project Hail Mary</span></div>
          <div class="fav"><span class="fcat">Artist</span><span class="fval">Bad Bunny</span></div>
          <div class="fav"><span class="fcat">Game</span><span class="fval">The Last of Us</span></div>
          <div class="fav"><span class="fcat">Club</span><span class="fval">Manchester United</span></div>
          <div class="fav"><span class="fcat">Letterboxd</span><span class="fval">Mantov09</span></div>
        </div>
      </div>
    </aside>

  </div>
</div>

<script>
(function() {
  /* Smooth scroll */
  document.querySelectorAll('#ab .nav a').forEach(function(a) {
    a.addEventListener('click', function(e) {
      e.preventDefault();
      var t = document.querySelector(a.getAttribute('href'));
      if (t) t.scrollIntoView({ behavior: 'smooth', block: 'start' });
    });
  });

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
      tc.forEach(function(c, i) { setTimeout(function() { c.classList.add('on'); }, i * 90); });
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
