<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>AmpX Ingénierie | Bureau d'Étude Thermique & Énergétique</title>
<meta name="description" content="Bureau d'étude technique spécialisé en CVC, plomberie, DPE, solaire photovoltaïque et IRVE. Optimisez la performance énergétique de vos bâtiments.">
<meta name="keywords" content="bureau d'étude thermique, CVC, étude énergétique, DPE, solaire, photovoltaïque, IRVE, bornes électriques, performance énergétique, chauffage ventilation climatisation">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Sans:ital,wght@0,300;0,400;0,500;1,300&display=swap" rel="stylesheet">
<style>
  :root {
    --navy: #0a0a0a;
    --navy-mid: #111111;
    --navy-light: #1a1a1a;
    --blue: #222222;
    --blue-bright: #333333;
    --green: #22c55e;
    --green-dark: #16a34a;
    --green-light: #4ade80;
    --white: #ffffff;
    --off-white: #f0f4f8;
    --gray-100: #e8edf3;
    --gray-200: #c8d4e0;
    --gray-400: #7a90a8;
    --gray-600: #4a607a;
    --text: #0a0a0a;
    --accent: #22c55e;
    --radius: 12px;
    --radius-lg: 20px;
    --shadow: 0 4px 24px rgba(10,22,40,0.12);
    --shadow-lg: 0 16px 48px rgba(10,22,40,0.18);
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--white);
    color: var(--text);
    overflow-x: hidden;
  }

  h1,h2,h3,h4,h5 { font-family: 'Syne', sans-serif; }

  /* ── NAV ── */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 1000;
    padding: 0 5%;
    background: rgba(10,22,40,0.96);
    backdrop-filter: blur(16px);
    border-bottom: 1px solid rgba(255,255,255,0.06);
    transition: all 0.3s;
  }

  .nav-inner {
    max-width: 1200px; margin: 0 auto;
    display: flex; align-items: center; justify-content: space-between;
    height: 72px;
  }

  .nav-logo {
    display: flex; align-items: center; gap: 10px;
    text-decoration: none;
    cursor: pointer;
  }

  .nav-logo-icon {
    width: 38px; height: 38px;
    background: linear-gradient(135deg, var(--green), var(--blue-bright));
    border-radius: 8px;
    display: flex; align-items: center; justify-content: center;
  }

  .nav-logo-icon svg { width: 22px; height: 22px; fill: white; }

  .nav-logo-text { color: white; }
  .nav-logo-text strong { font-family: 'Syne', sans-serif; font-size: 0.95rem; font-weight: 800; display: block; line-height: 1; }
  .nav-logo-text span { font-size: 0.7rem; color: var(--gray-200); letter-spacing: 0.08em; text-transform: uppercase; }

  .nav-links { display: flex; align-items: center; gap: 2px; }

  .nav-links a {
    color: rgba(255,255,255,0.75);
    text-decoration: none;
    font-size: 0.88rem;
    font-weight: 400;
    padding: 8px 14px;
    border-radius: 8px;
    transition: all 0.2s;
    cursor: pointer;
    letter-spacing: 0.01em;
  }

  .nav-links a:hover, .nav-links a.active {
    color: white;
    background: rgba(255,255,255,0.1);
  }

  .nav-cta {
    background: var(--green) !important;
    color: var(--navy) !important;
    font-weight: 600 !important;
    padding: 9px 20px !important;
  }

  .nav-cta:hover { background: var(--green-light) !important; }

  .hamburger {
    display: none;
    flex-direction: column; gap: 5px;
    cursor: pointer; padding: 6px;
  }

  .hamburger span {
    display: block; width: 24px; height: 2px;
    background: white; border-radius: 2px;
    transition: all 0.3s;
  }

  /* ── PAGES ── */
  .page { display: none; }
  .page.active { display: block; }

  /* ── HERO ── */
  .hero {
    min-height: 100vh;
    background: var(--navy);
    position: relative;
    display: flex; align-items: center;
    overflow: hidden;
    padding-top: 72px;
  }

  .hero-bg {
    position: absolute; inset: 0;
    background:
      radial-gradient(ellipse 60% 60% at 70% 50%, rgba(30,77,140,0.4) 0%, transparent 70%),
      radial-gradient(ellipse 40% 50% at 10% 80%, rgba(34,197,94,0.08) 0%, transparent 60%);
  }

  .hero-grid {
    position: absolute; inset: 0;
    background-image:
      linear-gradient(rgba(255,255,255,0.025) 1px, transparent 1px),
      linear-gradient(90deg, rgba(255,255,255,0.025) 1px, transparent 1px);
    background-size: 60px 60px;
  }

  .hero-content {
    position: relative; z-index: 2;
    max-width: 1200px; margin: 0 auto;
    padding: 80px 5%;
    display: grid; grid-template-columns: 1fr 1fr;
    gap: 60px; align-items: center;
  }

  .hero-badge {
    display: inline-flex; align-items: center; gap: 8px;
    background: rgba(34,197,94,0.12);
    border: 1px solid rgba(34,197,94,0.3);
    color: var(--green-light);
    font-size: 0.78rem; font-weight: 500;
    padding: 6px 14px; border-radius: 100px;
    margin-bottom: 24px;
    letter-spacing: 0.05em; text-transform: uppercase;
  }

  .hero-badge::before {
    content: ''; width: 6px; height: 6px;
    background: var(--green);
    border-radius: 50%;
    animation: pulse 2s infinite;
  }

  @keyframes pulse {
    0%,100% { opacity: 1; transform: scale(1); }
    50% { opacity: 0.5; transform: scale(1.5); }
  }

  .hero h1 {
    font-size: clamp(2rem, 4vw, 3.2rem);
    font-weight: 800;
    line-height: 1.1;
    color: white;
    margin-bottom: 20px;
  }

  .hero h1 .highlight {
    background: linear-gradient(135deg, var(--green-light), var(--green));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .hero-sub {
    font-size: 1.05rem;
    color: rgba(255,255,255,0.65);
    line-height: 1.7;
    margin-bottom: 36px;
    font-weight: 300;
  }

  .hero-actions { display: flex; gap: 14px; flex-wrap: wrap; }

  .btn-primary {
    display: inline-flex; align-items: center; gap: 8px;
    background: var(--green);
    color: var(--navy);
    font-family: 'Syne', sans-serif;
    font-weight: 700; font-size: 0.95rem;
    padding: 14px 28px;
    border-radius: var(--radius);
    text-decoration: none;
    border: none; cursor: pointer;
    transition: all 0.25s;
    white-space: nowrap;
  }

  .btn-primary:hover {
    background: var(--green-light);
    transform: translateY(-2px);
    box-shadow: 0 8px 28px rgba(34,197,94,0.35);
  }

  .btn-secondary {
    display: inline-flex; align-items: center; gap: 8px;
    background: transparent;
    color: white;
    font-family: 'Syne', sans-serif;
    font-weight: 600; font-size: 0.95rem;
    padding: 14px 28px;
    border-radius: var(--radius);
    border: 1px solid rgba(255,255,255,0.25);
    cursor: pointer;
    transition: all 0.25s;
    text-decoration: none;
  }

  .btn-secondary:hover {
    background: rgba(255,255,255,0.08);
    border-color: rgba(255,255,255,0.5);
  }

  .hero-stats {
    display: flex; gap: 28px; flex-wrap: wrap;
    margin-top: 48px;
    padding-top: 36px;
    border-top: 1px solid rgba(255,255,255,0.1);
  }

  .stat { }
  .stat-num {
    font-family: 'Syne', sans-serif;
    font-size: 1.8rem; font-weight: 800;
    color: white; line-height: 1;
  }
  .stat-num span { color: var(--green); }
  .stat-label { font-size: 0.78rem; color: rgba(255,255,255,0.5); margin-top: 2px; text-transform: uppercase; letter-spacing: 0.05em; }

  .hero-visual {
    position: relative;
  }

  .hero-card-stack {
    position: relative;
    display: grid;
    gap: 16px;
  }

  .hero-card {
    background: rgba(255,255,255,0.05);
    border: 1px solid rgba(255,255,255,0.1);
    border-radius: var(--radius-lg);
    padding: 24px 28px;
    backdrop-filter: blur(8px);
    transition: transform 0.3s;
  }

  .hero-card:hover { transform: translateY(-4px); }

  .hero-card-icon {
    width: 44px; height: 44px;
    background: rgba(34,197,94,0.15);
    border-radius: 10px;
    display: flex; align-items: center; justify-content: center;
    margin-bottom: 14px;
    font-size: 1.4rem;
  }

  .hero-card h4 { color: white; font-size: 1rem; font-weight: 700; margin-bottom: 4px; }
  .hero-card p { color: rgba(255,255,255,0.5); font-size: 0.82rem; line-height: 1.5; }

  .hero-card-row { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; }

  /* ── SECTIONS ── */
  section { padding: 100px 5%; }
  .container { max-width: 1200px; margin: 0 auto; }

  .section-label {
    display: inline-block;
    color: var(--green-dark);
    font-size: 0.75rem; font-weight: 600;
    text-transform: uppercase; letter-spacing: 0.12em;
    margin-bottom: 12px;
  }

  .section-title {
    font-size: clamp(1.8rem, 3vw, 2.6rem);
    font-weight: 800; line-height: 1.15;
    color: var(--navy); margin-bottom: 16px;
  }

  .section-sub {
    font-size: 1rem; color: var(--gray-600);
    line-height: 1.7; font-weight: 300;
    max-width: 560px;
  }

  .section-header { margin-bottom: 60px; }
  .section-header.centered { text-align: center; }
  .section-header.centered .section-sub { margin: 0 auto; }

  /* ── SERVICES GRID ── */
  .services-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 24px;
  }

  .service-card {
    background: white;
    border: 1px solid var(--gray-100);
    border-radius: var(--radius-lg);
    padding: 36px;
    transition: all 0.3s;
    cursor: pointer;
    position: relative;
    overflow: hidden;
  }

  .service-card::before {
    content: '';
    position: absolute; top: 0; left: 0; right: 0;
    height: 3px;
    background: linear-gradient(90deg, var(--green), var(--blue-bright));
    transform: scaleX(0); transform-origin: left;
    transition: transform 0.3s;
  }

  .service-card:hover {
    border-color: transparent;
    box-shadow: var(--shadow-lg);
    transform: translateY(-6px);
  }

  .service-card:hover::before { transform: scaleX(1); }

  .service-icon {
    width: 56px; height: 56px;
    border-radius: 14px;
    display: flex; align-items: center; justify-content: center;
    font-size: 1.7rem;
    margin-bottom: 22px;
  }

  .service-icon.blue { background: rgba(30,77,140,0.08); }
  .service-icon.green { background: rgba(34,197,94,0.1); }
  .service-icon.teal { background: rgba(20,184,166,0.1); }
  .service-icon.orange { background: rgba(249,115,22,0.1); }
  .service-icon.purple { background: rgba(139,92,246,0.1); }

  .service-card h3 { font-size: 1.15rem; font-weight: 700; color: var(--navy); margin-bottom: 12px; }
  .service-card p { font-size: 0.88rem; color: var(--gray-600); line-height: 1.7; }

  .service-link {
    display: inline-flex; align-items: center; gap: 6px;
    margin-top: 20px;
    color: var(--blue);
    font-size: 0.85rem; font-weight: 600;
    text-decoration: none;
    transition: gap 0.2s;
  }

  .service-link:hover { gap: 10px; }

  /* ── ADVANTAGES ── */
  .advantages-section {
    background: var(--navy);
    color: white;
  }

  .advantages-grid {
    display: grid; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
    gap: 32px;
  }

  .adv-card {
    padding: 36px 28px;
    border-radius: var(--radius-lg);
    background: rgba(255,255,255,0.04);
    border: 1px solid rgba(255,255,255,0.08);
    transition: all 0.3s;
  }

  .adv-card:hover {
    background: rgba(255,255,255,0.08);
    border-color: rgba(34,197,94,0.3);
  }

  .adv-icon { font-size: 2rem; margin-bottom: 18px; }
  .adv-card h4 { font-size: 1.05rem; font-weight: 700; margin-bottom: 10px; }
  .adv-card p { font-size: 0.87rem; color: rgba(255,255,255,0.55); line-height: 1.7; }

  /* ── ABOUT ── */
  .about-grid {
    display: grid; grid-template-columns: 1fr 1fr;
    gap: 80px; align-items: center;
  }

  .about-visual {
    position: relative;
  }

  .about-img-box {
    background: linear-gradient(135deg, var(--navy-mid), var(--blue));
    border-radius: var(--radius-lg);
    aspect-ratio: 4/3;
    display: flex; align-items: center; justify-content: center;
    font-size: 5rem;
    position: relative;
    overflow: hidden;
  }

  .about-img-box::after {
    content: '';
    position: absolute; inset: 0;
    background:
      radial-gradient(circle at 30% 70%, rgba(34,197,94,0.2), transparent 50%),
      radial-gradient(circle at 80% 20%, rgba(30,77,140,0.3), transparent 50%);
  }

  .about-badge {
    position: absolute; bottom: -20px; right: -20px;
    background: white;
    border-radius: var(--radius);
    padding: 18px 22px;
    box-shadow: var(--shadow-lg);
    text-align: center;
  }

  .about-badge-num {
    font-family: 'Syne', sans-serif;
    font-size: 2rem; font-weight: 800;
    color: var(--navy); line-height: 1;
  }

  .about-badge-num span { color: var(--green-dark); }
  .about-badge-label { font-size: 0.72rem; color: var(--gray-400); text-transform: uppercase; letter-spacing: 0.06em; }

  .values-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin-top: 36px; }

  .value-item {
    display: flex; align-items: flex-start; gap: 12px;
    padding: 16px;
    background: var(--off-white);
    border-radius: var(--radius);
  }

  .value-item-icon {
    width: 36px; height: 36px; flex-shrink: 0;
    background: var(--navy);
    border-radius: 8px;
    display: flex; align-items: center; justify-content: center;
    font-size: 1rem;
  }

  .value-item h5 { font-size: 0.88rem; font-weight: 700; color: var(--navy); margin-bottom: 2px; }
  .value-item p { font-size: 0.78rem; color: var(--gray-600); line-height: 1.5; }

  /* ── PROJECTS ── */
  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(340px, 1fr));
    gap: 28px;
  }

  .project-card {
    border-radius: var(--radius-lg);
    overflow: hidden;
    background: white;
    border: 1px solid var(--gray-100);
    transition: all 0.3s;
  }

  .project-card:hover {
    transform: translateY(-6px);
    box-shadow: var(--shadow-lg);
  }

  .project-img {
    height: 200px;
    display: flex; align-items: center; justify-content: center;
    font-size: 3.5rem;
    position: relative;
    overflow: hidden;
  }

  .project-img::before {
    content: '';
    position: absolute; inset: 0;
    opacity: 0.9;
  }

  .project-img-1::before { background: linear-gradient(135deg, #111111, #222222); }
  .project-img-2::before { background: linear-gradient(135deg, #064e3b, #16a34a); }
  .project-img-3::before { background: linear-gradient(135deg, #111111, #2a2a2a); }
  .project-img-4::before { background: linear-gradient(135deg, #7c2d12, #c2410c); }
  .project-img-5::before { background: linear-gradient(135deg, #111111, #22c55e 120%); }
  .project-img-6::before { background: linear-gradient(135deg, #0a0a0a, #0ea5e9); }

  .project-img span { position: relative; z-index: 1; }

  .project-tag {
    position: absolute; top: 14px; left: 14px; z-index: 2;
    background: rgba(255,255,255,0.18);
    backdrop-filter: blur(8px);
    color: white; font-size: 0.72rem; font-weight: 600;
    padding: 4px 12px; border-radius: 100px;
    text-transform: uppercase; letter-spacing: 0.06em;
    border: 1px solid rgba(255,255,255,0.25);
  }

  .project-body { padding: 28px; }
  .project-body h3 { font-size: 1.05rem; font-weight: 700; color: var(--navy); margin-bottom: 8px; }
  .project-body p { font-size: 0.85rem; color: var(--gray-600); line-height: 1.65; }

  .project-meta {
    display: flex; gap: 16px; margin-top: 16px;
    padding-top: 16px; border-top: 1px solid var(--gray-100);
  }

  .meta-item { display: flex; align-items: center; gap: 5px; font-size: 0.78rem; color: var(--gray-400); }

  /* ── CONTACT ── */
  .contact-grid {
    display: grid; grid-template-columns: 1fr 1.6fr;
    gap: 60px;
  }

  .contact-info h3 { font-size: 1.5rem; font-weight: 800; color: var(--navy); margin-bottom: 8px; }
  .contact-info > p { font-size: 0.9rem; color: var(--gray-600); line-height: 1.7; margin-bottom: 36px; }

  .contact-details { display: flex; flex-direction: column; gap: 20px; }

  .contact-detail {
    display: flex; align-items: flex-start; gap: 14px;
  }

  .contact-detail-icon {
    width: 42px; height: 42px; flex-shrink: 0;
    background: var(--navy);
    border-radius: 10px;
    display: flex; align-items: center; justify-content: center;
    font-size: 1.1rem;
  }

  .contact-detail strong { display: block; font-size: 0.78rem; color: var(--gray-400); text-transform: uppercase; letter-spacing: 0.06em; margin-bottom: 2px; }
  .contact-detail span { font-size: 0.9rem; color: var(--navy); font-weight: 500; }

  .map-placeholder {
    margin-top: 28px;
    height: 180px;
    background: linear-gradient(135deg, var(--navy-mid), var(--navy-light));
    border-radius: var(--radius);
    display: flex; align-items: center; justify-content: center;
    font-size: 2rem;
    position: relative;
    overflow: hidden;
  }

  .map-placeholder::after {
    content: 'Carte Google Maps';
    position: absolute; bottom: 12px; right: 14px;
    font-size: 0.72rem; color: rgba(255,255,255,0.4);
    font-family: 'DM Sans', sans-serif;
  }

  /* ── FORM ── */
  .contact-form {
    background: white;
    border: 1px solid var(--gray-100);
    border-radius: var(--radius-lg);
    padding: 44px;
    box-shadow: var(--shadow);
  }

  .contact-form h3 { font-size: 1.3rem; font-weight: 800; color: var(--navy); margin-bottom: 6px; }
  .contact-form > p { font-size: 0.85rem; color: var(--gray-600); margin-bottom: 28px; }

  .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin-bottom: 16px; }

  .form-group { margin-bottom: 16px; }

  .form-group label {
    display: block;
    font-size: 0.8rem; font-weight: 600;
    color: var(--navy); margin-bottom: 6px;
    text-transform: uppercase; letter-spacing: 0.04em;
  }

  .form-group input, .form-group select, .form-group textarea {
    width: 100%;
    border: 1.5px solid var(--gray-100);
    border-radius: var(--radius);
    padding: 12px 16px;
    font-family: 'DM Sans', sans-serif;
    font-size: 0.9rem;
    color: var(--navy);
    background: var(--off-white);
    transition: all 0.2s;
    outline: none;
    resize: vertical;
  }

  .form-group input:focus, .form-group select:focus, .form-group textarea:focus {
    border-color: var(--blue-bright);
    background: white;
    box-shadow: 0 0 0 3px rgba(37,99,192,0.1);
  }

  .form-group textarea { min-height: 120px; }

  .form-submit {
    width: 100%;
    background: var(--navy);
    color: white;
    font-family: 'Syne', sans-serif;
    font-weight: 700; font-size: 0.95rem;
    padding: 14px;
    border: none; border-radius: var(--radius);
    cursor: pointer;
    transition: all 0.25s;
    display: flex; align-items: center; justify-content: center; gap: 8px;
  }

  .form-submit:hover {
    background: var(--blue);
    transform: translateY(-2px);
    box-shadow: 0 8px 24px rgba(10,22,40,0.25);
  }

  .form-success {
    display: none;
    text-align: center;
    padding: 24px;
    background: rgba(34,197,94,0.08);
    border: 1px solid rgba(34,197,94,0.3);
    border-radius: var(--radius);
    margin-top: 16px;
    color: var(--green-dark);
    font-weight: 500;
  }

  /* ── SERVICES PAGE FULL ── */
  .service-full {
    background: white;
    border: 1px solid var(--gray-100);
    border-radius: var(--radius-lg);
    padding: 40px;
    margin-bottom: 24px;
    display: grid; grid-template-columns: auto 1fr auto;
    gap: 28px; align-items: start;
    transition: all 0.3s;
  }

  .service-full:hover {
    box-shadow: var(--shadow);
    border-color: rgba(34,197,94,0.3);
  }

  .service-full-icon {
    width: 64px; height: 64px;
    border-radius: var(--radius);
    display: flex; align-items: center; justify-content: center;
    font-size: 2rem;
    flex-shrink: 0;
  }

  .service-full h3 { font-size: 1.25rem; font-weight: 800; color: var(--navy); margin-bottom: 10px; }
  .service-full p { font-size: 0.9rem; color: var(--gray-600); line-height: 1.7; }

  .service-features { margin-top: 16px; display: flex; flex-wrap: wrap; gap: 8px; }

  .feat-tag {
    background: var(--off-white);
    color: var(--navy);
    font-size: 0.75rem; font-weight: 500;
    padding: 4px 12px; border-radius: 100px;
    border: 1px solid var(--gray-100);
  }

  /* ── FOOTER ── */
  footer {
    background: var(--navy);
    color: white;
    padding: 64px 5% 32px;
  }

  .footer-grid {
    max-width: 1200px; margin: 0 auto;
    display: grid; grid-template-columns: 2fr 1fr 1fr 1fr;
    gap: 48px; margin-bottom: 48px;
  }

  .footer-brand p {
    font-size: 0.87rem; color: rgba(255,255,255,0.5);
    line-height: 1.7; margin-top: 14px; max-width: 280px;
  }

  .footer-col h5 {
    font-size: 0.8rem; font-weight: 700;
    text-transform: uppercase; letter-spacing: 0.1em;
    color: rgba(255,255,255,0.4);
    margin-bottom: 16px;
  }

  .footer-col a {
    display: block;
    color: rgba(255,255,255,0.65);
    font-size: 0.87rem;
    text-decoration: none;
    margin-bottom: 10px;
    cursor: pointer;
    transition: color 0.2s;
  }

  .footer-col a:hover { color: var(--green-light); }

  .footer-bottom {
    max-width: 1200px; margin: 0 auto;
    padding-top: 28px;
    border-top: 1px solid rgba(255,255,255,0.08);
    display: flex; justify-content: space-between; align-items: center;
    flex-wrap: wrap; gap: 12px;
  }

  .footer-bottom p { font-size: 0.78rem; color: rgba(255,255,255,0.35); }

  .certifs { display: flex; gap: 10px; }
  .certif-badge {
    background: rgba(255,255,255,0.06);
    border: 1px solid rgba(255,255,255,0.12);
    color: rgba(255,255,255,0.5);
    font-size: 0.7rem; font-weight: 600;
    padding: 4px 10px; border-radius: 100px;
    text-transform: uppercase; letter-spacing: 0.05em;
  }

  /* ── CTA BAND ── */
  .cta-band {
    background: linear-gradient(135deg, var(--green-dark), var(--green));
    padding: 80px 5%;
    text-align: center;
  }

  .cta-band h2 {
    font-size: clamp(1.6rem, 3vw, 2.4rem);
    font-weight: 800;
    color: var(--navy);
    margin-bottom: 12px;
  }

  .cta-band p { font-size: 1rem; color: rgba(10,22,40,0.7); margin-bottom: 32px; }

  .btn-dark {
    display: inline-flex; align-items: center; gap: 8px;
    background: var(--navy);
    color: white;
    font-family: 'Syne', sans-serif;
    font-weight: 700; font-size: 0.95rem;
    padding: 14px 32px;
    border-radius: var(--radius);
    border: none; cursor: pointer;
    transition: all 0.25s;
    text-decoration: none;
  }

  .btn-dark:hover {
    background: var(--navy-light);
    transform: translateY(-2px);
    box-shadow: 0 10px 30px rgba(10,22,40,0.3);
  }

  /* ── DIVIDER ── */
  .section-divider {
    height: 1px;
    background: var(--gray-100);
    max-width: 1200px; margin: 0 auto;
  }

  /* ── ANIM ── */
  .fade-up {
    opacity: 0;
    transform: translateY(30px);
    transition: opacity 0.7s ease, transform 0.7s ease;
  }

  .fade-up.visible {
    opacity: 1;
    transform: translateY(0);
  }

  /* ── RESPONSIVE ── */
  @media (max-width: 900px) {
    .hero-content { grid-template-columns: 1fr; gap: 48px; }
    .about-grid { grid-template-columns: 1fr; gap: 40px; }
    .contact-grid { grid-template-columns: 1fr; gap: 40px; }
    .footer-grid { grid-template-columns: 1fr 1fr; gap: 36px; }
    .service-full { grid-template-columns: auto 1fr; }
    .service-full .btn-primary { grid-column: 2; }
  }

  @media (max-width: 640px) {
    section { padding: 72px 5%; }
    .nav-links { display: none; position: fixed; top: 72px; left: 0; right: 0; bottom: 0; background: rgba(10,22,40,0.98); flex-direction: column; align-items: stretch; padding: 24px; gap: 8px; overflow-y: auto; }
    .nav-links.open { display: flex; }
    .nav-links a { padding: 14px 16px; font-size: 1rem; }
    .hamburger { display: flex; }
    .hero-card-row { grid-template-columns: 1fr; }
    .footer-grid { grid-template-columns: 1fr; }
    .form-row { grid-template-columns: 1fr; }
    .service-full { grid-template-columns: 1fr; }
    .values-grid { grid-template-columns: 1fr; }
    .hero-stats { gap: 20px; }
    .contact-form { padding: 28px; }
  }
</style>
</head>
<body>

<!-- ═══════ NAV ═══════ -->
<nav id="navbar">
  <div class="nav-inner">
    <div class="nav-logo" onclick="showPage('accueil')">
      
      <div class="nav-logo-text">
        <strong>AmpX Ingénierie</strong>
        
      </div>
    </div>
    <div class="nav-links" id="navLinks">
      <a onclick="showPage('accueil');closeMenu()" class="active" id="nav-accueil">Accueil</a>
      <a onclick="showPage('apropos');closeMenu()" id="nav-apropos">À Propos</a>
      <a onclick="showPage('services');closeMenu()" id="nav-services">Services</a>
      <a onclick="showPage('projets');closeMenu()" id="nav-projets">Réalisations</a>
      <a onclick="showPage('contact');closeMenu()" id="nav-contact">Contact</a>
      <a onclick="showPage('contact');closeMenu()" class="nav-cta">Demander un devis →</a>
    </div>
    <div class="hamburger" id="hamburger" onclick="toggleMenu()">
      <span></span><span></span><span></span>
    </div>
  </div>
</nav>

<!-- ═══════ PAGE : ACCUEIL ═══════ -->
<div class="page active" id="page-accueil">

  <!-- Hero -->
  <section class="hero">
    <div class="hero-bg"></div>
    <div class="hero-grid"></div>
    <div class="hero-content container">
      <div class="hero-left">
        <div class="hero-badge">Bureau d'Études Techniques</div>
        <h1>Optimisez la <span class="highlight">performance énergétique</span> de vos bâtiments</h1>
        <p class="hero-sub">
          Conception, étude et réalisation de projets techniques et énergétiques pour particuliers, entreprises et collectivités. CVC, solaire, DPE, IRVE — une expertise complète.
        </p>
        <div class="hero-actions">
          <button class="btn-primary" onclick="showPage('contact')">Demander un devis →</button>
          <button class="btn-secondary" onclick="showPage('services')">Nos services</button>
        </div>
        <div class="hero-stats">
          <div class="stat">
            <div class="stat-num">250<span>+</span></div>
            <div class="stat-label">Projets réalisés</div>
          </div>
          <div class="stat">
            <div class="stat-num">15<span>ans</span></div>
            <div class="stat-label">D'expérience</div>
          </div>
          <div class="stat">
            <div class="stat-num">98<span>%</span></div>
            <div class="stat-label">Clients satisfaits</div>
          </div>
        </div>
      </div>
      <div class="hero-visual">
        <div class="hero-card-stack">
          <div class="hero-card">
            <div class="hero-card-icon">⚡</div>
            <h4>Audit Énergétique & DPE</h4>
            <p>Diagnostic certifié, recommandations d'optimisation et accompagnement réglementaire</p>
          </div>
          <div class="hero-card-row">
            <div class="hero-card">
              <div class="hero-card-icon">☀️</div>
              <h4>Solaire PV</h4>
              <p>Étude & installation photovoltaïque clé en main</p>
            </div>
            <div class="hero-card">
              <div class="hero-card-icon">🔌</div>
              <h4>IRVE</h4>
              <p>Bornes de recharge pour flottes et parkings</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Services rapides -->
  <section style="background: var(--off-white);">
    <div class="container">
      <div class="section-header centered">
        <span class="section-label">Expertise complète</span>
        <h2 class="section-title">Nos domaines d'intervention</h2>
        <p class="section-sub">Une approche globale intégrant tous les lots techniques pour des solutions performantes et durables</p>
      </div>
      <div class="services-grid">
        <div class="service-card fade-up">
          <div class="service-icon blue">🌡️</div>
          <h3>Ingénierie CVC</h3>
          <p>Conception et dimensionnement de systèmes de chauffage, ventilation et climatisation adaptés à vos bâtiments tertiaires et résidentiels.</p>
          <a class="service-link" onclick="showPage('services')">En savoir plus →</a>
        </div>
        <div class="service-card fade-up" style="transition-delay:0.1s">
          <div class="service-icon teal">💧</div>
          <h3>Plomberie & Hydraulique</h3>
          <p>Études et réalisation de réseaux hydrauliques, sanitaires et d'eau chaude sanitaire. Dimensionnement conforme aux normes DTU.</p>
          <a class="service-link" onclick="showPage('services')">En savoir plus →</a>
        </div>
        <div class="service-card fade-up" style="transition-delay:0.2s">
          <div class="service-icon green">☀️</div>
          <h3>Solaire Photovoltaïque</h3>
          <p>Étude de faisabilité, dimensionnement et suivi d'installation photovoltaïque. Optimisation du retour sur investissement.</p>
          <a class="service-link" onclick="showPage('services')">En savoir plus →</a>
        </div>
        <div class="service-card fade-up" style="transition-delay:0.3s">
          <div class="service-icon orange">📊</div>
          <h3>DPE & Audit Énergétique</h3>
          <p>Diagnostic de Performance Énergétique réglementaire et audit énergétique pour valoriser et optimiser votre patrimoine immobilier.</p>
          <a class="service-link" onclick="showPage('services')">En savoir plus →</a>
        </div>
        <div class="service-card fade-up" style="transition-delay:0.4s">
          <div class="service-icon purple">🔌</div>
          <h3>IRVE — Bornes Électriques</h3>
          <p>Étude et installation de bornes de recharge pour véhicules électriques (IRVE). Solutions pour particuliers, copropriétés et entreprises.</p>
          <a class="service-link" onclick="showPage('services')">En savoir plus →</a>
        </div>
        <div class="service-card fade-up" style="transition-delay:0.5s; background: var(--navy); border-color: var(--navy);">
          <div class="service-icon" style="background: rgba(255,255,255,0.1);">🏗️</div>
          <h3 style="color: white;">Approche globale</h3>
          <p style="color: rgba(255,255,255,0.6);">Tous lots techniques couverts, de la conception à la réception. Un interlocuteur unique pour l'ensemble de vos projets.</p>
          <a class="service-link" style="color: var(--green-light);" onclick="showPage('contact')">Nous contacter →</a>
        </div>
      </div>
    </div>
  </section>

  <!-- Avantages -->
  <section class="advantages-section">
    <div class="container">
      <div class="section-header centered">
        <span class="section-label" style="color: var(--green-light);">Pourquoi nous choisir</span>
        <h2 class="section-title" style="color: white;">L'expertise au service de votre projet</h2>
      </div>
      <div class="advantages-grid">
        <div class="adv-card">
          <div class="adv-icon">🎯</div>
          <h4>Expertise Certifiée</h4>
          <p>Ingénieurs qualifiés RGE, experts en thermique du bâtiment avec une maîtrise complète des réglementations RE 2020, RT 2012 et DTU.</p>
        </div>
        <div class="adv-card">
          <div class="adv-icon">🔄</div>
          <h4>Accompagnement Complet</h4>
          <p>De l'étude de faisabilité à la réception des travaux, nous vous accompagnons à chaque étape avec un suivi personnalisé.</p>
        </div>
        <div class="adv-card">
          <div class="adv-icon">⚡</div>
          <h4>Réactivité & Fiabilité</h4>
          <p>Délais respectés, rapports livrés dans les temps, disponibilité permanente pour répondre à vos questions techniques.</p>
        </div>
        <div class="adv-card">
          <div class="adv-icon">💡</div>
          <h4>Innovation Technique</h4>
          <p>Outils de simulation énergétique dernière génération, BIM, et veille réglementaire continue pour des solutions à la pointe.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- CTA -->
  <div class="cta-band">
    <div class="container">
      <h2>Prêt à optimiser vos installations ?</h2>
      <p>Obtenez une première analyse gratuite de votre projet en moins de 48h</p>
      <button class="btn-dark" onclick="showPage('contact')">Demander un devis gratuit →</button>
    </div>
  </div>

</div>

<!-- ═══════ PAGE : À PROPOS ═══════ -->
<div class="page" id="page-apropos">

  <section style="padding-top: 140px; background: var(--off-white);">
    <div class="container">
      <div class="about-grid">
        <div class="about-visual">
          <div class="about-img-box">
            <span style="position:relative;z-index:1;font-size:5rem;">🏗️</span>
          </div>
          <div class="about-badge">
            <div class="about-badge-num">15<span>+</span></div>
            <div class="about-badge-label">années d'exp.</div>
          </div>
        </div>
        <div>
          <span class="section-label">À propos de nous</span>
          <h2 class="section-title">Bureau d'études spécialisé en ingénierie du bâtiment</h2>
          <p style="font-size:0.95rem;color:var(--gray-600);line-height:1.8;margin-bottom:16px;">
            Fondé par des ingénieurs passionnés par la transition énergétique, <strong>AmpX Ingénierie</strong> est un bureau d'études techniques indépendant spécialisé dans la performance énergétique des bâtiments.
          </p>
          <p style="font-size:0.95rem;color:var(--gray-600);line-height:1.8;margin-bottom:28px;">
            Nous accompagnons particuliers, promoteurs, bailleurs sociaux et collectivités dans leurs projets de construction neuve, rénovation et optimisation énergétique. Notre approche pluridisciplinaire intègre l'ensemble des lots techniques : CVC, plomberie, électricité, solaire, IRVE.
          </p>
          <div class="values-grid">
            <div class="value-item">
              <div class="value-item-icon">🎯</div>
              <div>
                <h5>Excellence technique</h5>
                <p>Ingénieurs certifiés et formation continue</p>
              </div>
            </div>
            <div class="value-item">
              <div class="value-item-icon">🌿</div>
              <div>
                <h5>Engagement durable</h5>
                <p>Performance énergétique et bas carbone</p>
              </div>
            </div>
            <div class="value-item">
              <div class="value-item-icon">🤝</div>
              <div>
                <h5>Relation client</h5>
                <p>Proximité, écoute et transparence</p>
              </div>
            </div>
            <div class="value-item">
              <div class="value-item-icon">🔬</div>
              <div>
                <h5>Innovation</h5>
                <p>BIM, simulation dynamique, outils IA</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section>
    <div class="container">
      <div class="section-header centered">
        <span class="section-label">Nos certifications</span>
        <h2 class="section-title">Qualifications & Agréments</h2>
        <p class="section-sub">Des certifications reconnues qui garantissent la qualité et la conformité de nos prestations</p>
      </div>
      <div class="advantages-grid" style="--advantages-cols: 3;">
        <div class="adv-card" style="background: var(--off-white); border-color: var(--gray-100);">
          <div class="adv-icon">🏅</div>
          <h4 style="color: var(--navy);">RGE — Reconnu Garant de l'Environnement</h4>
          <p style="color: var(--gray-600);">Qualification indispensable pour l'éligibilité aux aides publiques (MaPrimeRénov', CEE).</p>
        </div>
        <div class="adv-card" style="background: var(--off-white); border-color: var(--gray-100);">
          <div class="adv-icon">📋</div>
          <h4 style="color: var(--navy);">Diagnostiqueur DPE Certifié</h4>
          <p style="color: var(--gray-600);">Certification COFRAC pour la réalisation de Diagnostics de Performance Énergétique opposables.</p>
        </div>
        <div class="adv-card" style="background: var(--off-white); border-color: var(--gray-100);">
          <div class="adv-icon">⚡</div>
          <h4 style="color: var(--navy);">Qualif. IRVE — QUALIFELEC</h4>
          <p style="color: var(--gray-600);">Qualification reconnue pour l'installation de bornes de recharge pour véhicules électriques.</p>
        </div>
      </div>
    </div>
  </section>

  <div class="cta-band">
    <div class="container">
      <h2>Discutons de votre projet</h2>
      <p>Chaque projet est unique. Contactez-nous pour une première consultation gratuite.</p>
      <button class="btn-dark" onclick="showPage('contact')">Prendre contact →</button>
    </div>
  </div>
</div>

<!-- ═══════ PAGE : SERVICES ═══════ -->
<div class="page" id="page-services">
  <section style="padding-top: 140px; background: var(--off-white);">
    <div class="container">
      <div class="section-header">
        <span class="section-label">Ce que nous faisons</span>
        <h2 class="section-title">Nos prestations techniques</h2>
        <p class="section-sub">Des études rigoureuses et des installations conformes aux réglementations en vigueur</p>
      </div>

      <div class="service-full">
        <div class="service-full-icon blue" style="background:rgba(30,77,140,0.1);">🌡️</div>
        <div>
          <h3>Ingénierie CVC — Chauffage, Ventilation, Climatisation</h3>
          <p>Conception et dimensionnement de systèmes CVC pour tout type de bâtiment : logements collectifs, bureaux, établissements recevant du public, industrie. Nous réalisons les études thermiques réglementaires (RE 2020, RT 2012), le dimensionnement des émetteurs et générateurs, les schémas de principe hydrauliques et les dossiers de consultation des entreprises.</p>
          <div class="service-features">
            <span class="feat-tag">Dimensionnement pompe à chaleur</span>
            <span class="feat-tag">Plan de réseaux aérauliques</span>
            <span class="feat-tag">CTA & VMC double flux</span>
            <span class="feat-tag">Plancher chauffant</span>
            <span class="feat-tag">Étude thermique RE 2020</span>
            <span class="feat-tag">Climatisation réversible</span>
          </div>
        </div>
        <button class="btn-primary" onclick="showPage('contact')" style="white-space:nowrap">Devis gratuit</button>
      </div>

      <div class="service-full">
        <div class="service-full-icon" style="background:rgba(20,184,166,0.1);">💧</div>
        <div>
          <h3>Plomberie & Réseaux Hydrauliques</h3>
          <p>Études et conception de réseaux hydrauliques sanitaires, eau froide/chaude, eaux usées et pluviales. Dimensionnement selon les DTU en vigueur. Nous intervenons en neuf comme en rénovation, sur des projets résidentiels, tertiaires et industriels.</p>
          <div class="service-features">
            <span class="feat-tag">Réseau ECS/EFS</span>
            <span class="feat-tag">Bilan hydraulique</span>
            <span class="feat-tag">Anti-légionellose</span>
            <span class="feat-tag">Gestion eaux pluviales</span>
            <span class="feat-tag">DTU 60.1 / 60.11</span>
            <span class="feat-tag">Plans d'exécution</span>
          </div>
        </div>
        <button class="btn-primary" onclick="showPage('contact')" style="white-space:nowrap">Devis gratuit</button>
      </div>

      <div class="service-full">
        <div class="service-full-icon" style="background:rgba(34,197,94,0.1);">☀️</div>
        <div>
          <h3>Études & Installations Solaires Photovoltaïques</h3>
          <p>De l'étude d'ensoleillement à la mise en service, nous pilotons intégralement vos projets photovoltaïques. Dimensionnement des panneaux, onduleurs, systèmes de stockage, raccordement réseau. Accompagnement pour les démarches administratives (permis de construire, déclaration Enedis).</p>
          <div class="service-features">
            <span class="feat-tag">Étude de faisabilité</span>
            <span class="feat-tag">Dimensionnement PV</span>
            <span class="feat-tag">Autoconsommation</span>
            <span class="feat-tag">Stockage batterie</span>
            <span class="feat-tag">Démarches Enedis</span>
            <span class="feat-tag">Suivi de chantier</span>
          </div>
        </div>
        <button class="btn-primary" onclick="showPage('contact')" style="white-space:nowrap">Devis gratuit</button>
      </div>

      <div class="service-full">
        <div class="service-full-icon" style="background:rgba(249,115,22,0.1);">📊</div>
        <div>
          <h3>Diagnostic de Performance Énergétique (DPE) & Audit Énergétique</h3>
          <p>Réalisation de DPE opposables pour vente et location, audits énergétiques réglementaires et Plans Pluriannuels de Travaux (PPPT). Nos diagnostiqueurs certifiés vous accompagnent pour valoriser votre patrimoine et identifier les travaux prioritaires selon le décret tertiaire.</p>
          <div class="service-features">
            <span class="feat-tag">DPE méthode 3CL</span>
            <span class="feat-tag">Audit réglementaire</span>
            <span class="feat-tag">PPPT copropriété</span>
            <span class="feat-tag">Décret tertiaire</span>
            <span class="feat-tag">Scénarios de rénovation</span>
            <span class="feat-tag">Aides MaPrimeRénov'</span>
          </div>
        </div>
        <button class="btn-primary" onclick="showPage('contact')" style="white-space:nowrap">Devis gratuit</button>
      </div>

      <div class="service-full">
        <div class="service-full-icon" style="background:rgba(139,92,246,0.1);">🔌</div>
        <div>
          <h3>Installation de Bornes de Recharge Électrique (IRVE)</h3>
          <p>Étude, fourniture et installation de bornes de recharge pour véhicules électriques. Solutions adaptées aux particuliers, copropriétés, parkings et flottes d'entreprise. Nous accompagnons les gestionnaires dans leurs obligations légales (décret IRVE) et le montage des dossiers de subventions.</p>
          <div class="service-features">
            <span class="feat-tag">Étude de charge</span>
            <span class="feat-tag">Bornes AC / DC</span>
            <span class="feat-tag">Copropriétés</span>
            <span class="feat-tag">Flottes entreprises</span>
            <span class="feat-tag">Pilotage intelligent</span>
            <span class="feat-tag">Aide ADVENIR</span>
          </div>
        </div>
        <button class="btn-primary" onclick="showPage('contact')" style="white-space:nowrap">Devis gratuit</button>
      </div>

    </div>
  </section>

  <div class="cta-band">
    <div class="container">
      <h2>Un projet en tête ? Parlons-en.</h2>
      <p>Nous répondons à toute demande de devis dans un délai de 48h ouvrées</p>
      <button class="btn-dark" onclick="showPage('contact')">Démarrer mon projet →</button>
    </div>
  </div>
</div>

<!-- ═══════ PAGE : PROJETS ═══════ -->
<div class="page" id="page-projets">
  <section style="padding-top: 140px; background: var(--off-white);">
    <div class="container">
      <div class="section-header centered">
        <span class="section-label">Réalisations</span>
        <h2 class="section-title">Nos projets récents</h2>
        <p class="section-sub">Un aperçu de nos interventions sur des bâtiments résidentiels, tertiaires et industriels en France</p>
      </div>
      <div class="projects-grid">

        <div class="project-card">
          <div class="project-img project-img-1">
            <span>🏢</span>
            <span class="project-tag">CVC & Thermique</span>
          </div>
          <div class="project-body">
            <h3>Rénovation énergétique — Résidence 120 logements</h3>
            <p>Étude thermique complète et remplacement de la chaufferie collective par des PAC air/eau haute performance. Passage de l'étiquette E à B.</p>
            <div class="project-meta">
              <span class="meta-item">📍 Lyon (69)</span>
              <span class="meta-item">📅 2024</span>
              <span class="meta-item">⚡ -52% énergie</span>
            </div>
          </div>
        </div>

        <div class="project-card">
          <div class="project-img project-img-2">
            <span>☀️</span>
            <span class="project-tag">Photovoltaïque</span>
          </div>
          <div class="project-body">
            <h3>Centrale PV — Site logistique 4 500 m²</h3>
            <p>Dimensionnement et suivi d'une installation solaire en autoconsommation de 320 kWc pour un entrepôt logistique. ROI atteint en 7 ans.</p>
            <div class="project-meta">
              <span class="meta-item">📍 Orléans (45)</span>
              <span class="meta-item">📅 2024</span>
              <span class="meta-item">⚡ 320 kWc</span>
            </div>
          </div>
        </div>

        <div class="project-card">
          <div class="project-img project-img-3">
            <span>📋</span>
            <span class="project-tag">Audit & DPE</span>
          </div>
          <div class="project-body">
            <h3>PPPT & Audit réglementaire — Copropriété 85 lots</h3>
            <p>Réalisation du Plan Pluriannuel de Travaux, DPE collectif et audit énergétique d'une copropriété construite en 1975. Scénarios de rénovation chiffrés.</p>
            <div class="project-meta">
              <span class="meta-item">📍 Paris (75)</span>
              <span class="meta-item">📅 2023</span>
              <span class="meta-item">⚡ 85 lots</span>
            </div>
          </div>
        </div>

        <div class="project-card">
          <div class="project-img project-img-4">
            <span>🔌</span>
            <span class="project-tag">IRVE</span>
          </div>
          <div class="project-body">
            <h3>Infrastructure IRVE — Parking d'entreprise 200 places</h3>
            <p>Étude de charge et déploiement de 48 bornes de recharge AC 22 kW avec pilotage intelligent pour une entreprise du secteur automobile.</p>
            <div class="project-meta">
              <span class="meta-item">📍 Bordeaux (33)</span>
              <span class="meta-item">📅 2024</span>
              <span class="meta-item">⚡ 48 bornes</span>
            </div>
          </div>
        </div>

        <div class="project-card">
          <div class="project-img project-img-5">
            <span>🏗️</span>
            <span class="project-tag">Neuf — RE 2020</span>
          </div>
          <div class="project-body">
            <h3>Immeuble de bureaux — Étude fluides complète</h3>
            <p>Mission de maîtrise d'œuvre fluides (CVC + plomberie + électricité) pour un immeuble de bureaux de 6 000 m² SHON conforme RE 2020.</p>
            <div class="project-meta">
              <span class="meta-item">📍 Nantes (44)</span>
              <span class="meta-item">📅 2023</span>
              <span class="meta-item">⚡ 6 000 m²</span>
            </div>
          </div>
        </div>

        <div class="project-card">
          <div class="project-img project-img-6">
            <span>💧</span>
            <span class="project-tag">Plomberie</span>
          </div>
          <div class="project-body">
            <h3>Réseau ECS sécurisé — EHPAD 180 lits</h3>
            <p>Conception du réseau d'eau chaude sanitaire avec dispositif anti-légionellose, bouclage et production solaire thermique pour un EHPAD.</p>
            <div class="project-meta">
              <span class="meta-item">📍 Toulouse (31)</span>
              <span class="meta-item">📅 2023</span>
              <span class="meta-item">⚡ 180 lits</span>
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>

  <div class="cta-band">
    <div class="container">
      <h2>Votre projet peut être notre prochaine réalisation</h2>
      <p>Quel que soit son envergure, nous étudions chaque demande avec soin</p>
      <button class="btn-dark" onclick="showPage('contact')">Nous contacter →</button>
    </div>
  </div>
</div>

<!-- ═══════ PAGE : CONTACT ═══════ -->
<div class="page" id="page-contact">
  <section style="padding-top: 140px; background: var(--off-white);">
    <div class="container">
      <div class="section-header">
        <span class="section-label">Parlons de votre projet</span>
        <h2 class="section-title">Contactez-nous</h2>
        <p class="section-sub">Réponse sous 48h ouvrées. Devis gratuit et sans engagement.</p>
      </div>

      <div class="contact-grid">
        <!-- Infos -->
        <div class="contact-info">
          <h3>AmpX Ingénierie</h3>
          <p>Bureau d'études techniques spécialisé en performance énergétique du bâtiment. Nos ingénieurs sont à votre disposition pour étudier votre projet.</p>

          <div class="contact-details">
            
            <div class="contact-detail">
              <div class="contact-detail-icon">📞</div>
              <div>
                <strong>Téléphone</strong>
                <span>+33 6 03 30 48 77</span>
              </div>
            </div>
            <div class="contact-detail">
              <div class="contact-detail-icon">✉️</div>
              <div>
                <strong>Email</strong>
                <span>contact@ampx.fr</span>
              </div>
            </div>
            <div class="contact-detail">
              <div class="contact-detail-icon">🕐</div>
              <div>
                <strong>Horaires</strong>
                <span>Lun–Ven : 8h30 – 18h00</span>
              </div>
            </div>
          </div>

          
        </div>

        <!-- Formulaire -->
        <div class="contact-form">
          <h3>Demande de devis</h3>
          <p>Décrivez-nous votre projet, nous vous recontactons rapidement</p>

          <div class="form-row">
            <div class="form-group">
              <label>Prénom & Nom *</label>
              <input type="text" id="f-nom" placeholder="Jean Dupont">
            </div>
            <div class="form-group">
              <label>Email *</label>
              <input type="email" id="f-email" placeholder="jean@email.fr">
            </div>
          </div>
          <div class="form-row">
            <div class="form-group">
              <label>Téléphone</label>
              <input type="tel" id="f-tel" placeholder="+33 6 00 00 00 00">
            </div>
            <div class="form-group">
              <label>Type de projet</label>
              <select id="f-type">
                <option value="">Sélectionnez...</option>
                <option>Ingénierie CVC</option>
                <option>Plomberie & Hydraulique</option>
                <option>Solaire Photovoltaïque</option>
                <option>DPE & Audit Énergétique</option>
                <option>Bornes IRVE</option>
                <option>Mission globale</option>
              </select>
            </div>
          </div>
          <div class="form-group">
            <label>Message *</label>
            <textarea id="f-msg" placeholder="Décrivez votre projet : type de bâtiment, surface, localisation, objectifs..."></textarea>
          </div>
          <button class="form-submit" onclick="submitForm()">
            <span>Envoyer ma demande</span> <span>→</span>
          </button>
          <div class="form-success" id="form-success">
            ✅ Votre demande a bien été envoyée ! Vous recevrez une confirmation par email et nous vous répondrons dans les 48h ouvrées.
          </div>
        </div>
      </div>
    </div>
  </section>
</div>

<!-- ═══════ FOOTER ═══════ -->
<footer>
  <div class="footer-grid">
    <div class="footer-brand">
      <div class="nav-logo" onclick="showPage('accueil')" style="margin-bottom:12px;">
        
        <div class="nav-logo-text">
          <strong>AmpX Ingénierie</strong>
          
        </div>
      </div>
      <p>Bureau d'études techniques spécialisé en ingénierie du bâtiment et performance énergétique. RGE certifié, diagnostiqueur DPE agréé.</p>
      <div class="certifs" style="margin-top:16px;">
        <span class="certif-badge">RGE</span>
        <span class="certif-badge">DPE Certifié</span>
        <span class="certif-badge">IRVE Qualif.</span>
      </div>
    </div>
    <div class="footer-col">
      <h5>Navigation</h5>
      <a onclick="showPage('accueil')">Accueil</a>
      <a onclick="showPage('apropos')">À Propos</a>
      <a onclick="showPage('services')">Services</a>
      <a onclick="showPage('projets')">Réalisations</a>
      <a onclick="showPage('contact')">Contact</a>
    </div>
    <div class="footer-col">
      <h5>Services</h5>
      <a onclick="showPage('services')">Ingénierie CVC</a>
      <a onclick="showPage('services')">Plomberie</a>
      <a onclick="showPage('services')">Solaire PV</a>
      <a onclick="showPage('services')">DPE & Audit</a>
      <a onclick="showPage('services')">Bornes IRVE</a>
    </div>
    <div class="footer-col">
      <h5>Contact</h5>
      <a>+33 6 03 30 48 77</a>
      <a>contact@ampx.fr</a>
      
      
    </div>
  </div>
  <div class="footer-bottom">
    <p>© 2025 AmpX. Tous droits réservés.</p>
    <p>AmpX Ingénierie · Bureau d'étude thermique · CVC · DPE · Solaire · IRVE</p>
  </div>
</footer>

<script>
  // ── Navigation ──
  function showPage(id) {
    document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
    document.querySelectorAll('.nav-links a').forEach(a => a.classList.remove('active'));
    document.getElementById('page-' + id).classList.add('active');
    const navEl = document.getElementById('nav-' + id);
    if (navEl) navEl.classList.add('active');
    window.scrollTo({ top: 0, behavior: 'smooth' });
    setTimeout(initAnimations, 100);
  }

  // ── Mobile Menu ──
  let menuOpen = false;

  function toggleMenu() {
    menuOpen = !menuOpen;
    document.getElementById('navLinks').classList.toggle('open', menuOpen);
  }

  function closeMenu() {
    menuOpen = false;
    document.getElementById('navLinks').classList.remove('open');
  }

  // ── Scroll Animations ──
  function initAnimations() {
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(e => {
        if (e.isIntersecting) {
          e.target.classList.add('visible');
          observer.unobserve(e.target);
        }
      });
    }, { threshold: 0.1 });

    document.querySelectorAll('.fade-up').forEach(el => {
      el.classList.remove('visible');
      observer.observe(el);
    });
  }

  initAnimations();

  // ── Form ──
  async function submitForm() {
    const nom = document.getElementById('f-nom').value.trim();
    const email = document.getElementById('f-email').value.trim();
    const msg = document.getElementById('f-msg').value.trim();
    const tel = document.getElementById('f-tel').value.trim();
    const type = document.getElementById('f-type').value;

    if (!nom || !email || !msg) {
      alert('Veuillez remplir les champs obligatoires (nom, email, message).');
      return;
    }
    if (!/\S+@\S+\.\S+/.test(email)) {
      alert('Veuillez saisir un email valide.');
      return;
    }

    const btn = document.querySelector('.form-submit');
    btn.innerHTML = '<span>Envoi en cours...</span>';
    btn.disabled = true;

    try {
      const response = await fetch('https://formspree.io/f/xojpwrvj', {
        method: 'POST',
        headers: { 'Content-Type': 'application/json', 'Accept': 'application/json' },
        body: JSON.stringify({
          nom: nom,
          email: email,
          telephone: tel || 'Non renseigné',
          type_projet: type || 'Non renseigné',
          message: msg
        })
      });

      if (response.ok) {
        document.getElementById('form-success').style.display = 'block';
        ['f-nom','f-email','f-tel','f-type','f-msg'].forEach(id => {
          const el = document.getElementById(id);
          if (el) el.value = '';
        });
        setTimeout(() => {
          document.getElementById('form-success').style.display = 'none';
        }, 8000);
      } else {
        alert('Une erreur est survenue. Veuillez réessayer ou nous contacter directement par email.');
      }
    } catch(err) {
      alert('Erreur de connexion. Vérifiez votre connexion internet et réessayez.');
    }

    btn.innerHTML = '<span>Envoyer ma demande</span> <span>→</span>';
    btn.disabled = false;
  }

  // ── Nav shadow on scroll ──
  window.addEventListener('scroll', () => {
    const nav = document.getElementById('navbar');
    nav.style.boxShadow = window.scrollY > 20
      ? '0 4px 24px rgba(0,0,0,0.3)'
      : 'none';
  });
</script>
</body>
</html>
