<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Isra Brahimi — AI & Computer Vision Engineer</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet" />
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --ink: #1a1a18;
    --ink-mid: #4a4a46;
    --ink-soft: #8a8a84;
    --ink-ghost: #c8c8c0;
    --paper: #fafaf7;
    --paper-warm: #f4f3ee;
    --accent: #2d6a4f;
    --accent-light: #e8f4ef;
    --accent-mid: #74c69d;
    --rule: #e2e2da;
    --serif: 'DM Serif Display', Georgia, serif;
    --sans: 'DM Sans', system-ui, sans-serif;
    --max: 900px;
  }

  html { scroll-behavior: smooth; }

  body {
    font-family: var(--sans);
    background: var(--paper);
    color: var(--ink);
    font-size: 16px;
    line-height: 1.7;
    -webkit-font-smoothing: antialiased;
  }

  /* ── NAV ── */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    background: rgba(250,250,247,0.92);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--rule);
    display: flex; align-items: center; justify-content: space-between;
    padding: 0 clamp(1.5rem, 5vw, 3rem);
    height: 60px;
  }
  .nav-logo {
    font-family: var(--serif);
    font-size: 1.1rem;
    color: var(--ink);
    text-decoration: none;
    letter-spacing: -0.01em;
  }
  .nav-links { display: flex; gap: 2rem; list-style: none; }
  .nav-links a {
    font-size: 0.82rem;
    font-weight: 500;
    color: var(--ink-mid);
    text-decoration: none;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--accent); }

  /* ── LAYOUT ── */
  .container { max-width: var(--max); margin: 0 auto; padding: 0 clamp(1.5rem, 5vw, 3rem); }

  section { padding: 6rem 0; }
  section + section { border-top: 1px solid var(--rule); }

  h2.section-label {
    font-family: var(--sans);
    font-size: 0.72rem;
    font-weight: 500;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 0.75rem;
  }
  h3.section-title {
    font-family: var(--serif);
    font-size: clamp(1.9rem, 3.5vw, 2.6rem);
    font-weight: 400;
    line-height: 1.15;
    color: var(--ink);
    margin-bottom: 2.5rem;
    letter-spacing: -0.02em;
  }

  /* ── HERO ── */
  #hero {
    padding-top: 140px;
    padding-bottom: 7rem;
    border-top: none;
    border-bottom: 1px solid var(--rule);
  }
  .hero-eyebrow {
    display: inline-flex; align-items: center; gap: 8px;
    font-size: 0.78rem; font-weight: 500; letter-spacing: 0.1em;
    text-transform: uppercase; color: var(--accent);
    background: var(--accent-light);
    padding: 4px 12px; border-radius: 99px;
    margin-bottom: 1.75rem;
    animation: fadeUp 0.5s ease both;
  }
  .hero-eyebrow::before { content: ''; display: block; width: 6px; height: 6px; border-radius: 50%; background: var(--accent); }
  .hero-name {
    font-family: var(--serif);
    font-size: clamp(3rem, 7vw, 5.5rem);
    font-weight: 400;
    line-height: 1.0;
    letter-spacing: -0.03em;
    color: var(--ink);
    margin-bottom: 1.5rem;
    animation: fadeUp 0.55s 0.08s ease both;
  }
  .hero-name em { font-style: italic; color: var(--accent); }
  .hero-tagline {
    font-size: clamp(1rem, 2vw, 1.2rem);
    color: var(--ink-mid);
    font-weight: 300;
    max-width: 560px;
    margin-bottom: 2.5rem;
    line-height: 1.65;
    animation: fadeUp 0.55s 0.16s ease both;
  }
  .hero-ctas {
    display: flex; gap: 1rem; flex-wrap: wrap;
    animation: fadeUp 0.55s 0.24s ease both;
  }
  .btn {
    display: inline-flex; align-items: center; gap: 6px;
    padding: 0.65rem 1.5rem;
    border-radius: 4px;
    font-size: 0.875rem; font-weight: 500;
    text-decoration: none; cursor: pointer;
    transition: all 0.18s ease;
    letter-spacing: 0.01em;
  }
  .btn-primary {
    background: var(--ink); color: var(--paper);
    border: 1.5px solid var(--ink);
  }
  .btn-primary:hover { background: var(--accent); border-color: var(--accent); }
  .btn-outline {
    background: transparent; color: var(--ink);
    border: 1.5px solid var(--ink-ghost);
  }
  .btn-outline:hover { border-color: var(--ink); }

  .hero-stats {
    display: flex; gap: 3rem; margin-top: 4rem;
    padding-top: 2.5rem; border-top: 1px solid var(--rule);
    animation: fadeUp 0.55s 0.32s ease both;
    flex-wrap: wrap;
  }
  .stat-num {
    font-family: var(--serif);
    font-size: 2rem; color: var(--ink);
    letter-spacing: -0.02em;
  }
  .stat-label { font-size: 0.8rem; color: var(--ink-soft); margin-top: 2px; }

  /* ── EXPERIENCE ── */
  .exp-list { display: flex; flex-direction: column; gap: 0; }
  .exp-item {
    display: grid;
    grid-template-columns: 140px 1fr;
    gap: 0 2.5rem;
    padding: 2rem 0;
    border-bottom: 1px solid var(--rule);
    opacity: 0;
    transform: translateY(16px);
    transition: opacity 0.4s ease, transform 0.4s ease;
  }
  .exp-item.visible { opacity: 1; transform: translateY(0); }
  .exp-date {
    font-size: 0.78rem; color: var(--ink-soft);
    font-weight: 400; padding-top: 4px;
    letter-spacing: 0.02em;
  }
  .exp-role {
    font-family: var(--serif);
    font-size: 1.15rem; font-weight: 400;
    color: var(--ink); margin-bottom: 3px;
  }
  .exp-company {
    font-size: 0.83rem; color: var(--accent);
    font-weight: 500; margin-bottom: 0.75rem;
    letter-spacing: 0.03em;
  }
  .exp-desc {
    font-size: 0.9rem; color: var(--ink-mid);
    line-height: 1.65; max-width: 540px;
  }
  .exp-tag {
    display: inline-block; margin-top: 0.75rem; margin-right: 6px;
    font-size: 0.72rem; font-weight: 500; letter-spacing: 0.05em;
    background: var(--paper-warm); color: var(--ink-mid);
    border: 1px solid var(--rule);
    padding: 2px 9px; border-radius: 3px;
  }

  /* ── PROJECTS ── */
  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
    gap: 1.25rem;
  }
  .project-card {
    background: #fff;
    border: 1px solid var(--rule);
    border-radius: 8px;
    padding: 1.5rem;
    text-decoration: none;
    color: inherit;
    display: flex; flex-direction: column;
    transition: border-color 0.2s, transform 0.2s;
    opacity: 0; transform: translateY(12px);
    transition: opacity 0.35s ease, transform 0.35s ease, border-color 0.2s;
  }
  .project-card.visible { opacity: 1; transform: translateY(0); }
  .project-card:hover { border-color: var(--accent-mid); transform: translateY(-3px); }
  .project-icon {
    width: 36px; height: 36px; border-radius: 8px;
    background: var(--accent-light);
    display: flex; align-items: center; justify-content: center;
    font-size: 16px; margin-bottom: 1rem;
  }
  .project-name {
    font-family: var(--serif);
    font-size: 1rem; font-weight: 400;
    color: var(--ink); margin-bottom: 0.4rem;
  }
  .project-desc {
    font-size: 0.83rem; color: var(--ink-mid);
    line-height: 1.6; flex: 1; margin-bottom: 1rem;
  }
  .project-stack {
    font-size: 0.7rem; color: var(--ink-soft);
    font-weight: 500; letter-spacing: 0.04em;
    text-transform: uppercase;
  }

  /* ── SKILLS ── */
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    gap: 1.5rem;
  }
  .skill-group-title {
    font-size: 0.72rem; font-weight: 500; letter-spacing: 0.1em;
    text-transform: uppercase; color: var(--ink-soft);
    margin-bottom: 0.75rem;
  }
  .skill-pills { display: flex; flex-wrap: wrap; gap: 6px; }
  .pill {
    font-size: 0.8rem; font-weight: 400;
    background: var(--paper-warm);
    border: 1px solid var(--rule);
    color: var(--ink-mid);
    padding: 3px 11px; border-radius: 99px;
    transition: background 0.15s, color 0.15s;
  }
  .pill:hover { background: var(--accent-light); color: var(--accent); }

  /* ── EDUCATION ── */
  .edu-card {
    background: #fff;
    border: 1px solid var(--rule);
    border-left: 3px solid var(--accent);
    border-radius: 0 8px 8px 0;
    padding: 1.5rem 1.75rem;
    margin-bottom: 1.25rem;
  }
  .edu-degree {
    font-family: var(--serif);
    font-size: 1.1rem; color: var(--ink);
    margin-bottom: 3px;
  }
  .edu-school { font-size: 0.85rem; color: var(--accent); font-weight: 500; margin-bottom: 6px; }
  .edu-detail { font-size: 0.85rem; color: var(--ink-mid); }
  .edu-highlight {
    display: inline-block; margin-top: 0.5rem;
    background: var(--accent-light); color: var(--accent);
    font-size: 0.75rem; font-weight: 500;
    padding: 3px 10px; border-radius: 4px;
  }

  /* ── CERTIFICATIONS ── */
  .cert-list { display: flex; flex-direction: column; gap: 0.6rem; margin-top: 1.5rem; }
  .cert-item {
    display: flex; align-items: center; gap: 10px;
    font-size: 0.88rem; color: var(--ink-mid);
    padding: 0.6rem 0; border-bottom: 1px solid var(--rule);
  }
  .cert-dot { width: 6px; height: 6px; border-radius: 50%; background: var(--accent); flex-shrink: 0; }
  .cert-year { margin-left: auto; font-size: 0.78rem; color: var(--ink-ghost); font-weight: 500; }

  /* ── CONTACT ── */
  #contact { text-align: center; border-bottom: none; }
  .contact-links { display: flex; gap: 1rem; justify-content: center; flex-wrap: wrap; margin-top: 2rem; }

  /* ── FOOTER ── */
  footer {
    text-align: center; padding: 2rem;
    font-size: 0.78rem; color: var(--ink-ghost);
    border-top: 1px solid var(--rule);
  }

  /* ── ANIMATIONS ── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(18px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  /* ── RESPONSIVE ── */
  @media (max-width: 600px) {
    .exp-item { grid-template-columns: 1fr; gap: 4px; }
    .exp-date { margin-bottom: 4px; }
    .nav-links { display: none; }
    .hero-stats { gap: 2rem; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a href="#" class="nav-logo">Isra Brahimi</a>
  <ul class="nav-links">
    <li><a href="#experience">Experience</a></li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#education">Education</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="container">
    <div class="hero-eyebrow">Available for opportunities</div>
    <h1 class="hero-name">Isra<br><em>Brahimi</em></h1>
    <p class="hero-tagline">
      AI &amp; Embedded Systems Engineer specialising in Computer Vision and Deep Learning.
      I build systems that teach machines to see — from real-time fire detection to medical image diagnosis.
    </p>
    <div class="hero-ctas">
      <a href="mailto:israbrahimi2002@gmail.com" class="btn btn-primary">Get in touch</a>
      <a href="https://github.com/biney17" class="btn btn-outline" target="_blank">View GitHub</a>
      <a href="#projects" class="btn btn-outline">See projects</a>
    </div>
    <div class="hero-stats">
      <div>
        <div class="stat-num">19.5<span style="font-size:1rem">/20</span></div>
        <div class="stat-label">Master's thesis score</div>
      </div>
      <div>
        <div class="stat-num">96%</div>
        <div class="stat-label">Medical image classification accuracy</div>
      </div>
      <div>
        <div class="stat-num">15+</div>
        <div class="stat-label">AI &amp; CV projects shipped</div>
      </div>
      <div>
        <div class="stat-num">Jijel</div>
        <div class="stat-label">Algeria — Remote-ready</div>
      </div>
    </div>
  </div>
</section>

<!-- EXPERIENCE -->
<section id="experience">
  <div class="container">
    <h2 class="section-label">Career</h2>
    <h3 class="section-title">Professional experience</h3>
    <div class="exp-list">

      <div class="exp-item">
        <div class="exp-date">Dec 2025 — Present</div>
        <div>
          <div class="exp-role">AI Engineer Intern</div>
          <div class="exp-company">Aitronix · Remote</div>
          <div class="exp-desc">
            Building and evaluating Computer Vision models for real-world deployment. Led training and testing pipelines using Python, TensorFlow, and OpenCV. Contributed to technical documentation and cross-team knowledge transfer on live CV projects including fire and smoke detection.
          </div>
          <span class="exp-tag">Python</span><span class="exp-tag">TensorFlow</span><span class="exp-tag">OpenCV</span><span class="exp-tag">YOLOv8</span>
        </div>
      </div>

      <div class="exp-item">
        <div class="exp-date">Jun – Jul 2024</div>
        <div>
          <div class="exp-role">Industrial Automation &amp; Maintenance Intern</div>
          <div class="exp-company">Algerian Qatari Steel</div>
          <div class="exp-desc">
            Gained hands-on experience with motors, conveyors, and Siemens PLC systems in a heavy industrial environment. Participated in quality control and testing protocols for production lines.
          </div>
          <span class="exp-tag">PLC</span><span class="exp-tag">Industrial Automation</span>
        </div>
      </div>

      <div class="exp-item">
        <div class="exp-date">Mar – Apr 2024</div>
        <div>
          <div class="exp-role">Siemens Automation Intern</div>
          <div class="exp-company">BIOREM Laboratories</div>
          <div class="exp-desc">
            Studied Siemens PLC control sequences and automation logic in a laboratory context, deepening understanding of industrial control system design.
          </div>
          <span class="exp-tag">Siemens PLC</span><span class="exp-tag">Control Systems</span>
        </div>
      </div>

      <div class="exp-item">
        <div class="exp-date">May – Sep 2023</div>
        <div>
          <div class="exp-role">Technical Trainer &amp; Content Developer</div>
          <div class="exp-company">ELLABS</div>
          <div class="exp-desc">
            Designed and delivered Arduino and Scratch curricula to students, building foundational programming and robotics skills. Completed a <em>Training of Trainers</em> certification. Created reusable educational materials still in active use.
          </div>
          <span class="exp-tag">Arduino</span><span class="exp-tag">Education</span><span class="exp-tag">Curriculum Design</span>
        </div>
      </div>

      <div class="exp-item">
        <div class="exp-date">Jun 2023</div>
        <div>
          <div class="exp-role">Telecommunications Intern</div>
          <div class="exp-company">Algérie Télécom</div>
          <div class="exp-desc">Observed national-scale telecom infrastructure and network operations.</div>
        </div>
      </div>

      <div class="exp-item">
        <div class="exp-date">Mar 2023</div>
        <div>
          <div class="exp-role">Instrumentation Intern</div>
          <div class="exp-company">Sonelgaz</div>
          <div class="exp-desc">Explored instrumentation systems and precision measurement equipment within the Algerian energy sector.</div>
        </div>
      </div>

    </div>
  </div>
</section>

<!-- PROJECTS -->
<section id="projects">
  <div class="container">
    <h2 class="section-label">Work</h2>
    <h3 class="section-title">Featured projects</h3>
    <div class="projects-grid">

      <a href="https://github.com/biney17/Fire-Smoke-Detection-YOLOv8" target="_blank" class="project-card">
        <div class="project-icon">🔥</div>
        <div class="project-name">Fire &amp; Smoke Detection</div>
        <div class="project-desc">Real-time detection system for industrial surveillance cameras. Processes live video streams and triggers alerts. Built at Aitronix.</div>
        <div class="project-stack">YOLOv8 · OpenCV · Python</div>
      </a>

      <a href="https://github.com/biney17/AI_Trainer" target="_blank" class="project-card">
        <div class="project-icon">🏋️</div>
        <div class="project-name">AI Personal Trainer</div>
        <div class="project-desc">Real-time posture and movement coach using pose estimation. Detects body movements via webcam and provides instant corrective feedback.</div>
        <div class="project-stack">MediaPipe · Keras · OpenCV</div>
      </a>

      <a href="https://github.com/biney17/AI-Virtual-Mouse" target="_blank" class="project-card">
        <div class="project-icon">🖱️</div>
        <div class="project-name">AI Virtual Mouse</div>
        <div class="project-desc">Touchless mouse controller using hand landmark tracking. Controls cursor and clicks with no physical hardware required.</div>
        <div class="project-stack">MediaPipe · OpenCV · Python</div>
      </a>

      <a href="https://github.com/biney17/eye-disease-classification" target="_blank" class="project-card">
        <div class="project-icon">👁️</div>
        <div class="project-name">Eye Disease Classifier</div>
        <div class="project-desc">CNN-based medical image classifier trained on retinal scans to detect ocular diseases. Applies augmentation for robust generalisation.</div>
        <div class="project-stack">TensorFlow · Keras · CNN</div>
      </a>

      <a href="https://github.com/biney17/brain-tumor-classification" target="_blank" class="project-card">
        <div class="project-icon">🧠</div>
        <div class="project-name">Brain Tumor Classification</div>
        <div class="project-desc">Deep learning classifier for MRI brain scans, identifying tumor presence and type to assist preliminary diagnostic workflows.</div>
        <div class="project-stack">CNN · TensorFlow · Keras</div>
      </a>

      <a href="https://github.com/biney17/Virtual_Painter" target="_blank" class="project-card">
        <div class="project-icon">🎨</div>
        <div class="project-name">Virtual Painter</div>
        <div class="project-desc">Draw in mid-air using your finger as a brush. Tracks hand movements in real time and renders strokes on a virtual canvas.</div>
        <div class="project-stack">MediaPipe · OpenCV · Python</div>
      </a>

      <a href="https://github.com/biney17/drowsiness-detection" target="_blank" class="project-card">
        <div class="project-icon">😴</div>
        <div class="project-name">Drowsiness Detection</div>
        <div class="project-desc">Real-time driver drowsiness monitoring system using eye aspect ratio tracking. Triggers alerts when fatigue is detected.</div>
        <div class="project-stack">OpenCV · Python · CV</div>
      </a>

      <a href="https://github.com/biney17/maintenance-automation-make" target="_blank" class="project-card">
        <div class="project-icon">🔧</div>
        <div class="project-name">Maintenance Automation</div>
        <div class="project-desc">Intelligent maintenance workflow system combining GPT reasoning with Make automation for AI-driven operational efficiency.</div>
        <div class="project-stack">Python · GPT API · Make</div>
      </a>

      <a href="https://github.com/biney17/bbc-news-classification-bert" target="_blank" class="project-card">
        <div class="project-icon">📰</div>
        <div class="project-name">BBC News Classifier — BERT</div>
        <div class="project-desc">Fine-tuned BERT transformer to classify BBC news articles across sport, tech, politics, business, and entertainment categories.</div>
        <div class="project-stack">BERT · HuggingFace · PyTorch</div>
      </a>

      <a href="https://github.com/biney17/abstractive-text-summarization" target="_blank" class="project-card">
        <div class="project-icon">📝</div>
        <div class="project-name">Abstractive Summarization</div>
        <div class="project-desc">T5-powered summarization pipeline that generates coherent summaries from long documents — understanding content, not just extracting it.</div>
        <div class="project-stack">T5 · HuggingFace · PyTorch</div>
      </a>

      <a href="https://github.com/biney17/rock-paper-scissors-ai" target="_blank" class="project-card">
        <div class="project-icon">✊</div>
        <div class="project-name">Rock-Paper-Scissors AI</div>
        <div class="project-desc">Gesture recognition game with pattern-prediction AI that learns your tendencies and adapts its strategy to beat you.</div>
        <div class="project-stack">Keras · OpenCV · Python</div>
      </a>

      <a href="https://github.com/biney17/ElZaheimr-classification" target="_blank" class="project-card">
        <div class="project-icon">🔬</div>
        <div class="project-name">Alzheimer's Classification</div>
        <div class="project-desc">Deep learning model for classifying Alzheimer's disease stages from MRI scans as part of a medical imaging research series.</div>
        <div class="project-stack">CNN · TensorFlow · Medical Imaging</div>
      </a>

    </div>
  </div>
</section>

<!-- SKILLS -->
<section id="skills">
  <div class="container">
    <h2 class="section-label">Expertise</h2>
    <h3 class="section-title">Technical skills</h3>
    <div class="skills-grid">
      <div>
        <div class="skill-group-title">Computer Vision</div>
        <div class="skill-pills">
          <span class="pill">YOLOv8</span><span class="pill">OpenCV</span><span class="pill">MediaPipe</span>
          <span class="pill">Haar Cascades</span><span class="pill">Pose Estimation</span><span class="pill">Object Detection</span>
        </div>
      </div>
      <div>
        <div class="skill-group-title">AI / Deep Learning</div>
        <div class="skill-pills">
          <span class="pill">TensorFlow</span><span class="pill">Keras</span><span class="pill">PyTorch</span>
          <span class="pill">CNNs</span><span class="pill">Transfer Learning</span><span class="pill">HuggingFace</span>
        </div>
      </div>
      <div>
        <div class="skill-group-title">NLP</div>
        <div class="skill-pills">
          <span class="pill">BERT</span><span class="pill">T5</span><span class="pill">Transformers</span>
          <span class="pill">Text Classification</span><span class="pill">Summarization</span>
        </div>
      </div>
      <div>
        <div class="skill-group-title">Programming</div>
        <div class="skill-pills">
          <span class="pill">Python</span><span class="pill">C / C++</span><span class="pill">MATLAB</span>
          <span class="pill">Assembly</span>
        </div>
      </div>
      <div>
        <div class="skill-group-title">Hardware &amp; Embedded</div>
        <div class="skill-pills">
          <span class="pill">Arduino</span><span class="pill">PCB Design</span><span class="pill">Siemens PLC</span>
          <span class="pill">Power Electronics</span><span class="pill">Sensors</span>
        </div>
      </div>
      <div>
        <div class="skill-group-title">Tools &amp; Platforms</div>
        <div class="skill-pills">
          <span class="pill">Git / GitHub</span><span class="pill">VS Code</span><span class="pill">Proteus</span>
          <span class="pill">ReactJS</span><span class="pill">Arduino IDE</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- EDUCATION -->
<section id="education">
  <div class="container">
    <h2 class="section-label">Background</h2>
    <h3 class="section-title">Education &amp; certifications</h3>

    <div class="edu-card">
      <div class="edu-degree">Master of Engineering — Embedded Systems</div>
      <div class="edu-school">Université Mohamed Seddik Benyahia, Jijel · 2023 – 2025</div>
      <div class="edu-detail">
        Thesis: <em>Intelligent Web Application for Preliminary Medical Image Diagnosis Using AI</em><br>
        4 CNN models · 96% classification accuracy · Full AI pipeline with ReactJS interface
      </div>
      <span class="edu-highlight">Thesis score: 19.5 / 20</span>
    </div>

    <div class="edu-card">
      <div class="edu-degree">Bachelor of Engineering — Electronics</div>
      <div class="edu-school">Université Mohamed Seddik Benyahia, Jijel · 2020 – 2023</div>
      <div class="edu-detail">PCB Layout · Power Electronics · Control Systems · Microprocessor Architecture</div>
    </div>

    <div class="cert-list">
      <div class="cert-item"><span class="cert-dot"></span>Machine Learning with Python — freeCodeCamp<span class="cert-year">2025</span></div>
      <div class="cert-item"><span class="cert-dot"></span>AI Automation Explorer — Make Academy<span class="cert-year">2025</span></div>
      <div class="cert-item"><span class="cert-dot"></span>Make Foundation — Make Academy<span class="cert-year">2025</span></div>
      <div class="cert-item"><span class="cert-dot"></span>Problem Solving &amp; Leadership — INJAZ El Djazair<span class="cert-year">2022</span></div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="container">
    <h2 class="section-label">Say hello</h2>
    <h3 class="section-title" style="margin-bottom:1rem">Let's work together</h3>
    <p style="color:var(--ink-mid); max-width:480px; margin:0 auto 2rem; font-size:1rem;">
      Open to roles in AI engineering, Computer Vision research, and embedded systems. Always happy to connect.
    </p>
    <div class="contact-links">
      <a href="mailto:israbrahimi2002@gmail.com" class="btn btn-primary">israbrahimi2002@gmail.com</a>
      <a href="https://github.com/biney17" target="_blank" class="btn btn-outline">GitHub</a>
      <a href="https://linkedin.com/in/your-profile" target="_blank" class="btn btn-outline">LinkedIn</a>
    </div>
  </div>
</section>

<footer>
  &copy; 2025 Isra Nour El Yakine Brahimi · Built for GitHub Pages
</footer>

<script>
  const observer = new IntersectionObserver((entries) => {
    entries.forEach((e, i) => {
      if (e.isIntersecting) {
        setTimeout(() => e.target.classList.add('visible'), i * 60);
      }
    });
  }, { threshold: 0.1 });

  document.querySelectorAll('.exp-item, .project-card').forEach(el => observer.observe(el));
</script>
</body>
</html>
