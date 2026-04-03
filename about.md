---
layout: default
title: "About"
permalink: /about/
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Sans:ital,wght@0,300;0,400;0,500;1,300&display=swap');

  #ab, #ab * { box-sizing: border-box; margin: 0; padding: 0; }

  #ab { all: initial; display: block; font-family: 'DM Sans', sans-serif; font-size: 15px; line-height: 1.6; color: #1a1a1a; background: #fafaf8; width: 100%; min-height: 100vh; padding: 2.5rem 1.25rem 5rem; }
  #ab .wrap { max-width: 640px; margin: 0 auto; }

  #ab .bk { display: inline-flex; align-items: center; gap: 0.3rem; font-size: 0.78rem; color: #888; text-decoration: none; font-weight: 300; letter-spacing: 0.02em; margin-bottom: 2.5rem; transition: color 0.15s; }
  #ab .bk:hover { color: #1a1a1a; }

  #ab .hero { display: grid; grid-template-columns: 1fr 88px; gap: 1.5rem; align-items: start; padding-bottom: 2rem; border-bottom: 1px solid #e8e8e8; margin-bottom: 2rem; }
  #ab .hero-left { display: flex; flex-direction: column; }

  #ab .hero-label { display: flex; align-items: center; gap: 0.55rem; font-size: 0.62rem; text-transform: uppercase; letter-spacing: 0.14em; font-weight: 500; color: #c0392b; margin-bottom: 0.5rem; }
  #ab .hero-label::before { content: ''; display: inline-block; width: 18px; height: 1.5px; background: #c0392b; flex-shrink: 0; }

  #ab .hero-name { font-family: 'DM Serif Display', serif; font-size: clamp(1.7rem,5vw,2.2rem); line-height: 1.1; color: #1a1a1a; letter-spacing: -0.02em; margin-bottom: 0.4rem; }
  #ab .hero-role { font-size: 0.82rem; color: #888; font-weight: 300; margin-bottom: 1rem; }
  #ab .hero-bio { font-size: 0.9rem; color: #444; font-weight: 300; line-height: 1.85; }

  #ab .hero-photo { width: 88px; height: 88px; border-radius: 4px; object-fit: cover; border: 1px solid #e8e8e8; display: block; background: #f0f0ee; }

  #ab .meta-row { display: flex; flex-wrap: wrap; gap: 0.4rem; margin-bottom: 2rem; }
  #ab .meta-pill { display: inline-flex; align-items: center; gap: 0.35rem; font-size: 0.75rem; font-weight: 300; color: #555; background: #fff; border: 1px solid #e8e8e8; border-radius: 2px; padding: 0.3rem 0.7rem; }
  #ab .meta-pill .dot { width: 6px; height: 6px; border-radius: 50%; background: #27ae60; flex-shrink: 0; animation: pulse 2.5s ease-in-out infinite; }
  @keyframes pulse { 0%,100%{ opacity:1 } 50%{ opacity:0.3 } }

  #ab .sec { margin-bottom: 2rem; padding-bottom: 2rem; border-bottom: 1px solid #e8e8e8; opacity: 0; transform: translateY(10px); transition: opacity 0.4s ease, transform 0.4s ease; }
  #ab .sec.on { opacity: 1; transform: translateY(0); }
  #ab .sec:last-child { border-bottom: none; margin-bottom: 0; padding-bottom: 0; }
  #ab .sc-lbl { font-size: 0.6rem; text-transform: uppercase; letter-spacing: 0.13em; font-weight: 500; color: #aaa; display: block; margin-bottom: 1rem; }

  #ab .why p { font-size: 0.9rem; line-height: 1.85; font-weight: 300; color: #444; margin-bottom: 0.75rem; }
  #ab .why p:last-child { margin-bottom: 0; }

  #ab .tools { display: flex; flex-wrap: wrap; gap: 0.45rem; }
  #ab .tool { background: #fff; border: 1px solid #e8e8e8; border-radius: 3px; padding: 0.55rem 0.75rem; display: flex; align-items: center; gap: 0.45rem; opacity: 0; transform: translateY(5px); transition: opacity 0.3s ease, transform 0.3s ease, border-color 0.15s, box-shadow 0.15s; }
  #ab .tool.on { opacity: 1; transform: translateY(0); }
  #ab .tool:hover { border-color: #bbb; box-shadow: 0 2px 8px rgba(0,0,0,0.06); }
  #ab .tool img { width: 18px; height: 18px; object-fit: contain; display: block; }
  #ab .tool span { font-size: 0.75rem; font-weight: 400; color: #555; }

  #ab .tags { display: flex; flex-wrap: wrap; gap: 0.35rem; margin-bottom: 0.65rem; }
  #ab .tag { font-size: 0.73rem; padding: 0.25rem 0.65rem; border: 1px solid #e8e8e8; border-radius: 2px; background: #fff; color: #888; cursor: pointer; font-weight: 300; user-select: none; transition: all 0.15s; }
  #ab .tag:hover, #ab .tag.on { background: #1a1a1a; color: #fff; border-color: #1a1a1a; }
  #ab .tip { font-size: 0.76rem; color: #c0392b; font-style: italic; font-weight: 300; min-height: 1.2rem; display: block; }

  #ab .favs { display: grid; grid-template-columns: 1fr 1fr; gap: 0; }
  #ab .fav { padding: 0.65rem 0.75rem 0.65rem 0; border-bottom: 1px solid #f0f0ee; display: flex; flex-direction: column; gap: 0.1rem; }
  #ab .fav:nth-child(even) { padding-left: 0.75rem; border-left: 1px solid #f0f0ee; }
  #ab .fcat { font-size: 0.55rem; text-transform: uppercase; letter-spacing: 0.11em; font-weight: 500; color: #ccc; }
  #ab .fval { font-size: 0.85rem; font-weight: 400; color: #1a1a1a; }

  #ab .lks { display: flex; flex-wrap: wrap; gap: 0.5rem; }
  #ab a.btn { font-family: 'DM Sans', sans-serif; font-size: 0.78rem; font-weight: 400; text-decoration: none; padding: 0.5rem 1rem; border-radius: 2px; transition: all 0.15s; letter-spacing: 0.02em; display: inline-block; }
  #ab a.btn-p { background: #1a1a1a; color: #fff; border: 1px solid #1a1a1a; }
  #ab a.btn-p:hover { background: #333; }
  #ab a.btn-s { background: transparent; color: #1a1a1a; border: 1px solid #e8e8e8; }
  #ab a.btn-s:hover { border-color: #1a1a1a; }

  @media (max-width: 500px) {
    #ab .hero { grid-template-columns: 1fr; }
    #ab .hero-photo { width: 72px; height: 72px; order: -1; }
    #ab .favs { grid-template-columns: 1fr; }
    #ab .fav:nth-child(even) { padding-left: 0; border-left: none; }
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
          I study data because I've always wanted to understand the story
          behind the numbers — starting with soccer stats as a kid, now
          building analytics projects across sports, business, and culture.
          I pair that with a Sports Communication minor because data without
          storytelling is just noise.
        </p>
      </div>
      <img class="hero-photo" src="/assets/images/headshot.jpg" alt="Manuel Tovar" loading="lazy" width="88" height="88"/>
    </div>

    <div class="meta-row">
      <span class="meta-pill">📍 Chicago, IL</span>
      <span class="meta-pill"><span class="dot"></span>Open to internships</span>
      <span class="meta-pill">⚽ Manchester United</span>
      <span class="meta-pill">Minor: Sports Communication</span>
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
        <div class="tool"><img src="https://upload.wikimedia.org/wikipedia/commons/c/cf/New_Power_BI_Logo.svg" alt="Power BI" width="18" height="18"><span>Power BI</span></div>
        <div class="tool"><img src="https://upload.wikimedia.org/wikipedia/commons/4/4b/Tableau_Logo.png" alt="Tableau" width="18" height="18"><span>Tableau</span></div>
        <div class="tool"><img src="https://upload.wikimedia.org/wikipedia/commons/3/34/Microsoft_Office_Excel_%282019%E2%80%93present%29.svg" alt="Excel" width="18" height="18"><span>Excel</span></div>
        <div class="tool"><img src="https://upload.wikimedia.org/wikipedia/commons/1/1b/R_logo.svg" alt="R" width="18" height="18"><span>R</span></div>
        <div class="tool"><img src="https://upload.wikimedia.org/wikipedia/commons/8/87/Sql_data_base_with_logo.png" alt="SQL" width="18" height="18"><span>SQL</span></div>
        <div class="tool"><img src="https://upload.wikimedia.org/wikipedia/commons/c/c3/Python-logo-notext.svg" alt="Python" width="18" height="18"><span>Python</span></div>
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
      tip.textContent = tag.dataset.tip || '';
    });
    tag.addEventListener('mouseleave', function(){ tag.classList.remove('on'); tip.textContent=''; });
  });
})();
</script>
