# Portfolio-2
mon portfolio 

<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#F5A623">
<title>Koulidiati Ange Lionel — Graphiste designer</title>
<meta name="description" content="Portfolio de Koulidiati Ange Lionel —Graphiste designer, spécialiste IA & automatisation, basé à Ouagadougou, Burkina Faso.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@500;700&family=Inter:wght@400;500;600&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root{
    --bg:#0b0b0d;
    --bg-alt:#141416;
    --card:#19191c;
    --border:#2a2a2e;
    --text:#f5f2ec;
    --text-dim:#1a084f;
    --accent:#2b0244;
    --accent-deep:#d68a12;
    --radius:14px;
  }
  *{box-sizing:border-box; margin:0; padding:0;}
  html{scroll-behavior:smooth;}
  body{
    background:var(--bg);
    color:var(--text);
    font-family:'Inter',sans-serif;
    line-height:1.5;
    -webkit-font-smoothing:antialiased;
    overflow-x:hidden;
  }
  h1,h2,h3,.display{
    font-family:'Space Grotesk',sans-serif;
    font-weight:700;
    letter-spacing:-0.02em;
    line-height:1.05;
  }
  .mono{
    font-family:'JetBrains Mono',monospace;
    font-size:0.72rem;
    letter-spacing:0.12em;
    text-transform:uppercase;
  }
  a{color:inherit; text-decoration:none;}
  img{max-width:100%; display:block;}
  .wrap{max-width:1180px; margin:0 auto; padding:0 32px;}
  @media (max-width:640px){.wrap{padding:0 20px;}}

  /* signature element: rotating asterisk */
  .ast{
    display:inline-block;
    color:var(--accent);
    animation:spin 9s linear infinite;
  }
  @keyframes spin{to{transform:rotate(360deg);}}
  @media (prefers-reduced-motion: reduce){
    .ast{animation:none;}
  }

  /* ---------- header ---------- */
  header{
    position:sticky; top:0; z-index:50;
    background:rgba(11,11,13,0.85);
    backdrop-filter:blur(10px);
    border-bottom:1px solid var(--border);
  }
  .nav{
    display:flex; align-items:center; justify-content:space-between;
    height:72px;
  }
  .logo{
    display:flex; align-items:center; gap:8px;
    font-family:'Space Grotesk',sans-serif; font-weight:700; font-size:1.05rem;
  }
  .logo .ast{font-size:1.1rem;}
  nav ul{display:flex; gap:32px; list-style:none;}
  nav ul a{font-size:0.88rem; color:var(--text-dim); transition:color .2s;}
  nav ul a:hover{color:var(--text);}
  .btn{
    display:inline-flex; align-items:center; gap:8px;
    padding:10px 20px; border-radius:999px;
    font-size:0.85rem; font-weight:600;
    transition:transform .2s, background .2s, color .2s;
  }
  .btn-accent{background:var(--accent); color:#10100f;}
  .btn-accent:hover{transform:translateY(-2px); background:#ffb84d;}
  .btn-ghost{border:1px solid var(--border); color:var(--text);}
  .btn-ghost:hover{border-color:var(--accent); color:var(--accent);}
  .nav-cta{display:flex; align-items:center; gap:16px;}
  .nav-toggle{display:none; background:none; border:none; color:var(--text); font-size:1.4rem;}

  @media (max-width:860px){
    nav ul{display:none;}
    .nav-toggle{display:block;}
  }

  /* ---------- badge ---------- */
  .badge{
    display:inline-flex; align-items:center; gap:8px;
    padding:6px 14px; border:1px solid var(--border); border-radius:999px;
    font-size:0.78rem; color:var(--text-dim); margin-bottom:28px;
  }
  .dot{width:7px; height:7px; border-radius:50%; background:#4ade80; box-shadow:0 0 8px #4ade80;}

  /* ---------- hero ---------- */
  .hero{padding:64px 0 0;}
  .hero-grid{
    display:grid; grid-template-columns:1.15fr 0.85fr; gap:48px; align-items:end;
  }
  .hero h1{font-size:clamp(2.4rem, 5.6vw, 4.4rem); margin-bottom:24px;}
  .hero h1 .ast{font-size:0.6em;}
  .hero p.lead{font-size:1.1rem; color:var(--text-dim); max-width:480px; margin-bottom:32px;}
  .tag-line{font-size:0.78rem; color:var(--text-dim); letter-spacing:0.1em; text-transform:uppercase; margin-bottom:28px;}
  .hero-cta{display:flex; gap:14px; flex-wrap:wrap;}
  .hero-photo{
    border-radius:var(--radius);
    overflow:hidden;
    aspect-ratio:4/5;
    background:var(--card);
    border:1px solid var(--border);
  }
  .hero-photo img{width:100%; height:100%; object-fit:cover;}
  @media (max-width:860px){
    .hero-grid{grid-template-columns:1fr; }
    .hero-photo{max-width:280px;}
  }

  /* ---------- marquee ---------- */
  .marquee-strip{
    border-top:1px solid var(--border); border-bottom:1px solid var(--border);
    background:var(--bg-alt);
    overflow:hidden;
    margin-top:56px;
    padding:18px 0;
  }
  .marquee-track{
    display:flex; width:max-content;
    animation:marquee 32s linear infinite;
    gap:14px;
  }
  .marquee-track span{
    font-family:'Space Grotesk',sans-serif; font-weight:500;
    font-size:1.1rem; color:var(--text-dim); white-space:nowrap;
  }
  .marquee-track span.x{color:var(--accent);}
  @keyframes marquee{from{transform:translateX(0);} to{transform:translateX(-50%);}}

  /* ---------- quote block ---------- */
  .quote-block{
    padding:96px 0; text-align:center;
  }
  .quote-block .eyebrow{color:var(--accent); margin-bottom:18px;}
  .quote-block h2{
    font-size:clamp(1.6rem, 4vw, 2.6rem);
    max-width:760px; margin:0 auto;
}
  .quote-block h2 em{font-style:italic; color:var(--text-dim);}

  /* ---------- section shell ---------- */
  section{padding:88px 0;}
  .section-head{margin-bottom:48px;}
  .eyebrow{
    font-family:'JetBrains Mono',monospace; font-size:0.72rem; letter-spacing:0.14em;
    text-transform:uppercase; color:var(--accent); margin-bottom:14px; display:block;
  }
  .section-head h2{font-size:clamp(1.8rem,3.6vw,2.6rem);}

  /* ---------- projects ---------- */
  .projects-grid{
    display:grid; grid-template-columns:1fr 1fr; gap:1px;
    background:var(--border); border:1px solid var(--border); border-radius:var(--radius); overflow:hidden;
  }
  .project-card{
    background:var(--bg); padding:36px; display:flex; flex-direction:column; gap:16px;
    transition:background .25s;
  }
  .project-card:hover{background:var(--card);}
  .project-num{font-family:'JetBrains Mono',monospace; color:var(--accent); font-size:0.85rem;}
  .project-tags{color:var(--text-dim); font-size:0.78rem;}
  .project-card h3{font-size:1.4rem;}
  .project-card p{color:var(--text-dim); font-size:0.92rem; flex:1;}
  .project-foot{display:flex; align-items:center; justify-content:space-between; font-size:0.82rem;}
  .project-foot .yr{color:var(--text-dim);}
  .project-foot .lnk{color:var(--accent); font-weight:600;}
  .project-card:hover .lnk{text-decoration:underline;}
  @media (max-width:720px){.projects-grid{grid-template-columns:1fr;}}

  /* ---------- stack ---------- */
  .stack-grid{display:grid; grid-template-columns:repeat(4,1fr); gap:28px;}
  .stack-col h4{font-size:0.85rem; color:var(--accent); margin-bottom:16px; letter-spacing:0.04em;}
  .stack-col ul{list-style:none;}
  .stack-col li{
    padding:10px 0; border-bottom:1px solid var(--border);
    font-size:0.92rem; color:var(--text-dim);
  }
  @media (max-width:860px){.stack-grid{grid-template-columns:repeat(2,1fr); row-gap:36px;}}

  .stats-bar{
    margin-top:64px; padding-top:48px; border-top:1px solid var(--border);
    display:grid; grid-template-columns:repeat(4,1fr); gap:24px;
  }
  .stat .num{font-family:'Space Grotesk',sans-serif; font-weight:700; font-size:2.2rem; color:var(--accent);}
  .stat .lbl{font-size:0.82rem; color:var(--text-dim); margin-top:4px;}
  @media (max-width:640px){.stats-bar{grid-template-columns:repeat(2,1fr); row-gap:32px;}}

  /* ---------- about ---------- */
  .about-grid{display:grid; grid-template-columns:1fr 320px; gap:56px; align-items:start;}
  .about-grid p{color:var(--text-dim); margin-bottom:18px; font-size:1.02rem; max-width:620px;}
  .about-grid strong{color:var(--text);}
  .langs{display:flex; gap:18px; margin-top:24px; font-size:0.9rem; color:var(--text-dim);}
  .about-photo{
    border-radius:var(--radius); overflow:hidden; border:1px solid var(--border);
    aspect-ratio:1/1;
  }
  .about-photo img{width:100%; height:100%; object-fit:cover;}
  .loc-tag{
    margin-top:14px; display:inline-flex; gap:8px; align-items:center;
    font-size:0.85rem; color:var(--text-dim);
  }
  @media (max-width:860px){.about-grid{grid-template-columns:1fr;} .about-photo{max-width:260px;}}

  /* ---------- certifications ---------- */
  .cert-grid{display:grid; grid-template-columns:repeat(4,1fr); gap:20px;}
  .cert-card{
    background:var(--card); border:1px dashed var(--border); border-radius:var(--radius);
    padding:28px 22px; min-height:140px;
    display:flex; flex-direction:column; justify-content:space-between;
  }
  .cert-card h4{font-size:0.95rem; color:var(--text-dim); font-weight:500;}
  .cert-card .org{font-size:0.78rem; color:var(--text-dim); opacity:0.6; margin-top:6px;}
  .cert-status{
    align-self:flex-start; margin-top:14px;
    font-size:0.7rem; padding:4px 10px; border-radius:999px;
    font-family:'JetBrains Mono',monospace; letter-spacing:0.06em;
  }
  .cert-status.validated{background:rgba(74,222,128,0.12); color:#4ade80;}
  .cert-status.soon{background:rgba(245,166,35,0.12); color:var(--accent);}
  .cert-note{
    margin-top:28px; font-size:0.85rem; color:var(--text-dim);
    border-left:2px solid var(--accent); padding-left:16px;
  }
  @media (max-width:860px){.cert-grid{grid-template-columns:repeat(2,1fr);}}

  /* ---------- contact ---------- */
  .contact{text-align:center;}
  .contact h2{font-size:clamp(2rem,5vw,3.4rem); margin-bottom:20px;}
  .contact p{color:var(--text-dim); max-width:480px; margin:0 auto 36px;}
  .contact-links{display:flex; justify-content:center; gap:28px; flex-wrap:wrap; margin-top:40px;}
  .contact-links a{
    font-size:0.92rem; color:var(--text-dim); border-bottom:1px solid transparent; padding-bottom:2px;
    transition:color .2s, border-color .2s;
  }
  .contact-links a:hover{color:var(--accent); border-color:var(--accent);}

  /* ---------- footer ---------- */
  footer{
    border-top:1px solid var(--border); padding:32px 0;
    display:flex; justify-content:space-between; align-items:center;
    font-size:0.78rem; color:var(--text-dim);
  }
  @media (max-width:640px){footer{flex-direction:column; gap:10px; text-align:center;}}
</style>
</head>
<body>

<header>
  <div class="wrap nav">
    <a class="logo" href="#"><span class="ast">✳</span> Koulidiati Ange Lionel</a>
    <nav><ul>
      <li><a href="#works">Projets</a></li>
      <li><a href="#stack">Stack</a></li>
      <li><a href="#about">À propos</a></li>
      <li><a href="#certifications">Certifs</a></li>
    </ul></nav>
    <div class="nav-cta">
      <a class="btn btn-accent" href="#contact">Me contacter →</a>
    </div>
  </div>
</header>

<main>
  <!-- HERO -->
  <section class="hero">
    <div class="wrap">
      <span class="badge"><span class="dot"></span> Disponible · Missions freelance · 2026</span>
      <div class="hero-grid">
        <div>
          <p class="tag-line">Identités web · Applications SaaS · Automatisation IA · Prompt Engineering</p>
          <h1>Déve­loppeur<br>Full-Stack &amp; IA <span class="ast">✳</span></h1>
          <p class="lead">Concevoir des systèmes web robustes et des pipelines IA scalables — pas des projets isolés.</p>
          <div class="hero-cta">
            <a class="btn btn-accent" href="#works">→ Voir mes projets</a>
            <a class="btn btn-ghost" href="#contact">Discutons</a>
          </div>
        </div>
        <div class="hero-photo">
          <img src="https://flickwick.pplx.app/avatar.jpg" alt="Koulidiati Ange Lionel">
        </div>
      </div>
    </div>

    <div class="marquee-strip">
      <div class="marquee-track">
        <span>Développement Web</span><span class="x">✳</span>
        <span>Applications SaaS</span><span class="x">✳</span>
        <span>Automatisation IA</span><span class="x">✳</span>
        <span>Prompt Engineering</span><span class="x">✳</span>
        <span>Design UX/UI</span><span class="x">✳</span>
        <span>APIs &amp; Intégrations</span><span class="x">✳</span>
        <!-- duplicate for seamless loop -->
        <span>Développement Web</span><span class="x">✳</span>
        <span>Applications SaaS</span><span class="x">✳</span>
        <span>Automatisation IA</span><span class="x">✳</span>
        <span>Prompt Engineering</span><span class="x">✳</span>
        <span>Design UX/UI</span><span class="x">✳</span>
        <span>APIs &amp; Intégrations</span><span class="x">✳</span>
      </div>
    </div>
  </section>

  <!-- QUOTE -->
  <div class="quote-block">
    <div class="wrap">
      <span class="eyebrow mono">2026 · Sélection de travaux</span>
      <h2>Le code a du sens <em>quand la forme suit la fonction</em></h2>
    </div>
  </div>

  <!-- PROJECTS -->
  <section id="works">
    <div class="wrap">
      <div class="section-head">
        <span class="eyebrow">Projets sélectionnés</span>
        <h2>Ce que je construis</h2>
      </div>
      <div class="projects-grid">

        <div class="project-card">
          <span class="project-num">01</span>
          <span class="project-tags mono">Next.js · PostgreSQL · IA</span>
          <h3>Plateforme SaaS<br>Marché Africain</h3>
          <p>Système de gestion commerciale adapté aux PME d'Afrique subsaharienne — paiements mobile money, multilingue, offline-first.</p>
          <div class="project-foot"><span class="yr">2025</span><a class="lnk" href="#">Voir le projet →</a></div>
        </div>

        <div class="project-card">
          <span class="project-num">02</span>
          <span class="project-tags mono">N8n · Claude API</span>
          <h3>Pipeline<br>Automatisation IA</h3>
          <p>Workflows N8n connectant Claude AI, Google Sheets et Telegram pour automatiser le reporting et les alertes métier.</p>
          <div class="project-foot"><span class="yr">2025</span><a class="lnk" href="#">Voir le projet →</a></div>
        </div>

        <div class="project-card">
          <span class="project-num">03</span>
          <span class="project-tags mono">React · UX Design</span>
          <h3>Dashboard<br>Analytics</h3>
          <p>Interface de visualisation pour une startup fintech — charts temps réel, exports PDF automatisés.</p>
          <div class="project-foot"><span class="yr">2024</span><a class="lnk" href="#">Voir le projet →</a></div>
        </div>

        <div class="project-card">
          <span class="project-num">04</span>
          <span class="project-tags mono">Flutter · Mobile</span>
          <h3>App Mobile<br>Club Échecs</h3>
          <p>Gestion de tournois et classements ELO automatisés pour le club d'échecs d'Ouagadougou.</p>
          <div class="project-foot"><span class="yr">2024</span><a class="lnk" href="#">Voir le projet →</a></div>
        </div>

      </div>
    </div>
  </section>

  <!-- STACK -->
  <section id="stack">
    <div class="wrap">
      <div class="section-head">
        <span class="eyebrow">Arsenal technique</span>
        <h2>Mon stack</h2>
      </div>
      <div class="stack-grid">
        <div class="stack-col">
          <h4>Frontend</h4>
          <ul>
            <li>Next.js 15</li><li>React.js</li><li>TypeScript</li>
            <li>Tailwind CSS</li><li>Flutter</li>
          </ul>
        </div>
        <div class="stack-col">
          <h4>Backend</h4>
          <ul>
            <li>Node.js / Express</li><li>PostgreSQL</li><li>REST APIs</li>
            <li>Python</li><li>Bash scripting</li>
          </ul>
        </div>
        <div class="stack-col">
          <h4>IA &amp; Automatisation</h4>
          <ul>
            <li>Claude / Anthropic API</li><li>Gemini CLI</li><li>N8n Workflows</li>
            <li>Prompt Engineering</li><li>Antigravity</li>
          </ul>
        </div>
        <div class="stack-col">
          <h4>Outils &amp; Cloud</h4>
          <ul>
            <li>GitHub / Git</li><li>Google Cloud</li><li>Vercel</li>
            <li>Figma</li><li>Claude Code</li>
          </ul>
        </div>
      </div>

      <div class="stats-bar">
        <div class="stat"><div class="num">8+</div><div class="lbl">Projets livrés</div></div>
        <div class="stat"><div class="num">3</div><div class="lbl">Années d'expérience</div></div>
        <div class="stat"><div class="num">∞</div><div class="lbl">Curiosité</div></div>
        <div class="stat"><div class="num">BF</div><div class="lbl">Basé à Ouagadougou</div></div>
      </div>
    </div>
  </section>

  <!-- ABOUT -->
  <section id="about">
    <div class="wrap">
      <div class="section-head">
        <span class="eyebrow">À propos</span>
        <h2>Qui suis-je ?</h2>
      </div>
      <div class="about-grid">
        <div>
          <p>Je suis <strong>CreAItive Studio</strong>, Graphiste designer passionee par la creaion d'image et de montage video basé à <strong>Ouagadougou, Burkina Faso</strong>.</p>
          <p>Je construis des produits numériques qui ont du sens — des applications SaaS pensées pour les réalités africaines, des pipelines IA qui automatisent ce qui est répétitif, et des interfaces qui font une vraie différence.</p>
          <p>Actuellement en licence d'ingénierie, je combine rigueur académique et pratique terrain. Je joue aux échecs, j'apprends le chinois, et je crois que la technologie africaine peut mener le monde.</p>
          <div class="langs">
            <span>🇫🇷 Français</span>
            <span>🇬🇧 English</span>
            <span>🇨🇳 中文 (en cours)</span>
          </div>
        </div>
        <div>
          <div class="about-photo">
            <img src="https://flickwick.pplx.app/avatar.jpg" alt="Photo de Koulidiati Ange Lionel">
          </div>
          <span class="loc-tag">📍 Ouagadougou, Burkina Faso 🇧🇫</span>
        </div>
      </div>
    </div>
  </section>

  <!-- CERTIFICATIONS -->
  <section id="certifications">
    <div class="wrap">
      <div class="section-head">
        <span class="eyebrow">Certifications</span>
        <h2>Ce que j'ai validé</h2>
      </div>
      <div class="cert-grid">
        <div class="cert-card">
          <div><h4>Ajouter une certification</h4><div class="org">Organisme · Année</div></div>
          <span class="cert-status validated">Validé</span>
        </div>
        <div class="cert-card">
          <div><h4>Ajouter une certification</h4><div class="org">Organisme · Année</div></div>
          <span class="cert-status validated">Validé</span>
        </div>
        <div class="cert-card">
          <div><h4>Ajouter une certification</h4><div class="org">Organisme · Année</div></div>
          <span class="cert-status validated">Validé</span>
        </div>
        <div class="cert-card">
          <div><h4>Ajouter une certification</h4><div class="org">Organisme · Année</div></div>
          <span class="cert-status soon">Bientôt</span>
        </div>
      </div>
      <p class="cert-note">Ces emplacements sont à remplir avec tes vraies certifications. Envoie-les moi et je les intègre immédiatement.</p>
    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact" class="contact">
    <div class="wrap">
      <span class="eyebrow">Contact</span>
      <h2>Un projet<br>en tête ?</h2>
      <p>Disponible pour missions freelance, collaborations et opportunités full-time.</p>
      <a class="btn btn-accent" href="mailto:contact@Koulidiatiangelioneil.dev">✉ contact@Koulidiatiangelioneil.dev</a>
      <div class="contact-links">
        <a href="https://github.com" target="_blank" rel="noopener">GitHub →</a>
        <a href="https://linkedin.com" target="_blank" rel="noopener">LinkedIn →</a>
      </div>
    </div>
  </section>
</main>

<footer>
  <div class="wrap" style="display:flex; justify-content:space-between; width:100%; flex-wrap:wrap; gap:10px;">
    <span>AG © 2026 Koulidiati Ange Lionel</span>
    <span>Ouagadougou, BF · Full-Stack &amp; IA</span>
  </div>
</footer>

</body>
</html>
