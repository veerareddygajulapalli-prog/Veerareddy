<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Veera Reddy Gajulapalli — Full Stack & AI Developer</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;700&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #0D1117;
    --surface: #161B22;
    --surface2: #1C2333;
    --border: #30363D;
    --amber: #F0A500;
    --amber-dim: rgba(240,165,0,0.12);
    --blue: #58A6FF;
    --green: #3FB950;
    --text: #E6EDF3;
    --muted: #8B949E;
    --radius: 10px;
  }

  html { scroll-behavior: smooth; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Inter', sans-serif;
    font-size: 16px;
    line-height: 1.6;
    min-height: 100vh;
  }

  /* ── NAV ─────────────────────────────────────────── */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    background: rgba(13,17,23,0.85);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--border);
    padding: 0 2rem;
    height: 56px;
    display: flex; align-items: center; justify-content: space-between;
  }
  .nav-logo {
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.95rem;
    color: var(--amber);
    letter-spacing: 0.04em;
  }
  .nav-links { display: flex; gap: 1.8rem; list-style: none; }
  .nav-links a {
    color: var(--muted); text-decoration: none; font-size: 0.85rem;
    font-weight: 500; letter-spacing: 0.03em;
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--text); }

  /* ── HERO ────────────────────────────────────────── */
  .hero {
    min-height: 100vh;
    display: flex; align-items: center;
    padding: 5rem 2rem 3rem;
    max-width: 900px;
    margin: 0 auto;
  }
  .hero-inner { width: 100%; }

  .terminal-tag {
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.82rem;
    color: var(--green);
    margin-bottom: 1.4rem;
    display: flex; align-items: center; gap: 0.5rem;
  }
  .terminal-tag::before {
    content: '>';
    color: var(--amber);
    font-weight: 700;
  }

  .hero h1 {
    font-size: clamp(2.4rem, 6vw, 4rem);
    font-weight: 700;
    line-height: 1.1;
    letter-spacing: -0.02em;
    color: var(--text);
    margin-bottom: 0.5rem;
  }
  .hero h1 span { color: var(--amber); }

  .hero-subtitle {
    font-family: 'JetBrains Mono', monospace;
    font-size: 1.05rem;
    color: var(--blue);
    margin-bottom: 1.5rem;
    font-weight: 500;
  }

  .hero-desc {
    max-width: 560px;
    color: var(--muted);
    font-size: 1rem;
    line-height: 1.75;
    margin-bottom: 2.2rem;
  }

  .hero-cta { display: flex; gap: 1rem; flex-wrap: wrap; }

  .btn {
    display: inline-flex; align-items: center; gap: 0.4rem;
    padding: 0.65rem 1.4rem;
    border-radius: 6px;
    font-size: 0.875rem;
    font-weight: 600;
    text-decoration: none;
    transition: all 0.2s;
    cursor: pointer;
    border: none;
  }
  .btn-primary { background: var(--amber); color: #0D1117; }
  .btn-primary:hover { background: #ffc234; transform: translateY(-1px); }
  .btn-outline { background: transparent; color: var(--text); border: 1px solid var(--border); }
  .btn-outline:hover { border-color: var(--amber); color: var(--amber); }

  .meta-row {
    display: flex; gap: 1.8rem; flex-wrap: wrap;
    margin-top: 3rem;
    padding-top: 2rem;
    border-top: 1px solid var(--border);
  }
  .meta-item { display: flex; flex-direction: column; }
  .meta-label {
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.72rem;
    color: var(--muted);
    text-transform: uppercase;
    letter-spacing: 0.08em;
    margin-bottom: 0.2rem;
  }
  .meta-value { font-size: 0.9rem; font-weight: 500; color: var(--text); }

  /* ── SECTION SHELL ───────────────────────────────── */
  section {
    max-width: 900px;
    margin: 0 auto;
    padding: 5rem 2rem;
    border-top: 1px solid var(--border);
  }
  .section-eyebrow {
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.75rem;
    color: var(--amber);
    text-transform: uppercase;
    letter-spacing: 0.12em;
    margin-bottom: 0.8rem;
  }
  .section-title {
    font-size: 1.85rem;
    font-weight: 700;
    letter-spacing: -0.02em;
    margin-bottom: 2.5rem;
    color: var(--text);
  }

  /* ── SKILLS ──────────────────────────────────────── */
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    gap: 1rem;
  }
  .skill-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: var(--radius);
    padding: 1.2rem 1.4rem;
    transition: border-color 0.2s, transform 0.2s;
  }
  .skill-card:hover { border-color: var(--amber); transform: translateY(-2px); }
  .skill-card-label {
    font-size: 0.72rem;
    font-family: 'JetBrains Mono', monospace;
    color: var(--muted);
    text-transform: uppercase;
    letter-spacing: 0.08em;
    margin-bottom: 0.6rem;
  }
  .skill-card-name { font-size: 0.95rem; font-weight: 600; color: var(--text); }
  .skill-dot {
    display: inline-block; width: 8px; height: 8px;
    border-radius: 50%; margin-right: 0.5rem;
  }
  .dot-amber { background: var(--amber); }
  .dot-blue  { background: var(--blue); }
  .dot-green { background: var(--green); }

  /* ── PROJECTS ────────────────────────────────────── */
  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(380px, 1fr));
    gap: 1.4rem;
  }
  .project-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: var(--radius);
    padding: 1.8rem;
    display: flex; flex-direction: column;
    transition: border-color 0.2s, transform 0.2s;
    position: relative;
    overflow: hidden;
  }
  .project-card::before {
    content: '';
    position: absolute; top: 0; left: 0; right: 0; height: 3px;
    background: linear-gradient(90deg, var(--amber), transparent);
    opacity: 0; transition: opacity 0.2s;
  }
  .project-card:hover { border-color: var(--amber); transform: translateY(-3px); }
  .project-card:hover::before { opacity: 1; }
  .project-icon { font-size: 1.8rem; margin-bottom: 1rem; }
  .project-title { font-size: 1.1rem; font-weight: 700; margin-bottom: 0.5rem; color: var(--text); }
  .project-desc { font-size: 0.9rem; color: var(--muted); line-height: 1.7; margin-bottom: 1.2rem; flex: 1; }
  .tag-row { display: flex; flex-wrap: wrap; gap: 0.5rem; margin-bottom: 1.4rem; }
  .tag {
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.72rem;
    background: var(--surface2);
    border: 1px solid var(--border);
    color: var(--blue);
    padding: 0.2rem 0.6rem;
    border-radius: 4px;
  }
  .project-link {
    font-size: 0.82rem; font-weight: 600;
    color: var(--amber); text-decoration: none;
    display: inline-flex; align-items: center; gap: 0.3rem;
    transition: gap 0.2s;
  }
  .project-link:hover { gap: 0.6rem; }

  /* ── ACHIEVEMENTS ────────────────────────────────── */
  .ach-list { display: flex; flex-direction: column; gap: 1rem; }
  .ach-item {
    display: flex; align-items: flex-start; gap: 1rem;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: var(--radius);
    padding: 1.2rem 1.4rem;
  }
  .ach-badge {
    flex-shrink: 0;
    width: 36px; height: 36px;
    background: var(--amber-dim);
    border: 1px solid var(--amber);
    border-radius: 8px;
    display: flex; align-items: center; justify-content: center;
    font-size: 1rem;
  }
  .ach-text { font-size: 0.9rem; color: var(--muted); }
  .ach-text strong { color: var(--text); font-weight: 600; }

  /* ── CONTACT ─────────────────────────────────────── */
  .contact-inner {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 3rem;
    align-items: start;
  }
  .contact-blurb { font-size: 0.95rem; color: var(--muted); line-height: 1.8; margin-bottom: 1.5rem; }
  .contact-links { display: flex; flex-direction: column; gap: 0.75rem; }
  .contact-link {
    display: flex; align-items: center; gap: 0.75rem;
    color: var(--text); text-decoration: none;
    font-size: 0.9rem;
    padding: 0.75rem 1rem;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: var(--radius);
    transition: border-color 0.2s, color 0.2s;
  }
  .contact-link:hover { border-color: var(--amber); color: var(--amber); }
  .contact-link-icon { font-size: 1.1rem; }
  .contact-status {
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.8rem;
    color: var(--green);
    display: flex; align-items: center; gap: 0.5rem;
    margin-bottom: 1.2rem;
  }
  .status-dot {
    width: 8px; height: 8px; border-radius: 50%;
    background: var(--green);
    animation: pulse 2s infinite;
  }
  @keyframes pulse {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.3; }
  }

  /* ── FOOTER ──────────────────────────────────────── */
  footer {
    text-align: center;
    padding: 2rem;
    border-top: 1px solid var(--border);
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.78rem;
    color: var(--muted);
  }

  /* ── CURSOR BLINK ────────────────────────────────── */
  .cursor {
    display: inline-block;
    width: 2px; height: 1em;
    background: var(--amber);
    margin-left: 2px;
    vertical-align: text-bottom;
    animation: blink 1s step-end infinite;
  }
  @keyframes blink { 50% { opacity: 0; } }

  /* ── RESPONSIVE ──────────────────────────────────── */
  @media (max-width: 640px) {
    nav { padding: 0 1rem; }
    .nav-links { gap: 1rem; }
    .nav-links a { font-size: 0.78rem; }
    section { padding: 3.5rem 1.2rem; }
    .projects-grid { grid-template-columns: 1fr; }
    .contact-inner { grid-template-columns: 1fr; }
    .hero { padding: 5rem 1.2rem 2rem; }
  }

  @media (prefers-reduced-motion: reduce) {
    .cursor, .status-dot { animation: none; }
    * { transition: none !important; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <span class="nav-logo">veera.dev</span>
  <ul class="nav-links">
    <li><a href="#skills">Skills</a></li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#achievements">Achievements</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<div class="hero">
  <div class="hero-inner">
    <p class="terminal-tag">Full Stack Developer &amp; AI/ML Engineer</p>
    <h1>Gajulapalli<br><span>Veera Reddy</span></h1>
    <p class="hero-subtitle">// building with code &amp; curiosity<span class="cursor"></span></p>
    <p class="hero-desc">
      Final year CSE student at Kalasalingam University, passionate about building
      scalable web applications and AI-powered tools that solve real-world problems.
      Currently exploring Java Full Stack, Machine Learning, and Cloud Computing.
    </p>
    <div class="hero-cta">
      <a href="https://drive.google.com/file/d/1M9yWVTBY2d-9pgFJRCUL0gr_17NgYocc/view" target="_blank" class="btn btn-primary">
        ↓ Resume
      </a>
      <a href="#contact" class="btn btn-outline">Get in touch</a>
    </div>
    <div class="meta-row">
      <div class="meta-item">
        <span class="meta-label">Location</span>
        <span class="meta-value">Hyderabad, India</span>
      </div>
      <div class="meta-item">
        <span class="meta-label">University</span>
        <span class="meta-value">Kalasalingam University</span>
      </div>
      <div class="meta-item">
        <span class="meta-label">Degree</span>
        <span class="meta-value">B.Tech CSE</span>
      </div>
      <div class="meta-item">
        <span class="meta-label">Status</span>
        <span class="meta-value" style="color: var(--green)">Open to work</span>
      </div>
    </div>
  </div>
</div>

<!-- SKILLS -->
<section id="skills">
  <p class="section-eyebrow">Tech Stack</p>
  <h2 class="section-title">Skills &amp; Tools</h2>
  <div class="skills-grid">
    <div class="skill-card">
      <p class="skill-card-label">Language</p>
      <p class="skill-card-name"><span class="skill-dot dot-amber"></span>Java</p>
    </div>
    <div class="skill-card">
      <p class="skill-card-label">Frontend</p>
      <p class="skill-card-name"><span class="skill-dot dot-blue"></span>HTML5 / CSS3</p>
    </div>
    <div class="skill-card">
      <p class="skill-card-label">Frontend</p>
      <p class="skill-card-name"><span class="skill-dot dot-blue"></span>JavaScript</p>
    </div>
    <div class="skill-card">
      <p class="skill-card-label">Database</p>
      <p class="skill-card-name"><span class="skill-dot dot-amber"></span>MySQL</p>
    </div>
    <div class="skill-card">
      <p class="skill-card-label">AI / NLP</p>
      <p class="skill-card-name"><span class="skill-dot dot-green"></span>Gemini AI</p>
    </div>
    <div class="skill-card">
      <p class="skill-card-label">AI / NLP</p>
      <p class="skill-card-name"><span class="skill-dot dot-green"></span>NLP &amp; OCR</p>
    </div>
    <div class="skill-card">
      <p class="skill-card-label">Version Control</p>
      <p class="skill-card-name"><span class="skill-dot dot-amber"></span>Git &amp; GitHub</p>
    </div>
    <div class="skill-card">
      <p class="skill-card-label">Editor</p>
      <p class="skill-card-name"><span class="skill-dot dot-blue"></span>VS Code</p>
    </div>
    <div class="skill-card">
      <p class="skill-card-label">Learning</p>
      <p class="skill-card-name"><span class="skill-dot dot-green"></span>Machine Learning</p>
    </div>
    <div class="skill-card">
      <p class="skill-card-label">Learning</p>
      <p class="skill-card-name"><span class="skill-dot dot-green"></span>Cloud Computing</p>
    </div>
  </div>
</section>

<!-- PROJECTS -->
<section id="projects">
  <p class="section-eyebrow">Work</p>
  <h2 class="section-title">Featured Projects</h2>
  <div class="projects-grid">
    <div class="project-card">
      <div class="project-icon">🧠</div>
      <h3 class="project-title">AI Exam Question Generator</h3>
      <p class="project-desc">
        Intelligent question paper generation from uploaded documents using NLP, OCR,
        and Gemini AI. Supports MCQs, short-answer, and long-answer formats with Bloom's
        Taxonomy classification, difficulty control, and PDF export.
      </p>
      <div class="tag-row">
        <span class="tag">NLP</span>
        <span class="tag">OCR</span>
        <span class="tag">Gemini AI</span>
        <span class="tag">Prompt Eng.</span>
      </div>
      <a href="https://github.com/veerareddygajulapalli-prog/HMVRQ" target="_blank" class="project-link">
        View on GitHub →
      </a>
    </div>
    <div class="project-card">
      <div class="project-icon">🍱</div>
      <h3 class="project-title">Food Revive System</h3>
      <p class="project-desc">
        A food waste management platform connecting donors with orphanages and farmers
        to reduce waste and support sustainability. Manages donation flows and builds
        donor–receiver networks for social impact.
      </p>
      <div class="tag-row">
        <span class="tag">HTML</span>
        <span class="tag">CSS</span>
        <span class="tag">JavaScript</span>
        <span class="tag">MySQL</span>
      </div>
      <a href="https://github.com/veerareddygajulapalli-prog" target="_blank" class="project-link">
        GitHub Profile →
      </a>
    </div>
  </div>
</section>

<!-- ACHIEVEMENTS -->
<section id="achievements">
  <p class="section-eyebrow">Recognition</p>
  <h2 class="section-title">Achievements &amp; Certifications</h2>
  <div class="ach-list">
    <div class="ach-item">
      <div class="ach-badge">🥉</div>
      <div class="ach-text"><strong>Top 3 Finalist — Crypton 2025 Hackathon</strong></div>
    </div>
    <div class="ach-item">
      <div class="ach-badge">🏅</div>
      <div class="ach-text"><strong>Hackathon 2025</strong>, Coimbatore</div>
    </div>
    <div class="ach-item">
      <div class="ach-badge">🏅</div>
      <div class="ach-text"><strong>Vintra 2023</strong>, Kalasalingam University</div>
    </div>
    <div class="ach-item">
      <div class="ach-badge">📜</div>
      <div class="ach-text"><strong>Certification</strong> — Database Management Systems</div>
    </div>
    <div class="ach-item">
      <div class="ach-badge">📜</div>
      <div class="ach-text"><strong>Certification</strong> — Design and Analysis of Algorithms</div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <p class="section-eyebrow">Let's talk</p>
  <h2 class="section-title">Get in Touch</h2>
  <div class="contact-inner">
    <div>
      <p class="contact-status">
        <span class="status-dot"></span> Available for full-time roles
      </p>
      <p class="contact-blurb">
        I'm actively seeking Full Stack Developer opportunities where I can build
        impactful applications and grow as an engineer. Open to internships, full-time
        roles, freelance work, and open source collaboration.
      </p>
      <a href="https://drive.google.com/file/d/1M9yWVTBY2d-9pgFJRCUL0gr_17NgYocc/view" target="_blank" class="btn btn-primary">
        ↓ Download Resume
      </a>
    </div>
    <div class="contact-links">
      <a href="mailto:veerareddygajulapalli@gmail.com" class="contact-link">
        <span class="contact-link-icon">✉</span>
        veerareddygajulapalli@gmail.com
      </a>
      <a href="https://www.linkedin.com/in/veera-reddy-gajulapalli" target="_blank" class="contact-link">
        <span class="contact-link-icon">in</span>
        linkedin.com/in/veera-reddy-gajulapalli
      </a>
      <a href="https://github.com/veerareddygajulapalli-prog" target="_blank" class="contact-link">
        <span class="contact-link-icon">⌥</span>
        github.com/veerareddygajulapalli-prog
      </a>
    </div>
  </div>
</section>

<footer>
  Built with intention · Gajulapalli Veera Reddy · Hyderabad, India
</footer>

</body>
</html>
