# IA.HUB
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Hub de Negocios IA · 100 Formas de Ganar Dinero Gratis</title>
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<style>
  :root{
    --bg:#060a13; --bg-alt:#0c1220; --card:#101829; --card-hover:#1a2438;
    --border:#1e2a42; --text:#e8eefc; --text-dim:#8fa3c0;
    --accent:#6366f1; --accent2:#22d3ee; --green:#10b981;
    --amber:#f59e0b; --red:#ef4444;
    --grad:linear-gradient(135deg,#6366f1 0%,#22d3ee 100%);
  }
  [data-theme="light"]{
    --bg:#f5f7fb; --bg-alt:#eef2f8; --card:#ffffff; --card-hover:#f0f4fa;
    --border:#d8e0ec; --text:#1a2332; --text-dim:#5a6b85;
    --accent:#4f46e5; --accent2:#0891b2;
  }
  *{margin:0;padding:0;box-sizing:border-box}
  html{scroll-behavior:smooth}
  body{font-family:-apple-system,BlinkMacSystemFont,'Segoe UI',Roboto,Helvetica,Arial,sans-serif;
    background:var(--bg);color:var(--text);line-height:1.6;overflow-x:hidden;
    transition:background .3s,color .3s}

  /* NAV */
  nav{position:sticky;top:0;z-index:100;background:rgba(6,10,19,.9);
    backdrop-filter:blur(14px);border-bottom:1px solid var(--border);padding:.85rem 2rem}
  [data-theme="light"] nav{background:rgba(245,247,251,.9)}
  .nav-inner{max-width:1300px;margin:0 auto;display:flex;justify-content:space-between;align-items:center;gap:1rem;flex-wrap:wrap}
  .logo{font-weight:800;font-size:1.1rem;letter-spacing:-.5px}
  .logo span{background:var(--grad);-webkit-background-clip:text;background-clip:text;color:transparent}
  .nav-links{display:flex;gap:1rem;flex-wrap:wrap;align-items:center}
  .nav-links a{color:var(--text-dim);text-decoration:none;font-size:.82rem;transition:.2s;font-weight:500}
  .nav-links a:hover{color:var(--accent2)}
  .nav-actions{display:flex;gap:.5rem;align-items:center}
  .icon-btn{background:transparent;border:1px solid var(--border);color:var(--text);
    width:38px;height:38px;border-radius:10px;cursor:pointer;display:flex;
    align-items:center;justify-content:center;font-size:1rem;transition:.2s;position:relative}
  .icon-btn:hover{border-color:var(--accent);background:rgba(99,102,241,.1)}
  .fav-count{position:absolute;top:-6px;right:-6px;background:var(--accent2);color:#000;
    font-size:.65rem;font-weight:800;border-radius:50%;width:18px;height:18px;
    display:flex;align-items:center;justify-content:center;opacity:0;transition:.2s}
  .fav-count.show{opacity:1}

  /* HERO */
  .hero{position:relative;padding:5rem 2rem 3.5rem;text-align:center;overflow:hidden}
  .hero::before{content:'';position:absolute;top:-40%;left:50%;transform:translateX(-50%);
    width:900px;height:900px;border-radius:50%;
    background:radial-gradient(circle,rgba(99,102,241,.18),transparent 65%);pointer-events:none}
  .hero-inner{max-width:860px;margin:0 auto;position:relative}
  .badge{display:inline-block;padding:.4rem 1.1rem;border-radius:999px;
    background:rgba(99,102,241,.15);border:1px solid rgba(99,102,241,.4);
    color:var(--accent2);font-size:.78rem;font-weight:700;letter-spacing:1px;
    margin-bottom:1.2rem;text-transform:uppercase}
  h1{font-size:clamp(1.9rem,4.8vw,3.2rem);font-weight:800;line-height:1.12;
    letter-spacing:-1.5px;margin-bottom:1rem}
  h1 span{background:var(--grad);-webkit-background-clip:text;background-clip:text;color:transparent}
  .hero p{color:var(--text-dim);font-size:1.05rem;max-width:700px;margin:0 auto 1.8rem}
  .cta-row{display:flex;gap:.9rem;justify-content:center;flex-wrap:wrap}
  .btn{padding:.8rem 1.6rem;border-radius:10px;font-weight:700;font-size:.9rem;
    text-decoration:none;transition:.25s;display:inline-block;cursor:pointer;
    border:none;font-family:inherit}
  .btn-primary{background:var(--grad);color:#fff;box-shadow:0 8px 28px rgba(99,102,241,.35)}
  .btn-primary:hover{transform:translateY(-2px);box-shadow:0 14px 40px rgba(99,102,241,.5)}
  .btn-ghost{background:transparent;color:var(--text);border:1px solid var(--border)}
  .btn-ghost:hover{border-color:var(--accent);background:rgba(99,102,241,.1)}

  /* SECTIONS */
  section{max-width:1300px;margin:0 auto;padding:3rem 2rem}
  .section-head{margin-bottom:2rem;max-width:820px}
  .kicker{color:var(--accent2);font-weight:700;font-size:.72rem;letter-spacing:2.5px;
    text-transform:uppercase;margin-bottom:.6rem;display:block}
  h2{font-size:clamp(1.5rem,3.2vw,2.2rem);font-weight:800;letter-spacing:-1px;
    margin-bottom:.8rem;line-height:1.2}
  .section-head p{color:var(--text-dim);font-size:.95rem}

  /* GRID */
  .grid{display:grid;gap:1.1rem}
  .grid-2{grid-template-columns:repeat(auto-fit,minmax(320px,1fr))}
  .grid-3{grid-template-columns:repeat(auto-fit,minmax(280px,1fr))}
  .grid-4{grid-template-columns:repeat(auto-fit,minmax(240px,1fr))}

  /* CARDS */
  .card{background:var(--card);border:1px solid var(--border);border-radius:16px;
    padding:1.5rem;transition:.3s;position:relative;overflow:hidden}
  .card:hover{background:var(--card-hover);border-color:rgba(99,102,241,.45);
    transform:translateY(-4px);box-shadow:0 16px 40px rgba(0,0,0,.45)}
  .card .icon{width:46px;height:46px;border-radius:12px;display:flex;align-items:center;
    justify-content:center;font-size:1.4rem;margin-bottom:.9rem;
    background:rgba(99,102,241,.12);border:1px solid rgba(99,102,241,.3)}
  .card h3{font-size:1.05rem;margin-bottom:.5rem;font-weight:700;letter-spacing:-.3px}
  .card p{color:var(--text-dim);font-size:.88rem;margin-bottom:.6rem}

  /* LINK */
  a.link{color:var(--accent2);text-decoration:none;font-weight:600;font-size:.85rem;
    display:inline-flex;align-items:center;gap:.25rem;transition:.2s;
    border-bottom:1px dashed rgba(34,211,238,.4)}
  a.link:hover{color:#fff;border-bottom-color:var(--accent2)}
  a.link::after{content:'↗';font-size:.7rem}

  /* ACORDEÓN */
  details{background:var(--card);border:1px solid var(--border);border-radius:12px;
    margin-bottom:.6rem;overflow:hidden;transition:.2s}
  details[open]{border-color:rgba(99,102,241,.5);background:var(--card-hover)}
  summary{padding:.9rem 1.1rem;cursor:pointer;font-weight:700;font-size:.9rem;
    display:flex;justify-content:space-between;align-items:center;list-style:none;user-select:none}
  summary::-webkit-details-marker{display:none}
  summary::after{content:'+';font-size:1.2rem;color:var(--accent2);transition:.3s;font-weight:400}
  details[open] summary::after{transform:rotate(45deg)}
  .details-content{padding:0 1.1rem 1.1rem;font-size:.85rem;color:var(--text-dim)}
  .details-content ul{list-style:none;margin-top:.4rem}
  .details-content ul li{padding:.25rem 0 .25rem 1.2rem;position:relative}
  .details-content ul li::before{content:'▸';position:absolute;left:0;color:var(--accent2)}

  /* TABLA COMPARADORA */
  .table-wrap{overflow-x:auto;border-radius:14px;border:1px solid var(--border)}
  table{width:100%;border-collapse:collapse;font-size:.85rem;min-width:800px}
  thead{background:var(--bg-alt)}
  th{padding:.9rem;text-align:left;font-weight:700;font-size:.75rem;
    text-transform:uppercase;letter-spacing:.5px;color:var(--text-dim);
    border-bottom:1px solid var(--border)}
  td{padding:.8rem .9rem;border-bottom:1px solid var(--border);vertical-align:top}
  tbody tr{transition:.2s}
  tbody tr:hover{background:rgba(99,102,241,.06)}
  tbody tr:last-child td{border-bottom:none}
  td strong{color:var(--text);font-weight:700}

  /* METER */
  .meter{display:flex;align-items:center;gap:.5rem}
  .meter-bar{width:70px;height:6px;background:var(--border);border-radius:3px;overflow:hidden;flex-shrink:0}
  .meter-fill{height:100%;background:var(--grad);border-radius:3px;transition:width 1s ease}
  .meter-num{font-size:.78rem;font-weight:800;color:var(--accent2);min-width:36px}

  /* CHART */
  .chart-container{background:var(--card);border:1px solid var(--border);
    border-radius:16px;padding:1.5rem;margin-top:1.2rem;position:relative;height:340px}
  .chart-container h4{font-size:.9rem;margin-bottom:.8rem;color:var(--text);font-weight:700}

  /* CALCULADORA */
  .calc-box{background:var(--card);border:1px solid var(--border);border-radius:20px;
    padding:2rem;margin-top:1.2rem}
  .calc-grid{display:grid;grid-template-columns:1fr 1fr;gap:2rem}
  @media(max-width:700px){.calc-grid{grid-template-columns:1fr}}
  .calc-control label{display:block;font-size:.82rem;color:var(--text-dim);
    margin-bottom:.35rem;font-weight:600}
  .calc-control input[type=range]{width:100%;accent-color:var(--accent2);height:6px;cursor:pointer}
  .calc-control .val{font-weight:800;color:var(--accent2);font-size:.95rem;float:right}
  .calc-result{background:var(--bg-alt);border-radius:14px;padding:1.5rem;
    text-align:center;border:1px solid var(--border)}
  .calc-result .label{font-size:.75rem;color:var(--text-dim);
    text-transform:uppercase;letter-spacing:1px;font-weight:700}
  .calc-result .amount{font-size:2.2rem;font-weight:800;background:var(--grad);
    -webkit-background-clip:text;background-clip:text;color:transparent;margin:.4rem 0}
  .calc-result .sub{font-size:.78rem;color:var(--text-dim)}

  /* 100 FORMAS LISTA */
  .formas-cat{margin-bottom:1.5rem}
  .formas-cat h3{font-size:1rem;font-weight:800;margin-bottom:.6rem;
    color:var(--accent2);letter-spacing:-.3px}
  .formas-lista{display:grid;grid-template-columns:repeat(auto-fill,minmax(260px,1fr));gap:.5rem}
  .forma-item{background:var(--card);border:1px solid var(--border);
    border-radius:10px;padding:.7rem .9rem;font-size:.82rem;
    color:var(--text-dim);transition:.2s;display:flex;justify-content:space-between;align-items:center;gap:.5rem}
  .forma-item:hover{background:var(--card-hover);border-color:rgba(99,102,241,.4);color:var(--text)}
  .forma-item a{color:var(--accent2);font-weight:600;text-decoration:none;font-size:.78rem;white-space:nowrap}
  .forma-item a:hover{color:#fff}
  .forma-item.hidden{display:none}
  .forma-content{flex:1;display:flex;flex-direction:column;gap:.2rem}
  .forma-tags{display:flex;gap:.3rem;flex-wrap:wrap;margin-top:.2rem}
  .mini-tag{font-size:.6rem;padding:.1rem .4rem;border-radius:4px;
    background:rgba(99,102,241,.12);color:var(--accent2);font-weight:700;
    text-transform:uppercase;letter-spacing:.3px}

  /* BUSCADOR / FILTROS */
  .filters-bar{display:flex;gap:.7rem;flex-wrap:wrap;margin-bottom:1.5rem;
    padding:1rem;background:var(--card);border:1px solid var(--border);border-radius:14px;align-items:center}
  .filters-bar input, .filters-bar select{
    background:var(--bg-alt);border:1px solid var(--border);color:var(--text);
    padding:.6rem .9rem;border-radius:9px;font-family:inherit;font-size:.85rem;outline:none;transition:.2s}
  .filters-bar input:focus, .filters-bar select:focus{border-color:var(--accent2)}
  .filters-bar input{flex:1;min-width:180px}
  .filters-bar .count{margin-left:auto;font-size:.8rem;color:var(--text-dim);font-weight:600}
  .filters-bar .count strong{color:var(--accent2)}

  /* HIGHLIGHT */
  .highlight{background:linear-gradient(135deg,rgba(99,102,241,.12),rgba(34,211,238,.06));
    border:1px solid rgba(99,102,241,.35);border-radius:20px;padding:2rem;
    margin-top:1.2rem;text-align:center}
  .highlight h3{font-size:1.25rem;margin-bottom:.7rem;letter-spacing:-.5px}
  .highlight p{color:var(--text-dim);max-width:620px;margin:0 auto .8rem;font-size:.9rem}
  .highlight .big{font-size:2rem;font-weight:800;background:var(--grad);
    -webkit-background-clip:text;background-clip:text;color:transparent;display:block;margin:.4rem 0}

  /* TOOL ROW */
  .tool-row{display:flex;justify-content:space-between;align-items:flex-start;
    gap:.8rem;padding:.7rem 0;border-bottom:1px solid var(--border)}
  .tool-row:last-child{border-bottom:none}
  .tool-info{flex:1}
  .tool-name{font-weight:700;font-size:.88rem;margin-bottom:.1rem}
  .tool-desc{color:var(--text-dim);font-size:.78rem;line-height:1.5}
  .tag{font-size:.65rem;font-weight:800;padding:.2rem .5rem;border-radius:6px;
    white-space:nowrap;text-transform:uppercase;letter-spacing:.4px;flex-shrink:0;margin-top:.1rem}
  .tag-free{background:rgba(16,185,129,.15);color:var(--green);border:1px solid rgba(16,185,129,.35)}
  .tag-limit{background:rgba(245,158,11,.15);color:var(--amber);border:1px solid rgba(245,158,11,.35)}

  /* FOOTER */
  footer{border-top:1px solid var(--border);padding:2.2rem 2rem;text-align:center;
    color:var(--text-dim);font-size:.82rem}
  footer a{color:var(--accent2);text-decoration:none}
  .footer-links{display:flex;justify-content:center;gap:1.2rem;flex-wrap:wrap;
    margin-bottom:.8rem;font-size:.78rem}

  /* REVEAL */
  .reveal{opacity:0;transform:translateY(30px);transition:.8s cubic-bezier(.2,.8,.2,1)}
  .reveal.visible{opacity:1;transform:none}

  /* ============ NUEVOS ESTILOS AÑADIDOS ============ */

  /* BOTÓN FAVORITO ⭐ */
  .fav-btn{position:absolute;top:.8rem;right:.8rem;background:transparent;
    border:none;font-size:1.1rem;cursor:pointer;opacity:.35;transition:.2s;
    z-index:5;padding:.2rem;line-height:1}
  .fav-btn:hover{opacity:1;transform:scale(1.15)}
  .fav-btn.active{opacity:1;filter:drop-shadow(0 0 6px rgba(250,204,21,.6))}

  /* DRAWER FAVORITOS */
  .drawer{position:fixed;top:0;right:0;width:380px;max-width:100vw;height:100vh;
    background:var(--bg-alt);border-left:1px solid var(--border);z-index:200;
    transform:translateX(100%);transition:transform .35s cubic-bezier(.2,.8,.2,1);
    display:flex;flex-direction:column;box-shadow:-20px 0 50px rgba(0,0,0,.4)}
  .drawer.open{transform:translateX(0)}
  .drawer-header{padding:1.2rem;border-bottom:1px solid var(--border);
    display:flex;justify-content:space-between;align-items:center}
  .drawer-header h3{font-size:1rem;font-weight:800}
  .drawer-close{background:transparent;border:none;color:var(--text);font-size:1.4rem;
    cursor:pointer;line-height:1;padding:.2rem}
  .drawer-body{flex:1;overflow-y:auto;padding:1rem}
  .drawer-empty{color:var(--text-dim);font-size:.85rem;text-align:center;padding:2rem 1rem;line-height:1.6}
  .fav-entry{background:var(--card);border:1px solid var(--border);border-radius:10px;
    padding:.8rem 1rem;margin-bottom:.6rem;font-size:.85rem}
  .fav-entry .fav-title{font-weight:700;margin-bottom:.2rem}
  .fav-entry .fav-type{font-size:.7rem;color:var(--accent2);text-transform:uppercase;
    font-weight:700;letter-spacing:.5px;margin-bottom:.3rem}
  .fav-entry .fav-actions{display:flex;gap:.5rem;margin-top:.4rem}
  .fav-entry button{background:transparent;border:1px solid var(--border);color:var(--text-dim);
    font-size:.72rem;padding:.25rem .55rem;border-radius:6px;cursor:pointer;font-family:inherit}
  .fav-entry button:hover{border-color:var(--red);color:var(--red)}
  .fav-entry a{color:var(--accent2);text-decoration:none;font-size:.75rem}
  .fav-entry a:hover{text-decoration:underline}

  /* QUIZ */
  .quiz-box{background:var(--card);border:1px solid var(--border);border-radius:20px;
    padding:2rem;margin-top:1.2rem}
  .quiz-progress{height:6px;background:var(--border);border-radius:3px;margin-bottom:1.5rem;overflow:hidden}
  .quiz-progress-fill{height:100%;background:var(--grad);width:0%;transition:width .4s}
  .quiz-step-label{font-size:.72rem;color:var(--accent2);font-weight:800;
    text-transform:uppercase;letter-spacing:1px;margin-bottom:.4rem}
  .quiz-question{font-size:1.15rem;font-weight:800;margin-bottom:1.2rem;line-height:1.35}
  .quiz-options{display:grid;gap:.6rem}
  .quiz-option{background:var(--bg-alt);border:1px solid var(--border);
    border-radius:10px;padding:.9rem 1.1rem;cursor:pointer;font-family:inherit;
    font-size:.9rem;color:var(--text);text-align:left;transition:.2s;font-weight:500}
  .quiz-option:hover{border-color:var(--accent2);background:rgba(34,211,238,.08);transform:translateX(4px)}
  .quiz-result{text-align:center;padding:1rem 0}
  .quiz-result .rec-icon{font-size:2.5rem;margin-bottom:.5rem}
  .quiz-result h3{font-size:1.3rem;margin-bottom:.5rem;color:var(--accent2)}
  .quiz-result p{color:var(--text-dim);font-size:.9rem;max-width:520px;margin:0 auto 1.2rem}
  .quiz-result .btn{margin:.3rem}

  /* PROMPTS COPIABLES */
  .prompt-block{background:var(--bg-alt);border:1px solid var(--border);
    border-radius:10px;padding:.8rem;margin-bottom:.6rem;position:relative}
  .prompt-block .prompt-label{font-size:.7rem;font-weight:800;color:var(--accent2);
    text-transform:uppercase;letter-spacing:.5px;margin-bottom:.4rem;display:flex;
    justify-content:space-between;align-items:center}
  .prompt-block .prompt-text{font-family:ui-monospace,Menlo,monospace;
    font-size:.78rem;line-height:1.5;color:var(--text);white-space:pre-wrap;word-break:break-word}
  .copy-btn{background:rgba(99,102,241,.15);border:1px solid rgba(99,102,241,.4);
    color:var(--accent2);font-size:.68rem;font-weight:700;padding:.2rem .5rem;
    border-radius:6px;cursor:pointer;font-family:inherit;text-transform:uppercase;
    letter-spacing:.4px}
  .copy-btn:hover{background:rgba(99,102,241,.3);color:#fff}
  .copy-btn.copied{background:rgba(16,185,129,.2);border-color:rgba(16,185,129,.5);color:var(--green)}

  /* ROADMAP */
  .roadmap{background:var(--card);border:1px solid var(--border);border-radius:20px;
    padding:2rem;margin-top:1.2rem}
  .roadmap-progress{height:8px;background:var(--border);border-radius:4px;
    margin-bottom:1.5rem;overflow:hidden}
  .roadmap-progress-fill{height:100%;background:var(--grad);width:0%;transition:width .4s}
  .roadmap-stats{display:flex;justify-content:space-between;margin-bottom:1rem;
    font-size:.82rem;color:var(--text-dim)}
  .roadmap-stats strong{color:var(--accent2)}
  .roadmap-list{display:grid;gap:.5rem}
  .roadmap-item{display:flex;gap:.75rem;align-items:flex-start;
    background:var(--bg-alt);border:1px solid var(--border);border-radius:10px;
    padding:.8rem 1rem;transition:.2s}
  .roadmap-item:hover{border-color:rgba(99,102,241,.4)}
  .roadmap-item.done{opacity:.55;background:rgba(16,185,129,.05);border-color:rgba(16,185,129,.25)}
  .roadmap-item input[type=checkbox]{accent-color:var(--green);width:18px;height:18px;
    margin-top:.2rem;cursor:pointer;flex-shrink:0}
  .roadmap-item .rm-day{font-size:.7rem;color:var(--accent2);font-weight:800;
    text-transform:uppercase;letter-spacing:.5px;margin-bottom:.15rem}
  .roadmap-item .rm-title{font-size:.88rem;font-weight:700}
  .roadmap-item .rm-desc{font-size:.78rem;color:var(--text-dim);margin-top:.15rem}
  .roadmap-item.done .rm-title{text-decoration:line-through}

  /* DEMO IA */
  .demo-box{background:var(--card);border:1px solid var(--border);border-radius:20px;
    padding:1.8rem;margin-top:1.2rem}
  .demo-form{display:flex;gap:.6rem;flex-wrap:wrap;margin-bottom:1rem}
  .demo-form textarea{flex:1;min-width:220px;min-height:60px;background:var(--bg-alt);
    border:1px solid var(--border);color:var(--text);border-radius:10px;
    padding:.7rem;font-family:inherit;font-size:.88rem;resize:vertical;outline:none}
  .demo-form textarea:focus{border-color:var(--accent2)}
  .demo-form select{background:var(--bg-alt);border:1px solid var(--border);
    color:var(--text);border-radius:10px;padding:.6rem;font-family:inherit;font-size:.82rem}
  .demo-output{background:var(--bg-alt);border:1px solid var(--border);
    border-radius:10px;padding:1rem;font-size:.85rem;line-height:1.6;
    min-height:80px;white-space:pre-wrap;word-break:break-word;color:var(--text)}
  .demo-output.loading{color:var(--text-dim);font-style:italic}
  .demo-hint{font-size:.72rem;color:var(--text-dim);margin-top:.6rem}

  /* FAQ / GLOSARIO */
  .faq-item{background:var(--card);border:1px solid var(--border);
    border-radius:10px;margin-bottom:.5rem;overflow:hidden}
  .faq-item summary{padding:.85rem 1.1rem;font-size:.88rem}
  .faq-item .details-content{font-size:.85rem}

  /* ERRORES COMUNES */
  .error-card{background:var(--card);border:1px solid var(--border);
    border-left:3px solid var(--red);border-radius:10px;padding:1rem 1.2rem}
  .error-card h4{font-size:.9rem;font-weight:700;margin-bottom:.3rem;color:var(--red)}
  .error-card p{font-size:.82rem;color:var(--text-dim)}

  /* PLANTILLAS */
  .plantilla-card{display:flex;justify-content:space-between;align-items:center;
    gap:1rem;background:var(--card);border:1px solid var(--border);
    border-radius:12px;padding:1rem 1.2rem;margin-bottom:.6rem;transition:.2s}
  .plantilla-card:hover{border-color:rgba(99,102,241,.4);background:var(--card-hover)}
  .plantilla-info h4{font-size:.9rem;font-weight:700;margin-bottom:.15rem}
  .plantilla-info p{font-size:.78rem;color:var(--text-dim)}
  .dl-btn{background:var(--grad);color:#fff;border:none;padding:.5rem 1rem;
    border-radius:8px;font-weight:700;font-size:.78rem;cursor:pointer;
    font-family:inherit;transition:.2s;white-space:nowrap}
  .dl-btn:hover{transform:translateY(-1px);box-shadow:0 6px 20px rgba(99,102,241,.4)}

  /* TOAST */
  .toast{position:fixed;bottom:2rem;left:50%;transform:translateX(-50%) translateY(100px);
    background:var(--green);color:#fff;padding:.8rem 1.5rem;border-radius:10px;
    font-weight:700;font-size:.85rem;z-index:999;transition:.35s;box-shadow:0 10px 30px rgba(0,0,0,.4)}
  .toast.show{transform:translateX(-50%) translateY(0)}

  @media(max-width:640px){
    .hero{padding:3.5rem 1.2rem 2.5rem}
    section{padding:2.2rem 1.2rem}
    nav{padding:.75rem 1.2rem}
    .nav-links{display:none}
    .chart-container{height:280px}
    .calc-result .amount{font-size:1.8rem}
    .drawer{width:100vw}
  }
</style>
</head>
<body>

<nav>
  <div class="nav-inner">
    <div class="logo">IA<span>·</span>Hub</div>
    <div class="nav-links">
      <a href="#apis">APIs</a>
      <a href="#demo">Demo IA</a>
      <a href="#modelos">Modelos</a>
      <a href="#quiz">Quiz</a>
      <a href="#100formas">100 formas</a>
      <a href="#comparador">Comparador</a>
      <a href="#calculadora">Calculadora</a>
      <a href="#roadmap">Roadmap</a>
      <a href="#graficos">Gráficos</a>
      <a href="#faq">FAQ</a>
    </div>
    <div class="nav-actions">
      <button class="icon-btn" id="themeBtn" title="Cambiar tema">🌙</button>
      <button class="icon-btn" id="favOpenBtn" title="Mis favoritos">⭐<span class="fav-count" id="favCount">0</span></button>
    </div>
  </div>
</nav>

<header class="hero">
  <div class="hero-inner">
    <span class="badge">Hub completo · 2026</span>
    <h1>El centro de <span>negocios con IA gratis</span>: modelos, 100 formas y herramientas</h1>
    <p>Todo en uno: los modelos de negocio que funcionan sin tokens, 100 formas concretas de monetizar, enlaces directos a las APIs gratuitas, demo de IA en vivo, calculadora, comparador, roadmap de 30 días y quiz recomendador.</p>
    <div class="cta-row">
      <a href="#quiz" class="btn btn-primary">Hacer el quiz →</a>
      <a href="#100formas" class="btn btn-ghost">Ver las 100 formas</a>
    </div>
  </div>
</header>

<!-- ===== SECCIÓN: APIS GRATUITAS (ENLACES) ===== -->
<section id="apis" class="reveal">
  <div class="section-head">
    <span class="kicker">La base · Herramientas</span>
    <h2>APIs de texto 100% gratuitas, sin clave y sin tokens</h2>
    <p>Estas son las puertas de entrada para construir tus productos sin pagar nada. Haz clic en cada una para acceder directamente a su página oficial y empezar a usarla.</p>
  </div>

  <div class="grid grid-2">
    <div class="card">
      <div class="icon">⚡</div>
      <h3>Puter.js</h3>
      <p>Acceso ilimitado a GPT, Claude, Mistral y Gemini desde el navegador. Sin clave API, sin registro, sin coste para el desarrollador.</p>
      <a href="https://developer.puter.com/" target="_blank" class="link">developer.puter.com</a>
    </div>
    <div class="card">
      <div class="icon">🌸</div>
      <h3>Pollinations.ai</h3>
      <p>Generación de texto gratuita, sin clave API y sin límites de tasa. Endpoint compatible con OpenAI. La opción más sencilla para empezar.</p>
      <a href="https://pollinations.ai/" target="_blank" class="link">pollinations.ai</a>
    </div>
    <div class="card">
      <div class="icon">🔑</div>
      <h3>KeylessAI</h3>
      <p>Endpoint compatible con OpenAI sin autenticación. Solo cambias la URL base y funciona con cualquier cliente. Ideal para agentes y scripts.</p>
      <a href="https://keylessai.thryx.workers.dev/v1" target="_blank" class="link">keylessai.thryx.workers.dev/v1</a>
    </div>
    <div class="card">
      <div class="icon">🌐</div>
      <h3>OpenRouter</h3>
      <p>Catálogo con 20+ modelos gratuitos (DeepSeek, Llama, etc.) con una sola clave API. Límite generoso para empezar.</p>
      <a href="https://openrouter.ai/" target="_blank" class="link">openrouter.ai</a>
    </div>
    <div class="card">
      <div class="icon">🚀</div>
      <h3>Groq</h3>
      <p>Inferencia ultrarrápida con modelos como GPT-OSS-120B. Plan gratuito: 30 RPM, 1.000 peticiones/día. Sin tarjeta de crédito.</p>
      <a href="https://console.groq.com/" target="_blank" class="link">console.groq.com</a>
    </div>
    <div class="card">
      <div class="icon">☁️</div>
      <h3>Cloudflare Workers AI</h3>
      <p>10.000 “Neurons” gratis al día. Modelos Llama, Gemma, Whisper. Sin tarjeta, directamente en el edge.</p>
      <a href="https://developers.cloudflare.com/workers-ai/" target="_blank" class="link">developers.cloudflare.com/workers-ai</a>
    </div>
  </div>

  <div style="margin-top:1.5rem">
    <details>
      <summary>🔍 Detalles ampliados de las APIs clave (límites, modelos, casos de uso)</summary>
      <div class="details-content">
        <p><strong>Puter.js:</strong> Modelos como GPT-6, GPT-5.4 Nano, Claude, Gemini y Mistral. El coste recae en el usuario final, no en el desarrollador. Requiere incluir un script CDN o instalar el módulo npm.</p>
        <p><strong>Pollinations:</strong> Endpoint de texto: <code>https://text.pollinations.ai/openai</code>. Modelos: OpenAI, Mistral, Gemini. Sin registro ni clave. Puede haber ralentizaciones en horas punta.</p>
        <p><strong>KeylessAI:</strong> URL base: <code>https://keylessai.thryx.workers.dev/v1</code>. Usa una clave ficticia como “not-needed”. Añade failover y filtrado de anuncios. Límite de ~100.000 peticiones/día en Cloudflare Workers.</p>
        <p><strong>Groq:</strong> Plan gratuito muy generoso para desarrollo. Modelos como Llama 3, Mixtral, Gemma. Ideal para prototipos que necesitan velocidad.</p>
      </div>
    </details>
  </div>
</section>

<!-- ===== NUEVA SECCIÓN: DEMO IA EN VIVO ===== -->
<section id="demo" class="reveal">
  <div class="section-head">
    <span class="kicker">Nuevo · Prueba la IA ahora</span>
    <h2>Demo de IA en vivo (sin clave, sin tokens)</h2>
    <p>Esta demo usa <a href="https://pollinations.ai/" target="_blank" class="link">Pollinations.ai</a>, que no requiere clave API ni registro. Escribe un prompt y comprueba por ti mismo que las APIs gratuitas funcionan. Es la misma tecnología que puedes usar para automatizar tu negocio.</p>
  </div>

  <div class="demo-box">
    <div class="demo-form">
      <textarea id="demoPrompt" placeholder="Ejemplo: Escribe un esquema de 5 capítulos para un micro-eBook sobre 'Cómo usar IA para freelancers'..."></textarea>
      <select id="demoModel">
        <option value="openai">OpenAI</option>
        <option value="mistral">Mistral</option>
      </select>
      <button class="btn btn-primary" id="demoBtn">Generar →</button>
    </div>
    <div class="demo-output" id="demoOutput">La respuesta de la IA aparecerá aquí...</div>
    <p class="demo-hint">💡 Si el servicio está saturado, prueba de nuevo en unos segundos. Esta demo llama directamente a la API pública de Pollinations.</p>
  </div>
</section>

<!-- ===== SECCIÓN: MODELOS DE NEGOCIO (con prompts copiables + favoritos) ===== -->
<section id="modelos" class="reveal">
  <div class="section-head">
    <span class="kicker">Paso 1 · Elige tu modelo</span>
    <h2>Modelos de negocio con IA gratuita y sin tokens</h2>
    <p>Cada modelo incluye su nivel de automatización, las herramientas que necesitas, <strong>prompts listos para copiar</strong> y un enlace directo a la plataforma de venta o creación. Pulsa la ⭐ para guardarlo en favoritos.</p>
  </div>

  <div class="grid grid-3">
    <div class="card" data-fav-id="modelo-micro-ebooks">
      <button class="fav-btn" data-fav-id="modelo-micro-ebooks" data-fav-type="Modelo" data-fav-title="Micro-eBooks y guías" data-fav-link="https://gumroad.com/">⭐</button>
      <div class="icon">📚</div>
      <h3>Micro-eBooks y guías</h3>
      <p>Guías de 20-40 páginas sobre un nicho hiperespecífico. Se venden en Gumroad de forma automatizada.</p>
      <div class="meter"><div class="meter-bar"><div class="meter-fill" style="width:95%"></div></div><span class="meter-num">95%</span></div>
      <a href="https://gumroad.com/" target="_blank" class="link" style="margin-top:.5rem;display:inline-flex">Gumroad →</a>
      <details style="margin-top:.8rem">
        <summary>📋 Prompts listos para copiar</summary>
        <div class="details-content">
          <div class="prompt-block">
            <div class="prompt-label">Prompt 1 · Esquema del eBook<button class="copy-btn">Copiar</button></div>
            <div class="prompt-text">Actúa como experto en [nicho]. Genera un esquema de 8 capítulos para un eBook de 30 páginas titulado "[título]" dirigido a [público objetivo]. Para cada capítulo incluye: título, 3 puntos clave y una acción práctica.</div>
          </div>
          <div class="prompt-block">
            <div class="prompt-label">Prompt 2 · Capítulo completo<button class="copy-btn">Copiar</button></div>
            <div class="prompt-text">Escribe el capítulo "[título del capítulo]" de mi eBook para [público]. Tono cercano y profesional, 1.200 palabras, con ejemplos concretos y una lista de 5 pasos accionables al final.</div>
          </div>
          <div class="prompt-block">
            <div class="prompt-label">Prompt 3 · Landing de venta<button class="copy-btn">Copiar</button></div>
            <div class="prompt-text">Redacta una landing page de venta para mi eBook "[título]" dirigido a [público]. Incluye: titular, subtítulo, 3 beneficios, 3 objeciones con respuesta, llamada a la acción y garantía.</div>
          </div>
        </div>
      </details>
    </div>

    <div class="card" data-fav-id="modelo-newsletters">
      <button class="fav-btn" data-fav-id="modelo-newsletters" data-fav-type="Modelo" data-fav-title="Newsletters de nicho" data-fav-link="https://substack.com/">⭐</button>
      <div class="icon">📧</div>
      <h3>Newsletters de nicho</h3>
      <p>Boletines especializados con suscripción gratuita o de pago. Contenido generado por IA y enviado automáticamente.</p>
      <div class="meter"><div class="meter-bar"><div class="meter-fill" style="width:90%"></div></div><span class="meter-num">90%</span></div>
      <a href="https://substack.com/" target="_blank" class="link" style="margin-top:.5rem;display:inline-flex">Substack →</a>
      <details style="margin-top:.8rem">
        <summary>📋 Prompts listos para copiar</summary>
        <div class="details-content">
          <div class="prompt-block">
            <div class="prompt-label">Prompt 1 · Primer número<button class="copy-btn">Copiar</button></div>
            <div class="prompt-text">Genera el primer número de una newsletter semanal sobre [tema] dirigida a [público]. Estructura: asunto, introducción personal, 3 noticias breves con enlace, un consejo práctico y un cierre con llamada a la acción.</div>
          </div>
          <div class="prompt-block">
            <div class="prompt-label">Prompt 2 · Calendario editorial<button class="copy-btn">Copiar</button></div>
            <div class="prompt-text">Crea un calendario editorial de 12 semanas para una newsletter sobre [tema]. Para cada semana indica: título del envío, ángulo principal y tipo de contenido (análisis, tutorial, entrevista, curaduría).</div>
          </div>
        </div>
      </details>
    </div>

    <div class="card" data-fav-id="modelo-descripciones">
      <button class="fav-btn" data-fav-id="modelo-descripciones" data-fav-type="Modelo" data-fav-title="Descripciones de productos" data-fav-link="https://www.shopify.com/">⭐</button>
      <div class="icon">🛒</div>
      <h3>Descripciones de productos</h3>
      <p>Paquetes de 20-50 descripciones para tiendas online. Se venden como servicio puntual o suscripción.</p>
      <div class="meter"><div class="meter-bar"><div class="meter-fill" style="width:90%"></div></div><span class="meter-num">90%</span></div>
      <a href="https://www.shopify.com/" target="_blank" class="link" style="margin-top:.5rem;display:inline-flex">Guía Shopify →</a>
      <details style="margin-top:.8rem">
        <summary>📋 Prompts listos para copiar</summary>
        <div class="details-content">
          <div class="prompt-block">
            <div class="prompt-label">Prompt 1 · Descripción SEO<button class="copy-btn">Copiar</button></div>
            <div class="prompt-text">Escribe una descripción de producto para [producto] de la categoría [categoría]. Incluye: titular atractivo, 100 palabras persuasivas, 5 bullets con beneficios, palabras clave: [keywords] y llamada a la acción final.</div>
          </div>
          <div class="prompt-block">
            <div class="prompt-label">Prompt 2 · Paquete en lote<button class="copy-btn">Copiar</button></div>
            <div class="prompt-text">A continuación te paso una lista de 10 productos de mi tienda de [nicho]. Para cada uno genera una descripción de 80 palabras con tono [tono]. Formato: "Producto: [nombre] | Descripción: [texto]".</div>
          </div>
        </div>
      </details>
    </div>

    <div class="card" data-fav-id="modelo-seo">
      <button class="fav-btn" data-fav-id="modelo-seo" data-fav-type="Modelo" data-fav-title="Contenido SEO para blogs" data-fav-link="https://koala.sh/">⭐</button>
      <div class="icon">📝</div>
      <h3>Contenido SEO para blogs</h3>
      <p>Artículos optimizados que generan tráfico y se monetizan con afiliados o publicidad.</p>
      <div class="meter"><div class="meter-bar"><div class="meter-fill" style="width:85%"></div></div><span class="meter-num">85%</span></div>
      <a href="https://koala.sh/" target="_blank" class="link" style="margin-top:.5rem;display:inline-flex">KoalaWriter →</a>
      <details style="margin-top:.8rem">
        <summary>📋 Prompts listos para copiar</summary>
        <div class="details-content">
          <div class="prompt-block">
            <div class="prompt-label">Prompt 1 · Artículo SEO completo<button class="copy-btn">Copiar</button></div>
            <div class="prompt-text">Escribe un artículo SEO de 1.800 palabras sobre "[keyword]" para [público]. Estructura: H1 con keyword, introducción con gancho, 5 H2 con H3 anidados, tabla comparativa, FAQ final y conclusión con CTA. Densidad de keyword: 1,5%.</div>
          </div>
          <div class="prompt-block">
            <div class="prompt-label">Prompt 2 · Análisis SERP<button class="copy-btn">Copiar</button></div>
            <div class="prompt-text">Analiza la intención de búsqueda de la keyword "[keyword]" y dime: 1) qué tipo de contenido posiciona (guía, lista, comparativa), 2) los 5 subtemas que no pueden faltar, 3) 3 ángulos diferenciadores que podría usar.</div>
          </div>
        </div>
      </details>
    </div>

    <div class="card" data-fav-id="modelo-recepcionista">
      <button class="fav-btn" data-fav-id="modelo-recepcionista" data-fav-type="Modelo" data-fav-title="Recepcionista AI para negocios" data-fav-link="https://aiindigo.com/">⭐</button>
      <div class="icon">📞</div>
      <h3>Recepcionista AI para negocios</h3>
      <p>Agentes de voz/chat que contestan llamadas, califican clientes y agendan citas para negocios locales.</p>
      <div class="meter"><div class="meter-bar"><div class="meter-fill" style="width:88%"></div></div><span class="meter-num">88%</span></div>
      <a href="https://aiindigo.com/" target="_blank" class="link" style="margin-top:.5rem;display:inline-flex">Guía AI Indigo →</a>
      <details style="margin-top:.8rem">
        <summary>📋 Prompts listos para copiar</summary>
        <div class="details-content">
          <div class="prompt-block">
            <div class="prompt-label">Prompt 1 · Script de recepción<button class="copy-btn">Copiar</button></div>
            <div class="prompt-text">Escribe un script de recepción telefónica para [tipo de negocio] que: salude, identifique la necesidad del cliente, ofrezca 2 opciones de cita y cierre confirmando los datos. Tono [cercano/profesional], máximo 200 palabras.</div>
          </div>
          <div class="prompt-block">
            <div class="prompt-label">Prompt 2 · Preguntas de calificación<button class="copy-btn">Copiar</button></div>
            <div class="prompt-text">Diseña 6 preguntas de calificación de leads para [tipo de negocio] que permitan saber si el cliente es potencial o no. Para cada pregunta indica qué respuesta lo descarta y cuál lo confirma como lead cualificado.</div>
          </div>
        </div>
      </details>
    </div>

    <div class="card" data-fav-id="modelo-leads">
      <button class="fav-btn" data-fav-id="modelo-leads" data-fav-type="Modelo" data-fav-title="Generación de leads B2B" data-fav-link="https://www.apollo.io/">⭐</button>
      <div class="icon">🎯</div>
      <h3>Generación de leads B2B</h3>
      <p>Encuentra emails verificados y datos de contacto para equipos de ventas usando IA y automatización.</p>
      <div class="meter"><div class="meter-bar"><div class="meter-fill" style="width:85%"></div></div><span class="meter-num">85%</span></div>
      <a href="https://www.apollo.io/" target="_blank" class="link" style="margin-top:.5rem;display:inline-flex">Apollo →</a>
      <details style="margin-top:.8rem">
        <summary>📋 Prompts listos para copiar</summary>
        <div class="details-content">
          <div class="prompt-block">
            <div class="prompt-label">Prompt 1 · Email en frío<button class="copy-btn">Copiar</button></div>
            <div class="prompt-text">Escribe un email en frío de máximo 100 palabras para [cargo] de empresas del sector [sector]. Debe: referenciar un dolor específico, presentar mi solución en 1 frase, incluir una prueba social y un CTA suave. Tono [directo/cercano].</div>
          </div>
          <div class="prompt-block">
            <div class="prompt-label">Prompt 2 · Secuencia de follow-up<button class="copy-btn">Copiar</button></div>
            <div class="prompt-text">Crea una secuencia de 4 emails de follow-up para prospectos B2B que no respondieron. Cada email debe tener un ángulo distinto (recordatorio, caso de éxito, valor educativo, ruptura). Máximo 80 palabras cada uno.</div>
          </div>
        </div>
      </details>
    </div>

    <div class="card" data-fav-id="modelo-youtube">
      <button class="fav-btn" data-fav-id="modelo-youtube" data-fav-type="Modelo" data-fav-title="Canales de YouTube sin rostro" data-fav-link="https://invideo.io/">⭐</button>
      <div class="icon">🎬</div>
      <h3>Canales de YouTube sin rostro</h3>
      <p>Vídeos educativos o de nicho generados con IA (voz, guion, edición) y monetizados con ads.</p>
      <div class="meter"><div class="meter-bar"><div class="meter-fill" style="width:80%"></div></div><span class="meter-num">80%</span></div>
      <a href="https://invideo.io/" target="_blank" class="link" style="margin-top:.5rem;display:inline-flex">InVideo AI →</a>
      <details style="margin-top:.8rem">
        <summary>📋 Prompts listos para copiar</summary>
        <div class="details-content">
          <div class="prompt-block">
            <div class="prompt-label">Prompt 1 · Guion de vídeo<button class="copy-btn">Copiar</button></div>
            <div class="prompt-text">Escribe un guion de 8 minutos para un vídeo de YouTube sobre "[tema]" para [público]. Incluye: hook de 15s, introducción, 4 secciones con transiciones, ejemplos concretos y cierre con CTA al canal. Tono [educativo/entretenido].</div>
          </div>
          <div class="prompt-block">
            <div class="prompt-label">Prompt 2 · Títulos y miniaturas<button class="copy-btn">Copiar</button></div>
            <div class="prompt-text">Propón 10 títulos de YouTube para un vídeo sobre "[tema]" con CTR alto (curiosidad, número, beneficio). Para cada título sugiere una idea visual de miniatura con texto de 3 palabras máximo.</div>
          </div>
        </div>
      </details>
    </div>

    <div class="card" data-fav-id="modelo-miniaturas">
      <button class="fav-btn" data-fav-id="modelo-miniaturas" data-fav-type="Modelo" data-fav-title="Diseño de miniaturas" data-fav-link="https://www.canva.com/">⭐</button>
      <div class="icon">🎨</div>
      <h3>Diseño de miniaturas</h3>
      <p>Miniaturas de alto CTR para youtubers usando IA generativa. Servicio recurrente y muy demandado.</p>
      <div class="meter"><div class="meter-bar"><div class="meter-fill" style="width:82%"></div></div><span class="meter-num">82%</span></div>
      <a href="https://www.canva.com/" target="_blank" class="link" style="margin-top:.5rem;display:inline-flex">Canva →</a>
      <details style="margin-top:.8rem">
        <summary>📋 Prompts listos para copiar</summary>
        <div class="details-content">
          <div class="prompt-block">
            <div class="prompt-label">Prompt 1 · Concepto de miniatura<button class="copy-btn">Copiar</button></div>
            <div class="prompt-text">Genera 5 conceptos de miniatura para un vídeo de YouTube titulado "[título]". Para cada concepto describe: composición visual, emoción facial, texto corto (máx 3 palabras), colores dominantes y por qué tendría CTR alto.</div>
          </div>
        </div>
      </details>
    </div>

    <div class="card" data-fav-id="modelo-cursos">
      <button class="fav-btn" data-fav-id="modelo-cursos" data-fav-type="Modelo" data-fav-title="Cursos online con IA" data-fav-link="https://hotmart.com/">⭐</button>
      <div class="icon">🎓</div>
      <h3>Cursos online con IA</h3>
      <p>Cursos creados con IA (guion, diapositivas, voz) sobre temas demandados. Se venden en plataformas como Hotmart.</p>
      <div class="meter"><div class="meter-bar"><div class="meter-fill" style="width:85%"></div></div><span class="meter-num">85%</span></div>
      <a href="https://hotmart.com/" target="_blank" class="link" style="margin-top:.5rem;display:inline-flex">Hotmart →</a>
      <details style="margin-top:.8rem">
        <summary>📋 Prompts listos para copiar</summary>
        <div class="details-content">
          <div class="prompt-block">
            <div class="prompt-label">Prompt 1 · Programa del curso<button class="copy-btn">Copiar</button></div>
            <div class="prompt-text">Diseña el programa de un curso online titulado "[título]" dirigido a [público]. Incluye 6 módulos con 4 lecciones cada uno, objetivos de aprendizaje, proyecto final y duración estimada. Formato: módulo, título, lecciones con descripción breve.</div>
          </div>
        </div>
      </details>
    </div>
  </div>
</section>

<!-- ===== NUEVA SECCIÓN: QUIZ RECOMENDADOR ===== -->
<section id="quiz" class="reveal">
  <div class="section-head">
    <span class="kicker">Nuevo · Herramienta</span>
    <h2>¿Qué modelo de negocio encaja contigo?</h2>
    <p>Responde 5 preguntas rápidas y te recomendamos el modelo con IA que mejor se adapta a tu tiempo, tus preferencias y tu tolerancia a hablar con clientes.</p>
  </div>

  <div class="quiz-box" id="quizBox">
    <!-- Contenido dinámico desde JS -->
  </div>
</section>

<!-- ===== SECCIÓN: 100 FORMAS DE GANAR DINERO (con buscador, filtros y favoritos) ===== -->
<section id="100formas" class="reveal">
  <div class="section-head">
    <span class="kicker">Paso 2 · Monetización</span>
    <h2>100 formas de ganar dinero con IA (gratis y sin tokens)</h2>
    <p>Organizadas por categorías. Usa el buscador y los filtros para encontrar la que mejor encaja contigo. Cada una incluye un enlace directo y un botón ⭐ para guardarla en favoritos.</p>
  </div>

  <div class="filters-bar">
    <input type="text" id="searchInput" placeholder="🔍 Buscar por palabra clave...">
    <select id="filterCat">
      <option value="">Todas las categorías</option>
      <option value="contenido">✍️ Contenido escrito</option>
      <option value="servicios">🤖 Servicios</option>
      <option value="productos">🎨 Productos digitales</option>
      <option value="audio">🎬 Audio y vídeo</option>
      <option value="codigo">💻 Código y técnico</option>
    </select>
    <select id="filterDiff">
      <option value="">Cualquier dificultad</option>
      <option value="baja">Baja</option>
      <option value="media">Media</option>
      <option value="alta">Alta</option>
    </select>
    <select id="filterAuto">
      <option value="">Cualquier automatización</option>
      <option value="90">≥ 90%</option>
      <option value="85">≥ 85%</option>
      <option value="80">≥ 80%</option>
    </select>
    <span class="count">Mostrando <strong id="visibleCount">100</strong> de 100</span>
  </div>

  <!-- CATEGORÍA 1: CONTENIDO ESCRITO -->
  <div class="formas-cat">
    <h3>✍️ Contenido escrito (1-20)</h3>
    <div class="formas-lista">
      <div class="forma-item" data-cat="contenido" data-diff="baja" data-auto="90"><div class="forma-content"><span>1. Escribir artículos de blog SEO para nichos</span><div class="forma-tags"><span class="mini-tag">contenido</span><span class="mini-tag">baja</span><span class="mini-tag">90%</span></div></div><a href="https://koala.sh/" target="_blank">Koala</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-1" data-fav-type="Forma #1" data-fav-title="Escribir artículos de blog SEO para nichos" data-fav-link="https://koala.sh/">⭐</button></div>
      <div class="forma-item" data-cat="contenido" data-diff="baja" data-auto="90"><div class="forma-content"><span>2. Crear newsletters de pago con resúmenes de industria</span><div class="forma-tags"><span class="mini-tag">contenido</span><span class="mini-tag">baja</span><span class="mini-tag">90%</span></div></div><a href="https://substack.com/" target="_blank">Substack</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-2" data-fav-type="Forma #2" data-fav-title="Crear newsletters de pago con resúmenes de industria" data-fav-link="https://substack.com/">⭐</button></div>
      <div class="forma-item" data-cat="contenido" data-diff="baja" data-auto="95"><div class="forma-content"><span>3. Vender micro-eBooks en Gumroad</span><div class="forma-tags"><span class="mini-tag">contenido</span><span class="mini-tag">baja</span><span class="mini-tag">95%</span></div></div><a href="https://gumroad.com/" target="_blank">Gumroad</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-3" data-fav-type="Forma #3" data-fav-title="Vender micro-eBooks en Gumroad" data-fav-link="https://gumroad.com/">⭐</button></div>
      <div class="forma-item" data-cat="contenido" data-diff="baja" data-auto="90"><div class="forma-content"><span>4. Generar descripciones de productos para e-commerce</span><div class="forma-tags"><span class="mini-tag">contenido</span><span class="mini-tag">baja</span><span class="mini-tag">90%</span></div></div><a href="https://www.shopify.com/" target="_blank">Shopify</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-4" data-fav-type="Forma #4" data-fav-title="Generar descripciones de productos para e-commerce" data-fav-link="https://www.shopify.com/">⭐</button></div>
      <div class="forma-item" data-cat="contenido" data-diff="baja" data-auto="88"><div class="forma-content"><span>5. Redactar textos publicitarios para Facebook/Google Ads</span><div class="forma-tags"><span class="mini-tag">contenido</span><span class="mini-tag">baja</span><span class="mini-tag">88%</span></div></div><a href="https://chat.openai.com/" target="_blank">ChatGPT</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-5" data-fav-type="Forma #5" data-fav-title="Redactar textos publicitarios para Facebook/Google Ads" data-fav-link="https://chat.openai.com/">⭐</button></div>
      <div class="forma-item" data-cat="contenido" data-diff="baja" data-auto="85"><div class="forma-content"><span>6. Escribir guiones para vídeos de YouTube</span><div class="forma-tags"><span class="mini-tag">contenido</span><span class="mini-tag">baja</span><span class="mini-tag">85%</span></div></div><a href="https://invideo.io/" target="_blank">InVideo</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-6" data-fav-type="Forma #6" data-fav-title="Escribir guiones para vídeos de YouTube" data-fav-link="https://invideo.io/">⭐</button></div>
      <div class="forma-item" data-cat="contenido" data-diff="media" data-auto="85"><div class="forma-content"><span>7. Crear cursos online con IA</span><div class="forma-tags"><span class="mini-tag">contenido</span><span class="mini-tag">media</span><span class="mini-tag">85%</span></div></div><a href="https://hotmart.com/" target="_blank">Hotmart</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-7" data-fav-type="Forma #7" data-fav-title="Crear cursos online con IA" data-fav-link="https://hotmart.com/">⭐</button></div>
      <div class="forma-item" data-cat="contenido" data-diff="baja" data-auto="88"><div class="forma-content"><span>8. Redactar propuestas comerciales para freelancers</span><div class="forma-tags"><span class="mini-tag">contenido</span><span class="mini-tag">baja</span><span class="mini-tag">88%</span></div></div><a href="https://www.notion.so/" target="_blank">Notion AI</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-8" data-fav-type="Forma #8" data-fav-title="Redactar propuestas comerciales para freelancers" data-fav-link="https://www.notion.so/">⭐</button></div>
      <div class="forma-item" data-cat="contenido" data-diff="media" data-auto="85"><div class="forma-content"><span>9. Generar informes de investigación de mercado</span><div class="forma-tags"><span class="mini-tag">contenido</span><span class="mini-tag">media</span><span class="mini-tag">85%</span></div></div><a href="https://www.perplexity.ai/" target="_blank">Perplexity</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-9" data-fav-type="Forma #9" data-fav-title="Generar informes de investigación de mercado" data-fav-link="https://www.perplexity.ai/">⭐</button></div>
      <div class="forma-item" data-cat="contenido" data-diff="baja" data-auto="88"><div class="forma-content"><span>10. Escribir correos de venta y secuencias de email marketing</span><div class="forma-tags"><span class="mini-tag">contenido</span><span class="mini-tag">baja</span><span class="mini-tag">88%</span></div></div><a href="https://convertkit.com/" target="_blank">ConvertKit</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-10" data-fav-type="Forma #10" data-fav-title="Escribir correos de venta y secuencias de email marketing" data-fav-link="https://convertkit.com/">⭐</button></div>
      <div class="forma-item" data-cat="contenido" data-diff="baja" data-auto="90"><div class="forma-content"><span>11. Crear libros de bajo contenido para Amazon KDP</span><div class="forma-tags"><span class="mini-tag">contenido</span><span class="mini-tag">baja</span><span class="mini-tag">90%</span></div></div><a href="https://kdp.amazon.com/" target="_blank">Amazon KDP</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-11" data-fav-type="Forma #11" data-fav-title="Crear libros de bajo contenido para Amazon KDP" data-fav-link="https://kdp.amazon.com/">⭐</button></div>
      <div class="forma-item" data-cat="contenido" data-diff="baja" data-auto="88"><div class="forma-content"><span>12. Redactar preguntas frecuentes y bases de conocimiento para empresas</span><div class="forma-tags"><span class="mini-tag">contenido</span><span class="mini-tag">baja</span><span class="mini-tag">88%</span></div></div><a href="https://chat.openai.com/" target="_blank">ChatGPT</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-12" data-fav-type="Forma #12" data-fav-title="Redactar preguntas frecuentes y bases de conocimiento" data-fav-link="https://chat.openai.com/">⭐</button></div>
      <div class="forma-item" data-cat="contenido" data-diff="baja" data-auto="88"><div class="forma-content"><span>13. Generar descripciones de inmuebles para portales inmobiliarios</span><div class="forma-tags"><span class="mini-tag">contenido</span><span class="mini-tag">baja</span><span class="mini-tag">88%</span></div></div><a href="https://chat.openai.com/" target="_blank">ChatGPT</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-13" data-fav-type="Forma #13" data-fav-title="Generar descripciones de inmuebles" data-fav-link="https://chat.openai.com/">⭐</button></div>
      <div class="forma-item" data-cat="contenido" data-diff="baja" data-auto="88"><div class="forma-content"><span>14. Escribir biografías y perfiles profesionales (LinkedIn)</span><div class="forma-tags"><span class="mini-tag">contenido</span><span class="mini-tag">baja</span><span class="mini-tag">88%</span></div></div><a href="https://www.linkedin.com/" target="_blank">LinkedIn</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-14" data-fav-type="Forma #14" data-fav-title="Escribir biografías y perfiles profesionales" data-fav-link="https://www.linkedin.com/">⭐</button></div>
      <div class="forma-item" data-cat="contenido" data-diff="media" data-auto="80"><div class="forma-content"><span>15. Crear plantillas de contratos y documentos legales simples</span><div class="forma-tags"><span class="mini-tag">contenido</span><span class="mini-tag">media</span><span class="mini-tag">80%</span></div></div><a href="https://www.notion.so/" target="_blank">Notion</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-15" data-fav-type="Forma #15" data-fav-title="Crear plantillas de contratos y documentos legales" data-fav-link="https://www.notion.so/">⭐</button></div>
      <div class="forma-item" data-cat="contenido" data-diff="baja" data-auto="88"><div class="forma-content"><span>16. Redactar menús y descripciones para restaurantes</span><div class="forma-tags"><span class="mini-tag">contenido</span><span class="mini-tag">baja</span><span class="mini-tag">88%</span></div></div><a href="https://chat.openai.com/" target="_blank">ChatGPT</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-16" data-fav-type="Forma #16" data-fav-title="Redactar menús y descripciones para restaurantes" data-fav-link="https://chat.openai.com/">⭐</button></div>
      <div class="forma-item" data-cat="contenido" data-diff="baja" data-auto="90"><div class="forma-content"><span>17. Generar contenido para redes sociales (posts, captions)</span><div class="forma-tags"><span class="mini-tag">contenido</span><span class="mini-tag">baja</span><span class="mini-tag">90%</span></div></div><a href="https://buffer.com/" target="_blank">Buffer</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-17" data-fav-type="Forma #17" data-fav-title="Generar contenido para redes sociales" data-fav-link="https://buffer.com/">⭐</button></div>
      <div class="forma-item" data-cat="contenido" data-diff="baja" data-auto="85"><div class="forma-content"><span>18. Escribir reseñas de productos patrocinadas</span><div class="forma-tags"><span class="mini-tag">contenido</span><span class="mini-tag">baja</span><span class="mini-tag">85%</span></div></div><a href="https://www.amazon.com/" target="_blank">Amazon</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-18" data-fav-type="Forma #18" data-fav-title="Escribir reseñas de productos patrocinadas" data-fav-link="https://www.amazon.com/">⭐</button></div>
      <div class="forma-item" data-cat="contenido" data-diff="baja" data-auto="85"><div class="forma-content"><span>19. Crear guías de viaje personalizadas</span><div class="forma-tags"><span class="mini-tag">contenido</span><span class="mini-tag">baja</span><span class="mini-tag">85%</span></div></div><a href="https://chat.openai.com/" target="_blank">ChatGPT</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-19" data-fav-type="Forma #19" data-fav-title="Crear guías de viaje personalizadas" data-fav-link="https://chat.openai.com/">⭐</button></div>
      <div class="forma-item" data-cat="contenido" data-diff="baja" data-auto="88"><div class="forma-content"><span>20. Redactar discursos y presentaciones</span><div class="forma-tags"><span class="mini-tag">contenido</span><span class="mini-tag">baja</span><span class="mini-tag">88%</span></div></div><a href="https://gamma.app/" target="_blank">Gamma</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-20" data-fav-type="Forma #20" data-fav-title="Redactar discursos y presentaciones" data-fav-link="https://gamma.app/">⭐</button></div>
    </div>
  </div>

  <!-- CATEGORÍA 2: SERVICIOS Y AUTOMATIZACIÓN -->
  <div class="formas-cat">
    <h3>🤖 Servicios y automatización (21-40)</h3>
    <div class="formas-lista">
      <div class="forma-item" data-cat="servicios" data-diff="media" data-auto="88"><div class="forma-content"><span>21. Recepcionista AI para negocios locales</span><div class="forma-tags"><span class="mini-tag">servicios</span><span class="mini-tag">media</span><span class="mini-tag">88%</span></div></div><a href="https://aiindigo.com/" target="_blank">Intervo</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-21" data-fav-type="Forma #21" data-fav-title="Recepcionista AI para negocios locales" data-fav-link="https://aiindigo.com/">⭐</button></div>
      <div class="forma-item" data-cat="servicios" data-diff="baja" data-auto="85"><div class="forma-content"><span>22. Chatbots de atención al cliente para pymes</span><div class="forma-tags"><span class="mini-tag">servicios</span><span class="mini-tag">baja</span><span class="mini-tag">85%</span></div></div><a href="https://www.chatbase.co/" target="_blank">Chatbase</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-22" data-fav-type="Forma #22" data-fav-title="Chatbots de atención al cliente para pymes" data-fav-link="https://www.chatbase.co/">⭐</button></div>
      <div class="forma-item" data-cat="servicios" data-diff="baja" data-auto="88"><div class="forma-content"><span>23. Automatización de seguimiento de leads con Make/Zapier</span><div class="forma-tags"><span class="mini-tag">servicios</span><span class="mini-tag">baja</span><span class="mini-tag">88%</span></div></div><a href="https://www.make.com/" target="_blank">Make</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-23" data-fav-type="Forma #23" data-fav-title="Automatización de seguimiento de leads" data-fav-link="https://www.make.com/">⭐</button></div>
      <div class="forma-item" data-cat="servicios" data-diff="media" data-auto="82"><div class="forma-content"><span>24. Generación de leads B2B con Apollo + Clay</span><div class="forma-tags"><span class="mini-tag">servicios</span><span class="mini-tag">media</span><span class="mini-tag">82%</span></div></div><a href="https://www.apollo.io/" target="_blank">Apollo</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-24" data-fav-type="Forma #24" data-fav-title="Generación de leads B2B" data-fav-link="https://www.apollo.io/">⭐</button></div>
      <div class="forma-item" data-cat="servicios" data-diff="baja" data-auto="88"><div class="forma-content"><span>25. Configurar flujos de trabajo con IA para pymes</span><div class="forma-tags"><span class="mini-tag">servicios</span><span class="mini-tag">baja</span><span class="mini-tag">88%</span></div></div><a href="https://zapier.com/" target="_blank">Zapier</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-25" data-fav-type="Forma #25" data-fav-title="Configurar flujos de trabajo con IA para pymes" data-fav-link="https://zapier.com/">⭐</button></div>
      <div class="forma-item" data-cat="servicios" data-diff="baja" data-auto="88"><div class="forma-content"><span>26. Servicio de gestión de redes sociales con IA</span><div class="forma-tags"><span class="mini-tag">servicios</span><span class="mini-tag">baja</span><span class="mini-tag">88%</span></div></div><a href="https://buffer.com/" target="_blank">Buffer</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-26" data-fav-type="Forma #26" data-fav-title="Servicio de gestión de redes sociales con IA" data-fav-link="https://buffer.com/">⭐</button></div>
      <div class="forma-item" data-cat="servicios" data-diff="media" data-auto="85"><div class="forma-content"><span>27. Auditoría SEO automatizada para sitios web</span><div class="forma-tags"><span class="mini-tag">servicios</span><span class="mini-tag">media</span><span class="mini-tag">85%</span></div></div><a href="https://surfer.com/" target="_blank">Surfer</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-27" data-fav-type="Forma #27" data-fav-title="Auditoría SEO automatizada" data-fav-link="https://surfer.com/">⭐</button></div>
      <div class="forma-item" data-cat="servicios" data-diff="media" data-auto="80"><div class="forma-content"><span>28. Consultoría de implementación de IA para pequeños negocios</span><div class="forma-tags"><span class="mini-tag">servicios</span><span class="mini-tag">media</span><span class="mini-tag">80%</span></div></div><a href="https://www.make.com/" target="_blank">Make</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-28" data-fav-type="Forma #28" data-fav-title="Consultoría de implementación de IA" data-fav-link="https://www.make.com/">⭐</button></div>
      <div class="forma-item" data-cat="servicios" data-diff="baja" data-auto="88"><div class="forma-content"><span>29. Creación de asistentes virtuales personalizados</span><div class="forma-tags"><span class="mini-tag">servicios</span><span class="mini-tag">baja</span><span class="mini-tag">88%</span></div></div><a href="https://www.chatbase.co/" target="_blank">Chatbase</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-29" data-fav-type="Forma #29" data-fav-title="Creación de asistentes virtuales personalizados" data-fav-link="https://www.chatbase.co/">⭐</button></div>
      <div class="forma-item" data-cat="servicios" data-diff="baja" data-auto="90"><div class="forma-content"><span>30. Automatización de facturación y contabilidad básica</span><div class="forma-tags"><span class="mini-tag">servicios</span><span class="mini-tag">baja</span><span class="mini-tag">90%</span></div></div><a href="https://www.notion.so/" target="_blank">Notion</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-30" data-fav-type="Forma #30" data-fav-title="Automatización de facturación y contabilidad básica" data-fav-link="https://www.notion.so/">⭐</button></div>
      <div class="forma-item" data-cat="servicios" data-diff="baja" data-auto="88"><div class="forma-content"><span>31. Servicio de transcripción y resumen de reuniones</span><div class="forma-tags"><span class="mini-tag">servicios</span><span class="mini-tag">baja</span><span class="mini-tag">88%</span></div></div><a href="https://otter.ai/" target="_blank">Otter.ai</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-31" data-fav-type="Forma #31" data-fav-title="Servicio de transcripción y resumen de reuniones" data-fav-link="https://otter.ai/">⭐</button></div>
      <div class="forma-item" data-cat="servicios" data-diff="baja" data-auto="88"><div class="forma-content"><span>32. Gestión de email marketing automatizada</span><div class="forma-tags"><span class="mini-tag">servicios</span><span class="mini-tag">baja</span><span class="mini-tag">88%</span></div></div><a href="https://convertkit.com/" target="_blank">ConvertKit</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-32" data-fav-type="Forma #32" data-fav-title="Gestión de email marketing automatizada" data-fav-link="https://convertkit.com/">⭐</button></div>
      <div class="forma-item" data-cat="servicios" data-diff="media" data-auto="85"><div class="forma-content"><span>33. Creación de embudos de venta con IA</span><div class="forma-tags"><span class="mini-tag">servicios</span><span class="mini-tag">media</span><span class="mini-tag">85%</span></div></div><a href="https://www.clickfunnels.com/" target="_blank">ClickFunnels</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-33" data-fav-type="Forma #33" data-fav-title="Creación de embudos de venta con IA" data-fav-link="https://www.clickfunnels.com/">⭐</button></div>
      <div class="forma-item" data-cat="servicios" data-diff="media" data-auto="82"><div class="forma-content"><span>34. Optimización de anuncios con IA</span><div class="forma-tags"><span class="mini-tag">servicios</span><span class="mini-tag">media</span><span class="mini-tag">82%</span></div></div><a href="https://ads.google.com/" target="_blank">Google Ads</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-34" data-fav-type="Forma #34" data-fav-title="Optimización de anuncios con IA" data-fav-link="https://ads.google.com/">⭐</button></div>
      <div class="forma-item" data-cat="servicios" data-diff="media" data-auto="82"><div class="forma-content"><span>35. Servicio de moderación de comunidades con IA</span><div class="forma-tags"><span class="mini-tag">servicios</span><span class="mini-tag">media</span><span class="mini-tag">82%</span></div></div><a href="https://discord.com/" target="_blank">Discord</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-35" data-fav-type="Forma #35" data-fav-title="Servicio de moderación de comunidades con IA" data-fav-link="https://discord.com/">⭐</button></div>
      <div class="forma-item" data-cat="servicios" data-diff="baja" data-auto="88"><div class="forma-content"><span>36. Automatización de respuestas en WhatsApp Business</span><div class="forma-tags"><span class="mini-tag">servicios</span><span class="mini-tag">baja</span><span class="mini-tag">88%</span></div></div><a href="https://www.whatsapp.com/business/" target="_blank">WhatsApp</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-36" data-fav-type="Forma #36" data-fav-title="Automatización de respuestas en WhatsApp Business" data-fav-link="https://www.whatsapp.com/business/">⭐</button></div>
      <div class="forma-item" data-cat="servicios" data-diff="baja" data-auto="85"><div class="forma-content"><span>37. Creación de encuestas y análisis de resultados</span><div class="forma-tags"><span class="mini-tag">servicios</span><span class="mini-tag">baja</span><span class="mini-tag">85%</span></div></div><a href="https://www.typeform.com/" target="_blank">Typeform</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-37" data-fav-type="Forma #37" data-fav-title="Creación de encuestas y análisis de resultados" data-fav-link="https://www.typeform.com/">⭐</button></div>
      <div class="forma-item" data-cat="servicios" data-diff="baja" data-auto="88"><div class="forma-content"><span>38. Servicio de limpieza y enriquecimiento de datos</span><div class="forma-tags"><span class="mini-tag">servicios</span><span class="mini-tag">baja</span><span class="mini-tag">88%</span></div></div><a href="https://www.make.com/" target="_blank">Make</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-38" data-fav-type="Forma #38" data-fav-title="Servicio de limpieza y enriquecimiento de datos" data-fav-link="https://www.make.com/">⭐</button></div>
      <div class="forma-item" data-cat="servicios" data-diff="baja" data-auto="88"><div class="forma-content"><span>39. Automatización de reservas para restaurantes/peluquerías</span><div class="forma-tags"><span class="mini-tag">servicios</span><span class="mini-tag">baja</span><span class="mini-tag">88%</span></div></div><a href="https://calendly.com/" target="_blank">Calendly</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-39" data-fav-type="Forma #39" data-fav-title="Automatización de reservas para restaurantes/peluquerías" data-fav-link="https://calendly.com/">⭐</button></div>
      <div class="forma-item" data-cat="servicios" data-diff="baja" data-auto="85"><div class="forma-content"><span>40. Consultoría de productividad con IA</span><div class="forma-tags"><span class="mini-tag">servicios</span><span class="mini-tag">baja</span><span class="mini-tag">85%</span></div></div><a href="https://www.notion.so/" target="_blank">Notion AI</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-40" data-fav-type="Forma #40" data-fav-title="Consultoría de productividad con IA" data-fav-link="https://www.notion.so/">⭐</button></div>
    </div>
  </div>

  <!-- CATEGORÍA 3: PRODUCTOS DIGITALES Y DISEÑO -->
  <div class="formas-cat">
    <h3>🎨 Productos digitales y diseño (41-60)</h3>
    <div class="formas-lista">
      <div class="forma-item" data-cat="productos" data-diff="baja" data-auto="90"><div class="forma-content"><span>41. Vender plantillas de Notion</span><div class="forma-tags"><span class="mini-tag">productos</span><span class="mini-tag">baja</span><span class="mini-tag">90%</span></div></div><a href="https://www.notion.so/" target="_blank">Notion</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-41" data-fav-type="Forma #41" data-fav-title="Vender plantillas de Notion" data-fav-link="https://www.notion.so/">⭐</button></div>
      <div class="forma-item" data-cat="productos" data-diff="baja" data-auto="85"><div class="forma-content"><span>42. Crear y vender presets de Lightroom</span><div class="forma-tags"><span class="mini-tag">productos</span><span class="mini-tag">baja</span><span class="mini-tag">85%</span></div></div><a href="https://www.adobe.com/" target="_blank">Adobe</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-42" data-fav-type="Forma #42" data-fav-title="Crear y vender presets de Lightroom" data-fav-link="https://www.adobe.com/">⭐</button></div>
      <div class="forma-item" data-cat="productos" data-diff="baja" data-auto="82"><div class="forma-content"><span>43. Diseñar miniaturas para YouTube</span><div class="forma-tags"><span class="mini-tag">productos</span><span class="mini-tag">baja</span><span class="mini-tag">82%</span></div></div><a href="https://www.canva.com/" target="_blank">Canva</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-43" data-fav-type="Forma #43" data-fav-title="Diseñar miniaturas para YouTube" data-fav-link="https://www.canva.com/">⭐</button></div>
      <div class="forma-item" data-cat="productos" data-diff="media" data-auto="80"><div class="forma-content"><span>44. Generar y vender arte digital con IA</span><div class="forma-tags"><span class="mini-tag">productos</span><span class="mini-tag">media</span><span class="mini-tag">80%</span></div></div><a href="https://www.midjourney.com/" target="_blank">Midjourney</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-44" data-fav-type="Forma #44" data-fav-title="Generar y vender arte digital con IA" data-fav-link="https://www.midjourney.com/">⭐</button></div>
      <div class="forma-item" data-cat="productos" data-diff="baja" data-auto="88"><div class="forma-content"><span>45. Crear imprimibles (planificadores, agendas)</span><div class="forma-tags"><span class="mini-tag">productos</span><span class="mini-tag">baja</span><span class="mini-tag">88%</span></div></div><a href="https://www.etsy.com/" target="_blank">Etsy</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-45" data-fav-type="Forma #45" data-fav-title="Crear imprimibles" data-fav-link="https://www.etsy.com/">⭐</button></div>
      <div class="forma-item" data-cat="productos" data-diff="baja" data-auto="85"><div class="forma-content"><span>46. Vender mockups y recursos de diseño</span><div class="forma-tags"><span class="mini-tag">productos</span><span class="mini-tag">baja</span><span class="mini-tag">85%</span></div></div><a href="https://www.canva.com/" target="_blank">Canva</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-46" data-fav-type="Forma #46" data-fav-title="Vender mockups y recursos de diseño" data-fav-link="https://www.canva.com/">⭐</button></div>
      <div class="forma-item" data-cat="productos" data-diff="media" data-auto="82"><div class="forma-content"><span>47. Crear logotipos y branding con IA</span><div class="forma-tags"><span class="mini-tag">productos</span><span class="mini-tag">media</span><span class="mini-tag">82%</span></div></div><a href="https://looka.com/" target="_blank">Looka</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-47" data-fav-type="Forma #47" data-fav-title="Crear logotipos y branding con IA" data-fav-link="https://looka.com/">⭐</button></div>
      <div class="forma-item" data-cat="productos" data-diff="media" data-auto="80"><div class="forma-content"><span>48. Vender fuentes tipográficas generadas por IA</span><div class="forma-tags"><span class="mini-tag">productos</span><span class="mini-tag">media</span><span class="mini-tag">80%</span></div></div><a href="https://www.fontsquirrel.com/" target="_blank">FontSquirrel</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-48" data-fav-type="Forma #48" data-fav-title="Vender fuentes tipográficas generadas por IA" data-fav-link="https://www.fontsquirrel.com/">⭐</button></div>
      <div class="forma-item" data-cat="productos" data-diff="baja" data-auto="85"><div class="forma-content"><span>49. Crear y vender iconos personalizados</span><div class="forma-tags"><span class="mini-tag">productos</span><span class="mini-tag">baja</span><span class="mini-tag">85%</span></div></div><a href="https://www.flaticon.com/" target="_blank">Flaticon</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-49" data-fav-type="Forma #49" data-fav-title="Crear y vender iconos personalizados" data-fav-link="https://www.flaticon.com/">⭐</button></div>
      <div class="forma-item" data-cat="productos" data-diff="baja" data-auto="85"><div class="forma-content"><span>50. Diseñar y vender plantillas de presentaciones</span><div class="forma-tags"><span class="mini-tag">productos</span><span class="mini-tag">baja</span><span class="mini-tag">85%</span></div></div><a href="https://gamma.app/" target="_blank">Gamma</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-50" data-fav-type="Forma #50" data-fav-title="Diseñar y vender plantillas de presentaciones" data-fav-link="https://gamma.app/">⭐</button></div>
      <div class="forma-item" data-cat="productos" data-diff="baja" data-auto="85"><div class="forma-content"><span>51. Generar y vender fondos de pantalla</span><div class="forma-tags"><span class="mini-tag">productos</span><span class="mini-tag">baja</span><span class="mini-tag">85%</span></div></div><a href="https://www.canva.com/" target="_blank">Canva</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-51" data-fav-type="Forma #51" data-fav-title="Generar y vender fondos de pantalla" data-fav-link="https://www.canva.com/">⭐</button></div>
      <div class="forma-item" data-cat="productos" data-diff="baja" data-auto="85"><div class="forma-content"><span>52. Crear stickers para WhatsApp/Telegram</span><div class="forma-tags"><span class="mini-tag">productos</span><span class="mini-tag">baja</span><span class="mini-tag">85%</span></div></div><a href="https://www.canva.com/" target="_blank">Canva</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-52" data-fav-type="Forma #52" data-fav-title="Crear stickers para WhatsApp/Telegram" data-fav-link="https://www.canva.com/">⭐</button></div>
      <div class="forma-item" data-cat="productos" data-diff="baja" data-auto="85"><div class="forma-content"><span>53. Vender tarjetas de felicitación digitales</span><div class="forma-tags"><span class="mini-tag">productos</span><span class="mini-tag">baja</span><span class="mini-tag">85%</span></div></div><a href="https://www.etsy.com/" target="_blank">Etsy</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-53" data-fav-type="Forma #53" data-fav-title="Vender tarjetas de felicitación digitales" data-fav-link="https://www.etsy.com/">⭐</button></div>
      <div class="forma-item" data-cat="productos" data-diff="baja" data-auto="85"><div class="forma-content"><span>54. Diseñar y vender currículums plantilla</span><div class="forma-tags"><span class="mini-tag">productos</span><span class="mini-tag">baja</span><span class="mini-tag">85%</span></div></div><a href="https://www.canva.com/" target="_blank">Canva</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-54" data-fav-type="Forma #54" data-fav-title="Diseñar y vender currículums plantilla" data-fav-link="https://www.canva.com/">⭐</button></div>
      <div class="forma-item" data-cat="productos" data-diff="baja" data-auto="85"><div class="forma-content"><span>55. Crear y vender invitaciones digitales</span><div class="forma-tags"><span class="mini-tag">productos</span><span class="mini-tag">baja</span><span class="mini-tag">85%</span></div></div><a href="https://www.etsy.com/" target="_blank">Etsy</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-55" data-fav-type="Forma #55" data-fav-title="Crear y vender invitaciones digitales" data-fav-link="https://www.etsy.com/">⭐</button></div>
      <div class="forma-item" data-cat="productos" data-diff="baja" data-auto="85"><div class="forma-content"><span>56. Vender recursos para redes sociales (banners, portadas)</span><div class="forma-tags"><span class="mini-tag">productos</span><span class="mini-tag">baja</span><span class="mini-tag">85%</span></div></div><a href="https://www.canva.com/" target="_blank">Canva</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-56" data-fav-type="Forma #56" data-fav-title="Vender recursos para redes sociales" data-fav-link="https://www.canva.com/">⭐</button></div>
      <div class="forma-item" data-cat="productos" data-diff="media" data-auto="80"><div class="forma-content"><span>57. Generar y vender ilustraciones para libros infantiles</span><div class="forma-tags"><span class="mini-tag">productos</span><span class="mini-tag">media</span><span class="mini-tag">80%</span></div></div><a href="https://www.midjourney.com/" target="_blank">Midjourney</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-57" data-fav-type="Forma #57" data-fav-title="Generar y vender ilustraciones para libros infantiles" data-fav-link="https://www.midjourney.com/">⭐</button></div>
      <div class="forma-item" data-cat="productos" data-diff="media" data-auto="80"><div class="forma-content"><span>58. Crear y vender cómics cortos con IA</span><div class="forma-tags"><span class="mini-tag">productos</span><span class="mini-tag">media</span><span class="mini-tag">80%</span></div></div><a href="https://www.midjourney.com/" target="_blank">Midjourney</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-58" data-fav-type="Forma #58" data-fav-title="Crear y vender cómics cortos con IA" data-fav-link="https://www.midjourney.com/">⭐</button></div>
      <div class="forma-item" data-cat="productos" data-diff="baja" data-auto="85"><div class="forma-content"><span>59. Vender plantillas de currículum y cartas de presentación</span><div class="forma-tags"><span class="mini-tag">productos</span><span class="mini-tag">baja</span><span class="mini-tag">85%</span></div></div><a href="https://www.canva.com/" target="_blank">Canva</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-59" data-fav-type="Forma #59" data-fav-title="Vender plantillas de currículum y cartas" data-fav-link="https://www.canva.com/">⭐</button></div>
      <div class="forma-item" data-cat="productos" data-diff="media" data-auto="82"><div class="forma-content"><span>60. Diseñar y vender camisetas con diseños IA</span><div class="forma-tags"><span class="mini-tag">productos</span><span class="mini-tag">media</span><span class="mini-tag">82%</span></div></div><a href="https://printful.com/" target="_blank">Printful</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-60" data-fav-type="Forma #60" data-fav-title="Diseñar y vender camisetas con diseños IA" data-fav-link="https://printful.com/">⭐</button></div>
    </div>
  </div>

  <!-- CATEGORÍA 4: AUDIO Y VÍDEO -->
  <div class="formas-cat">
    <h3>🎬 Audio y vídeo (61-80)</h3>
    <div class="formas-lista">
      <div class="forma-item" data-cat="audio" data-diff="media" data-auto="80"><div class="forma-content"><span>61. Crear canales de YouTube sin rostro</span><div class="forma-tags"><span class="mini-tag">audio</span><span class="mini-tag">media</span><span class="mini-tag">80%</span></div></div><a href="https://invideo.io/" target="_blank">InVideo AI</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-61" data-fav-type="Forma #61" data-fav-title="Crear canales de YouTube sin rostro" data-fav-link="https://invideo.io/">⭐</button></div>
      <div class="forma-item" data-cat="audio" data-diff="baja" data-auto="85"><div class="forma-content"><span>62. Generar vídeos cortos para TikTok/Reels</span><div class="forma-tags"><span class="mini-tag">audio</span><span class="mini-tag">baja</span><span class="mini-tag">85%</span></div></div><a href="https://www.capcut.com/" target="_blank">CapCut</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-62" data-fav-type="Forma #62" data-fav-title="Generar vídeos cortos para TikTok/Reels" data-fav-link="https://www.capcut.com/">⭐</button></div>
      <div class="forma-item" data-cat="audio" data-diff="media" data-auto="82"><div class="forma-content"><span>63. Producir pódcasts con voz IA</span><div class="forma-tags"><span class="mini-tag">audio</span><span class="mini-tag">media</span><span class="mini-tag">82%</span></div></div><a href="https://elevenlabs.io/" target="_blank">ElevenLabs</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-63" data-fav-type="Forma #63" data-fav-title="Producir pódcasts con voz IA" data-fav-link="https://elevenlabs.io/">⭐</button></div>
      <div class="forma-item" data-cat="audio" data-diff="media" data-auto="82"><div class="forma-content"><span>64. Crear audiolibros con IA</span><div class="forma-tags"><span class="mini-tag">audio</span><span class="mini-tag">media</span><span class="mini-tag">82%</span></div></div><a href="https://www.audible.com/" target="_blank">Audible</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-64" data-fav-type="Forma #64" data-fav-title="Crear audiolibros con IA" data-fav-link="https://www.audible.com/">⭐</button></div>
      <div class="forma-item" data-cat="audio" data-diff="baja" data-auto="85"><div class="forma-content"><span>65. Servicio de locución para anuncios</span><div class="forma-tags"><span class="mini-tag">audio</span><span class="mini-tag">baja</span><span class="mini-tag">85%</span></div></div><a href="https://elevenlabs.io/" target="_blank">ElevenLabs</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-65" data-fav-type="Forma #65" data-fav-title="Servicio de locución para anuncios" data-fav-link="https://elevenlabs.io/">⭐</button></div>
      <div class="forma-item" data-cat="audio" data-diff="baja" data-auto="85"><div class="forma-content"><span>66. Edición de vídeo automatizada para clientes</span><div class="forma-tags"><span class="mini-tag">audio</span><span class="mini-tag">baja</span><span class="mini-tag">85%</span></div></div><a href="https://www.descript.com/" target="_blank">Descript</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-66" data-fav-type="Forma #66" data-fav-title="Edición de vídeo automatizada para clientes" data-fav-link="https://www.descript.com/">⭐</button></div>
      <div class="forma-item" data-cat="audio" data-diff="baja" data-auto="88"><div class="forma-content"><span>67. Generar música de fondo libre de derechos</span><div class="forma-tags"><span class="mini-tag">audio</span><span class="mini-tag">baja</span><span class="mini-tag">88%</span></div></div><a href="https://www.soundraw.io/" target="_blank">Soundraw</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-67" data-fav-type="Forma #67" data-fav-title="Generar música de fondo libre de derechos" data-fav-link="https://www.soundraw.io/">⭐</button></div>
      <div class="forma-item" data-cat="audio" data-diff="baja" data-auto="85"><div class="forma-content"><span>68. Crear efectos de sonido personalizados</span><div class="forma-tags"><span class="mini-tag">audio</span><span class="mini-tag">baja</span><span class="mini-tag">85%</span></div></div><a href="https://elevenlabs.io/" target="_blank">ElevenLabs</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-68" data-fav-type="Forma #68" data-fav-title="Crear efectos de sonido personalizados" data-fav-link="https://elevenlabs.io/">⭐</button></div>
      <div class="forma-item" data-cat="audio" data-diff="media" data-auto="82"><div class="forma-content"><span>69. Servicio de doblaje de vídeos a otros idiomas</span><div class="forma-tags"><span class="mini-tag">audio</span><span class="mini-tag">media</span><span class="mini-tag">82%</span></div></div><a href="https://elevenlabs.io/" target="_blank">ElevenLabs</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-69" data-fav-type="Forma #69" data-fav-title="Servicio de doblaje de vídeos a otros idiomas" data-fav-link="https://elevenlabs.io/">⭐</button></div>
      <div class="forma-item" data-cat="audio" data-diff="media" data-auto="80"><div class="forma-content"><span>70. Crear vídeos explicativos para empresas</span><div class="forma-tags"><span class="mini-tag">audio</span><span class="mini-tag">media</span><span class="mini-tag">80%</span></div></div><a href="https://invideo.io/" target="_blank">InVideo</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-70" data-fav-type="Forma #70" data-fav-title="Crear vídeos explicativos para empresas" data-fav-link="https://invideo.io/">⭐</button></div>
      <div class="forma-item" data-cat="audio" data-diff="baja" data-auto="88"><div class="forma-content"><span>71. Generar subtítulos automáticos para vídeos</span><div class="forma-tags"><span class="mini-tag">audio</span><span class="mini-tag">baja</span><span class="mini-tag">88%</span></div></div><a href="https://www.descript.com/" target="_blank">Descript</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-71" data-fav-type="Forma #71" data-fav-title="Generar subtítulos automáticos para vídeos" data-fav-link="https://www.descript.com/">⭐</button></div>
      <div class="forma-item" data-cat="audio" data-diff="media" data-auto="80"><div class="forma-content"><span>72. Producir vídeos de formación corporativa</span><div class="forma-tags"><span class="mini-tag">audio</span><span class="mini-tag">media</span><span class="mini-tag">80%</span></div></div><a href="https://invideo.io/" target="_blank">InVideo</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-72" data-fav-type="Forma #72" data-fav-title="Producir vídeos de formación corporativa" data-fav-link="https://invideo.io/">⭐</button></div>
      <div class="forma-item" data-cat="audio" data-diff="baja" data-auto="85"><div class="forma-content"><span>73. Crear y vender plantillas de vídeo para redes</span><div class="forma-tags"><span class="mini-tag">audio</span><span class="mini-tag">baja</span><span class="mini-tag">85%</span></div></div><a href="https://www.capcut.com/" target="_blank">CapCut</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-73" data-fav-type="Forma #73" data-fav-title="Crear y vender plantillas de vídeo para redes" data-fav-link="https://www.capcut.com/">⭐</button></div>
      <div class="forma-item" data-cat="audio" data-diff="media" data-auto="80"><div class="forma-content"><span>74. Servicio de creación de vídeos de producto</span><div class="forma-tags"><span class="mini-tag">audio</span><span class="mini-tag">media</span><span class="mini-tag">80%</span></div></div><a href="https://invideo.io/" target="_blank">InVideo</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-74" data-fav-type="Forma #74" data-fav-title="Servicio de creación de vídeos de producto" data-fav-link="https://invideo.io/">⭐</button></div>
      <div class="forma-item" data-cat="audio" data-diff="media" data-auto="80"><div class="forma-content"><span>75. Generar vídeos con avatares IA para formación</span><div class="forma-tags"><span class="mini-tag">audio</span><span class="mini-tag">media</span><span class="mini-tag">80%</span></div></div><a href="https://www.synthesia.io/" target="_blank">Synthesia</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-75" data-fav-type="Forma #75" data-fav-title="Generar vídeos con avatares IA para formación" data-fav-link="https://www.synthesia.io/">⭐</button></div>
      <div class="forma-item" data-cat="audio" data-diff="media" data-auto="80"><div class="forma-content"><span>76. Crear y vender podcasts de nicho</span><div class="forma-tags"><span class="mini-tag">audio</span><span class="mini-tag">media</span><span class="mini-tag">80%</span></div></div><a href="https://elevenlabs.io/" target="_blank">ElevenLabs</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-76" data-fav-type="Forma #76" data-fav-title="Crear y vender podcasts de nicho" data-fav-link="https://elevenlabs.io/">⭐</button></div>
      <div class="forma-item" data-cat="audio" data-diff="baja" data-auto="85"><div class="forma-content"><span>77. Servicio de edición de pódcast para empresas</span><div class="forma-tags"><span class="mini-tag">audio</span><span class="mini-tag">baja</span><span class="mini-tag">85%</span></div></div><a href="https://www.descript.com/" target="_blank">Descript</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-77" data-fav-type="Forma #77" data-fav-title="Servicio de edición de pódcast para empresas" data-fav-link="https://www.descript.com/">⭐</button></div>
      <div class="forma-item" data-cat="audio" data-diff="baja" data-auto="85"><div class="forma-content"><span>78. Crear y vender audios relajantes/meditación</span><div class="forma-tags"><span class="mini-tag">audio</span><span class="mini-tag">baja</span><span class="mini-tag">85%</span></div></div><a href="https://elevenlabs.io/" target="_blank">ElevenLabs</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-78" data-fav-type="Forma #78" data-fav-title="Crear y vender audios relajantes/meditación" data-fav-link="https://elevenlabs.io/">⭐</button></div>
      <div class="forma-item" data-cat="audio" data-diff="baja" data-auto="85"><div class="forma-content"><span>79. Generar y vender sonidos para apps</span><div class="forma-tags"><span class="mini-tag">audio</span><span class="mini-tag">baja</span><span class="mini-tag">85%</span></div></div><a href="https://www.soundraw.io/" target="_blank">Soundraw</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-79" data-fav-type="Forma #79" data-fav-title="Generar y vender sonidos para apps" data-fav-link="https://www.soundraw.io/">⭐</button></div>
      <div class="forma-item" data-cat="audio" data-diff="baja" data-auto="85"><div class="forma-content"><span>80. Servicio de creación de jingles publicitarios</span><div class="forma-tags"><span class="mini-tag">audio</span><span class="mini-tag">baja</span><span class="mini-tag">85%</span></div></div><a href="https://www.soundraw.io/" target="_blank">Soundraw</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-80" data-fav-type="Forma #80" data-fav-title="Servicio de creación de jingles publicitarios" data-fav-link="https://www.soundraw.io/">⭐</button></div>
    </div>
  </div>

  <!-- CATEGORÍA 5: CÓDIGO Y PRODUCTOS TÉCNICOS -->
  <div class="formas-cat">
    <h3>💻 Código y productos técnicos (81-100)</h3>
    <div class="formas-lista">
      <div class="forma-item" data-cat="codigo" data-diff="alta" data-auto="75"><div class="forma-content"><span>81. Crear pequeños SaaS con IA</span><div class="forma-tags"><span class="mini-tag">codigo</span><span class="mini-tag">alta</span><span class="mini-tag">75%</span></div></div><a href="https://cursor.sh/" target="_blank">Cursor</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-81" data-fav-type="Forma #81" data-fav-title="Crear pequeños SaaS con IA" data-fav-link="https://cursor.sh/">⭐</button></div>
      <div class="forma-item" data-cat="codigo" data-diff="media" data-auto="80"><div class="forma-content"><span>82. Desarrollar plugins de WordPress</span><div class="forma-tags"><span class="mini-tag">codigo</span><span class="mini-tag">media</span><span class="mini-tag">80%</span></div></div><a href="https://wordpress.org/" target="_blank">WordPress</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-82" data-fav-type="Forma #82" data-fav-title="Desarrollar plugins de WordPress" data-fav-link="https://wordpress.org/">⭐</button></div>
      <div class="forma-item" data-cat="codigo" data-diff="media" data-auto="80"><div class="forma-content"><span>83. Crear extensiones de Chrome</span><div class="forma-tags"><span class="mini-tag">codigo</span><span class="mini-tag">media</span><span class="mini-tag">80%</span></div></div><a href="https://developer.chrome.com/" target="_blank">Chrome Dev</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-83" data-fav-type="Forma #83" data-fav-title="Crear extensiones de Chrome" data-fav-link="https://developer.chrome.com/">⭐</button></div>
      <div class="forma-item" data-cat="codigo" data-diff="media" data-auto="80"><div class="forma-content"><span>84. Desarrollar bots para Discord/Telegram</span><div class="forma-tags"><span class="mini-tag">codigo</span><span class="mini-tag">media</span><span class="mini-tag">80%</span></div></div><a href="https://discord.com/developers/" target="_blank">Discord Dev</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-84" data-fav-type="Forma #84" data-fav-title="Desarrollar bots para Discord/Telegram" data-fav-link="https://discord.com/developers/">⭐</button></div>
      <div class="forma-item" data-cat="codigo" data-diff="media" data-auto="80"><div class="forma-content"><span>85. Vender scripts de automatización</span><div class="forma-tags"><span class="mini-tag">codigo</span><span class="mini-tag">media</span><span class="mini-tag">80%</span></div></div><a href="https://github.com/" target="_blank">GitHub</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-85" data-fav-type="Forma #85" data-fav-title="Vender scripts de automatización" data-fav-link="https://github.com/">⭐</button></div>
      <div class="forma-item" data-cat="codigo" data-diff="media" data-auto="80"><div class="forma-content"><span>86. Crear y vender APIs simples</span><div class="forma-tags"><span class="mini-tag">codigo</span><span class="mini-tag">media</span><span class="mini-tag">80%</span></div></div><a href="https://rapidapi.com/" target="_blank">RapidAPI</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-86" data-fav-type="Forma #86" data-fav-title="Crear y vender APIs simples" data-fav-link="https://rapidapi.com/">⭐</button></div>
      <div class="forma-item" data-cat="codigo" data-diff="alta" data-auto="75"><div class="forma-content"><span>87. Desarrollar apps móviles con IA</span><div class="forma-tags"><span class="mini-tag">codigo</span><span class="mini-tag">alta</span><span class="mini-tag">75%</span></div></div><a href="https://flutter.dev/" target="_blank">Flutter</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-87" data-fav-type="Forma #87" data-fav-title="Desarrollar apps móviles con IA" data-fav-link="https://flutter.dev/">⭐</button></div>
      <div class="forma-item" data-cat="codigo" data-diff="media" data-auto="80"><div class="forma-content"><span>88. Crear herramientas online gratuitas con ads</span><div class="forma-tags"><span class="mini-tag">codigo</span><span class="mini-tag">media</span><span class="mini-tag">80%</span></div></div><a href="https://vercel.com/" target="_blank">Vercel</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-88" data-fav-type="Forma #88" data-fav-title="Crear herramientas online gratuitas con ads" data-fav-link="https://vercel.com/">⭐</button></div>
      <div class="forma-item" data-cat="codigo" data-diff="media" data-auto="80"><div class="forma-content"><span>89. Servicio de consultoría técnica en IA</span><div class="forma-tags"><span class="mini-tag">codigo</span><span class="mini-tag">media</span><span class="mini-tag">80%</span></div></div><a href="https://www.make.com/" target="_blank">Make</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-89" data-fav-type="Forma #89" data-fav-title="Servicio de consultoría técnica en IA" data-fav-link="https://www.make.com/">⭐</button></div>
      <div class="forma-item" data-cat="codigo" data-diff="media" data-auto="82"><div class="forma-content"><span>90. Crear y vender bases de datos de leads</span><div class="forma-tags"><span class="mini-tag">codigo</span><span class="mini-tag">media</span><span class="mini-tag">82%</span></div></div><a href="https://www.apollo.io/" target="_blank">Apollo</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-90" data-fav-type="Forma #90" data-fav-title="Crear y vender bases de datos de leads" data-fav-link="https://www.apollo.io/">⭐</button></div>
      <div class="forma-item" data-cat="codigo" data-diff="baja" data-auto="88"><div class="forma-content"><span>91. Desarrollar chatbots para webs de empresas</span><div class="forma-tags"><span class="mini-tag">codigo</span><span class="mini-tag">baja</span><span class="mini-tag">88%</span></div></div><a href="https://www.chatbase.co/" target="_blank">Chatbase</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-91" data-fav-type="Forma #91" data-fav-title="Desarrollar chatbots para webs de empresas" data-fav-link="https://www.chatbase.co/">⭐</button></div>
      <div class="forma-item" data-cat="codigo" data-diff="media" data-auto="80"><div class="forma-content"><span>92. Crear herramientas de generación de contenido</span><div class="forma-tags"><span class="mini-tag">codigo</span><span class="mini-tag">media</span><span class="mini-tag">80%</span></div></div><a href="https://www.make.com/" target="_blank">Make</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-92" data-fav-type="Forma #92" data-fav-title="Crear herramientas de generación de contenido" data-fav-link="https://www.make.com/">⭐</button></div>
      <div class="forma-item" data-cat="codigo" data-diff="baja" data-auto="88"><div class="forma-content"><span>93. Automatizar procesos internos de empresas</span><div class="forma-tags"><span class="mini-tag">codigo</span><span class="mini-tag">baja</span><span class="mini-tag">88%</span></div></div><a href="https://zapier.com/" target="_blank">Zapier</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-93" data-fav-type="Forma #93" data-fav-title="Automatizar procesos internos de empresas" data-fav-link="https://zapier.com/">⭐</button></div>
      <div class="forma-item" data-cat="codigo" data-diff="alta" data-auto="75"><div class="forma-content"><span>94. Desarrollar sistemas de recomendación simples</span><div class="forma-tags"><span class="mini-tag">codigo</span><span class="mini-tag">alta</span><span class="mini-tag">75%</span></div></div><a href="https://github.com/" target="_blank">GitHub</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-94" data-fav-type="Forma #94" data-fav-title="Desarrollar sistemas de recomendación simples" data-fav-link="https://github.com/">⭐</button></div>
      <div class="forma-item" data-cat="codigo" data-diff="media" data-auto="80"><div class="forma-content"><span>95. Crear y vender plantillas de código</span><div class="forma-tags"><span class="mini-tag">codigo</span><span class="mini-tag">media</span><span class="mini-tag">80%</span></div></div><a href="https://github.com/" target="_blank">GitHub</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-95" data-fav-type="Forma #95" data-fav-title="Crear y vender plantillas de código" data-fav-link="https://github.com/">⭐</button></div>
      <div class="forma-item" data-cat="codigo" data-diff="media" data-auto="80"><div class="forma-content"><span>96. Servicio de integración de IA en webs existentes</span><div class="forma-tags"><span class="mini-tag">codigo</span><span class="mini-tag">media</span><span class="mini-tag">80%</span></div></div><a href="https://www.make.com/" target="_blank">Make</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-96" data-fav-type="Forma #96" data-fav-title="Servicio de integración de IA en webs existentes" data-fav-link="https://www.make.com/">⭐</button></div>
      <div class="forma-item" data-cat="codigo" data-diff="alta" data-auto="75"><div class="forma-content"><span>97. Desarrollar asistentes de voz para empresas</span><div class="forma-tags"><span class="mini-tag">codigo</span><span class="mini-tag">alta</span><span class="mini-tag">75%</span></div></div><a href="https://elevenlabs.io/" target="_blank">ElevenLabs</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-97" data-fav-type="Forma #97" data-fav-title="Desarrollar asistentes de voz para empresas" data-fav-link="https://elevenlabs.io/">⭐</button></div>
      <div class="forma-item" data-cat="codigo" data-diff="media" data-auto="80"><div class="forma-content"><span>98. Crear y vender datasets procesados con IA</span><div class="forma-tags"><span class="mini-tag">codigo</span><span class="mini-tag">media</span><span class="mini-tag">80%</span></div></div><a href="https://www.kaggle.com/" target="_blank">Kaggle</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-98" data-fav-type="Forma #98" data-fav-title="Crear y vender datasets procesados con IA" data-fav-link="https://www.kaggle.com/">⭐</button></div>
      <div class="forma-item" data-cat="codigo" data-diff="baja" data-auto="88"><div class="forma-content"><span>99. Automatizar la generación de informes con IA</span><div class="forma-tags"><span class="mini-tag">codigo</span><span class="mini-tag">baja</span><span class="mini-tag">88%</span></div></div><a href="https://www.make.com/" target="_blank">Make</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-99" data-fav-type="Forma #99" data-fav-title="Automatizar la generación de informes con IA" data-fav-link="https://www.make.com/">⭐</button></div>
      <div class="forma-item" data-cat="codigo" data-diff="baja" data-auto="85"><div class="forma-content"><span>100. Crear un directorio de herramientas IA y monetizar con afiliados</span><div class="forma-tags"><span class="mini-tag">codigo</span><span class="mini-tag">baja</span><span class="mini-tag">85%</span></div></div><a href="https://www.notion.so/" target="_blank">Notion</a><button class="fav-btn" style="position:static;opacity:.4;font-size:.95rem" data-fav-id="forma-100" data-fav-type="Forma #100" data-fav-title="Crear un directorio de herramientas IA" data-fav-link="https://www.notion.so/">⭐</button></div>
    </div>
  </div>
</section>

<!-- ===== SECCIÓN: COMPARADOR ===== -->
<section id="comparador" class="reveal">
  <div class="section-head">
    <span class="kicker">Herramienta · Comparador</span>
    <h2>Compara los modelos de negocio de un vistazo</h2>
    <p>Filtra por inversión inicial, nivel de automatización o dificultad para encontrar el modelo que mejor encaja contigo.</p>
  </div>

  <div class="table-wrap">
    <table>
      <thead>
        <tr>
          <th>Modelo</th>
          <th>Inversión inicial</th>
          <th>Automatización</th>
          <th>Dificultad</th>
          <th>Tiempo hasta 1er ingreso</th>
          <th>Herramienta clave</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td><strong>Micro-eBooks</strong></td>
          <td>€0</td>
          <td><div class="meter"><div class="meter-bar"><div class="meter-fill" style="width:95%"></div></div><span class="meter-num">95%</span></div></td>
          <td>Baja</td>
          <td>1-2 semanas</td>
          <td><a href="https://gumroad.com/" target="_blank" class="link">Gumroad</a></td>
        </tr>
        <tr>
          <td><strong>Newsletters de nicho</strong></td>
          <td>€0</td>
          <td><div class="meter"><div class="meter-bar"><div class="meter-fill" style="width:90%"></div></div><span class="meter-num">90%</span></div></td>
          <td>Baja-Media</td>
          <td>2-4 semanas</td>
          <td><a href="https://substack.com/" target="_blank" class="link">Substack</a></td>
        </tr>
        <tr>
          <td><strong>Descripciones de productos</strong></td>
          <td>€0</td>
          <td><div class="meter"><div class="meter-bar"><div class="meter-fill" style="width:90%"></div></div><span class="meter-num">90%</span></div></td>
          <td>Baja</td>
          <td>1 semana</td>
          <td><a href="https://chat.openai.com/" target="_blank" class="link">ChatGPT</a></td>
        </tr>
        <tr>
          <td><strong>Contenido SEO</strong></td>
          <td>€0</td>
          <td><div class="meter"><div class="meter-bar"><div class="meter-fill" style="width:85%"></div></div><span class="meter-num">85%</span></div></td>
          <td>Media</td>
          <td>1-3 meses</td>
          <td><a href="https://koala.sh/" target="_blank" class="link">Koala</a></td>
        </tr>
        <tr>
          <td><strong>Recepcionista AI</strong></td>
          <td>€0</td>
          <td><div class="meter"><div class="meter-bar"><div class="meter-fill" style="width:88%"></div></div><span class="meter-num">88%</span></div></td>
          <td>Media</td>
          <td>2-4 semanas</td>
          <td><a href="https://aiindigo.com/" target="_blank" class="link">Intervo</a></td>
        </tr>
        <tr>
          <td><strong>Generación de leads B2B</strong></td>
          <td>€0</td>
          <td><div class="meter"><div class="meter-bar"><div class="meter-fill" style="width:85%"></div></div><span class="meter-num">85%</span></div></td>
          <td>Media</td>
          <td>2-3 semanas</td>
          <td><a href="https://www.apollo.io/" target="_blank" class="link">Apollo</a></td>
        </tr>
        <tr>
          <td><strong>YouTube sin rostro</strong></td>
          <td>€0</td>
          <td><div class="meter"><div class="meter-bar"><div class="meter-fill" style="width:80%"></div></div><span class="meter-num">80%</span></div></td>
          <td>Media</td>
          <td>1-3 meses</td>
          <td><a href="https://invideo.io/" target="_blank" class="link">InVideo</a></td>
        </tr>
        <tr>
          <td><strong>Diseño de miniaturas</strong></td>
          <td>€0</td>
          <td><div class="meter"><div class="meter-bar"><div class="meter-fill" style="width:82%"></div></div><span class="meter-num">82%</span></div></td>
          <td>Baja</td>
          <td>1 semana</td>
          <td><a href="https://www.canva.com/" target="_blank" class="link">Canva</a></td>
        </tr>
      </tbody>
    </table>
  </div>
</section>

<!-- ===== SECCIÓN: CALCULADORA DE GANANCIAS ===== -->
<section id="calculadora" class="reveal">
  <div class="section-head">
    <span class="kicker">Herramienta · Calculadora</span>
    <h2>Calcula tus ganancias mensuales estimadas</h2>
    <p>Ajusta los controles según tu modelo de negocio. Los rangos están basados en datos reales de principiantes en 2026.</p>
  </div>

  <div class="calc-box">
    <div class="calc-grid">
      <div>
        <div class="calc-control">
          <label>Precio del producto (€) <span class="val" id="valPrecio">19</span></label>
          <input type="range" id="precio" min="3" max="97" value="19" step="1">
        </div>
        <div class="calc-control" style="margin-top:1rem">
          <label>Visitantes al mes <span class="val" id="valTrafico">500</span></label>
          <input type="range" id="trafico" min="50" max="10000" value="500" step="50">
        </div>
        <div class="calc-control" style="margin-top:1rem">
          <label>Tasa de conversión (%) <span class="val" id="valConv">3</span></label>
          <input type="range" id="conversion" min="0.5" max="15" value="3" step="0.5">
        </div>
        <div class="calc-control" style="margin-top:1rem">
          <label>Comisión de plataforma (%) <span class="val" id="valComision">10</span></label>
          <input type="range" id="comision" min="0" max="30" value="10" step="1">
        </div>
      </div>
      <div style="display:flex;flex-direction:column;justify-content:center">
        <div class="calc-result">
          <div class="label">Ingreso neto estimado</div>
          <div class="amount" id="resultado">€0</div>
          <div class="sub" id="detalle">0 ventas · comisión aplicada</div>
        </div>
        <p style="font-size:.75rem;color:var(--text-dim);margin-top:.8rem;text-align:center">* Estimación orientativa. No incluye impuestos ni otros costes.</p>
      </div>
    </div>
  </div>
</section>

<!-- ===== NUEVA SECCIÓN: ROADMAP 30 DÍAS ===== -->
<section id="roadmap" class="reveal">
  <div class="section-head">
    <span class="kicker">Nuevo · Plan de acción</span>
    <h2>Roadmap de 30 días: de cero a tu primer ingreso</h2>
    <p>Marca cada hito cuando lo completes. Tu progreso se guarda automáticamente en tu navegador para que puedas volver cuando quieras.</p>
  </div>

  <div class="roadmap">
    <div class="roadmap-stats">
      <span>Progreso: <strong id="rmDone">0</strong> / <strong id="rmTotal">20</strong> hitos</span>
      <span><strong id="rmPercent">0%</strong> completado</span>
    </div>
    <div class="roadmap-progress"><div class="roadmap-progress-fill" id="rmFill"></div></div>
    <div class="roadmap-list" id="rmList">
      <!-- Se genera dinámicamente desde JS -->
    </div>
  </div>
</section>

<!-- ===== SECCIÓN: GRÁFICOS ===== -->
<section id="graficos" class="reveal">
  <div class="section-head">
    <span class="kicker">Visualización de datos</span>
    <h2>Gráficos para decidir mejor</h2>
    <p>Compara el potencial de automatización y el esfuerzo inicial de cada modelo.</p>
  </div>

  <div class="grid grid-2">
    <div class="chart-container">
      <h4>Nivel de automatización por modelo (%)</h4>
      <canvas id="chartAuto"></canvas>
    </div>
    <div class="chart-container">
      <h4>Tiempo estimado hasta el primer ingreso (semanas)</h4>
      <canvas id="chartTiempo"></canvas>
    </div>
  </div>
</section>

<!-- ===== NUEVA SECCIÓN: ERRORES COMUNES ===== -->
<section id="errores" class="reveal">
  <div class="section-head">
    <span class="kicker">Nuevo · Aprende de los errores</span>
    <h2>10 errores que arruinan a los principiantes</h2>
    <p>Evítalos desde el primer día. Son los mismos que cometen el 80% de los que empiezan y no consiguen resultados.</p>
  </div>

  <div class="grid grid-2">
    <div class="error-card"><h4>1. Elegir un nicho demasiado amplio</h4><p>"Ganar dinero con IA" no es un nicho. "IA para fisioterapeutas" sí. Cuanto más específico, menos competencia y más conversión.</p></div>
    <div class="error-card"><h4>2. No revisar el contenido generado</h4><p>La IA alucina, inventa datos y suena artificial. Sin un mínimo de edición humana, tu reputación se va al garete.</p></div>
    <div class="error-card"><h4>3. Ignorar el SEO desde el principio</h4><p>Sin tráfico no hay ventas. Aprender lo básico de keywords e intención de búsqueda es obligatorio.</p></div>
    <div class="error-card"><h4>4. No construir lista de email</h4><p>Las redes sociales son alquiladas. Tu lista de correo es lo único que realmente posees. Empieza desde el día 1.</p></div>
    <div class="error-card"><h4>5. Depender de una sola API gratuita</h4><p>Si la API cae, tu negocio cae. Ten siempre 2-3 alternativas configuradas (Groq, Cloudflare, OpenRouter...).</p></div>
    <div class="error-card"><h4>6. No medir nada</h4><p>Sin métricas no sabes qué funciona. Instala analítica gratuita (Plausible, Umami o Google Analytics) desde el principio.</p></div>
    <div class="error-card"><h4>7. Lanzar sin validar</h4><p>Antes de crear 20 eBooks, valida con 1. Si no vende ese, 20 tampoco lo harán. Habla con 5 personas de tu nicho antes de crear nada.</p></div>
    <div class="error-card"><h4>8. Copiar el modelo de otro sin adaptarlo</h4><p>Lo que funciona para un nicho angloparlante puede no funcionar en español. Adapta el precio, el tono y el canal.</p></div>
    <div class="error-card"><h4>9. No tener una oferta clara</h4><p>"Te ayudo con IA" no vende. "Te creo 30 descripciones de producto en 48h por 90€" sí. Sé específico con el resultado y el precio.</p></div>
    <div class="error-card"><h4>10. Abandonar a las 2 semanas</h4><p>Los primeros resultados tardan entre 1 y 3 meses. El que persiste gana. La constancia importa más que la perfección.</p></div>
  </div>
</section>

<!-- ===== NUEVA SECCIÓN: FAQ ===== -->
<section id="faq" class="reveal">
  <div class="section-head">
    <span class="kicker">Nuevo · Dudas frecuentes</span>
    <h2>Preguntas frecuentes</h2>
    <p>Las dudas que más nos llegan sobre empezar un negocio con IA gratis.</p>
  </div>

  <details class="faq-item">
    <summary>¿Es legal vender contenido generado por IA?</summary>
    <div class="details-content"><p>Sí, en la mayoría de jurisdicciones (incluida la UE y España) el contenido generado por IA se puede vender, siempre que no infrinjas derechos de autor de terceros, no suplantes identidad y declares cuando sea requerido. Las plataformas como Gumroad, Amazon KDP o Substack permiten contenido IA, pero cada una tiene sus normas: revísalas antes de publicar.</p></div>
  </details>
  <details class="faq-item">
    <summary>¿Puedo usar ChatGPT gratis para vender productos?</summary>
    <div class="details-content"><p>Sí. El plan gratuito de ChatGPT te permite generar texto y usarlo comercialmente. Para automatizar necesitarás APIs gratuitas como Pollinations, Puter.js, Groq o Cloudflare Workers AI, que también permiten uso comercial sin coste (con sus límites y condiciones).</p></div>
  </details>
  <details class="faq-item">
    <summary>¿Cuánto tardo en ganar el primer euro?</summary>
    <div class="details-content"><p>Depende del modelo. Micro-eBooks o descripciones de productos: 1-2 semanas. Newsletters: 2-4 semanas. Contenido SEO o YouTube: 1-3 meses. La clave no es la velocidad, sino montar un sistema que funcione y repetirlo.</p></div>
  </details>
  <details class="faq-item">
    <summary>¿Qué pasa si la API gratuita deja de funcionar?</summary>
    <div class="details-content"><p>Es un riesgo real. Ten siempre 2-3 alternativas: Pollinations, Puter.js, Groq, Cloudflare o OpenRouter. Cambia la URL base en tu código y listo. Por eso recomendamos no depender de una sola API.</p></div>
  </details>
  <details class="faq-item">
    <summary>¿Necesito saber programar?</summary>
    <div class="details-content"><p>No. Puedes empezar con ChatGPT + Gumroad + Make/Zapier sin tocar una línea de código. Si quieres ir más allá (crear un SaaS, un bot o una demo), herramientas como Cursor o Claude te permiten programar con lenguaje natural.</p></div>
  </details>
  <details class="faq-item">
    <summary>¿Cuánto dinero puedo llegar a ganar?</summary>
    <div class="details-content"><p>Los rangos realistas para principiantes son €500-€2.000/mes en los primeros meses. Con constancia y varios productos, se puede superar. Desconfía de quien prometa miles de euros en una semana: no es realista.</p></div>
  </details>
  <details class="faq-item">
    <summary>¿Necesito registrar una empresa?</summary>
    <div class="details-content"><p>Para empezar, no. En España puedes facturar como autónomo (con alta en Hacienda y Seguridad Social) o usar plataformas que ya gestionan los impuestos (como Gumroad en algunos casos). Consulta con un asesor fiscal cuando empieces a facturar de forma recurrente.</p></div>
  </details>
  <details class="faq-item">
    <summary>¿Las APIs gratuitas tienen límite?</summary>
    <div class="details-content"><p>Sí. Cada API tiene su propio rate limit: Groq (30 RPM, 1.000/día), Cloudflare (10.000 Neurons/día), Pollinations (sin límite pero con posible ralentización), OpenRouter (50 peticiones/día gratis). Para prototipos y pequeños negocios son más que suficientes.</p></div>
  </details>
</section>

<!-- ===== NUEVA SECCIÓN: GLOSARIO ===== -->
<section id="glosario" class="reveal">
  <div class="section-head">
    <span class="kicker">Nuevo · Glosario</span>
    <h2>Términos que verás una y otra vez</h2>
    <p>Definiciones rápidas para que no te pierdas con la jerga.</p>
  </div>

  <div class="grid grid-2">
    <details class="faq-item"><summary>API</summary><div class="details-content"><p>Interfaz de Programación de Aplicaciones. Es la "puerta" que permite que tu programa hable con la IA. Cuando alguien dice "usa la API de Pollinations", se refiere a llamar a su URL para obtener respuestas.</p></div></details>
    <details class="faq-item"><summary>Token</summary><div class="details-content"><p>Unidad mínima de texto que procesa un modelo. Aproximadamente 1 token = 0,75 palabras. Cuando una API es "sin tokens" significa que no te cobra por tokens consumidos.</p></div></details>
    <details class="faq-item"><summary>Prompt</summary><div class="details-content"><p>La instrucción que le das a la IA. Cuanto más específico, claro y con contexto, mejor será la respuesta. Ejemplo: "Escribe un esquema de 8 capítulos para un eBook sobre X dirigido a Y".</p></div></details>
    <details class="faq-item"><summary>Wrapper</summary><div class="details-content"><p>Una capa que envuelve a otra API para ofrecer una funcionalidad distinta. KeylessAI, por ejemplo, es un wrapper que agrega varias APIs gratuitas en un solo endpoint.</p></div></details>
    <details class="faq-item"><summary>Rate limit</summary><div class="details-content"><p>Límite de peticiones que puedes hacer a una API por unidad de tiempo. Groq, por ejemplo, permite 30 peticiones por minuto en su plan gratuito.</p></div></details>
    <details class="faq-item"><summary>RAG</summary><div class="details-content"><p>Retrieval-Augmented Generation. Técnica que combina búsqueda de información con generación de texto. Útil para que la IA responda sobre documentos propios.</p></div></details>
    <details class="faq-item"><summary>Fine-tuning</summary><div class="details-content"><p>Reentrenar un modelo con tus propios datos para que se adapte a tu estilo o nicho. No es imprescindible al principio: los prompts bien hechos suelen bastar.</p></div></details>
    <details class="faq-item"><summary>Alucinación</summary><div class="details-content"><p>Cuando la IA inventa datos, citas o hechos que parecen reales pero no lo son. Por eso siempre hay que revisar lo que genera.</p></div></details>
    <details class="faq-item"><summary>No-code</summary><div class="details-content"><p>Herramientas que permiten crear automatizaciones sin programar. Make y Zapier son los dos ejemplos más populares y tienen planes gratuitos.</p></div></details>
    <details class="faq-item"><summary>localStorage</summary><div class="details-content"><p>Almacenamiento del navegador que permite guardar datos en el dispositivo del usuario. Es donde se guardan tus favoritos y el progreso del roadmap de esta web.</p></div></details>
  </div>
</section>

<!-- ===== NUEVA SECCIÓN: PLANTILLAS DESCARGABLES ===== -->
<section id="plantillas" class="reveal">
  <div class="section-head">
    <span class="kicker">Nuevo · Descargables</span>
    <h2>Plantillas listas para descargar</h2>
    <p>Todo lo que necesitas para empezar, en archivos listos para usar. Descarga, rellena y empieza.</p>
  </div>

  <div class="plantilla-card">
    <div class="plantilla-info"><h4>📋 Checklist de 30 días</h4><p>Los 20 hitos del roadmap en formato texto para imprimir o pegar en Notion.</p></div>
    <button class="dl-btn" data-dl="checklist">Descargar .txt</button>
  </div>
  <div class="plantilla-card">
    <div class="plantilla-info"><h4>✍️ Plantilla de prompt maestro</h4><p>Estructura para crear prompts potentes para cualquier modelo de negocio.</p></div>
    <button class="dl-btn" data-dl="prompt">Descargar .txt</button>
  </div>
  <div class="plantilla-card">
    <div class="plantilla-info"><h4>📊 Comparativa de APIs gratuitas</h4><p>Tabla con las 6 APIs principales, sus límites y para qué sirve cada una.</p></div>
    <button class="dl-btn" data-dl="apis">Descargar .txt</button>
  </div>
  <div class="plantilla-card">
    <div class="plantilla-info"><h4>🧮 Calculadora de ganancias</h4><p>Hoja con la fórmula de la calculadora para que la uses offline.</p></div>
    <button class="dl-btn" data-dl="calc">Descargar .txt</button>
  </div>
</section>

<footer>
  <div class="footer-links">
    <a href="https://developer.puter.com/" target="_blank">Puter.js</a>
    <a href="https://pollinations.ai/" target="_blank">Pollinations</a>
    <a href="https://openrouter.ai/" target="_blank">OpenRouter</a>
    <a href="https://console.groq.com/" target="_blank">Groq</a>
    <a href="https://developers.cloudflare.com/workers-ai/" target="_blank">Cloudflare AI</a>
    <a href="https://www.make.com/" target="_blank">Make</a>
    <a href="https://gumroad.com/" target="_blank">Gumroad</a>
    <a href="https://substack.com/" target="_blank">Substack</a>
  </div>
  <p>Hub creado para empezar hoy · Sin tokens, sin APIs de pago, con enlaces directos.</p>
  <p style="margin-top:.4rem;font-size:.75rem">La automatización del 100% es un mito. Apunta al 90-95% y mantén el control de calidad.</p>
</footer>

<!-- DRAWER DE FAVORITOS -->
<div class="drawer" id="favDrawer">
  <div class="drawer-header">
    <h3>⭐ Mis favoritos</h3>
    <button class="drawer-close" id="favCloseBtn">×</button>
  </div>
  <div class="drawer-body" id="favBody"></div>
</div>

<!-- TOAST -->
<div class="toast" id="toast">Guardado</div>

<script>
  // ===== REVEAL =====
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) { entry.target.classList.add('visible'); observer.unobserve(entry.target); }
    });
  }, { threshold: 0.06 });
  document.querySelectorAll('.reveal').forEach(el => observer.observe(el));

  // ===== SMOOTH SCROLL =====
  document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function(e) {
      const target = document.querySelector(this.getAttribute('href'));
      if (target) { e.preventDefault(); target.scrollIntoView({ behavior: 'smooth', block: 'start' }); }
    });
  });

  // ===== CALCULADORA =====
  const precioEl = document.getElementById('precio');
  const traficoEl = document.getElementById('trafico');
  const convEl = document.getElementById('conversion');
  const comisionEl = document.getElementById('comision');
  const valPrecio = document.getElementById('valPrecio');
  const valTrafico = document.getElementById('valTrafico');
  const valConv = document.getElementById('valConv');
  const valComision = document.getElementById('valComision');
  const resultadoEl = document.getElementById('resultado');
  const detalleEl = document.getElementById('detalle');

  function actualizarCalc() {
    const precio = parseFloat(precioEl.value);
    const trafico = parseInt(traficoEl.value);
    const conv = parseFloat(convEl.value) / 100;
    const comision = parseFloat(comisionEl.value) / 100;
    const ventas = trafico * conv;
    const bruto = ventas * precio;
    const neto = bruto * (1 - comision);

    valPrecio.textContent = precio;
    valTrafico.textContent = trafico;
    valConv.textContent = convEl.value;
    valComision.textContent = comisionEl.value;

    resultadoEl.textContent = '€' + neto.toFixed(0).replace(/\B(?=(\d{3})+(?!\d))/g, '.');
    detalleEl.textContent = ventas.toFixed(1) + ' ventas · comisión del ' + comisionEl.value + '%';
  }

  [precioEl, traficoEl, convEl, comisionEl].forEach(el => el.addEventListener('input', actualizarCalc));
  actualizarCalc();

  // ===== GRÁFICO AUTOMATIZACIÓN =====
  const ctxAuto = document.getElementById('chartAuto').getContext('2d');
  new Chart(ctxAuto, {
    type: 'bar',
    data: {
      labels: ['Micro-eBooks', 'Newsletters', 'Descripciones', 'SEO', 'Recepcionista AI', 'Leads B2B', 'YouTube', 'Miniaturas'],
      datasets: [{
        label: '% de automatización',
        data: [95, 90, 90, 85, 88, 85, 80, 82],
        backgroundColor: [
          'rgba(99,102,241,.8)', 'rgba(34,211,238,.8)', 'rgba(16,185,129,.8)',
          'rgba(245,158,11,.8)', 'rgba(139,92,246,.8)', 'rgba(236,72,153,.8)',
          'rgba(20,184,166,.8)', 'rgba(249,115,22,.8)'
        ],
        borderColor: ['#6366f1','#22d3ee','#10b981','#f59e0b','#8b5cf6','#ec4899','#14b8a6','#f97316'],
        borderWidth: 1.5, borderRadius: 8
      }]
    },
    options: {
      indexAxis: 'y', responsive: true, maintainAspectRatio: false,
      plugins: { legend: { display: false } },
      scales: {
        x: { beginAtZero: true, max: 100, ticks: { color: '#8fa3c0', callback: v => v + '%' }, grid: { color: 'rgba(30,42,66,.6)' } },
        y: { ticks: { color: '#8fa3c0', font: { size: 10 } }, grid: { display: false } }
      }
    }
  });

  // ===== GRÁFICO TIEMPO =====
  const ctxTiempo = document.getElementById('chartTiempo').getContext('2d');
  new Chart(ctxTiempo, {
    type: 'bar',
    data: {
      labels: ['Micro-eBooks', 'Newsletters', 'Descripciones', 'SEO', 'Recepcionista AI', 'Leads B2B', 'YouTube', 'Miniaturas'],
      datasets: [{
        label: 'Semanas hasta 1er ingreso',
        data: [1.5, 3, 1, 8, 3, 2.5, 8, 1],
        backgroundColor: [
          'rgba(99,102,241,.7)', 'rgba(34,211,238,.7)', 'rgba(16,185,129,.7)',
          'rgba(245,158,11,.7)', 'rgba(139,92,246,.7)', 'rgba(236,72,153,.7)',
          'rgba(20,184,166,.7)', 'rgba(249,115,22,.7)'
        ],
        borderColor: ['#6366f1','#22d3ee','#10b981','#f59e0b','#8b5cf6','#ec4899','#14b8a6','#f97316'],
        borderWidth: 1.5, borderRadius: 8
      }]
    },
    options: {
      indexAxis: 'y', responsive: true, maintainAspectRatio: false,
      plugins: { legend: { display: false } },
      scales: {
        x: { beginAtZero: true, ticks: { color: '#8fa3c0', callback: v => v + ' sem' }, grid: { color: 'rgba(30,42,66,.6)' } },
        y: { ticks: { color: '#8fa3c0', font: { size: 10 } }, grid: { display: false } }
      }
    }
  });

  // ===== ANIMACIÓN METERS =====
  const meterObserver = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        const fill = entry.target.querySelector('.meter-fill');
        if (fill) { const w = fill.style.width; fill.style.width = '0%'; setTimeout(() => { fill.style.width = w; }, 200); }
        meterObserver.unobserve(entry.target);
      }
    });
  }, { threshold: 0.3 });
  document.querySelectorAll('.meter').forEach(m => meterObserver.observe(m));

  // ============================================================
  // ============ NUEVAS FUNCIONALIDADES ========================
  // ============================================================

  // ===== TOAST =====
  const toast = document.getElementById('toast');
  function showToast(msg, color) {
    toast.textContent = msg;
    toast.style.background = color || 'var(--green)';
    toast.classList.add('show');
    setTimeout(() => toast.classList.remove('show'), 2200);
  }

  // ===== TEMA CLARO/OSCURO =====
  const themeBtn = document.getElementById('themeBtn');
  const savedTheme = localStorage.getItem('iaHubTheme') || 'dark';
  document.documentElement.setAttribute('data-theme', savedTheme === 'light' ? 'light' : 'dark');
  themeBtn.textContent = savedTheme === 'light' ? '☀️' : '🌙';

  themeBtn.addEventListener('click', () => {
    const current = document.documentElement.getAttribute('data-theme');
    const next = current === 'light' ? 'dark' : 'light';
    document.documentElement.setAttribute('data-theme', next);
    themeBtn.textContent = next === 'light' ? '☀️' : '🌙';
    localStorage.setItem('iaHubTheme', next);
  });

  // ===== FAVORITOS =====
  const FAV_KEY = 'iaHubFavs';
  function getFavs() {
    try { return JSON.parse(localStorage.getItem(FAV_KEY)) || []; }
    catch(e) { return []; }
  }
  function saveFavs(arr) { localStorage.setItem(FAV_KEY, JSON.stringify(arr)); }

  function updateFavCount() {
    const count = getFavs().length;
    const badge = document.getElementById('favCount');
    badge.textContent = count;
    badge.classList.toggle('show', count > 0);
  }

  function renderFavs() {
    const favs = getFavs();
    const body = document.getElementById('favBody');
    if (favs.length === 0) {
      body.innerHTML = '<div class="drawer-empty">Aún no tienes favoritos.<br>Pulsa la ⭐ en cualquier modelo o forma para guardarlo aquí.</div>';
      return;
    }
    body.innerHTML = favs.map(f => `
      <div class="fav-entry">
        <div class="fav-type">${f.type}</div>
        <div class="fav-title">${f.title}</div>
        ${f.link ? `<a href="${f.link}" target="_blank">Abrir herramienta ↗</a>` : ''}
        <div class="fav-actions">
          <button data-remove="${f.id}">Eliminar</button>
        </div>
      </div>
    `).join('');
    body.querySelectorAll('[data-remove]').forEach(btn => {
      btn.addEventListener('click', () => {
        const id = btn.getAttribute('data-remove');
        const newFavs = getFavs().filter(x => x.id !== id);
        saveFavs(newFavs);
        syncFavBtns();
        renderFavs();
        updateFavCount();
        showToast('Eliminado de favoritos', 'var(--red)');
      });
    });
  }

  function syncFavBtns() {
    const favs = getFavs();
    const ids = new Set(favs.map(f => f.id));
    document.querySelectorAll('.fav-btn[data-fav-id]').forEach(btn => {
      const id = btn.getAttribute('data-fav-id');
      if (ids.has(id)) btn.classList.add('active');
      else btn.classList.remove('active');
    });
  }

  function toggleFav(btn) {
    const id = btn.getAttribute('data-fav-id');
    const type = btn.getAttribute('data-fav-type') || 'Elemento';
    const title = btn.getAttribute('data-fav-title') || 'Sin título';
    const link = btn.getAttribute('data-fav-link') || '';
    let favs = getFavs();
    const exists = favs.find(f => f.id === id);
    if (exists) {
      favs = favs.filter(f => f.id !== id);
      showToast('Eliminado de favoritos', 'var(--red)');
    } else {
      favs.push({ id, type, title, link });
      showToast('⭐ Añadido a favoritos', 'var(--green)');
    }
    saveFavs(favs);
    syncFavBtns();
    renderFavs();
    updateFavCount();
  }

  document.querySelectorAll('.fav-btn[data-fav-id]').forEach(btn => {
    btn.addEventListener('click', (e) => {
      e.stopPropagation();
      e.preventDefault();
      toggleFav(btn);
    });
  });

  document.getElementById('favOpenBtn').addEventListener('click', () => {
    document.getElementById('favDrawer').classList.add('open');
    renderFavs();
  });
  document.getElementById('favCloseBtn').addEventListener('click', () => {
    document.getElementById('favDrawer').classList.remove('open');
  });

  updateFavCount();
  syncFavBtns();
  renderFavs();

  // ===== PROMPTS COPIABLES =====
  document.querySelectorAll('.copy-btn').forEach(btn => {
    btn.addEventListener('click', async (e) => {
      e.preventDefault();
      const promptText = btn.closest('.prompt-block').querySelector('.prompt-text').textContent;
      try {
        await navigator.clipboard.writeText(promptText);
        const original = btn.textContent;
        btn.textContent = '✓ Copiado';
        btn.classList.add('copied');
        setTimeout(() => { btn.textContent = original; btn.classList.remove('copied'); }, 1800);
        showToast('Prompt copiado al portapapeles', 'var(--green)');
      } catch (err) {
        showToast('No se pudo copiar', 'var(--red)');
      }
    });
  });

  // ===== BUSCADOR + FILTROS =====
  const searchInput = document.getElementById('searchInput');
  const filterCat = document.getElementById('filterCat');
  const filterDiff = document.getElementById('filterDiff');
  const filterAuto = document.getElementById('filterAuto');
  const visibleCount = document.getElementById('visibleCount');

  function applyFilters() {
    const q = searchInput.value.toLowerCase().trim();
    const cat = filterCat.value;
    const diff = filterDiff.value;
    const autoMin = filterAuto.value ? parseInt(filterAuto.value) : 0;
    let visible = 0;
    document.querySelectorAll('.forma-item').forEach(item => {
      const text = item.querySelector('.forma-content span').textContent.toLowerCase();
      const itemCat = item.getAttribute('data-cat');
      const itemDiff = item.getAttribute('data-diff');
      const itemAuto = parseInt(item.getAttribute('data-auto'));
      const matchQ = !q || text.includes(q);
      const matchCat = !cat || itemCat === cat;
      const matchDiff = !diff || itemDiff === diff;
      const matchAuto = !autoMin || itemAuto >= autoMin;
      if (matchQ && matchCat && matchDiff && matchAuto) {
        item.classList.remove('hidden');
        visible++;
      } else {
        item.classList.add('hidden');
      }
    });
    visibleCount.textContent = visible;
  }

  [searchInput, filterCat, filterDiff, filterAuto].forEach(el => {
    el.addEventListener('input', applyFilters);
    el.addEventListener('change', applyFilters);
  });

  // ===== QUIZ RECOMENDADOR =====
  const quizQuestions = [
    {
      q: '¿Cuánto tiempo puedes dedicar a la semana?',
      opts: [
        { text: 'Poco (menos de 5 h)', weights: { 'descripciones': 3, 'miniaturas': 3, 'micro-ebooks': 2 } },
        { text: 'Medio (5-15 h)', weights: { 'micro-ebooks': 3, 'newsletters': 3, 'leads': 2 } },
        { text: 'Mucho (más de 15 h)', weights: { 'seo': 3, 'youtube': 3, 'cursos': 2 } }
      ]
    },
    {
      q: '¿Qué prefieres hacer?',
      opts: [
        { text: 'Escribir y editar texto', weights: { 'micro-ebooks': 3, 'newsletters': 3, 'seo': 2, 'descripciones': 2 } },
        { text: 'Crear cosas visuales o de audio', weights: { 'youtube': 3, 'miniaturas': 3 } },
        { text: 'Automatizar procesos y hablar con clientes', weights: { 'recepcionista': 3, 'leads': 3, 'cursos': 1 } }
      ]
    },
    {
      q: '¿Te gusta hablar con clientes?',
      opts: [
        { text: 'Sí, me gusta tratar con gente', weights: { 'recepcionista': 3, 'leads': 3, 'descripciones': 1 } },
        { text: 'Prefiero no hablar con nadie', weights: { 'micro-ebooks': 3, 'newsletters': 3, 'seo': 2, 'miniaturas': 2 } }
      ]
    },
    {
      q: '¿Quieres resultados rápidos o construir a largo plazo?',
      opts: [
        { text: 'Rápidos (semanas)', weights: { 'descripciones': 3, 'miniaturas': 3, 'micro-ebooks': 2 } },
        { text: 'Largo plazo (meses, más rentable)', weights: { 'seo': 3, 'newsletters': 3, 'youtube': 3 } }
      ]
    },
    {
      q: '¿Cuánto puedes invertir al principio?',
      opts: [
        { text: 'Nada (0 €)', weights: { 'micro-ebooks': 3, 'descripciones': 3, 'newsletters': 3, 'miniaturas': 2 } },
        { text: 'Algo (hasta 50 €)', weights: { 'cursos': 2, 'youtube': 2, 'leads': 2 } }
      ]
    }
  ];

  const modelInfo = {
    'micro-ebooks': { name: 'Micro-eBooks y guías', icon: '📚', desc: 'Creas guías de 20-40 páginas sobre un nicho concreto y las vendes en Gumroad. Automatización del 95%, resultados en 1-2 semanas.', link: 'https://gumroad.com/' },
    'newsletters': { name: 'Newsletters de nicho', icon: '📧', desc: 'Boletines especializados con suscripción gratuita o de pago. Contenido generado por IA y enviado automáticamente. Resultados en 2-4 semanas.', link: 'https://substack.com/' },
    'descripciones': { name: 'Descripciones de productos', icon: '🛒', desc: 'Paquetes de 20-50 descripciones para tiendas online. Servicio puntual o suscripción. Resultados en 1 semana.', link: 'https://www.shopify.com/' },
    'seo': { name: 'Contenido SEO para blogs', icon: '📝', desc: 'Artículos optimizados que generan tráfico y se monetizan con afiliados o publicidad. Resultados en 1-3 meses.', link: 'https://koala.sh/' },
    'recepcionista': { name: 'Recepcionista AI para negocios', icon: '📞', desc: 'Agentes de voz/chat que contestan llamadas, califican clientes y agendan citas para negocios locales. Resultados en 2-4 semanas.', link: 'https://aiindigo.com/' },
    'leads': { name: 'Generación de leads B2B', icon: '🎯', desc: 'Encuentras emails verificados y datos de contacto para equipos de ventas usando IA. Resultados en 2-3 semanas.', link: 'https://www.apollo.io/' },
    'youtube': { name: 'Canales de YouTube sin rostro', icon: '🎬', desc: 'Vídeos educativos o de nicho generados con IA y monetizados con ads. Resultados en 1-3 meses.', link: 'https://invideo.io/' },
    'miniaturas': { name: 'Diseño de miniaturas', icon: '🎨', desc: 'Miniaturas de alto CTR para youtubers usando IA generativa. Servicio recurrente y muy demandado. Resultados en 1 semana.', link: 'https://www.canva.com/' },
    'cursos': { name: 'Cursos online con IA', icon: '🎓', desc: 'Cursos creados con IA (guion, diapositivas, voz) sobre temas demandados. Resultados en 2-4 semanas.', link: 'https://hotmart.com/' }
  };

  let quizIndex = 0;
  let quizScores = {};

  function renderQuiz() {
    const box = document.getElementById('quizBox');
    if (quizIndex >= quizQuestions.length) {
      // Resultado
      let best = null, bestScore = -1;
      for (const k in quizScores) {
        if (quizScores[k] > bestScore) { bestScore = quizScores[k]; best = k; }
      }
      const info = modelInfo[best];
      box.innerHTML = `
        <div class="quiz-result">
          <div class="rec-icon">${info.icon}</div>
          <h3>Te recomendamos: ${info.name}</h3>
          <p>${info.desc}</p>
          <a href="${info.link}" target="_blank" class="btn btn-primary">Empezar con esta herramienta →</a>
          <button class="btn btn-ghost" id="quizRestart">Repetir el quiz</button>
        </div>
      `;
      document.getElementById('quizRestart').addEventListener('click', () => {
        quizIndex = 0; quizScores = {}; renderQuiz();
      });
      return;
    }

    const q = quizQuestions[quizIndex];
    const progress = (quizIndex / quizQuestions.length) * 100;
    box.innerHTML = `
      <div class="quiz-progress"><div class="quiz-progress-fill" style="width:${progress}%"></div></div>
      <div class="quiz-step-label">Pregunta ${quizIndex + 1} de ${quizQuestions.length}</div>
      <div class="quiz-question">${q.q}</div>
      <div class="quiz-options">
        ${q.opts.map((o, i) => `<button class="quiz-option" data-opt="${i}">${o.text}</button>`).join('')}
      </div>
    `;
    box.querySelectorAll('.quiz-option').forEach(btn => {
      btn.addEventListener('click', () => {
        const opt = q.opts[parseInt(btn.getAttribute('data-opt'))];
        for (const k in opt.weights) {
          quizScores[k] = (quizScores[k] || 0) + opt.weights[k];
        }
        quizIndex++;
        renderQuiz();
      });
    });
  }
  renderQuiz();

  // ===== DEMO IA EN VIVO =====
  const demoBtn = document.getElementById('demoBtn');
  const demoPrompt = document.getElementById('demoPrompt');
  const demoOutput = document.getElementById('demoOutput');
  const demoModel = document.getElementById('demoModel');

  demoBtn.addEventListener('click', async () => {
    const prompt = demoPrompt.value.trim();
    if (!prompt) {
      showToast('Escribe un prompt primero', 'var(--amber)');
      return;
    }
    demoOutput.classList.add('loading');
    demoOutput.textContent = 'Generando respuesta... (puede tardar unos segundos)';
    demoBtn.disabled = true;
    demoBtn.textContent = 'Generando...';
    try {
      const model = demoModel.value;
      const url = `https://text.pollinations.ai/${encodeURIComponent(prompt)}?model=${model}`;
      const res = await fetch(url);
      if (!res.ok) throw new Error('HTTP ' + res.status);
      let text = await res.text();
      // Pollinations a veces devuelve JSON si se pide con ?json, aquí devuelve texto plano
      demoOutput.textContent = text.trim() || '(Respuesta vacía)';
      demoOutput.classList.remove('loading');
    } catch (err) {
      demoOutput.classList.remove('loading');
      demoOutput.textContent = '❌ Error: no se pudo conectar con la API. Puede estar saturada. Prueba de nuevo en unos segundos o cambia el modelo.';
    } finally {
      demoBtn.disabled = false;
      demoBtn.textContent = 'Generar →';
    }
  });

  // ===== ROADMAP 30 DÍAS =====
  const roadmapData = [
    { day: 'Día 1', title: 'Elegir un modelo de negocio', desc: 'Haz el quiz o revisa el comparador. Elige UNO solo.' },
    { day: 'Día 2', title: 'Elegir un nicho hiperconcreto', desc: 'Cuanto más específico, mejor. Apunta a un público real.' },
    { day: 'Día 3', title: 'Investigar la competencia', desc: 'Busca 5 competidores en tu nicho y analiza qué hacen bien y qué mal.' },
    { day: 'Día 4', title: 'Definir tu oferta', desc: 'Qué vendes, a quién, a qué precio y con qué promesa concreta.' },
    { day: 'Día 5', title: 'Crear el primer borrador con IA', desc: 'Usa los prompts de esta web para generar el contenido base.' },
    { day: 'Día 6', title: 'Revisar y editar el contenido', desc: 'Añade tu voz, corrige errores y asegura calidad. Sin esto, no publiques.' },
    { day: 'Día 7', title: 'Diseñar la portada o presentación', desc: 'Con Canva gratis. No necesitas ser diseñador: limpio y claro es suficiente.' },
    { day: 'Día 8', title: 'Crear cuenta en la plataforma de venta', desc: 'Gumroad, Substack o la que hayas elegido. Configura el perfil.' },
    { day: 'Día 9', title: 'Subir el producto', desc: 'Publica con título, descripción, precio y archivo listo para descargar.' },
    { day: 'Día 10', title: 'Crear la landing de venta', desc: 'Usa el prompt de landing que tienes en la sección de modelos.' },
    { day: 'Día 11', title: 'Configurar email marketing', desc: 'ConvertKit o Substack gratuito. Captura emails desde el día 1.' },
    { day: 'Día 12', title: 'Configurar la automatización', desc: 'Con Make o Zapier: conecta tu nube con la plataforma de venta.' },
    { day: 'Día 13', title: 'Elegir 3 canales de captación', desc: 'Reddit, LinkedIn, grupos de Discord, foros de tu nicho. Elige 3 y comprométete.' },
    { day: 'Día 14', title: 'Publicar en el primer canal', desc: 'Comparte tu producto con contexto y valor, no solo el enlace.' },
    { day: 'Día 15', title: 'Publicar en el segundo canal', desc: 'Adapta el mensaje al tono de cada comunidad.' },
    { day: 'Día 16', title: 'Publicar en el tercer canal', desc: 'Documenta qué funciona y qué no en cada uno.' },
    { day: 'Día 17', title: 'Analizar primeras métricas', desc: 'Visitas, conversión, ventas. Instala analítica si no lo has hecho.' },
    { day: 'Día 18', title: 'Ajustar precio o mensaje', desc: 'Según los datos. No tengas miedo de cambiar.' },
    { day: 'Día 19', title: 'Crear el segundo producto', desc: 'Reutiliza el proceso. Ahora tardarás la mitad.' },
    { day: 'Día 20', title: 'Construir el hábito', desc: 'Publica, mide, ajusta, repite. Los resultados llegan con la constancia.' }
  ];

  const RM_KEY = 'iaHubRoadmap';
  function getRmState() {
    try { return JSON.parse(localStorage.getItem(RM_KEY)) || {}; }
    catch(e) { return {}; }
  }
  function saveRmState(s) { localStorage.setItem(RM_KEY, JSON.stringify(s)); }

  function renderRoadmap() {
    const state = getRmState();
    const list = document.getElementById('rmList');
    list.innerHTML = roadmapData.map((item, i) => {
      const done = state[i] ? 'checked' : '';
      const cls = state[i] ? 'done' : '';
      return `<div class="roadmap-item ${cls}" data-idx="${i}">
        <input type="checkbox" ${done} data-idx="${i}">
        <div>
          <div class="rm-day">${item.day}</div>
          <div class="rm-title">${item.title}</div>
          <div class="rm-desc">${item.desc}</div>
        </div>
      </div>`;
    }).join('');
    list.querySelectorAll('input[type=checkbox]').forEach(cb => {
      cb.addEventListener('change', () => {
        const idx = cb.getAttribute('data-idx');
        const s = getRmState();
        s[idx] = cb.checked;
        saveRmState(s);
        const item = cb.closest('.roadmap-item');
        item.classList.toggle('done', cb.checked);
        updateRoadmapProgress();
      });
    });
    updateRoadmapProgress();
  }

  function updateRoadmapProgress() {
    const state = getRmState();
    const done = Object.values(state).filter(Boolean).length;
    const total = roadmapData.length;
    const pct = Math.round((done / total) * 100);
    document.getElementById('rmDone').textContent = done;
    document.getElementById('rmTotal').textContent = total;
    document.getElementById('rmPercent').textContent = pct + '%';
    document.getElementById('rmFill').style.width = pct + '%';
  }

  renderRoadmap();

  // ===== PLANTILLAS DESCARGABLES =====
  const plantillas = {
    checklist: `CHECKLIST 30 DÍAS PARA TU NEGOCIO CON IA GRATIS
=================================================

${roadmapData.map((r, i) => `[ ] ${r.day}: ${r.title}\n    ${r.desc}`).join('\n\n')}

-------------------------------------------------
Descargado desde el Hub de Negocios IA.
`,
    prompt: `PLANTILLA DE PROMPT MAESTRO
=============================

Estructura recomendada para cualquier prompt:

1. ROL
   "Actúa como [experto en X] con [años] de experiencia en [nicho]."

2. CONTEXTO
   "Mi público objetivo es [descripción]. Mi producto es [qué].
    Mi tono debe ser [cercano/profesional/directo]."

3. TAREA
   "Genera [entregable concreto: esquema, artículo, guion...]
    con las siguientes especificaciones: [longitud, formato, estructura]."

4. RESTRICCIONES
   "No uses [palabras prohibidas]. Evita [tono inadecuado].
    Incluye [elementos obligatorios]."

5. FORMATO DE SALIDA
   "Devuelve el resultado en [Markdown / lista / tabla / JSON]."

6. EJEMPLO (opcional pero muy útil)
   "Aquí tienes un ejemplo del estilo que quiero: [ejemplo]."

-------------------------------------------------
Consejo: cuanto más específico, mejor resultado.
Descargado desde el Hub de Negocios IA.
`,
    apis: `COMPARATIVA DE APIs GRATUITAS (2026)
=====================================

1. PUTER.JS
   URL: https://developer.puter.com/
   Modelos: GPT-6, Claude, Gemini, Mistral
   Límite: Sin límite para el desarrollador
   Ideal para: apps web, prototipos, herramientas internas

2. POLLINATIONS.AI
   URL: https://pollinations.ai/
   Modelos: OpenAI, Mistral, Gemini
   Límite: Sin límite de tasa (posible lentitud)
   Ideal para: demos, prototipos rápidos, pruebas

3. KEYLESSAI
   URL: https://keylessai.thryx.workers.dev/v1
   Modelos: Múltiples vía failover
   Límite: ~100.000 peticiones/día
   Ideal para: scripts, agentes, clientes OpenAI

4. OPENROUTER
   URL: https://openrouter.ai/
   Modelos: 20+ gratuitos (DeepSeek, Llama...)
   Límite: 50 peticiones/día gratis
   Ideal para: variedad de modelos con una sola clave

5. GROQ
   URL: https://console.groq.com/
   Modelos: Llama, Mixtral, Gemma, GPT-OSS
   Límite: 30 RPM, 1.000/día, 200K tokens/día
   Ideal para: velocidad, prototipos en producción

6. CLOUDFLARE WORKERS AI
   URL: https://developers.cloudflare.com/workers-ai/
   Modelos: Llama, Gemma, Whisper
   Límite: 10.000 Neurons/día
   Ideal para: edge, apps globales, sin tarjeta

-------------------------------------------------
Descargado desde el Hub de Negocios IA.
`,
    calc: `CALCULADORA DE GANANCIAS (FÓRMULA)
===================================

Ventas = Visitantes × Tasa de conversión
Ingreso bruto = Ventas × Precio
Ingreso neto = Ingreso bruto × (1 - Comisión)

EJEMPLO:
- Precio: 19 €
- Visitantes/mes: 500
- Conversión: 3% → 0,03
- Comisión: 10% → 0,10

Ventas = 500 × 0,03 = 15
Ingreso bruto = 15 × 19 = 285 €
Ingreso neto = 285 × 0,90 = 256,50 €/mes

RANGOS REALISTAS PARA PRINCIPIANTES:
- Mes 1-2: 0-200 €/mes
- Mes 3-4: 200-800 €/mes
- Mes 5-6: 500-2.000 €/mes
- A partir del mes 6: 2.000 €+/mes con constancia

-------------------------------------------------
Descargado desde el Hub de Negocios IA.
`
  };

  document.querySelectorAll('.dl-btn').forEach(btn => {
    btn.addEventListener('click', () => {
      const key = btn.getAttribute('data-dl');
      const content = plantillas[key];
      if (!content) return;
      const blob = new Blob([content], { type: 'text/plain;charset=utf-8' });
      const url = URL.createObjectURL(blob);
      const a = document.createElement('a');
      a.href = url;
      a.download = `ia-hub-${key}.txt`;
      document.body.appendChild(a);
      a.click();
      document.body.removeChild(a);
      URL.revokeObjectURL(url);
      showToast('📥 Plantilla descargada', 'var(--green)');
    });
  });
</script>

</body>
</html>
