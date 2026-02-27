# galSheli.github.io
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>PM Brand Theme — Style Guide & Preview</title>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,500;0,9..144,700;1,9..144,400&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  /* ============================================
     GOOGLE SITES THEME — PRODUCT MANAGER
     Palette: Energetic Clean + Soft Neutrals
     ============================================ */

  :root {
    --cream:     #F7F3EE;
    --cream-mid: #EDE7DC;
    --sage:      #8FAF8C;
    --sage-deep: #5C7A59;
    --blush:     #D4A89A;
    --blush-light: #F0D5CE;
    --charcoal:  #2C2C2C;
    --stone:     #7A7060;
    --white:     #FFFFFF;

    --font-display: 'Fraunces', Georgia, serif;
    --font-body:    'DM Sans', sans-serif;

    --radius-sm: 6px;
    --radius-md: 14px;
    --radius-lg: 28px;
    --shadow:    0 4px 24px rgba(44,44,44,0.08);
    --shadow-md: 0 8px 40px rgba(44,44,44,0.12);
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    background: var(--cream);
    color: var(--charcoal);
    font-family: var(--font-body);
    font-weight: 300;
    line-height: 1.7;
    overflow-x: hidden;
  }

  /* ─── NAVIGATION ─── */
  nav {
    position: sticky; top: 0; z-index: 100;
    background: rgba(247,243,238,0.88);
    backdrop-filter: blur(14px);
    border-bottom: 1px solid var(--cream-mid);
    padding: 0 48px;
    display: flex; align-items: center; justify-content: space-between;
    height: 64px;
  }
  .nav-logo {
    font-family: var(--font-display);
    font-weight: 700; font-size: 1.2rem;
    color: var(--charcoal);
    letter-spacing: -0.02em;
  }
  .nav-logo span { color: var(--sage-deep); }
  .nav-links { display: flex; gap: 36px; list-style: none; }
  .nav-links a {
    font-size: 0.85rem; font-weight: 500; letter-spacing: 0.06em; text-transform: uppercase;
    color: var(--stone); text-decoration: none;
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--sage-deep); }

  /* ─── HERO ─── */
  .hero {
    min-height: 92vh;
    display: grid; grid-template-columns: 1fr 1fr; align-items: center;
    padding: 80px 48px;
    gap: 60px;
    position: relative; overflow: hidden;
  }
  .hero::before {
    content: '';
    position: absolute; top: -120px; right: -80px;
    width: 520px; height: 520px; border-radius: 50%;
    background: radial-gradient(circle, var(--blush-light) 0%, transparent 70%);
    pointer-events: none;
  }
  .hero::after {
    content: '';
    position: absolute; bottom: -60px; left: 30%;
    width: 300px; height: 300px; border-radius: 50%;
    background: radial-gradient(circle, rgba(143,175,140,0.2) 0%, transparent 70%);
    pointer-events: none;
  }
  .hero-text { position: relative; z-index: 1; }
  .hero-eyebrow {
    display: inline-block;
    font-size: 0.75rem; font-weight: 500; letter-spacing: 0.12em; text-transform: uppercase;
    color: var(--sage-deep);
    background: rgba(143,175,140,0.15);
    padding: 6px 14px; border-radius: 40px;
    margin-bottom: 24px;
    animation: fadeUp 0.6s ease both;
  }
  .hero h1 {
    font-family: var(--font-display);
    font-size: clamp(3rem, 6vw, 5rem);
    font-weight: 700; line-height: 1.05;
    letter-spacing: -0.03em;
    color: var(--charcoal);
    animation: fadeUp 0.7s 0.1s ease both;
  }
  .hero h1 em {
    font-style: italic; font-weight: 300;
    color: var(--sage-deep);
  }
  .hero-sub {
    margin-top: 20px;
    font-size: 1.05rem; color: var(--stone); max-width: 440px;
    animation: fadeUp 0.7s 0.2s ease both;
  }
  .hero-actions {
    margin-top: 40px; display: flex; gap: 16px; flex-wrap: wrap;
    animation: fadeUp 0.7s 0.3s ease both;
  }

  /* ─── BUTTONS ─── */
  .btn {
    display: inline-flex; align-items: center; gap: 8px;
    padding: 14px 28px; border-radius: var(--radius-lg);
    font-family: var(--font-body); font-size: 0.9rem; font-weight: 500;
    text-decoration: none; cursor: pointer; border: none;
    transition: transform 0.2s, box-shadow 0.2s;
  }
  .btn:hover { transform: translateY(-2px); }
  .btn-primary {
    background: var(--charcoal); color: var(--white);
    box-shadow: 0 4px 16px rgba(44,44,44,0.2);
  }
  .btn-primary:hover { box-shadow: 0 8px 28px rgba(44,44,44,0.28); }
  .btn-secondary {
    background: transparent; color: var(--charcoal);
    border: 1.5px solid var(--cream-mid);
  }
  .btn-secondary:hover { background: var(--cream-mid); }
  .btn-sage {
    background: var(--sage); color: var(--white);
    box-shadow: 0 4px 16px rgba(92,122,89,0.25);
  }
  .btn-sage:hover { box-shadow: 0 8px 24px rgba(92,122,89,0.35); }

  /* ─── HERO IMAGE / CARD ─── */
  .hero-card {
    position: relative; z-index: 1;
    background: var(--white);
    border-radius: var(--radius-lg);
    box-shadow: var(--shadow-md);
    padding: 40px;
    animation: fadeUp 0.8s 0.2s ease both;
  }
  .hero-card-tag {
    font-size: 0.72rem; font-weight: 500; letter-spacing: 0.1em; text-transform: uppercase;
    color: var(--blush); margin-bottom: 16px;
  }
  .hero-card h3 {
    font-family: var(--font-display); font-size: 1.6rem; font-weight: 500;
    letter-spacing: -0.02em; margin-bottom: 12px;
  }
  .hero-card p { font-size: 0.9rem; color: var(--stone); margin-bottom: 24px; }
  .stat-row { display: flex; gap: 28px; }
  .stat { }
  .stat-num {
    font-family: var(--font-display); font-size: 2rem; font-weight: 700;
    color: var(--sage-deep); letter-spacing: -0.04em;
  }
  .stat-label { font-size: 0.78rem; color: var(--stone); }
  .card-bar {
    margin-top: 28px;
    background: var(--cream); border-radius: 8px; padding: 16px;
  }
  .bar-label { font-size: 0.78rem; font-weight: 500; color: var(--stone); margin-bottom: 8px; display: flex; justify-content: space-between; }
  .bar-track { background: var(--cream-mid); border-radius: 99px; height: 6px; overflow: hidden; }
  .bar-fill { height: 100%; border-radius: 99px; background: linear-gradient(90deg, var(--sage), var(--blush)); transition: width 1s ease; }

  /* ─── SECTION WRAPPER ─── */
  section { padding: 100px 48px; }
  .section-label {
    font-size: 0.72rem; font-weight: 500; letter-spacing: 0.12em; text-transform: uppercase;
    color: var(--sage-deep); margin-bottom: 12px;
  }
  .section-title {
    font-family: var(--font-display);
    font-size: clamp(2rem, 4vw, 3rem);
    font-weight: 700; letter-spacing: -0.03em;
    line-height: 1.1; max-width: 600px;
  }
  .section-title em { font-style: italic; font-weight: 300; color: var(--blush); }

  /* ─── COLOR PALETTE ─── */
  .palette-section { background: var(--white); }
  .swatch-grid {
    display: flex; gap: 16px; margin-top: 40px; flex-wrap: wrap;
  }
  .swatch {
    flex: 1; min-width: 120px; border-radius: var(--radius-md);
    overflow: hidden; box-shadow: var(--shadow);
  }
  .swatch-color { height: 100px; }
  .swatch-info { padding: 12px 14px; background: var(--cream); }
  .swatch-name { font-size: 0.8rem; font-weight: 500; }
  .swatch-hex { font-size: 0.72rem; color: var(--stone); font-family: monospace; }

  /* ─── TYPOGRAPHY ─── */
  .type-section { background: var(--cream); }
  .type-samples { margin-top: 40px; display: flex; flex-direction: column; gap: 32px; }
  .type-sample { border-left: 2px solid var(--cream-mid); padding-left: 24px; }
  .type-meta { font-size: 0.72rem; color: var(--stone); margin-bottom: 6px; letter-spacing: 0.08em; text-transform: uppercase; }

  /* ─── COMPONENTS ─── */
  .comp-section { background: var(--white); }
  .comp-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 24px; margin-top: 40px; }

  /* Card Component */
  .card {
    background: var(--cream);
    border-radius: var(--radius-md);
    padding: 28px;
    transition: transform 0.2s, box-shadow 0.2s;
    cursor: default;
  }
  .card:hover { transform: translateY(-4px); box-shadow: var(--shadow-md); }
  .card-icon {
    width: 44px; height: 44px; border-radius: 12px;
    display: flex; align-items: center; justify-content: center;
    font-size: 1.2rem; margin-bottom: 16px;
  }
  .card-icon.sage { background: rgba(143,175,140,0.2); }
  .card-icon.blush { background: rgba(212,168,154,0.2); }
  .card-icon.cream { background: var(--cream-mid); }
  .card h4 { font-family: var(--font-display); font-size: 1.1rem; font-weight: 500; margin-bottom: 8px; }
  .card p { font-size: 0.88rem; color: var(--stone); }

  /* Tag / Chip */
  .tag {
    display: inline-block;
    font-size: 0.75rem; font-weight: 500; letter-spacing: 0.04em;
    padding: 5px 12px; border-radius: 40px;
  }
  .tag-sage { background: rgba(143,175,140,0.18); color: var(--sage-deep); }
  .tag-blush { background: rgba(212,168,154,0.18); color: #9C5E52; }
  .tag-stone { background: var(--cream-mid); color: var(--stone); }

  /* ─── GOOGLE SITES GUIDE ─── */
  .guide-section { background: var(--cream-mid); }
  .guide-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 32px; margin-top: 40px; }
  .guide-block {
    background: var(--white); border-radius: var(--radius-md); padding: 28px;
  }
  .guide-block h4 {
    font-family: var(--font-display); font-size: 1rem; font-weight: 500; margin-bottom: 16px;
    padding-bottom: 12px; border-bottom: 1px solid var(--cream-mid);
  }
  .guide-row { display: flex; justify-content: space-between; align-items: center; padding: 8px 0; border-bottom: 1px solid var(--cream); font-size: 0.85rem; }
  .guide-row:last-child { border-bottom: none; }
  .guide-row span:first-child { color: var(--stone); }
  .guide-row span:last-child { font-weight: 500; font-family: monospace; font-size: 0.8rem; }
  .color-dot {
    display: inline-block; width: 14px; height: 14px; border-radius: 50%;
    margin-right: 6px; vertical-align: middle;
  }

  /* ─── FOOTER ─── */
  footer {
    background: var(--charcoal); color: rgba(255,255,255,0.6);
    padding: 40px 48px;
    display: flex; justify-content: space-between; align-items: center;
    font-size: 0.82rem;
  }
  footer .logo { font-family: var(--font-display); font-size: 1rem; font-weight: 700; color: var(--white); }

  /* ─── ANIMATIONS ─── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(20px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  @media (max-width: 768px) {
    .hero { grid-template-columns: 1fr; padding: 60px 24px; }
    nav { padding: 0 24px; }
    nav .nav-links { display: none; }
    section { padding: 60px 24px; }
    .guide-grid { grid-template-columns: 1fr; }
    footer { flex-direction: column; gap: 12px; text-align: center; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">Jane <span>Doe</span></div>
  <ul class="nav-links">
    <li><a href="#">Work</a></li>
    <li><a href="#">About</a></li>
    <li><a href="#">Writing</a></li>
    <li><a href="#">Contact</a></li>
  </ul>
  <a href="#" class="btn btn-primary" style="padding:10px 20px;font-size:0.82rem;">Let's Talk</a>
</nav>

<!-- HERO -->
<div class="hero">
  <div class="hero-text">
    <div class="hero-eyebrow">Product Manager · Strategist</div>
    <h1>Building products <em>people love</em></h1>
    <p class="hero-sub">I bridge user needs, business goals, and engineering to ship products that actually matter.</p>
    <div class="hero-actions">
      <a href="#" class="btn btn-primary">View My Work →</a>
      <a href="#" class="btn btn-secondary">Download Resume</a>
    </div>
  </div>
  <div class="hero-card">
    <div class="hero-card-tag">✦ Current Focus</div>
    <h3>Growth & Retention</h3>
    <p>Leading 0→1 features that drive user activation and long-term engagement.</p>
    <div class="stat-row">
      <div class="stat">
        <div class="stat-num">3×</div>
        <div class="stat-label">Retention lift</div>
      </div>
      <div class="stat">
        <div class="stat-num">12+</div>
        <div class="stat-label">Features shipped</div>
      </div>
      <div class="stat">
        <div class="stat-num">4</div>
        <div class="stat-label">Years in PM</div>
      </div>
    </div>
    <div class="card-bar">
      <div class="bar-label"><span>User Satisfaction Score</span><span>94%</span></div>
      <div class="bar-track"><div class="bar-fill" style="width:94%"></div></div>
    </div>
  </div>
</div>

<!-- COLOR PALETTE -->
<section class="palette-section">
  <div class="section-label">Brand System</div>
  <h2 class="section-title">Your Color <em>Palette</em></h2>
  <div class="swatch-grid">
    <div class="swatch">
      <div class="swatch-color" style="background:#F7F3EE"></div>
      <div class="swatch-info"><div class="swatch-name">Cream</div><div class="swatch-hex">#F7F3EE</div></div>
    </div>
    <div class="swatch">
      <div class="swatch-color" style="background:#EDE7DC"></div>
      <div class="swatch-info"><div class="swatch-name">Cream Mid</div><div class="swatch-hex">#EDE7DC</div></div>
    </div>
    <div class="swatch">
      <div class="swatch-color" style="background:#8FAF8C"></div>
      <div class="swatch-info"><div class="swatch-name">Sage</div><div class="swatch-hex">#8FAF8C</div></div>
    </div>
    <div class="swatch">
      <div class="swatch-color" style="background:#5C7A59"></div>
      <div class="swatch-info"><div class="swatch-name">Sage Deep</div><div class="swatch-hex">#5C7A59</div></div>
    </div>
    <div class="swatch">
      <div class="swatch-color" style="background:#D4A89A"></div>
      <div class="swatch-info"><div class="swatch-name">Blush</div><div class="swatch-hex">#D4A89A</div></div>
    </div>
    <div class="swatch">
      <div class="swatch-color" style="background:#2C2C2C"></div>
      <div class="swatch-info"><div class="swatch-name">Charcoal</div><div class="swatch-hex">#2C2C2C</div></div>
    </div>
  </div>
</section>

<!-- TYPOGRAPHY -->
<section class="type-section">
  <div class="section-label">Typography</div>
  <h2 class="section-title">Fonts That <em>Speak</em></h2>
  <div class="type-samples">
    <div class="type-sample">
      <div class="type-meta">Display — Fraunces (Google Font)</div>
      <div style="font-family:'Fraunces',serif;font-size:2.8rem;font-weight:700;letter-spacing:-0.03em;line-height:1.1">
        Heading One Style
      </div>
    </div>
    <div class="type-sample">
      <div class="type-meta">Display Italic — Fraunces Light Italic</div>
      <div style="font-family:'Fraunces',serif;font-size:2rem;font-weight:300;font-style:italic;color:#5C7A59">
        Subheading accent style
      </div>
    </div>
    <div class="type-sample">
      <div class="type-meta">Body — DM Sans (Google Font)</div>
      <div style="font-family:'DM Sans',sans-serif;font-size:1rem;font-weight:300;color:#7A7060;max-width:560px">
        Body copy should feel airy and readable. Use light weight (300) for long paragraphs and medium (500) for emphasis and UI labels.
      </div>
    </div>
    <div class="type-sample">
      <div class="type-meta">Label / Tag — DM Sans Medium Uppercase</div>
      <div style="font-family:'DM Sans',sans-serif;font-size:0.72rem;font-weight:500;letter-spacing:0.12em;text-transform:uppercase;color:#5C7A59">
        Section Label · Product Manager · Tag Text
      </div>
    </div>
  </div>
</section>

<!-- COMPONENTS -->
<section class="comp-section">
  <div class="section-label">UI Components</div>
  <h2 class="section-title">Building <em>Blocks</em></h2>

  <!-- Buttons row -->
  <div style="display:flex;gap:16px;flex-wrap:wrap;margin:32px 0 48px;">
    <a href="#" class="btn btn-primary">Primary Action</a>
    <a href="#" class="btn btn-secondary">Secondary</a>
    <a href="#" class="btn btn-sage">Sage CTA</a>
  </div>

  <!-- Tags row -->
  <div style="display:flex;gap:10px;flex-wrap:wrap;margin-bottom:48px;">
    <span class="tag tag-sage">Product Strategy</span>
    <span class="tag tag-blush">User Research</span>
    <span class="tag tag-stone">Roadmapping</span>
    <span class="tag tag-sage">0→1 Products</span>
    <span class="tag tag-blush">Data-Driven</span>
    <span class="tag tag-stone">Agile / Scrum</span>
  </div>

  <!-- Cards -->
  <div class="comp-grid">
    <div class="card">
      <div class="card-icon sage">🎯</div>
      <h4>Strategy & Vision</h4>
      <p>Defining product direction with clear north stars, OKRs, and measurable outcomes.</p>
    </div>
    <div class="card">
      <div class="card-icon blush">🔬</div>
      <h4>User Research</h4>
      <p>Turning qualitative insights into quantitative signals that inform every decision.</p>
    </div>
    <div class="card">
      <div class="card-icon cream">🚀</div>
      <h4>Execution</h4>
      <p>Shipping fast, iterating faster — keeping teams aligned and stakeholders informed.</p>
    </div>
  </div>
</section>

<!-- GOOGLE SITES SETUP GUIDE -->
<section class="guide-section">
  <div class="section-label">Google Sites Setup</div>
  <h2 class="section-title">How to Apply <em>This Theme</em></h2>
  <div class="guide-grid">

    <div class="guide-block">
      <h4>🎨 Colors to Set in Google Sites</h4>
      <div class="guide-row">
        <span>Page Background</span>
        <span><span class="color-dot" style="background:#F7F3EE"></span>#F7F3EE</span>
      </div>
      <div class="guide-row">
        <span>Header / Nav Background</span>
        <span><span class="color-dot" style="background:#F7F3EE"></span>#F7F3EE</span>
      </div>
      <div class="guide-row">
        <span>Header Text / Logo</span>
        <span><span class="color-dot" style="background:#2C2C2C"></span>#2C2C2C</span>
      </div>
      <div class="guide-row">
        <span>Button / Accent Color</span>
        <span><span class="color-dot" style="background:#5C7A59"></span>#5C7A59</span>
      </div>
      <div class="guide-row">
        <span>Section Alt Background</span>
        <span><span class="color-dot" style="background:#EDE7DC"></span>#EDE7DC</span>
      </div>
      <div class="guide-row">
        <span>Highlight / Accent</span>
        <span><span class="color-dot" style="background:#D4A89A"></span>#D4A89A</span>
      </div>
    </div>

    <div class="guide-block">
      <h4>🔡 Fonts to Set in Google Sites</h4>
      <div class="guide-row">
        <span>Heading Font</span>
        <span>Fraunces</span>
      </div>
      <div class="guide-row">
        <span>Body Font</span>
        <span>DM Sans</span>
      </div>
      <div class="guide-row">
        <span>H1 Size</span>
        <span>48–64px</span>
      </div>
      <div class="guide-row">
        <span>H2 Size</span>
        <span>32–40px</span>
      </div>
      <div class="guide-row">
        <span>Body Size</span>
        <span>16px</span>
      </div>
      <div class="guide-row">
        <span>Font Weight (body)</span>
        <span>300 / Light</span>
      </div>
    </div>

    <div class="guide-block">
      <h4>📐 Layout Tips</h4>
      <div class="guide-row"><span>Content width</span><span>Max 1140px</span></div>
      <div class="guide-row"><span>Section padding</span><span>80–100px top/bottom</span></div>
      <div class="guide-row"><span>Card border-radius</span><span>14–28px (rounded)</span></div>
      <div class="guide-row"><span>White space</span><span>Generous — don't crowd</span></div>
      <div class="guide-row"><span>Column layouts</span><span>1 or 2 cols max</span></div>
    </div>

    <div class="guide-block">
      <h4>✦ Brand Voice Tips</h4>
      <div class="guide-row"><span>Headlines</span><span>Confident + warm</span></div>
      <div class="guide-row"><span>Body copy</span><span>Clear, no jargon</span></div>
      <div class="guide-row"><span>CTA buttons</span><span>Action-oriented</span></div>
      <div class="guide-row"><span>Section labels</span><span>ALL CAPS, sage color</span></div>
      <div class="guide-row"><span>Imagery style</span><span>Natural, warm tones</span></div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="logo">Your Name</div>
  <div>Product Manager · Personal Site Theme</div>
  <div>Built with intention ✦</div>
</footer>

</body>
</html>
