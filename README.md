# Porte
Menu
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Porte · Carta</title>
<meta name="theme-color" content="#23271F">
<style>
:root{
  --bg:#23271F; --bg-2:#20241C; --crema:#EDE7D8; --crema-2:#CFC7B3;
  --linea:#3B3F35; --dorado:#D8B545; --radius:18px;
  --shadow:0 1px 0 rgba(0,0,0,.25), 0 12px 28px rgba(0,0,0,.25);
}
*{box-sizing:border-box}
html{scroll-behavior:smooth;-webkit-text-size-adjust:100%}
body{
  margin:0;background:linear-gradient(180deg,var(--bg),#1C2018 60%);
  color:var(--crema);
  font-family:-apple-system, ui-sans-serif, BlinkMacSystemFont, "Helvetica Neue", Inter, Arial, system-ui, sans-serif;
  line-height:1.6;
  padding-left:env(safe-area-inset-left);padding-right:env(safe-area-inset-right);
  -webkit-font-smoothing:antialiased; -moz-osx-font-smoothing:grayscale;
}
.serif{font-family:"Times New Roman", Georgia, serif}
.container{max-width:760px;margin:0 auto;padding:0 clamp(16px,3vw,24px)}
a{color:inherit;text-decoration:none}
:focus-visible{outline:2px solid var(--dorado);outline-offset:3px}
@media (prefers-reduced-motion: reduce){*{animation-duration:.001ms!important;animation-iteration-count:1!important;transition-duration:.001ms!important;scroll-behavior:auto!important}}

/* HERO */
.hero{min-height:54svh;display:grid;place-items:center;padding:48px 0 12px;border-bottom:1px solid var(--linea);
  background:radial-gradient(40% 50% at 50% 0%, rgba(216,181,69,.12), rgba(216,181,69,0) 70%)}
.hero-inner{width:100%;display:grid;gap:14px}
.brand-top a{display:inline-grid;place-items:center;width:40px;height:40px;border-radius:999px;border:1px solid var(--linea);color:var(--crema-2)}
.brand-top a:hover{background:rgba(255,255,255,.03)}
.logo{font-size:clamp(44px,12vw,78px);letter-spacing:.06em;line-height:1;font-weight:400}
.tagline{color:var(--crema-2);max-width:70ch}

/* Search & pills */
.search{display:flex;gap:10px;align-items:center;background:rgba(255,255,255,.04);border:1px solid var(--linea);
  border-radius:999px;padding:12px 16px;backdrop-filter: blur(2px)}
.search input{flex:1;border:0;outline:none;font-size:16px;background:transparent;color:var(--crema)}
.search svg{opacity:.8}
.filters-title{font-size:12px;letter-spacing:.08em;text-transform:uppercase;color:var(--crema-2);margin:8px 0 6px 6px}
.pills-inline{display:flex;gap:10px;overflow:auto;padding-bottom:4px;scrollbar-width:thin;scroll-snap-type:x mandatory;-webkit-overflow-scrolling:touch}
.pill{scroll-snap-align:start;flex:0 0 auto;min-height:42px;padding:10px 16px;border-radius:999px;
  background:rgba(216,181,69,.14);color:#E9DFBF;border:1px solid rgba(216,181,69,.35);font-weight:600}
.pill:is(:hover,:focus){background:rgba(216,181,69,.22)}
.pill.active{background:rgba(216,181,69,.34)}

/* Sticky pills */
.pills-wrap{position:sticky;top:0;z-index:40;background:linear-gradient(180deg, rgba(35,39,31,.96), rgba(35,39,31,.92));
  border-bottom:1px solid var(--linea);backdrop-filter: blur(6px);display:none;box-shadow:0 2px 12px rgba(0,0,0,.35)}
.pills{display:flex;gap:8px;overflow:auto;padding:8px clamp(12px,3vw,24px)}

/* Secciones */
.main{padding:16px 0 96px}
.section{padding:14px 0;border-bottom:1px solid var(--linea)}
.card{background:linear-gradient(180deg, rgba(255,255,255,.02), rgba(255,255,255,.00));border:1px solid var(--linea);border-radius:var(--radius);padding:18px;box-shadow:var(--shadow)}
.h2{display:flex;align-items:center;gap:12px;font-size:clamp(18px,2.6vw,22px);letter-spacing:.02em;color:#EAE4D2;margin:0 0 8px}
.icon{width:22px;height:22px;flex:0 0 22px;color:#E6D8AE}
.h3{font-size:15px;color:#D7CFB9;margin:10px 0 6px}
.items{display:grid;gap:6px}
.item{display:grid;grid-template-columns:1fr minmax(92px, auto);gap:10px;padding:10px 0;border-bottom:1px dashed var(--linea);align-items:start;min-height:46px}
.item:last-child{border-bottom:0}
.name{font-family:"Times New Roman", Georgia, serif;font-size:18px;letter-spacing:.01em}
.desc{font-size:13.5px;color:var(--crema-2);margin-top:4px}
.price{font-variant-numeric:tabular-nums;letter-spacing:.02em;color:#E6D8AE;align-self:center;text-align:right}
.section-nav{display:flex;justify-content:flex-end;gap:10px;margin-top:8px;flex-wrap:wrap}
.link-min{font-size:12px;color:#D6CCA9;border-bottom:1px solid rgba(216,181,69,.35);padding-bottom:2px}
.link-min:hover{border-color:var(--dorado)}

/* Bottom nav */
.bottom-nav{position:fixed;left:0;right:0;bottom:0;z-index:45;background:rgba(28,32,24,.92);backdrop-filter: blur(6px);
  border-top:1px solid var(--linea);display:grid;grid-template-columns:repeat(3,1fr)}
.bottom-nav a{padding:14px 8px;text-align:center;text-decoration:none;color:#D6CCA9;font-size:14px;font-family:"Times New Roman", Georgia, serif}
.bottom-nav a.active{color:#EAE4D2;border-top:3px solid var(--dorado)}

/* Back to top */
#toTop{position:fixed;right:16px;bottom:104px;z-index:50;border-radius:999px;border:1px solid var(--linea);background:rgba(255,255,255,.03);
  padding:10px 12px;text-decoration:none;color:#EAE4D2;box-shadow:0 10px 25px rgba(0,0,0,.35), 0 2px 6px rgba(0,0,0,.25);
  font-size:13px;display:none;min-height:44px;align-items:center}
#toTop.show{display:inline-flex;gap:6px}

/* Responsive */
@media (max-width: 380px){ .logo{font-size:42px} .pill{padding:8px 12px;font-size:13px} .name{font-size:17px} .desc{font-size:13px} }
@media (min-width: 960px){ .container{max-width:880px} .item{grid-template-columns:1fr minmax(120px, 200px)} }

/* Print */
@media print{
  body{background:#fff;color:#111}
  .hero,.pills-wrap,.bottom-nav,#toTop{display:none!important}
  .card{box-shadow:none;border-color:#ddd;background:#fff}
}
</style>
</head>
<body>
<!-- Sprite SVG -->
<svg width="0" height="0" style="position:absolute;visibility:hidden" aria-hidden="true">
  <symbol id="i-cheese-soft" viewBox="0 0 24 24"><path fill="currentColor" d="M3 9.5c0-.8.4-1.5 1-1.9L13 2.7c.6-.4 1.4-.4 2 0l6 3.6c.6.4 1 .9 1 1.6V10l-19 7.5V9.5Z"/><circle cx="9" cy="12" r="1.2" fill="#D8B545"/><circle cx="13.5" cy="10" r="1" fill="#D8B545"/></symbol>
  <symbol id="i-cheese-semi" viewBox="0 0 24 24"><path fill="currentColor" d="M3 10.5v7.3c0 .8.4 1.5 1.2 1.8l7.8 3c.6.2 1.3.2 1.9 0l7.8-3c.7-.3 1.2-1 1.2-1.8v-7.3L12 7 3 10.5Z"/><path d="M3 10.5 12 7l9 3.5" stroke="#D8B545" stroke-width="1"/></symbol>
  <symbol id="i-cheese-hard" viewBox="0 0 24 24"><path fill="currentColor" d="M2.5 11.5 12 6l9.5 5.5v5.4c0 .7-.4 1.4-1 1.7l-8 4.3c-.9.5-2 .5-2.9 0l-8-4.3c-.6-.3-1-.9-1-1.7v-5.4Z"/><path d="M12 6v16.3" stroke="#D8B545" stroke-width="1.2"/></symbol>
  <symbol id="i-blue" viewBox="0 0 24 24"><path fill="currentColor" d="M4 18V7.5c0-.7.4-1.3 1-1.6l7-3.7c.6-.3 1.4-.3 2 0l7 3.7c.6.3 1 .9 1 1.6V18l-9-3-9 3Z"/><path d="M6 8l12 6M6 12l8 4" stroke="#D8B545" stroke-width="1.2"/></symbol>
  <symbol id="i-hot" viewBox="0 0 24 24"><path d="M12 3c2 2 3 3.7 3 5.5S13.7 12 12 12s-3-1.2-3-3S10 5 12 3Z" fill="currentColor"/><path d="M7 14c0 3 2.2 6 5 6s5-3 5-6" stroke="#D8B545" stroke-width="1.2" fill="none"/></symbol>
  <symbol id="i-cured" viewBox="0 0 24 24"><rect x="3" y="6" width="18" height="12" rx="3" fill="currentColor"/><circle cx="9" cy="12" r="1.3" fill="#FFF9F0"/><circle cx="13.5" cy="12" r="1.3" fill="#FFF9F0"/></symbol>
  <symbol id="i-fish" viewBox="0 0 24 24"><path fill="currentColor" d="M3 12c4-3 8-4 12-4 2 0 4 .5 6 1.5-1.5 3-4 6-6 7-4 0-8-1-12-4Z"/><circle cx="9" cy="11" r="1" fill="#FFF9F0"/></symbol>
  <symbol id="i-main" viewBox="0 0 24 24"><path d="M6 3v10M9 3v10" stroke="currentColor" stroke-width="2"/><rect x="13" y="3" width="2" height="10" fill="currentColor"/><path d="M4 18h16" stroke="#D8B545" stroke-width="1.2"/></symbol>
  <symbol id="i-dessert" viewBox="0 0 24 24"><path fill="currentColor" d="M4 14h16l-2 6H6l-2-6Zm2-4 6-5 6 5H6Z"/></symbol>
  <symbol id="i-cocktail" viewBox="0 0 24 24"><path d="M3 5h18l-7 7v6l3 1v1H7v-1l3-1v-6L3 5Z" fill="currentColor"/></symbol>
  <symbol id="i-wine" viewBox="0 0 24 24"><path d="M7 3h10l-1 7a6 6 0 0 1-8 0L7 3Zm5 10v6l3 1v1H9v-1l3-1v-6Z" fill="currentColor"/></symbol>
  <symbol id="i-bottle" viewBox="0 0 24 24"><path d="M10 2h4v3l2 2v13a3 3 0 0 1-3 3h-2a3 3 0 0 1-3-3V7l2-2V2Z" fill="currentColor"/></symbol>
  <symbol id="i-drink" viewBox="0 0 24 24"><path d="M5 4h14l-1 12a4 4 0 0 1-4 4H10a4 4 0 0 1-4-4L5 4Z" fill="currentColor"/></symbol>
</svg>

<header class="hero" id="top">
  <div class="container hero-inner">
    <div class="brand-top"><a href="#menu" aria-label="Volver"><svg width="16" height="16" viewBox="0 0 24 24"><path fill="currentColor" d="M15.4 7.4 14 6l-6 6 6 6 1.4-1.4L10.8 12z"/></svg></a></div>
    <div class="serif logo">PORTE</div>
    <p class="tagline serif">Porte es una invitación. Un rincón íntimo, cercano, pensado para ser vivido con los sentidos abiertos.</p>
    <div class="search" role="search" aria-label="Buscar en el menú">
      <svg width="18" height="18" viewBox="0 0 24 24" aria-hidden="true"><path fill="#D6CCA9" d="M15.5 14h-.79l-.28-.27A6.471 6.471 0 0016 9.5 6.5 6.5 0 109.5 16c1.61 0 3.09-.59 4.23-1.57l.27.28v.79l5 4.99L20.49 19l-4.99-5zm-6 0C7.01 14 5 11.99 5 9.5S7.01 5 9.5 5 14 7.01 14 9.5 11.99 14 9.5 14z"/></svg>
      <input id="q" type="search" placeholder="Buscar plato, queso o bebida" aria-label="Buscar">
    </div>
    <div class="filters-hero" aria-label="Categorías">
      <p class="filters-title serif">Categorías</p>
      <div class="pills-inline">
        <a class="pill" href="#quesos-de-pasta-blanda">Quesos: Blanda</a>
        <a class="pill" href="#quesos-de-pasta-semi-dura">Quesos: Semi-dura</a>
        <a class="pill" href="#quesos-de-pasta-dura">Quesos: Dura</a>
        <a class="pill" href="#azules">Azules</a>
        <a class="pill" href="#quesos-calientes">Calientes</a>
        <a class="pill" href="#charcuteria-artesanal">Charcutería</a>
        <a class="pill" href="#mar-tierra">Mar & Tierra</a>
        <a class="pill" href="#platos-principales">Principales</a>
        <a class="pill" href="#postres">Postres</a>
        <a class="pill" href="#cocteles">Cócteles</a>
        <a class="pill" href="#vinos-por-copa">Vinos (copa)</a>
        <a class="pill" href="#vinos-por-botella">Vinos (botella)</a>
        <a class="pill" href="#bebidas">Bebidas</a>
      </div>
    </div>
  </div>
</header>

<nav class="pills-wrap" id="sticky-nav" role="navigation" aria-label="Secciones del menú">
  <div class="pills">
    <a class="pill" href="#quesos-de-pasta-blanda">Quesos: Blanda</a>
    <a class="pill" href="#quesos-de-pasta-semi-dura">Quesos: Semi-dura</a>
    <a class="pill" href="#quesos-de-pasta-dura">Quesos: Dura</a>
    <a class="pill" href="#azules">Azules</a>
    <a class="pill" href="#quesos-calientes">Calientes</a>
    <a class="pill" href="#charcuteria-artesanal">Charcutería</a>
    <a class="pill" href="#mar-tierra">Mar & Tierra</a>
    <a class="pill" href="#platos-principales">Principales</a>
    <a class="pill" href="#postres">Postres</a>
    <a class="pill" href="#cocteles">Cócteles</a>
    <a class="pill" href="#vinos-por-copa">Vinos (copa)</a>
    <a class="pill" href="#vinos-por-botella">Vinos (botella)</a>
    <a class="pill" href="#bebidas">Bebidas</a>
  </div>
</nav>

<main id="menu" class="main container">
  <!-- QUESOS BLANDA -->
  <section class="section" id="quesos-de-pasta-blanda"><div class="card">
    <h2 class="h2 serif"><svg class="icon"><use href="#i-cheese-soft"/></svg>Quesos de pasta blanda</h2>
    <div class="items">
      <div class="item"><div class="txt"><div class="name serif">Cuartirolo (El Abascay, Buenos Aires)</div></div><div class="price">$7.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Lincoln (La Suerte, Buenos Aires)</div></div><div class="price">$7.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Rebleusson (Fermier, Buenos Aires)</div></div><div class="price">$7.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Morbier (Fermier, Buenos Aires)</div></div><div class="price">$7.000</div></div>
    </div>
    <div class="section-nav"><a class="link-min" href="#top">↑ Portada</a><a class="link-min" href="#menu">↺ Menú</a></div>
  </div></section>

  <!-- QUESOS SEMI-DURA -->
  <section class="section" id="quesos-de-pasta-semi-dura"><div class="card">
    <h2 class="h2 serif"><svg class="icon"><use href="#i-cheese-semi"/></svg>Quesos de pasta semi-dura</h2>
    <div class="items">
      <div class="item"><div class="txt"><div class="name serif">Blanco danés (La Boheme, Córdoba)</div></div><div class="price">$7.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Raclette (Fermier, Buenos Aires)</div></div><div class="price">$7.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Camembert de cabra (La Boheme, Córdoba)</div></div><div class="price">$7.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Crottin de Cabra (Piedras Blancas, Buenos Aires)</div></div><div class="price">$7.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Coeur de Cabra (Piedras Blancas, Buenos Aires)</div></div><div class="price">$7.000</div></div>
    </div>
    <div class="section-nav"><a class="link-min" href="#top">↑ Portada</a><a class="link-min" href="#menu">↺ Menú</a></div>
  </div></section>

  <!-- QUESOS DURA -->
  <section class="section" id="quesos-de-pasta-dura"><div class="card">
    <h2 class="h2 serif"><svg class="icon"><use href="#i-cheese-hard"/></svg>Quesos de pasta dura</h2>
    <div class="items">
      <div class="item"><div class="txt"><div class="name serif">Fontina estilo italiano (Fermier, Buenos Aires)</div></div><div class="price">$8.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Pecorino (Weke, Buenos Aires)</div></div><div class="price">$8.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Cheddar Inglés (La Suerte, Buenos Aires)</div></div><div class="price">$11.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Cuatro Esquinas (Ventimiglia, Río Negro)</div></div><div class="price">$11.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Especial Parmesano 24 meses (Vaquero, Buenos Aires)</div></div><div class="price">$11.000</div></div>
    </div>
    <div class="section-nav"><a class="link-min" href="#top">↑ Portada</a><a class="link-min" href="#menu">↺ Menú</a></div>
  </div></section>

  <!-- AZULES -->
  <section class="section" id="azules"><div class="card">
    <h2 class="h2 serif"><svg class="icon"><use href="#i-blue"/></svg>Azules</h2>
    <div class="items">
      <div class="item"><div class="txt"><div class="name serif">Azul Gourmet (Toro Azul, Córdoba)</div></div><div class="price">$8.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Blue Couly (Ventimiglia, Río Negro)</div></div><div class="price">$11.000</div></div>
    </div>
    <div class="section-nav"><a class="link-min" href="#top">↑ Portada</a><a class="link-min" href="#menu">↺ Menú</a></div>
  </div></section>

  <!-- CALIENTES -->
  <section class="section" id="quesos-calientes"><div class="card">
    <h2 class="h2 serif"><svg class="icon"><use href="#i-hot"/></svg>Quesos calientes</h2>
    <div class="items">
      <div class="item"><div class="txt"><div class="name serif">Raclette</div><div class="desc">Peras, pepinillos y cebolla sobre pan de campo.</div></div><div class="price">$16.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Tartifle</div><div class="desc">Reblochon, papas, nabo y panceta (ensalada verde).</div></div><div class="price">$18.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Queso Wellington</div><div class="desc">Vacheroleau y frutos secos en hojaldre, coulis de frambuesas (hojas verdes).</div></div><div class="price">$23.000</div></div>
    </div>
    <div class="section-nav"><a class="link-min" href="#top">↑ Portada</a><a class="link-min" href="#menu">↺ Menú</a></div>
  </div></section>

  <!-- CHARCUTERÍA -->
  <section class="section" id="charcuteria-artesanal"><div class="card">
    <h2 class="h2 serif"><svg class="icon"><use href="#i-cured"/></svg>Charcutería artesanal</h2>
    <div class="items">
      <div class="item"><div class="txt"><div class="name serif">Salame chacarero</div></div><div class="price">$7.500</div></div>
      <div class="item"><div class="txt"><div class="name serif">Spianatta con frutos secos</div></div><div class="price">$7.500</div></div>
      <div class="item"><div class="txt"><div class="name serif">Mortadela con pistachos</div></div><div class="price">$7.500</div></div>
      <div class="item"><div class="txt"><div class="name serif">Jamón crudo especial</div></div><div class="price">$9.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Cecina Angus</div></div><div class="price">$9.500</div></div>
      <div class="item"><div class="txt"><div class="name serif">Ración de olivas encurtidas y marinadas</div></div><div class="price">$4.500</div></div>
      <div class="item"><div class="txt"><div class="name serif">Ración de pan y aceite de oliva</div></div><div class="price">$3.500</div></div>
    </div>
    <div class="section-nav"><a class="link-min" href="#top">↑ Portada</a><a class="link-min" href="#menu">↺ Menú</a></div>
  </div></section>

  <!-- MAR & TIERRA -->
  <section class="section" id="mar-tierra"><div class="card">
    <h2 class="h2 serif"><svg class="icon"><use href="#i-fish"/></svg>Mar & Tierra</h2>
    <div class="items">
      <div class="item"><div class="txt"><div class="name serif">Anchoas, cebolla morada, manteca y oliva</div></div><div class="price">$9.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Pulpo, papas y salsa americana</div></div><div class="price">$40.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Pato crispy con crema de ají amarillo</div></div><div class="price">$23.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Papas con Cheddar</div></div><div class="price">$8.500</div></div>
      <div class="item"><div class="txt"><div class="name serif">Coliflor, yogurt y ají amarillo</div></div><div class="price">$7.500</div></div>
    </div>
    <div class="section-nav"><a class="link-min" href="#top">↑ Portada</a><a class="link-min" href="#menu">↺ Menú</a></div>
  </div></section>

  <!-- PRINCIPALES -->
  <section class="section" id="platos-principales"><div class="card">
    <h2 class="h2 serif"><svg class="icon"><use href="#i-main"/></svg>Platos principales</h2>
    <div class="items">
      <div class="item"><div class="txt"><div class="name serif">Pesca del Atlántico</div><div class="desc">Beurre blanc anisada, puré de cebollas y vegetales confitados.</div></div><div class="price">$26.500</div></div>
      <div class="item"><div class="txt"><div class="name serif">Lasagnette de hongos</div><div class="desc">Pasta al huevo, hongos salteados, bechamel y parmesano.</div></div><div class="price">$25.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Parmentier de cordero</div><div class="desc">Cordero braseado, demiglace y puré gratinado con queso.</div></div><div class="price">$27.500</div></div>
      <div class="item"><div class="txt"><div class="name serif">Corte vacuno 250 g / 500 g</div><div class="desc">Papas fritas y salsa Café de París.</div></div><div class="price">$28.000 / 48.000</div></div>
    </div>
    <div class="section-nav"><a class="link-min" href="#top">↑ Portada</a><a class="link-min" href="#menu">↺ Menú</a></div>
  </div></section>

  <!-- POSTRES -->
  <section class="section" id="postres"><div class="card">
    <h2 class="h2 serif"><svg class="icon"><use href="#i-dessert"/></svg>Postres</h2>
    <div class="items">
      <div class="item"><div class="txt"><div class="name serif">Affogato</div><div class="desc">Helado de sabayón, espresso, nueces pecan caramelizadas.</div></div><div class="price">$11.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Plato de quesos y dulces</div></div><div class="price">$12.500</div></div>
      <div class="item"><div class="txt"><div class="name serif">Tarta de queso</div><div class="desc">Blend vaca/cabra, mermelada de estación.</div></div><div class="price">$14.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Moelleux de chocolate</div><div class="desc">Con helado de vainilla y quinotos.</div></div><div class="price">$11.000</div></div>
    </div>
    <div class="section-nav"><a class="link-min" href="#top">↑ Portada</a><a class="link-min" href="#menu">↺ Menú</a></div>
  </div></section>

  <!-- CÓCTELES -->
  <section class="section" id="cocteles"><div class="card">
    <h2 class="h2 serif"><svg class="icon"><use href="#i-cocktail"/></svg>Cócteles</h2>
    <div class="subgroup"><h3 class="h3 serif">De autor</h3><div class="items">
      <div class="item"><div class="txt"><div class="name serif">Mi Rosa</div></div><div class="price">$10.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Asteroide B612</div></div><div class="price">$12.500</div></div>
      <div class="item"><div class="txt"><div class="name serif">Saint Exupery</div></div><div class="price">$12.500</div></div>
      <div class="item"><div class="txt"><div class="name serif">Boababs</div></div><div class="price">$10.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Sahara (sin alcohol)</div></div><div class="price">$8.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Volcán extinguido (sin alcohol)</div></div><div class="price">$8.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Pozo del desierto (sin alcohol)</div></div><div class="price">$8.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">El zorro (sin alcohol)</div></div><div class="price">$8.000</div></div>
    </div></div>
    <div class="subgroup"><h3 class="h3 serif">Clásicos</h3><div class="items">
      <div class="item"><div class="txt"><div class="name serif">Old Fashioned</div></div><div class="price">$12.500</div></div>
      <div class="item"><div class="txt"><div class="name serif">Adonis</div></div><div class="price">$11.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Bloody Mary</div></div><div class="price">$11.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Greta Garbo</div></div><div class="price">$11.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Penicillin</div></div><div class="price">$11.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Side Car</div></div><div class="price">$11.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">French 75</div></div><div class="price">$10.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Bellini</div></div><div class="price">$10.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Mai Tai</div></div><div class="price">$10.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Espresso Martini</div></div><div class="price">$11.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Cosmopolitan</div></div><div class="price">$11.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Old Cuban</div></div><div class="price">$10.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Negroni / Gin & Tonic / Aperol Spritz / Fernet</div></div><div class="price">$9.500</div></div>
    </div></div>
    <div class="section-nav"><a class="link-min" href="#top">↑ Portada</a><a class="link-min" href="#menu">↺ Menú</a></div>
  </div></section>

  <!-- VINOS COPA -->
  <section class="section" id="vinos-por-copa"><div class="card">
    <h2 class="h2 serif"><svg class="icon"><use href="#i-wine"/></svg>Vinos por copa</h2>
    <div class="items">
      <div class="item"><div class="txt"><div class="name serif">Phillippe Caraguel Extra Brut NV</div></div><div class="price">$6.500</div></div>
      <div class="item"><div class="txt"><div class="name serif">Passion de los Andes 2024 (Sauvignon Blanc)</div></div><div class="price">$7.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Bianco D'Uco 2024 (Malvasía)</div></div><div class="price">$9.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Serbal 2024 (Chardonnay)</div></div><div class="price">$6.500</div></div>
      <div class="item"><div class="txt"><div class="name serif">Trasciende 2024 (Torrontés)</div></div><div class="price">$13.500</div></div>
      <div class="item"><div class="txt"><div class="name serif">Lisa Rosé IGP Méditerranée 2024</div></div><div class="price">$11.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Sacha Tigre Criolla Quebradeña 2024</div></div><div class="price">$10.500</div></div>
      <div class="item"><div class="txt"><div class="name serif">La Cayetana 2024 (Malbec)</div></div><div class="price">$11.500</div></div>
      <div class="item"><div class="txt"><div class="name serif">Passion de los Andes Coll. 2024 (Cabernet Sauvignon)</div></div><div class="price">$7.500</div></div>
      <div class="item"><div class="txt"><div class="name serif">Tanito 2024 (blend)</div></div><div class="price">$7.000</div></div>
    </div>
    <div class="section-nav"><a class="link-min" href="#top">↑ Portada</a><a class="link-min" href="#menu">↺ Menú</a></div>
  </div></section>

  <!-- VINOS BOTELLA -->
  <section class="section" id="vinos-por-botella"><div class="card">
    <h2 class="h2 serif"><svg class="icon"><use href="#i-bottle"/></svg>Vinos por botella</h2>
    <div class="items">
      <div class="item"><div class="txt"><div class="name serif">Phillippe Caraguel Extra Brut NV</div></div><div class="price">$25.700</div></div>
      <div class="item"><div class="txt"><div class="name serif">Phillippe Caraguel Rosé Extra Brut NV</div></div><div class="price">$25.700</div></div>
      <div class="item"><div class="txt"><div class="name serif">Passion de los Andes 2024 (Sauvignon Blanc)</div></div><div class="price">$18.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Serbal 2024 (Chardonnay)</div></div><div class="price">$20.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Bianco D'Uco 2024 (Malvasía)</div></div><div class="price">$31.500</div></div>
      <div class="item"><div class="txt"><div class="name serif">La Coste de los Andes 2023 (Chardonnay)</div></div><div class="price">$47.500</div></div>
      <div class="item"><div class="txt"><div class="name serif">45 Rugientes 2024 (Gewurz/PinotGris/Chardonnay)</div></div><div class="price">$53.750</div></div>
      <div class="item"><div class="txt"><div class="name serif">Catalpa 2024 (Pinot Noir)</div></div><div class="price">$34.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">45 Rugientes 2024 (Pinot Noir)</div></div><div class="price">$53.750</div></div>
      <div class="item"><div class="txt"><div class="name serif">La Cayetana 2024 (Malbec)</div></div><div class="price">$33.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Ovum 2024 (Cabernet Franc)</div></div><div class="price">$29.600</div></div>
      <div class="item"><div class="txt"><div class="name serif">Edad Moderna 2024 (Cabernet Sauvignon)</div></div><div class="price">$33.500</div></div>
      <div class="item"><div class="txt"><div class="name serif">Tanito 2024 (blend)</div></div><div class="price">$25.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Rosso D’Uco 2024 (Sangiovese/Syrah/Merlot)</div></div><div class="price">$25.000</div></div>
    </div>
    <div class="section-nav"><a class="link-min" href="#top">↑ Portada</a><a class="link-min" href="#menu">↺ Menú</a></div>
  </div></section>

  <!-- BEBIDAS -->
  <section class="section" id="bebidas"><div class="card">
    <h2 class="h2 serif"><svg class="icon"><use href="#i-drink"/></svg>Bebidas</h2>
    <div class="items">
      <div class="item"><div class="txt"><div class="name serif">Agua</div></div><div class="price">$3.500</div></div>
      <div class="item"><div class="txt"><div class="name serif">Agua con gas</div></div><div class="price">$3.500</div></div>
      <div class="item"><div class="txt"><div class="name serif">Agua Perrier</div></div><div class="price">$7.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Gaseosas</div></div><div class="price">$3.500</div></div>
      <div class="item"><div class="txt"><div class="name serif">Grolsch</div></div><div class="price">$7.000</div></div>
      <div class="item"><div class="txt"><div class="name serif">Guinness Extra Stout</div></div><div class="price">$9.000</div></div>
    </div>
    <div class="section-nav"><a class="link-min" href="#top">↑ Portada</a><a class="link-min" href="#menu">↺ Menú</a></div>
  </div></section>
</main>

<a id="toTop" href="#top" aria-label="Volver arriba">↑</a>

<nav class="bottom-nav" aria-label="Accesos rápidos">
  <a href="#menu" id="bn-menu" class="active">Menú</a>
  <a href="#vinos-por-copa" id="bn-vinos">Vinos</a>
  <a href="#cocteles" id="bn-cocteles">Cócteles</a>
</nav>

<script>
const sticky = document.getElementById('sticky-nav');
const toTop = document.getElementById('toTop');
const heroHeight = document.querySelector('.hero').offsetHeight;
function onScroll(){
  const y = window.scrollY || window.pageYOffset;
  sticky.style.display = (y > heroHeight - 60) ? 'block' : 'none';
  if (y > 280) toTop.classList.add('show'); else toTop.classList.remove('show');
}
window.addEventListener('scroll', onScroll, {passive:true}); onScroll();

// Active pill por sección
const sections = [...document.querySelectorAll('main .section')];
const pills = [...document.querySelectorAll('.pill')];
const iobs = new IntersectionObserver((entries) => {
  entries.forEach(e => {
    if (e.isIntersecting) {
      const id = e.target.id;
      pills.forEach(p => {
        const href = p.getAttribute('href');
        p.classList.toggle('active', href === '#' + id);
      });
    }
  });
}, {rootMargin: '-20% 0px -70% 0px', threshold: 0.1});
sections.forEach(s => iobs.observe(s));

// Bottom nav activo
const idsMap = new Map([['bn-menu','menu'],['bn-vinos','vinos-por-copa'],['bn-cocteles','cocteles']]);
const iobs2 = new IntersectionObserver((entries) => {
  entries.forEach(e => {
    if (e.isIntersecting) {
      const id = e.target.id;
      for (const [key, val] of idsMap) {
        document.getElementById(key).classList.toggle('active', id === val);
      }
    }
  });
}, {rootMargin: '-30% 0px -60% 0px', threshold: 0.1});
['menu','vinos-por-copa','cocteles'].forEach(id => { const el = document.getElementById(id); if (el) iobs2.observe(el); });

// Búsqueda en vivo
const q = document.getElementById('q');
q.addEventListener('input', (e) => {
  const term = e.target.value.toLowerCase().trim();
  sections.forEach(sec => {
    const items = sec.querySelectorAll('.item');
    let visibleCount = 0;
    items.forEach(it => {
      const txt = it.textContent.toLowerCase();
      const show = !term || txt.includes(term);
      it.style.display = show ? '' : 'none';
      if (show) visibleCount++;
    });
    sec.style.display = (visibleCount === 0 && term) ? 'none' : '';
  });
});
</script>
</body>
</html>
