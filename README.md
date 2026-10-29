<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="theme-color" content="#0b1022">
  <meta name="description" content="Perumal A. — First-year Information Technology student and aspiring web developer.">
  <title>Perumal A. | IT Student & Aspiring Web Developer</title>
  <style>
    :root {
      --bg: #080d1c;
      --panel: rgba(255,255,255,.075);
      --panel-hover: rgba(255,255,255,.11);
      --line: rgba(255,255,255,.15);
      --text: #f4f6ff;
      --muted: #b7bfd8;
      --cyan: #66e3ff;
      --violet: #b69cff;
      --pink: #ff91d5;
      --green: #92f5c7;
      --radius: 24px;
      --shadow: 0 24px 70px rgba(0,0,0,.28);
    }
    * { box-sizing: border-box; margin: 0; padding: 0; }
    html { scroll-behavior: smooth; scroll-padding-top: 92px; }
    body {
      min-height: 100vh;
      background:
        radial-gradient(ellipse at 12% 12%, rgba(85,93,255,.18), transparent 36%),
        radial-gradient(ellipse at 88% 34%, rgba(0,218,255,.12), transparent 32%),
        radial-gradient(ellipse at 48% 92%, rgba(255,91,194,.10), transparent 35%),
        var(--bg);
      color: var(--text);
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      line-height: 1.65;
      overflow-x: hidden;
    }
    a { color: inherit; text-decoration: none; }
    button, input, textarea { font: inherit; }
    button, a { -webkit-tap-highlight-color: transparent; }
    ::selection { background: rgba(102,227,255,.3); }
    .orb {
      position: fixed; z-index: -1; border-radius: 50%; filter: blur(2px);
      pointer-events: none; opacity: .42; animation: drift 13s ease-in-out infinite alternate;
    }
    .orb.one { width: 240px; height: 240px; background: #553bff; top: 15%; left: -120px; }
    .orb.two { width: 180px; height: 180px; background: #00c9e8; top: 54%; right: -90px; animation-delay: -5s; }
    @keyframes drift { from { transform: translate(0,0) scale(1); } to { transform: translate(30px,-35px) scale(1.08); } }
    @keyframes float { 0%,100% { transform: translateY(0); } 50% { transform: translateY(-9px); } }
    @keyframes glow { 0%,100% { box-shadow: 0 0 18px rgba(102,227,255,.12); } 50% { box-shadow: 0 0 34px rgba(182,156,255,.26); } }
    @keyframes fadeUp { from { opacity: 0; transform: translateY(22px); } to { opacity: 1; transform: translateY(0); } }
    .container { width: min(1120px, calc(100% - 40px)); margin-inline: auto; }
    .glass {
      background: var(--panel);
      border: 1px solid var(--line);
      box-shadow: var(--shadow);
      backdrop-filter: blur(18px);
      -webkit-backdrop-filter: blur(18px);
    }
    header {
      position: sticky; top: 0; z-index: 50;
      background: rgba(8,13,28,.76);
      backdrop-filter: blur(18px);
      border-bottom: 1px solid rgba(255,255,255,.08);
    }
    .nav { min-height: 76px; display: flex; align-items: center; justify-content: space-between; gap: 22px; }
    .brand { font-weight: 850; letter-spacing: -.04em; font-size: 1.25rem; }
    .brand span { color: var(--cyan); }
    .nav-links { display: flex; align-items: center; gap: 23px; list-style: none; }
    .nav-links a { color: var(--muted); font-size: .91rem; transition: color .2s ease; }
    .nav-links a:hover, .nav-links a.active { color: var(--cyan); }
    .menu-toggle { display: none; color: var(--text); background: var(--panel); border: 1px solid var(--line); border-radius: 12px; padding: 8px 12px; cursor: pointer; }
    section { padding: 92px 0; }
    .hero { min-height: calc(100vh - 76px); display: grid; align-items: center; padding-top: 72px; }
    .hero-grid { display: grid; grid-template-columns: 1.25fr .75fr; align-items: center; gap: 54px; }
    .eyebrow { display: inline-flex; gap: 9px; align-items: center; padding: 7px 13px; border: 1px solid rgba(102,227,255,.27); border-radius: 999px; color: var(--cyan); background: rgba(102,227,255,.07); font-size: .83rem; font-weight: 650; }
    .dot { width: 7px; height: 7px; border-radius: 50%; background: var(--green); box-shadow: 0 0 12px var(--green); }
    h1 { font-size: clamp(2.8rem, 6.6vw, 5.4rem); line-height: 1.04; letter-spacing: -.065em; margin: 24px 0 18px; }
    .gradient-text { background: linear-gradient(100deg, var(--cyan), var(--violet) 55%, var(--pink)); -webkit-background-clip: text; background-clip: text; color: transparent; }
    .hero h2 { font-size: clamp(1.15rem, 2.5vw, 1.65rem); color: #e0e5ff; font-weight: 600; margin-bottom: 16px; }
    .hero p, .section-intro { color: var(--muted); max-width: 650px; }
    .actions { display: flex; flex-wrap: wrap; gap: 13px; margin-top: 29px; }
    .btn { display: inline-flex; align-items: center; justify-content: center; gap: 9px; padding: 12px 19px; border-radius: 13px; border: 1px solid var(--line); font-weight: 700; cursor: pointer; transition: transform .22s, box-shadow .22s, background .22s; }
    .btn:hover { transform: translateY(-3px); box-shadow: 0 12px 30px rgba(0,0,0,.24); }
    .btn-primary { color: #08111e; background: linear-gradient(100deg, var(--cyan), #b6f5ff); border-color: transparent; }
    .btn-secondary { background: rgba(255,255,255,.055); color: var(--text); }
    .hero-card { padding: 28px; border-radius: 30px; animation: float 6s ease-in-out infinite, glow 5s ease-in-out infinite; position: relative; overflow: hidden; }
    .hero-card::before { content: ""; position: absolute; width: 170px; height: 170px; border-radius: 50%; background: rgba(102,227,255,.13); filter: blur(35px); top: -70px; right: -50px; }
    .avatar { width: 126px; height: 126px; display: grid; place-items: center; margin: 0 auto 18px; border-radius: 36px; background: linear-gradient(135deg, rgba(102,227,255,.23), rgba(182,156,255,.3)); border: 1px solid rgba(255,255,255,.22); font-size: 2.5rem; font-weight: 900; letter-spacing: -.06em; color: white; transform: rotate(-4deg); }
    .hero-card h3 { text-align: center; font-size: 1.35rem; }
    .hero-card .sub { text-align: center; color: var(--muted); font-size: .92rem; margin-top: 3px; }
    .mini-stats { display: grid; grid-template-columns: repeat(2,1fr); gap: 12px; margin-top: 25px; }
    .stat { border: 1px solid var(--line); background: rgba(255,255,255,.045); border-radius: 16px; padding: 14px; }
    .stat strong { display: block; color: var(--cyan); font-size: 1.06rem; }
    .stat span { font-size: .78rem; color: var(--muted); }
    .section-heading { margin-bottom: 34px; }
    .kicker { color: var(--cyan); text-transform: uppercase; font-weight: 800; letter-spacing: .16em; font-size: .75rem; }
    h2.section-title { font-size: clamp(2rem,4vw,3rem); line-height: 1.15; letter-spacing: -.045em; margin-top: 8px; }
    .section-intro { margin-top: 12px; }
    .about-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 22px; }
    .panel { border-radius: var(--radius); padding: 27px; }
    .panel h3 { font-size: 1.16rem; margin-bottom: 12px; }
    .panel p { color: var(--muted); }
    .focus-list { display: grid; gap: 13px; margin-top: 18px; }
    .focus-item { display: flex; align-items: flex-start; gap: 12px; color: var(--muted); }
    .icon-box { flex: 0 0 38px; width: 38px; height: 38px; display: grid; place-items: center; border-radius: 12px; color: var(--cyan); background: rgba(102,227,255,.1); border: 1px solid rgba(102,227,255,.18); }
    .focus-item strong { display: block; color: var(--text); font-size: .95rem; }
    .skills-grid { display: grid; grid-template-columns: repeat(2,1fr); gap: 18px; }
    .skill-card { border-radius: 20px; padding: 23px; transition: transform .25s, background .25s, border-color .25s; }
    .skill-card:hover, .project-card:hover, .panel:hover { transform: translateY(-5px); background: var(--panel-hover); border-color: rgba(102,227,255,.3); }
    .skill-card h3 { margin-bottom: 15px; font-size: 1.05rem; }
    .tags { display: flex; flex-wrap: wrap; gap: 9px; }
    .tag { display: inline-flex; align-items: center; padding: 7px 11px; border-radius: 10px; background: rgba(182,156,255,.10); border: 1px solid rgba(182,156,255,.18); color: #e4dcff; font-size: .84rem; }
    .skill-card:nth-child(2) .tag { background: rgba(102,227,255,.08); border-color: rgba(102,227,255,.18); color: #b9f5ff; }
    .skill-card:nth-child(3) .tag { background: rgba(146,245,199,.08); border-color: rgba(146,245,199,.18); color: #c3ffe2; }
    .skill-card:nth-child(4) .tag { background: rgba(255,145,213,.08); border-color: rgba(255,145,213,.18); color: #ffd1ed; }
    .projects-grid { display: grid; grid-template-columns: repeat(2,1fr); gap: 20px; }
    .project-card { border-radius: 22px; overflow: hidden; transition: transform .25s, background .25s, border-color .25s; }
    .project-art { min-height: 155px; display: grid; place-items: center; background: linear-gradient(135deg, rgba(102,227,255,.16), rgba(182,156,255,.19), rgba(255,145,213,.12)); border-bottom: 1px solid var(--line); font-size: 3rem; }
    .project-content { padding: 23px; }
    .project-content p { color: var(--muted); margin: 9px 0 15px; }
    .text-link { color: var(--cyan); font-weight: 700; font-size: .9rem; }
    .timeline { display: grid; gap: 16px; }
    .timeline-item { display: grid; grid-template-columns: 52px 1fr; gap: 16px; padding: 22px; border-radius: 20px; }
    .timeline-icon { width: 48px; height: 48px; display: grid; place-items: center; border-radius: 15px; background: rgba(182,156,255,.12); border: 1px solid rgba(182,156,255,.2); font-size: 1.3rem; }
    .timeline-item p { color: var(--muted); margin-top: 4px; }
    .status { display: inline-block; margin-top: 9px; padding: 4px 9px; border-radius: 999px; color: var(--green); background: rgba(146,245,199,.08); border: 1px solid rgba(146,245,199,.2); font-size: .77rem; }
    .cert-note { padding: 24px; border-radius: 18px; color: var(--muted); border: 1px dashed rgba(255,255,255,.24); background: rgba(255,255,255,.035); }
    .social-grid { display: flex; flex-wrap: wrap; gap: 12px; margin-top: 20px; }
    .social-link { display: inline-flex; align-items: center; gap: 10px; padding: 12px 16px; border: 1px solid var(--line); border-radius: 14px; background: var(--panel); transition: transform .2s, border-color .2s; }
    .social-link:hover { transform: translateY(-3px); border-color: rgba(102,227,255,.4); }
    .contact-grid { display: grid; grid-template-columns: .9fr 1.1fr; gap: 22px; align-items: start; }
    .contact-detail { display: flex; gap: 13px; align-items: center; margin-top: 18px; color: var(--muted); }
    .contact-detail strong { color: var(--text); display: block; }
    form { display: grid; gap: 13px; }
    label { font-size: .88rem; color: #e0e5ff; font-weight: 650; }
    input, textarea { width: 100%; padding: 12px 14px; color: var(--text); background: rgba(3,7,19,.5); border: 1px solid var(--line); border-radius: 12px; outline: none; margin-top: 6px; }
    input:focus, textarea:focus { border-color: var(--cyan); box-shadow: 0 0 0 3px rgba(102,227,255,.1); }
    textarea { min-height: 120px; resize: vertical; }
    .form-note { color: var(--muted); font-size: .8rem; }
    footer { border-top: 1px solid rgba(255,255,255,.09); padding: 25px 0 32px; color: var(--muted); font-size: .88rem; }
    .footer-row { display: flex; align-items: center; justify-content: space-between; gap: 15px; flex-wrap: wrap; }
    .top-link { color: var(--cyan); }
    .reveal { opacity: 0; transform: translateY(18px); transition: opacity .65s ease, transform .65s ease; }
    .reveal.visible { opacity: 1; transform: translateY(0); }
    @media (prefers-reduced-motion: reduce) {
      *, *::before, *::after { scroll-behavior: auto !important; animation-duration: .01ms !important; transition-duration: .01ms !important; }
      .reveal { opacity: 1; transform: none; }
    }
    @media (max-width: 850px) {
      .nav-links { gap: 13px; }
      .nav-links a { font-size: .82rem; }
      .hero-grid { gap: 28px; }
      .hero-card { padding: 22px; }
    }
    @media (max-width: 700px) {
      .container { width: min(100% - 30px, 560px); }
      .nav { min-height: 68px; }
      .menu-toggle { display: inline-block; }
      .nav-links { display: none; position: absolute; top: 68px; left: 15px; right: 15px; padding: 15px; border: 1px solid var(--line); border-radius: 18px; background: rgba(8,13,28,.97); box-shadow: var(--shadow); flex-direction: column; align-items: stretch; gap: 3px; }
      .nav-links.open { display: flex; }
      .nav-links a { display: block; padding: 10px 12px; font-size: .95rem; }
      section { padding: 70px 0; }
      .hero { min-height: auto; padding: 72px 0 55px; }
      .hero-grid, .about-grid, .contact-grid { grid-template-columns: 1fr; }
      .hero-grid { gap: 35px; }
      .hero-card { max-width: 420px; width: 100%; margin-inline: auto; }
      .skills-grid, .projects-grid { grid-template-columns: 1fr; }
      h1 { font-size: clamp(2.8rem, 13vw, 4.2rem); }
      .section-heading { margin-bottom: 26px; }
    }
  </style>
</head>
<body>
  <div class="orb one" aria-hidden="true"></div>
  <div class="orb two" aria-hidden="true"></div>

  <header>
    <nav class="nav container" aria-label="Main navigation">
      <a class="brand" href="#home" aria-label="Perumal home">Perumal<span>.A</span></a>
      <button class="menu-toggle" id="menuToggle" aria-expanded="false" aria-controls="navLinks" aria-label="Toggle navigation">☰ Menu</button>
      <ul class="nav-links" id="navLinks">
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#education">Education</a></li>
        <li><a href="#certificates">Certificates</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <section class="hero" id="home">
      <div class="container hero-grid">
        <div class="hero-copy">
          <span class="eyebrow"><span class="dot"></span> First-year IT student · Open to learning</span>
          <h1>Hi, I'm<br><span class="gradient-text">Perumal.A</span></h1>
          <h2>Passionate IT Student &amp; Aspiring Web Developer</h2>
          <p>I enjoy turning creative ideas into clean, user-friendly digital experiences. I'm building my foundation in web development and programming, one project and one new concept at a time.</p>
          <div class="actions">
            <a class="btn btn-primary" href="#projects">Explore My Work <span aria-hidden="true">↗</span></a>
            <a class="btn btn-secondary" href="#contact">Get in Touch <span aria-hidden="true">✉</span></a>
          </div>
        </div>
        <aside class="hero-card glass" aria-label="Portfolio introduction card">
          <div class="avatar" aria-hidden="true">PA</div>
          <h3>Perumal A.</h3>
          <p class="sub">Information Technology</p>
          <div class="mini-stats">
            <div class="stat"><strong>HTML &amp; CSS</strong><span>Web foundations</span></div>
            <div class="stat"><strong>Python</strong><span>Programming basics</span></div>
            <div class="stat"><strong>Curious</strong><span>Always learning</span></div>
            <div class="stat"><strong>Creative</strong><span>Problem-solving</span></div>
          </div>
        </aside>
      </div>
    </section>

    <section id="about">
      <div class="container">
        <div class="section-heading reveal">
          <span class="kicker">A little about me</span>
          <h2 class="section-title">Curious mind. <span class="gradient-text">Builder mindset.</span></h2>
          <p class="section-intro">I'm at the beginning of my technology journey, excited to learn how ideas become useful digital products.</p>
        </div>
        <div class="about-grid">
          <article class="panel glass reveal">
            <h3>My Story</h3>
            <p>I am a first-year Information Technology student with a strong curiosity for how the web works and a passion for building clean, user-friendly digital experiences. I enjoy turning creative ideas into functional websites while continuously expanding my technical knowledge. Currently, I am sharpening my fundamentals in web development and programming, driven to learn modern technologies and solve real-world problems through code.</p>
          </article>
          <article class="panel glass reveal">
            <h3>What I'm focused on</h3>
            <div class="focus-list">
              <div class="focus-item"><span class="icon-box">⌘</span><div><strong>Building strong fundamentals</strong><span>Practising HTML, CSS, and programming basics.</span></div></div>
              <div class="focus-item"><span class="icon-box">✦</span><div><strong>Designing for people</strong><span>Creating clear, responsive, and easy-to-use pages.</span></div></div>
              <div class="focus-item"><span class="icon-box">↗</span><div><strong>Growing through projects</strong><span>Learning by experimenting, building, and improving.</span></div></div>
            </div>
          </article>
        </div>
      </div>
    </section>

    <section id="skills">
      <div class="container">
        <div class="section-heading reveal">
          <span class="kicker">What I work with</span>
          <h2 class="section-title">My <span class="gradient-text">technical toolkit</span></h2>
          <p class="section-intro">Skills I'm developing as I grow into a confident web developer.</p>
        </div>
        <div class="skills-grid">
          <article class="skill-card glass reveal">
            <h3>🌐 Core Web Technologies</h3>
            <div class="tags"><span class="tag">HTML5</span><span class="tag">CSS3</span><span class="tag">Flexbox</span><span class="tag">CSS Grid</span><span class="tag">Responsive Design</span></div>
          </article>
          <article class="skill-card glass reveal">
            <h3>💻 Programming Languages</h3>
            <div class="tags"><span class="tag">Python</span><span class="tag">JavaScript Basics</span></div>
          </article>
          <article class="skill-card glass reveal">
            <h3>🛠️ Development Tools</h3>
            <div class="tags"><span class="tag">Visual Studio Code</span><span class="tag">Git Basics</span><span class="tag">GitHub Basics</span></div>
          </article>
          <article class="skill-card glass reveal">
            <h3>✨ Soft Skills</h3>
            <div class="tags"><span class="tag">Problem-Solving</span><span class="tag">Team Collaboration</span><span class="tag">Analytical Thinking</span><span class="tag">Eagerness to Learn</span></div>
          </article>
        </div>
      </div>
    </section>

    <section id="projects">
      <div class="container">
        <div class="section-heading reveal">
          <span class="kicker">Learning by doing</span>
          <h2 class="section-title">Featured <span class="gradient-text">projects</span></h2>
          <p class="section-intro">A place to showcase what I build. Replace these starter cards with your real projects as you complete them.</p>
        </div>
        <div class="projects-grid">
          <article class="project-card glass reveal">
            <div class="project-art" aria-hidden="true">✧</div>
            <div class="project-content">
              <h3>Personal Portfolio Website</h3>
              <p>A responsive portfolio introducing my background, skills, learning journey, and future work. Built as a single HTML file.</p>
              <div class="tags"><span class="tag">HTML</span><span class="tag">CSS</span><span class="tag">JavaScript</span></div>
            </div>
          </article>
          <article class="project-card glass reveal">
            <div class="project-art" aria-hidden="true">⌘</div>
            <div class="project-content">
              <h3>My Next Web Project</h3>
              <p>Use this space for your next mini-project, such as a student information page, a simple calculator, or a landing page.</p>
              <div class="tags"><span class="tag">In progress</span><span class="tag">Practice</span></div>
            </div>
          </article>
        </div>
      </div>
    </section>

    <section id="education">
      <div class="container">
        <div class="section-heading reveal">
          <span class="kicker">My learning journey</span>
          <h2 class="section-title">Education &amp; <span class="gradient-text">growth</span></h2>
        </div>
        <div class="timeline">
          <article class="timeline-item glass reveal">
            <div class="timeline-icon" aria-hidden="true">🎓</div>
            <div>
              <h3>Bachelor's Degree in Information Technology</h3>
              <p>First-year Engineering Student · Currently studying</p>
              <span class="status">In progress</span>
            </div>
          </article>
          <article class="timeline-item glass reveal">
            <div class="timeline-icon" aria-hidden="true">📘</div>
            <div>
              <h3>Independent Learning</h3>
              <p>Practising HTML, CSS, Python, and the basics of JavaScript while exploring modern web development.</p>
              <span class="status">Learning every day</span>
            </div>
          </article>
        </div>
      </div>
    </section>

    <section id="certificates">
      <div class="container">
        <div class="section-heading reveal">
          <span class="kicker">Milestones</span>
          <h2 class="section-title">Certificates &amp; <span class="gradient-text">achievements</span></h2>
          <p class="section-intro">Showcase verified courses, workshop certificates, and achievements here.</p>
        </div>
        <div class="cert-note glass reveal">
          <strong>Ready for your achievements</strong>
          <p style="margin-top:8px">No certificates have been added yet. When you earn one, update this section with its title, issuing organisation, and completion date. Only list certificates you've actually received.</p>
        </div>
      </div>
    </section>

    <section id="social">
      <div class="container">
        <div class="section-heading reveal">
          <span class="kicker">Find me online</span>
          <h2 class="section-title">Social <span class="gradient-text">links</span></h2>
          <p class="section-intro">Add your profile URLs to connect with classmates, developers, and future collaborators.</p>
        </div>
        <div class="social-grid reveal">
          <a class="social-link" href="https://github.com/" target="_blank" rel="noopener noreferrer"><span aria-hidden="true">⌘</span> GitHub <span aria-hidden="true">↗</span></a>
          <a class="social-link" href="https://www.linkedin.com/" target="_blank" rel="noopener noreferrer"><span aria-hidden="true">in</span> LinkedIn <span aria-hidden="true">↗</span></a>
          <a class="social-link" href="https://www.instagram.com/" target="_blank" rel="noopener noreferrer"><span aria-hidden="true">◎</span> Instagram <span aria-hidden="true">↗</span></a>
        </div>
        <p class="form-note" style="margin-top:13px">These links currently open the main websites. Replace them with your own profile links before publishing.</p>
      </div>
    </section>

    <section id="contact">
      <div class="container">
        <div class="section-heading reveal">
          <span class="kicker">Let's connect</span>
          <h2 class="section-title">Get in <span class="gradient-text">touch</span></h2>
          <p class="section-intro">Have an idea, learning resource, or project to discuss? I'd be glad to hear from you.</p>
        </div>
        <div class="contact-grid">
          <div class="panel glass reveal">
            <h3>Contact details</h3>
            <p>I'm interested in learning from others, collaborating on beginner-friendly projects, and exploring new ideas in technology.</p>
            <div class="contact-detail"><span class="icon-box">✉</span><div><strong>Email</strong><span>Add your email address here</span></div></div>
            <div class="contact-detail"><span class="icon-box">⌘</span><div><strong>Field</strong><span>Information Technology</span></div></div>
            <div class="contact-detail"><span class="icon-box">↗</span><div><strong>Current goal</strong><span>Learn, build, and improve</span></div></div>
          </div>
          <div class="panel glass reveal">
            <h3>Send a message</h3>
            <form id="contactForm">
              <label for="senderName">Your name<input id="senderName" name="senderName" autocomplete="name" required placeholder="Enter your name"></label>
              <label for="senderEmail">Your email<input id="senderEmail" name="senderEmail" type="email" autocomplete="email" required placeholder="you@example.com"></label>
              <label for="message">Message<textarea id="message" name="message" required placeholder="Write your message..."></textarea></label>
              <button class="btn btn-primary" type="submit">Prepare Email <span aria-hidden="true">↗</span></button>
              <p class="form-note">This form opens your email app with a draft. Add your real email address in the code first.</p>
            </form>
          </div>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="container footer-row">
      <p>© <span id="year"></span> Perumal.A · Built with curiosity and code.</p>
      <a class="top-link" href="#home">Back to top ↑</a>
    </div>
  </footer>

  <script>
    // Mobile navigation
    const menuToggle = document.getElementById('menuToggle');
    const navLinks = document.getElementById('navLinks');
    menuToggle.addEventListener('click', () => {
      const isOpen = navLinks.classList.toggle('open');
      menuToggle.setAttribute('aria-expanded', String(isOpen));
      menuToggle.textContent = isOpen ? '✕ Close' : '☰ Menu';
    });
    navLinks.querySelectorAll('a').forEach(link => {
      link.addEventListener('click', () => {
        navLinks.classList.remove('open');
        menuToggle.setAttribute('aria-expanded', 'false');
        menuToggle.textContent = '☰ Menu';
      });
    });

    // Reveal cards as they enter the viewport
    const revealItems = document.querySelectorAll('.reveal');
    if ('IntersectionObserver' in window) {
      const observer = new IntersectionObserver((entries, obs) => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            entry.target.classList.add('visible');
            obs.unobserve(entry.target);
          }
        });
      }, { threshold: 0.12 });
      revealItems.forEach(item => observer.observe(item));
    } else {
      revealItems.forEach(item => item.classList.add('visible'));
    }

    // Highlight the current navigation section
    const sections = document.querySelectorAll('main section[id]');
    const navAnchors = navLinks.querySelectorAll('a');
    if ('IntersectionObserver' in window) {
      const sectionObserver = new IntersectionObserver(entries => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            navAnchors.forEach(a => a.classList.toggle('active', a.getAttribute('href') === '#' + entry.target.id));
          }
        });
      }, { rootMargin: '-35% 0px -55% 0px' });
      sections.forEach(section => sectionObserver.observe(section));
    }

    document.getElementById('year').textContent = new Date().getFullYear();

    // Set YOUR real email address in the line below before using the contact form.
    const portfolioEmail = 'your-email@example.com';
    document.getElementById('contactForm').addEventListener('submit', event => {
      event.preventDefault();
      if (portfolioEmail === 'your-email@example.com') {
        alert('Before using this form, open the HTML file and replace your-email@example.com in the JavaScript with your real email address.');
        return;
      }
      const name = document.getElementById('senderName').value.trim();
      const email = document.getElementById('senderEmail').value.trim();
      const message = document.getElementById('message').value.trim();
      const subject = encodeURIComponent('Portfolio message from ' + name);
      const body = encodeURIComponent('From: ' + name + '\nReply to: ' + email + '\n\n' + message);
      window.location.href = 'mailto:' + portfolioEmail + '?subject=' + subject + '&body=' + body;
    });
  </script>
</body>
</html>


