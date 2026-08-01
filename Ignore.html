<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>RAMP — Roblox Auto MIDI Player</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=JetBrains+Mono:wght@400;500;700&display=swap');
  :root{
    --bg:#0c0d11;--surf:#181a21;--surf2:#101216;--border:#262a33;
    --tx:#e8e6ef;--muted:#9a9aad;--faint:#6a7080;--head:#f1f2f6;
    --ac:#6366f1;--ac-hi:#8b8dff;--ac-bg:#20223a;--teal:#1D9E75;
    --ok:#3ecf8e;--err:#e05555;
    --mono:"JetBrains Mono",ui-monospace,Menlo,Consolas,monospace;
    --sans:"Space Grotesk","Segoe UI",system-ui,sans-serif;
  }
  *{margin:0;padding:0;box-sizing:border-box}
  html{scroll-behavior:smooth;scroll-padding-top:120px}
  body{background:var(--bg);color:var(--tx);font-family:var(--sans);line-height:1.6;-webkit-font-smoothing:antialiased}
  a{color:inherit;text-decoration:none}
  ::selection{background:var(--ac);color:#fff}
  code{font-family:var(--mono);font-size:.9em;background:var(--surf2);border:1px solid var(--border);padding:2px 6px;border-radius:5px;color:var(--ac-hi)}
  .wrap{max-width:1120px;margin:0 auto;padding:0 26px}

  /* header */
  .hdr{position:sticky;top:0;z-index:50;background:linear-gradient(180deg,rgba(18,20,30,.96),rgba(12,13,17,.92));backdrop-filter:blur(16px);border-bottom:1px solid var(--border);box-shadow:0 1px 0 rgba(99,102,241,.14)}
  .hdr-top{display:flex;align-items:center;gap:16px;padding:14px 0}
  .logo{display:flex;align-items:center;gap:10px;font-weight:700;font-size:19px;letter-spacing:.3px}
  .logo .mk{display:grid;grid-template-columns:1fr 1fr;width:30px;height:30px;border-radius:7px;overflow:hidden;gap:1px;box-shadow:0 0 0 1px var(--border),0 4px 14px -6px var(--ac)}
  .logo .mk span{display:grid;place-items:center;background:var(--surf);font-size:10px;font-weight:700;color:var(--ac-hi)}
  .logo .mk span:nth-child(2),.logo .mk span:nth-child(3){color:var(--tx)}
  .logo .word b{color:var(--ac-hi);font-weight:700}
  .logo .word{cursor:pointer;position:relative;display:inline-flex;align-items:center;overflow:hidden;white-space:nowrap}
  .logo .word .full{max-width:0;opacity:0;overflow:hidden;transition:max-width .4s cubic-bezier(.4,0,.2,1),opacity .3s;white-space:nowrap}
  .logo .word .short{transition:max-width .4s cubic-bezier(.4,0,.2,1),opacity .3s;max-width:120px;opacity:1}
  .logo .word.expanded .short{max-width:0;opacity:0}
  .logo .word.expanded .full{max-width:340px;opacity:1}
  .hdr-actions{margin-left:auto;display:flex;gap:10px;align-items:center}
  .badge-v{font-family:var(--mono);font-size:12px;font-weight:700;background:var(--ac-bg);color:var(--ac-hi);padding:5px 11px;border-radius:20px;box-shadow:inset 0 0 0 1px rgba(139,141,255,.28)}
  .btn{font-family:var(--sans);font-weight:600;font-size:14px;cursor:pointer;padding:9px 17px;border-radius:9px;border:1px solid transparent;transition:.15s;display:inline-flex;align-items:center;gap:8px}
  .btn-p{background:var(--ac);color:#fff}
  .btn-p:hover{background:var(--ac-hi);box-shadow:0 8px 22px -10px var(--ac)}
  .btn-g{background:var(--surf);border-color:var(--border);color:var(--tx)}
  .btn-g:hover{border-color:var(--ac)}
  nav.tabs{display:flex;gap:2px;flex-wrap:wrap;padding-bottom:2px}
  nav.tabs a{font-size:13px;color:var(--muted);padding:10px 13px;border-bottom:2px solid transparent;white-space:nowrap;transition:.15s}
  nav.tabs a:hover{color:var(--tx)}
  nav.tabs a.on{color:var(--ac-hi);border-color:var(--ac)}

  /* hero */
  .hero{padding:66px 0 50px;border-bottom:1px solid var(--border);background:radial-gradient(1200px 380px at 70% -10%,rgba(99,102,241,.12),transparent)}
  .hero h1{font-size:clamp(38px,6vw,66px);font-weight:700;letter-spacing:-1.5px;line-height:1;color:var(--head);margin-bottom:20px}
  .hero h1 .g{background:linear-gradient(105deg,var(--ac-hi),var(--teal));-webkit-background-clip:text;background-clip:text;color:transparent}
  .hero .sub{font-size:19px;color:var(--muted);max-width:34em;margin-bottom:30px}
  .hero-cta{display:flex;gap:12px;flex-wrap:wrap}
  .hero-stats{display:flex;gap:30px;margin-top:34px;flex-wrap:wrap}
  .hero-stats .s b{display:block;font-size:26px;font-weight:700;color:var(--head);font-family:var(--mono)}
  .hero-stats .s span{font-size:13px;color:var(--faint)}

  /* sections */
  section{padding:66px 0;border-bottom:1px solid var(--border)}
  .kicker{font-family:var(--mono);font-size:12px;letter-spacing:2px;text-transform:uppercase;color:var(--teal);margin-bottom:13px}
  h2{font-size:clamp(26px,3.4vw,38px);font-weight:700;letter-spacing:-.6px;color:var(--head);line-height:1.1;margin-bottom:14px}
  h2+.lead{font-size:17px;color:var(--muted);max-width:40em;margin-bottom:40px}
  h3{font-size:20px;font-weight:600;color:var(--head);margin-bottom:8px}

  /* detailed feature blocks */
  .feat{display:grid;grid-template-columns:220px 1fr;gap:30px;padding:30px 0;border-top:1px solid var(--border)}
  .feat:first-of-type{border-top:none}
  .feat .side .tab-name{font-family:var(--mono);font-size:12px;color:var(--ac-hi);background:var(--ac-bg);padding:4px 10px;border-radius:6px;display:inline-block;margin-bottom:12px}
  .feat .side h3{font-size:22px}
  .feat .side .ic{font-size:30px;margin-bottom:12px}
  .feat .body p{color:var(--muted);margin-bottom:14px}
  .feat .body ul{list-style:none;margin:6px 0 0}
  .feat .body li{padding:7px 0 7px 24px;position:relative;color:var(--muted);font-size:14.5px;border-top:1px solid var(--surf2)}
  .feat .body li::before{content:"▸";position:absolute;left:2px;color:var(--teal)}
  .feat .body li b{color:var(--tx);font-weight:600}
  .pill-row{display:flex;gap:8px;flex-wrap:wrap;margin-top:14px}
  .pill{font-family:var(--mono);font-size:11px;padding:4px 10px;border-radius:6px;background:var(--surf);border:1px solid var(--border);color:var(--muted)}

  /* cards grid */
  .grid3{display:grid;grid-template-columns:repeat(3,1fr);gap:16px}
  .card{background:var(--surf);border:1px solid var(--border);border-radius:13px;padding:24px;transition:.16s}
  .card:hover{border-color:var(--ac);transform:translateY(-2px)}
  .card .ic{font-size:24px;margin-bottom:12px}
  .card p{font-size:14px;color:var(--muted);margin-top:6px}

  /* why ramp */
  .why-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:14px}
  .why-card{background:var(--surf);border:1px solid var(--border);border-radius:13px;padding:22px 20px;transition:.16s}
  .why-card:hover{border-color:var(--ac);transform:translateY(-3px)}
  .why-card .wic{font-size:26px;margin-bottom:13px}
  .why-card h3{font-size:16px;margin-bottom:8px}
  .why-card p{font-size:13.5px;color:var(--muted);line-height:1.55}
  @media(max-width:980px){.why-grid{grid-template-columns:repeat(2,1fr)}}
  @media(max-width:560px){.why-grid{grid-template-columns:1fr}}

  /* specs */
  .spec-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:26px}
  .spec-col h4{font-family:var(--mono);font-size:12px;letter-spacing:1px;text-transform:uppercase;color:var(--ac-hi);margin-bottom:6px;padding-bottom:8px;border-bottom:1px solid var(--ac-bg)}
  .spec-col .modetable td{padding:10px 4px}
  .spec-col .modetable td:first-child{color:var(--muted);font-family:var(--sans);white-space:normal}
  .spec-col .modetable td:last-child{color:var(--tx);text-align:right;font-family:var(--mono);font-size:12.5px}
  @media(max-width:720px){.spec-grid{grid-template-columns:1fr}}

  /* architecture diagram */
  .arch-legend{display:flex;gap:20px;flex-wrap:wrap;margin-bottom:20px;font-size:13px;color:var(--muted)}
  .arch-legend span{display:flex;align-items:center;gap:7px}
  .arch-legend i{width:11px;height:11px;border-radius:3px;display:inline-block}
  .arch-wrap{position:relative;background:radial-gradient(700px 320px at 50% 40%,rgba(99,102,241,.07),transparent);border:1px solid var(--border);border-radius:16px;padding:10px;overflow:hidden}
  #arch{width:100%;height:auto;display:block}
  #arch .edge{stroke:var(--border);stroke-width:1.4;fill:none;transition:.2s}
  #arch .edge.hot{stroke:var(--ac-hi);stroke-width:2.2}
  #arch .node circle{transition:.18s;cursor:pointer}
  #arch .node:hover circle{filter:brightness(1.25)}
  #arch .node text{font-family:var(--sans);font-size:12px;font-weight:600;fill:var(--tx);pointer-events:none;text-anchor:middle}
  #arch .node .sub{font-family:var(--mono);font-size:9px;fill:var(--faint)}
  #arch .hub circle{cursor:default}
  #arch .hub text{font-size:14px;font-weight:700;fill:#fff}
  .arch-tip{position:absolute;pointer-events:none;background:var(--surf);border:1px solid var(--ac);border-radius:10px;padding:11px 14px;max-width:260px;font-size:13px;color:var(--tx);opacity:0;transform:translateY(4px);transition:.15s;z-index:5;box-shadow:0 10px 30px -10px #000}
  .arch-tip.on{opacity:1;transform:translateY(0)}
  .arch-tip b{color:var(--ac-hi);display:block;margin-bottom:4px;font-family:var(--mono);font-size:12px}
  .arch-tip span{color:var(--muted);font-size:12.5px;line-height:1.5}

  /* how it works diagram */
  .diagram{display:flex;align-items:stretch;gap:6px;flex-wrap:wrap;justify-content:center;margin-bottom:36px}
  .dnode{flex:1;min-width:120px;background:var(--surf);border:1px solid var(--border);border-radius:13px;padding:20px 14px;text-align:center;transition:.16s;position:relative}
  .dnode:hover{border-color:var(--ac);transform:translateY(-3px)}
  .dnode.accent{background:linear-gradient(165deg,rgba(99,102,241,.14),var(--surf));border-color:var(--ac)}
  .dnode .dic{font-size:26px;margin-bottom:10px}
  .dnode b{display:block;font-size:14.5px;color:var(--head)}
  .dnode span{display:block;font-size:11.5px;color:var(--faint);margin-top:3px;font-family:var(--mono)}
  .darrow{display:flex;flex-direction:column;align-items:center;justify-content:center;color:var(--ac-hi);font-size:15px;min-width:56px;position:relative}
  .darrow span{font-family:var(--mono);font-size:9.5px;letter-spacing:.5px;color:var(--teal);text-transform:uppercase;margin-bottom:2px}
  .how-notes{display:grid;grid-template-columns:repeat(2,1fr);gap:14px}
  .hn{background:var(--surf2);border:1px solid var(--border);border-radius:11px;padding:18px 20px}
  .hn b{color:var(--ac-hi);font-family:var(--mono);font-size:13px;display:block;margin-bottom:6px}
  .hn p{color:var(--muted);font-size:14px}
  @media(max-width:820px){
    .darrow{transform:rotate(90deg);min-width:auto;padding:4px 0}
    .diagram{flex-direction:column}
    .how-notes{grid-template-columns:1fr}
  }

  /* how it works steps */
  .steps{counter-reset:s;display:grid;gap:14px}
  .step{display:grid;grid-template-columns:44px 1fr;gap:18px;align-items:start;background:var(--surf);border:1px solid var(--border);border-radius:12px;padding:20px 22px}
  .step .n{counter-increment:s;width:44px;height:44px;border-radius:11px;background:var(--ac-bg);color:var(--ac-hi);font-family:var(--mono);font-weight:700;font-size:18px;display:grid;place-items:center}
  .step .n::before{content:counter(s)}
  .step p{color:var(--muted);font-size:14.5px;margin-top:4px}

  /* mode table */
  .modetable{width:100%;border-collapse:collapse;font-size:14px;margin-top:8px}
  .modetable th,.modetable td{text-align:left;padding:13px 14px;border-bottom:1px solid var(--border)}
  .modetable th{font-family:var(--mono);font-size:11px;letter-spacing:1px;text-transform:uppercase;color:var(--faint)}
  .modetable td:first-child{font-family:var(--mono);color:var(--ac-hi);white-space:nowrap}
  .modetable tr:hover td{background:var(--surf2)}

  /* pricing */
  .lb{display:grid;grid-template-columns:1fr 1fr;gap:20px}
  .pc{border:1px solid var(--border);border-radius:16px;padding:30px;background:var(--surf)}
  .pc.pro{border-color:var(--ac);background:linear-gradient(165deg,rgba(99,102,241,.08),var(--surf))}
  .pc h3{font-family:var(--mono);font-size:13px;letter-spacing:1px;text-transform:uppercase;color:var(--muted);margin-bottom:14px}
  .pc .price{font-size:38px;font-weight:700;color:var(--head);display:flex;align-items:baseline;gap:8px}
  .pc .price .r{font-size:15px;color:var(--teal);font-family:var(--mono)}
  .pc ul{list-style:none;margin-top:20px}
  .pc li{font-size:14px;color:var(--muted);padding:9px 0 9px 24px;position:relative;border-top:1px solid var(--border)}
  .pc li::before{content:"✓";position:absolute;left:0;color:var(--teal);font-weight:700}
  .pc li.no{color:var(--faint)} .pc li.no::before{content:"—";color:var(--faint)}

  /* install */
  .codebox{background:#08090c;border:1px solid var(--border);border-radius:11px;padding:18px 20px;font-family:var(--mono);font-size:13px;color:var(--muted);overflow-x:auto}
  .codebox .c{color:var(--teal)}

  /* faq */
  details{background:var(--surf);border:1px solid var(--border);border-radius:11px;padding:2px 20px;margin-bottom:11px;transition:.15s}
  details[open]{border-color:var(--ac)}
  summary{cursor:pointer;padding:17px 0;font-weight:600;color:var(--head);list-style:none;display:flex;justify-content:space-between;align-items:center}
  summary::-webkit-details-marker{display:none}
  summary::after{content:"+";color:var(--ac-hi);font-size:20px}
  details[open] summary::after{content:"−"}
  details p{color:var(--muted);font-size:14.5px;padding:0 0 18px}

  .safe{border:1px solid var(--border);border-radius:14px;padding:26px 28px;background:var(--surf);display:flex;gap:18px}
  .safe .sh{font-size:28px}
  .safe p{color:var(--muted);font-size:14.5px}
  .safe a{color:var(--ac-hi)}

  footer{padding:34px 0;color:var(--faint);font-size:13px}
  footer .wrap{display:flex;justify-content:space-between;gap:14px;flex-wrap:wrap}

  @media(max-width:820px){
    .feat{grid-template-columns:1fr;gap:14px}
    .grid3,.lb{grid-template-columns:1fr}
    nav.tabs{gap:0}
  }
  @media(prefers-reduced-motion:reduce){*{animation:none!important;transition:none!important}}
</style>
</head>
<body>

<header class="hdr">
  <div class="wrap">
    <div class="hdr-top">
      <a href="#top" class="logo"><span class="mk"><span>R</span><span>A</span><span>M</span><span>P</span></span> <span class="word" id="wordmark" title="Click to expand"><span class="short">R<b>A</b>MP</span><span class="full"><b>R</b>oblox <b>A</b>uto <b>M</b>IDI <b>P</b>layer</span></span></a>
      <div class="hdr-actions">
        <span class="badge-v">v4.0</span>
        <a href="#install" class="btn btn-g">Install</a>
        <a href="#download" class="btn btn-p">↓ Download</a>
      </div>
    </div>
    <nav class="tabs" id="tabnav">
      <a href="#overview" class="on">Overview</a>
      <a href="#why">Why RAMP</a>
      <a href="#autoplay">Auto-player</a>
      <a href="#modes">Modes &amp; transpose</a>
      <a href="#convert">Convert to MIDI</a>
      <a href="#live">Live play</a>
      <a href="#visualizer">Visualizer</a>
      <a href="#customize">Customize</a>
      <a href="#how">How it works</a>
      <a href="#architecture">Architecture</a>
      <a href="#specs">Specs</a>
      <a href="#install">Installation</a>
      <a href="#pricing">Limit Breaker</a>
      <a href="#faq">FAQ</a>
      <a href="#safe">Safety</a>
    </nav>
  </div>
</header>

<a id="top"></a>
<div class="hero" id="overview"><div class="wrap">
  <div class="kicker">Roblox Auto MIDI Player · v4.0 · open-source</div>
  <h1>The best Roblox<br>piano player of<br><span class="g">2026.</span></h1>
  <p class="sub">Load a MIDI and RAMP performs it on any Roblox piano with human timing and live velocity. Convert audio, video, and sheet music into MIDI. Play a real keyboard live. All in one portable app.</p>
  <div class="hero-cta">
    <a href="#download" class="btn btn-p">↓ Download for Windows</a>
    <a href="#autoplay" class="btn btn-g">Explore the features</a>
  </div>
  <div class="hero-stats">
    <div class="s"><b>11</b><span>feature tabs</span></div>
    <div class="s"><b>128</b><span>notes mappable</span></div>
    <div class="s"><b>10k+</b><span>notes/sec visualizer</span></div>
    <div class="s"><b>£0</b><span>free &amp; open-source</span></div>
  </div>
</div></div>

<!-- OVERVIEW SUMMARY -->
<section><div class="wrap">
  <div class="kicker">What's inside</div>
  <h2>Eleven tabs, one app.</h2>
  <p class="lead">RAMP isn't a single-trick autoplayer — every tab is a full tool. Here's the whole surface at a glance; each one is documented in detail below.</p>
  <div class="grid3">
    <div class="card"><div class="ic">▶️</div><h3>Player</h3><p>The auto-player: load a MIDI, human-like performance, speed, transpose, sustain, panic.</p></div>
    <div class="card"><div class="ic">🎹</div><h3>Connect</h3><p>Play a real MIDI keyboard (USB or Bluetooth) and RAMP presses the keys live.</p></div>
    <div class="card"><div class="ic">🌈</div><h3>Visualizer</h3><p>Full black-MIDI Synthesia-style falling-notes engine at 60 fps.</p></div>
    <div class="card"><div class="ic">🎬</div><h3>Transcribe</h3><p>Audio → MIDI, video → MIDI, and PDF sheet music → MIDI, all local.</p></div>
    <div class="card"><div class="ic">🔤</div><h3>Qwerty Sheet</h3><p>Turn a MIDI into a letter sheet with playability levels and practice mode.</p></div>
    <div class="card"><div class="ic">⌨️</div><h3>PianoBinds</h3><p>Remap all 88 keys to match the in-game NoteBinds panel exactly.</p></div>
    <div class="card"><div class="ic">🎚️</div><h3>Velocity</h3><p>Dynamics: auto-volume, velocity curves, auto-velocity from note density.</p></div>
    <div class="card"><div class="ic">🎯</div><h3>Octave</h3><p>Range modes and octave handling for whatever piano you're on.</p></div>
    <div class="card"><div class="ic">⚙️</div><h3>Settings</h3><p>Hotkeys, overlay, focus guard, sound output, playlist behaviour.</p></div>
    <div class="card"><div class="ic">📋</div><h3>Logs</h3><p>Live activity log — see every transpose decision and key press.</p></div>
    <div class="card"><div class="ic">🎨</div><h3>Customize</h3><p>Full theming — every colour, gradients, background images, fonts, scale.</p></div>
    <div class="card"><div class="ic">◱</div><h3>Simple mode</h3><p>A compact 6-tab window for when you just want to play, not tweak.</p></div>
  </div>
</div></section>

<!-- WHY RAMP -->
<section id="why"><div class="wrap">
  <div class="kicker">Why RAMP</div>
  <h2>Why pick RAMP over another autoplayer?</h2>
  <p class="lead">Plenty of Roblox piano tools exist. Here's what actually sets RAMP apart — every point is something you can verify yourself.</p>

  <div class="why-grid">
    <div class="why-card">
      <div class="wic">🔓</div>
      <h3>Fully open-source</h3>
      <p>Every line of RAMP is public. You can read exactly what it does, check its network activity, and even build it yourself. Most autoplayers are closed binaries you have to just trust.</p>
    </div>
    <div class="why-card">
      <div class="wic">🎬</div>
      <h3>Three converters built in</h3>
      <p>Audio, Synthesia video, and PDF sheet music all turn into MIDI — right inside the app, running locally. Not just a player: a full pipeline from "I want this song" to playing it.</p>
    </div>
    <div class="why-card">
      <div class="wic">🎭</div>
      <h3>Genuinely human playback</h3>
      <p>Great Pretender re-rolls timing and dynamics every play with warm-up, rubato and optional mistakes — so it doesn't read as a bot. Not just a flat "humanize" toggle.</p>
    </div>
    <div class="why-card">
      <div class="wic">💜</div>
      <h3>Free — one optional unlock</h3>
      <p>The entire app is free. The only paid thing is Limit Breaker (1,000 Robux) for the extended key range, and you never need it for normal play. No subscriptions, no locked core features.</p>
    </div>
    <div class="why-card">
      <div class="wic">🎨</div>
      <h3>Themeable to the pixel</h3>
      <p>Every colour, gradient, background and font is editable, with 11 presets and savable custom themes. Make it look like anything.</p>
    </div>
    <div class="why-card">
      <div class="wic">🔵</div>
      <h3>Real hardware, incl. Bluetooth</h3>
      <p>Play a physical MIDI keyboard live — over USB or wireless Bluetooth — with velocity and octave doubling. Your playing, RAMP's key presses.</p>
    </div>
    <div class="why-card">
      <div class="wic">⚡</div>
      <h3>Built for heavy MIDI</h3>
      <p>A batched SendInput pipeline and a 60 fps visualizer that holds up at 10,000+ notes/sec — black MIDI plays without choking.</p>
    </div>
    <div class="why-card">
      <div class="wic">📦</div>
      <h3>Portable &amp; auto-updating</h3>
      <p>No installer, no setup — extract and run. It checks for its own updates, so you're always current.</p>
    </div>
  </div>

  <p style="color:var(--faint);font-size:13px;margin-top:26px;text-align:center">Don't take our word for it — RAMP is open-source, so you can confirm every claim on this page for yourself.</p>
</div></section>
<section id="autoplay"><div class="wrap">
  <div class="kicker">The auto-player</div>
  <h2>It performs. It doesn't paste.</h2>
  <p class="lead">The core of RAMP. Every play is re-rolled with human imperfections, so the same MIDI never comes out identical twice — and it never reads like a bot.</p>

  <div class="feat">
    <div class="side"><div class="ic">🎭</div><span class="tab-name">Player tab</span><h3>Great Pretender</h3></div>
    <div class="body">
      <p>A humanisation engine that layers realistic imperfections over the raw MIDI. Instead of machine-perfect timing, you get a believable human performance.</p>
      <ul>
        <li><b>Warm-up &amp; stage fright</b> — subtle tempo drift at the start, settling as the "performer" relaxes.</li>
        <li><b>Rubato</b> — expressive push-and-pull in timing around phrases, not a rigid grid.</li>
        <li><b>Note-length drift</b> — held notes vary slightly, like real fingers.</li>
        <li><b>Wrong notes on demand</b> — optional, tunable "mistakes" for total realism.</li>
      </ul>
      <div class="pill-row"><span class="pill">Subtle</span><span class="pill">Balanced</span><span class="pill">Expressive</span><span class="pill">Pro</span><span class="pill">custom blend</span></div>
    </div>
  </div>

  <div class="feat">
    <div class="side"><div class="ic">⚡</div><span class="tab-name">Player tab</span><h3>Playback control</h3></div>
    <div class="body">
      <p>Full transport control over the performance, all reachable by global hotkey so Roblox never loses focus.</p>
      <ul>
        <li><b>Speed</b> — nudge tempo up/down live (±0.01 to ±0.05 steps, or reset).</li>
        <li><b>Sustain</b> — hold the sustain pedal, with pedal-change tracking from the MIDI.</li>
        <li><b>Seek &amp; rewind</b> — jump anywhere instantly, even in huge black-MIDI files.</li>
        <li><b>Panic (F4)</b> — instantly releases every held key if a note ever sticks.</li>
      </ul>
    </div>
  </div>

  <div class="feat">
    <div class="side"><div class="ic">📚</div><span class="tab-name">Player tab</span><h3>Library &amp; playlist</h3></div>
    <div class="body">
      <p>Browse your whole MIDI collection from the sidebar, with folders, search, sort, and favourites.</p>
      <ul>
        <li><b>Folder browsing</b> — nested folders, deep search across your music.</li>
        <li><b>Playlist mode</b> — auto-next through a set, with an optional 3-second countdown between songs.</li>
        <li><b>Loop</b> — repeat the current song.</li>
        <li><b>Track filtering</b> — mute or solo individual MIDI tracks.</li>
      </ul>
    </div>
  </div>
</div></section>

<!-- MODES & TRANSPOSE -->
<section id="modes"><div class="wrap">
  <div class="kicker">Range &amp; transpose</div>
  <h2>Fits any piano, automatically.</h2>
  <p class="lead">Different Roblox pianos have different ranges. RAMP finds the one transposition that keeps the whole song playable, and gives you five range modes to match the game you're in.</p>

  <div class="feat">
    <div class="side"><div class="ic">🎯</div><span class="tab-name">Player + Octave</span><h3>Auto-transpose</h3></div>
    <div class="body">
      <p>RAMP scans the whole song, finds the transposition that fits the most notes inside the keyboard's range, and locks to it — with sticky best-shift logic and lookahead so it doesn't thrash mid-song. The Logs tab shows you exactly which shift it chose and why.</p>
    </div>
  </div>

  <table class="modetable">
    <thead><tr><th>Mode</th><th>Range</th><th>Best for</th></tr></thead>
    <tbody>
      <tr><td>61-key</td><td>MIDI 36–96</td><td>Standard virtual-piano keyboards</td></tr>
      <tr><td>88 Transpose</td><td>MIDI 21–108</td><td>Full 88-key pianos via arrow-key transpose</td></tr>
      <tr><td>88 Ctrl</td><td>MIDI 21–108</td><td>Full 88 keys using Ctrl-extended keys</td></tr>
      <tr><td>128 (fold)</td><td>MIDI 0–127</td><td>Extreme-range MIDIs — out-of-range notes fold back in</td></tr>
      <tr><td>128 Octave</td><td>MIDI 0–127</td><td>Shifts whole octaves with the piano's own transpose</td></tr>
    </tbody>
  </table>
  <p style="color:var(--faint);font-size:13px;margin-top:14px">With Limit Breaker, the range extends to a 97-key layout (up to MIDI 117) for pianos like Piano Haven.</p>
</div></section>

<!-- CONVERT -->
<section id="convert"><div class="wrap">
  <div class="kicker">New in v4.0 · runs locally</div>
  <h2>Turn anything into MIDI.</h2>
  <p class="lead">The Transcribe tab has three separate engines. Nothing uploads — every conversion happens on your own machine.</p>

  <div class="feat">
    <div class="side"><div class="ic">🎵</div><span class="tab-name">Transcribe › MP3</span><h3>Audio → MIDI</h3></div>
    <div class="body">
      <p>Transcribe any song or audio file into playable MIDI using a built-in neural model. Free and unlimited on your PC — install the model once and it's yours.</p>
      <ul><li>Works on MP3, WAV, M4A, FLAC, OGG.</li><li>Preview before you commit.</li><li>Loads straight into the Player when done.</li></ul>
    </div>
  </div>

  <div class="feat">
    <div class="side"><div class="ic">🎬</div><span class="tab-name">Transcribe › MP4</span><h3>Video → MIDI</h3></div>
    <div class="body">
      <p>Reads a Synthesia-style piano video <b>visually</b> — it watches the falling bars, detects the keyboard, learns the note colours, and reconstructs the MIDI. No audio needed.</p>
      <ul>
        <li>Two live preview panels — <b>what it sees</b> and <b>what it understands</b>.</li>
        <li>Nine-step pipeline you can watch in real time.</li>
        <li>Optional audio cross-check for real velocities.</li>
        <li>Reference library of keyboard layouts it remembers.</li>
      </ul>
    </div>
  </div>

  <div class="feat">
    <div class="side"><div class="ic">📄</div><span class="tab-name">Transcribe › PDF</span><h3>Sheet music → MIDI</h3></div>
    <div class="body">
      <p>Reads the actual noteheads, staves, clefs and accidentals out of a digitally-exported sheet-music PDF and turns them into notes — including chords.</p>
      <ul>
        <li>Built for MuseScore and Sibelius exports (Leland, Bravura, Opus fonts).</li>
        <li>Detects staff lines, maps each notehead's position to a pitch through the clef.</li>
        <li>Groups stacked noteheads into chords.</li>
        <li><b>Best on MuseScore 4 exports</b> today — more formats and rhythm depth coming.</li>
      </ul>
    </div>
  </div>
</div></section>

<!-- LIVE -->
<section id="live"><div class="wrap">
  <div class="kicker">Play it yourself</div>
  <h2>Bring your own keyboard.</h2>
  <p class="lead">Plug in a real MIDI keyboard and RAMP presses the Roblox keys as you play — with live velocity, sustain, and the visualizer following along.</p>
  <div class="grid3">
    <div class="card"><div class="ic">🔵</div><h3>Bluetooth mode <span style="color:var(--teal);font-size:12px">NEW</span></h3><p>Connect a wireless MIDI keyboard over Bluetooth — no cable, no adapter.</p></div>
    <div class="card"><div class="ic">🎚️</div><h3>Double octave <span style="color:var(--teal);font-size:12px">NEW</span></h3><p>Octave doubling thickens every live note, on both MIDI Connect and QWERTY output.</p></div>
    <div class="card"><div class="ic">↔️</div><h3>Two output methods</h3><p>Send virtual-piano QWERTY keys, or MidiConnect numpad — your choice.</p></div>
    <div class="card"><div class="ic">🎼</div><h3>Live velocity</h3><p>How hard you play carries through to the Roblox piano in real time.</p></div>
    <div class="card"><div class="ic">🎯</div><h3>Focus-aware</h3><p>"Only send keys while Roblox is focused" keeps stray presses out of other apps.</p></div>
    <div class="card"><div class="ic">🌈</div><h3>Visualizer sync</h3><p>Point the visualizer at MIDI Connect to watch your own playing fall.</p></div>
  </div>
</div></section>

<!-- VISUALIZER -->
<section id="visualizer"><div class="wrap">
  <div class="kicker">See the music</div>
  <h2>A real black-MIDI visualizer.</h2>
  <p class="lead">Not a toy — a full Synthesia-style falling-notes engine that holds a steady frame rate even under absurd note counts.</p>
  <div class="grid3">
    <div class="card"><div class="ic">⚡</div><h3>10,000+ notes/sec</h3><p>Frame pooling and tuned rendering keep it smooth where other visualizers choke.</p></div>
    <div class="card"><div class="ic">🎨</div><h3>Per-track colours</h3><p>Every MIDI track gets its own colour, so dense pieces stay readable.</p></div>
    <div class="card"><div class="ic">🖥️</div><h3>Its own tab + sources</h3><p>Watch a loaded MIDI, live QWERTY, or your MIDI-Connect playing.</p></div>
  </div>
</div></section>

<!-- CUSTOMIZE -->
<section id="customize"><div class="wrap">
  <div class="kicker">Make it yours</div>
  <h2>Theme every pixel.</h2>
  <p class="lead">RAMP ships in "Dark Slate," but everything is editable — this is one of the most themeable apps you'll find.</p>
  <div class="grid3">
    <div class="card"><div class="ic">🎨</div><h3>Every colour</h3><p>Accents, surfaces, borders, text tiers and status colours — all individually editable.</p></div>
    <div class="card"><div class="ic">🌈</div><h3>11 quick themes</h3><p>Indigo, Violet, Dracula, Ocean, Teal, Forest, Gold, Fire, Crimson, Candy, Neon, Mono.</p></div>
    <div class="card"><div class="ic">🖼️</div><h3>Gradients &amp; images</h3><p>Gradient accents, background images with opacity, scrollbar styles.</p></div>
    <div class="card"><div class="ic">🔤</div><h3>Fonts &amp; scale</h3><p>Swap the UI font and scale the whole interface.</p></div>
    <div class="card"><div class="ic">💾</div><h3>Save presets</h3><p>Name and store your own themes, switch any time.</p></div>
    <div class="card"><div class="ic">↔️</div><h3>Resizable window</h3><p>Drag any edge to resize, plus a compact Simple mode.</p></div>
  </div>
</div></section>

<!-- HOW IT WORKS -->
<section id="how"><div class="wrap">
  <div class="kicker">Under the hood</div>
  <h2>How RAMP plays.</h2>
  <p class="lead">No magic — a MIDI comes in one end, precise key presses come out the other, timed to the millisecond and mapped to the virtual-piano layout.</p>

  <div class="diagram">
    <div class="dnode"><div class="dic">🎼</div><b>MIDI file</b><span>notes + timing</span></div>
    <div class="darrow"><span>parse</span>▶</div>
    <div class="dnode"><div class="dic">🎯</div><b>Transpose</b><span>fit the range</span></div>
    <div class="darrow"><span>map</span>▶</div>
    <div class="dnode"><div class="dic">⌨️</div><b>Key map</b><span>plain / Shift / Ctrl</span></div>
    <div class="darrow"><span>humanise</span>▶</div>
    <div class="dnode"><div class="dic">🎭</div><b>Pretender</b><span>human timing</span></div>
    <div class="darrow"><span>SendInput</span>▶</div>
    <div class="dnode accent"><div class="dic">🎹</div><b>Roblox piano</b><span>keys pressed</span></div>
  </div>

  <div class="how-notes">
    <div class="hn"><b>1 · Read the MIDI</b><p>RAMP parses the file into timed note events, builds a tempo map, and works out the best transposition for your range mode.</p></div>
    <div class="hn"><b>2 · Map notes to keys</b><p>Each MIDI note becomes a virtual-piano key — plain, Shift or Ctrl — exactly what the Roblox piano expects. PianoBinds can remap any of them.</p></div>
    <div class="hn"><b>3 · Humanise (optional)</b><p>Great Pretender re-rolls timing and dynamics so the performance sounds human, never mechanical.</p></div>
    <div class="hn"><b>4 · Send the keys</b><p>A locked, batched Windows <code>SendInput</code> pipeline fires the presses with millisecond timing — fast enough for black MIDI, without stealing Roblox's focus.</p></div>
  </div>
</div></section>

<!-- ARCHITECTURE -->
<section id="architecture"><div class="wrap">
  <div class="kicker">The open-source map</div>
  <h2>How the pieces fit together.</h2>
  <p class="lead">RAMP is open-source, so here's the whole thing at a glance — what each part does and how they connect. No code, just the map. Hover any node to see its job.</p>

  <div class="arch-legend">
    <span><i style="background:var(--ac)"></i> Interface</span>
    <span><i style="background:var(--teal)"></i> Playback core</span>
    <span><i style="background:#c084fc"></i> Input</span>
    <span><i style="background:#f59e0b"></i> Converters</span>
    <span><i style="background:#38bdf8"></i> Output</span>
  </div>

  <div class="arch-wrap">
    <svg id="arch" viewBox="0 0 900 620" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="RAMP architecture diagram"></svg>
    <div class="arch-tip" id="archtip"></div>
  </div>
</div></section>
<!-- SPECS -->
<section id="specs"><div class="wrap">
  <div class="kicker">The fine print</div>
  <h2>Specs &amp; numbers.</h2>
  <p class="lead">For the people who want the concrete details — here's exactly what RAMP does, in numbers.</p>

  <div class="spec-grid">
    <div class="spec-col">
      <h4>Playback</h4>
      <table class="modetable">
        <tr><td>Note range</td><td>MIDI 0–127 (128 notes)</td></tr>
        <tr><td>Range modes</td><td>5 (61-key → 128 Octave)</td></tr>
        <tr><td>Extended range</td><td>97 keys / MIDI 117 (Limit Breaker)</td></tr>
        <tr><td>Speed control</td><td>±0.01 to ±0.05 live steps</td></tr>
        <tr><td>Pretender presets</td><td>4 + custom blend</td></tr>
        <tr><td>Panic release</td><td>instant, one hotkey (F4)</td></tr>
      </table>
    </div>
    <div class="spec-col">
      <h4>Visualizer</h4>
      <table class="modetable">
        <tr><td>Throughput</td><td>10,000+ notes / second</td></tr>
        <tr><td>Frame rate</td><td>locked 60 fps</td></tr>
        <tr><td>Sources</td><td>player · live QWERTY · MIDI keyboard</td></tr>
        <tr><td>Per-track colour</td><td>yes, unlimited tracks</td></tr>
        <tr><td>Sustain tails</td><td>yes</td></tr>
        <tr><td>Focus mode</td><td>full-window clean view</td></tr>
      </table>
    </div>
    <div class="spec-col">
      <h4>Convert</h4>
      <table class="modetable">
        <tr><td>Audio formats</td><td>MP3 · WAV · M4A · FLAC · OGG</td></tr>
        <tr><td>Video formats</td><td>MP4 · MKV · MOV · WEBM · AVI</td></tr>
        <tr><td>Sheet formats</td><td>MuseScore · Sibelius PDF</td></tr>
        <tr><td>Runs</td><td>100% locally, no upload</td></tr>
        <tr><td>Video pipeline</td><td>9 visual stages</td></tr>
        <tr><td>PDF pipeline</td><td>7 stages, chord-aware</td></tr>
      </table>
    </div>
    <div class="spec-col">
      <h4>App</h4>
      <table class="modetable">
        <tr><td>Platform</td><td>Windows 10 / 11 (64-bit)</td></tr>
        <tr><td>Install</td><td>none — portable folder</td></tr>
        <tr><td>Feature tabs</td><td>11 + compact Simple mode</td></tr>
        <tr><td>Themes</td><td>11 presets + full custom</td></tr>
        <tr><td>Editable colours</td><td>15, plus fonts &amp; scale</td></tr>
        <tr><td>Updates</td><td>automatic from GitHub</td></tr>
      </table>
    </div>
  </div>
</div></section>
<section id="install"><div class="wrap">
  <div class="kicker">Get started</div>
  <h2>Installation.</h2>
  <p class="lead">RAMP is portable — there's no installer. Download, extract, run.</p>
  <div class="steps" style="margin-bottom:24px">
    <div class="step"><div class="n"></div><div><h3>Download the zip</h3><p>Grab <code>RAMP_release.zip</code> from the latest release.</p></div></div>
    <div class="step"><div class="n"></div><div><h3>Extract anywhere</h3><p>Unzip it to any folder — Desktop, Documents, wherever.</p></div></div>
    <div class="step"><div class="n"></div><div><h3>Run RAMP.exe</h3><p>Double-click and you're in. That's the whole install.</p></div></div>
  </div>
  <p style="color:var(--muted);margin-bottom:8px">Prefer to run from source or build your own exe?</p>
  <div class="codebox">
<span class="c"># run from source</span><br>
1. Install Python 3.13 (tick "Add to PATH")<br>
2. Run <b>Setup.bat</b> — installs dependencies<br>
3. Run <b>Start RAMP.bat</b><br><br>
<span class="c"># or build your own RAMP.exe</span><br>
Run <b>build_exe.bat</b>
  </div>
  <p style="color:var(--faint);font-size:13px;margin-top:16px">Requires Windows 10 / 11 (64-bit). Updates are automatic.</p>
</div></section>

<!-- PRICING -->
<section id="pricing"><div class="wrap">
  <div class="kicker">Free app · one optional unlock</div>
  <h2>RAMP is free. Limit Breaker is the only extra.</h2>
  <p class="lead">Everything on this page ships free and open-source. Limit Breaker is a one-time unlock for players who want to push past the standard range.</p>
  <div class="lb">
    <div class="pc">
      <h3>RAMP — Free</h3>
      <div class="price">£0</div>
      <ul>
        <li>The full auto-player &amp; all human-play features</li>
        <li>Audio, video &amp; PDF → MIDI</li>
        <li>Live MIDI keyboard + Bluetooth</li>
        <li>Visualizer, velocity, PianoBinds, theming</li>
        <li>Auto-updates, portable, open-source</li>
      </ul>
    </div>
    <div class="pc pro">
      <h3>Limit Breaker</h3>
      <div class="price">1,000 <span class="r">Robux</span></div>
      <ul>
        <li>Unlocks the extended <b>97-key range</b> (up to MIDI 117)</li>
        <li>Piano Haven keys for wider-range pianos</li>
        <li>One-time purchase, tied to your account</li>
        <li class="no">Not needed for normal 88-key play</li>
      </ul>
    </div>
  </div>
</div></section>

<!-- FAQ -->
<section id="faq"><div class="wrap">
  <div class="kicker">Questions</div>
  <h2>FAQ.</h2>
  <details><summary>Does RAMP work on every Roblox piano?</summary><p>RAMP targets standard virtual-piano keyboards and full 88-key pianos, with five range modes to match. Some games use custom layouts — PianoBinds lets you remap keys to fit them, and auto-transpose keeps songs in range.</p></details>
  <details><summary>Do I need to install anything?</summary><p>No. RAMP is portable — download, extract, run <code>RAMP.exe</code>. The audio→MIDI model is the only optional one-time download, and only if you use that feature.</p></details>
  <details><summary>Is it free?</summary><p>Yes, the whole app is free and open-source. The only paid extra is Limit Breaker (1,000 Robux) which unlocks the extended 97-key range — not needed for normal play.</p></details>
  <details><summary>Why does my antivirus flag it?</summary><p>It's a false positive. RAMP is a PyInstaller app that sends keystrokes (that's how it plays piano) and isn't code-signed yet, which trips heuristic scanners. It's open-source — read the code, watch its network, or build it yourself. See the Safety section below.</p></details>
  <details><summary>Can I play my own MIDI keyboard through it?</summary><p>Yes — the Connect tab. Plug in over USB or Bluetooth and RAMP presses the Roblox keys as you play, with live velocity and optional octave doubling.</p></details>
  <details><summary>Does the video/PDF converter upload my files?</summary><p>No. Both run entirely on your PC — nothing is uploaded.</p></details>
  <details><summary>How accurate is the video → MIDI converter?</summary><p>Very accurate on pitch and timing, because it reads the falling notes directly rather than guessing from audio. It shows you two live panels — what it sees and what it understands — so you can watch it work. For dynamics (how hard each note was played), turn on the optional audio cross-check.</p></details>
  <details><summary>Which sheet-music PDFs work best?</summary><p>PDFs exported from notation software — MuseScore, Sibelius, Finale — because RAMP reads the real note glyphs, not pixels. MuseScore 4 exports work best today. Scanned or photographed sheets aren't supported yet.</p></details>
  <details><summary>Can I use my own custom key layout?</summary><p>Yes — the PianoBinds tab remaps any of the 88 keys to match a game's NoteBinds panel. There are built-in presets, and you can build, save and export your own.</p></details>
  <details><summary>Will it get my Roblox account banned?</summary><p>RAMP sends key presses like a very fast typist — it doesn't inject into Roblox or modify the game. That said, always follow the rules of whatever experience you're playing in; some may have their own policies on autoplayers.</p></details>
  <details><summary>Does RAMP update itself?</summary><p>Yes. On launch it checks this repo's releases and offers any new version, so you're always current without re-downloading manually.</p></details>
</div></section>

<!-- SAFETY -->
<section id="safe"><div class="wrap">
  <div class="safe">
    <div class="sh">🛡️</div>
    <div>
      <h3>Is RAMP safe? Yes — and you can prove it.</h3>
      <p>RAMP never touches your browser, cookies, Roblox login, or passwords — there's no such code in it, and it's fully open-source so you can confirm that. Some antivirus tools flag it anyway because it's a PyInstaller app that sends keystrokes and isn't code-signed yet — a false positive. Read the code, watch its network (only a GitHub update check), or build it yourself. See <a href="#">SECURITY.md</a> for how false-positives get cleared, and only download from the official Releases page.</p>
    </div>
  </div>
</div></section>

<!-- DOWNLOAD -->
<section id="download" style="text-align:center;border:none"><div class="wrap">
  <div class="kicker" style="text-align:center">Ready when you are</div>
  <h2>Get RAMP v4.0.</h2>
  <p class="lead" style="margin:0 auto 28px">Extract anywhere, run <code>RAMP.exe</code>. That's the whole install.</p>
  <a href="#" class="btn btn-p" style="font-size:16px;padding:14px 28px">↓ Download RAMP_release.zip</a>
</div></section>

<footer><div class="wrap">
  <div>Not affiliated with or endorsed by Roblox Corporation. Use responsibly.</div>
  <div>RAMP v4.0 · by M7xt · open-source</div>
</div></footer>

<script>
/* ---- architecture spider-web ---- */
(function(){
  const svg=document.getElementById('arch');
  const tip=document.getElementById('archtip');
  const wrap=svg.parentElement;
  const NS='http://www.w3.org/2000/svg';
  const COL={ui:'#6366f1',core:'#1D9E75',input:'#c084fc',conv:'#f59e0b',out:'#38bdf8',hub:'#8b8dff'};

  // real RAMP modules, positioned as a web around the central app
  const cx=450, cy=310;
  const N={
    hub:{x:cx,y:cy,r:44,c:COL.hub,hub:true,name:'RAMP',sub:'the app',
      desc:'The main application. Ties every part together — the interface you see and the engines behind it.'},
    // interface ring (left)
    qt:{x:200,y:150,r:30,c:COL.ui,name:'Interface',sub:'ramp_qt',
      desc:'The whole window and all 11 tabs — Player, Connect, Visualizer, Transcribe, PianoBinds, Customize and the rest. What you actually click.'},
    launch:{x:150,y:300,r:24,c:COL.ui,name:'Launcher',sub:'ramp_launcher',
      desc:'Starts RAMP up, checks for updates, and hands off to the main window.'},
    sheet:{x:210,y:460,r:26,c:COL.ui,name:'Qwerty Sheet',sub:'ramp_sheet',
      desc:'Turns a MIDI into a letter sheet with playability levels and a practice mode.'},
    // playback core (top)
    player:{x:450,y:120,r:34,c:COL.core,name:'Player',sub:'ramp_player',
      desc:'The heart of playback. Reads the MIDI, times every note, humanises the performance, and decides which keys to press.'},
    engine:{x:640,y:150,r:28,c:COL.core,name:'MIDI engine',sub:'ramp_engine',
      desc:'Parses MIDI files into timed note events and builds the tempo map the Player follows.'},
    synth:{x:700,y:300,r:24,c:COL.core,name:'Sound',sub:'ramp_synth / sfz',
      desc:'Optional local sound — hear the MIDI as it plays, through soundfonts or a built-in synth.'},
    // input (bottom right)
    connect:{x:660,y:460,r:28,c:COL.input,name:'Connect',sub:'ramp_connect',
      desc:'Live play. Reads your real MIDI keyboard so RAMP presses the Roblox keys as you perform.'},
    ble:{x:770,y:410,r:20,c:COL.input,name:'Bluetooth',sub:'ramp_ble',
      desc:'Wireless MIDI — connect a keyboard over Bluetooth, no cable needed.'},
    live:{x:560,y:540,r:22,c:COL.input,name:'Live keys',sub:'ramp_livekeys',
      desc:'Handles the QWERTY live-play path and octave doubling.'},
    // converters (bottom left)
    transcribe:{x:340,y:540,r:26,c:COL.conv,name:'Transcribe',sub:'ramp_transcribe',
      desc:'The audio → MIDI path — turns a song into playable MIDI on your PC.'},
    synthesia:{x:180,y:560,r:24,c:COL.conv,name:'Video → MIDI',sub:'synthesia_engine',
      desc:'Reads the falling notes in a Synthesia-style video and rebuilds the MIDI, frame by frame.'},
    pdf:{x:100,y:440,r:22,c:COL.conv,name:'PDF → MIDI',sub:'pdf_to_midi',
      desc:'Reads noteheads, staves and clefs out of a sheet-music PDF and turns them into notes.'},
    audio:{x:430,y:600,r:18,c:COL.conv,name:'Audio check',sub:'audioverify',
      desc:'Cross-checks a video transcription against its soundtrack for real velocities.'},
    // output (right)
    send:{x:640,y:300,r:26,c:COL.out,name:'Key sender',sub:'sendinput_block',
      desc:'The output. Fires the actual key presses to Windows in fast, safe batches — what makes the piano play.'},
  };
  // connections (from -> to)
  const E=[
    ['hub','qt'],['hub','player'],['hub','launch'],['qt','sheet'],['qt','connect'],
    ['qt','transcribe'],['qt','customize'],['hub','launch'],
    ['player','engine'],['player','synth'],['player','send'],
    ['connect','ble'],['connect','live'],['connect','send'],['live','send'],
    ['transcribe','audio'],['transcribe','synthesia'],['transcribe','pdf'],
    ['synthesia','audio'],['qt','synthesia'],['qt','pdf'],
    ['player','qt'],['engine','send'],
  ].filter(([a,b])=>N[a]&&N[b]);

  // draw edges
  const edgeEls=[];
  E.forEach(([a,b])=>{
    const l=document.createElementNS(NS,'line');
    l.setAttribute('x1',N[a].x);l.setAttribute('y1',N[a].y);
    l.setAttribute('x2',N[b].x);l.setAttribute('y2',N[b].y);
    l.setAttribute('class','edge');l.dataset.a=a;l.dataset.b=b;
    svg.appendChild(l);edgeEls.push(l);
  });
  // draw nodes
  Object.entries(N).forEach(([k,n])=>{
    const g=document.createElementNS(NS,'g');
    g.setAttribute('class','node'+(n.hub?' hub':''));
    const c=document.createElementNS(NS,'circle');
    c.setAttribute('cx',n.x);c.setAttribute('cy',n.y);c.setAttribute('r',n.r);
    c.setAttribute('fill',n.hub?n.c:'var(--surf)');
    c.setAttribute('stroke',n.c);c.setAttribute('stroke-width',n.hub?0:2);
    if(n.hub)c.setAttribute('fill-opacity','1');
    g.appendChild(c);
    const t=document.createElementNS(NS,'text');
    t.setAttribute('x',n.x);t.setAttribute('y',n.y+(n.hub?2:-1));
    t.textContent=n.name;g.appendChild(t);
    if(n.sub){
      const s=document.createElementNS(NS,'text');
      s.setAttribute('x',n.x);s.setAttribute('y',n.y+(n.hub?16:11));
      s.setAttribute('class','sub');s.textContent=n.sub;g.appendChild(s);
    }
    if(!n.hub){
      g.addEventListener('mouseenter',()=>{
        tip.innerHTML='<b>'+n.name+' · '+n.sub+'</b><span>'+n.desc+'</span>';
        tip.classList.add('on');
        edgeEls.forEach(e=>e.classList.toggle('hot',e.dataset.a===k||e.dataset.b===k));
      });
      g.addEventListener('mousemove',(ev)=>{
        const r=wrap.getBoundingClientRect();
        let x=ev.clientX-r.left+14, y=ev.clientY-r.top+14;
        if(x+270>r.width)x=ev.clientX-r.left-274;
        tip.style.left=x+'px';tip.style.top=y+'px';
      });
      g.addEventListener('mouseleave',()=>{
        tip.classList.remove('on');
        edgeEls.forEach(e=>e.classList.remove('hot'));
      });
    }
    svg.appendChild(g);
  });
})();
</script>

<script>
  // highlight the active nav tab as you scroll
  const links=[...document.querySelectorAll('nav.tabs a')];
  const ids=links.map(a=>a.getAttribute('href').slice(1));
  const secs=ids.map(id=>document.getElementById(id)).filter(Boolean);
  const obs=new IntersectionObserver((es)=>{
    es.forEach(e=>{
      if(e.isIntersecting){
        const id=e.target.id;
        links.forEach(a=>a.classList.toggle('on',a.getAttribute('href')==='#'+id));
      }
    });
  },{rootMargin:'-45% 0px -50% 0px'});
  secs.forEach(s=>obs.observe(s));
</script>
<script>
/* ---- click RAMP wordmark to expand to full name ---- */
(function(){
  const w=document.getElementById('wordmark');
  if(!w)return;
  w.addEventListener('click',function(ev){
    ev.preventDefault();          // don't jump to top; just toggle the name
    ev.stopPropagation();
    w.classList.toggle('expanded');
  });
})();
</script>
</body>
</html>
