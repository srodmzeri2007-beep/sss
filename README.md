[Maison Verde – Clothing Brand.html](https://github.com/user-attachments/files/33964969/Maison.Verde.Clothing.Brand.html)

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Maison Verde – Clothing Brand</title>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,500;0,600;1,500&family=Jost:wght@300;400;500&display=swap">
<style>
:root{
  --green-900:#06231a; --green-800:#0a3125; --green-700:#0f4332;
  --gold:#d4a62a; --gold-soft:#e8c45a; --white:#fbf8ef; --muted:#b9c7bd;
  --ease:cubic-bezier(.22,.8,.24,1);
  --serif:"Cormorant Garamond",Georgia,"Times New Roman",serif;
  --sans:"Jost","Helvetica Neue",Arial,sans-serif;
  color-scheme:dark;
}
*{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth;height:100%}
:root{padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
html{scroll-padding-top:90px}
body{background:var(--green-900);color:var(--white);font-family:var(--sans);font-weight:300;line-height:1.7;overflow-x:hidden;
  background-image:radial-gradient(circle at 80% 0%,rgba(212,166,42,.08),transparent 45%)}
a{color:inherit;text-decoration:none}
button{font:inherit;color:inherit;cursor:pointer;background:none;border:0}
:focus-visible{outline:2px solid var(--gold);outline-offset:3px}
h1,h2,h3{font-family:var(--serif);font-weight:500;line-height:1.1}
.wrap{width:min(1120px,92%);margin-inline:auto}

/* NAV */
header{position:sticky;top:env(safe-area-inset-top,0px);z-index:20;background:rgba(6,35,26,.88);backdrop-filter:blur(10px);border-bottom:1px solid var(--gold)}
.nav{display:flex;align-items:center;justify-content:space-between;height:76px}
.logo{display:flex;align-items:center;gap:12px}
.logo svg{width:46px;height:46px;transition:transform .6s var(--ease)}
.logo:hover svg{transform:rotate(-6deg) scale(1.08)}
.logo span{font-family:var(--serif);font-size:1.5rem;letter-spacing:.14em;color:var(--gold-soft)}
nav ul{display:flex;gap:34px;list-style:none}
nav a{position:relative;padding:6px 0;font-size:.95rem;letter-spacing:.06em}
nav a::after{content:"";position:absolute;left:0;bottom:0;height:1px;width:100%;background:var(--gold);transform:scaleX(0);transform-origin:left;transition:transform .45s var(--ease)}
nav a:hover::after{transform:scaleX(1)}
.burger{display:none;width:44px;height:44px;border:1px solid var(--gold);border-radius:50%;position:relative}
.burger i{position:absolute;left:12px;right:12px;height:1px;background:var(--gold);transition:.4s var(--ease)}
.burger i:nth-child(1){top:16px}.burger i:nth-child(2){top:22px}.burger i:nth-child(3){top:28px}
.burger.open i:nth-child(1){top:22px;transform:rotate(45deg)}
.burger.open i:nth-child(2){opacity:0}
.burger.open i:nth-child(3){top:22px;transform:rotate(-45deg)}

/* BUTTONS */
.btn{display:inline-block;padding:14px 34px;border:1px solid var(--gold);color:var(--gold-soft);letter-spacing:.1em;position:relative;overflow:hidden;z-index:0;transition:color .5s var(--ease),transform .3s var(--ease)}
.btn::before{content:"";position:absolute;inset:0;background:var(--gold);transform:translateY(101%);transition:transform .5s var(--ease);z-index:-1}
.btn:hover{color:var(--green-900)}
.btn:hover::before{transform:translateY(0)}
.btn:active{transform:scale(.97)}

/* HERO */
.hero{min-height:calc(100vh - 76px);display:grid;place-items:center;text-align:center;padding:70px 0}
.hero-frame{border:1px solid var(--gold);padding:70px 32px 64px;position:relative;max-width:820px;animation:rise 1.2s var(--ease) both}
.hero-frame::before{content:"";position:absolute;inset:10px;border:1px solid rgba(212,166,42,.35);pointer-events:none}
.hero-crown{width:84px;margin:0 auto 22px;display:block}
.hero h1{font-size:clamp(2.6rem,7vw,5.2rem);color:var(--white)}
.hero h1 em{color:var(--gold-soft)}
.hero p{max-width:480px;margin:22px auto 34px;color:var(--muted)}
@keyframes rise{from{opacity:0;transform:translateY(30px)}to{opacity:1;transform:none}}

/* SECTIONS */
section{padding:100px 0}
.title{text-align:center;margin-bottom:46px}
.title h2{font-size:clamp(2rem,4.5vw,3rem)}
.title .line{width:70px;height:1px;background:var(--gold);margin:18px auto 0;position:relative}
.title .line::after{content:"";position:absolute;left:50%;top:-3px;width:7px;height:7px;background:var(--gold);transform:translateX(-50%) rotate(45deg)}

/* FILTER */
.filters{display:flex;justify-content:center;flex-wrap:wrap;gap:12px;margin-bottom:44px}
.chip{padding:9px 26px;border:1px solid rgba(212,166,42,.5);border-radius:40px;transition:.4s var(--ease);letter-spacing:.05em}
.chip:hover{border-color:var(--gold)}
.chip.active{background:var(--gold);color:var(--green-900);border-color:var(--gold)}

/* PRODUCTS */
.grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(240px,1fr));gap:26px}
.card{border:1px solid var(--gold);background:var(--green-800);cursor:pointer;text-align:left;display:block;width:100%;
  transition:opacity .5s var(--ease),transform .5s var(--ease),box-shadow .5s var(--ease)}
.card:hover{transform:translateY(-6px);box-shadow:0 18px 40px rgba(0,0,0,.35),0 0 0 1px var(--gold-soft)}
.card.hide{opacity:0;transform:scale(.92);pointer-events:none}
.card.gone{display:none}
.thumb{aspect-ratio:4/5;display:grid;place-items:center;background:linear-gradient(160deg,var(--green-700),var(--green-900));border-bottom:1px solid var(--gold)}
.thumb svg{width:55%;fill:none;stroke:var(--gold);stroke-width:1.6;stroke-linejoin:round;transition:transform .7s var(--ease)}
.card:hover .thumb svg{transform:scale(1.1) rotate(-3deg)}
.info{padding:18px 20px 22px;display:flex;justify-content:space-between;align-items:baseline;gap:10px}
.info h3{font-size:1.35rem}
.info b{color:var(--gold-soft);font-weight:400}

/* ABOUT */
.about{display:grid;grid-template-columns:1fr 1fr;gap:56px;align-items:center}
.about h2{font-size:clamp(2rem,4vw,2.8rem);margin-bottom:18px}
.about p{color:var(--muted);margin-bottom:16px}
.stats{display:grid;grid-template-columns:1fr 1fr;border:1px solid var(--gold)}
.stats div{padding:34px 20px;text-align:center;border:1px solid rgba(212,166,42,.4);margin:-1px 0 0 -1px}
.stats strong{display:block;font-family:var(--serif);font-size:2.6rem;color:var(--gold-soft);font-weight:500}
.stats span{color:var(--muted);font-size:.9rem}

/* CONTACT */
form{max-width:560px;margin:auto;display:grid;gap:16px}
input,textarea{width:100%;padding:14px 16px;background:transparent;border:1px solid rgba(212,166,42,.55);color:var(--white);font:inherit;transition:border-color .4s,box-shadow .4s}
input:focus,textarea:focus{outline:none;border-color:var(--gold-soft);box-shadow:0 0 0 3px rgba(212,166,42,.18)}
::placeholder{color:#8fa497}
.thanks{display:grid;grid-template-rows:0fr;transition:grid-template-rows .6s var(--ease)}
.thanks.show{grid-template-rows:1fr}
.thanks p{overflow:hidden;text-align:center;color:var(--gold-soft)}

footer{border-top:1px solid var(--gold);text-align:center;padding:40px 0;color:var(--muted);font-size:.9rem}
footer .logo{justify-content:center;margin-bottom:12px}

/* MODAL */
.modal{position:fixed;inset:0;z-index:50;display:grid;place-items:center;padding:20px;background:rgba(3,18,13,.82);backdrop-filter:blur(6px);opacity:0;visibility:hidden;transition:opacity .45s var(--ease),visibility .45s}
.modal.open{opacity:1;visibility:visible}
.sheet{width:min(780px,100%);max-height:90vh;overflow:auto;display:grid;grid-template-columns:1fr 1fr;background:var(--green-900);border:1px solid var(--gold);position:relative;transform:translateY(40px) scale(.96);transition:transform .55s var(--ease)}
.modal.open .sheet{transform:none}
.sheet .thumb{aspect-ratio:auto;min-height:320px;border-bottom:0;border-right:1px solid var(--gold)}
.sheet .body{padding:40px 30px}
.sheet h3{font-size:2rem;margin-bottom:6px}
.sheet .price{color:var(--gold-soft);font-size:1.3rem;margin-bottom:14px}
.sheet p{color:var(--muted);margin-bottom:18px}
.sizes{display:flex;gap:8px;margin-bottom:22px}
.sizes button{width:42px;height:42px;border:1px solid rgba(212,166,42,.5);transition:.35s var(--ease)}
.sizes button.on,.sizes button:hover{background:var(--gold);color:var(--green-900)}
.close{position:absolute;top:12px;right:12px;width:40px;height:40px;border:1px solid var(--gold);border-radius:50%;color:var(--gold-soft);font-size:1.2rem;transition:transform .5s var(--ease)}
.close:hover{transform:rotate(90deg)}

/* TOAST */
.toast{position:fixed;left:50%;bottom:calc(28px + env(safe-area-inset-bottom,0px));transform:translate(-50%,30px);opacity:0;background:var(--gold);color:var(--green-900);padding:12px 26px;z-index:60;transition:.5s var(--ease);pointer-events:none}
.toast.show{opacity:1;transform:translate(-50%,0)}

/* SCROLL REVEAL */
.reveal{opacity:0;transform:translateY(34px);transition:opacity .9s var(--ease),transform .9s var(--ease)}
.reveal.in{opacity:1;transform:none}

@media(max-width:820px){
  .burger{display:block}
  nav{position:absolute;top:100%;left:0;right:0;background:var(--green-900);border-bottom:1px solid var(--gold);max-height:0;overflow:hidden;transition:max-height .6s var(--ease)}
  nav.open{max-height:320px}
  nav ul{flex-direction:column;gap:0;padding:10px 0}
  nav li{text-align:center}
  nav a{display:block;padding:14px}
  .about,.sheet{grid-template-columns:1fr}
  .sheet .thumb{min-height:220px;border-right:0;border-bottom:1px solid var(--gold)}
  section{padding:70px 0}
}
@media(prefers-reduced-motion:reduce){*{animation:none!important;transition-duration:.01ms!important;scroll-behavior:auto!important}}
</style>
</head>
<body>

<!-- Reusable logo symbol: white crown above a gold monogram ring -->
<svg width="0" height="0" style="position:absolute" aria-hidden="true">
  <defs>
    <symbol id="logo" viewBox="0 0 100 100">
      <circle cx="50" cy="62" r="30" fill="none" stroke="#d4a62a" stroke-width="2.5"/>
      <circle cx="50" cy="62" r="25" fill="none" stroke="#d4a62a" stroke-width="1" opacity=".6"/>
      <text x="50" y="72" text-anchor="middle" font-family="Cormorant Garamond,Georgia,serif" font-size="30" font-weight="600" fill="#e8c45a">MV</text>
      <path d="M26 30 L32 12 L42 24 L50 8 L58 24 L68 12 L74 30 Z" fill="#fbf8ef" stroke="#d4a62a" stroke-width="1.5" stroke-linejoin="round"/>
      <rect x="26" y="30" width="48" height="5" fill="#fbf8ef" stroke="#d4a62a" stroke-width="1.5"/>
      <circle cx="32" cy="11" r="2.2" fill="#fbf8ef"/><circle cx="50" cy="7" r="2.4" fill="#fbf8ef"/><circle cx="68" cy="11" r="2.2" fill="#fbf8ef"/>
    </symbol>
  </defs>
</svg>

<header>
  <div class="wrap nav">
    <a href="#home" class="logo" aria-label="Maison Verde home"><svg><use href="#logo"/></svg><span>MAISON VERDE</span></a>
    <nav id="menu" aria-label="Main">
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#shop">Collection</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
    <button class="burger" id="burger" aria-label="Open menu" aria-expanded="false"><i></i><i></i><i></i></button>
  </div>
</header>

<main>
  <section class="hero" id="home">
    <div class="wrap">
      <div class="hero-frame">
        <svg class="hero-crown" viewBox="0 0 100 50" aria-hidden="true">
          <path d="M14 44 L20 14 L36 30 L50 6 L64 30 L80 14 L86 44 Z" fill="#fbf8ef" stroke="#d4a62a" stroke-width="2" stroke-linejoin="round"/>
          <rect x="14" y="44" width="72" height="5" fill="#fbf8ef" stroke="#d4a62a" stroke-width="2"/>
        </svg>
        <h1>Dressed like <em>royalty</em>,<br>made for every day</h1>
        <p>Tailored jackets, soft knits and signature essentials, cut in deep green and finished in gold.</p>
        <a href="#shop" class="btn">Shop the collection</a>
      </div>
    </div>
  </section>

  <section id="shop">
    <div class="wrap reveal">
      <div class="title"><h2>The Collection</h2><div class="line"></div></div>
      <div class="filters" id="filters">
        <button class="chip active" data-f="all">All</button>
        <button class="chip" data-f="tops">Tops</button>
        <button class="chip" data-f="outer">Outerwear</button>
        <button class="chip" data-f="bottoms">Bottoms</button>
      </div>
      <div class="grid" id="grid"></div>
    </div>
  </section>

  <section id="about">
    <div class="wrap about reveal">
      <div>
        <h2>Crafted with quiet confidence</h2>
        <p>Maison Verde began with one idea: everyday clothing should feel like a crown you can wear. We use heavyweight cotton, wool and linen, and finish each piece with gold-thread detailing.</p>
        <p>Every garment is cut in small batches, so quality always comes before quantity.</p>
      </div>
      <div class="stats">
        <div><strong>12</strong><span>Years of tailoring</span></div>
        <div><strong>48</strong><span>Signature pieces</span></div>
        <div><strong>100%</strong><span>Natural fabrics</span></div>
        <div><strong>30</strong><span>Countries shipped</span></div>
      </div>
    </div>
  </section>

  <section id="contact">
    <div class="wrap reveal">
      <div class="title"><h2>Get in touch</h2><div class="line"></div></div>
      <form id="form">
        <input type="text" placeholder="Your name" required aria-label="Your name">
        <input type="email" placeholder="Email address" required aria-label="Email address">
        <textarea rows="4" placeholder="Your message" required aria-label="Your message"></textarea>
        <button class="btn" type="submit">Send message</button>
        <div class="thanks" id="thanks"><p>Message sent. We’ll reply within one day.</p></div>
      </form>
    </div>
  </section>
</main>

<footer>
  <a href="#home" class="logo"><svg width="46" height="46"><use href="#logo"/></svg><span>MAISON VERDE</span></a>
  <p>© 2026 Maison Verde. All rights reserved.</p>
</footer>

<div class="modal" id="modal" aria-hidden="true">
  <div class="sheet" role="dialog" aria-modal="true" aria-labelledby="m-name">
    <button class="close" id="close" aria-label="Close">✕</button>
    <div class="thumb" id="m-thumb"></div>
    <div class="body">
      <h3 id="m-name"></h3>
      <div class="price" id="m-price"></div>
      <p id="m-desc"></p>
      <div class="sizes" id="sizes"><button>S</button><button class="on">M</button><button>L</button><button>XL</button></div>
      <button class="btn" id="add">Add to bag</button>
    </div>
  </div>
</div>
<div class="toast" id="toast" role="status"></div>

<script>
const icons={
  shirt:'<svg viewBox="0 0 100 100"><path d="M35 14 L12 28 L22 46 L32 40 L32 88 L68 88 L68 40 L78 46 L88 28 L65 14 Q50 26 35 14Z"/></svg>',
  jacket:'<svg viewBox="0 0 100 100"><path d="M36 12 L10 26 L14 78 L30 78 L30 40 M64 12 L90 26 L86 78 L70 78 L70 40 M36 12 L50 30 L64 12 M50 30 L50 88 M30 40 L30 88 L70 88 L70 40"/></svg>',
  pants:'<svg viewBox="0 0 100 100"><path d="M30 10 L70 10 L76 90 L54 90 L50 44 L46 90 L24 90 Z M30 10 L30 20 L70 20"/></svg>',
  hoodie:'<svg viewBox="0 0 100 100"><path d="M34 12 Q50 34 66 12 L90 30 L84 50 L72 44 L72 88 L28 88 L28 44 L16 50 L10 30 Z M42 40 L42 56 M58 40 L58 56"/></svg>'
};
const products=[
  {n:'Emerald Overshirt',p:98,c:'tops',i:'shirt',d:'Heavy cotton twill with gold-thread stitching on the collar and cuffs.'},
  {n:'Regent Blazer',p:240,c:'outer',i:'jacket',d:'A structured wool blazer in forest green with a satin-lined interior.'},
  {n:'Crown Hoodie',p:120,c:'tops',i:'hoodie',d:'Brushed fleece hoodie with a small white crown embroidered on the chest.'},
  {n:'Gilded Trousers',p:135,c:'bottoms',i:'pants',d:'Straight-leg trousers in a soft wool blend with a gold button fastening.'},
  {n:'Sovereign Coat',p:320,c:'outer',i:'jacket',d:'A long wool coat with deep pockets and a hidden gold zip lining.'},
  {n:'Velvet Tee',p:64,c:'tops',i:'shirt',d:'Midweight organic cotton tee with a relaxed royal-cut shoulder.'},
  {n:'Heritage Chinos',p:110,c:'bottoms',i:'pants',d:'Garment-washed chinos in olive green with a tapered leg.'},
  {n:'Monarch Bomber',p:210,c:'outer',i:'jacket',d:'Water-resistant bomber with ribbed gold-trim cuffs and hem.'}
];
const $=s=>document.querySelector(s);
const grid=$('#grid');

grid.innerHTML=products.map((p,k)=>`
  <button class="card" data-c="${p.c}" data-k="${k}" aria-label="View ${p.n}">
    <div class="thumb">${icons[p.i]}</div>
    <div class="info"><h3>${p.n}</h3><b>$${p.p}</b></div>
  </button>`).join('');

/* Filter with smooth fade */
$('#filters').addEventListener('click',e=>{
  const chip=e.target.closest('.chip'); if(!chip)return;
  document.querySelectorAll('.chip').forEach(c=>c.classList.remove('active'));
  chip.classList.add('active');
  const f=chip.dataset.f;
  document.querySelectorAll('.card').forEach(card=>{
    const show=f==='all'||card.dataset.c===f;
    if(show){card.classList.remove('gone');requestAnimationFrame(()=>requestAnimationFrame(()=>card.classList.remove('hide')))}
    else{card.classList.add('hide');setTimeout(()=>{if(card.classList.contains('hide'))card.classList.add('gone')},450)}
  });
});

/* Product modal */
const modal=$('#modal');let current=null,lastFocus=null;
grid.addEventListener('click',e=>{
  const card=e.target.closest('.card'); if(!card)return;
  current=products[card.dataset.k];lastFocus=card;
  $('#m-thumb').innerHTML=icons[current.i];
  $('#m-name').textContent=current.n;
  $('#m-price').textContent='$'+current.p;
  $('#m-desc').textContent=current.d;
  modal.classList.add('open');modal.setAttribute('aria-hidden','false');
  document.body.style.overflow='hidden';$('#close').focus();
});
function closeModal(){modal.classList.remove('open');modal.setAttribute('aria-hidden','true');document.body.style.overflow='';if(lastFocus)lastFocus.focus()}
$('#close').onclick=closeModal;
modal.addEventListener('click',e=>{if(e.target===modal)closeModal()});
document.addEventListener('keydown',e=>{if(e.key==='Escape')closeModal()});
$('#sizes').addEventListener('click',e=>{
  if(e.target.tagName!=='BUTTON')return;
  document.querySelectorAll('#sizes button').forEach(b=>b.classList.remove('on'));
  e.target.classList.add('on');
});

/* Toast */
let t;function toast(msg){const el=$('#toast');el.textContent=msg;el.classList.add('show');clearTimeout(t);t=setTimeout(()=>el.classList.remove('show'),2200)}
$('#add').onclick=()=>{closeModal();setTimeout(()=>toast(current.n+' added to your bag'),300)};

/* Mobile menu */
const burger=$('#burger'),menu=$('#menu');
burger.onclick=()=>{const o=menu.classList.toggle('open');burger.classList.toggle('open',o);burger.setAttribute('aria-expanded',o)};
menu.addEventListener('click',e=>{if(e.target.tagName==='A'){menu.classList.remove('open');burger.classList.remove('open');burger.setAttribute('aria-expanded','false')}});

/* Contact form */
$('#form').addEventListener('submit',e=>{e.preventDefault();$('#thanks').classList.add('show');e.target.reset()});

/* Scroll reveal */
const io=new IntersectionObserver(es=>es.forEach(en=>{if(en.isIntersecting){en.target.classList.add('in');io.unobserve(en.target)}}),{threshold:.12});
document.querySelectorAll('.reveal').forEach(el=>io.observe(el));
</script>
</body>
</html>
