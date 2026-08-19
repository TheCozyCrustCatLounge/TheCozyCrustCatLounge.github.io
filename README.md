# thecozycrustcatlounge.github.io 
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>The Cozy Crust Cat Lounge — Cat Café</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,400;0,9..144,600;0,9..144,700;1,9..144,500&family=Nunito+Sans:wght@400;600;700;800&family=Space+Mono:wght@400;700&display=swap" rel="stylesheet">
<style>
  :root{
    --blush:#f3d9d0;
    --cream:#fff9f2;
    --plum:#4a2536;
    --ink:#2b1e22;
    --mustard:#e4a94a;
    --sage:#6b9080;
    --sage-dark:#4f6f61;
    --line: rgba(74,37,54,0.18);
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background:var(--blush);
    color:var(--ink);
    font-family:'Nunito Sans', sans-serif;
    -webkit-font-smoothing:antialiased;
  }
  h1,h2,h3{
    font-family:'Fraunces', serif;
    margin:0;
    color:var(--plum);
  }
  .eyebrow{
    font-family:'Space Mono', monospace;
    font-size:0.72rem;
    letter-spacing:0.18em;
    text-transform:uppercase;
    color:var(--sage-dark);
  }
  a{color:inherit;}
  img{display:block; max-width:100%;}

  /* ---------- Nav ---------- */
  nav{
    position:sticky; top:0; z-index:50;
    display:flex; align-items:center; justify-content:space-between;
    padding:1.1rem 6%;
    background:rgba(243,217,208,0.88);
    backdrop-filter: blur(8px);
    border-bottom:1px solid var(--line);
  }
  .brand{
    font-family:'Fraunces', serif;
    font-weight:600;
    font-size:1.3rem;
    display:flex; align-items:center; gap:0.5rem;
    color:var(--plum);
  }
  .brand svg{width:26px; height:26px;}
  .nav-links{display:flex; gap:2rem; list-style:none; margin:0; padding:0;}
  .nav-links a{
    text-decoration:none; font-weight:700; font-size:0.92rem;
    color:var(--plum); position:relative; padding-bottom:3px;
  }
  .nav-links a::after{
    content:""; position:absolute; left:0; bottom:0; height:2px; width:0;
    background:var(--mustard); transition:width .25s ease;
  }
  .nav-links a:hover::after{width:100%;}
  .nav-toggle{display:none; background:none; border:none; cursor:pointer;}

  /* ---------- Hero ---------- */
  .hero{
    position:relative;
    padding:5.5rem 6% 7rem;
    overflow:hidden;
    display:grid; grid-template-columns: 1.1fr 0.9fr; gap:2rem; align-items:center;
  }
  .hero-copy h1{
    font-size:clamp(2.6rem, 5vw, 4.4rem);
    line-height:1.02;
    font-weight:700;
  }
  .hero-copy .accent-word{
    font-style:italic; font-weight:500; color:var(--sage-dark);
    position:relative;
  }
  .hero-copy p{
    max-width:36ch;
    font-size:1.08rem;
    line-height:1.6;
    margin-top:1.3rem;
    color:var(--ink);
  }
  .hero-actions{display:flex; gap:1rem; margin-top:2.1rem; flex-wrap:wrap;}
  .btn{
    display:inline-flex; align-items:center; gap:0.5rem;
    padding:0.85rem 1.5rem;
    border-radius:100px;
    font-weight:800; font-size:0.95rem;
    text-decoration:none;
    border:2px solid var(--plum);
    transition: transform .18s ease, background .18s ease, color .18s ease;
  }
  .btn-solid{background:var(--plum); color:var(--cream);}
  .btn-solid:hover{transform:translateY(-2px); background:var(--ink);}
  .btn-outline{background:transparent; color:var(--plum);}
  .btn-outline:hover{transform:translateY(-2px); background:var(--plum); color:var(--cream);}

  .hero-art{ position:relative; height:420px; }
  .cat-hero-svg{ width:100%; height:100%; }

  .paw-trail{
    display:flex; justify-content:center; gap:2.4rem; padding:0 6% 2.5rem;
    opacity:0.55;
  }
  .paw-trail svg{width:20px; height:20px;}
  .paw-trail svg:nth-child(even){ transform: translateY(10px) rotate(12deg); }
  .paw-trail svg:nth-child(odd){ transform: rotate(-10deg); }

  section{padding:5rem 6%;}
  .section-head{ max-width:640px; margin:0 auto 3rem; text-align:center;}
  .section-head h2{
    font-size:clamp(2rem, 3.4vw, 2.8rem);
    margin-top:0.5rem;
    font-weight:600;
  }
  .section-head p{ margin-top:0.9rem; color:var(--plum); opacity:0.85; line-height:1.6;}
  .underline{
    display:inline-block; position:relative;
  }
  .underline svg{
    position:absolute; left:0; bottom:-8px; width:100%; height:10px;
  }

  /* ---------- About teaser ---------- */
  .about-teaser{
    background:var(--cream);
    border-top:1px solid var(--line);
    border-bottom:1px solid var(--line);
  }
  .teaser-grid{
    max-width:1000px; margin:0 auto;
    display:grid; grid-template-columns: repeat(3,1fr); gap:2rem;
    text-align:center;
  }
  .teaser-grid .item svg{ width:38px; height:38px; margin:0 auto 1rem; color:var(--sage-dark); }
  .teaser-grid h3{ font-size:1.15rem; font-weight:600;}
  .teaser-grid p{ font-size:0.92rem; color:var(--ink); opacity:0.8; margin-top:0.4rem; line-height:1.5;}

  /* ---------- Menu ---------- */
  #menu{ max-width:1000px; margin:0 auto; }
  .menu-tabs{
    display:flex; justify-content:center; gap:0.6rem; margin-bottom:2.6rem; flex-wrap:wrap;
  }
  .menu-tab{
    font-family:'Space Mono', monospace; font-size:0.78rem; letter-spacing:0.06em;
    padding:0.5rem 1.1rem; border-radius:100px; border:1.5px solid var(--plum);
    background:transparent; color:var(--plum); cursor:pointer; text-transform:uppercase;
    transition:.2s;
  }
  .menu-tab.active, .menu-tab:hover{ background:var(--plum); color:var(--cream); }
  .menu-group{ display:none; }
  .menu-group.active{ display:block; animation:fade .4s ease; }
  @keyframes fade{ from{opacity:0; transform:translateY(6px);} to{opacity:1; transform:none;} }
  .menu-row{
    display:flex; justify-content:space-between; align-items:baseline;
    padding:1.15rem 0; border-bottom:1px dashed var(--line);
    gap:1rem;
  }
  .menu-row:last-child{border-bottom:none;}
  .menu-row .name{ font-family:'Fraunces', serif; font-weight:600; font-size:1.15rem; }
  .menu-row .desc{ font-size:0.9rem; opacity:0.75; margin-top:0.2rem; max-width:46ch;}
  .menu-row .price{ font-family:'Space Mono', monospace; font-weight:700; color:var(--sage-dark); white-space:nowrap;}

  /* ---------- Cats ---------- */
  .cats-note{
    max-width:560px; margin:0 auto 3rem; text-align:center;
    background:var(--cream); border:1px dashed var(--sage-dark);
    padding:1rem 1.4rem; border-radius:14px; font-size:0.92rem; color:var(--sage-dark); font-weight:700;
  }
  .cat-grid{
    display:grid; grid-template-columns:repeat(auto-fit,minmax(230px,1fr));
    gap:2.2rem; max-width:1100px; margin:0 auto;
  }
  .cat-card{
    background:var(--cream);
    border-radius:16px;
    padding:1rem 1rem 1.4rem;
    box-shadow: 0 10px 24px rgba(74,37,54,0.08);
    transform:rotate(var(--tilt,0deg));
    transition:transform .25s ease, box-shadow .25s ease;
    position:relative;
  }
  .cat-card:hover{ transform:rotate(0deg) translateY(-6px); box-shadow:0 16px 30px rgba(74,37,54,0.16); }
  .cat-card:nth-child(1){--tilt:-2deg;}
  .cat-card:nth-child(2){--tilt:1.5deg;}
  .cat-card:nth-child(3){--tilt:-1deg;}
  .cat-card:nth-child(4){--tilt:2deg;}
  .cat-card:nth-child(5){--tilt:-1.5deg;}
  .cat-card:nth-child(6){--tilt:1deg;}
  .cat-portrait{
    background: var(--blush);
    border-radius:10px; height:170px;
    display:flex; align-items:center; justify-content:center; margin-bottom:1rem;
    overflow:hidden;
  }
  .cat-portrait svg{ width:78%; height:78%; }
  .cat-card h3{ font-size:1.2rem; display:flex; align-items:center; gap:0.4rem;}
  .cat-tag{
    font-family:'Space Mono', monospace; font-size:0.68rem; color:var(--sage-dark);
    text-transform:uppercase; letter-spacing:0.05em; margin-top:0.15rem; display:block;
  }
  .cat-card p{ font-size:0.88rem; line-height:1.5; margin-top:0.6rem; opacity:0.85;}

  /* ---------- About / location ---------- */
  #about{ background:var(--plum); color:var(--cream); }
  #about .section-head h2, #about .section-head p{ color:var(--cream); }
  #about .section-head p{ opacity:0.85; }
  .about-grid{
    max-width:1000px; margin:0 auto; display:grid;
    grid-template-columns: 1fr 1fr; gap:3rem;
  }
  .about-story p{ line-height:1.75; margin-bottom:1rem; opacity:0.92; }
  .hours-card{
    background:rgba(255,249,242,0.06);
    border:1px solid rgba(255,249,242,0.2);
    border-radius:16px; padding:1.8rem;
  }
  .hours-card h3{ color:var(--cream); font-size:1.1rem; margin-bottom:1rem;}
  .hours-row{ display:flex; justify-content:space-between; font-size:0.92rem; padding:0.45rem 0; border-bottom:1px solid rgba(255,249,242,0.12);}
  .hours-row:last-child{border:none;}
  .addr{ margin-top:1.6rem; font-size:0.92rem; line-height:1.7; opacity:0.85;}
  .addr .eyebrow{ color:var(--mustard); }

  footer{
    background:var(--ink); color:rgba(255,249,242,0.6);
    text-align:center; padding:2.2rem 6%; font-size:0.85rem;
  }
  footer strong{ color:var(--cream); }

  @media (max-width: 860px){
    .hero{ grid-template-columns:1fr; padding-top:3.5rem; text-align:center;}
    .hero-copy p{ margin-left:auto; margin-right:auto; }
    .hero-actions{ justify-content:center; }
    .hero-art{ height:280px; order:-1; }
    .nav-links{
      position:fixed; top:64px; right:0; height:calc(100vh - 64px); width:70%;
      background:var(--cream); flex-direction:column; padding:2.5rem 2rem;
      transform:translateX(100%); transition:transform .3s ease;
    }
    .nav-links.open{ transform:translateX(0); }
    .nav-toggle{ display:block; }
    .teaser-grid{ grid-template-columns:1fr; gap:2.4rem; }
    .about-grid{ grid-template-columns:1fr; }
  }
  @media (prefers-reduced-motion: reduce){
    html{scroll-behavior:auto;}
    *{transition:none !important; animation:none !important;}
  }
  :focus-visible{ outline:3px solid var(--mustard); outline-offset:2px; }
</style>
</head>
<body>

<nav>
  <div class="brand">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M4 9c0-3 2-5 3-5s1 2 1 3M20 9c0-3-2-5-3-5s-1 2-1 3M4 9c0 6 3 10 8 10s8-4 8-10c-2 1-4 2-8 2s-6-1-8-2Z"/><circle cx="9.5" cy="10.5" r=".6" fill="currentColor"/><circle cx="14.5" cy="10.5" r=".6" fill="currentColor"/></svg>
    The Cozy Crust Cat Lounge
  </div>
  <button class="nav-toggle" aria-label="Toggle menu" onclick="document.querySelector('.nav-links').classList.toggle('open')">
    <svg width="26" height="26" viewBox="0 0 24 24" fill="none" stroke="#4a2536" stroke-width="2"><path d="M3 6h18M3 12h18M3 18h18"/></svg>
  </button>
  <ul class="nav-links">
    <li><a href="#menu">Menu</a></li>
    <li><a href="#cats">House Cats</a></li>
    <li><a href="#about">About &amp; Location</a></li>
    <li><a href="#reserve">Lounge Passes</a></li>
  </ul>
</nav>

<header class="hero">
  <div class="hero-copy">
    <p class="eyebrow">Coffee, kitchen &amp; company — opening June 2027</p>
    <h1>Good food, <span class="accent-word">better</span> company.</h1>
    <p>A full kitchen up front and a house full of resident cats in the back. Come for the menu, stay because eleven cats have decided you're not leaving yet.</p>
    <div class="hero-actions">
      <a href="#menu" class="btn btn-solid">See the menu</a>
      <a href="#cats" class="btn btn-outline">Meet the cats</a>
    </div>
  </div>
  <div class="hero-art">
    <svg class="cat-hero-svg" viewBox="0 0 400 400" fill="none">
      <ellipse cx="200" cy="330" rx="150" ry="18" fill="#4a2536" opacity="0.08"/>
      <g stroke="#4a2536" stroke-width="4" stroke-linejoin="round" stroke-linecap="round">
        <path d="M120 250 C110 160 150 90 200 90 C250 90 290 160 280 250 C280 300 240 320 200 320 C160 320 120 300 120 250Z" fill="#e4a94a" opacity="0.9"/>
        <path d="M140 110 L120 60 L165 95Z" fill="#e4a94a"/>
        <path d="M260 110 L280 60 L235 95Z" fill="#e4a94a"/>
        <path d="M148 100 L134 72 L162 92Z" fill="#f3d9d0"/>
        <path d="M252 100 L266 72 L238 92Z" fill="#f3d9d0"/>
        <circle cx="168" cy="175" r="7" fill="#4a2536" stroke="none"/>
        <circle cx="232" cy="175" r="7" fill="#4a2536" stroke="none"/>
        <path d="M195 195 L205 195 L200 205Z" fill="#4a2536" stroke="none"/>
        <path d="M200 208 C190 220 210 220 200 208Z"/>
        <path d="M160 200 C120 195 90 205 70 195M160 210 C120 215 90 225 75 235" opacity="0.6"/>
        <path d="M240 200 C280 195 310 205 330 195M240 210 C280 215 310 225 325 235" opacity="0.6"/>
      </g>
      <ellipse cx="150" cy="150" rx="10" ry="16" fill="#f3d9d0" opacity="0.5"/>
      <ellipse cx="250" cy="150" rx="10" ry="16" fill="#f3d9d0" opacity="0.5"/>
    </svg>
  </div>
</header>

<div class="paw-trail" aria-hidden="true">
  <svg viewBox="0 0 24 24" fill="#4a2536"><circle cx="12" cy="15" r="5"/><circle cx="5" cy="7" r="2.2"/><circle cx="10" cy="4" r="2.2"/><circle cx="14" cy="4" r="2.2"/><circle cx="19" cy="7" r="2.2"/></svg>
  <svg viewBox="0 0 24 24" fill="#4a2536"><circle cx="12" cy="15" r="5"/><circle cx="5" cy="7" r="2.2"/><circle cx="10" cy="4" r="2.2"/><circle cx="14" cy="4" r="2.2"/><circle cx="19" cy="7" r="2.2"/></svg>
  <svg viewBox="0 0 24 24" fill="#4a2536"><circle cx="12" cy="15" r="5"/><circle cx="5" cy="7" r="2.2"/><circle cx="10" cy="4" r="2.2"/><circle cx="14" cy="4" r="2.2"/><circle cx="19" cy="7" r="2.2"/></svg>
  <svg viewBox="0 0 24 24" fill="#4a2536"><circle cx="12" cy="15" r="5"/><circle cx="5" cy="7" r="2.2"/><circle cx="10" cy="4" r="2.2"/><circle cx="14" cy="4" r="2.2"/><circle cx="19" cy="7" r="2.2"/></svg>
  <svg viewBox="0 0 24 24" fill="#4a2536"><circle cx="12" cy="15" r="5"/><circle cx="5" cy="7" r="2.2"/><circle cx="10" cy="4" r="2.2"/><circle cx="14" cy="4" r="2.2"/><circle cx="19" cy="7" r="2.2"/></svg>
</div>

<section class="about-teaser">
  <div class="teaser-grid">
    <div class="item">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M3 12h4l3 8 4-16 3 8h4"/></svg>
      <h3>Real kitchen</h3>
      <p>Made-to-order breakfast and lunch, cooked in a kitchen fully separate from the cats — every time.</p>
    </div>
    <div class="item">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M4 9c0-3 2-5 3-5s1 2 1 3M20 9c0-3-2-5-3-5s-1 2-1 3M4 9c0 6 3 10 8 10s8-4 8-10c-2 1-4 2-8 2s-6-1-8-2Z"/></svg>
      <h3>A house full of cats</h3>
      <p>Our resident cats live here full-time. They're part of the family, not up for adoption — just good company.</p>
    </div>
    <div class="item">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><circle cx="12" cy="12" r="9"/><path d="M12 7v5l3 3"/></svg>
      <h3>Sit and stay a while</h3>
      <p>No rush. Order, settle in, and let a cat decide where the rest of your afternoon goes.</p>
    </div>
  </div>
</section>

<section id="menu">
  <div class="section-head">
    <p class="eyebrow">On the table</p>
    <h2 class="underline">The menu
      <svg viewBox="0 0 200 10" preserveAspectRatio="none"><path d="M2 8 C50 2, 150 2, 198 8" stroke="#e4a94a" stroke-width="4" fill="none" stroke-linecap="round"/></svg>
    </h2>
    <p>A short, kitchen-driven menu — built small on purpose so everything comes out fresh.</p>
  </div>

  <div class="menu-tabs">
    <button class="menu-tab active" data-target="breakfast">Morning Comforts</button>
    <button class="menu-tab" data-target="lunch">All-Day Eats</button>
    <button class="menu-tab" data-target="drinks">Cold Drinks</button>
  </div>

  <div class="menu-group active" id="breakfast">
    <div class="menu-row"><div><div class="name">Pancake</div><div class="desc">Served warm with syrup</div></div><div class="price">$4.28</div></div>
    <div class="menu-row"><div><div class="name">Pancakes (2)</div><div class="desc">Served warm with syrup</div></div><div class="price">$7.49</div></div>
    <div class="menu-row"><div><div class="name">Bread Roll</div><div class="desc">Fresh baked, served warm</div></div><div class="price">$2.14</div></div>
    <div class="menu-row"><div><div class="name">Bread Rolls (4)</div><div class="desc">Fresh baked, served warm</div></div><div class="price">$3.21</div></div>
    <div class="menu-row"><div><div class="name">Chocolate Donut</div><div class="desc">Fresh daily</div></div><div class="price">$2.14</div></div>
    <div class="menu-row"><div><div class="name">Chocolate Donuts (6)</div><div class="desc">Fresh daily</div></div><div class="price">$12.84</div></div>
    <div class="menu-row"><div><div class="name">Vanilla Donut</div><div class="desc">Fresh daily</div></div><div class="price">$2.14</div></div>
    <div class="menu-row"><div><div class="name">Vanilla Donuts (6)</div><div class="desc">Fresh daily</div></div><div class="price">$12.84</div></div>
  </div>

  <div class="menu-group" id="lunch">
    <div class="menu-row"><div><div class="name">Dad's Legendary Pepperoni Roll</div><div class="desc">Baked fresh on-site, a West Virginia classic</div></div><div class="price">$2.14</div></div>
    <div class="menu-row"><div><div class="name">Dad's Legendary Pepperoni Rolls (2)</div><div class="desc">Baked fresh on-site, a West Virginia classic</div></div><div class="price">$4.28</div></div>
    <div class="menu-row"><div><div class="name">Deep Dish Personal Pizza — Cheese</div><div class="desc">Individual 5-inch thick-crust</div></div><div class="price">$6.42</div></div>
    <div class="menu-row"><div><div class="name">Deep Dish Personal Pizza — Pepperoni</div><div class="desc">Individual 5-inch thick-crust</div></div><div class="price">$7.49</div></div>
    <div class="menu-row"><div><div class="name">Assorted Chips</div><div class="desc">Single-serve bags</div></div><div class="price">$1.61</div></div>
  </div>

  <div class="menu-group" id="drinks">
    <div class="menu-row"><div><div class="name">Bottled Water</div><div class="desc">Chilled</div></div><div class="price">$2.14</div></div>
  </div>

  <div style="max-width:640px; margin:2.4rem auto 0; background:var(--cream); border:1px dashed var(--sage-dark); border-radius:14px; padding:1.1rem 1.4rem; font-size:0.85rem; color:var(--ink); opacity:0.85; line-height:1.6; text-align:center;">
    Menu prices already include local sales tax — the odd cents cover that, not us. We're a 100% card-only, cash-free lounge.
  </div>
</section>

<section id="cats">
  <div class="section-head">
    <p class="eyebrow">The regulars</p>
    <h2 class="underline">Meet the house cats
      <svg viewBox="0 0 200 10" preserveAspectRatio="none"><path d="M2 8 C50 2, 150 2, 198 8" stroke="#e4a94a" stroke-width="4" fill="none" stroke-linecap="round"/></svg>
    </h2>
    <p>Four residents, each with their own booth preferences and opinions about your lunch.</p>
  </div>
  <p class="cats-note">🐾 Our cats live here permanently and are not available for adoption — they're residents, not guests.</p>

  <div class="cat-grid">
    <div class="cat-card">
      <div class="cat-portrait">
        <svg viewBox="0 0 100 100"><ellipse cx="50" cy="60" rx="34" ry="28" fill="#f3d9d0" stroke="#4a2536" stroke-width="2"/><path d="M28 40 L20 20 L40 35Z" fill="#f3d9d0" stroke="#4a2536" stroke-width="2"/><path d="M72 40 L80 20 L60 35Z" fill="#f3d9d0" stroke="#4a2536" stroke-width="2"/><path d="M40 45 q10 -8 20 0 q-6 10 -20 0Z" fill="#e4a94a"/><path d="M60 70 q10 4 8 15" fill="none" stroke="#2b1e22" stroke-width="3"/><circle cx="40" cy="55" r="4" fill="#4a2536"/><circle cx="60" cy="55" r="4" fill="#4a2536"/></svg>
      </div>
      <h3>Biscuit <span aria-hidden="true">🐾</span></h3>
      <span class="cat-tag">Window Booth, table 3 · Calico kitten</span>
      <p>Self-appointed greeter. Inspects your bag the moment you sit down.</p>
    </div>
    <div class="cat-card">
      <div class="cat-portrait">
        <svg viewBox="0 0 100 100"><ellipse cx="50" cy="60" rx="34" ry="28" fill="#e4a94a"/><path d="M28 40 L20 20 L40 35Z" fill="#e4a94a"/><path d="M72 40 L80 20 L60 35Z" fill="#e4a94a"/><circle cx="40" cy="55" r="4" fill="#4a2536"/><circle cx="60" cy="55" r="4" fill="#4a2536"/></svg>
      </div>
      <h3>Marmalade <span aria-hidden="true">🐾</span></h3>
      <span class="cat-tag">Sunny corner, all day · Orange tabby</span>
      <p>Professional napper. Located wherever the sun is hitting.</p>
    </div>
    <div class="cat-card">
      <div class="cat-portrait">
        <svg viewBox="0 0 100 100"><ellipse cx="50" cy="60" rx="34" ry="28" fill="#2b1e22"/><path d="M28 40 L20 20 L40 35Z" fill="#2b1e22"/><path d="M72 40 L80 20 L60 35Z" fill="#2b1e22"/><circle cx="40" cy="55" r="4" fill="#e4a94a"/><circle cx="60" cy="55" r="4" fill="#e4a94a"/></svg>
      </div>
      <h3>Pepper <span aria-hidden="true">🐾</span></h3>
      <span class="cat-tag">Bookshelf, top row · Black cat</span>
      <p>Watches the whole room from above. Rarely comes down before noon.</p>
    </div>
    <div class="cat-card">
      <div class="cat-portrait">
        <svg viewBox="0 0 100 100"><ellipse cx="50" cy="60" rx="36" ry="30" fill="#6b9080"/><path d="M28 40 L20 20 L40 35Z" fill="#6b9080"/><path d="M72 40 L80 20 L60 35Z" fill="#6b9080"/><path d="M35 48 q8 -6 16 0Z" fill="#4a2536" opacity="0.4"/><path d="M55 65 q10 -5 18 3Z" fill="#4a2536" opacity="0.4"/><circle cx="40" cy="55" r="4" fill="#fff9f2"/><circle cx="60" cy="55" r="4" fill="#fff9f2"/></svg>
      </div>
      <h3>Waffle <span aria-hidden="true">🐾</span></h3>
      <span class="cat-tag">Under the counter · Grey tortie</span>
      <p>Chunky and convinced the kitchen space is a personal heater. Mostly correct.</p>
    </div>
  </div>
</section>

<section id="about">
  <div class="section-head">
    <p class="eyebrow">Our story</p>
    <h2 class="underline">About &amp; location
      <svg viewBox="0 0 200 10" preserveAspectRatio="none"><path d="M2 8 C50 2, 150 2, 198 8" stroke="#e4a94a" stroke-width="4" fill="none" stroke-linecap="round"/></svg>
    </h2>
  </div>
  <div class="about-grid">
    <div class="about-story">
      <p>The Cozy Crust Cat Lounge started with a simple idea: a restaurant that's genuinely good on its own, in a building that happens to be home to six cats.</p>
      <p>The dining room sits right up front — cozy tables, an open counter where you order, no cat hair in sight. Seating is kept small on purpose: two four-person tables and two two-person tables, twelve seats total, for a calm, low-stress room. Food comes from a fully separate back kitchen, walled off behind the counter.</p>
      <p>The cats live next door, in their own room with its own door. Grab your food, then head over and step into cat paradise whenever you're ready. Two rooms, two purposes, no crossover.</p>
      <p>They're residents, not rescues waiting on adoption. This is simply where they live, and you're welcome to visit.</p>
    </div>
    <div class="hours-card">
      <h3>Hours</h3>
      <div class="hours-row"><span>Mon, Wed, Fri</span><span>9:00am – 3:00pm</span></div>
      <div class="hours-row"><span>(Staff lunch break)</span><span>12:30 – 1:00pm</span></div>
      <div class="hours-row"><span>Tue, Thu, Sat, Sun</span><span>Closed to the public</span></div>
      <p style="font-size:0.85rem; opacity:0.75; margin:0.9rem 0 0;">Cards and mobile tap only — we're a cash-free lounge.</p>
      <div class="addr">
        <p class="eyebrow">Find us</p>
        417 Holland Ave, Suite 2<br>
        Westover, WV 26501<br>
        brycepheasant@icloud.com
      </div>
    </div>
  </div>
</section>

<section id="reserve" style="background:var(--cream); border-top:1px solid var(--line);">
  <div class="section-head">
    <p class="eyebrow">Plan your visit</p>
    <h2 class="underline">Cat lounge time passes
      <svg viewBox="0 0 200 10" preserveAspectRatio="none"><path d="M2 8 C50 2, 150 2, 198 8" stroke="#e4a94a" stroke-width="4" fill="none" stroke-linecap="round"/></svg>
    </h2>
    <p>Pick how long you'd like to spend in the cat lounge. Open Mondays, Wednesdays, and Fridays, 9am–3pm (staff lunch break 12:30–1pm).</p>
  </div>
  <div style="max-width:420px; margin:0 auto 2.4rem; display:flex; flex-direction:column; gap:0.6rem;">
    <div class="menu-row"><div><div class="name">30-Minute Scurry Pass</div></div><div class="price">$6.42</div></div>
    <div class="menu-row"><div><div class="name">60-Minute Snuggle Pass</div></div><div class="price">$10.70</div></div>
    <div class="menu-row"><div><div class="name">90-Minute Sanctuary Pass</div></div><div class="price">$14.98</div></div>
  </div>
  <form id="reserve-form" style="max-width:420px; margin:0 auto; display:flex; flex-direction:column; gap:1rem;">
    <label style="font-weight:700; font-size:0.9rem;">Date
      <input type="date" id="reserve-date" name="Date" required style="width:100%; padding:0.7rem; margin-top:0.4rem; border-radius:8px; border:1.5px solid var(--plum); font-family:'Nunito Sans', sans-serif; font-size:1rem;">
    </label>
    <label style="font-weight:700; font-size:0.9rem;">Arrival time
      <select id="reserve-time" name="Arrival Time" required style="width:100%; padding:0.7rem; margin-top:0.4rem; border-radius:8px; border:1.5px solid var(--plum); font-family:'Nunito Sans', sans-serif; font-size:1rem;">
        <option value="">Select a time</option>
        <option>9:00 AM</option>
        <option>10:00 AM</option>
        <option>11:00 AM</option>
        <option>1:00 PM</option>
        <option>2:00 PM</option>
      </select>
    </label>
    <label style="font-weight:700; font-size:0.9rem;">Pass length
      <select id="reserve-pass" name="Pass" required style="width:100%; padding:0.7rem; margin-top:0.4rem; border-radius:8px; border:1.5px solid var(--plum); font-family:'Nunito Sans', sans-serif; font-size:1rem;">
        <option value="">Select a pass</option>
        <option>30-Minute Scurry Pass — $6.42</option>
        <option>60-Minute Snuggle Pass — $10.70</option>
        <option>90-Minute Sanctuary Pass — $14.98</option>
      </select>
    </label>
    <label style="font-weight:700; font-size:0.9rem;">Your name
      <input type="text" id="reserve-name" name="Name" required style="width:100%; padding:0.7rem; margin-top:0.4rem; border-radius:8px; border:1.5px solid var(--plum); font-family:'Nunito Sans', sans-serif; font-size:1rem;">
    </label>
    <button type="submit" class="btn btn-solid" style="justify-content:center;">Request lounge time</button>
    <p style="text-align:center; font-size:0.85rem; opacity:0.75; margin:0;">Cards and mobile tap only when you arrive — we're a cash-free lounge.</p>
  </form>
</section>

<footer>
  <strong>The Cozy Crust Cat Lounge</strong> — good food, resident cats, no rush. Opening June 2027.
</footer>

<script>
  document.querySelectorAll('.menu-tab').forEach(tab => {
    tab.addEventListener('click', () => {
      document.querySelectorAll('.menu-tab').forEach(t => t.classList.remove('active'));
      document.querySelectorAll('.menu-group').forEach(g => g.classList.remove('active'));
      tab.classList.add('active');
      document.getElementById(tab.dataset.target).classList.add('active');
    });
  });

  // Cat lounge pass request: only Mon/Wed/Fri are open to the public, submissions email the owner
  document.getElementById('reserve-form').addEventListener('submit', function(e){
    e.preventDefault();
    const dateVal = document.getElementById('reserve-date').value;
    if(!dateVal){ return; }
    const chosenDay = new Date(dateVal + 'T00:00:00').getDay(); // 0=Sun ... 6=Sat
    const openDays = [1, 3, 5]; // Mon, Wed, Fri
    if(!openDays.includes(chosenDay)){
      alert('The Lounge is closed to the public on this day to give our resident cats a peaceful vacation!');
      return;
    }
    const form = this;
    const submitBtn = form.querySelector('button[type="submit"]');
    submitBtn.disabled = true;
    submitBtn.textContent = 'Sending...';

    fetch('https://formsubmit.co/ajax/brycepheasant@icloud.com', {
      method: 'POST',
      headers: { 'Accept': 'application/json' },
      body: new FormData(form)
    })
    .then(res => res.json())
    .then(() => {
      alert('Thanks! Your request has been sent — remember, we\'re cards/tap only. See you soon!');
      form.reset();
    })
    .catch(() => {
      alert('Sorry, something went wrong sending your request. Please try again or reach out directly.');
    })
    .finally(() => {
      submitBtn.disabled = false;
      submitBtn.textContent = 'Request lounge time';
    });
  });
</script>

</body>
</html>
