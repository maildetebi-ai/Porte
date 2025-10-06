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
:root{--bg:#23271F;--bg-2:#1C2018;--crema:#EDE7D8;--crema-2:#CFC7B3;--linea:#3B3F35;--dorado:#D8B545;--radius:18px;--bn-h:64px}
*{box-sizing:border-box}
html{scroll-behavior:smooth;-webkit-text-size-adjust:100%}
body{margin:0;background:linear-gradient(180deg,var(--bg),var(--bg-2) 60%);color:var(--crema);
  font-family:-apple-system, ui-sans-serif, Inter, Arial;line-height:1.6;overflow-x:hidden;
  padding-bottom:calc(var(--bn-h) + env(safe-area-inset-bottom,0px));
  padding-left:env(safe-area-inset-left);padding-right:env(safe-area-inset-right);
  overscroll-behavior-y:none}
.serif{font-family:'Times New Roman', Georgia, serif}
.container{max-width:920px;margin:0 auto;padding:0 20px}
a{text-decoration:none;color:inherit}
.hero{min-height:48svh;display:grid;place-items:center;padding:40px 0 12px;border-bottom:1px solid var(--linea)}
.logo{font-size:clamp(44px,12vw,78px);letter-spacing:.06em}
.search{display:flex;gap:10px;align-items:center;background:rgba(255,255,255,.04);border:1px solid var(--linea);
  border-radius:999px;padding:12px 16px}
.search input{flex:1;background:transparent;border:0;outline:none;color:var(--crema)}
.pills-inline{display:flex;gap:10px;overflow-x:auto;padding-bottom:6px;scrollbar-width:none;-webkit-overflow-scrolling:touch}
.pill{flex:0 0 auto;min-height:44px;padding:10px 16px;border-radius:999px;background:rgba(216,181,69,.14);border:1px solid rgba(216,181,69,.35);white-space:nowrap}
.pill.active{background:rgba(216,181,69,.28)}
.section{padding:6px 0 14px;border-bottom:1px solid var(--linea);scroll-margin-top:calc(var(--bn-h) + 24px)}
.card{background:rgba(255,255,255,.02);border:1px solid var(--linea);border-radius:var(--radius);padding:18px}
.items{display:grid;gap:6px}
.item{display:grid;grid-template-columns:1fr auto;gap:12px;padding:10px 0;border-bottom:1px dashed var(--linea);align-items:start}
.item:last-child{border-bottom:0}
.details{display:grid;gap:4px}
.name{font-family:'Times New Roman', Georgia, serif;font-size:18px}
.desc{font-size:13.5px;color:var(--crema-2)}
.price{font-variant-numeric:tabular-nums;color:#E6D8AE;white-space:nowrap}
.price-stack{display:grid;gap:6px;justify-items:end;font-variant-numeric:tabular-nums}
.price-stack .label{display:inline-block;margin-right:8px;color:var(--crema-2);font-size:12px;text-transform:uppercase;letter-spacing:.08em}
.price-stack div{display:flex;gap:8px;align-items:center;justify-content:flex-end}
.wine-grid{display:grid;gap:18px}
@media(min-width:780px){.wine-grid{grid-template-columns:repeat(2,1fr);gap:24px}}
.bottom-nav{position:fixed;left:0;right:0;bottom:0;z-index:45;background:rgba(28,32,24,.94);backdrop-filter:blur(6px);
  border-top:1px solid var(--linea);display:grid;grid-template-columns:repeat(3,1fr);height:var(--bn-h);
  padding-bottom:env(safe-area-inset-bottom,0px)}
.bottom-nav a{display:grid;place-items:center;color:#D6CCA9;font-size:14px}
.bottom-nav a.active{color:#EAE4D2;border-top:3px solid var(--dorado)}
#toTop{position:fixed;right:16px;bottom:calc(var(--bn-h) + 24px);border-radius:999px;border:1px solid var(--linea);
  background:rgba(255,255,255,.03);padding:10px 12px;color:#EAE4D2;display:none}
#toTop.show{display:inline-block}
</style>
</head>
<body>

<header class="hero" id="top">
  <div class="container">
    <div class="serif logo">PORTE</div>
    <p class="serif">Un rincón íntimo, cercano, pensado para ser vivido con todos los sentidos.</p>
    <div class="search">
      <input id="q" type="search" placeholder="Buscar en la carta">
    </div>
    <div class="pills-inline">
      <a class="pill" href="#aperitivos">Aperitivos</a>
      <a class="pill" href="#quesos">Quesos</a>
      <a class="pill" href="#entradas">Entradas</a>
      <a class="pill" href="#principales">Principales</a>
      <a class="pill" href="#postres">Postres</a>
      <a class="pill" href="#vinos">Vinos</a>
      <a class="pill" href="#espirituosos">Espirituosos</a>
    </div>
  </div>
</header>

<main class="container">
  <section class="section" id="aperitivos"><div class="card">
    <h3 class="serif">Aperitivos</h3>
    <div class="items">
      <div class="item"><div class="details"><div class="name serif">Ramazzotti Rosato Tonic</div></div><div class="price">$4.500</div></div>
      <div class="item"><div class="details"><div class="name serif">Lillet Rosé &amp; Soda</div></div><div class="price">$4.500</div></div>
      <div class="item"><div class="details"><div class="name serif">Cocchi Americano &amp; Soda</div></div><div class="price">$4.500</div></div>
      <div class="item"><div class="details"><div class="name serif">Vermut casero, soda, naranja</div></div><div class="price">$3.800</div></div>
      <div class="item"><div class="details"><div class="name serif">Cynar Julep</div></div><div class="price">$4.800</div></div>
      <div class="item"><div class="details"><div class="name serif">Sbagliatto</div></div><div class="price">$4.800</div></div>
    </div>
  </div></section>

  <section class="section" id="quesos"><div class="card">
    <h3 class="serif">Quesos</h3>
    <div class="items">
      <div class="item"><div class="details"><div class="name serif">Cuartirolo</div></div><div class="price">$7.000</div></div>
      <div class="item"><div class="details"><div class="name serif">Saint Maure</div></div><div class="price">$9.000</div></div>
      <div class="item"><div class="details"><div class="name serif">Brie</div></div><div class="price">$9.000</div></div>
      <div class="item"><div class="details"><div class="name serif">Gorgonzola Dolce</div></div><div class="price">$9.000</div></div>
      <div class="item"><div class="details"><div class="name serif">Manchego</div></div><div class="price">$11.000</div></div>
      <div class="item"><div class="details"><div class="name serif">Queso de Cabra</div></div><div class="price">$9.000</div></div>
      <div class="item"><div class="details"><div class="name serif">Selección Porte (4 quesos)</div></div><div class="price">$18.000</div></div>
    </div>
  </div></section>

  <section class="section" id="entradas"><div class="card">
    <h3 class="serif">Entradas</h3>
    <div class="items">
      <div class="item"><div class="details"><div class="name serif">Sopa fría de remolacha, yogur &amp; pepino</div></div><div class="price">$6.800</div></div>
      <div class="item"><div class="details"><div class="name serif">Burrata, tomates confitados &amp; pesto de pistacho</div></div><div class="price">$9.200</div></div>
      <div class="item"><div class="details"><div class="name serif">Carpaccio de hongos, parmesano &amp; aceite de trufa</div></div><div class="price">$8.700</div></div>
      <div class="item"><div class="details"><div class="name serif">Tostón de ricotta batida, higos asados &amp; miel</div></div><div class="price">$7.600</div></div>
    </div>
  </div></section>

  <section class="section" id="principales"><div class="card">
    <h3 class="serif">Principales</h3>
    <div class="items">
      <div class="item"><div class="details"><div class="name serif">Raclette, peras asadas, pepinillos &amp; pan de masa madre</div></div><div class="price">$16.800</div></div>
      <div class="item"><div class="details"><div class="name serif">Pesca del día, emulsión cítrica &amp; finas hierbas</div></div><div class="price">$23.000</div></div>
      <div class="item"><div class="details"><div class="name serif">Gnocchi de sémola gratinados, ragú de hongos</div></div><div class="price">$18.000</div></div>
      <div class="item"><div class="details"><div class="name serif">Corte vacuno, papas fritas &amp; salsa Café de París</div></div><div class="price">$29.000</div></div>
    </div>
  </div></section>

  <section class="section" id="postres"><div class="card">
    <h3 class="serif">Postres</h3>
    <div class="items">
      <div class="item"><div class="details"><div class="name serif">Pavlova de frutos rojos</div></div><div class="price">$6.500</div></div>
      <div class="item"><div class="details"><div class="name serif">Mousse de chocolate, oliva &amp; sal marina</div></div><div class="price">$6.200</div></div>
      <div class="item"><div class="details"><div class="name serif">Cheesecake de queso azul &amp; peras</div></div><div class="price">$6.800</div></div>
    </div>
  </div></section>

  <section class="section" id="vinos"><div class="card">
    <h3 class="serif">Vinos</h3>
    <div class="wine-grid">
      <div>
        <h4 class="serif">Blancos</h4>
        <div class="items">
          <div class="item wine-item"><div class="details"><div class="name serif">Costa &amp; Pampa Sauvignon Blanc</div><div class="desc">Chapadmalal, Buenos Aires</div></div><div class="price-stack"><div><span class="label">Copa</span><span class="price">$2.800</span></div><div><span class="label">Botella</span><span class="price">$13.500</span></div></div></div>
          <div class="item wine-item"><div class="details"><div class="name serif">Riccitelli Old Vines Semillón</div><div class="desc">Río Negro</div></div><div class="price-stack"><div><span class="label">Copa</span><span class="price">$3.100</span></div><div><span class="label">Botella</span><span class="price">$15.000</span></div></div></div>
          <div class="item wine-item"><div class="details"><div class="name serif">Pulenta Estate Chardonnay</div><div class="desc">Valle de Uco</div></div><div class="price-stack"><div><span class="label">Copa</span><span class="price">$3.300</span></div><div><span class="label">Botella</span><span class="price">$16.500</span></div></div></div>
        </div>
        <h4 class="serif">Rosados</h4>
        <div class="items">
          <div class="item wine-item"><div class="details"><div class="name serif">Lagarde Goes Pink</div><div class="desc">Luján de Cuyo</div></div><div class="price-stack"><div><span class="label">Copa</span><span class="price">$3.000</span></div><div><span class="label">Botella</span><span class="price">$14.500</span></div></div></div>
        </div>
      </div>
      <div>
        <h4 class="serif">Tintos</h4>
        <div class="items">
          <div class="item wine-item"><div class="details"><div class="name serif">Proyecto Hermanas Pinot Noir</div><div class="desc">Patagonia</div></div><div class="price-stack"><div><span class="label">Copa</span><span class="price">$3.200</span></div><div><span class="label">Botella</span><span class="price">$15.800</span></div></div></div>
          <div class="item wine-item"><div class="details"><div class="name serif">Riccitelli Old Vines Malbec</div><div class="desc">Luján de Cuyo</div></div><div class="price-stack"><div><span class="label">Copa</span><span class="price">$3.300</span></div><div><span class="label">Botella</span><span class="price">$16.500</span></div></div></div>
          <div class="item wine-item"><div class="details"><div class="name serif">Luigi Bosca De Sangre Cabernet Franc</div><div class="desc">Valle de Uco</div></div><div class="price-stack"><div><span class="label">Copa</span><span class="price">$3.400</span></div><div><span class="label">Botella</span><span class="price">$17.200</span></div></div></div>
          <div class="item wine-item"><div class="details"><div class="name serif">Pulenta Estate Gran Cabernet Sauvignon</div><div class="desc">Agrelo</div></div><div class="price-stack"><div><span class="label">Copa</span><span class="price">$3.500</span></div><div><span class="label">Botella</span><span class="price">$18.500</span></div></div></div>
        </div>
        <h4 class="serif">Espumosos</h4>
        <div class="items">
          <div class="item wine-item"><div class="details"><div class="name serif">Rosell Boher Extra Brut</div><div class="desc">Valle de Uco</div></div><div class="price-stack"><div><span class="label">Copa</span><span class="price">$3.100</span></div><div><span class="label">Botella</span><span class="price">$15.500</span></div></div></div>
          <div class="item wine-item"><div class="details"><div class="name serif">Alpamanta Bubbles Pet Nat</div><div class="desc">Luján de Cuyo</div></div><div class="price-stack"><div><span class="label">Copa</span><span class="price">$3.500</span></div><div><span class="label">Botella</span><span class="price">$17.500</span></div></div></div>
        </div>
      </div>
    </div>
  </div></section>

  <section class="section" id="espirituosos"><div class="card">
    <h3 class="serif">Espirituosos</h3>
    <div class="items">
      <div class="item"><div class="details"><div class="name serif">Gin Heraclito London Dry</div></div><div class="price">$4.500</div></div>
      <div class="item"><div class="details"><div class="name serif">Gin Príncipe de los Apóstoles</div></div><div class="price">$4.700</div></div>
      <div class="item"><div class="details"><div class="name serif">Vodka 42 Below</div></div><div class="price">$4.200</div></div>
      <div class="item"><div class="details"><div class="name serif">Tequila Tromba Blanco</div></div><div class="price">$5.200</div></div>
      <div class="item"><div class="details"><div class="name serif">Bourbon Wild Turkey 101</div></div><div class="price">$5.000</div></div>
      <div class="item"><div class="details"><div class="name serif">Whisky Chivas 13</div></div><div class="price">$5.300</div></div>
      <div class="item"><div class="details"><div class="name serif">Ron Plantation 5 años</div></div><div class="price">$4.500</div></div>
      <div class="item"><div class="details"><div class="name serif">Fernet Branca</div></div><div class="price">$3.000</div></div>
    </div>
  </div></section>
</main>

<a id="toTop" href="#top">↑</a>

<nav class="bottom-nav">
  <a href="#aperitivos" id="bn-aperitivos" class="active">Aperitivos</a>
  <a href="#principales" id="bn-principales">Cocina</a>
  <a href="#vinos" id="bn-vinos">Bodega</a>
</nav>

<script>
const toTop=document.getElementById('toTop');
window.addEventListener('scroll',()=>{toTop.classList.toggle('show',window.scrollY>280)},{passive:true});
const q=document.getElementById('q');
q.addEventListener('input',e=>{
  const t=e.target.value.toLowerCase();
  document.querySelectorAll('.item').forEach(it=>{
    it.style.display=it.textContent.toLowerCase().includes(t)?'':'none';
  });
});
</script>
</body>
</html>
