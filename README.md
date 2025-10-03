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
.card{background:rgba(255,255,255,.02);border:1px solid var(--linea);border-radius:var(--radius);padding:14px}
.items{display:grid;gap:6px}
.item{display:grid;grid-template-columns:1fr auto;gap:10px;padding:10px 0;border-bottom:1px dashed var(--linea);align-items:start}
.item:last-child{border-bottom:0}
.name{font-family:'Times New Roman', Georgia, serif;font-size:18px}
.desc{font-size:13.5px;color:var(--crema-2)}
.price{font-variant-numeric:tabular-nums;color:#E6D8AE;white-space:nowrap}
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
      <input id="q" type="search" placeholder="Buscar plato, queso o bebida">
    </div>
    <div class="pills-inline">
      <a class="pill" href="#quesos">Quesos</a>
      <a class="pill" href="#cocina">Cocina</a>
      <a class="pill" href="#barra">Barra</a>
    </div>
  </div>
</header>

<main class="container">
  <section class="section" id="quesos"><div class="card">
    <h3 class="serif">Quesos</h3>
    <div class="items">
      <div class="item"><div><div class="name serif">Cuartirolo</div><div class="desc">Leche de vaca; sabor suave y cremoso.</div></div><div class="price">$7.000</div></div>
      <div class="item"><div><div class="name serif">Parmesano 24 meses</div><div class="desc">Grana amplio; cristales de tirosina.</div></div><div class="price">$11.000</div></div>
    </div>
  </div></section>

  <section class="section" id="cocina"><div class="card">
    <h3 class="serif">Cocina Porte</h3>
    <div class="items">
      <div class="item"><div><div class="name serif">Raclette</div><div class="desc">Peras, pickles y cebolla sobre pan de campo.</div></div><div class="price">$16.000</div></div>
      <div class="item"><div><div class="name serif">Corte vacuno</div><div class="desc">Con papas fritas y salsa Café de París.</div></div><div class="price">$29.000</div></div>
    </div>
  </div></section>

  <section class="section" id="barra"><div class="card">
    <h3 class="serif">Barra</h3>
    <div class="items">
      <div class="item"><div><div class="name serif">Old Fashioned</div><div class="desc">Benchmark N°8, azúcar, angostura, naranja.</div></div><div class="price">$13.500</div></div>
      <div class="item"><div><div class="name serif">Negroni</div><div class="desc">Clásico italiano.</div></div><div class="price">$9.500</div></div>
    </div>
  </div></section>
</main>

<a id="toTop" href="#top">↑</a>

<nav class="bottom-nav">
  <a href="#quesos" id="bn-menu" class="active">Menú</a>
  <a href="#cocina" id="bn-vinos">Cocina</a>
  <a href="#barra" id="bn-cocteles">Barra</a>
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
