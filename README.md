<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Mahmoud Ayman — AI/ML Engineer</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&family=JetBrains+Mono:wght@400;500;700&family=Syne:wght@700;800&display=swap" rel="stylesheet"/>
<style>
  :root {
    --bg: #050810;
    --bg2: #080d1a;
    --bg3: #0c1220;
    --card: #0f1626;
    --card2: #121c30;
    --border: rgba(10,102,194,0.18);
    --border2: rgba(96,165,250,0.12);
    --blue: #0A66C2;
    --blue2: #1d7de0;
    --accent: #60a5fa;
    --accent2: #38bdf8;
    --glow: rgba(10,102,194,0.35);
    --text: #e2e8f0;
    --text2: #94a3b8;
    --text3: #64748b;
    --green: #22c55e;
    --mono: 'JetBrains Mono', monospace;
    --sans: 'Space Grotesk', sans-serif;
    --display: 'Syne', sans-serif;
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  html { scroll-behavior: smooth; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: var(--sans);
    line-height: 1.6;
    overflow-x: hidden;
  }

  /* ── NOISE OVERLAY ── */
  body::before {
    content: '';
    position: fixed; inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.03'/%3E%3C/svg%3E");
    pointer-events: none; z-index: 0; opacity: .4;
  }

  /* ── GRID BG ── */
  body::after {
    content: '';
    position: fixed; inset: 0;
    background-image:
      linear-gradient(rgba(10,102,194,0.04) 1px, transparent 1px),
      linear-gradient(90deg, rgba(10,102,194,0.04) 1px, transparent 1px);
    background-size: 60px 60px;
    pointer-events: none; z-index: 0;
  }

  .wrap { position: relative; z-index: 1; max-width: 1000px; margin: 0 auto; padding: 0 28px; }

  /* ── NAV ── */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    background: rgba(5,8,16,0.75);
    backdrop-filter: blur(20px);
    border-bottom: 1px solid var(--border);
    padding: 16px 0;
  }
  .nav-inner {
    max-width: 1000px; margin: 0 auto; padding: 0 28px;
    display: flex; align-items: center; justify-content: space-between;
  }
  .nav-logo {
    font-family: var(--mono); font-size: 13px; color: var(--accent);
    letter-spacing: .05em;
  }
  .nav-logo span { color: var(--text3); }
  .nav-links { display: flex; gap: 28px; }
  .nav-links a {
    font-size: 13px; color: var(--text2); text-decoration: none;
    font-family: var(--mono); letter-spacing: .04em;
    transition: color .2s;
  }
  .nav-links a:hover { color: var(--accent); }
  .nav-dot { width: 6px; height: 6px; border-radius: 50%; background: var(--green); box-shadow: 0 0 8px var(--green); animation: pulse 2s infinite; }
  @keyframes pulse { 0%,100%{opacity:1} 50%{opacity:.4} }

  /* ── HERO ── */
  .hero {
    min-height: 100vh;
    display: flex; align-items: center;
    padding: 120px 0 80px;
    position: relative;
  }
  .hero-glow {
    position: absolute; top: 20%; left: 50%; transform: translateX(-50%);
    width: 700px; height: 400px;
    background: radial-gradient(ellipse at center, rgba(10,102,194,0.12) 0%, transparent 70%);
    pointer-events: none;
  }
  .badge-row { display: flex; gap: 10px; margin-bottom: 28px; flex-wrap: wrap; }
  .badge {
    font-family: var(--mono); font-size: 11px; letter-spacing: .08em;
    padding: 5px 12px; border-radius: 4px;
    border: 1px solid var(--border);
    background: var(--card);
    color: var(--accent);
  }
  .badge.green { color: var(--green); border-color: rgba(34,197,94,0.2); }

  .hero-name {
    font-family: var(--display);
    font-size: clamp(52px, 8vw, 88px);
    font-weight: 800;
    line-height: 1;
    letter-spacing: -.03em;
    margin-bottom: 10px;
  }
  .hero-name .line2 {
    background: linear-gradient(135deg, var(--blue) 0%, var(--accent2) 100%);
    -webkit-background-clip: text; -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .hero-title {
    font-size: 18px; color: var(--text2); font-weight: 400;
    margin-bottom: 24px; letter-spacing: .02em;
  }
  .hero-title strong { color: var(--text); font-weight: 600; }

  .hero-desc {
    font-size: 15px; color: var(--text2); max-width: 560px;
    line-height: 1.75; margin-bottom: 40px;
  }

  .hero-cta { display: flex; gap: 14px; flex-wrap: wrap; }
  .btn {
    display: inline-flex; align-items: center; gap: 8px;
    padding: 12px 24px; border-radius: 8px;
    font-family: var(--sans); font-size: 14px; font-weight: 600;
    text-decoration: none; transition: all .25s; cursor: pointer; border: none;
  }
  .btn-primary {
    background: var(--blue); color: #fff;
    box-shadow: 0 0 30px rgba(10,102,194,0.35);
  }
  .btn-primary:hover { background: var(--blue2); box-shadow: 0 0 40px rgba(10,102,194,0.55); transform: translateY(-1px); }
  .btn-secondary {
    background: transparent; color: var(--text);
    border: 1px solid var(--border2);
  }
  .btn-secondary:hover { border-color: var(--accent); color: var(--accent); transform: translateY(-1px); }

  .hero-stats {
    display: flex; gap: 40px; margin-top: 60px;
    padding-top: 40px; border-top: 1px solid var(--border);
  }
  .stat-num {
    font-family: var(--display); font-size: 38px; font-weight: 800;
    background: linear-gradient(135deg, var(--accent) 0%, var(--blue) 100%);
    -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text;
  }
  .stat-label { font-size: 12px; color: var(--text3); letter-spacing: .06em; text-transform: uppercase; margin-top: 2px; }

  /* ── SECTION ── */
  section { padding: 90px 0; }
  .section-label {
    font-family: var(--mono); font-size: 11px; letter-spacing: .15em;
    color: var(--accent); text-transform: uppercase; margin-bottom: 12px;
    display: flex; align-items: center; gap: 10px;
  }
  .section-label::after { content: ''; flex: 1; max-width: 60px; height: 1px; background: var(--blue); }
  .section-title {
    font-family: var(--display); font-size: clamp(28px, 4vw, 42px);
    font-weight: 800; letter-spacing: -.02em; margin-bottom: 50px;
  }
  .section-title span {
    background: linear-gradient(135deg, var(--accent) 0%, var(--blue) 100%);
    -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text;
  }

  /* ── EXPERTISE GRID ── */
  .expertise-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 20px; }
  .exp-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 14px;
    padding: 28px;
    position: relative; overflow: hidden;
    transition: all .3s;
  }
  .exp-card::before {
    content: '';
    position: absolute; top: 0; left: 0; right: 0; height: 2px;
    background: linear-gradient(90deg, transparent, var(--blue), transparent);
    opacity: 0; transition: opacity .3s;
  }
  .exp-card:hover { border-color: rgba(10,102,194,0.4); transform: translateY(-3px); box-shadow: 0 20px 40px rgba(0,0,0,0.3); }
  .exp-card:hover::before { opacity: 1; }
  .exp-icon { font-size: 28px; margin-bottom: 16px; }
  .exp-title { font-size: 16px; font-weight: 700; margin-bottom: 14px; color: var(--text); }
  .exp-list { list-style: none; display: flex; flex-direction: column; gap: 8px; }
  .exp-list li {
    font-size: 13px; color: var(--text2);
    padding-left: 16px; position: relative;
  }
  .exp-list li::before { content: '→'; position: absolute; left: 0; color: var(--blue); font-family: var(--mono); }

  /* ── TECH STACK ── */
  .stack-grid { display: flex; flex-wrap: wrap; gap: 10px; }
  .tech-tag {
    font-family: var(--mono); font-size: 12px;
    padding: 7px 14px; border-radius: 6px;
    background: var(--card); border: 1px solid var(--border);
    color: var(--text2); transition: all .2s;
  }
  .tech-tag:hover { border-color: var(--blue); color: var(--accent); background: var(--card2); }
  .tech-tag.highlight { border-color: rgba(10,102,194,0.35); color: var(--accent); }

  /* ── FEATURED PROJECT ── */
  .project-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 18px;
    overflow: hidden;
    position: relative;
  }
  .project-card::before {
    content: '';
    position: absolute; inset: 0;
    background: linear-gradient(135deg, rgba(10,102,194,0.06) 0%, transparent 60%);
    pointer-events: none;
  }
  .project-header {
    padding: 36px 36px 28px;
    border-bottom: 1px solid var(--border);
    display: flex; align-items: flex-start; justify-content: space-between; gap: 20px;
    flex-wrap: wrap;
  }
  .project-title-block {}
  .project-eyebrow { font-family: var(--mono); font-size: 11px; color: var(--accent); letter-spacing: .1em; text-transform: uppercase; margin-bottom: 8px; }
  .project-name { font-family: var(--display); font-size: 28px; font-weight: 800; margin-bottom: 8px; }
  .project-desc { font-size: 14px; color: var(--text2); max-width: 420px; }
  .project-links { display: flex; gap: 10px; flex-shrink: 0; }

  .metrics-row {
    display: grid; grid-template-columns: repeat(4, 1fr);
    border-bottom: 1px solid var(--border);
  }
  .metric {
    padding: 24px; text-align: center;
    border-right: 1px solid var(--border);
  }
  .metric:last-child { border-right: none; }
  .metric-val { font-family: var(--display); font-size: 26px; font-weight: 800; color: var(--accent); }
  .metric-lbl { font-size: 11px; color: var(--text3); margin-top: 4px; letter-spacing: .05em; }

  .project-features {
    display: grid; grid-template-columns: 1fr 1fr;
    padding: 28px 36px; gap: 14px;
  }
  .feature {
    display: flex; align-items: flex-start; gap: 10px;
    font-size: 13px; color: var(--text2);
  }
  .feature-dot { width: 6px; height: 6px; border-radius: 50%; background: var(--blue); margin-top: 5px; flex-shrink: 0; }

  .stack-pills { display: flex; flex-wrap: wrap; gap: 8px; padding: 20px 36px 28px; border-top: 1px solid var(--border); }
  .pill {
    font-family: var(--mono); font-size: 11px; padding: 4px 10px;
    border-radius: 4px; background: rgba(10,102,194,0.12);
    border: 1px solid rgba(10,102,194,0.25); color: var(--accent);
  }

  /* ── CLIENTS ── */
  .clients-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(280px, 1fr)); gap: 14px; }
  .client-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 12px; padding: 20px 22px;
    text-decoration: none; display: block;
    transition: all .25s;
    position: relative; overflow: hidden;
  }
  .client-card::after {
    content: '↗';
    position: absolute; top: 18px; right: 18px;
    font-size: 14px; color: var(--text3);
    transition: all .25s;
  }
  .client-card:hover { border-color: rgba(10,102,194,0.4); transform: translateY(-2px); }
  .client-card:hover::after { color: var(--accent); transform: translate(2px, -2px); }
  .client-name { font-weight: 700; font-size: 15px; color: var(--text); margin-bottom: 5px; }
  .client-desc { font-size: 12px; color: var(--text3); line-height: 1.5; margin-bottom: 10px; }
  .client-tags { display: flex; flex-wrap: wrap; gap: 6px; }
  .client-tag { font-family: var(--mono); font-size: 10px; padding: 2px 7px; border-radius: 3px; background: rgba(10,102,194,0.1); color: var(--text3); border: 1px solid var(--border); }

  /* ── STANDARDS ── */
  .standards-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); gap: 16px; }
  .std-card {
    background: var(--card); border: 1px solid var(--border);
    border-radius: 12px; padding: 24px;
    display: flex; gap: 16px; align-items: flex-start;
    transition: all .25s;
  }
  .std-card:hover { border-color: rgba(10,102,194,0.35); }
  .std-icon { font-size: 22px; }
  .std-title { font-weight: 700; font-size: 14px; margin-bottom: 6px; }
  .std-body { font-size: 12px; color: var(--text3); line-height: 1.6; }

  /* ── CONTACT ── */
  .contact-wrap {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 20px; padding: 60px;
    text-align: center;
    position: relative; overflow: hidden;
  }
  .contact-wrap::before {
    content: '';
    position: absolute; top: -100px; left: 50%; transform: translateX(-50%);
    width: 500px; height: 300px;
    background: radial-gradient(ellipse, rgba(10,102,194,0.15) 0%, transparent 70%);
    pointer-events: none;
  }
  .contact-title { font-family: var(--display); font-size: 38px; font-weight: 800; margin-bottom: 14px; }
  .contact-sub { font-size: 15px; color: var(--text2); margin-bottom: 36px; }
  .contact-links { display: flex; justify-content: center; gap: 12px; flex-wrap: wrap; }
  .contact-link {
    display: inline-flex; align-items: center; gap: 8px;
    padding: 11px 22px; border-radius: 8px;
    font-size: 13px; font-weight: 600; text-decoration: none;
    border: 1px solid var(--border); background: var(--bg2);
    color: var(--text2); transition: all .25s;
  }
  .contact-link:hover { border-color: var(--blue); color: var(--accent); background: var(--card2); }

  /* ── FOOTER ── */
  footer {
    padding: 32px 0; text-align: center;
    border-top: 1px solid var(--border);
    font-family: var(--mono); font-size: 12px; color: var(--text3);
  }
  footer span { color: var(--blue); }

  /* ── ANIMATIONS ── */
  .fade-in { opacity: 0; transform: translateY(24px); animation: fadeUp .7s forwards; }
  @keyframes fadeUp { to { opacity: 1; transform: none; } }
  .d1 { animation-delay: .1s; }
  .d2 { animation-delay: .2s; }
  .d3 { animation-delay: .3s; }
  .d4 { animation-delay: .4s; }
  .d5 { animation-delay: .5s; }

  @media(max-width:640px) {
    .hero-stats { gap: 24px; flex-wrap: wrap; }
    .metrics-row { grid-template-columns: 1fr 1fr; }
    .project-features { grid-template-columns: 1fr; }
    .project-header { flex-direction: column; }
    .contact-wrap { padding: 36px 22px; }
    .nav-links { display: none; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-inner">
    <div class="nav-logo"><span>~/</span>mahmoud-aymann</div>
    <div class="nav-links">
      <a href="#expertise">Expertise</a>
      <a href="#project">Projects</a>
      <a href="#clients">Clients</a>
      <a href="#contact">Contact</a>
    </div>
    <div class="nav-dot"></div>
  </div>
</nav>

<!-- HERO -->
<div class="wrap">
  <section class="hero">
    <div class="hero-glow"></div>
    <div>
      <div class="badge-row fade-in d1">
        <span class="badge">AI / ML Engineer</span>
        <span class="badge green">● Available for Projects</span>
        <span class="badge">Egypt → Global</span>
      </div>

      <h1 class="hero-name fade-in d2">
        Mahmoud<br/>
        <span class="line2">Ayman.</span>
      </h1>

      <p class="hero-title fade-in d3">
        Building <strong>Computer Vision</strong>, <strong>NLP</strong> &amp; <strong>LLM Systems</strong> —
        from research to production.
      </p>

      <p class="hero-desc fade-in d4">
        I take business problems, architect the right AI solution,
        and deliver polished, deployed products. Not just notebooks —
        real systems that scale.
      </p>

      <div class="hero-cta fade-in d5">
        <a href="https://mahmoudayman.me" class="btn btn-primary" target="_blank">
          🌐 View Portfolio
        </a>
        <a href="mailto:mahmoudaymann153@gmail.com" class="btn btn-secondary">
          📧 Hire Me
        </a>
        <a href="https://www.linkedin.com/in/mahmoud-aymann/" class="btn btn-secondary" target="_blank">
          in LinkedIn
        </a>
      </div>

      <div class="hero-stats fade-in d5">
        <div>
          <div class="stat-num">100+</div>
          <div class="stat-label">Clients Served</div>
        </div>
        <div>
          <div class="stat-num">95%+</div>
          <div class="stat-label">Model Accuracy</div>
        </div>
        <div>
          <div class="stat-num">&lt;50ms</div>
          <div class="stat-label">Inference Speed</div>
        </div>
        <div>
          <div class="stat-num">E2E</div>
          <div class="stat-label">Delivery</div>
        </div>
      </div>
    </div>
  </section>
</div>

<!-- EXPERTISE -->
<div class="wrap" id="expertise">
  <section>
    <div class="section-label">What I Do</div>
    <h2 class="section-title">Core <span>Expertise</span></h2>
    <div class="expertise-grid">
      <div class="exp-card">
        <div class="exp-icon">🔍</div>
        <div class="exp-title">Computer Vision</div>
        <ul class="exp-list">
          <li>Object Detection, Segmentation & OCR</li>
          <li>Real-time Inference Pipelines</li>
          <li>Object Tracking & Anomaly Detection</li>
          <li>Quality Inspection Systems</li>
          <li>Edge Deployment (ONNX / TorchScript)</li>
        </ul>
      </div>
      <div class="exp-card">
        <div class="exp-icon">💬</div>
        <div class="exp-title">NLP & Language Models</div>
        <ul class="exp-list">
          <li>Text Classification, NER & Summarization</li>
          <li>RAG Pipelines & Fine-tuning</li>
          <li>Advanced Prompt Engineering</li>
          <li>Semantic Search & Chunking</li>
          <li>LLM Agents & Function Calling</li>
        </ul>
      </div>
      <div class="exp-card">
        <div class="exp-icon">🧠</div>
        <div class="exp-title">LLM Systems Architecture</div>
        <ul class="exp-list">
          <li>RAG with FAISS, Pinecone, Weaviate</li>
          <li>LangChain & LlamaIndex Frameworks</li>
          <li>Context Management & Retrieval</li>
          <li>FastAPI-based LLM Microservices</li>
          <li>Guardrails, Caching & Rate Limiting</li>
        </ul>
      </div>
      <div class="exp-card">
        <div class="exp-icon">🚀</div>
        <div class="exp-title">MLOps & Production</div>
        <ul class="exp-list">
          <li>Docker & CI/CD Pipelines</li>
          <li>On-prem, VPC & Cloud Deployment</li>
          <li>Model Versioning & Experiment Tracking</li>
          <li>Production Observability & Dashboards</li>
          <li>Full IaC & Reproducible Pipelines</li>
        </ul>
      </div>
      <div class="exp-card">
        <div class="exp-icon">🌐</div>
        <div class="exp-title">End-to-End AI Solutions</div>
        <ul class="exp-list">
          <li>REST APIs with FastAPI & Flask</li>
          <li>Modern Web UIs & Secure Endpoints</li>
          <li>Cloud Hosting: Railway, Vercel, Hostinger</li>
          <li>Discovery → MVP → Deployment → Monitoring</li>
        </ul>
      </div>
      <div class="exp-card">
        <div class="exp-icon">⚡</div>
        <div class="exp-title">Tech Stack</div>
        <div class="stack-grid" style="margin-top:8px;">
          <span class="tech-tag highlight">PyTorch</span>
          <span class="tech-tag highlight">HuggingFace</span>
          <span class="tech-tag highlight">LangChain</span>
          <span class="tech-tag">OpenCV</span>
          <span class="tech-tag">scikit-learn</span>
          <span class="tech-tag">FastAPI</span>
          <span class="tech-tag">Docker</span>
          <span class="tech-tag">ONNX</span>
          <span class="tech-tag">Python</span>
          <span class="tech-tag">YOLO</span>
        </div>
      </div>
    </div>
  </section>
</div>

<!-- FEATURED PROJECT -->
<div class="wrap" id="project">
  <section>
    <div class="section-label">Featured Work</div>
    <h2 class="section-title">Blood Cell <span>Prediction</span></h2>
    <div class="project-card">
      <div class="project-header">
        <div class="project-title-block">
          <div class="project-eyebrow">Medical AI System</div>
          <div class="project-name">Automated Blood Cell Classification</div>
          <div class="project-desc">End-to-end medical AI system for real-time blood cell analysis. Production-deployed with zero data retention and enterprise-grade security.</div>
        </div>
        <div class="project-links">
          <a href="https://web-production-4a424.up.railway.app/" class="btn btn-primary" target="_blank">🟢 Live Demo</a>
          <a href="https://github.com/mahmoud-aymann/blood_cell_prediction" class="btn btn-secondary" target="_blank">GitHub</a>
        </div>
      </div>

      <div class="metrics-row">
        <div class="metric"><div class="metric-val">95%+</div><div class="metric-lbl">Test Accuracy</div></div>
        <div class="metric"><div class="metric-val">&lt;50ms</div><div class="metric-lbl">Inference</div></div>
        <div class="metric"><div class="metric-val">8</div><div class="metric-lbl">Cell Classes</div></div>
        <div class="metric"><div class="metric-val">0</div><div class="metric-lbl">Data Stored</div></div>
      </div>

      <div class="project-features">
        <div class="feature"><div class="feature-dot"></div><span>Drag-and-drop web UI with real-time confidence scores</span></div>
        <div class="feature"><div class="feature-dot"></div><span>REST API with secure in-memory processing</span></div>
        <div class="feature"><div class="feature-dot"></div><span>Reproducible training pipeline with seed control</span></div>
        <div class="feature"><div class="feature-dot"></div><span>ONNX / TorchScript export-ready for edge deployment</span></div>
        <div class="feature"><div class="feature-dot"></div><span>Dockerized — one-click Railway deploy template</span></div>
        <div class="feature"><div class="feature-dot"></div><span>Versioned datasets & config-driven experiments</span></div>
      </div>

      <div class="stack-pills">
        <span class="pill">PyTorch</span>
        <span class="pill">Flask</span>
        <span class="pill">OpenCV</span>
        <span class="pill">scikit-learn</span>
        <span class="pill">Docker</span>
        <span class="pill">Railway</span>
      </div>
    </div>
  </section>
</div>

<!-- CLIENTS -->
<div class="wrap" id="clients">
  <section>
    <div class="section-label">Selected Work</div>
    <h2 class="section-title">Client <span>Projects</span></h2>
    <div class="clients-grid">
      <a href="https://uqab.io/" class="client-card" target="_blank">
        <div class="client-name">UQAB</div>
        <div class="client-desc">End-to-end digital transformation · Elite engineers & consultants</div>
        <div class="client-tags"><span class="client-tag">Enterprise</span><span class="client-tag">AI</span><span class="client-tag">Consulting</span></div>
      </a>
      <a href="https://smarthands.sa" class="client-card" target="_blank">
        <div class="client-name">Smart Hands</div>
        <div class="client-desc">Professional services platform · Scalable backend architecture</div>
        <div class="client-tags"><span class="client-tag">Laravel</span><span class="client-tag">PHP</span><span class="client-tag">MySQL</span></div>
      </a>
      <a href="https://mudunsa.com/" class="client-card" target="_blank">
        <div class="client-name">Mudun SA</div>
        <div class="client-desc">Urban development platform · Clean design & content delivery</div>
        <div class="client-tags"><span class="client-tag">HTML</span><span class="client-tag">CSS</span><span class="client-tag">JS</span></div>
      </a>
      <a href="https://dazzle-architect.com/" class="client-card" target="_blank">
        <div class="client-name">Dazzle Architect</div>
        <div class="client-desc">Architecture & Design showcase</div>
        <div class="client-tags"><span class="client-tag">HTML</span><span class="client-tag">Bootstrap</span></div>
      </a>
      <a href="https://burj-alenjaz.com/" class="client-card" target="_blank">
        <div class="client-name">Burj Al Enjaz</div>
        <div class="client-desc">Real Estate Development platform</div>
        <div class="client-tags"><span class="client-tag">HTML</span><span class="client-tag">Bootstrap</span></div>
      </a>
      <a href="https://nurviaconsultation.com/" class="client-card" target="_blank">
        <div class="client-name">Nurvia</div>
        <div class="client-desc">Modern digital platform · Scalable web solutions</div>
        <div class="client-tags"><span class="client-tag">Web</span><span class="client-tag">UI/UX</span><span class="client-tag">Performance</span></div>
      </a>
      <a href="http://luxelinksoftware.com/" class="client-card" target="_blank">
        <div class="client-name">Luxe Link Software</div>
        <div class="client-desc">Web, Mobile & AI solutions · Enterprise security</div>
        <div class="client-tags"><span class="client-tag">Web</span><span class="client-tag">Mobile</span><span class="client-tag">AI</span></div>
      </a>
      <a href="https://arabgulfae.com/" class="client-card" target="_blank">
        <div class="client-name">Arabgulf Electronic Trading</div>
        <div class="client-desc">Premium e-commerce platform · UAE based</div>
        <div class="client-tags"><span class="client-tag">E-commerce</span><span class="client-tag">UAE</span></div>
      </a>
      <a href="https://wisesoftware-sa.com/" class="client-card" target="_blank">
        <div class="client-name">Wise Software</div>
        <div class="client-desc">Tech services e-commerce · Modern UI</div>
        <div class="client-tags"><span class="client-tag">HTML</span><span class="client-tag">JS</span></div>
      </a>
    </div>
  </section>
</div>

<!-- STANDARDS -->
<div class="wrap">
  <section>
    <div class="section-label">How I Work</div>
    <h2 class="section-title">Enterprise <span>Standards</span></h2>
    <div class="standards-grid">
      <div class="std-card">
        <div class="std-icon">🔐</div>
        <div><div class="std-title">Security</div><div class="std-body">Secure data handling, private endpoints, and granular access controls on every delivery.</div></div>
      </div>
      <div class="std-card">
        <div class="std-icon">☁️</div>
        <div><div class="std-title">Deployment</div><div class="std-body">On-prem, VPC, or managed cloud — with full Infrastructure-as-Code support.</div></div>
      </div>
      <div class="std-card">
        <div class="std-icon">📈</div>
        <div><div class="std-title">Observability</div><div class="std-body">Experiment tracking, model versioning, and metrics dashboards included by default.</div></div>
      </div>
      <div class="std-card">
        <div class="std-icon">📋</div>
        <div><div class="std-title">Reproducibility</div><div class="std-body">Full documentation and auditability baked into every project from day one.</div></div>
      </div>
      <div class="std-card">
        <div class="std-icon">🤝</div>
        <div><div class="std-title">Engagement</div><div class="std-body">Clear milestones, defined SLAs, and transparent reporting throughout.</div></div>
      </div>
    </div>
  </section>
</div>

<!-- CONTACT -->
<div class="wrap" id="contact">
  <section>
    <div class="contact-wrap">
      <h2 class="contact-title">Let's Build <span style="background:linear-gradient(135deg,var(--accent),var(--blue));-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;">Something.</span></h2>
      <p class="contact-sub">Open to freelance projects, technical collaborations, and full-time opportunities.</p>
      <div class="contact-links">
        <a href="https://mahmoudayman.me" class="contact-link" target="_blank">🌐 Portfolio</a>
        <a href="mailto:mahmoudaymann153@gmail.com" class="contact-link">📧 Email</a>
        <a href="https://www.linkedin.com/in/mahmoud-aymann/" class="contact-link" target="_blank">in LinkedIn</a>
        <a href="http://www.medium.com/@mahmoudayman1" class="contact-link" target="_blank">✍ Medium</a>
        <a href="https://github.com/mahmoud-aymann" class="contact-link" target="_blank">⌥ GitHub</a>
      </div>
    </div>
  </section>
</div>

<!-- FOOTER -->
<footer>
  <div class="wrap">
    Built with precision by <span>Mahmoud Ayman</span> · AI/ML Engineer · Egypt 🇪🇬
  </div>
</footer>

</body>
</html>
