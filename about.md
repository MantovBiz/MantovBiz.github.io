---
layout: default
title: "About"
permalink: /about/
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Sans:ital,wght@0,300;0,400;0,500;1,300&display=swap');

  :root {
    --bg: #fafaf8;
    --text: #1a1a1a;
    --muted: #666;
    --light: #e8e8e8;
    --lighter: #f3f3f1;
    --accent: #c0392b;
  }

  #ab,
  #ab * {
    box-sizing: border-box;
  }

  #ab {
    all: initial;
    display: block;
    font-family: 'DM Sans', sans-serif;
    font-size: 15px;
    line-height: 1.65;
    color: var(--text);
    background: var(--bg);
    width: 100%;
    min-height: 100vh;
    padding: clamp(1.25rem, 3vw, 2.5rem) clamp(1rem, 3vw, 1.5rem) 5rem;
  }

  #ab .wrap {
    width: min(100%, 980px);
    margin: 0 auto;
  }

  #ab .bk {
    display: inline-flex;
    align-items: center;
    gap: 0.35rem;
    font-size: 0.8rem;
    color: #888;
    text-decoration: none;
    font-weight: 300;
    letter-spacing: 0.02em;
    margin-bottom: 2rem;
    transition: color 0.15s ease;
  }

  #ab .bk:hover {
    color: var(--text);
  }

  #ab .hero {
    display: grid;
    grid-template-columns: 1fr 120px;
    gap: 1.5rem;
    align-items: start;
    padding-bottom: 2rem;
    border-bottom: 1px solid var(--light);
    margin-bottom: 2rem;
  }

  #ab .hero-left {
    display: flex;
    flex-direction: column;
  }

  #ab .hero-label {
    display: flex;
    align-items: center;
    gap: 0.55rem;
    font-size: 0.62rem;
    text-transform: uppercase;
    letter-spacing: 0.14em;
    font-weight: 500;
    color: var(--accent);
    margin-bottom: 0.5rem;
  }

  #ab .hero-label::before {
    content: '';
    display: inline-block;
    width: 18px;
    height: 1.5px;
    background: var(--accent);
    flex-shrink: 0;
  }

  #ab .hero-name {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(2rem, 5vw, 3.2rem);
    line-height: 1.05;
    letter-spacing: -0.02em;
    margin-bottom: 0.35rem;
  }

  #ab .hero-role {
    font-size: 0.84rem;
    color: #888;
    font-weight: 300;
    margin-bottom: 1rem;
  }

  #ab .hero-bio {
    font-size: 0.96rem;
    color: #444;
    font-weight: 300;
    line-height: 1.85;
    max-width: 62ch;
  }

  #ab .hero-photo {
    width: 120px;
    height: 120px;
    border-radius: 6px;
    object-fit: cover;
    border: 1px solid var(--light);
    display: block;
    background: #f0f0ee;
  }

  #ab .meta-row {
    display: flex;
    flex-wrap: wrap;
    gap: 0.45rem;
    margin-bottom: 2rem;
  }

  #ab .meta-pill {
    display: inline-flex;
    align-items: center;
    gap: 0.35rem;
    font-size: 0.75rem;
    font-weight: 300;
    color: #555;
    background: #fff;
    border: 1px solid var(--light);
    border-radius: 3px;
    padding: 0.35rem 0.75rem;
  }

  #ab .meta-pill .dot {
    width: 6px;
    height: 6px;
    border-radius: 50%;
    background: #27ae60;
    flex-shrink: 0;
    animation: pulse 2.5s ease-in-out infinite;
  }

  @keyframes pulse {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.3; }
  }

  #ab .sec {
    margin-bottom: 2rem;
    padding-bottom: 2rem;
    border-bottom: 1px solid var(--light);
    opacity: 0;
    transform: translateY(10px);
    transition: opacity 0.4s ease, transform 0.4s ease;
  }

  #ab .sec.on {
    opacity: 1;
    transform: translateY(0);
  }

  #ab .sec:last-child {
    border-bottom: none;
    margin-bottom: 0;
    padding-bottom: 0;
  }

  #ab .sc-lbl {
    font-size: 0.6rem;
    text-transform: uppercase;
    letter-spacing: 0.13em;
    font-weight: 500;
    color: #aaa;
    display: block;
    margin-bottom: 1rem;
  }

  #ab .why p {
    font-size: 0.96rem;
    line-height: 1.85;
    font-weight: 300;
    color: #444;
    margin-bottom: 0.85rem;
    max-width: 70ch;
  }

  #ab .why p:last-child {
    margin-bottom: 0;
  }

  #ab .tools {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(130px, 1fr));
    gap: 0.6rem;
  }

  #ab .tool {
    background: #fff;
    border: 1px solid var(--light);
    border-radius: 4px;
    padding: 0.7rem 0.8rem;
    display: flex;
    align-items: center;
    gap: 0.55rem;
    opacity: 0;
    transform: translateY(5px);
    transition: opacity 0.3s ease, transform 0.3s ease, border-color 0.15s, box-shadow 0.15s;
  }

  #ab .tool.on {
    opacity: 1;
    transform: translateY(0);
  }

  #ab .tool:hover {
    border-color: #bbb;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.06);
  }

  #ab .tool img {
    width: 18px;
    height: 18px;
    object-fit: contain;
    display: block;
    flex-shrink: 0;
  }

  #ab .tool span {
    font-size: 0.78rem;
    font-weight: 400;
    color: #555;
  }

  #ab .tags {
    display: flex;
    flex-wrap: wrap;
    gap: 0.4rem;
    margin-bottom: 0.75rem;
  }

  #ab .tag {
    font-size: 0.74rem;
    padding: 0.28rem 0.68rem;
    border: 1px solid var(--light);
    border-radius: 3px;
    background: #fff;
    color: #888;
    cursor: pointer;
    font-weight: 300;
    user-select: none;
    transition: all 0.15s ease;
  }

  #ab .tag:hover,
  #ab .tag.on {
    background: var(--text);
    color: #fff;
    border-color: var(--text);
  }

  #ab .tip {
    font-size: 0.78rem;
    color: var(--accent);
    font-style: italic;
    font-weight: 300;
    min-height: 1.2rem;
    display: block;
  }

  #ab .favs {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 0;
  }

  #ab .fav {
    padding: 0.7rem 0.8rem 0.7rem 0;
    border-bottom: 1px solid #f0f0ee;
    display: flex;
    flex-direction: column;
    gap: 0.15rem;
  }

  #ab .fav:nth-child(even) {
    padding-left: 0.8rem;
    border-left: 1px solid #f0f0ee;
  }

  #ab .fcat {
    font-size: 0.55rem;
    text-transform: uppercase;
    letter-spacing: 0.11em;
    font-weight: 500;
    color: #ccc;
  }

  #ab .fval {
    font-size: 0.86rem;
    font-weight: 400;
    color: var(--text);
  }

  #ab .lks {
    display: flex;
    flex-wrap: wrap;
    gap: 0.6rem;
  }

  #ab a.btn {
    font-family: 'DM Sans', sans-serif;
    font-size: 0.8rem;
    font-weight: 400;
    text-decoration: none;
    padding: 0.55rem 1rem;
    border-radius: 3px;
    transition: all 0.15s ease;
    letter-spacing: 0.02em;
    display: inline-block;
  }

  #ab a.btn-p {
    background: var(--text);
    color: #fff;
    border: 1px solid var(--text);
  }

  #ab a.btn-p:hover {
    background: #333;
  }

  #ab a.btn-s {
    background: transparent;
    color: var(--text);
    border: 1px solid var(--light);
  }

  #ab a.btn-s:hover {
    border-color: var(--text);
  }

  @media (max-width: 700px) {
    #ab .hero {
      grid-template-columns: 1fr;
    }

    #ab .hero-photo {
      width: 88px;
      height: 88px;
      order: -1;
    }

    #ab .favs {
      grid-template-columns: 1fr;
    }

    #ab .fav:nth-child(even) {
      padding-left: 0;
      border-left: none;
    }
  }

  @media (max-width: 500px) {
    #ab {
      padding-top: 1rem;
    }

    #ab .hero {
      gap: 1rem;
    }

    #ab .hero-name {
      font-size: 2rem;
    }

    #ab .tools {
      grid-template-columns: 1fr 1fr;
    }

    #ab a.btn {
      width: 100%;
      text-align: center;
    }

    #ab .lks {
      flex-direction: column;
    }
  }
</style>

<div id="ab">
  <div class="wrap">
    <a href="/" class="bk">← Home</a>

    <div class="hero">
      <div class="hero-left">
        <span class="hero-label">About</span>
        <span class="hero-name">Manuel Tovar</span>
        <span class="hero-role">MIS &amp; Business Analytics · DePaul University</span>
        <p class="hero-bio">
          I study data because I've always wanted to understand the story behind the numbers — starting with soccer stats as a kid, now building analytics projects across sports, business, and culture. I pair that with a Sports Communication minor because data without storytelling is just noise.
        </p>
      </div>
      <img class="hero-photo" src="/assets/images/headshot.jpg" alt="Manuel Tovar" loading="lazy" width="120" height="120"/>
    </div>

    <div class="sec" id="s-why">
      <span class="sc-lbl">Why I study what I study</span>
      <div class="why">
        <p>Ever since I was a kid, I loved watching sports and seeing the stats behind the game. Possession data, heatmaps, pass networks — the visuals that tell the story captivated me early. That curiosity is what pushed me toward Business Analytics.</p>
        <p>I also love stories — reading, watching, telling them. Data and storytelling together is exactly where I want to be.</p>
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
        <div class="tool"><img src="https://upload.wikimedia.org/wikipedia/commons/c/c3/Python-logo-notext.svg" alt="Python"><span>Python</span></div>
      </div>
    </div>

    <div class="sec" id="s-int">
      <span class="sc-lbl">Interests — hover to learn more</span>
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

    <div class="sec" id="s-cta">
      <span class="sc-lbl">Let's connect</span>
      <div class="lks">
        <a href="/articles/" class="btn btn-p">Read articles</a>
        <a href="/projects/" class="btn btn-s">View projects</a>
        <a href="https://www.linkedin.com/in/mantovbiz/" target="_blank" rel="noopener noreferrer" class="btn btn-s">LinkedIn ↗</a>
      </div>
    </div>
  </div>
</div>

<script>
(function() {
  var fo = new IntersectionObserver(function(entries){
    entries.forEach(function(e){ if(e.isIntersecting) e.target.classList.add('on'); });
  }, { threshold: 0.07 });
  document.querySelectorAll('#ab .sec').forEach(function(el){ fo.observe(el); });

  var tc = document.querySelectorAll('#ab .tool');
  var to = new IntersectionObserver(function(entries){
    entries.forEach(function(e){
      if(!e.isIntersecting) return;
      tc.forEach(function(c,i){ setTimeout(function(){ c.classList.add('on'); }, i*70); });
      to.disconnect();
    });
  }, { threshold: 0.1 });
  var tg = document.getElementById('js-tools');
  if(tg) to.observe(tg);

  var tags = document.querySelectorAll('#ab .tag');
  var tip  = document.getElementById('js-tip');
  tags.forEach(function(tag){
    tag.addEventListener('mouseenter', function(){
      tags.forEach(function(t){ t.classList.remove('on'); });
      tag.classList.add('on');
      tip.textCon
