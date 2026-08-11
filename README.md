<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Documentación de Sistemas · Módulo 3.4</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=IBM+Plex+Sans:wght@400;500;600&family=IBM+Plex+Mono:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#0B2545;
    --ink-2:#123163;
    --paper:#EDF1F5;
    --paper-2:#FFFFFF;
    --line:#63D2FF;
    --accent:#FFB454;
    --ok:#5FD3A3;
    --muted:#7C93B3;
    --text:#132038;
    --radius:2px;
    --grid: 32px;
  }

  *{ box-sizing:border-box; }
  html{ scroll-behavior:smooth; }

  body{
    margin:0;
    background:var(--paper);
    color:var(--text);
    font-family:'IBM Plex Sans', sans-serif;
    -webkit-font-smoothing:antialiased;
  }

  /* ---------- blueprint grid background ---------- */
  .grid-bg{
    background-image:
      linear-gradient(rgba(11,37,69,.055) 1px, transparent 1px),
      linear-gradient(90deg, rgba(11,37,69,.055) 1px, transparent 1px);
    background-size: var(--grid) var(--grid);
  }

  a{ color:inherit; }

  h1,h2,h3{
    font-family:'Space Grotesk', sans-serif;
    margin:0;
    letter-spacing:-0.01em;
  }

  .mono{ font-family:'IBM Plex Mono', monospace; }

  .eyebrow{
    font-family:'IBM Plex Mono', monospace;
    font-size:12px;
    letter-spacing:.14em;
    text-transform:uppercase;
    color:var(--muted);
  }

  .wrap{
    max-width:1040px;
    margin:0 auto;
    padding:0 28px;
  }

  /* ---------- HERO / TITLE BLOCK ---------- */
  .hero{
    background:var(--ink);
    background-image:
      linear-gradient(rgba(255,255,255,.045) 1px, transparent 1px),
      linear-gradient(90deg, rgba(255,255,255,.045) 1px, transparent 1px);
    background-size: var(--grid) var(--grid);
    color:#EAF2FF;
    padding:64px 0 0 0;
    position:relative;
    overflow:hidden;
  }

  .hero::after{
    content:"";
    position:absolute;
    left:0; right:0; bottom:0;
    height:1px;
    background:linear-gradient(90deg, transparent, var(--line), transparent);
  }

  .hero-top{
    display:flex;
    justify-content:space-between;
    align-items:flex-start;
    gap:24px;
    animation: fadeUp .7s ease both;
  }

  .hero-eyebrow{
    font-family:'IBM Plex Mono', monospace;
    font-size:12px;
    letter-spacing:.16em;
    text-transform:uppercase;
    color:var(--line);
    display:flex;
    align-items:center;
    gap:10px;
  }
  .hero-eyebrow::before{
    content:"";
    width:8px; height:8px;
    background:var(--line);
    display:inline-block;
    border-radius:50%;
    box-shadow:0 0 0 3px rgba(99,210,255,.18);
  }

  .hero h1{
    font-size:clamp(34px, 5.4vw, 58px);
    line-height:1.05;
    font-weight:700;
    max-width:780px;
    margin-top:18px;
    color:#fff;
  }

  .hero p.lead{
    margin-top:16px;
    max-width:560px;
    color:#B9CBE6;
    font-size:16.5px;
    line-height:1.6;
  }

  /* title block stamp, engineering-drawing style */
  .stamp{
    border:1px solid rgba(255,255,255,.22);
    background:rgba(255,255,255,.04);
    backdrop-filter: blur(2px);
    min-width:230px;
    font-family:'IBM Plex Mono', monospace;
    font-size:11.5px;
    flex-shrink:0;
  }
  .stamp-row{
    display:flex;
    justify-content:space-between;
    gap:12px;
    padding:9px 14px;
    border-bottom:1px solid rgba(255,255,255,.14);
  }
  .stamp-row:last-child{ border-bottom:none; }
  .stamp-row span:first-child{ color:var(--line); letter-spacing:.06em; }
  .stamp-row span:last-child{ color:#E8F1FF; text-align:right; }

  .hero-foot{
    margin-top:44px;
    padding:22px 0;
    border-top:1px solid rgba(255,255,255,.14);
    display:flex;
    flex-wrap:wrap;
    gap:14px 34px;
    font-family:'IBM Plex Mono', monospace;
    font-size:12.5px;
    color:#93A9CC;
    animation: fadeUp .8s .1s ease both;
  }
  .hero-foot b{ color:#EAF2FF; font-weight:500; }

  @keyframes fadeUp{
    from{ opacity:0; transform:translateY(10px); }
    to{ opacity:1; transform:translateY(0); }
  }

  /* ---------- SECTION HEADERS ---------- */
  .section{ padding:64px 0; }
  .section-head{
    display:flex;
    align-items:baseline;
    gap:14px;
    margin-bottom:28px;
  }
  .section-num{
    font-family:'IBM Plex Mono', monospace;
    color:var(--line-2, #2A7FB8);
    color:#2A7FB8;
    font-size:13px;
    background:#DCEAFB;
    border:1px solid #BBDBF6;
    padding:3px 8px;
    border-radius:var(--radius);
  }
  .section-head h2{
    font-size:26px;
    font-weight:600;
  }
  .section-rule{
    height:1px;
    background:repeating-linear-gradient(90deg, #B9C6D6 0 6px, transparent 6px 12px);
    margin-top:14px;
  }

  /* ---------- DOCUMENT VIEWER ---------- */
  .doc-card{
    background:var(--paper-2);
    border:1px solid #D6DEE8;
    border-radius:var(--radius);
    overflow:hidden;
  }
  .doc-toolbar{
    display:flex;
    align-items:center;
    justify-content:space-between;
    gap:16px;
    flex-wrap:wrap;
    padding:14px 18px;
    background:#F3F6FA;
    border-bottom:1px solid #D6DEE8;
  }
  .doc-toolbar-title{
    display:flex;
    align-items:center;
    gap:10px;
    font-family:'IBM Plex Mono', monospace;
    font-size:13px;
    color:var(--ink-2);
  }
  .doc-toolbar-title .dot{
    width:7px; height:7px; border-radius:50%;
    background:var(--ok);
  }
  .doc-actions{ display:flex; gap:10px; flex-wrap:wrap; }

  .btn{
    display:inline-flex;
    align-items:center;
    gap:8px;
    font-family:'IBM Plex Mono', monospace;
    font-size:12.5px;
    letter-spacing:.02em;
    padding:9px 14px;
    border-radius:var(--radius);
    text-decoration:none;
    border:1px solid transparent;
    cursor:pointer;
    transition:transform .15s ease, background .15s ease, border-color .15s ease;
  }
  .btn:hover{ transform:translateY(-1px); }
  .btn:focus-visible{ outline:2px solid var(--ink); outline-offset:2px; }

  .btn-primary{
    background:var(--ink);
    color:#fff;
  }
  .btn-primary:hover{ background:var(--ink-2); }

  .btn-ghost{
    background:transparent;
    color:var(--ink);
    border-color:#C7D3E2;
  }
  .btn-ghost:hover{ background:#E7EEF6; }

  .doc-frame-wrap{
    background:#DEE6EF;
    padding:22px;
  }
  .doc-frame-wrap iframe{
    width:100%;
    height:640px;
    border:1px solid #C7D3E2;
    background:#fff;
    border-radius:var(--radius);
    display:block;
  }

  .doc-fallback{
    display:none;
    padding:48px 22px;
    text-align:center;
    font-family:'IBM Plex Mono', monospace;
    font-size:13px;
    color:var(--muted);
  }

  /* ---------- PRODUCTS / DELIVERABLES ---------- */
  .deliverables{
    display:flex;
    flex-direction:column;
    border:1px solid #D6DEE8;
    border-radius:var(--radius);
    overflow:hidden;
    background:var(--paper-2);
  }
  .deliv-row{
    display:flex;
    align-items:center;
    gap:18px;
    padding:16px 20px;
    border-bottom:1px solid #E4EAF1;
    transition:background .15s ease;
  }
  .deliv-row:last-child{ border-bottom:none; }
  .deliv-row:hover{ background:#F5F8FB; }

  .deliv-num{
    font-family:'IBM Plex Mono', monospace;
    font-size:12px;
    color:var(--muted);
    width:26px;
    flex-shrink:0;
  }
  .deliv-name{
    flex:1;
    font-size:15px;
    font-weight:500;
  }
  .deliv-status{
    display:flex;
    align-items:center;
    gap:7px;
    font-family:'IBM Plex Mono', monospace;
    font-size:11.5px;
    color:var(--ok);
    letter-spacing:.04em;
    text-transform:uppercase;
    flex-shrink:0;
  }
  .deliv-status::before{
    content:"";
    width:7px; height:7px;
    border-radius:50%;
    background:var(--ok);
  }

  /* ---------- TOOLS ---------- */
  .tools-row{
    display:flex;
    flex-wrap:wrap;
    gap:12px;
  }
  .tool-chip{
    display:flex;
    align-items:center;
    gap:9px;
    background:var(--paper-2);
    border:1px solid #D6DEE8;
    padding:11px 16px;
    border-radius:var(--radius);
    font-family:'IBM Plex Mono', monospace;
    font-size:13px;
  }
  .tool-chip .sw{
    width:8px; height:8px;
    background:var(--accent);
  }

  /* ---------- FOOTER ---------- */
  footer{
    background:var(--ink);
    color:#B9CBE6;
    padding:44px 0;
    margin-top:20px;
  }
  .foot-grid{
    display:flex;
    justify-content:space-between;
    align-items:center;
    flex-wrap:wrap;
    gap:18px;
  }
  footer .quote{
    font-family:'Space Grotesk', sans-serif;
    color:#EAF2FF;
    font-size:16px;
    font-style:italic;
  }
  footer .meta{
    font-family:'IBM Plex Mono', monospace;
    font-size:12px;
    color:#7C93B3;
    text-align:right;
    line-height:1.7;
  }

  @media (max-width: 720px){
    .hero-top{ flex-direction:column; }
    .stamp{ width:100%; }
    .doc-frame-wrap iframe{ height:420px; }
    .foot-grid{ flex-direction:column; align-items:flex-start; text-align:left; }
    footer .meta{ text-align:left; }
  }

  @media (prefers-reduced-motion: reduce){
    *{ animation:none !important; transition:none !important; }
  }
</style>
</head>
<body>

<!-- ============ HERO ============ -->
<header class="hero">
  <div class="wrap">
    <div class="hero-top">
      <div>
        <div class="hero-eyebrow">Módulo 3.4 · Documentación de sistemas</div>
        <h1>Definir la estrategia<br>documental antes de<br>escribir una sola línea.</h1>
        <p class="lead">Investigación de normas, análisis de manuales y benchmarking para el diseño del manual técnico del proyecto — Instituto Nacional de Osicala.</p>
      </div>
      <div class="stamp">
        <div class="stamp-row"><span>DOC</span><span>Etapa 1–4</span></div>
        <div class="stamp-row"><span>MÓDULO</span><span>3.4</span></div>
        <div class="stamp-row"><span>DOCENTE</span><span>J. F. Hernández</span></div>
        <div class="stamp-row"><span>SECCIÓN</span><span>A</span></div>
        <div class="stamp-row"><span>REV</span><span>2026</span></div>
      </div>
    </div>

    <div class="hero-foot">
      <span><b>5</b> entregables completados</span>
      <span><b>PDF + Word</b> disponibles abajo</span>
      <span><b>INO</b> · Bachillerato Técnico en Desarrollo de Software</span>
    </div>
  </div>
</header>

<!-- ============ DOCUMENTO ============ -->
<section class="section grid-bg">
  <div class="wrap">
    <div class="section-head">
      <span class="section-num">01</span>
      <h2>Documento</h2>
    </div>
    <div class="section-rule" style="margin-bottom:26px;"></div>

    <div class="doc-card">
      <div class="doc-toolbar">
        <div class="doc-toolbar-title">
          <span class="dot"></span>
          etapa_decidir_1_2_3_4.pdf
        </div>
        <div class="doc-actions">
          <a class="btn btn-ghost" href="./etapa_decidir_1_2_3_4.pdf" target="_blank" rel="noopener">Abrir en pestaña nueva</a>
          <a class="btn btn-primary" href="./etapa_decidir_1_2_3_4.pdf" download>Descargar PDF</a>
          <a class="btn btn-ghost" href="./etapa_decidir_1_2_3_4.docx" download>Descargar Word</a>
        </div>
      </div>
      <div class="doc-frame-wrap">
        <iframe src="./etapa_decidir_1_2_3_4.pdf" title="Vista previa del documento"></iframe>
      </div>
    </div>
  </div>
</section>

<!-- ============ PRODUCTOS ============ -->
<section class="section">
  <div class="wrap">
    <div class="section-head">
      <span class="section-num">02</span>
      <h2>Productos</h2>
    </div>
    <div class="section-rule" style="margin-bottom:26px;"></div>

    <div class="deliverables">
      <div class="deliv-row"><span class="deliv-num">01</span><span class="deliv-name">Investigación de Normas</span><span class="deliv-status">Completo</span></div>
      <div class="deliv-row"><span class="deliv-num">02</span><span class="deliv-name">Análisis de Manuales</span><span class="deliv-status">Completo</span></div>
      <div class="deliv-row"><span class="deliv-num">03</span><span class="deliv-name">Benchmarking</span><span class="deliv-status">Completo</span></div>
      <div class="deliv-row"><span class="deliv-num">04</span><span class="deliv-name">Matriz de Diseño</span><span class="deliv-status">Completo</span></div>
      <div class="deliv-row"><span class="deliv-num">05</span><span class="deliv-name">Borrador del Manual</span><span class="deliv-status">Completo</span></div>
    </div>
  </div>
</section>

<!-- ============ HERRAMIENTAS ============ -->
<section class="section grid-bg">
  <div class="wrap">
    <div class="section-head">
      <span class="section-num">03</span>
      <h2>Herramientas</h2>
    </div>
    <div class="section-rule" style="margin-bottom:26px;"></div>

    <div class="tools-row">
      <div class="tool-chip"><span class="sw"></span>ShareX</div>
      <div class="tool-chip"><span class="sw"></span>Word</div>
      <div class="tool-chip"><span class="sw"></span>OBS</div>
      <div class="tool-chip"><span class="sw"></span>GIMP</div>
    </div>
  </div>
</section>

<!-- ============ FOOTER ============ -->
<footer>
  <div class="wrap foot-grid">
    <div class="quote">"La buena documentación no se escribe, se diseña."</div>
    <div class="meta">
      Prof. Juan Francisco Hernández<br>
      INO · Módulo 3.4 · 2026
    </div>
  </div>
</footer>

</body>
</html>
