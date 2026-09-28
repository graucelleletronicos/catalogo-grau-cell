# catalogo-grau-cell
[indexgraucell.html](https://github.com/user-attachments/files/32760478/indexgraucell.html)
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Grau Cell Eletrônicos | Catálogo Virtual</title>
  <meta name="description" content="Tecnologia, acessórios e assistência em um só lugar.">

  <!-- Fontes (Google Fonts) -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Sora:wght@600;700;800&family=Inter:wght@400;500;600&family=JetBrains+Mono:wght@500;700&display=swap" rel="stylesheet">

  <style>
    /* =====================================================================
       GRAU CELL — DESIGN TOKENS & ESTILOS GERAIS
    ===================================================================== */
    :root {
      --white: #ffffff;
      --black: #14161a;
      --yellow-light: #fff3c4;
      --yellow-soft: #fffaf0;
      --blue-royal: #1c3fd6;
      --blue-royal-dark: #142d9e;
      --blue-light: #4ea8ff;
      --border-soft: #eee4bd;
      --gray-text: #5b5f6b;
      --radius-lg: 22px;
      --radius-md: 14px;
      --radius-sm: 8px;
      --shadow-card: 0 8px 24px rgba(28,63,214,.08), 0 2px 6px rgba(20,22,26,.05);
      --font-display: 'Sora', sans-serif;
      --font-body: 'Inter', sans-serif;
      --font-mono: 'JetBrains Mono', monospace;
    }

    * { box-sizing: border-box; margin: 0; padding: 0; }
    html { scroll-behavior: smooth; }
    body {
      font-family: var(--font-body);
      color: var(--black);
      background: var(--white);
      line-height: 1.5;
      -webkit-font-smoothing: antialiased;
    }
    img { max-width: 100%; display: block; }
    button { font-family: inherit; cursor: pointer; }
    a { color: inherit; text-decoration: none; }
    :focus-visible { outline: 3px solid var(--blue-light); outline-offset: 2px; }
    ::selection { background: var(--blue-light); color: var(--black); }

    .container { max-width: 1180px; margin: 0 auto; padding: 0 20px; }
    .section { padding: 64px 0; }
    .section-title-wrap { text-align: center; margin-bottom: 36px; }
    .eyebrow {
      display: inline-block; font-family: var(--font-mono); font-size: .72rem;
      letter-spacing: .14em; text-transform: uppercase; color: var(--blue-royal);
      background: var(--yellow-light); border: 1px solid var(--border-soft);
      padding: 5px 14px; border-radius: 999px; margin-bottom: 12px;
    }
    .section-title { font-family: var(--font-display); font-size: clamp(1.5rem, 3vw, 2.1rem); font-weight: 800; }
    .section-sub { color: var(--gray-text); margin-top: 8px; max-width: 560px; margin-inline: auto; font-size: .98rem; }

    /* TOPO / HEADER */
    header.topbar {
      position: sticky; top: 0; z-index: 50;
      background: rgba(255, 255, 255, .88);
      backdrop-filter: blur(10px);
      border-bottom: 1px solid var(--border-soft);
    }
    .topbar-inner {
      display: flex; align-items: center; gap: 16px; padding: 12px 20px;
      max-width: 1180px; margin: 0 auto;
    }
    .brand { display: flex; align-items: center; gap: 10px; flex-shrink: 0; }
    .logo-badge {
      width: 42px; height: 42px; border-radius: 12px;
      background: linear-gradient(135deg, var(--blue-royal), var(--blue-light));
      color: #fff; font-family: var(--font-display); font-weight: 800; font-size: 1rem;
      display: flex; align-items: center; justify-content: center;
      box-shadow: 0 4px 14px rgba(28,63,214,.35);
    }
    .brand-name { font-family: var(--font-display); font-weight: 800; font-size: 1.05rem; line-height: 1.1; }
    .logo-slot, .logo-slot-lg { overflow: hidden; }
    .logo-slot img, .logo-slot-lg img { width: 100%; height: 100%; object-fit: contain; }
    .logo-slot.has-image, .logo-slot-lg.has-image { background: #fff; }

    .brand-name small { display: block; font-family: var(--font-body); font-weight: 500; font-size: .68rem; color: var(--gray-text); }
    .topbar-search { flex: 1; max-width: 420px; }
    .topbar-search input {
      width: 100%; border: 1.5px solid var(--border-soft); background: var(--yellow-soft);
      border-radius: 999px; padding: 10px 16px; font-size: .9rem; color: var(--black);
    }
    .topbar-search input::placeholder { color: #9a9683; }

    /* HERO / CAPA */
    .hero {
      position: relative; overflow: hidden;
      padding: 72px 20px 56px;
      text-align: center;
      background: var(--white);
    }
    .hero::before, .hero::after {
      content: ""; position: absolute; border-radius: 50%; filter: blur(60px); z-index: 0;
    }
    .hero::before {
      width: 420px; height: 420px; background: radial-gradient(circle, rgba(28,63,214,.22), transparent 70%);
      top: -160px; left: -120px;
    }
    .hero::after {
      width: 380px; height: 380px; background: radial-gradient(circle, rgba(255,224,102,.55), transparent 70%);
      bottom: -160px; right: -100px;
    }
    .hero-content { position: relative; z-index: 1; max-width: 640px; margin: 0 auto; }
    .logo-badge-lg {
      width: 74px; height: 74px; border-radius: 20px; margin: 0 auto 18px;
      background: linear-gradient(135deg, var(--blue-royal), var(--blue-light));
      color: #fff; font-family: var(--font-display); font-weight: 800; font-size: 1.7rem;
      display: flex; align-items: center; justify-content: center;
      box-shadow: 0 10px 30px rgba(28,63,214,.35);
    }
    .hero h1 {
      font-family: var(--font-display); font-weight: 800;
      font-size: clamp(2rem, 5vw, 2.9rem); letter-spacing: -.01em;
    }
    .hero p.tagline { margin-top: 12px; font-size: 1.05rem; color: var(--gray-text); }
    .hero-actions { margin-top: 26px; display: flex; gap: 12px; justify-content: center; flex-wrap: wrap; }

    /* BOTÕES */
    .btn {
      display: inline-flex; align-items: center; gap: 8px; font-weight: 600; font-size: .92rem;
      padding: 12px 22px; border-radius: 999px; border: none; transition: .2s transform, .2s box-shadow, .2s background;
    }
    .btn:active { transform: scale(.97); }
    .btn-primary { background: var(--blue-royal); color: #fff; box-shadow: 0 8px 20px rgba(28,63,214,.32); }
    .btn-primary:hover { background: var(--blue-royal-dark); box-shadow: 0 10px 26px rgba(28,63,214,.42); }
    .btn-outline { background: #fff; color: var(--black); border: 1.5px solid var(--black); }
    .btn-outline:hover { background: var(--black); color: #fff; }
    .btn-light { background: var(--yellow-light); color: var(--black); border: 1px solid var(--border-soft); }
    .btn-light:hover { background: var(--blue-light); color: #fff; }
    .btn-sm { padding: 8px 14px; font-size: .8rem; }
    .btn-block { width: 100%; justify-content: center; }
    .btn-danger { background: #fff; color: #c62839; border: 1.5px solid #f3c3ca; }
    .btn-danger:hover { background: #c62839; color: #fff; }

    /* SLIDER AUTOMÁTICO (PROPORÇÃO 1200x400) */
    .slider-container {
      max-width: 1180px;
      width: 100%;
      aspect-ratio: 1200 / 400;
      margin: 0 auto 36px auto;
      overflow: hidden;
      border-radius: var(--radius-lg);
      border: 1.5px solid var(--black);
      box-shadow: var(--shadow-card);
      position: relative;
      background: #f8f9fa;
    }
    .slider-wrapper {
      display: flex;
      width: 500%;
      height: 100%;
      transition: transform 0.6s ease-in-out;
    }
    .slide {
      width: 20%;
      height: 100%;
      flex-shrink: 0;
    }
    .slide img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
    }

    /* BANNER LOJA FÍSICA */
    .visit-banner {
      position: relative; overflow: hidden;
      background: linear-gradient(120deg, var(--blue-royal), #2a54f0 55%, var(--blue-light));
      color: #fff; border-radius: var(--radius-lg);
      margin: 0 20px; padding: 28px 28px;
      display: flex; align-items: center; justify-content: space-between; gap: 24px; flex-wrap: wrap;
      box-shadow: 0 16px 36px rgba(28,63,214,.28);
    }
    .visit-banner::after {
      content: ""; position: absolute; inset: 0;
      background: radial-gradient(circle at 85% 20%, rgba(255,243,196,.35), transparent 55%);
      pointer-events: none;
    }
    .visit-banner-text { position: relative; z-index: 1; }
    .visit-banner-text .eyebrow-w {
      font-family: var(--font-mono); font-size: .72rem; letter-spacing: .14em; text-transform: uppercase;
      background: rgba(255,255,255,.18); padding: 4px 12px; border-radius: 999px; display: inline-block; margin-bottom: 10px;
    }
    .visit-banner h2 { font-family: var(--font-display); font-size: 1.4rem; font-weight: 800; }
    .visit-banner-meta { margin-top: 10px; display: flex; gap: 18px; flex-wrap: wrap; font-size: .88rem; opacity: .95; }
    .visit-banner-meta span { display: flex; align-items: center; gap: 6px; }
    .visit-banner-actions { position: relative; z-index: 1; display: flex; gap: 10px; flex-wrap: wrap; }
    .btn-white { background: #fff; color: var(--blue-royal); }
    .btn-white:hover { background: var(--yellow-light); }
    .btn-ghost-w { background: transparent; color: #fff; border: 1.5px solid rgba(255,255,255,.55); }
    .btn-ghost-w:hover { background: rgba(255,255,255,.15); }

    /* FILTROS / CATEGORIAS */
    .filters-bar {
      position: sticky; top: 66px; z-index: 40;
      background: var(--white); padding: 16px 0; border-bottom: 1px solid var(--border-soft);
    }
    .chip-row { display: flex; gap: 8px; overflow-x: auto; padding: 2px 20px; scrollbar-width: thin; }
    .chip-row::-webkit-scrollbar { height: 5px; }
    .chip-row::-webkit-scrollbar-thumb { background: var(--border-soft); border-radius: 10px; }
    .chip {
      flex-shrink: 0; font-size: .82rem; font-weight: 600; padding: 9px 16px; border-radius: 999px;
      background: var(--yellow-soft); border: 1.5px solid var(--border-soft); color: var(--black);
      transition: .15s;
    }
    .chip:hover { border-color: var(--blue-light); }
    .chip.active { background: var(--blue-royal); border-color: var(--blue-royal); color: #fff; }

    /* GRID DE PRODUTOS & ESTILO DO CARD (BRANCO GELO + BORDA PRETA) */
    .grid {
      display: grid; grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
      gap: 20px; margin-top: 28px;
    }
    .card {
      position: relative;
      background: #f8f9fa; /* Branco gelo */
      border: 1.5px solid var(--black); /* Borda preta */
      border-radius: var(--radius-lg);
      padding: 16px; display: flex; flex-direction: column; gap: 10px;
      box-shadow: var(--shadow-card);
      transition: .25s transform, .25s box-shadow;
    }
    .card:hover { transform: translateY(-4px); box-shadow: 0 14px 28px rgba(0,0,0,.15); }
    .card::before {
      content: ""; position: absolute; top: 0; right: 0; width: 26px; height: 26px;
      background: #e9ecef;
      clip-path: polygon(100% 0, 0 0, 100% 100%);
      border-bottom: 1.5px solid var(--black); 
      border-left: 1.5px solid var(--black);
      border-top-right-radius: var(--radius-lg);
    }
    .card-media {
      aspect-ratio: 1/1; border-radius: var(--radius-md); overflow: hidden;
      background: linear-gradient(135deg, var(--blue-royal), var(--blue-light));
      display: flex; align-items: center; justify-content: center; position: relative;
    }
    .card-media img { width: 100%; height: 100%; object-fit: cover; }
    .card-media .emoji-fallback { font-size: 2.6rem; }
    .badge {
      position: absolute; top: 8px; left: 8px; font-family: var(--font-mono); font-size: .66rem; font-weight: 700;
      background: #fff; color: var(--blue-royal); padding: 4px 9px; border-radius: 999px; letter-spacing: .03em;
      box-shadow: 0 2px 8px rgba(0,0,0,.12);
    }
    .card-cat { font-size: .68rem; font-weight: 700; letter-spacing: .06em; text-transform: uppercase; color: var(--blue-royal); }
    .card h3 { font-family: var(--font-display); font-size: 1.02rem; font-weight: 700; line-height: 1.25; }
    .card .specs { font-size: .8rem; color: var(--gray-text); }
    .card .desc { font-size: .83rem; color: var(--gray-text); flex: 1; }
    .card .price { font-family: var(--font-mono); font-weight: 700; font-size: 1.18rem; color: var(--black); margin-top: 2px; }
    .card .price small { display: block; font-family: var(--font-body); font-weight: 500; font-size: .72rem; color: var(--gray-text); }
    .card .warranty-tag {
      font-size: .72rem; color: var(--blue-royal); display: flex; align-items: center; gap: 5px; font-weight: 600;
    }
    .card-actions { display: flex; gap: 8px; margin-top: 6px; }
    .card-admin-actions { display: flex; gap: 8px; margin-top: 2px; }
    .card-admin-actions button { flex: 1; }
    .empty-state { text-align: center; padding: 50px 20px; color: var(--gray-text); }
    .empty-state .big-emoji { font-size: 2.4rem; margin-bottom: 10px; }

    /* SERVIÇOS */
    .service-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(220px, 1fr)); gap: 18px; margin-top: 28px; }
    .service-card {
      background: #fff; border: 1.5px solid var(--border-soft); border-radius: var(--radius-md);
      padding: 20px; text-align: left; transition: .2s;
    }
    .service-card:hover { border-color: var(--blue-light); box-shadow: 0 10px 24px rgba(28,63,214,.1); }
    .service-card .icon {
      width: 44px; height: 44px; border-radius: 12px; background: var(--yellow-light);
      display: flex; align-items: center; justify-content: center; font-size: 1.3rem; margin-bottom: 12px;
    }
    .service-card h4 { font-family: var(--font-display); font-size: 1rem; font-weight: 700; margin-bottom: 6px; }
    .service-card p { font-size: .85rem; color: var(--gray-text); margin-bottom: 12px; }
    .service-quote { font-family: var(--font-mono); font-size: .75rem; color: var(--blue-royal); font-weight: 700; }

    /* INFORMAÇÕES (PAGAMENTO / GARANTIA) */
    .info-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(210px, 1fr)); gap: 16px; margin-top: 28px; }
    .info-card {
      background: var(--yellow-soft); border: 1px solid var(--border-soft); border-radius: var(--radius-md);
      padding: 20px;
    }
    .info-card .icon { font-size: 1.6rem; margin-bottom: 10px; }
    .info-card h4 { font-family: var(--font-display); font-weight: 700; font-size: .98rem; margin-bottom: 6px; }
    .info-card p { font-size: .84rem; color: var(--gray-text); }
    .payment-note {
      margin-top: 22px; font-size: .8rem; color: var(--gray-text); background: var(--yellow-soft);
      border-left: 3px solid var(--blue-royal); padding: 12px 16px; border-radius: 8px;
    }

    /* PASSO A PASSO */
    .steps { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 20px; margin-top: 32px; }
    .step { text-align: center; position: relative; }
    .step .step-num {
      width: 46px; height: 46px; border-radius: 50%; margin: 0 auto 12px;
      background: linear-gradient(135deg, var(--blue-royal), var(--blue-light));
      color: #fff; font-family: var(--font-display); font-weight: 800; display: flex; align-items: center; justify-content: center;
      box-shadow: 0 8px 18px rgba(28,63,214,.28);
    }
    .step h4 { font-family: var(--font-display); font-size: .95rem; font-weight: 700; margin-bottom: 4px; }
    .step p { font-size: .82rem; color: var(--gray-text); }

    /* RODAPÉ */
    footer {
      background: var(--black); color: #fff; margin-top: 40px;
      padding: 56px 0 26px; position: relative; overflow: hidden;
    }
    footer::before {
      content: ""; position: absolute; width: 400px; height: 400px; border-radius: 50%;
      background: radial-gradient(circle, rgba(28,63,214,.35), transparent 70%); filter: blur(50px);
      top: -140px; right: -100px;
    }
    .footer-grid {
      position: relative; z-index: 1;
      display: grid; grid-template-columns: 1.3fr 1fr 1fr; gap: 34px;
    }
    .footer-brand .logo-badge { margin-bottom: 12px; }
    .footer-brand p { font-size: .85rem; color: #c7c9d4; margin-top: 8px; max-width: 280px; }
    .footer-col h5 { font-family: var(--font-display); font-size: .85rem; text-transform: uppercase; letter-spacing: .08em; color: var(--blue-light); margin-bottom: 14px; }
    .footer-col p, .footer-col a { display: block; font-size: .88rem; color: #e4e5ec; margin-bottom: 10px; }
    .footer-col a:hover { color: var(--blue-light); }
    .qr-row { display: flex; gap: 14px; margin-top: 6px; }
    .qr-box {
      width: 84px; height: 84px; background: #fff; border-radius: 10px;
      display: flex; align-items: center; justify-content: center; padding: 6px;
    }
    .qr-box img { width: 100%; height: 100%; object-fit: contain; }
    .qr-label { font-size: .68rem; color: #9aa; text-align: center; margin-top: 6px; }
    .footer-bottom {
      position: relative; z-index: 1; margin-top: 40px; padding-top: 20px; border-top: 1px solid rgba(255,255,255,.12);
      display: flex; justify-content: space-between; flex-wrap: wrap; gap: 10px; font-size: .76rem; color: #9698a6;
    }

  /* CONTÊINER DOS BOTÕES SOCIAIS */
    .social-buttons-container {
      display: flex;
      gap: 16px;
      align-items: center;
      justify-content: center;
      padding: 20px 0;
    }

    /* ESTILO BASE CIRCULAR */
    .social-btn {
      width: 60px;
      height: 60px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      text-decoration: none;
      transition: transform 0.2s ease, box-shadow 0.2s ease;
    }

    .social-btn img {
      width: 32px;
      height: 32px;
      object-fit: cover;
      border-radius: 50%;
    }

    .btn-whatsapp-round {
      background-color: #1b4df5;
      box-shadow: 0 8px 20px rgba(27, 77, 245, 0.35);
    }

    .btn-instagram-round {
      background-color: #ffffff;
      border: 1.5px solid #1a1a1a;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
    }

    .social-btn:hover {
      transform: translateY(-3px);
    }

    /* MODAIS */
    .overlay {
      position: fixed; inset: 0; background: rgba(20,22,26,.6); backdrop-filter: blur(3px);
      display: none; align-items: center; justify-content: center; z-index: 100; padding: 20px;
    }
    .overlay.open { display: flex; }
    .modal {
      background: #fff; border-radius: var(--radius-lg); width: 100%; max-width: 440px;
      max-height: 88vh; overflow-y: auto; padding: 28px; position: relative;
      box-shadow: 0 30px 60px rgba(0,0,0,.35);
    }
    .modal.modal-lg { max-width: 560px; }
    .modal-close {
      position: absolute; top: 16px; right: 16px; background: var(--yellow-light);
      width: 32px; height: 32px; border-radius: 50%; border: none; font-size: 1rem; color: var(--black);
    }
    .modal h3 { font-family: var(--font-display); font-size: 1.2rem; font-weight: 800; margin-bottom: 6px; }
    .modal p.hint { font-size: .82rem; color: var(--gray-text); margin-bottom: 18px; }
    .field { margin-bottom: 14px; }
    .field label { display: block; font-size: .78rem; font-weight: 600; margin-bottom: 6px; color: var(--black); }
    .field input, .field select, .field textarea {
      width: 100%; padding: 11px 13px; border: 1.5px solid var(--border-soft); border-radius: 10px;
      font-family: inherit; font-size: .9rem; background: var(--yellow-soft); color: var(--black);
    }
    .field textarea { resize: vertical; min-height: 64px; }
    .field-row { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; }
    .form-error { font-size: .8rem; color: #c62839; margin-top: 8px; display: none; }
    .form-error.show { display: block; }

    /* PAINEL ADMIN */
    .admin-bar {
      display: none; position: sticky; top: 0; z-index: 55;
      background: var(--black); color: #fff; padding: 10px 20px; font-size: .82rem;
      align-items: center; justify-content: space-between; gap: 10px; flex-wrap: wrap;
    }
    .admin-bar.open { display: flex; }
    .admin-bar strong { color: var(--blue-light); }
    .admin-bar .admin-bar-actions { display: flex; gap: 8px; }

    /* IMAGENS DOS BOTÕES */
    .btn-image, .btn-image-lg {
      width: 22px; height: 22px; object-fit: contain; flex: 0 0 auto;
      border-radius: 50%;
    }
    .btn-image-lg { width: 28px; height: 28px; }
    .share-catalog { margin-top: 18px; display: flex; justify-content: center; }

    /* MEDIA QUERIES */
    @media (max-width: 760px) {
      .topbar-inner { flex-wrap: wrap; padding: 10px 14px; }
      .topbar-search { order: 3; max-width: 100%; width: 100%; }
      .brand-name { font-size: .95rem; }
      .hero { padding: 52px 16px 42px; }
      .hero-actions { flex-direction: column; align-items: stretch; }
      .hero-actions .btn { width: 100%; justify-content: center; }
      .slider-container { margin: 0 12px 24px 12px; width: calc(100% - 24px); }
      .visit-banner { flex-direction: column; align-items: flex-start; margin: 0 12px; padding: 22px 20px; }
      .visit-banner-actions { width: 100%; }
      .visit-banner-actions .btn { flex: 1; justify-content: center; }
      .footer-grid { grid-template-columns: 1fr; }
      .filters-bar { top: 104px; }
      .field-row { grid-template-columns: 1fr; }
      .grid { grid-template-columns: repeat(2, minmax(0, 1fr)); gap: 12px; }
      .card { padding: 12px; border-radius: 16px; }
      .card h3 { font-size: .92rem; }
      .card .desc { font-size: .76rem; }
      .card .price { font-size: 1rem; }
      .card-actions .btn { padding: 9px 10px; }
      .qr-row { flex-wrap: wrap; }
      .admin-bar { font-size: .74rem; }
      .admin-bar .admin-bar-actions { width: 100%; overflow-x: auto; }
      .admin-bar .admin-bar-actions .btn { flex-shrink: 0; }
    }

    @media (max-width: 390px) {
      .grid { grid-template-columns: 1fr; }
    }
  </style>
  <script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
</head>
<body>

  <!-- BARRA ADMIN -->
  <div class="admin-bar" id="adminBar">
    <span>🔐 Modo <strong>Lojista</strong> ativo — edições ficam salvas online.</span>
    <div class="admin-bar-actions">
      <button class="btn btn-sm btn-light" id="btnOpenAddProduct">+ Novo produto</button>
      <button class="btn btn-sm btn-light" id="btnOpenSlider">🖼️ Alterar Banners</button>
      <button class="btn btn-sm btn-light" id="btnOpenLogo">🖼️ Alterar logo</button>
      <button class="btn btn-sm btn-light" id="btnOpenButtonImages">🖼️ Imagens dos botões</button>
      <button class="btn btn-sm btn-outline" id="btnLogoutAdmin">Sair</button>
    </div>
  </div>

  <!-- TOPO -->
  <header class="topbar">
    <div class="topbar-inner">
      <div class="brand">
        <div class="logo-badge logo-slot"></div>
        <div class="brand-name">Grau Cell <small>Eletrônicos</small></div>
      </div>
      <div class="topbar-search">
        <input type="text" id="searchInput" placeholder="🔎 Buscar produto, marca ou serviço...">
      </div>
    </div>
  </header>

  <!-- HERO / CAPA -->
  <section class="hero">
    <div class="hero-content">
      <div class="logo-badge-lg logo-slot-lg"></div>
      <h1>Grau Cell Eletrônicos</h1>
      <p class="tagline">Tecnologia, acessórios e assistência em um só lugar.</p>
    </div>
  </section>

  
  <!-- BOTÕES SOCIAIS REDONDOS -->
<div class="social-buttons-container">
  <a class="social-btn btn-whatsapp-round" id="heroWhatsapp" href="#" target="_blank" rel="noopener" aria-label="WhatsApp">
    <img id="heroWhatsappImg" src="" alt="WhatsApp">
  </a>

  <a class="social-btn btn-instagram-round" id="heroInstagram" href="#" target="_blank" rel="noopener" aria-label="Instagram">
    <img id="heroInstagramImg" src="" alt="Instagram">
  </a>
</div>

  <!-- SLIDER AUTOMÁTICO DE 5 BANNERS (1200x400) -->
  <div class="container">
    <div class="slider-container">
      <div class="slider-wrapper" id="sliderWrapper">
        <div class="slide"><img id="slideImg0" src="https://via.placeholder.com/1200x400/1c3fd6/ffffff?text=Banner+1" alt="Banner 1"></div>
        <div class="slide"><img id="slideImg1" src="https://via.placeholder.com/1200x400/4ea8ff/ffffff?text=Banner+2" alt="Banner 2"></div>
        <div class="slide"><img id="slideImg2" src="https://via.placeholder.com/1200x400/14161a/ffffff?text=Banner+3" alt="Banner 3"></div>
        <div class="slide"><img id="slideImg3" src="https://via.placeholder.com/1200x400/fff3c4/14161a?text=Banner+4" alt="Banner 4"></div>
        <div class="slide"><img id="slideImg4" src="https://via.placeholder.com/1200x400/25d366/ffffff?text=Banner+5" alt="Banner 5"></div>
      </div>
    </div>
  </div>

  <!-- BANNER LOJA FÍSICA -->
  <div class="visit-banner">
    <div class="visit-banner-text">
      <span class="eyebrow-w">Loja física</span>
      <h2>Venha conhecer a Grau Cell de pertinho 👋</h2>
      <div class="visit-banner-meta">
        <span>📍 <span id="storeAddress">—</span></span>
        <span>🕐 <span id="storeHours">—</span></span>
      </div>
    </div>
    <div class="visit-banner-actions">
      <a class="btn btn-white" id="mapsLink" href="#" target="_blank" rel="noopener">🧭 Como chegar</a>
      <a class="btn btn-ghost-w" id="visitWhatsapp" href="#" target="_blank" rel="noopener">
        <img class="btn-image" id="visitWhatsappImg" alt=""> WhatsApp
      </a>
    </div>
  </div>

  <!-- FILTROS -->
  <div class="filters-bar">
    <div class="chip-row" id="chipRow"></div>
  </div>

  <!-- CATÁLOGO -->
  <section class="section" style="padding-top:36px;">
    <div class="container">
      <div class="section-title-wrap" id="catalogTitleWrap">
        <span class="eyebrow">Catálogo</span>
        <h2 class="section-title">Nossos produtos</h2>
        <p class="section-sub">Toque em "Comprar" para falar direto com a loja pelo WhatsApp.</p>
      </div>
      <div class="grid" id="productGrid"></div>
      <div class="empty-state" id="emptyState" style="display:none;">
        <div class="big-emoji">📦</div>
        <p>Nenhum produto encontrado. Tente outra busca ou categoria.</p>
      </div>
    </div>
  </section>

  <!-- ASSISTÊNCIA TÉCNICA -->
  <section class="section" id="assistencia" style="background:var(--yellow-soft);">
    <div class="container">
      <div class="section-title-wrap">
        <span class="eyebrow">Suporte técnico</span>
        <h2 class="section-title">Assistência técnica</h2>
        <p class="section-sub">Reparo rápido e de confiança. O valor varia conforme o modelo e o defeito — solicite seu orçamento sem compromisso.</p>
      </div>
      <div class="service-grid" id="serviceGrid"></div>
    </div>
  </section>

  <!-- FORMAS DE PAGAMENTO -->
  <section class="section">
    <div class="container">
      <div class="section-title-wrap">
        <span class="eyebrow">Pagamento</span>
        <h2 class="section-title">Formas de pagamento</h2>
      </div>
      <div class="info-grid">
        <div class="info-card"><div class="icon">💳</div><h4>Cartão em até 18x*</h4><p>Parcelamento facilitado no crédito, sujeito a taxas conforme a bandeira.</p></div>
        <div class="info-card"><div class="icon">💵</div><h4>À vista</h4><p>Condições especiais para pagamento à vista em dinheiro.</p></div>
        <div class="info-card"><div class="icon">📲</div><h4>Pix</h4><p>Aprovação imediata, sem taxas.</p></div>
        <div class="info-card"><div class="icon">📱</div><h4>PayJoy (Android)</h4><p>Financiamento facilitado para aparelhos Android, conforme aprovação.</p></div>
      </div>
      <p class="payment-note">*As condições de parcelamento podem variar de acordo com a operadora do cartão e o valor da compra. Consulte um de nossos atendentes para simular o parcelamento ideal para você.</p>
    </div>
  </section>

  <!-- GARANTIA -->
  <section class="section" style="background:var(--yellow-soft);">
    <div class="container">
      <div class="section-title-wrap">
        <span class="eyebrow">Confiança</span>
        <h2 class="section-title">Garantia</h2>
        <p class="section-sub">Transparência do início ao fim da sua compra.</p>
      </div>
      <div class="info-grid">
        <div class="info-card"><div class="icon">📱</div><h4>Aparelhos</h4><p>Todos os aparelhos possuem garantia contra defeitos de fabricação, conforme informado em cada produto.</p></div>
        <div class="info-card"><div class="icon">🛠️</div><h4>Serviços</h4><p>Os reparos realizados pela nossa assistência possuem garantia sobre o serviço executado.</p></div>
        <div class="info-card"><div class="icon">🔩</div><h4>Peças</h4><p>Peças e componentes utilizados nos reparos possuem garantia própria, informada no momento do orçamento.</p></div>
        <div class="info-card"><div class="icon">⚠️</div><h4>O que não é coberto</h4><p>Danos por queda, contato com líquidos, uso indevido ou violação do aparelho não são cobertos pela garantia.</p></div>
      </div>
    </div>
  </section>

  <!-- COMO COMPRAR -->
  <section class="section">
    <div class="container">
      <div class="section-title-wrap">
        <span class="eyebrow">Passo a passo</span>
        <h2 class="section-title">Como comprar</h2>
      </div>
      <div class="steps">
        <div class="step"><div class="step-num">1</div><h4>Escolha seu aparelho</h4><p>Navegue pelo catálogo e encontre o produto ideal.</p></div>
        <div class="step"><div class="step-num">2</div><h4>Fale conosco</h4><p>Toque em "Comprar" e continue a conversa no WhatsApp.</p></div>
        <div class="step"><div class="step-num">3</div><h4>Consulte as condições</h4><p>Confirme preço, forma de pagamento e disponibilidade.</p></div>
        <div class="step"><div class="step-num">4</div><h4>Retire na loja</h4><p>Venha até a Grau Cell buscar seu produto. Consulte também opções de entrega.</p></div>
      </div>
    </div>
  </section>

  <!-- RODAPÉ -->
  <footer id="contato">
    <div class="container footer-grid">
      <div class="footer-brand">
        <div class="logo-badge logo-slot"></div>
        <h3 style="font-family:var(--font-display);">Grau Cell Eletrônicos</h3>
        <p>Tecnologia, acessórios e assistência em um só lugar. Venha nos visitar ou fale com a gente pelo WhatsApp.</p>
      </div>
      <div class="footer-col">
        <h5>Contato</h5>
        <a id="footerWhatsapp" href="#" target="_blank" rel="noopener">📲 WhatsApp</a>
        <a id="footerInstagram" href="#" target="_blank" rel="noopener">📸 Instagram</a>
        <p>📍 <span id="footerAddress">—</span></p>
        <p>🕐 <span id="footerHours">—</span></p>
      </div>
      <div class="footer-col">
        <h5>Aponte a câmera</h5>
        <div class="qr-row">
          <div>
            <div class="qr-box"><img id="qrWhatsapp" alt="QR Code WhatsApp"></div>
            <div class="qr-label">WhatsApp</div>
          </div>
          <div>
            <div class="qr-box"><img id="qrInstagram" alt="QR Code Instagram"></div>
            <div class="qr-label">Instagram</div>
          </div>
        </div>
      </div>
    </div>

    <div class="container share-catalog">
      <button class="btn btn-light" id="btnShareCatalog">🔗 Compartilhar catálogo</button>
    </div>

    <div class="container" style="margin-top:22px;text-align:center;position:relative;z-index:1;">
      <button class="btn btn-sm btn-ghost-w" id="btnOpenLogin">🔐 Área do Lojista</button>
    </div>
    <div class="container footer-bottom">
      <span>© <span id="currentYear"></span> Grau Cell Eletrônicos. Todos os direitos reservados.</span>
      <span>Catálogo virtual feito com 💙 para a loja.</span>
    </div>
  </footer>

  <!-- BOTÃO FLUTUANTE -->
<a class="wa-float" id="floatWhatsapp" href="#" target="_blank" rel="noopener" aria-label="Falar no WhatsApp">💬</a>

  <!-- MODAL - LOGIN DO LOJISTA -->
  <div class="overlay" id="loginOverlay">
    <div class="modal">
      <button class="modal-close" data-close="loginOverlay">✕</button>
      <h3>Agradecemos a preferência</h3>
      <p class="hint">Entre com o e-mail e a senha cadastrados no Supabase.</p>
      <form id="loginForm">
        <div class="field">
          <label for="loginEmail">E-mail</label>
          <input type="email" id="loginEmail" autocomplete="username" required>
        </div>
        <div class="field">
          <label for="loginPassword">Senha</label>
          <input type="password" id="loginPassword" autocomplete="current-password" required>
        </div>
        <p class="form-error" id="loginError">Senha incorreta. Tente novamente.</p>
        <button type="submit" class="btn btn-primary btn-block">Entrar</button>
      </form>
    </div>
  </div>

  <!-- MODAL - CONFIGURAR BANNERS DO SLIDER -->
  <div class="overlay" id="sliderOverlay">
    <div class="modal modal-lg">
      <button class="modal-close" data-close="sliderOverlay">✕</button>
      <h3>🖼️ Banners do Carrossel (1200 x 400)</h3>
      <p class="hint">Escolha os ficheiros do seu computador para cada um dos 5 banners.</p>
      
      <div class="field"><label for="slideFile0">Banner 1 (Ficheiro)</label><input type="file" id="slideFile0" accept="image/*"></div>
      <div class="field"><label for="slideFile1">Banner 2 (Ficheiro)</label><input type="file" id="slideFile1" accept="image/*"></div>
      <div class="field"><label for="slideFile2">Banner 3 (Ficheiro)</label><input type="file" id="slideFile2" accept="image/*"></div>
      <div class="field"><label for="slideFile3">Banner 4 (Ficheiro)</label><input type="file" id="slideFile3" accept="image/*"></div>
      <div class="field"><label for="slideFile4">Banner 5 (Ficheiro)</label><input type="file" id="slideFile4" accept="image/*"></div>

      <button type="button" class="btn btn-primary btn-block" id="btnSaveSlider">💾 Salvar Banners</button>
    </div>
  </div>

  <!-- MODAL - CONFIGURAR LOGO -->
  <div class="overlay" id="logoOverlay">
    <div class="modal">
      <button class="modal-close" data-close="logoOverlay">✕</button>
      <h3>🖼️ Logo do catálogo</h3>
      <p class="hint">Escolha a logo da Grau Cell. Ela aparecerá no topo, na capa e no rodapé.</p>
      <div class="field">
        <label for="logoFile">Escolher logo do computador</label>
        <input type="file" id="logoFile" accept="image/*">
      </div>
      <div class="field">
        <label for="logoUrl">Ou usar URL da logo</label>
        <input type="url" id="logoUrl" placeholder="https://...">
      </div>
      <div id="logoPreview" style="margin:10px 0 16px;text-align:center;"></div>
      <button type="button" class="btn btn-primary btn-block" id="btnSaveLogo">💾 Salvar logo</button>
      <button type="button" class="btn btn-danger btn-block" id="btnRemoveLogo" style="margin-top:8px;">🗑️ Remover logo</button>
    </div>
  </div>

  <!-- MODAL - CONFIGURAR IMAGENS DOS BOTÕES -->
  <div class="overlay" id="buttonImagesOverlay">
    <div class="modal">
      <button class="modal-close" data-close="buttonImagesOverlay">✕</button>
      <h3>🖼️ Imagens dos botões</h3>
      <p class="hint">Troque a imagem exibida nos botões Instagram, Fale no WhatsApp e WhatsApp.</p>

      <div class="field">
        <label for="instagramButtonImage">Instagram — URL</label>
        <input type="url" id="instagramButtonImage" placeholder="https://...">
      </div>
      <div class="field">
        <label for="instagramButtonImageFile">Instagram — imagem do computador</label>
        <input type="file" id="instagramButtonImageFile" accept="image/*">
      </div>

      <div class="field">
        <label for="whatsappButtonImage">Fale no WhatsApp — URL</label>
        <input type="url" id="whatsappButtonImage" placeholder="https://...">
      </div>
      <div class="field">
        <label for="whatsappButtonImageFile">Fale no WhatsApp — imagem do computador</label>
        <input type="file" id="whatsappButtonImageFile" accept="image/*">
      </div>

      <div class="field">
        <label for="visitWhatsappButtonImage">WhatsApp — URL</label>
        <input type="url" id="visitWhatsappButtonImage" placeholder="https://...">
      </div>
      <div class="field">
        <label for="visitWhatsappButtonImageFile">WhatsApp — imagem do computador</label>
        <input type="file" id="visitWhatsappButtonImageFile" accept="image/*">
      </div>

      <button type="button" class="btn btn-primary btn-block" id="btnSaveButtonImages">💾 Salvar imagens</button>
      <button type="button" class="btn btn-danger btn-block" id="btnRemoveButtonImages" style="margin-top:8px;">🗑️ Remover imagens personalizadas</button>
    </div>
  </div>

  <!-- MODAL - ADICIONAR / EDITAR PRODUTO -->
  <div class="overlay" id="productOverlay">
    <div class="modal modal-lg">
      <button class="modal-close" data-close="productOverlay">✕</button>
      <h3 id="productFormTitle">Novo produto</h3>
      <p class="hint">Preencha os dados do produto ou serviço.</p>
      <form id="productForm">
        <input type="hidden" id="productId">
        <div class="field">
          <label for="productName">Nome do produto *</label>
          <input type="text" id="productName" placeholder="Ex: Realme C75 256GB" required>
        </div>
        <div class="field-row">
          <div class="field">
            <label for="productCategory">Categoria *</label>
            <select id="productCategory" required></select>
          </div>
          <div class="field">
            <label for="productPrice">Preço à vista (R$)</label>
            <input type="text" id="productPrice" placeholder="Ex: 1499,00">
          </div>
        </div>
        <div class="field">
          <label for="productSpecs">Especificações (opcional)</label>
          <input type="text" id="productSpecs" placeholder="Ex: 256GB • 8GB RAM">
        </div>
        <div class="field">
          <label for="productDesc">Descrição / diferenciais</label>
          <textarea id="productDesc" placeholder="Ex: 🔋 Bateria de alta capacidade"></textarea>
        </div>
        <div class="field-row">
          <div class="field">
            <label for="productWarranty">Garantia (opcional)</label>
            <input type="text" id="productWarranty" placeholder="Ex: 90 dias">
          </div>
          <div class="field">
            <label for="productBadge">Selo (opcional)</label>
            <input type="text" id="productBadge" placeholder="Ex: Mais vendido">
          </div>
        </div>
        <div class="field">
          <label for="productImage">URL da imagem (opcional)</label>
          <input type="url" id="productImage" placeholder="https://...">
        </div>
        <div class="field">
          <label for="productImageFile">Ou escolha uma imagem do computador</label>
          <input type="file" id="productImageFile" accept="image/*">
        </div>
        <button type="submit" class="btn btn-primary btn-block">💾 Salvar produto</button>
      </form>
    </div>
  </div>

  <script>
    /* 1) CONFIGURAÇÕES DA LOJA */
    const STORE_CONFIG = {
      whatsappNumber: "5562991555048",
      instagramUser: "grau.cell",
      address: "Av. Senador Canedo, Qd 62 Lt 13 - Jardim das Oliveiras, Senador Canedo - GO",
      mapsUrl: "https://maps.google.com/?q=Grau+Cell+Eletrônicos+Senador+Canedo",
      hours: "Seg a Sex, 09h às 18:30",
      defaultMessage: "Olá! Vim pelo catálogo virtual da Grau Cell e gostaria de mais informações.",
      buttonImages: { instagram: "", whatsapp: "", visitWhatsapp: "" }
    };

    /* 2) CATEGORIAS DO CATÁLOGO */
    const CATEGORIES = [
      { id: "todos", label: "🗂️ Todos" },
      { id: "acessorio-capinha", label: "Capinhas" },
      { id: "acessorio-pelicula", label: "Películas" },
      { id: "acessorio-cabo", label: "Cabos" },
      { id: "acessorio-carregador", label: "Carregadores" },
      { id: "acessorio-fone", label: "Fones" },
      { id: "acessorio-smartwatch", label: "Smartwatches" },
      { id: "acessorio-suporte", label: "Suportes/ventosas" },
      { id: "acessorio-informatica", label: "Informáticas" },
      { id: "acessorio-caixa", label: "Caixas de som" },
      { id: "acessorio-infantil", label: "Opções para Infantil" },
      { id: "acessorio-cartão", label: "Cartão de memória" },
      { id: "acessorio-umidificador", label: "Umidificador" },
      { id: "acessorio-adaptadores", label: "Adaptadores" },
      { id: "acessorio-suportes", label: "Suportes de celulares para carro/moto" },
      { id: "acessorio-mídia", label: "Mídia" },
      { id: "acessorio-powerbank", label: "Powerbanks" },
      { id: "acessorio-pilha", label: "Pilhas" },
      { id: "acessorio-garrafa", label: "Garrafas/copos de água" },
      { id: "acessorio-rádio", label: "Rádio" },
      { id: "acessorio-Outros", label: "Outros" },
    ];
    const CATEGORY_LABELS = Object.fromEntries(CATEGORIES.map(c => [c.id, c.label]));

    /* 3) SERVIÇOS */
    const SERVICES = [
      { icon:"🖥️", name:"Troca de tela", desc: "Troca de telas quebradas, trincadas ou com falhas, com peças de qualidade e película de brinde." },
      { icon:"🔋", name:"Troca de bateria", desc:"Substituição de baterias com baixa duração, estufadas ou com desgaste, com serviço de qualidade e garantia." },
      { icon:"🔌", name:"Conector/base de carga", desc:"Reparo ou substituição do conector de carga para aparelhos que não carregam, apresentam mau contato ou carregam com dificuldade." },
      { icon:"🧩", name:"Reparo de placa", desc:"Diagnóstico e reparo de falhas na placa, incluindo problemas de energia, carregamento e funcionamento do aparelho." },
      { icon:"⚙️", name:"Formatação/configuração", desc:"Formatação, atualização, configuração e otimização do aparelho para deixá-lo pronto para uso." },
      { icon:"🛠️", name:"Outros serviços", desc:"Realizamos diversos reparos, como câmera, alto-falante, microfone, botões e outros serviços sob avaliação."},
    ];

    /* 4) PRODUTOS INICIAIS */
    const SEED_PRODUCTS = [
      { id:"p1", name:"Realme C75", category:"celular-destaque", price:"1.499,00", specs:"256GB • 8GB RAM", badge:"Mais vendido", warranty:"Garantia de 12 meses (fabricante)", desc:"🔋 Bateria de alta capacidade\n📸 Ótimo conjunto de câmeras\n💧 Resistente à água", image:"" },
      { id:"p2", name:"Samsung Galaxy A16", category:"celular-novo", price:"1.199,00", specs:"128GB • 4GB RAM", badge:"", warranty:"Garantia de 12 meses (fabricante)", desc:"📷 Câmera tripla\n🖥️ Tela grande AMOLED\n🔋 Bateria de longa duração", image:"" },
      { id:"p3", name:"iPhone 11 Seminovo", category:"celular-seminovo", price:"1.899,00", specs:"64GB", badge:"Vitrine", warranty:"Garantia de 90 dias (loja)", desc:"✅ Bateria testada acima de 85%\n🔍 Revisado e higienizado\n📦 Acompanha cabo", image:"" },
      { id:"p4", name:"Capinha Anti-impacto", category:"acessorio-capinha", price:"29,90", specs:"Vários modelos", badge:"", warranty:"", desc:"Proteção reforçada nas bordas e câmera.", image:"" },
      { id:"p5", name:"Película de Vidro 3D", category:"acessorio-pelicula", price:"19,90", specs:"Vários modelos", badge:"", warranty:"", desc:"Proteção total da tela contra riscos e quedas.", image:"" },
      { id:"p6", name:"Carregador Turbo 33W", category:"acessorio-carregador", price:"49,90", specs:"USB-C", badge:"", warranty:"Garantia de 3 meses", desc:"Carregamento rápido e seguro.", image:"" },
      { id:"p7", name:"Fone Bluetooth TWS", category:"acessorio-fone", price:"79,90", specs:"Com case carregador", badge:"", warranty:"Garantia de 3 meses", desc:"Som nítido e conexão estável.", image:"" },
      { id:"p8", name:"Smartwatch D20", category:"acessorio-smartwatch", price:"89,90", specs:"Monitor cardíaco", badge:"", warranty:"Garantia de 3 meses", desc:"Notificações, monitor de saúde e várias funções.", image:"" },
    ];

    const CATEGORY_EMOJI = {
      "celular-novo":"📱","celular-seminovo":"♻️","celular-destaque":"⭐",
      "acessorio-capinha":"📦","acessorio-pelicula":"🛡️","acessorio-cabo":"🔌",
      "acessorio-carregador":"⚡","acessorio-fone":"🎧","acessorio-smartwatch":"⌚",
      "acessorio-suporte":"📐","acessorio-cordinha":"🎀"
    };

    /* 5) SUPABASE */
    const SUPABASE_URL = "https://ssqbpkxnsthggxnihzfw.supabase.co";
    const SUPABASE_ANON_KEY = "sb_publishable_wuWblDpOQd1Aue_AHuDOxA_UKucfIGn";
    const SUPABASE_TABLE = "catalog_state";
    const SUPABASE_BUCKET = "catalog-images";
    const REMOTE_ID = "main";
    const supabaseClient = window.supabase.createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

    const LS_PRODUCTS_KEY = "graucell_products";
    const LS_LOGO_KEY = "graucell_logo";
    const LS_BUTTON_IMAGES_KEY = "graucell_button_images";
    const LS_SLIDER_KEY = "graucell_slider_images";
    const SS_AUTH_KEY = "graucell_admin_auth";

    function loadProducts() {
      try {
        const raw = localStorage.getItem(LS_PRODUCTS_KEY);
        if (raw) return JSON.parse(raw);
      } catch(e) {}
      return SEED_PRODUCTS.slice();
    }

    async function loadRemoteState() {
      const { data, error } = await supabaseClient
        .from(SUPABASE_TABLE)
        .select("id,products,logo,button_images")
        .eq("id", REMOTE_ID)
        .maybeSingle();
      if (error) throw error;
      return data;
    }

async function saveRemoteState() {
      // Todos os dados de imagem ficam centralizados no Supabase:
      // produtos -> products[].image
      // logo -> logo
      // botões + banners -> button_images
      const payload = {
        id: REMOTE_ID,
        products,
        logo: getLogo(),
        button_images: getButtonImages()
      };

      const { error } = await supabaseClient
        .from(SUPABASE_TABLE)
        .upsert(payload, { onConflict: "id" });

      if (error) throw error;

      localStorage.setItem(LS_PRODUCTS_KEY, JSON.stringify(products));
    }
    function isAdminAuthenticated() {
      return sessionStorage.getItem(SS_AUTH_KEY) === "true";
    }

    let products = loadProducts();
    let currentFilter = "todos";
    let currentSearch = "";
    let remoteReady = false;

    async function syncFromSupabase() {
      try {
        const state = await loadRemoteState();
        if (state) {
          products = Array.isArray(state.products) ? state.products : SEED_PRODUCTS.slice();
          localStorage.setItem(LS_PRODUCTS_KEY, JSON.stringify(products));
          if (state.logo) localStorage.setItem(LS_LOGO_KEY, state.logo);
          else localStorage.removeItem(LS_LOGO_KEY);
          const remoteButtonImages = state.button_images || {};
          localStorage.setItem(LS_BUTTON_IMAGES_KEY, JSON.stringify(remoteButtonImages));

          // Os banners são armazenados junto das imagens dos botões para
          // não depender de uma coluna slider_images que não existe na tabela atual.
          if (Array.isArray(remoteButtonImages.slider)) {
            localStorage.setItem(LS_SLIDER_KEY, JSON.stringify(remoteButtonImages.slider));
          }
        } else {
          await saveRemoteState();
        }
        remoteReady = true;
        renderLogo();
        renderStoreInfo();
        renderCatalog();
        renderSliderImages();
      } catch (err) {
        console.error("Erro ao sincronizar catálogo:", err);
      }
    }

    async function uploadImage(file, folder) {
      if (!file) return "";
      const ext = (file.name.split(".").pop() || "jpg").toLowerCase().replace(/[^a-z0-9]/g, "");
      const path = `${folder}/${Date.now()}-${Math.random().toString(36).slice(2)}.${ext || "jpg"}`;
      const { error } = await supabaseClient.storage.from(SUPABASE_BUCKET).upload(path, file, {
        upsert: false,
        contentType: file.type || "image/jpeg",
        cacheControl: "31536000"
      });
      if (error) throw error;
      const { data } = supabaseClient.storage.from(SUPABASE_BUCKET).getPublicUrl(path);
      if (!data || !data.publicUrl) throw new Error("URL pública não gerada.");
      return data.publicUrl;
    }

    async function saveProducts(productsToSave) {
      products = productsToSave;
      if (!remoteReady) throw new Error("Catálogo online ainda não está pronto.");
      await saveRemoteState();
    }

    /* 6) HELPERS DE WHATSAPP / LINKS */
    function waLink(message) {
      const text = encodeURIComponent(message || STORE_CONFIG.defaultMessage);
      return `https://wa.me/${STORE_CONFIG.whatsappNumber}?text=${text}`;
    }
    function igLink() { return `https://instagram.com/${STORE_CONFIG.instagramUser}`; }
    function qrLink(url) { return `https://api.qrserver.com/v1/create-qr-code/?size=160x160&data=${encodeURIComponent(url)}`; }

    /* 7) LOGO & ELEMENTOS */
    function getLogo() { return localStorage.getItem(LS_LOGO_KEY) || ""; }
    function renderLogo() {
      const logo = getLogo();
      document.querySelectorAll(".logo-slot, .logo-slot-lg").forEach(el => {
        if (logo) {
          el.classList.add("has-image");
          el.innerHTML = `<img src="${escapeHtml(logo)}" alt="Logo Grau Cell">`;
        } else {
          el.classList.remove("has-image");
          el.innerHTML = "GC";
        }
      });
    }

    function getButtonImages() {
      try {
        const saved = JSON.parse(localStorage.getItem(LS_BUTTON_IMAGES_KEY) || "{}");
        // Os banners ficam dentro do mesmo JSON já existente no Supabase.
        // Assim não é necessário criar uma nova coluna na tabela catalog_state.
        return {
          ...STORE_CONFIG.buttonImages,
          ...saved,
          slider: getSliderImages()
        };
      } catch (e) {
        return {
          ...STORE_CONFIG.buttonImages,
          slider: getSliderImages()
        };
      }
    }
    function setButtonImage(id, src) {
      const el = document.getElementById(id);
      if (!el) return;
      if (src) { el.src = src; el.style.display = "block"; }
      else { el.removeAttribute("src"); el.style.display = "none"; }
    }

    function renderButtonImages() {
      const imgs = getButtonImages();
      setButtonImage("heroInstagramImg", imgs.instagram);
      setButtonImage("heroWhatsappImg", imgs.whatsapp);
      setButtonImage("visitWhatsappImg", imgs.visitWhatsapp || imgs.whatsapp);
    }

    function renderStoreInfo() {
      document.getElementById("heroWhatsapp").href = waLink();
      document.getElementById("heroInstagram").href = igLink();
      document.getElementById("visitWhatsapp").href = waLink();
      document.getElementById("footerWhatsapp").href = waLink();
      document.getElementById("footerInstagram").href = igLink();
      document.getElementById("floatWhatsapp").href = waLink();
      document.getElementById("mapsLink").href = STORE_CONFIG.mapsUrl;
      document.getElementById("storeAddress").textContent = STORE_CONFIG.address;
      document.getElementById("storeHours").textContent = STORE_CONFIG.hours;
      document.getElementById("footerAddress").textContent = STORE_CONFIG.address;
      document.getElementById("footerHours").textContent = STORE_CONFIG.hours;
      document.getElementById("qrWhatsapp").src = qrLink(waLink());
      document.getElementById("qrInstagram").src = qrLink(igLink());
      document.getElementById("currentYear").textContent = new Date().getFullYear();
      renderButtonImages();
    }

    /* 8) CARROSSEL / SLIDER AUTOMÁTICO */
    let currentSlide = 0;
    setInterval(() => {
      currentSlide = (currentSlide + 1) % 5;
      const wrapper = document.getElementById("sliderWrapper");
      if (wrapper) wrapper.style.transform = `translateX(-${currentSlide * 20}%)`;
    }, 3500);

    function getSliderImages() {
      try { return JSON.parse(localStorage.getItem(LS_SLIDER_KEY) || "[]"); }
      catch(e) { return []; }
    }

    function renderSliderImages() {
      const saved = getSliderImages();
      for (let i = 0; i < 5; i++) {
        const imgEl = document.getElementById(`slideImg${i}`);
        if (imgEl && saved[i]) imgEl.src = saved[i];
      }
    }

    /* 9) CATEGORIAS */
    function renderChips() {
      const row = document.getElementById("chipRow");
      row.innerHTML = "";
      CATEGORIES.forEach(cat => {
        const btn = document.createElement("button");
        btn.className = "chip" + (cat.id === currentFilter ? " active" : "");
        btn.textContent = cat.label;
        btn.addEventListener("click", () => {
          currentFilter = cat.id;
          renderChips();
          renderCatalog();
        });
        row.appendChild(btn);
      });
    }

    /* 10) PRODUTOS DO CATÁLOGO */
    function getFilteredProducts() {
      const nonAssistCategories = CATEGORIES.map(c => c.id).filter(id => id !== "todos");
      return products.filter(p => {
        if(!nonAssistCategories.includes(p.category)) return false;
        const matchesCategory = currentFilter === "todos" || p.category === currentFilter;
        const term = currentSearch.trim().toLowerCase();
        const matchesSearch = !term ||
          p.name.toLowerCase().includes(term) ||
          (p.desc || "").toLowerCase().includes(term) ||
          (p.specs || "").toLowerCase().includes(term);
        return matchesCategory && matchesSearch;
      });
    }

    function productCardHTML(p) {
      const emoji = CATEGORY_EMOJI[p.category] || "📦";
      const mediaInner = p.image
        ? `<img src="${escapeHtml(p.image)}" alt="${escapeHtml(p.name)}" onerror="this.parentElement.innerHTML='<span class=\\'emoji-fallback\\'>${emoji}</span>'">`
        : `<span class="emoji-fallback">${emoji}</span>`;
      const badge = p.badge ? `<span class="badge">${escapeHtml(p.badge)}</span>` : "";
      const specs = p.specs ? `<div class="specs">${escapeHtml(p.specs)}</div>` : "";
      const desc = p.desc ? `<div class="desc">${escapeHtml(p.desc).replace(/\n/g,"<br>")}</div>` : "";
      const price = p.price ? `<div class="price">R$ ${escapeHtml(p.price)}</div>` : `<div class="price" style="font-size:.95rem;">Consulte o valor</div>`;
      const warranty = p.warranty ? `<div class="warranty-tag">🛡️ ${escapeHtml(p.warranty)}</div>` : "";
      const message = `${STORE_CONFIG.defaultMessage} Tenho interesse em: ${p.name}.`;
      const adminActions = isAdminAuthenticated() ? `
        <div class="card-admin-actions">
          <button class="btn btn-sm btn-light" onclick="openProductForm('${p.id}')">✏️ Editar</button>
          <button class="btn btn-sm btn-danger" onclick="deleteProduct('${p.id}')">🗑️ Excluir</button>
        </div>` : "";
      return `
        <article class="card"> 
          <div class="card-media">
            ${mediaInner}
            ${badge}
          </div> 
          <div class="card-cat">${CATEGORY_LABELS[p.category] || ""}</div>
          <h3>${escapeHtml(p.name)}</h3>
          ${specs}
          ${desc}
          ${price}
          ${warranty}
          <div class="card-actions">
            <a class="btn btn-primary btn-block btn-sm" href="${waLink(message)}" target="_blank" rel="noopener">🛒 Comprar</a>
          </div>
          ${adminActions}
        </article>`;
    }

    function renderCatalog() {
      const grid = document.getElementById("productGrid");
      const empty = document.getElementById("emptyState");
      const list = getFilteredProducts();
      grid.innerHTML = list.map(productCardHTML).join("");
      empty.style.display = list.length ? "none" : "block";
    }

    /* 11) SERVIÇOS */
    function renderServices() {
      const grid = document.getElementById("serviceGrid");
      grid.innerHTML = SERVICES.map(s => {
        const message = `${STORE_CONFIG.defaultMessage} Gostaria de um orçamento para: ${s.name}.`;
        return `
          <div class="service-card">
            <div class="icon">${s.icon}</div>
            <h4>${escapeHtml(s.name)}</h4>
            <p>${escapeHtml(s.desc)}</p>
            <div class="service-quote">💬 Consulte o orçamento</div>
            <a class="btn btn-sm btn-light btn-block" style="margin-top:10px;" href="${waLink(message)}" target="_blank" rel="noopener">Solicitar orçamento</a>
          </div>`;
      }).join("");
    }

    function escapeHtml(str) {
      return String(str ?? "").replace(/[&<>"']/g, s => ({
        "&":"&amp;","<":"&lt;",">":"&gt;","\"":"&quot;","'":"&#39;"
      }[s]));
    }

    /* 12) PAINEL LOJISTA E MODAIS */
    const loginOverlay = document.getElementById("loginOverlay");
    const productOverlay = document.getElementById("productOverlay");
    const buttonImagesOverlay = document.getElementById("buttonImagesOverlay");
    const sliderOverlay = document.getElementById("sliderOverlay");

    document.getElementById("btnOpenLogin").addEventListener("click", async () => {
      const { data } = await supabaseClient.auth.getSession();
      if (data.session) {
        sessionStorage.setItem(SS_AUTH_KEY, "true");
        toggleAdminMode(true);
        return;
      }
      document.getElementById("loginError").classList.remove("show");
      document.getElementById("loginEmail").value = "";
      document.getElementById("loginPassword").value = "";
      loginOverlay.classList.add("open");
      document.getElementById("loginEmail").focus();
    });

    document.getElementById("loginForm").addEventListener("submit", async (e) => {
      e.preventDefault();
      const email = document.getElementById("loginEmail").value.trim();
      const password = document.getElementById("loginPassword").value;
      const errorEl = document.getElementById("loginError");
      errorEl.classList.remove("show");
      try {
        const { error } = await supabaseClient.auth.signInWithPassword({ email, password });
        if (error) throw error;
        sessionStorage.setItem(SS_AUTH_KEY, "true");
        loginOverlay.classList.remove("open");
        toggleAdminMode(true);
      } catch (err) {
        errorEl.textContent = "E-mail ou senha incorretos.";
        errorEl.classList.add("show");
      }
    });

    document.getElementById("btnLogoutAdmin").addEventListener("click", async () => {
      await supabaseClient.auth.signOut();
      sessionStorage.removeItem(SS_AUTH_KEY);
      toggleAdminMode(false);
    });

    function toggleAdminMode(on) {
      document.getElementById("adminBar").classList.toggle("open", on);
      document.getElementById("btnOpenLogin").textContent = on ? "🔑 Painel aberto" : "Agradecemos a preferência";
      renderCatalog();
    }

    document.querySelectorAll("[data-close]").forEach(btn => {
      btn.addEventListener("click", () => {
        document.getElementById(btn.dataset.close).classList.remove("open");
      });
    });

    [loginOverlay, productOverlay, buttonImagesOverlay, sliderOverlay].forEach(ov => {
      if(ov) ov.addEventListener("click", (e) => { if(e.target === ov) ov.classList.remove("open"); });
    });

    /* 13) CONFIGURAR SLIDER BANNERS */
    document.getElementById("btnOpenSlider")?.addEventListener("click", () => {
      for (let i = 0; i < 5; i++) {
        const input = document.getElementById(`slideFile${i}`);
        if (input) input.value = "";
      }
      sliderOverlay.classList.add("open");
    });

    document.getElementById("btnSaveSlider")?.addEventListener("click", async () => {
      const saved = getSliderImages();
      let alterou = false;

      try {
        for (let i = 0; i < 5; i++) {
          const fileInput = document.getElementById(`slideFile${i}`);
          if (!fileInput || !fileInput.files[0]) continue;

          // A imagem é enviada para o Storage; o Supabase guarda a URL pública.
          saved[i] = await uploadImage(fileInput.files[0], "banners");
          alterou = true;
        }

        if (!alterou) {
          sliderOverlay.classList.remove("open");
          return;
        }

        // Atualiza o estado local antes de sincronizar.
        localStorage.setItem(LS_SLIDER_KEY, JSON.stringify(saved));
        await saveRemoteState();

        renderSliderImages();
        sliderOverlay.classList.remove("open");
        alert("Banners atualizados e salvos online com sucesso!");
      } catch (err) {
        console.error("Erro ao salvar banners:", err);
        alert("Erro ao salvar os banners online: " + (err.message || "erro desconhecido"));
      }
    });
    /* 14) CADASTRO PRODUTOS */
    function populateCategorySelect() {
      const select = document.getElementById("productCategory");
      select.innerHTML = CATEGORIES.filter(c => c.id !== "todos")
        .map(c => `<option value="${c.id}">${c.label}</option>`).join("");
    }

    function openProductForm(productId) {
      const isEdit = !!productId;
      document.getElementById("productFormTitle").textContent = isEdit ? "Editar produto" : "Novo produto";
      const p = isEdit ? products.find(x => x.id === productId) : null;
      document.getElementById("productId").value = p ? p.id : "";
      document.getElementById("productName").value = p ? p.name : "";
      document.getElementById("productCategory").value = p ? p.category : CATEGORIES[1].id;
      document.getElementById("productPrice").value = p ? p.price : "";
      document.getElementById("productSpecs").value = p ? p.specs : "";
      document.getElementById("productDesc").value = p ? p.desc : "";
      document.getElementById("productBadge").value = p ? p.badge : "";
      document.getElementById("productWarranty").value = p ? p.warranty : "";
      document.getElementById("productImage").value = p ? p.image : "";
      document.getElementById("productImageFile").value = "";
      productOverlay.classList.add("open");
    }

    document.getElementById("btnOpenAddProduct").addEventListener("click", () => openProductForm(null));

    document.getElementById("productForm").addEventListener("submit", async (e) => {
      e.preventDefault();
      const id = document.getElementById("productId").value || ("p" + Date.now());
      let image = document.getElementById("productImage").value.trim();
      const imageFile = document.getElementById("productImageFile").files[0];

      if (imageFile) {
        try { image = await uploadImage(imageFile, "products"); }
        catch (err) { alert("Erro ao carregar imagem."); return; }
      }

      const data = {
        id,
        name: document.getElementById("productName").value.trim(),
        category: document.getElementById("productCategory").value,
        price: document.getElementById("productPrice").value.trim(),
        specs: document.getElementById("productSpecs").value.trim(),
        desc: document.getElementById("productDesc").value.trim(),
        badge: document.getElementById("productBadge").value.trim(),
        warranty: document.getElementById("productWarranty").value.trim(),
        image
      };

      const existingIndex = products.findIndex(p => p.id === id);
      if (existingIndex >= 0) { products[existingIndex] = data; }
      else { products.push(data); }

      try {
        await saveProducts(products);
        productOverlay.classList.remove("open");
        renderCatalog();
      } catch (err) { alert("Erro ao salvar produto online."); }
    });

    async function deleteProduct(id) {
      if (!confirm("Tem certeza que deseja excluir este produto?")) return;
      products = products.filter(p => p.id !== id);
      try {
        await saveProducts(products);
        renderCatalog();
      } catch (err) { alert("Erro ao excluir produto."); }
    }

    /* 15) BUSCA & OUTROS MODAIS */
    document.getElementById("searchInput").addEventListener("input", (e) => {
      currentSearch = e.target.value;
      renderCatalog();
    });

    const logoOverlay = document.getElementById("logoOverlay");
    document.getElementById("btnOpenLogo").addEventListener("click", () => {
      const logo = getLogo();
      document.getElementById("logoUrl").value = logo && !logo.startsWith("data:") ? logo : "";
      document.getElementById("logoFile").value = "";
      document.getElementById("logoPreview").innerHTML = logo
        ? `<img src="${escapeHtml(logo)}" style="max-width:180px;max-height:120px;border-radius:12px;object-fit:contain;border:1px solid var(--border-soft);padding:8px;">`
        : `<span style="color:var(--gray-text);font-size:.85rem;">Nenhuma logo personalizada.</span>`;
      logoOverlay.classList.add("open");
    });

    document.getElementById("btnSaveLogo").addEventListener("click", async () => {
      let logo = document.getElementById("logoUrl").value.trim();
      const file = document.getElementById("logoFile").files[0];
      if (file) {
        try { logo = await uploadImage(file, "logo"); }
        catch (err) { alert("Erro ao carregar a logo."); return; }
      }
      if (!logo) { alert("Escolha uma imagem ou informe uma URL."); return; }

      try {
        localStorage.setItem(LS_LOGO_KEY, logo);
        await saveRemoteState();
        logoOverlay.classList.remove("open");
        renderLogo();
      } catch (err) { alert("Erro ao salvar logo online."); }
    });

    document.getElementById("btnRemoveLogo").addEventListener("click", async () => {
      if (!confirm("Remover a logo personalizada?")) return;
      localStorage.removeItem(LS_LOGO_KEY);
      try {
        await saveRemoteState();
        logoOverlay.classList.remove("open");
        renderLogo();
      } catch (err) { alert("Erro ao remover logo."); }
    });

    document.getElementById("btnOpenButtonImages").addEventListener("click", () => {
      const imgs = getButtonImages();
      document.getElementById("instagramButtonImage").value = imgs.instagram.startsWith("data:") ? "" : imgs.instagram;
      document.getElementById("whatsappButtonImage").value = imgs.whatsapp.startsWith("data:") ? "" : imgs.whatsapp;
      document.getElementById("visitWhatsappButtonImage").value = (imgs.visitWhatsapp || "").startsWith("data:") ? "" : (imgs.visitWhatsapp || "");
      buttonImagesOverlay.classList.add("open");
    });

    document.getElementById("btnSaveButtonImages").addEventListener("click", async () => {
      const imgs = getButtonImages();
      const fields = [
        ["instagramButtonImage", "instagramButtonImageFile", "instagram"],
        ["whatsappButtonImage", "whatsappButtonImageFile", "whatsapp"],
        ["visitWhatsappButtonImage", "visitWhatsappButtonImageFile", "visitWhatsapp"]
      ];

      for (const [urlId, fileId, key] of fields) {
        let value = document.getElementById(urlId).value.trim();
        const file = document.getElementById(fileId).files[0];
        if (file) {
          try { value = await uploadImage(file, `buttons/${key}`); }
          catch (err) { alert("Erro ao carregar imagem do botão."); return; }
        }
        imgs[key] = value;
      }

      try {
        localStorage.setItem(LS_BUTTON_IMAGES_KEY, JSON.stringify(imgs));
        await saveRemoteState();
        buttonImagesOverlay.classList.remove("open");
        renderButtonImages();
      } catch (err) { alert("Erro ao salvar imagens."); }
    });

    document.getElementById("btnRemoveButtonImages").addEventListener("click", async () => {
      if (!confirm("Remover todas as imagens personalizadas dos botões?")) return;
      localStorage.removeItem(LS_BUTTON_IMAGES_KEY);
      try {
        await saveRemoteState();
        buttonImagesOverlay.classList.remove("open");
        renderButtonImages();
      } catch (err) { alert("Erro ao remover imagens."); }
    });

    document.getElementById("btnShareCatalog").addEventListener("click", async () => {
      const shareData = {
        title: "Grau Cell Eletrônicos | Catálogo Virtual",
        text: "Confira o catálogo virtual da Grau Cell!",
        url: window.location.href
      };
      try {
        if (navigator.share) await navigator.share(shareData);
        else if (navigator.clipboard) {
          await navigator.clipboard.writeText(window.location.href);
          alert("Link do catálogo copiado!");
        } else prompt("Copie o link do catálogo:", window.location.href);
      } catch (err) {}
    });

    /* 16) INICIALIZAÇÃO */
    async function init() {
      renderLogo();
      renderStoreInfo();
      populateCategorySelect();
      renderChips();
      renderCatalog();
      renderServices();
      renderSliderImages();
      
      const { data } = await supabaseClient.auth.getSession();
      if (data && data.session) {
        sessionStorage.setItem(SS_AUTH_KEY, "true");
      } else {
        sessionStorage.removeItem(SS_AUTH_KEY);
      }
      toggleAdminMode(!!(data && data.session));
      await syncFromSupabase();
    }

    init();
  </script>
</body>
</html>
