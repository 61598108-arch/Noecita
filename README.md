<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Un jardín para Noemí 🌷</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;700&family=Playfair+Display:ital,wght@0,500;0,600;1,500&display=swap" rel="stylesheet">
<style>
:root{color-scheme:light;--rosa:#e8789c;--osc:#4a2a3d;--crema:#fff8f4;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
*{box-sizing:border-box}
html{scroll-behavior:smooth;background:var(--crema)}
body{margin:0;font-family:"DM Sans",system-ui,sans-serif;color:var(--osc);background:var(--crema);overflow-x:hidden}
h1,h2,h3{font-family:"Playfair Display",Georgia,serif;font-weight:500;margin:0}
button{font:inherit;cursor:pointer;border:0}
.btn{background:linear-gradient(135deg,#f08fb0,#e0558a);color:#fff;border-radius:50px;padding:15px 30px;font-weight:700;box-shadow:0 10px 26px #e0558a55;transition:.3s}
.btn:hover{transform:translateY(-3px) scale(1.03);box-shadow:0 16px 34px #e0558a66}
.tag{letter-spacing:4px;font-size:12px;text-transform:uppercase;font-weight:700;color:#b5557a}
/* escena */
.escena{position:relative;overflow:hidden;background:linear-gradient(180deg,#ffd9c7 0%,#ffc2d1 38%,#f9a8c4 62%,#e98fb3 100%)}
.hero{min-height:100svh;display:flex;align-items:flex-start;justify-content:center;text-align:center;padding:12vh 22px 0}
.sol{position:absolute;left:50%;top:34%;width:520px;height:520px;margin-left:-260px;border-radius:50%;background:radial-gradient(circle,#fff6d6 0%,#ffe3a8aa 30%,#ffd0a000 70%);animation:late 6s ease-in-out infinite}
@keyframes late{50%{transform:scale(1.08);opacity:.85}}
.colina{position:absolute;left:-5%;width:110%;bottom:0;border-radius:50% 50% 0 0/100% 100% 0 0}
.c1{height:34%;background:linear-gradient(#9fc47a,#6a9a52)}
.c2{height:24%;left:-20%;width:90%;background:linear-gradient(#7fae60,#4f8446);opacity:.95}
.c3{height:20%;left:40%;width:90%;background:linear-gradient(#8bb86a,#5b9050)}
.hero .in{position:relative;z-index:30;max-width:720px;color:#4a1f37;animation:ent 1.6s ease both}
@keyframes ent{from{opacity:0;transform:translateY(30px)}to{opacity:1;transform:none}}
.hero h1{font-size:clamp(54px,11vw,108px);line-height:1.05;margin:14px 0;text-shadow:0 2px 24px #fff8}
.hero h1 em{color:#c93a73}
.hero p{font-size:clamp(16px,2.4vw,20px);line-height:1.8;max-width:560px;margin:0 auto 26px;color:#5a2d45}
/* tulipanes */
.campo{position:absolute;inset:auto 0 0 0;height:62%;z-index:20;pointer-events:none}
.tulip{position:absolute;transform-origin:50% 100%;animation:crecer 1.6s cubic-bezier(.2,.9,.3,1.1) both,mecer 5s ease-in-out infinite;filter:drop-shadow(0 6px 5px #2e4a2a40)}
.tulip svg{height:100%;width:auto;display:block;overflow:visible}
@keyframes crecer{from{transform:scaleY(0) scaleX(.5);opacity:0}to{transform:scaleY(1) scaleX(1);opacity:1}}
@keyframes mecer{0%,100%{rotate:-2.5deg}50%{rotate:2.5deg}}
.petalo{position:fixed;top:-30px;z-index:15;pointer-events:none;width:11px;height:15px;border-radius:70% 0 70% 70%;background:linear-gradient(135deg,#ffc6d8,#f07aa2);opacity:.85;animation:caer linear forwards}
@keyframes caer{to{transform:translate(80px,112vh) rotate(540deg);opacity:0}}
/* secciones */
section.s{padding:90px 20px;text-align:center}
section.s h2{font-size:clamp(34px,5vw,54px);margin:14px 0}
.sub{max-width:640px;margin:0 auto 30px;line-height:1.9;color:#85606f}
.mini{height:min(62vh,440px);margin:34px auto 28px;max-width:960px;border-radius:28px;box-shadow:0 24px 60px #b04d7a40}
.mini .campo{height:80%}
.cnt{margin-top:18px;font-weight:700;color:#b5457a;min-height:26px}
.tarjetas{max-width:1080px;margin:0 auto;display:grid;grid-template-columns:repeat(3,1fr);gap:22px}
.tarjeta{background:#fff;border:1px solid #f5dde6;border-radius:26px;padding:34px 22px;box-shadow:0 14px 36px #b0647426;transition:.35s}
.tarjeta:hover{transform:translateY(-8px);box-shadow:0 22px 46px #b0647438}
.emoji{font-size:58px;filter:drop-shadow(0 8px 6px #0002)}
.tarjeta h3{font-size:25px;margin:8px 0}
.tarjeta p{line-height:1.7;margin:0 0 18px}
.regalo{min-height:48px;margin-top:18px;color:#a54e75;font-weight:600;line-height:1.6}
.pop{animation:ent .6s ease both}
.rosado{background:linear-gradient(150deg,#ffe8ef,#fff7f0)}
.carta{max-width:700px;margin:30px auto 0;padding:44px 40px;text-align:left;font-size:18px;line-height:2;font-family:"Playfair Display",Georgia,serif;color:#5a3a49;background:repeating-linear-gradient(#fffdf8 0 35px,#f1e3dc 35px 36px);border-radius:6px;box-shadow:0 2px 0 #fff inset,0 24px 50px #a25b7833,0 0 0 1px #ecd5cc;position:relative;transform:rotate(-.6deg)}
.carta::before{content:"🌷";position:absolute;top:-22px;right:26px;font-size:40px}
.carta p{margin:0 0 14px}
.oculto{display:none}
.frase{font:italic 500 clamp(22px,4vw,33px)/1.7 "Playfair Display",serif;color:#a34f72;max-width:740px;margin:26px auto}
footer{text-align:center;padding:40px 20px;color:#906c7b}
@media(max-width:720px){.tarjetas{grid-template-columns:1fr}section.s{padding:64px 18px}.carta{padding:34px 24px;font-size:16px}.sol{width:380px;height:380px;margin-left:-190px}}
@media(prefers-reduced-motion:reduce){*,*::before,*::after{animation-duration:.01ms!important;animation-iteration-count:1!important;scroll-behavior:auto!important}}
</style>
</head>
<body>
<svg width="0" height="0" style="position:absolute" aria-hidden="true"><defs id="defs">
<linearGradient id="lf" x1="0" y1="0" x2="1" y2="1"><stop offset="0" stop-color="#8fca64"/><stop offset="1" stop-color="#3f7a38"/></linearGradient>
<linearGradient id="st" x1="0" x2="1"><stop offset="0" stop-color="#4c8a3a"/><stop offset="1" stop-color="#78b255"/></linearGradient>
</defs></svg>

<header class="escena hero" id="inicio">
  <div class="sol"></div>
  <div class="colina c3"></div><div class="colina c2"></div><div class="colina c1"></div>
  <div class="in">
    <div class="tag">Un pequeño detalle para ti 🌷</div>
    <h1>Bienvenida,<br><em>Noemí</em> ♡</h1>
    <p>Holaaa, Noemí. 🥹 Tal vez hoy no estés pasando por tu mejor momento, así que preparé algo pequeñito para ti. No sé si conseguiré sacarte una sonrisa, pero espero que este jardín te regale un momento bonito.</p>
    <button class="btn" onclick="ir('jardin')">Entrar a tu jardín 🌷</button>
  </div>
  <div class="campo" id="campoHero"></div>
</header>

<main>
<section class="s rosado" id="jardin">
  <div class="tag">Un rincón lleno de flores</div>
  <h2>Un jardín de tulipanes para ti 🌷</h2>
  <p class="sub">Dicen que las flores hacen los días un poquito más bonitos. Por eso quise llenar este lugar de tulipanes, especialmente para ti.</p>
  <div class="escena mini"><div class="sol" style="top:10%;width:380px;height:380px;margin-left:-190px"></div><div class="colina c2"></div><div class="colina c1"></div><div class="campo" id="campoMini"></div></div>
  <p class="sub">No son flores que puedas sostener entre tus manos, pero sí un detalle que puedes visitar cuando quieras. 💗</p>
  <button class="btn" onclick="florecer()">🌷 Hacer florecer el jardín</button>
  <p class="cnt" id="cnt">Presiona y mira cómo crecen ✨</p>
</section>

<section class="s" id="sorpresas">
  <div class="tag">Algo para alegrarte</div>
  <h2>Te preparé tres sorpresitas 🎁</h2>
  <p class="sub">Abre cada regalo. Son pequeños detalles que espero te hagan sonreír.</p>
  <div class="tarjetas">
    <article class="tarjeta"><div class="emoji">🧸</div><h3>Un osito para ti</h3><p>Este osito tiene un mensaje especial.</p><button class="btn" onclick="regalo(0)">Abrir regalo 🎀</button><div class="regalo" id="r0" aria-live="polite"></div></article>
    <article class="tarjeta"><div class="emoji">🐣</div><h3>Una pequeña bromita</h3><p>Una broma tan mala que quizás te dé risa.</p><button class="btn" onclick="regalo(1)">Abrir regalo 🎀</button><div class="regalo" id="r1" aria-live="polite"></div></article>
    <article class="tarjeta"><div class="emoji">💌</div><h3>Un recordatorio bonito</h3><p>Algo que me gustaría que recordaras.</p><button class="btn" onclick="regalo(2)">Abrir regalo 🎀</button><div class="regalo" id="r2" aria-live="polite"></div></article>
  </div>
</section>

<section class="s rosado" id="carta">
  <div class="tag">Unas palabras con cariño</div>
  <h2>Hay algo que quiero decirte 💌</h2>
  <p class="sub">No es nada que tengas que responder. Ábrelo solamente si te apetece.</p>
  <button class="btn" id="bc" onclick="abrirCarta()">✉️ Abrir mi carta</button>
  <div class="carta oculto" id="cc">
    <p>Hola, Noemí. 🌷</p>
    <p>No sé exactamente qué estás pasando ni cómo te estás sintiendo en este momento, pero espero de corazón que las cosas mejoren para ti.</p>
    <p>Sé que hay días en los que simplemente no tenemos ganas de sonreír, y está bien. No tienes que estar feliz todo el tiempo.</p>
    <p>Quise preparar este pequeño jardín porque, a pesar de todo, me gustaría que tuvieras un momento bonito. Que pudieras distraerte, mirar las flores y quizás reírte un poquito con alguna de mis tonterías.</p>
    <p>No espero nada a cambio. Solo deseo que estés bien, que encuentres tranquilidad y que la vida te regale muchos motivos para sonreír.</p>
    <p>Cuídate mucho, Noemí. Y nunca olvides que mereces cosas bonitas. 💗</p>
    <p style="text-align:right">Con cariño. 🌷</p>
  </div>
</section>

<section class="s" id="final">
  <div style="font-size:70px">🌷</div>
  <h2>Una última cosita, Noemí…</h2>
  <p class="frase">“Ojalá que, entre tantas cosas que pasan en la vida, nunca te falten motivos para volver a sonreír.”</p>
  <p class="sub">Gracias por visitar este pequeño jardín. No tienes que responder ni decir nada. Solo quería regalarte algo bonito.</p>
  <button class="btn" onclick="celebrar()">Una última sorpresa ✨</button>
</section>
</main>
<footer>Hecho con cariño, tulipanes y buenos deseos. 🌷</footer>

<script>
const cols=[["#ffb3c8","#ee5b8a","#a8174f"],["#ffe0e8","#f59bb5","#c4557a"],["#ffc27a","#f0713c","#b53a1a"],["#fff4b0","#ffd13a","#d99a00"],["#efc4ff","#b873ee","#6f27b8"]];
const defs=document.getElementById("defs");
cols.forEach((c,i)=>{defs.insertAdjacentHTML("beforeend",`<linearGradient id="p${i}" x1="0" y1="0" x2="0" y2="1"><stop offset="0" stop-color="${c[0]}"/><stop offset=".55" stop-color="${c[1]}"/><stop offset="1" stop-color="${c[2]}"/></linearGradient>`)});
function svgTulip(i){
 return `<svg viewBox="0 0 60 170" aria-hidden="true">
 <path d="M30 170C27 135 33 100 30 64" stroke="url(#st)" stroke-width="3.6" fill="none" stroke-linecap="round"/>
 <path d="M30 160C6 148 2 112 12 88C24 104 31 132 30 160Z" fill="url(#lf)"/>
 <path d="M30 150C54 142 58 108 49 90C37 104 29 126 30 150Z" fill="url(#lf)" opacity=".92"/>
 <path d="M13 24C8 46 14 64 30 68C22 50 22 34 13 24Z" fill="url(#p${i})" opacity=".8"/>
 <path d="M47 24C52 46 46 64 30 68C38 50 38 34 47 24Z" fill="url(#p${i})" opacity=".8"/>
 <path d="M30 6C45 20 49 46 30 70C11 46 15 20 30 6Z" fill="url(#p${i})"/>
 <path d="M30 6C24 22 22 44 30 70C38 44 36 22 30 6Z" fill="#fff" opacity=".16"/>
 <ellipse cx="24" cy="30" rx="3" ry="11" fill="#fff" opacity=".35" transform="rotate(12 24 30)"/>
 </svg>`;
}
function plantar(id,n){
 const box=document.getElementById(id);
 for(let k=0;k<n;k++){
  const d=document.createElement("div");
  const alto=34+Math.random()*52, bot=Math.random()*38;
  d.className="tulip";
  d.style.cssText=`left:${2+Math.random()*92}%;bottom:${bot}%;height:${alto*(1-bot/160)}%;z-index:${Math.round(100-bot)};animation-delay:${(k*.07).toFixed(2)}s,${(Math.random()*-5).toFixed(2)}s;animation-duration:1.6s,${(4+Math.random()*3).toFixed(1)}s`;
  d.innerHTML=svgTulip(Math.floor(Math.random()*cols.length));
  box.appendChild(d);
 }
}
plantar("campoHero",34);plantar("campoMini",16);
function ir(id){document.getElementById(id).scrollIntoView({behavior:"smooth"})}
let flores=16;
function florecer(){
 plantar("campoMini",8);flores+=8;
 document.getElementById("cnt").textContent="¡Ya florecieron "+flores+" tulipanes para ti! 🌷";
 lluvia(26);
}
const msj=[
 ["🧸 El osito dice: Te mando un abrazo suavecito, de esos que acompañan sin apretar. 💗","🧸 El osito también quiere regalarte un tulipán. 🌷"],
 ["🌷 ¿Qué le dijo una flor a otra? ¡Deja de plantarme! 😂","🐝 ¿Qué hace una abeja en el gimnasio? ¡Zum-ba! 😂"],
 ["💗 No tienes que estar feliz todos los días. También mereces descansar.","🌤️ Un día difícil no significa que mañana será igual. Te deseo días más tranquilos."]
];
const veces=[0,0,0];
function regalo(n){
 const e=document.getElementById("r"+n);
 e.textContent=msj[n][veces[n]%2];veces[n]++;
 e.classList.remove("pop");void e.offsetWidth;e.classList.add("pop");
 lluvia(14);
}
function abrirCarta(){
 const c=document.getElementById("cc"),b=document.getElementById("bc");
 c.classList.toggle("oculto");c.classList.add("pop");
 if(c.classList.contains("oculto")){b.textContent="✉️ Abrir mi carta"}
 else{b.textContent="💌 Cerrar la carta";lluvia(16)}
}
function celebrar(){lluvia(70);plantar("campoMini",6)}
const quieto=matchMedia("(prefers-reduced-motion: reduce)").matches;
function petalo(){
 if(quieto)return;
 const p=document.createElement("span");p.className="petalo";
 p.style.left=Math.random()*100+"vw";
 p.style.transform=`scale(${.6+Math.random()*.9})`;
 p.style.animationDuration=(7+Math.random()*6)+"s";
 document.body.appendChild(p);setTimeout(()=>p.remove(),14000);
}
function lluvia(n){for(let i=0;i<n;i++)setTimeout(petalo,i*60)}
setInterval(()=>{if(!document.hidden)petalo()},900);
</script>
</body>
</html>
