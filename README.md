<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Happy 2 Months</title>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,500;1,9..144,400&family=DM+Sans:wght@400;500&display=swap">
<style>
:root{
  --night:#1d1030; --plum:#341a4f; --rose:#ff6f91; --peach:#ffc99a; --lilac:#c9b6ff; --cream:#fff4ec;
  --display:'Fraunces',Georgia,serif; --body:'DM Sans',system-ui,sans-serif;
}
*{box-sizing:border-box;margin:0}
html,body{height:100%;overflow:hidden}
body{font-family:var(--body);color:var(--cream);background:radial-gradient(120% 90% at 20% 10%,var(--plum),var(--night));-webkit-tap-highlight-color:transparent}
body::after{content:"";position:fixed;inset:0;pointer-events:none;background:radial-gradient(60% 50% at 50% 55%,rgba(255,111,145,.16),transparent 70%);animation:glow 4s ease-in-out infinite}
@keyframes glow{50%{opacity:.4}}
#hearts,#confetti,#fx{position:fixed;inset:0;pointer-events:none}
#hearts span{position:absolute;bottom:-40px;opacity:0;animation:float linear infinite;color:var(--rose)}
@keyframes float{0%{transform:translateY(0) rotate(0);opacity:0}10%{opacity:.4}100%{transform:translateY(-110vh) rotate(40deg);opacity:0}}
#fx span{position:absolute;animation:pluck 1.1s ease-out forwards;transform:translate(-50%,-50%)}
@keyframes pluck{to{transform:translate(-50%,-190%) scale(1.5);opacity:0}}
#fx .tr{animation:fade .7s forwards;color:var(--peach);font-size:14px}
@keyframes fade{to{opacity:0;transform:translate(-50%,-50%) scale(.2)}}

.slide{position:absolute;inset:0;display:flex;flex-direction:column;align-items:center;justify-content:center;
  text-align:center;padding:24px 24px 96px;opacity:0;visibility:hidden;transform:scale(.96);
  transition:opacity .7s ease,transform .7s ease,visibility .7s}
.slide.active{opacity:1;visibility:visible;transform:none}
.a{opacity:0}
.active .a{animation:rise .9s cubic-bezier(.2,.7,.2,1) var(--d,0s) both}
@keyframes rise{from{opacity:0;transform:translateY(26px)}to{opacity:1;transform:none}}
@keyframes pop{0%{opacity:0;transform:scale(.4)}70%{transform:scale(1.08)}100%{opacity:1;transform:scale(1)}}
@keyframes beat{0%,100%{transform:scale(1)}14%{transform:scale(1.09)}28%{transform:scale(1)}42%{transform:scale(1.06)}}

h1,h2{font-family:var(--display);font-weight:500;line-height:1.1}
h1{font-size:clamp(2.2rem,7vw,4.6rem)}
h2{font-size:clamp(1.8rem,5vw,3rem);margin-bottom:28px}
p{font-size:clamp(1rem,2.4vw,1.25rem);max-width:34ch;line-height:1.6;color:#f1dfe6}
em{font-family:var(--display);font-style:italic;color:var(--peach)}

/* hero */
.big{position:relative;font-family:var(--display);font-size:clamp(9rem,34vw,20rem);line-height:.85;color:var(--rose);text-shadow:0 0 60px rgba(255,111,145,.5)}
.big i{position:absolute;font-style:normal;font-size:clamp(1.4rem,5vw,2.6rem);color:var(--peach);animation:twinkle 2s ease-in-out infinite}
.big i:nth-child(1){top:6%;left:-14%}.big i:nth-child(2){top:30%;right:-18%;animation-delay:.7s}.big i:nth-child(3){bottom:10%;left:-10%;animation-delay:1.3s}
@keyframes twinkle{50%{opacity:.2;transform:scale(.6) rotate(20deg)}}
.active .big{animation:pop 1.1s cubic-bezier(.2,.8,.2,1) .2s both,beat 2.2s ease-in-out 1.4s infinite}
.hero h1{margin-top:8px}.hero p{margin-top:14px}

/* counter */
.count{display:flex;gap:clamp(14px,5vw,48px);margin:8px 0 26px}
.count div{display:flex;flex-direction:column;align-items:center}
.count b{font-family:var(--display);font-weight:500;font-size:clamp(2.8rem,11vw,6rem);color:var(--peach);line-height:1;font-variant-numeric:tabular-nums}
.count small{font-size:.95rem;color:var(--lilac);margin-top:6px}

/* timeline */
.line{position:relative;display:flex;flex-direction:column;gap:26px;text-align:left;max-width:440px;padding-left:34px}
.line::before{content:"";position:absolute;left:7px;top:6px;bottom:6px;width:2px;background:linear-gradient(var(--rose),var(--lilac));transform-origin:top;transform:scaleY(0)}
.active .line::before{animation:grow 1.6s ease .3s forwards}
@keyframes grow{to{transform:scaleY(1)}}
.line div{position:relative}
.line div::before{content:"\2665";position:absolute;left:-36px;top:0;font-size:1.1rem;color:var(--rose);text-shadow:0 0 12px var(--rose)}
.line h3{font-family:var(--display);font-weight:500;font-size:1.35rem;margin-bottom:2px}
.line p{font-size:1rem;max-width:none}

/* polaroids */
.pols{display:flex;gap:clamp(10px,3vw,28px);justify-content:center;flex-wrap:wrap}
.pol{width:clamp(120px,26vw,190px);background:var(--cream);color:#3a2347;padding:10px 10px 14px;border-radius:4px;box-shadow:0 14px 30px rgba(0,0,0,.4);transform:rotate(var(--r))}
.pol .ph{aspect-ratio:1;border-radius:2px;background:linear-gradient(135deg,var(--rose),var(--lilac));display:grid;place-items:center;font-size:2.4rem;overflow:hidden}
.pol .ph img{width:100%;height:100%;object-fit:cover}
.pol span{display:block;margin-top:10px;font-family:var(--display);font-style:italic;font-size:.95rem}
.active .pol{animation:drop .9s cubic-bezier(.3,1.4,.5,1) var(--d) both}
@keyframes drop{from{opacity:0;transform:translateY(-120px) rotate(calc(var(--r) * 4))}to{opacity:1;transform:rotate(var(--r))}}

/* letter */
.letter{max-width:460px;padding:30px 28px;border-radius:6px;background:rgba(255,244,236,.07);border:1px solid rgba(255,201,154,.35);text-align:left}
.letter p{max-width:none;min-height:9em;font-family:var(--display);font-style:italic;font-size:clamp(1.05rem,2.6vw,1.3rem);color:var(--cream)}
.letter p::after{content:"|";color:var(--rose);animation:blink .8s steps(1) infinite}
@keyframes blink{50%{opacity:0}}
.sig{margin-top:14px;text-align:right;color:var(--peach);font-family:var(--display)}

/* reasons */
.reasons{display:flex;flex-wrap:wrap;gap:14px;justify-content:center;max-width:640px}
.reasons span{padding:12px 20px;border-radius:999px;border:1.5px solid var(--lilac);font-size:clamp(.95rem,2.4vw,1.15rem);background:rgba(201,182,255,.08);transition:background .2s,transform .2s}
.reasons span:hover{background:rgba(255,111,145,.3);transform:scale(1.07)}
.active .reasons span{animation:pop .7s cubic-bezier(.2,.8,.2,1) var(--d) both}

/* finale */
.finale h1{font-size:clamp(2.2rem,8vw,5rem)}
.finale h1 em{display:block}
button{font:inherit;cursor:pointer;color:inherit}
.btns{display:flex;gap:22px;align-items:center;justify-content:center;margin-top:34px;min-height:64px}
.yes,.replay{padding:12px 30px;border-radius:999px;border:1.5px solid var(--peach);background:transparent;color:var(--peach);transition:background .2s,color .2s}
.yes{background:var(--rose);border-color:var(--rose);color:#fff;font-weight:500;box-shadow:0 0 28px rgba(255,111,145,.55);transition:transform .3s}
.no{padding:10px 22px;border-radius:999px;border:1.5px solid rgba(255,244,236,.4);background:transparent;font-size:.95rem;transition:left .25s,top .25s;z-index:4}
.replay:hover{background:var(--peach);color:var(--night)}
.after{display:none;margin-top:22px}
.said .btns{display:none}.said .after{display:block;animation:pop .8s both}
.said h1{animation:beat 1.4s ease-in-out infinite}

/* nav */
nav{position:fixed;left:0;right:0;bottom:0;display:flex;align-items:center;justify-content:center;gap:18px;padding:18px;z-index:5}
nav button{width:44px;height:44px;border-radius:50%;border:1.5px solid rgba(255,244,236,.4);background:rgba(29,16,48,.5);font-size:1.1rem;backdrop-filter:blur(6px)}
nav button:hover{border-color:var(--rose)}
button:focus-visible{outline:2px solid var(--peach);outline-offset:3px}
#dots{display:flex;gap:10px}
#dots i{width:9px;height:9px;border-radius:50%;background:rgba(255,244,236,.3);cursor:pointer;transition:all .3s}
#dots i.on{background:var(--rose);width:26px;border-radius:6px}
#bar{position:fixed;top:0;left:0;height:3px;background:linear-gradient(90deg,var(--rose),var(--peach));width:0;z-index:6;transition:width .6s}

@media (prefers-reduced-motion:reduce){
  *{animation-duration:.01s!important;animation-delay:0s!important;transition-duration:.01s!important}
  #hearts{display:none}
}
</style>
</head>
<body>
<div id="bar"></div>
<div id="hearts" aria-hidden="true"></div>

<!-- 1 Hero -->
<section class="slide hero">
  <div class="big">2<i>&#10022;</i><i>&#9825;</i><i>&#10022;</i></div>
  <h1 class="a" style="--d:.9s">Months of us</h1>
  <p class="a" style="--d:1.3s">Happy anniversary, <em class="to">my love</em>. &#128150;</p>
</section>

<!-- 2 Counter -->
<section class="slide" data-count>
  <h2 class="a">Time with you so far</h2>
  <div class="count a" style="--d:.3s">
    <div><b id="cDays">0</b><small>days</small></div>
    <div><b id="cHours">0</b><small>hours</small></div>
    <div><b>&#8734;</b><small>smiles</small></div>
  </div>
  <p class="a" style="--d:.8s">And every one of them was better because you were in it.</p>
</section>

<!-- 3 Timeline -->
<section class="slide">
  <h2 class="a">How it began</h2>
  <div class="line">
    <div class="a" style="--d:.5s"><h3>The first hello</h3><p>The moment we first chatted.</p></div>
    <div class="a" style="--d:1.1s"><h3>The day we told each other how we felt</h3><p>All the nervous laughs we had.</p></div>
    <div class="a" style="--d:1.7s"><h3>Everything since</h3><p>Two months of small moments that became our favorites.</p></div>
  </div>
</section>

<!-- 4 Polaroids (filled from CONFIG.photos) -->
<section class="slide">
  <h2 class="a">Our little moments</h2>
  <div class="pols" id="pols"></div>
</section>

<!-- 5 Letter -->
<section class="slide" data-letter>
  <h2 class="a">A little note for you</h2>
  <div class="letter a" style="--d:.3s">
    <p id="note"></p>
    <div class="sig" id="sig"></div>
  </div>
</section>

<!-- 6 Reasons -->
<section class="slide">
  <h2 class="a">What I love about you</h2>
  <div class="reasons">
    <span style="--d:.3s">&#128525; Your laugh</span>
    <span style="--d:.5s">&#128066; How you listened</span>
    <span style="--d:.7s">&#127800; Your kindness</span>
    <span style="--d:.9s">&#128514; Your jokes</span>
    <span style="--d:1.1s">&#127968; The way you make home feel anywhere</span>
    <span style="--d:1.3s">&#128150; Just you</span>
  </div>
</section>

<!-- 7 Finale -->
<section class="slide finale" id="ask" data-ask>
  <h1 class="a" id="q">Will you keep being mine,<em class="to">my love?</em></h1>
  <div class="a" style="--d:.8s">
    <div class="btns">
      <button class="yes" id="yes">Yes, always &#128149;</button>
      <button class="no" id="no">No</button>
    </div>
    <div class="after">
      <p>I knew you’d say yes. Two months down, <em>so many more to go.</em></p>
      <button class="replay" onclick="go(0)" style="margin-top:20px">Watch again</button>
    </div>
  </div>
</section>

<nav>
  <button id="prev" aria-label="Previous slide">&#8592;</button>
  <div id="dots"></div>
  <button id="auto" aria-label="Toggle autoplay" title="Autoplay">&#9654;</button>
  <button id="next" aria-label="Next slide">&#8594;</button>
</nav>
<div id="fx" aria-hidden="true"></div>
<canvas id="confetti" aria-hidden="true"></canvas>

<script>
/* ===== EDIT THESE ===== */
const CONFIG = {
  to: "my love",                 // their name or nickname
  from: "Yours",                 // your name, shown under the note
  start: "2026-09-21",           // the day we got together (YYYY-MM-DD)
  letter: "From the first hello, you made ordinary days feel like little adventures. I love your laugh, your kindness, and how safe I feel with you. Here’s to more late-night talks, more trips, and so many more months with you.",
  photos: [                      // add src: "photo1.jpg" to show a real picture
    {src: "", caption: "Our first chat", emoji: "\u{1F4AC}"},
    {src: "", caption: "Nervous laughs", emoji: "\u{1F60A}"},
    {src: "", caption: "Us, always", emoji: "\u{1F495}"}
  ]
};
/* ====================== */

document.querySelectorAll('.to').forEach(e => e.textContent = CONFIG.to);
document.getElementById('sig').textContent = '\u2014 ' + CONFIG.from + ' \u2665';
document.getElementById('pols').innerHTML = CONFIG.photos.map((p, i) =>
  `<div class="pol" style="--r:${[-5,3,-2][i % 3]}deg;--d:${.4 + i * .5}s"><div class="ph">${p.src ? `<img src="${p.src}" alt="">` : p.emoji}</div><span></span></div>`).join('');
document.querySelectorAll('#pols .pol span').forEach((s, i) => s.textContent = CONFIG.photos[i].caption);

const slides = [...document.querySelectorAll('.slide')];
const dots = document.getElementById('dots');
const bar = document.getElementById('bar');
let cur = -1, timer = null, typer = null;

slides.forEach((_, i) => {
  const d = document.createElement('i');
  d.onclick = () => { stopAuto(); go(i); };
  dots.appendChild(d);
});

function go(i){
  if (i < 0 || i >= slides.length || i === cur) return;
  clearInterval(typer);
  document.getElementById('ask').classList.remove('said'); resetNo();
  slides.forEach(s => s.classList.remove('active'));
  void document.body.offsetWidth;
  slides[i].classList.add('active');
  [...dots.children].forEach((d, k) => d.classList.toggle('on', k === i));
  bar.style.width = ((i + 1) / slides.length * 100) + '%';
  cur = i;
  const s = slides[i];
  if (s.hasAttribute('data-count')) countUp();
  if (s.hasAttribute('data-letter')) typeLetter();
}
const next = () => go(Math.min(cur + 1, slides.length - 1));
const prev = () => go(Math.max(cur - 1, 0));
document.getElementById('next').onclick = () => { stopAuto(); next(); };
document.getElementById('prev').onclick = () => { stopAuto(); prev(); };
document.addEventListener('keydown', e => {
  if (e.key === 'ArrowRight') { stopAuto(); next(); }
  if (e.key === 'ArrowLeft') { stopAuto(); prev(); }
});
let x0 = null;
document.addEventListener('touchstart', e => x0 = e.touches[0].clientX, {passive:true});
document.addEventListener('touchend', e => {
  if (x0 === null) return;
  const dx = e.changedTouches[0].clientX - x0;
  if (Math.abs(dx) > 60) { stopAuto(); dx < 0 ? next() : prev(); }
  x0 = null;
});

/* autoplay (slower on the letter slide so it can be read) */
const autoBtn = document.getElementById('auto');
function startAuto(){
  autoBtn.innerHTML = '&#10074;&#10074;';
  (function step(){
    timer = setTimeout(() => {
      if (cur < slides.length - 2) { next(); step(); } else { next(); stopAuto(); }
    }, slides[cur].hasAttribute('data-letter') ? 16000 : 6500);
  })();
}
function stopAuto(){ clearTimeout(timer); timer = null; autoBtn.innerHTML = '&#9654;'; }
autoBtn.onclick = () => timer ? stopAuto() : startAuto();

/* counter */
function countUp(){
  const ms = Date.now() - new Date(CONFIG.start + 'T00:00:00').getTime();
  animate('cDays', Math.max(0, Math.floor(ms / 864e5)));
  animate('cHours', Math.max(0, Math.floor(ms / 36e5)));
}
function animate(id, target){
  const el = document.getElementById(id), t0 = performance.now();
  (function tick(t){
    const p = Math.min((t - t0) / 1800, 1);
    el.textContent = Math.round(target * (1 - Math.pow(1 - p, 3))).toLocaleString();
    if (p < 1) requestAnimationFrame(tick);
  })(t0);
}

/* typewriter love note */
function typeLetter(){
  const el = document.getElementById('note'); el.textContent = '';
  let n = 0;
  setTimeout(() => {
    typer = setInterval(() => {
      el.textContent = CONFIG.letter.slice(0, ++n);
      if (n >= CONFIG.letter.length) clearInterval(typer);
    }, 38);
  }, 900);
}

/* the question: "No" runs away, "Yes" grows */
const yes = document.getElementById('yes'), no = document.getElementById('no');
let scale = 1;
function dodge(e){
  e.preventDefault();
  no.style.position = 'fixed';
  no.style.left = (20 + Math.random() * (innerWidth - 120)) + 'px';
  no.style.top = (70 + Math.random() * (innerHeight - 190)) + 'px';
  scale = Math.min(scale + .15, 2); yes.style.transform = `scale(${scale})`;
}
function resetNo(){ no.removeAttribute('style'); yes.style.transform = ''; scale = 1; }
no.addEventListener('pointerenter', dodge);
no.addEventListener('click', dodge);
yes.onclick = () => {
  document.getElementById('ask').classList.add('said');
  document.getElementById('q').innerHTML = 'Forever starts now,<em>' + CONFIG.to + ' &#128149;</em>';
  burst(innerWidth / 2, innerHeight * .4, 200);
  setTimeout(() => burst(innerWidth * .2, innerHeight * .5, 90), 300);
  setTimeout(() => burst(innerWidth * .8, innerHeight * .5, 90), 600);
  for (let i = 0; i < 24; i++) setTimeout(() => pluck(Math.random() * innerWidth, innerHeight * (.5 + Math.random() * .4)), i * 90);
};

/* floating hearts in the background */
const hearts = document.getElementById('hearts');
for (let i = 0; i < 20; i++){
  const h = document.createElement('span');
  h.textContent = i % 4 ? '\u2665' : '\u2661';
  h.style.left = Math.random() * 100 + '%';
  h.style.fontSize = (12 + Math.random() * 26) + 'px';
  h.style.animationDuration = (12 + Math.random() * 14) + 's';
  h.style.animationDelay = (-Math.random() * 20) + 's';
  hearts.appendChild(h);
}

/* tap anywhere = hearts, mouse = sparkle trail */
const fx = document.getElementById('fx');
function pluck(x, y){
  const s = document.createElement('span');
  s.textContent = ['\u{1F495}','\u2764\uFE0F','\u{1F497}','\u{1F496}'][Math.random() * 4 | 0];
  s.style.left = x + 'px'; s.style.top = y + 'px'; s.style.fontSize = (18 + Math.random() * 18) + 'px';
  fx.appendChild(s); setTimeout(() => s.remove(), 1200);
}
document.addEventListener('pointerdown', e => { if (!e.target.closest('nav,button')) for (let i = 0; i < 3; i++) setTimeout(() => pluck(e.clientX + (Math.random() - .5) * 40, e.clientY), i * 80); });
let last = 0;
document.addEventListener('pointermove', e => {
  if (e.pointerType !== 'mouse' || Date.now() - last < 55) return; last = Date.now();
  const s = document.createElement('span'); s.className = 'tr'; s.textContent = '\u2726';
  s.style.left = e.clientX + 'px'; s.style.top = e.clientY + 'px';
  fx.appendChild(s); setTimeout(() => s.remove(), 700);
});

/* confetti (rectangles + hearts) */
const cv = document.getElementById('confetti'), ctx = cv.getContext('2d');
let parts = [], raf = null;
function size(){ cv.width = innerWidth; cv.height = innerHeight; }
addEventListener('resize', size); size();
function burst(x, y, n){
  const colors = ['#ff6f91','#ffc99a','#c9b6ff','#fff4ec'];
  for (let i = 0; i < n; i++){
    parts.push({x, y, vx: (Math.random() - .5) * 18, vy: -Math.random() * 16 - 3, r: 4 + Math.random() * 6,
      c: colors[i % 4], rot: Math.random() * 6, vr: (Math.random() - .5) * .3, life: 1, h: i % 3 === 0});
  }
  if (!raf) loop();
}
function loop(){
  ctx.clearRect(0, 0, cv.width, cv.height);
  parts.forEach(p => {
    p.vy += .28; p.x += p.vx; p.y += p.vy; p.rot += p.vr; p.life -= .006;
    ctx.save(); ctx.globalAlpha = Math.max(p.life, 0); ctx.translate(p.x, p.y); ctx.rotate(p.rot); ctx.fillStyle = p.c;
    if (p.h){ ctx.font = (p.r * 3) + 'px serif'; ctx.fillText('\u2665', -p.r, p.r); } else ctx.fillRect(-p.r, -p.r / 2, p.r * 2, p.r);
    ctx.restore();
  });
  parts = parts.filter(p => p.life > 0 && p.y < cv.height + 20);
  raf = parts.length ? requestAnimationFrame(loop) : (ctx.clearRect(0, 0, cv.width, cv.height), null);
}

go(0);
</script>
</body>
</html>
