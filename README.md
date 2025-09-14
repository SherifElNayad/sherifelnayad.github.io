<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Sherif Abd El Khalek Ali — Backend Engineer</title>
  <meta name="description" content="Sherif Abd El Khalek Ali — Java Backend Developer (Spring Boot, Microservices, Kafka). Portfolio, experience, projects, and contact." />
  <meta name="theme-color" content="#0b0f17" />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg: #0b0f17;            /* page background */
      --panel: #0f1624;         /* cards */
      --panel-2:#0b1320;        /* alt cards */
      --text: #e6edf3;          /* main text */
      --muted:#93a1b3;          /* secondary text */
      --brand:#00c2ff;          /* cyan */
      --brand-2:#7c4dff;        /* purple */
      --ok:#22c55e;             /* green */
      --warn:#f59e0b;           /* amber */
      --danger:#ef4444;         /* red */
      --ring: 0 0 0 2px color-mix(in lab, var(--brand) 65%, transparent);
      --radius: 18px;
      --shadow: 0 20px 60px rgba(0,0,0,.45), 0 0 1px rgba(255,255,255,.05) inset;
      --glass: linear-gradient(180deg, rgba(255,255,255,.04), rgba(255,255,255,.02));
      --grid-gap: 22px;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family: Inter, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, "Apple Color Emoji", "Segoe UI Emoji";
      background: radial-gradient(1200px 800px at 100% -10%, rgba(124,77,255,.25), transparent),
                  radial-gradient(900px 600px at -10% 10%, rgba(0,194,255,.22), transparent),
                  var(--bg);
      color:var(--text);
      line-height:1.6;
      letter-spacing:.1px;
    }
    a{color:var(--brand);text-decoration:none}
    a:hover{opacity:.9}

    /* Layout */
    .wrap{max-width:1180px;margin-inline:auto;padding:28px}
    header.site{
      position:relative;
      border-radius: calc(var(--radius) + 6px);
      padding:42px;
      background: var(--glass);
      backdrop-filter: blur(8px);
      border:1px solid rgba(255,255,255,.06);
      box-shadow: var(--shadow);
      overflow:hidden;
      isolation:isolate;
    }
    .glow{position:absolute;inset:auto -20% -80% -20%;height:300px;filter: blur(60px);opacity:.55;background:conic-gradient(from 120deg at 50% 50%, rgba(0,194,255,.25), rgba(124,77,255,.25), transparent 65%)}

    nav.top{
      display:flex;gap:14px;align-items:center;justify-content:space-between;margin-bottom:30px
    }
    .brand{display:flex;align-items:center;gap:12px;font-weight:800;font-size:1.1rem;letter-spacing:.4px}
    .brand .dot{width:12px;height:12px;border-radius:50%;background:linear-gradient(135deg,var(--brand),var(--brand-2));box-shadow:0 0 0 4px rgba(124,77,255,.15),0 0 18px var(--brand)}
    .links{display:flex;gap:18px;flex-wrap:wrap}
    .links a{color:var(--muted)}

    .hero{display:grid;grid-template-columns: 1.1fr .9fr;gap:36px;align-items:center}
    .me{
      display:flex;flex-direction:column;gap:14px
    }
    .kicker{color:var(--brand);font-weight:600;letter-spacing:.2em;text-transform:uppercase;font-size:.82rem}
    h1{
      margin:0;font-size:clamp(1.9rem, 2vw + 1.4rem, 3.2rem);line-height:1.1;
      background: linear-gradient(180deg, #fff, #c7d2fe 60%, #9adfff);
      background-clip: text;-webkit-background-clip:text;color:transparent;
      text-wrap:balance
    }
    .tagline{color:var(--muted);margin-top:6px;max-width:62ch}
    .cta{display:flex;gap:14px;margin-top:18px;flex-wrap:wrap}
    .btn{display:inline-flex;align-items:center;gap:10px;padding:12px 16px;border-radius:14px;border:1px solid rgba(255,255,255,.08);background:linear-gradient(180deg, rgba(255,255,255,.06), rgba(255,255,255,.01));box-shadow:var(--shadow);color:#fff}
    .btn.primary{background:linear-gradient(135deg,var(--brand),var(--brand-2));border-color:transparent}
    .btn:hover{transform:translateY(-1px)}

    .avatar{
      width:min(260px, 100%);
      aspect-ratio:1/1;border-radius:22px;
      background:linear-gradient(135deg, rgba(124,77,255,.25), rgba(0,194,255,.3));
      border:1px solid rgba(255,255,255,.08);
      padding:8px;box-shadow: var(--shadow);
    }
    .avatar > div{width:100%;height:100%;border-radius:16px;background: url('https://avatars.githubusercontent.com/u/9919?s=200&v=4') center/cover, linear-gradient(180deg,#0e1623,#0b1220)}

    /* Section shell */
    section{margin-top:42px}
    .section-title{display:flex;align-items:center;gap:12px;margin:4px 0 18px;font-weight:800;letter-spacing:.6px;text-transform:uppercase;color:var(--muted);font-size:.88rem}
    .section-title .bar{height:10px;width:10px;border-radius:2px;background:linear-gradient(135deg,var(--brand),var(--brand-2))}

    /* Cards */
    .grid{display:grid;gap:var(--grid-gap)}
    .cols-3{grid-template-columns:repeat(3,1fr)}
    .cols-2{grid-template-columns:repeat(2,1fr)}
    .card{
      background:var(--panel);
      border:1px solid rgba(255,255,255,.06);
      border-radius:var(--radius);
      padding:20px 22px;
      box-shadow:var(--shadow);
      transition:transform .2s ease, border-color .2s ease;
    }
    .card:hover{transform:translateY(-4px);border-color:rgba(0,194,255,.25)}

    /* Experience */
    .xp{display:grid;gap:10px}
    .xp .header{display:flex;justify-content:space-between;gap:10px;flex-wrap:wrap}
    .xp .role{font-weight:700}
    .xp .meta{color:var(--muted);font-size:.95rem}
    .tags{display:flex;gap:8px;flex-wrap:wrap;margin-top:8px}
    .tag{font-size:.8rem;border:1px solid rgba(255,255,255,.09);color:#dbeafe;background:rgba(124,77,255,.08);padding:6px 10px;border-radius:999px}

    /* Projects */
    .project{display:grid;gap:10px}
    .project .title{font-weight:700}
    .project .stack{color:var(--muted)}

    /* Skills */
    .skills{display:flex;flex-wrap:wrap;gap:10px}
    .skills .chip{border:1px solid rgba(255,255,255,.09);background:rgba(255,255,255,.04);padding:8px 12px;border-radius:999px}

    /* Contact */
    .contact{display:grid;gap:10px}
    .contact a{color:#e6edf3}
    .contact .row{display:flex;gap:12px;flex-wrap:wrap}

    footer{margin:46px 0 12px;color:var(--muted);font-size:.9rem;display:flex;justify-content:space-between;flex-wrap:wrap;gap:10px}

    /* Responsive */
    @media (max-width: 980px){
      .hero{grid-template-columns:1fr}
      .cols-3{grid-template-columns:1fr 1fr}
      .cols-2{grid-template-columns:1fr}
    }
    @media (max-width: 640px){
      .cols-3{grid-template-columns:1fr}
      .wrap{padding:20px}
      header.site{padding:28px}
    }

    /* Tiny animation */
    @keyframes pulseGlow {from{box-shadow:0 0 0 0 rgba(0,194,255,.35)} to{box-shadow:0 0 0 14px rgba(0,194,255,0)}}
    .pulse{animation:pulseGlow 2s infinite}
  </style>
</head>
<body>
  <div class="wrap">
    <header class="site">
      <div class="glow" aria-hidden></div>
      <nav class="top">
        <div class="brand"><span class="dot"></span> Sherif Abd El Khalek Ali</div>
        <div class="links">
          <a href="#experience">Experience</a>
          <a href="#projects">Projects</a>
          <a href="#skills">Skills</a>
          <a href="#contact">Contact</a>
        </div>
      </nav>

      <div class="hero">
        <div class="me">
          <div class="kicker">Java Backend Developer</div>
          <h1>Building resilient microservices with Spring Boot, Kafka & clean architecture.</h1>
          <p class="tagline">I design and deliver backend systems that are observable, secure, and easy to evolve. I enjoy replacing brittle monolith bits with well‑bounded, event‑driven services.</p>
          <div class="cta">
            <a class="btn primary pulse" href="#contact">Hire Me</a>
            <a class="btn" href="https://www.linkedin.com/in/sherif-abd-el-khalek-96b9a4162" target="_blank" rel="noopener">LinkedIn</a>
            <a class="btn" href="mailto:Sherifali121@gmail.com">Email</a>
          </div>
        </div>
        <div class="avatar" aria-hidden>
          <div title="Sherif's photo placeholder"></div>
        </div>
      </div>
    </header>

    <!-- Experience -->
    <section id="experience">
      <div class="section-title"><span class="bar"></span> Experience</div>
      <div class="grid cols-2">
        <article class="card xp">
          <div class="header">
            <div class="role">Java Backend Developer — Etisalat& (e&)</div>
            <div class="meta">Nov 2024 – Present · Cairo, Egypt</div>
          </div>
          <ul>
            <li>Designed & developed new <strong>microservices</strong> to replace legacy monolithic components.</li>
            <li>Utilized <strong>PL/SQL</strong> for efficient data retrieval & manipulation.</li>
            <li>Built backend services with <strong>Spring Boot, JPA, Hibernate</strong>.</li>
            <li>Adopted <strong>Kafka</strong> for inter‑service communication & streaming.</li>
          </ul>
          <div class="tags">
            <span class="tag">Spring Boot</span><span class="tag">Kafka</span><span class="tag">JPA</span><span class="tag">PL/SQL</span>
          </div>
        </article>

        <article class="card xp">
          <div class="header">
            <div class="role">Java Backend Developer — Flairstech (Ciena)</div>
            <div class="meta">Apr 2024 – Nov 2024 · Cairo, Egypt</div>
          </div>
          <ul>
            <li>Collaborated in sprint planning & provided accurate task estimates.</li>
            <li>Developed & integrated new features across squads and services.</li>
            <li>Coordinated cross‑squad integration for complex feature delivery.</li>
          </ul>
          <div class="tags">
            <span class="tag">Spring Boot</span><span class="tag">Microservices</span><span class="tag">Agile</span>
          </div>
        </article>

        <article class="card xp">
          <div class="header">
            <div class="role">Java Backend Developer — Silicon Expert</div>
            <div class="meta">Jan 2022 – Mar 2023 · Cairo, Egypt</div>
          </div>
          <ul>
            <li>Built backend solutions with <strong>Spring Boot, JPA, Hibernate</strong>.</li>
            <li>Utilized <strong>SQL</strong> to ensure efficient data access.</li>
            <li>Worked with cross‑functional squads to address customer needs.</li>
            <li>Improved system reliability by resolving legacy API issues.</li>
          </ul>
          <div class="tags">
            <span class="tag">Spring Boot</span><span class="tag">Hibernate</span><span class="tag">SQL</span>
          </div>
        </article>
      </div>
    </section>

    <!-- Projects -->
    <section id="projects">
      <div class="section-title"><span class="bar"></span> Projects</div>
      <div class="grid cols-3">
        <article class="card project">
          <div class="title">Digital Certificates Using Blockchain</div>
          <div class="stack">Hyperledger Fabric · Vue.js</div>
          <p>A web platform for issuing and verifying academic graduation certificates across a secure consortium of universities and recruiters.</p>
        </article>
        <article class="card project">
          <div class="title">Wabtec CMT</div>
          <div class="stack">Spring Boot · Java</div>
          <p>Manages component metadata to guide purchase decisions with up‑to‑date part info and market prices, reducing manual communication.</p>
        </article>
        <article class="card project">
          <div class="title">Eshtri Aqar</div>
          <div class="stack">Spring Boot</div>
          <p>E‑commerce for real‑estate transactions; showcases units and streamlines buying flows to help users make confident decisions.</p>
        </article>
      </div>
    </section>

    <!-- Skills -->
    <section id="skills">
      <div class="section-title"><span class="bar"></span> Skills</div>
      <div class="card">
        <div class="skills">
          <span class="chip">Java</span>
          <span class="chip">Spring Boot</span>
          <span class="chip">Hibernate / JPA</span>
          <span class="chip">SQL / PL/SQL</span>
          <span class="chip">Kafka</span>
          <span class="chip">Microservices</span>
          <span class="chip">REST APIs</span>
          <span class="chip">Vue.js</span>
          <span class="chip">Flutter</span>
          <span class="chip">Laravel</span>
          <span class="chip">Node.js</span>
          <span class="chip">Ruby on Rails</span>
          <span class="chip">JavaScript</span>
          <span class="chip">Python</span>
          <span class="chip">Dart</span>
          <span class="chip">C++</span>
        </div>
      </div>
    </section>

    <!-- Contact -->
    <section id="contact">
      <div class="section-title"><span class="bar"></span> Contact</div>
      <div class="card contact">
        <div class="row"><strong>Email:</strong> <a href="mailto:Sherifali121@gmail.com">Sherifali121@gmail.com</a></div>
        <div class="row"><strong>Phone:</strong> <a href="tel:+201060512256">+20 106 051 2256</a></div>
        <div class="row"><strong>LinkedIn:</strong> <a href="https://www.linkedin.com/in/sherif-abd-el-khalek-96b9a4162/" target="_blank" rel="noopener">linkedin.com/in/sherif-el-nayad-96b9a4162</a></div>
      </div>
    </section>

    <footer>
      <span>© <span id="year"></span> Sherif Abd El Khalek Ali</span>
      <span>Built with ♥ in Cairo</span>
    </footer>
  </div>

  <script>
    // tiny JS just for the year and anchor scroll polish
    document.getElementById('year').textContent = new Date().getFullYear();
    document.querySelectorAll('a[href^="#"]').forEach(a=>{
      a.addEventListener('click', e=>{
        const id = a.getAttribute('href');
        if(id.length>1){ e.preventDefault(); document.querySelector(id)?.scrollIntoView({behavior:'smooth'}); }
      });
    });
  </script>
</body>
</html>
