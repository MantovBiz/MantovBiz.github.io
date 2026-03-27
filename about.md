---
layout: default
title: "About"
permalink: /about/
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Sans:ital,wght@0,300;0,400;0,500;1,300&display=swap');

  /* ── Hard reset the shell and everything inside it ── */
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
    box-sizing: border-box;
    padding: 2.5rem 2rem 6rem;
  }

  #ab * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  /* ── Back link ── */
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

  /* ══════════════════════════════════════════════════════
     FLEXBOX ROW — sidebar | main | panel
     Flexbox is used instead of CSS Grid because it doesn't
     rely on grid-template-areas and works correctly even
     when the parent width isn't explicitly set by the theme.
  ══════════════════════════════════════════════════════ */
  #ab .row {
    display: flex;
    flex-direction: row;
    align-items: flex-start;
    gap: 2rem;
    width: 100%;
  }

  /* ── LEFT SIDEBAR ── */
  #ab .sb {
    flex: 0 0 200px;
    width: 200px;
    position: sticky;
    top: 1.5rem;
    align-self: flex-start;
  }

  #ab .av {
    width: 78px;
    height: 78px;
    border-radius: 50%;
    background: #fff;
    border: 1px solid #e8e8e8;
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'DM Serif Display', serif;
    font-size: 1.35rem;
    color: #c0392b;
    margin-bottom: 0.8rem;
    letter-spacing: -1px;
    flex-shrink: 0;
  }

  #ab .sb-name {
    font-family: 'DM Serif Display', serif;
    font-size: 1.1rem;
    line-height: 1.2;
    letter-spacing: -0.01em;
    color: #1a1a1a;
    display: block;
    margin-bottom: 0.2rem;
  }

  #ab .sb-role {
    font-size: 0.74rem;
    color: #888;
    font-weight: 300;
    line-height: 1.6;
    display: block;
    margin-bottom: 1rem;
  }

  #ab .div {
    border: none;
    border-top: 1px solid #e8e8e8;
    margin: 0.8rem 0;
    display: block;
  }

  #ab .ml {
    font-size: 0.57rem;
    text-transform: uppercase;
    letter-spacing: 0.12em;
    font-weight: 500;
    color: #aaa;
    display: block;
    margin-bottom: 0.14rem;
  }

  #ab .mv {
    font-size: 0.75rem;
    color: #1a1a1a;
    font-weight: 300;
    display: flex;
    align-items: center;
    gap: 0.3rem;
    margin-bottom: 0.65rem;
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
    font-size: 0.57rem;
    text-transform: uppercase;
    letter-spacing: 0.12em;
    font-weight: 500;
    color: #aaa;
    display: block;
    margin-bottom: 0.4rem;
  }

  #ab .nav { list-style: none; margin-bottom: 0.8rem; }
  #ab .nav li a {
    display: block;
    font-size: 0.75rem;
    color: #888;
    text-decoration: none;
    padding: 0.25rem 0;
    border-bottom: 1px solid #e8e8e8;
    font-weight: 300;
    transition: color 0.15s, padding-left 0.15s;
  }
  #ab .nav li:last-child a { border-bottom: none; }
  #ab .nav li a:hover { color: #1a1a1a; padding-left: 0.3rem; }

  #ab .lks { display: flex; flex-direction: column; gap: 0.32rem; }
  #ab .lk {
    font-size: 0.73rem;
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
    font-size: 0.62rem;
    text-transform: uppercase;
    letter-spacing: 0.13em;
    font-weight: 500;
    color: #c0392b;
    display: block;
    margin-bottom: 0.38rem;
  }

  #ab h1 {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(1.75rem, 2.8vw, 2.6rem);
    letter-spacing: -0.02em;
    line-height: 1.08;
    color: #1a1a1a;
    font-weight: 400;
    margin-bottom: 0.6rem;
    display: block;
  }

  #ab .bio {
    font-size: 0.93rem;
    color: #555;
    font-weight: 300;
    line-height: 1.85;
    display: block;
    margin-bottom: 1.6rem;
    padding-bottom: 1.6rem;
    border-bottom: 1px solid #e8e8e8;
  }

  /* Stat cards */
  #ab .stats {
    display: flex;
    gap: 0.6rem;
    margin-bottom: 2rem;
  }

  #ab .stat {
    flex: 1;
    background: #fff;
    border: 1px solid #e8e8e8;
    border-radius: 4px;
    padding: 0.75rem 0.85rem;
    opacity: 0;
    transform: translateY(8px);
    transition: opacity 0.4s ease, transform 0.4s ease, border-color 0.15s;
  }
  #ab .stat.on { opacity: 1; transform: translateY(0); }
  #ab .stat:hover { border-color: #bbb; }

  #ab .sn {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(1.3rem, 2vw, 1.7rem);
    letter-spacing: -0.03em;
    line-height: 1;
    color: #1a1a1a;
    display: block;
    margin-bottom: 0.16rem;
  }

  #ab .sl {
    font-size: 0.6rem;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    font-weight: 500;
    color: #888;
    display: block;
  }

  /* Section label */
  #ab .sc-lbl {
    font-size: 0.61rem;
    text-transform: uppercase;
    letter-spacing: 0.12em;
    font-weight: 500;
    color: #888;
    display: block;
    margin-bottom: 0.9rem;
    padding-bottom: 0.45rem;
    border-bottom: 1px solid #e8e8e8;
  }

  /* Fade-up section */
  #ab .sec {
    margin-bottom: 2.1rem;
    opacity: 0;
    transform: translateY(14px);
    transition: opacity 0.5s ease, transform 0.5s ease;
    display: block;
  }
  #ab .sec.on { opacity: 1; transform: translateY(0); }

  /* Why body */
  #ab .why p {
    font-size: 0.92rem;
    line-height: 1.88;
    font-weight: 300;
    color: #444;
    margin-bottom: 0.9rem;
    display: block;
  }
  #ab .why p:last-child { margin-bottom: 0; }

  /* Currently */
  #ab .now {
    display: flex;
    flex-wrap: wrap;
    gap: 0.6rem;
  }

  #ab .nc {
    flex: 1 1 calc(50% - 0.3rem);
    min-width: 140px;
    background: #fff;
    border: 1px solid #e8e8e8;
    border-radius: 4px;
    padding: 0.7rem 0.85rem;
    transition: border-color 0.15s, transform 0.15s;
    display: block;
  }
  #ab .nc:hover { border-color: #bbb; transform: translateY(-1px); }

  #ab .nc-lbl {
    font-size: 0.57rem;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    font-weight: 500;
    color: #c0392b;
    display: block;
    margin-bottom: 0.16rem;
  }
  #ab .nc-title {
    font-size: 0.84rem;
    font-weight: 400;
    color: #1a1a1a;
    line-height: 1.35;
    display: block;
  }
  #ab .nc-sub {
    font-size: 0.69rem;
    color: #888;
    font-weight: 300;
    display: block;
    margin-top: 0.1rem;
  }

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
  #ab .tool:hover { border-color: #bbb; transform: translateY(-2px); box-shadow: 0 4px 12px rgba(0,0,0,0.06); }
  #ab .tool img { width: 26px; height: 26px; object-fit: contain; display: block; }
  #ab .tool span {
    font-size: 0.58rem;
    text-transform: uppercase;
    letter-spacing: 0.08em;
    font-weight: 500;
    color: #888;
    text-align: center;
    display: block;
  }

  /* Interests */
  #ab .tags { display: flex; flex-wrap: wrap; gap: 0.38rem; margin-bottom: 0.7rem; }

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
    font-size: 0.77rem;
    color: #c0392b;
    font-style: italic;
    font-weight: 300;
    min-height: 1.3rem;
    display: block;
  }

  /* CTA */
  #ab .cta {
    display: flex;
    gap: 0.55rem;
    flex-wrap: wrap;
    padding-top: 1.6rem;
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

  /* ── RIGHT PANEL ── */
  #ab .pn {
    flex: 0 0 220px;
    width: 220px;
    position: sticky;
    top: 1.5rem;
    align-self: flex-start;
    display: flex;
    flex-direction: column;
    gap: 0.85rem;
  }

  #ab .pc {
    background: #fff;
    border: 1px solid #e8e8e8;
    border-radius: 4px;
    padding: 0.85rem 0.95rem;
    display: block;
  }

  #ab .pc-lbl {
    font-size: 0.57rem;
    text-transform: uppercase;
    letter-spacing: 0.12em;
    font-weight: 500;
    color: #aaa;
    display: block;
    margin-bottom: 0.75rem;
    padding-bottom: 0.42rem;
    border-bottom: 1px solid #e8e8e8;
  }

  /* Goals */
  #ab .goals { list-style: none; display: flex; flex-direction: column; gap: 0.5rem; }

  #ab .goal {
    display: flex;
    align-items: flex-start;
    gap: 0.5rem;
    font-size: 0.76rem;
    font-weight: 300;
    color: #444;
    line-height: 1.5;
  }

  #ab .gd {
    width: 7px;
    height: 7px;
    border-radius: 50%;
    flex-shrink: 0;
    margin-top: 0.34rem;
    display: block;
  }
  #ab .gd-done { background: #27ae60; }
  #ab .gd-now  { background: #c0392b; }
  #ab .gd-next { background: #e8e8e8; border: 1px solid #bbb; }

  #ab .glbl {
    font-size: 0.55rem;
    text-transform: uppercase;
    letter-spacing: 0.08em;
    font-weight: 500;
    color: #aaa;
    display: block;
    margin-bottom: 0.04rem;
  }

  /* Favorites */
  #ab .favs { display: flex; flex-direction: column; }
  #ab .fav {
    display: flex;
    justify-content: space-between;
    align-items: baseline;
    padding: 0.38rem 0;
    border-bottom: 1px solid #e8e8e8;
    gap: 0.4rem;
  }
  #ab .fav:last-child { border-bottom: none; }
  #ab .fcat { font-size: 0.57rem; text-transform: uppercase; letter-spacing: 0.08em; font-weight: 500; color: #aaa; flex-shrink: 0; }
  #ab .fval { font-size: 0.73rem; font-weight: 300; color: #1a1a1a; text-align: right; line-height: 1.3; }

  /* Fun facts */
  #ab .ft {
    font-size: 0.78rem;
    font-weight: 300;
    color: #444;
    line-height: 1.7;
    min-height: 3.4rem;
    transition: opacity 0.3s;
    display: block;
  }

  #ab .fc {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-top: 0.65rem;
  }

  #ab .fds { display: flex; gap: 4px; }
  #ab .fd {
    width: 5px; height: 5px;
    border-radius: 50%;
    background: #e8e8e8;
    border: none;
    cursor: pointer;
    padding: 0;
    transition: background 0.2s;
  }
  #ab .fd.on { background: #1a1a1a; }

  #ab .fn {
    font-size: 0.65rem;
    color: #888;
    cursor: pointer;
    background: none;
    border: none;
    font-family: 'DM Sans', sans-serif;
    padding: 0;
  }
  #ab .fn:hover { color: #1a1a1a; }

  /* ══════════════════════════════════════════════════════
     RESPONSIVE
  ══════════════════════════════════════════════════════ */

  /* Tablet: drop right panel below, keep sidebar */
  @media (max-width: 960px) {
    #ab .row { flex-wrap: wrap; }
    #ab .sb  { flex: 0 0 180px; width: 180px; }
    #ab .mn  { flex: 1 1 0; min-width: 0; }
    #ab .pn  {
      flex: 1 1 100%;
      width: 100%;
      position: static;
      flex-direction: row;
      flex-wrap: wrap;
      gap: 0.7rem;
    }
    #ab .pc  { flex: 1 1 200px; }
  }

  /* Mobile: full single column */
  @media (max-width: 600px) {
    #ab { padding: 1.25rem 1rem 4rem; }

    #ab .row { flex-direction: column; gap: 1.25rem; }

    #ab .sb {
      position: static;
      width: 100%;
      flex: none;
      display: flex;
      align-items: center;
      gap: 0.85rem;
      flex-wrap: wrap;
      padding-bottom: 1rem;
      border-bottom: 1px solid #e8e8e8;
    }

    #ab .av { width: 54px; height: 54px; font-size: 1rem; margin-bottom: 0; }
    #ab .sb-name { font-size: 0.95rem; }
    #ab .sb-role { margin-bottom: 0; }
    #ab .div, #ab .ml, #ab .mv, #ab .nl, #ab .nav, #ab .lks { display: none; }

    #ab .mn { flex: none; width: 100%; }

    #ab .pn {
      position: static;
      width: 100%;
      flex: none;
      flex-direction: column;
    }

    #ab .stats { flex-wrap: wrap; }
    #ab .stat  { flex: 1 1 calc(50% - 0.3rem); min-width: 100px; }
    #ab .nc    { flex: 1 1 100%; }
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
        <li><a href="#s-now">Currently</a></li>
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

      <div class="stats" id="js-stats">
        <div class="stat"><span class="sn">5</span><span class="sl">Tools</span></div>
        <div class="stat"><span class="sn">2</span><span class="sl">Degrees</span></div>
        <div class="stat"><span class="sn">8+</span><span class="sl">Interests</span></div>
        <div class="stat"><span class="sn">∞</span><span class="sl">Curiosity</span></div>
      </div>

      <div class="sec" id="s-why">
        <span class="sc-lbl">Why I study what I study</span>
        <div class="why">
          <p>Ever since I was a kid, I loved watching sports and seeing the stats behind the game. Soccer is my passion — seeing the amount of possession, passes completed vs attempted, heatmaps, and many other visuals is all so interesting to me, which is why I wanted to learn more about it.</p>
          <p>This is why I decided to study Business Analytics, because it would give me the fundamentals of analyzing data. I also love stories, whether it is reading or watching, which is why I decided to get a Sports Communication minor. Pairing those together would help me get to where I want to be.</p>
          <p>Now here I am, writing whatever I find in my research or just want to talk about and share with others. Feel free to check out my projects and the articles that I have written. Thank you for taking the time to check out some of my work!</p>
        </div>
      </div>

      <div class="sec" id="s-now">
        <span class="sc-lbl">Currently</span>
        <div class="now">
          <div class="nc"><span class="nc-lbl">Reading</span><span class="nc-title">Project Hail Mary</span><span class="nc-sub">Andy Weir · Sci-Fi</span></div>
          <div class="nc"><span class="nc-lbl">Watching</span><span class="nc-title">Speed Racer</span><span class="nc-sub">All-time favorite rewatch</span></div>
          <div class="nc"><span class="nc-lbl">Listening to</span><span class="nc-title">Bad Bunny</span><span class="nc-sub">Nadie Sabe Lo Que Va a Pasar Mañana</span></div>
          <div class="nc"><span class="nc-lbl">Playing</span><span class="nc-title">The Last of Us</span><span class="nc-sub">PS4 · Single player</span></div>
        </div>
      </div>

      <div class="sec" id="s-tools">
        <span class="sc-lbl">Tools &amp; skills</span>
        <div class="tools" id="js-tools">
          <div class="tool"><img src="https://upload.wikimedia.org/wikipedia/commons/c/cf/New_Power_BI_Logo.svg" alt="Power BI"><span>Power BI</span></div>
          <div class="tool"><img src="https://upload.wikimedia.org/wikipedia/commons/4/4b/Tableau_Logo.png" alt="Tableau"><span>Tableau</span></div>
          <div class="tool"><img src="https://upload.wikimedia.org/wikipedia/commons/3/34/Microsoft_Office_Excel_%282019%E2%80%93present%29.svg" alt="Excel"><span>Excel</span></div>
          <div class="tool"><img src="https://upload.wikimedia.org/wikipedia/commons/1/1b/R_logo.svg" alt="R"><span>R</span></div>
          <div class="tool"><img src="https://upload.wikimedia.org/wikipedia/commons/8/87/Sql_data_base_with_logo.png" alt="SQL"><span>SQL</span></div>
        </div>
      </div>

      <div class="sec" id="s-int">
        <span class="sc-lbl">Interests</span>
        <div class="tags">
          <span class="tag" data-tip="The nerdy stuff — analyzing data behind the game is almost as fun as watching it.">Sports analytics</span>
          <span class="tag" data-tip="Visuals tell a story with a little. Possession maps, heatmaps, pass networks — I love them all.">Data visualization</span>
          <span class="tag" data-tip="Movies move me. Favorite film: Speed Racer. Find me on Letterboxd: Mantov09">Film &amp; cinema</span>
          <span class="tag" data-tip="Bad Bunny, Kendrick Lamar, Dave — probably my top 3.">Music</span>
          <span class="tag" data-tip="Sci-Fi and Greek Mythology. Favorites: Percy Jackson, Project Hail Mary, Michael Vey.">Books</span>
          <span class="tag" data-tip="Single player is my lane. The Last of Us, Dispatch, Spider-Man PS4.">Video games</span>
          <span class="tag" data-tip="Few things beat playing a game with people you enjoy spending time with.">Board games</span>
          <span class="tag" data-tip="Manchester United supporter. Also Cubs, Bears, Blackhawks.">Sports</span>
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

    <!-- RIGHT PANEL -->
    <aside class="pn">

      <div class="pc">
        <span class="pc-lbl">Goals &amp; roadmap</span>
        <ul class="goals">
          <li class="goal"><span class="gd gd-done"></span><div><span class="glbl">Done</span>Declared Business Analytics + Sports Comm minor</div></li>
          <li class="goal"><span class="gd gd-done"></span><div><span class="glbl">Done</span>Built this blog &amp; launched first projects</div></li>
          <li class="goal"><span class="gd gd-now"></span><div><span class="glbl">Now</span>Deepening SQL, R, and data viz skills</div></li>
          <li class="goal"><span class="gd gd-next"></span><div><span class="glbl">Next</span>Land a sports analytics or data internship</div></li>
          <li class="goal"><span class="gd gd-next"></span><div><span class="glbl">Future</span>Work at the intersection of sports &amp; data storytelling</div></li>
        </ul>
      </div>

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

      <div class="pc">
        <span class="pc-lbl">Fun facts</span>
        <span class="ft" id="js-ft"></span>
        <div class="fc">
          <div class="fds" id="js-fds"></div>
          <button class="fn" id="js-fn">Next →</button>
        </div>
      </div>

    </aside>

  </div><!-- /.row -->
</div><!-- /#ab -->

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

  /* Stat cards stagger */
  var sc = document.querySelectorAll('#ab .stat');
  var so = new IntersectionObserver(function(entries) {
    entries.forEach(function(e) {
      if (!e.isIntersecting) return;
      sc.forEach(function(c, i) { setTimeout(function() { c.classList.add('on'); }, i * 80); });
      so.disconnect();
    });
  }, { threshold: 0.1 });
  var sr = document.getElementById('js-stats');
  if (sr) so.observe(sr);

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

  /* Fun facts */
  var facts = [
    "I can watch Speed Racer an unlimited number of times and still feel something every single time.",
    "I track every film I watch on Letterboxd. Find me at Mantov09.",
    "Soccer data changed how I watch the game — I can't see a match without mentally noting possession and pressing patterns.",
    "Percy Jackson got me into Greek mythology before it was cool again.",
    "I genuinely believe The Last of Us has one of the best stories ever written, in any medium.",
    "Bad Bunny, Kendrick, and Dave is a playlist I could run on loop for a full week.",
    "I want to work where sports meets data storytelling — telling the story behind the numbers."
  ];
  var fi = 0;
  var ft = document.getElementById('js-ft');
  var fds = document.getElementById('js-fds');
  var fn = document.getElementById('js-fn');

  function dots() {
    fds.innerHTML = '';
    facts.forEach(function(_, i) {
      var d = document.createElement('button');
      d.className = 'fd' + (i === fi ? ' on' : '');
      d.addEventListener('click', function() { show(i); });
      fds.appendChild(d);
    });
  }

  function show(idx) {
    ft.style.opacity = '0';
    setTimeout(function() {
      fi = (idx + facts.length) % facts.length;
      ft.textContent = facts[fi];
      ft.style.opacity = '1';
      dots();
    }, 250);
  }

  ft.textContent = facts[0];
  dots();
  fn.addEventListener('click', function() { show(fi + 1); });
  setInterval(function() { show(fi + 1); }, 6000);
})();
</script>
