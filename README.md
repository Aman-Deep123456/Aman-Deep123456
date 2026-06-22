<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Amandeep Singh — GitHub Profile</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&family=JetBrains+Mono:wght@400;500;700&display=swap" rel="stylesheet"/>
<style>
  :root {
    --bg: #faf7f2;
    --bg2: #f3ede3;
    --surface: #ede6d8;
    --card: #ffffff;
    --border: rgba(120, 80, 20, 0.12);
    --border2: rgba(120, 80, 20, 0.07);
    --accent: #b45309;
    --accent2: #d97706;
    --accent3: #92400e;
    --teal: #0f766e;
    --blue: #1d4ed8;
    --rose: #be123c;
    --green: #15803d;
    --text: #1c1917;
    --muted: #57534e;
    --dim: #a8a29e;
    --shadow: rgba(120,80,20,0.08);
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Space Grotesk', sans-serif;
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* ── PAPER TEXTURE DOTS ── */
  .paper-bg {
    position: fixed; inset: 0;
    background-image: radial-gradient(circle, rgba(120,80,20,0.06) 1px, transparent 1px);
    background-size: 28px 28px;
    pointer-events: none; z-index: 0;
  }

  /* ── FLOATING BLOBS ── */
  .blob {
    position: fixed; border-radius: 50%; filter: blur(80px);
    pointer-events: none; z-index: 0; opacity: 0.35;
    animation: float var(--d) ease-in-out infinite;
  }
  .blob1 { width:420px;height:420px; top:-100px;right:-80px; background:radial-gradient(circle,#fde68a,#fbbf24); --d:8s; }
  .blob2 { width:320px;height:320px; bottom:100px;left:-60px; background:radial-gradient(circle,#bfdbfe,#93c5fd); --d:10s; animation-delay:-3s; }
  .blob3 { width:280px;height:280px; top:40%;right:10%; background:radial-gradient(circle,#fecaca,#fda4af); --d:12s; animation-delay:-6s; }
  @keyframes float {
    0%,100%{transform:translateY(0) scale(1);}
    50%{transform:translateY(-30px) scale(1.05);}
  }

  /* ── LAYOUT ── */
  .page { position:relative;z-index:1;max-width:960px;margin:0 auto;padding:0 24px 80px; }

  /* ── HERO ── */
  .hero { text-align:center; padding:80px 0 60px; position:relative; }

  .status-badge {
    display:inline-flex; align-items:center; gap:8px;
    background:rgba(21,128,61,0.08);
    border:1px solid rgba(21,128,61,0.25);
    color:var(--green);
    font-family:'JetBrains Mono',monospace; font-size:12px;
    padding:6px 16px; border-radius:100px; margin-bottom:28px;
    letter-spacing:0.05em;
  }
  .status-dot {
    width:7px;height:7px;background:var(--green);
    border-radius:50%; animation:blink 1.5s ease-in-out infinite;
  }
  @keyframes blink{0%,100%{opacity:1}50%{opacity:0.2}}

  .hero h1 {
    font-size:clamp(2.8rem,6vw,5rem);
    font-weight:700; line-height:1.08; letter-spacing:-0.03em;
    background:linear-gradient(135deg,#1c1917 0%,#b45309 45%,#d97706 100%);
    -webkit-background-clip:text; -webkit-text-fill-color:transparent;
    background-clip:text; margin-bottom:16px;
  }

  .hero-role {
    font-family:'JetBrains Mono',monospace; font-size:14px;
    color:var(--accent); margin-bottom:20px; letter-spacing:0.04em;
  }
  .hero-role span { color:var(--dim); }

  .hero-desc {
    font-size:16px; color:var(--muted);
    max-width:500px; margin:0 auto 36px; line-height:1.75;
  }

  /* ── TERMINAL ── */
  .terminal {
    display:inline-block;
    background:#fefce8;
    border:1px solid rgba(180,83,9,0.2);
    border-radius:14px;
    padding:20px 28px;
    text-align:left; margin-bottom:40px; min-width:380px;
    box-shadow:0 4px 24px rgba(180,83,9,0.1), 0 1px 0 rgba(255,255,255,0.8) inset;
  }
  .terminal-bar { display:flex;gap:7px;margin-bottom:14px; }
  .dot{width:12px;height:12px;border-radius:50%;}
  .dot-r{background:#ff5f57;} .dot-y{background:#febc2e;} .dot-g{background:#28c840;}
  .terminal-line {
    font-family:'JetBrains Mono',monospace; font-size:13px;
    color:var(--muted); line-height:1.9;
  }
  .terminal-line .prompt{color:#b45309;}
  .terminal-line .cmd{color:#0f766e;}
  .terminal-line .val{color:#15803d;}
  .terminal-line .key{color:#be123c;}
  #cursor {
    display:inline-block;width:9px;height:15px;
    background:var(--accent); animation:blink 1s step-end infinite;
    vertical-align:middle; margin-left:2px; border-radius:2px;
  }

  /* ── SOCIAL ── */
  .socials { display:flex;gap:10px;justify-content:center;flex-wrap:wrap; }
  .social-btn {
    display:inline-flex;align-items:center;gap:8px;
    padding:9px 18px; border-radius:8px; font-size:13px;font-weight:600;
    text-decoration:none; letter-spacing:0.02em;
    border:1px solid var(--border);
    background:var(--card);
    color:var(--text);
    transition:all 0.2s ease;
    box-shadow:0 1px 4px var(--shadow);
  }
  .social-btn:hover {
    background:var(--accent); color:#fff;
    border-color:var(--accent);
    transform:translateY(-2px);
    box-shadow:0 8px 20px rgba(180,83,9,0.25);
  }
  .social-btn svg{width:15px;height:15px;}

  /* ── SECTION ── */
  section{margin-top:64px;}
  .section-label {
    font-family:'JetBrains Mono',monospace; font-size:11px;
    text-transform:uppercase; letter-spacing:0.2em;
    color:var(--accent); margin-bottom:8px;
  }
  .section-title {
    font-size:26px;font-weight:700;color:var(--text);
    margin-bottom:28px;
    display:flex;align-items:center;gap:14px;
  }
  .section-title::after {
    content:'';flex:1;height:1px;
    background:linear-gradient(90deg,var(--border),transparent);
  }

  /* ── STAT CARDS ── */
  .stats-grid { display:grid;grid-template-columns:repeat(4,1fr);gap:14px; }
  .stat-card {
    background:var(--card);
    border:1px solid var(--border);
    border-radius:16px; padding:24px 16px; text-align:center;
    transition:all 0.3s; cursor:default;
    box-shadow:0 2px 8px var(--shadow);
    position:relative; overflow:hidden;
  }
  .stat-card::before {
    content:'';position:absolute;top:0;left:0;right:0;height:3px;
    background:var(--top);opacity:0;transition:opacity 0.3s;
  }
  .stat-card:hover{transform:translateY(-4px);box-shadow:0 12px 32px var(--shadow);}
  .stat-card:hover::before{opacity:1;}
  .stat-card[data-accent="amber"]{--top:linear-gradient(90deg,#b45309,#d97706);}
  .stat-card[data-accent="teal"]{--top:linear-gradient(90deg,#0f766e,#14b8a6);}
  .stat-card[data-accent="rose"]{--top:linear-gradient(90deg,#be123c,#f43f5e);}
  .stat-card[data-accent="blue"]{--top:linear-gradient(90deg,#1d4ed8,#3b82f6);}
  .stat-num {
    font-family:'JetBrains Mono',monospace;
    font-size:34px;font-weight:700;
    display:block;margin-bottom:6px;
  }
  .stat-card[data-accent="amber"] .stat-num{color:var(--accent);}
  .stat-card[data-accent="teal"] .stat-num{color:var(--teal);}
  .stat-card[data-accent="rose"] .stat-num{color:var(--rose);}
  .stat-card[data-accent="blue"] .stat-num{color:var(--blue);}
  .stat-label{font-size:12px;color:var(--muted);letter-spacing:0.04em;}

  /* ── ABOUT ── */
  .about-grid{display:grid;grid-template-columns:1fr 1fr;gap:16px;}
  .about-card {
    background:var(--card);border:1px solid var(--border);
    border-radius:16px;padding:28px;
    box-shadow:0 2px 8px var(--shadow);
  }
  .about-card h3 {
    font-size:11px;font-weight:600;color:var(--accent);
    margin-bottom:16px;text-transform:uppercase;
    letter-spacing:0.15em;font-family:'JetBrains Mono',monospace;
  }
  .about-card ul{list-style:none;}
  .about-card ul li {
    font-size:14px;color:var(--muted);
    padding:8px 0;border-bottom:1px solid var(--border2);
    display:flex;align-items:center;gap:10px;line-height:1.5;
  }
  .about-card ul li:last-child{border-bottom:none;}
  .about-card ul li .icon{font-size:16px;flex-shrink:0;}

  /* ── TABS ── */
  .tabs{display:flex;gap:8px;margin-bottom:18px;flex-wrap:wrap;}
  .tab {
    padding:7px 18px;border-radius:100px;font-size:13px;font-weight:500;
    border:1px solid var(--border);background:var(--card);
    color:var(--muted);cursor:pointer;transition:all 0.2s;
    font-family:'Space Grotesk',sans-serif;
    box-shadow:0 1px 3px var(--shadow);
  }
  .tab.active,.tab:hover{
    background:var(--accent);color:#fff;border-color:var(--accent);
    box-shadow:0 4px 12px rgba(180,83,9,0.25);
  }
  .tech-panel{display:none;}
  .tech-panel.active{display:flex;flex-wrap:wrap;gap:10px;}
  .tech-pill {
    display:inline-flex;align-items:center;gap:8px;
    background:var(--card);border:1px solid var(--border);
    border-radius:8px;padding:8px 14px;font-size:13px;font-weight:500;
    color:var(--text);transition:all 0.2s;cursor:default;
    box-shadow:0 1px 3px var(--shadow);
  }
  .tech-pill:hover{
    background:var(--bg2);border-color:rgba(180,83,9,0.3);
    transform:translateY(-2px);box-shadow:0 4px 12px var(--shadow);
  }
  .tech-pill img{width:18px;height:18px;object-fit:contain;}

  /* ── LEARNING ── */
  .learning-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:14px;}
  .learn-card {
    background:var(--card);border:1px solid var(--border);
    border-radius:14px;padding:22px;transition:all 0.3s;cursor:default;
    box-shadow:0 2px 8px var(--shadow);
  }
  .learn-card:hover{
    border-color:rgba(180,83,9,0.3);
    background:#fffbeb;
    transform:translateY(-3px);box-shadow:0 8px 24px var(--shadow);
  }
  .learn-icon{font-size:26px;margin-bottom:10px;}
  .learn-title{font-size:14px;font-weight:600;color:var(--text);margin-bottom:4px;}
  .learn-sub{font-size:12px;color:var(--muted);line-height:1.5;}
  .learn-bar{margin-top:14px;height:4px;background:var(--surface);border-radius:2px;overflow:hidden;}
  .learn-fill{height:100%;border-radius:2px;background:linear-gradient(90deg,var(--accent),var(--accent2));}

  /* ── HIGHLIGHTS ── */
  .highlights-list{display:flex;flex-direction:column;gap:10px;}
  .highlight-row {
    display:flex;align-items:center;gap:16px;
    background:var(--card);border:1px solid var(--border);
    border-radius:12px;padding:16px 20px;
    transition:all 0.25s;cursor:default;
    box-shadow:0 1px 4px var(--shadow);
  }
  .highlight-row:hover{
    border-color:rgba(180,83,9,0.3);
    background:#fffbeb;
    transform:translateX(4px);
    box-shadow:0 4px 16px var(--shadow);
  }
  .hl-icon {
    font-size:20px;width:44px;height:44px;
    display:flex;align-items:center;justify-content:center;
    background:rgba(180,83,9,0.08);border-radius:10px;flex-shrink:0;
  }
  .hl-body{flex:1;}
  .hl-title{font-size:14px;font-weight:600;color:var(--text);margin-bottom:2px;}
  .hl-desc{font-size:13px;color:var(--muted);}
  .hl-badge {
    font-family:'JetBrains Mono',monospace;font-size:11px;
    padding:4px 10px;border-radius:6px;
    background:rgba(180,83,9,0.08);color:var(--accent);
    border:1px solid rgba(180,83,9,0.15);white-space:nowrap;
  }

  /* ── LC + STATS ── */
  .lc-section{text-align:center;}
  .lc-section img{border-radius:12px;box-shadow:0 4px 20px rgba(180,83,9,0.12);max-width:100%;}
  .stats-row{display:grid;grid-template-columns:1fr 1fr;gap:14px;margin-bottom:14px;}
  .stats-row img,.streak-img img,.activity-img img{
    width:100%;border-radius:12px;box-shadow:0 2px 12px var(--shadow);
  }

  /* ── CONNECT ── */
  .connect-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:14px;}
  .connect-card {
    display:flex;flex-direction:column;align-items:center;gap:10px;
    background:var(--card);border:1px solid var(--border);
    border-radius:16px;padding:26px 16px;
    text-decoration:none;transition:all 0.3s;cursor:pointer;
    box-shadow:0 2px 8px var(--shadow);
  }
  .connect-card:hover{
    border-color:var(--c);
    box-shadow:0 8px 28px var(--shadow-c);
    transform:translateY(-4px);background:#fffbeb;
  }
  .cc-icon {
    width:48px;height:48px;border-radius:12px;
    display:flex;align-items:center;justify-content:center;
    background:var(--bg-icon);font-size:20px;
    border:1px solid var(--border);
  }
  .cc-name{font-size:14px;font-weight:600;color:var(--text);}
  .cc-handle{font-size:11px;color:var(--dim);font-family:'JetBrains Mono',monospace;}

  /* ── FOOTER ── */
  footer {
    text-align:center;margin-top:72px;
    padding:32px 0 16px;
    border-top:1px solid var(--border);
    color:var(--dim);font-size:13px;
  }
  footer span{color:var(--accent);font-weight:600;}

  /* ── REVEAL ── */
  .reveal{opacity:0;transform:translateY(24px);transition:all 0.6s ease;}
  .reveal.visible{opacity:1;transform:none;}

  ::-webkit-scrollbar{width:5px;}
  ::-webkit-scrollbar-track{background:var(--bg);}
  ::-webkit-scrollbar-thumb{background:var(--accent);border-radius:3px;}
</style>
</head>
<body>

<div class="paper-bg"></div>
<div class="blob blob1"></div>
<div class="blob blob2"></div>
<div class="blob blob3"></div>

<div class="page">

  <!-- HERO -->
  <div class="hero">
    <div class="status-badge">
      <span class="status-dot"></span>
      Open to Internships &amp; SWE Roles
    </div>

    <h1>Amandeep Singh</h1>

    <div class="hero-role">
      <span>~/</span> Full Stack Dev <span>·</span> Backend Engineer <span>·</span> Cloud Enthusiast
    </div>

    <p class="hero-desc">
      B.Tech CSE (3rd Year) · Dehradun, India<br/>
      Building scalable systems, solving hard problems, shipping real products.
    </p>

    <div class="terminal">
      <div class="terminal-bar">
        <span class="dot dot-r"></span>
        <span class="dot dot-y"></span>
        <span class="dot dot-g"></span>
      </div>
      <div class="terminal-line" id="term-output"></div>
    </div>

    <div class="socials">
      <a class="social-btn" href="https://github.com/Aman-Deep123456" target="_blank">
        <svg viewBox="0 0 24 24" fill="currentColor"><path d="M12 2C6.477 2 2 6.477 2 12c0 4.418 2.865 8.166 6.839 9.489.5.092.682-.217.682-.482 0-.237-.008-.866-.013-1.7-2.782.604-3.369-1.34-3.369-1.34-.454-1.156-1.11-1.463-1.11-1.463-.908-.62.069-.608.069-.608 1.003.07 1.531 1.03 1.531 1.03.892 1.529 2.341 1.087 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.11-4.555-4.943 0-1.091.39-1.984 1.029-2.683-.103-.253-.446-1.27.098-2.647 0 0 .84-.269 2.75 1.025A9.578 9.578 0 0112 6.836c.85.004 1.705.114 2.504.336 1.909-1.294 2.747-1.025 2.747-1.025.546 1.377.202 2.394.1 2.647.64.699 1.028 1.592 1.028 2.683 0 3.842-2.339 4.687-4.566 4.935.359.309.678.919.678 1.852 0 1.336-.012 2.415-.012 2.741 0 .267.18.578.688.48C19.138 20.163 22 16.418 22 12c0-5.523-4.477-10-10-10z"/></svg>
        GitHub
      </a>
      <a class="social-btn" href="https://www.linkedin.com/in/aman-deep-74300b28b/" target="_blank">
        <svg viewBox="0 0 24 24" fill="currentColor"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 112.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
        LinkedIn
      </a>
      <a class="social-btn" href="https://portfolio-amandeep-tau.vercel.app" target="_blank">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><path d="M2 12h20M12 2a15.3 15.3 0 010 20M12 2a15.3 15.3 0 000 20"/></svg>
        Portfolio
      </a>
      <a class="social-btn" href="https://leetcode.com/u/Aman_Deep123/" target="_blank">
        <svg viewBox="0 0 24 24" fill="currentColor"><path d="M13.483 0a1.374 1.374 0 0 0-.961.438L7.116 6.226l-3.854 4.126a5.266 5.266 0 0 0-1.209 2.104 5.35 5.35 0 0 0-.125.513 5.527 5.527 0 0 0 .062 2.362 5.83 5.83 0 0 0 .349 1.017 5.938 5.938 0 0 0 1.271 1.818l4.277 4.193.039.038c2.248 2.165 5.852 2.133 8.063-.074l2.396-2.392c.54-.54.54-1.414.003-1.955a1.378 1.378 0 0 0-1.951-.003l-2.396 2.392a3.021 3.021 0 0 1-4.205.038l-.02-.019-4.276-4.193c-.652-.64-.972-1.469-.948-2.263a2.68 2.68 0 0 1 .066-.523 2.545 2.545 0 0 1 .619-1.164L9.13 8.114c1.058-1.134 3.204-1.27 4.43-.278l3.501 2.831c.593.48 1.461.387 1.94-.207a1.384 1.384 0 0 0-.207-1.943l-3.5-2.831c-.8-.647-1.766-1.045-2.774-1.202l2.015-2.158A1.384 1.384 0 0 0 13.483 0zm-2.866 12.815a1.38 1.38 0 0 0-1.38 1.382 1.38 1.38 0 0 0 1.38 1.382H20.79a1.38 1.38 0 0 0 1.38-1.382 1.38 1.38 0 0 0-1.38-1.382z"/></svg>
        LeetCode
      </a>
      <a class="social-btn" href="mailto:bhagatmandeep50@gmail.com">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
        Email
      </a>
    </div>
  </div>

  <!-- STATS -->
  <section class="reveal">
    <div class="stats-grid">
      <div class="stat-card" data-accent="amber">
        <span class="stat-num" data-target="500">0</span>
        <div class="stat-label">LeetCode Problems</div>
      </div>
      <div class="stat-card" data-accent="teal">
        <span class="stat-num" data-target="3">0</span>
        <div class="stat-label">Year of B.Tech</div>
      </div>
      <div class="stat-card" data-accent="rose">
        <span class="stat-num" data-target="10">0</span>
        <div class="stat-label">Tech Stack Items</div>
      </div>
      <div class="stat-card" data-accent="blue">
        <span class="stat-num" data-target="6">0</span>
        <div class="stat-label">Currently Learning</div>
      </div>
    </div>
  </section>

  <!-- ABOUT -->
  <section class="reveal">
    <div class="section-label">// About</div>
    <div class="section-title">Who I Am</div>
    <div class="about-grid">
      <div class="about-card">
        <h3>// Building</h3>
        <ul>
          <li><span class="icon">🌐</span> Full Stack Web Apps (React + Node)</li>
          <li><span class="icon">🤖</span> AI-Powered apps with Core ML &amp; Create ML</li>
          <li><span class="icon">🔌</span> IoT &amp; Embedded Systems Projects</li>
          <li><span class="icon">⚡</span> Scalable Backend Services &amp; REST APIs</li>
        </ul>
      </div>
      <div class="about-card">
        <h3>// Core Strengths</h3>
        <ul>
          <li><span class="icon">🧠</span> Data Structures &amp; Algorithms</li>
          <li><span class="icon">🏗️</span> System Design &amp; Architecture</li>
          <li><span class="icon">☁️</span> Cloud Computing (AWS)</li>
          <li><span class="icon">🔧</span> DevOps &amp; CI/CD Pipelines</li>
        </ul>
      </div>
    </div>
  </section>

  <!-- TECH STACK -->
  <section class="reveal">
    <div class="section-label">// Skills</div>
    <div class="section-title">Tech Arsenal</div>
    <div class="tabs">
      <button class="tab active" onclick="switchTab(this,'lang')">Languages</button>
      <button class="tab" onclick="switchTab(this,'frontend')">Frontend</button>
      <button class="tab" onclick="switchTab(this,'backend')">Backend &amp; DB</button>
      <button class="tab" onclick="switchTab(this,'cloud')">Cloud &amp; DevOps</button>
    </div>
    <div class="tech-panel active" id="tab-lang">
      <span class="tech-pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/c/c-original.svg"/>C</span>
      <span class="tech-pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/cplusplus/cplusplus-original.svg"/>C++</span>
      <span class="tech-pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg"/>Java</span>
      <span class="tech-pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg"/>Python</span>
      <span class="tech-pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg"/>JavaScript</span>
      <span class="tech-pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/swift/swift-original.svg"/>Swift</span>
    </div>
    <div class="tech-panel" id="tab-frontend">
      <span class="tech-pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg"/>React</span>
      <span class="tech-pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg"/>HTML5</span>
      <span class="tech-pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg"/>CSS3</span>
      <span class="tech-pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tailwindcss/tailwindcss-plain.svg"/>Tailwind CSS</span>
    </div>
    <div class="tech-panel" id="tab-backend">
      <span class="tech-pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg"/>Node.js</span>
      <span class="tech-pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mongodb/mongodb-original.svg"/>MongoDB</span>
      <span class="tech-pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original.svg"/>PostgreSQL</span>
      <span class="tech-pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/firebase/firebase-plain.svg"/>Firebase</span>
    </div>
    <div class="tech-panel" id="tab-cloud">
      <span class="tech-pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/amazonwebservices/amazonwebservices-original.svg"/>AWS</span>
      <span class="tech-pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg"/>Docker</span>
      <span class="tech-pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/kubernetes/kubernetes-plain.svg"/>Kubernetes</span>
      <span class="tech-pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linux/linux-original.svg"/>Linux</span>
      <span class="tech-pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg"/>Git</span>
      <span class="tech-pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg"/>GitHub</span>
    </div>
  </section>

  <!-- LEARNING -->
  <section class="reveal">
    <div class="section-label">// Progress</div>
    <div class="section-title">Currently Learning</div>
    <div class="learning-grid">
      <div class="learn-card"><div class="learn-icon">🏗️</div><div class="learn-title">Microservices</div><div class="learn-sub">Decomposing monoliths, service mesh, event-driven patterns</div><div class="learn-bar"><div class="learn-fill" style="width:70%"></div></div></div>
      <div class="learn-card"><div class="learn-icon">🐳</div><div class="learn-title">Docker &amp; Kubernetes</div><div class="learn-sub">Containerization, orchestration, Helm charts</div><div class="learn-bar"><div class="learn-fill" style="width:60%"></div></div></div>
      <div class="learn-card"><div class="learn-icon">☁️</div><div class="learn-title">AWS Cloud</div><div class="learn-sub">EC2, S3, Lambda, RDS, IAM, CloudFormation</div><div class="learn-bar"><div class="learn-fill" style="width:55%"></div></div></div>
      <div class="learn-card"><div class="learn-icon">🔁</div><div class="learn-title">DevOps &amp; CI/CD</div><div class="learn-sub">GitHub Actions, pipelines, infra-as-code</div><div class="learn-bar"><div class="learn-fill" style="width:65%"></div></div></div>
      <div class="learn-card"><div class="learn-icon">🌐</div><div class="learn-title">Distributed Systems</div><div class="learn-sub">CAP theorem, consensus, fault tolerance</div><div class="learn-bar"><div class="learn-fill" style="width:45%"></div></div></div>
      <div class="learn-card"><div class="learn-icon">🧠</div><div class="learn-title">Advanced DSA</div><div class="learn-sub">Graphs, DP, segment trees, competitive prep</div><div class="learn-bar"><div class="learn-fill" style="width:80%"></div></div></div>
    </div>
  </section>

  <!-- HIGHLIGHTS -->
  <section class="reveal">
    <div class="section-label">// Achievements</div>
    <div class="section-title">Highlights</div>
    <div class="highlights-list">
      <div class="highlight-row"><div class="hl-icon">⚡</div><div class="hl-body"><div class="hl-title">LeetCode Problem Solving</div><div class="hl-desc">Solved 500+ problems across arrays, trees, graphs, DP, and system design questions</div></div><div class="hl-badge">500+ problems</div></div>
      <div class="highlight-row"><div class="hl-icon">🌐</div><div class="hl-body"><div class="hl-title">Full Stack Web Applications</div><div class="hl-desc">Built end-to-end apps using React, Node.js, MongoDB, and PostgreSQL with REST APIs</div></div><div class="hl-badge">Production Ready</div></div>
      <div class="highlight-row"><div class="hl-icon">🤖</div><div class="hl-body"><div class="hl-title">AI-Powered iOS Applications</div><div class="hl-desc">Developed intelligent apps integrating Core ML &amp; Create ML on the Apple ecosystem</div></div><div class="hl-badge">Swift · Core ML</div></div>
      <div class="highlight-row"><div class="hl-icon">🔌</div><div class="hl-body"><div class="hl-title">IoT Project Development</div><div class="hl-desc">Hands-on embedded systems &amp; hardware-software integration projects</div></div><div class="hl-badge">Hardware + Software</div></div>
      <div class="highlight-row"><div class="hl-icon">🌍</div><div class="hl-body"><div class="hl-title">Open Source Contributions</div><div class="hl-desc">Active contributor — improving codebases and collaborating with developers worldwide</div></div><div class="hl-badge">Active</div></div>
    </div>
  </section>

  <!-- LEETCODE -->
  <section class="reveal lc-section">
    <div class="section-label">// Competitive</div>
    <div class="section-title">LeetCode Stats</div>
    <img src="https://leetcard.jacoblin.cool/Aman_Deep123?theme=light&font=JetBrains+Mono&ext=contest&border=b45309" alt="LeetCode Stats"/>
  </section>

  <!-- GITHUB STATS -->
  <section class="reveal">
    <div class="section-label">// Activity</div>
    <div class="section-title">GitHub Stats</div>
    <div class="stats-row">
      <div><img src="https://github-readme-stats.vercel.app/api?username=Aman-Deep123456&show_icons=true&theme=default&hide_border=true&bg_color=ffffff&title_color=b45309&icon_color=d97706&text_color=1c1917&count_private=true" alt="GitHub Stats"/></div>
      <div><img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Aman-Deep123456&layout=compact&theme=default&hide_border=true&bg_color=ffffff&title_color=b45309&text_color=1c1917&langs_count=8" alt="Top Languages"/></div>
    </div>
    <div class="streak-img" style="margin-bottom:14px">
      <img src="https://github-readme-streak-stats.herokuapp.com/?user=Aman-Deep123456&theme=default&hide_border=true&background=ffffff&stroke=b45309&ring=d97706&fire=be123c&currStreakNum=1c1917&sideNums=57534e&currStreakLabel=b45309&sideLabels=b45309&dates=a8a29e" alt="Streak Stats"/>
    </div>
    <div class="activity-img">
      <img src="https://github-readme-activity-graph.vercel.app/graph?username=Aman-Deep123456&theme=minimal&bg_color=ffffff&color=b45309&line=d97706&point=be123c&area=true&hide_border=true" alt="Activity Graph"/>
    </div>
  </section>

  <!-- CONNECT -->
  <section class="reveal">
    <div class="section-label">// Contact</div>
    <div class="section-title">Let's Connect</div>
    <div class="connect-grid">
      <a class="connect-card" href="https://github.com/Aman-Deep123456" target="_blank" style="--c:rgba(28,25,23,0.4);--shadow-c:rgba(28,25,23,0.1);--bg-icon:rgba(28,25,23,0.06)">
        <div class="cc-icon">🐙</div><div class="cc-name">GitHub</div><div class="cc-handle">@Aman-Deep123456</div>
      </a>
      <a class="connect-card" href="https://www.linkedin.com/in/aman-deep-74300b28b/" target="_blank" style="--c:rgba(10,102,194,0.5);--shadow-c:rgba(10,102,194,0.1);--bg-icon:rgba(10,102,194,0.07)">
        <div class="cc-icon">💼</div><div class="cc-name">LinkedIn</div><div class="cc-handle">aman-deep-74300b28b</div>
      </a>
      <a class="connect-card" href="https://portfolio-amandeep-tau.vercel.app" target="_blank" style="--c:rgba(180,83,9,0.4);--shadow-c:rgba(180,83,9,0.1);--bg-icon:rgba(180,83,9,0.07)">
        <div class="cc-icon">🌐</div><div class="cc-name">Portfolio</div><div class="cc-handle">portfolio-amandeep</div>
      </a>
      <a class="connect-card" href="https://leetcode.com/u/Aman_Deep123/" target="_blank" style="--c:rgba(255,161,22,0.5);--shadow-c:rgba(255,161,22,0.1);--bg-icon:rgba(255,161,22,0.08)">
        <div class="cc-icon">⚡</div><div class="cc-name">LeetCode</div><div class="cc-handle">Aman_Deep123</div>
      </a>
      <a class="connect-card" href="mailto:bhagatmandeep50@gmail.com" style="--c:rgba(234,67,53,0.4);--shadow-c:rgba(234,67,53,0.08);--bg-icon:rgba(234,67,53,0.06)">
        <div class="cc-icon">✉️</div><div class="cc-name">Email</div><div class="cc-handle">bhagatmandeep50@gmail</div>
      </a>
      <div class="connect-card" style="--c:rgba(21,128,61,0.4);--shadow-c:rgba(21,128,61,0.08);--bg-icon:rgba(21,128,61,0.06);cursor:default">
        <div class="cc-icon">🟢</div><div class="cc-name">Status</div><div class="cc-handle">Open to opportunities</div>
      </div>
    </div>
  </section>

  <footer>
    <p>Crafted with ☕ by <span>Amandeep Singh</span> · Keep Building · Keep Learning · Keep Growing 🚀</p>
  </footer>
</div>

<script>
// Terminal typewriter
const lines = [
  { prompt: '❯ ', cmd: 'cat ', val: 'profile.json' },
  { raw: '  <span class="key">"name"</span>: <span class="val">"Amandeep Singh"</span>,' },
  { raw: '  <span class="key">"role"</span>: <span class="val">"Full Stack Developer"</span>,' },
  { raw: '  <span class="key">"leetcode"</span>: <span class="val">"500+ solved"</span>,' },
  { raw: '  <span class="key">"status"</span>: <span class="val">"Open to Opportunities ✅"</span>' },
];
const out = document.getElementById('term-output');
let lineIdx=0,charIdx=0,content='';
function typeNext(){
  if(lineIdx>=lines.length)return;
  const line=lines[lineIdx];
  if(line.raw){content+=line.raw+'<br/>';out.innerHTML=content+'<span id="cursor"></span>';lineIdx++;charIdx=0;setTimeout(typeNext,120);return;}
  const full=line.prompt+line.cmd+line.val;
  if(charIdx<=full.length){
    const typed=full.slice(0,charIdx);
    let d='';
    if(typed.startsWith(line.prompt+line.cmd))d=`<span class="prompt">${line.prompt}</span><span class="cmd">${line.cmd}</span><span class="val">${typed.slice(line.prompt.length+line.cmd.length)}</span>`;
    else if(typed.startsWith(line.prompt))d=`<span class="prompt">${line.prompt}</span><span class="cmd">${typed.slice(line.prompt.length)}</span>`;
    else d=`<span class="prompt">${typed}</span>`;
    out.innerHTML=content+d+'<span id="cursor"></span>';charIdx++;setTimeout(typeNext,55);
  }else{content+=`<span class="prompt">${line.prompt}</span><span class="cmd">${line.cmd}</span><span class="val">${line.val}</span><br/>`;lineIdx++;charIdx=0;setTimeout(typeNext,300);}
}
setTimeout(typeNext,800);

// Tab switcher
function switchTab(btn,id){
  document.querySelectorAll('.tab').forEach(t=>t.classList.remove('active'));
  document.querySelectorAll('.tech-panel').forEach(p=>p.classList.remove('active'));
  btn.classList.add('active');
  document.getElementById('tab-'+id).classList.add('active');
}

// Scroll reveal
const obs=new IntersectionObserver(entries=>{entries.forEach(e=>{if(e.isIntersecting)e.target.classList.add('visible');});},{threshold:0.1});
document.querySelectorAll('.reveal').forEach(el=>obs.observe(el));

// Counter animation
function animateCounter(el){
  const target=parseInt(el.dataset.target);
  const suffix=target>=500?'+':'';
  let start=0;const step=target/50;
  const iv=setInterval(()=>{start=Math.min(start+step,target);el.textContent=Math.floor(start)+suffix;if(start>=target)clearInterval(iv);},28);
}
const cobs=new IntersectionObserver(entries=>{entries.forEach(e=>{if(e.isIntersecting){e.target.querySelectorAll('[data-target]').forEach(animateCounter);cobs.unobserve(e.target);}});},{threshold:0.3});
document.querySelectorAll('.stats-grid').forEach(el=>cobs.observe(el));
</script>
</body>
</html>
