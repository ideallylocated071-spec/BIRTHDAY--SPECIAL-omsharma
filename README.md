<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Happy Birthday Om Sharma! 🎂</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,700;1,700&family=Poppins:wght@300;400;500;600;700&family=Dancing+Script:wght@600;700&display=swap" rel="stylesheet"/>
<style>
*,*::before,*::after{margin:0;padding:0;box-sizing:border-box}
html{scroll-behavior:smooth}
body{font-family:'Poppins',sans-serif;background:#0a0010;min-height:100vh;color:#fff;overflow-x:hidden}

/* ── STAR CANVAS ── */
#starCanvas{position:fixed;inset:0;z-index:0;pointer-events:none}

/* ── BG ── */
.page-bg{
  position:fixed;inset:0;z-index:0;
  background:
    radial-gradient(ellipse 80% 60% at 50% 0%,#2d0050 0%,transparent 70%),
    radial-gradient(ellipse 60% 50% at 0% 100%,#1a0030 0%,transparent 60%),
    radial-gradient(ellipse 60% 60% at 100% 80%,#0d001f 0%,transparent 60%),
    linear-gradient(180deg,#0a0010 0%,#12001e 100%);
}

/* ── PETALS ── */
.petal{position:fixed;pointer-events:none;animation:petalFall linear infinite;z-index:2;opacity:.7}
@keyframes petalFall{0%{transform:translateY(-40px) rotate(0deg);opacity:.8}100%{transform:translateY(110vh) rotate(540deg);opacity:0}}

/* ── MUSIC ── */
#musicToggle{
  position:fixed;top:18px;right:18px;z-index:9999;
  width:46px;height:46px;border-radius:50%;
  border:1px solid rgba(255,255,255,.2);
  background:rgba(255,255,255,.1);backdrop-filter:blur(12px);
  color:#fff;font-size:18px;cursor:pointer;
  box-shadow:0 4px 20px rgba(0,0,0,.4);transition:transform .2s;
}
#musicToggle:hover{transform:scale(1.1)}

/* ── PAGES ── */
.page{display:none;min-height:100vh;flex-direction:column;align-items:center;justify-content:center;padding:30px 16px 40px;position:relative;z-index:3;animation:pageIn .8s cubic-bezier(.22,1,.36,1) both}
.page.active{display:flex}
@keyframes pageIn{from{opacity:0;transform:translateY(28px) scale(.97)}to{opacity:1;transform:translateY(0) scale(1)}}

/* ── ORB DECORATIONS ── */
.orb{position:fixed;border-radius:50%;pointer-events:none;filter:blur(80px);opacity:.15;animation:orbDrift ease-in-out infinite alternate;z-index:1}
.orb1{width:340px;height:340px;background:#9333ea;top:-100px;left:-80px;animation-duration:8s}
.orb2{width:280px;height:280px;background:#ec4899;bottom:-80px;right:-60px;animation-duration:10s;animation-delay:-3s}
.orb3{width:220px;height:220px;background:#6366f1;top:40%;left:55%;animation-duration:12s;animation-delay:-6s}
@keyframes orbDrift{0%{transform:translate(0,0) scale(1)}100%{transform:translate(28px,-28px) scale(1.1)}}

/* ══════════════════════════════
   GIFT SURPRISE PAGE (page1)
══════════════════════════════ */
.surprise-wrap{display:flex;flex-direction:column;align-items:center;gap:10px;text-align:center;max-width:420px;width:100%}

.top-tag{font-size:12px;letter-spacing:.18em;text-transform:uppercase;color:rgba(249,168,212,.6);margin-bottom:4px;animation:fadeDown .8s ease both;animation-delay:.2s}
@keyframes fadeDown{from{opacity:0;transform:translateY(-12px)}to{opacity:1;transform:translateY(0)}}

.surprise-title{
  font-family:'Dancing Script',cursive;
  font-size:clamp(28px,8vw,52px);
  background:linear-gradient(135deg,#fff 0%,#f9a8d4 40%,#e879f9 75%,#c084fc 100%);
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;
  filter:drop-shadow(0 0 28px rgba(232,121,249,.55));
  line-height:1.15;
  animation:fadeDown .8s ease both;animation-delay:.35s;
}

.name-badge{
  display:inline-block;
  background:linear-gradient(135deg,#9333ea,#ec4899);
  border-radius:40px;padding:8px 26px;
  font-family:'Playfair Display',serif;font-style:italic;
  font-size:clamp(22px,6vw,38px);font-weight:700;
  color:#fff;
  box-shadow:0 0 0 3px rgba(232,121,249,.3),0 12px 40px rgba(147,51,234,.45);
  animation:namePop .9s cubic-bezier(.34,1.56,.64,1) both;animation-delay:.55s;
  position:relative;overflow:hidden;
}
.name-badge::before{content:'';position:absolute;inset:0;background:linear-gradient(90deg,transparent,rgba(255,255,255,.15),transparent);animation:shimmer 2.5s ease-in-out infinite}
@keyframes shimmer{0%{transform:translateX(-100%)}100%{transform:translateX(100%)}}
@keyframes namePop{from{opacity:0;transform:scale(.5) rotate(-8deg)}to{opacity:1;transform:scale(1) rotate(0)}}

.gift-stage{
  position:relative;width:180px;height:180px;
  display:flex;align-items:center;justify-content:center;
  cursor:pointer;
  animation:floatGift 3s ease-in-out infinite;
  margin:10px 0;
}
@keyframes floatGift{0%,100%{transform:translateY(0) rotate(-2deg)}50%{transform:translateY(-14px) rotate(2deg)}}
.gift-emoji{font-size:120px;filter:drop-shadow(0 0 28px rgba(232,121,249,.7)) drop-shadow(0 8px 24px rgba(0,0,0,.5));transition:transform .3s}
.gift-stage:hover .gift-emoji{transform:scale(1.1)}
.gift-ring{position:absolute;inset:-16px;border-radius:50%;border:1.5px solid rgba(232,121,249,.25);animation:ringPulse 2.5s ease-in-out infinite}
.gift-ring2{position:absolute;inset:-34px;border-radius:50%;border:1px solid rgba(249,168,212,.15);animation:ringPulse 2.5s ease-in-out infinite .5s}
@keyframes ringPulse{0%,100%{opacity:.3;transform:scale(1)}50%{opacity:.9;transform:scale(1.06)}}

.tap-hint{
  font-size:13px;color:rgba(249,168,212,.65);letter-spacing:.06em;
  animation:hintBlink 2s ease-in-out infinite;
}
@keyframes hintBlink{0%,100%{opacity:.5}50%{opacity:1}}

.funny-tagline{
  font-size:14px;color:rgba(255,255,255,.5);
  line-height:1.6;max-width:320px;font-style:italic;
}

/* ══════════════════════════════
   REVEAL SCREEN (page1b)
══════════════════════════════ */
#page1b{background:transparent}
.reveal-card{
  background:rgba(255,255,255,.05);
  backdrop-filter:blur(28px) saturate(160%);
  border:1px solid rgba(255,255,255,.1);
  border-radius:32px;
  padding:clamp(28px,6vw,52px) clamp(22px,5vw,48px);
  max-width:460px;width:100%;
  box-shadow:0 0 0 1px rgba(232,121,249,.12),0 28px 80px rgba(0,0,0,.5),inset 0 1px 0 rgba(255,255,255,.08);
  text-align:center;
}
.reveal-emoji-row{font-size:36px;letter-spacing:8px;margin-bottom:16px;animation:bounceIn .6s cubic-bezier(.34,1.56,.64,1) both}
@keyframes bounceIn{from{opacity:0;transform:scale(.4)}to{opacity:1;transform:scale(1)}}

.reveal-title{
  font-family:'Playfair Display',serif;font-style:italic;font-weight:700;
  font-size:clamp(26px,7vw,44px);
  background:linear-gradient(135deg,#fff 10%,#f9a8d4 45%,#e879f9 80%);
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;
  filter:drop-shadow(0 0 18px rgba(232,121,249,.4));
  line-height:1.2;margin-bottom:10px;
}
.reveal-funny{
  font-size:clamp(13px,3.5vw,16px);color:rgba(249,168,212,.8);
  line-height:1.75;margin-bottom:20px;
}
.neon-div{width:160px;height:1px;margin:0 auto 20px;background:linear-gradient(90deg,transparent,#e879f9,#f9a8d4,#e879f9,transparent);box-shadow:0 0 10px #e879f9}

/* ── TEDDY GRID ── */
.teddy-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:14px;margin:14px 0 18px;width:100%}
.teddy-card{
  background:rgba(255,255,255,.07);
  border:1px solid rgba(255,255,255,.1);
  border-radius:20px;padding:18px 12px;
  cursor:pointer;transition:transform .3s,box-shadow .3s;
  animation:teddyIn .6s cubic-bezier(.34,1.56,.64,1) both;
  animation-delay:var(--td);
}
.teddy-card:hover{transform:translateY(-6px) scale(1.04);box-shadow:0 12px 32px rgba(232,121,249,.3)}
.teddy-card .t-emoji{font-size:clamp(38px,10vw,52px);display:block;margin-bottom:6px}
.teddy-card .t-name{font-size:11px;color:rgba(249,168,212,.7);letter-spacing:.07em}
@keyframes teddyIn{from{opacity:0;transform:scale(.6) rotate(-8deg)}to{opacity:1;transform:scale(1) rotate(0)}}

.msg-bubble{
  background:rgba(232,121,249,.1);
  border:1px solid rgba(232,121,249,.25);
  border-radius:18px;padding:16px 18px;
  font-size:13px;color:rgba(255,255,255,.75);
  line-height:1.7;margin-bottom:18px;
  font-style:italic;display:none;
  animation:bubbleIn .4s ease both;
}
@keyframes bubbleIn{from{opacity:0;transform:scale(.9)}to{opacity:1;transform:scale(1)}}

.glass-btn{
  width:100%;padding:15px;border:none;border-radius:16px;
  font-family:'Poppins',sans-serif;font-size:14px;font-weight:600;
  letter-spacing:.04em;cursor:pointer;color:#fff;
  background:linear-gradient(135deg,#9333ea,#ec4899);
  box-shadow:0 8px 28px rgba(147,51,234,.4);
  transition:transform .2s,box-shadow .2s;margin-top:6px;
}
.glass-btn:hover{transform:translateY(-2px);box-shadow:0 14px 40px rgba(147,51,234,.55)}
.glass-btn:active{transform:scale(.98)}
.glass-btn-outline{background:transparent;border:1.5px solid rgba(232,121,249,.4);color:rgba(249,168,212,.9);box-shadow:none;margin-top:10px}
.glass-btn-outline:hover{background:rgba(232,121,249,.1);box-shadow:0 0 20px rgba(232,121,249,.2)}

/* ══════════════════════════════
   PAGE 2 — FUNNY LETTER
══════════════════════════════ */
#page2{background:transparent}
.letter-wrap{
  background:rgba(255,255,255,.05);
  backdrop-filter:blur(24px);
  border:1px solid rgba(255,255,255,.1);
  border-radius:28px;padding:clamp(26px,6vw,48px) clamp(20px,5vw,44px);
  max-width:480px;width:100%;
  box-shadow:0 28px 80px rgba(0,0,0,.5),0 0 0 1px rgba(232,121,249,.1);
  position:relative;overflow:hidden;
}
.letter-wrap::after{content:'🎉';font-size:100px;position:absolute;right:-10px;bottom:-10px;opacity:.06;line-height:1}
.letter-from{font-size:11px;letter-spacing:.15em;text-transform:uppercase;color:rgba(249,168,212,.55);margin-bottom:8px}
.letter-head{font-family:'Dancing Script',cursive;font-size:clamp(22px,6vw,36px);color:#f9a8d4;margin-bottom:6px}
.letter-divline{width:80px;height:1px;background:linear-gradient(90deg,transparent,#e879f9,transparent);margin:0 auto 18px}
.letter-body{font-size:14px;color:rgba(255,255,255,.75);line-height:1.9;white-space:pre-line;text-align:left}
.letter-sign{font-family:'Dancing Script',cursive;font-size:22px;color:#e879f9;margin-top:22px;text-align:right}

/* ── FUNNY FACT BADGES ── */
.fact-strip{display:flex;flex-wrap:wrap;gap:8px;margin:14px 0;justify-content:center}
.fact-badge{
  background:rgba(232,121,249,.12);border:1px solid rgba(232,121,249,.25);
  border-radius:20px;padding:6px 14px;
  font-size:12px;color:rgba(249,168,212,.9);
  cursor:default;transition:transform .2s,background .2s;
}
.fact-badge:hover{transform:scale(1.06);background:rgba(232,121,249,.22)}

/* ══════════════════════════════
   PAGE 3 — MEMORY GALLERY
══════════════════════════════ */
#page3{background:transparent;padding:20px 12px 36px}
.gallery-top{text-align:center;margin-bottom:18px}
.gallery-head{font-family:'Dancing Script',cursive;font-size:clamp(26px,6vw,40px);color:#f9a8d4;filter:drop-shadow(0 0 12px rgba(249,168,212,.5))}
.gallery-sub{font-size:13px;color:rgba(255,255,255,.4);margin-top:4px}
.polaroid-strip{display:flex;gap:18px;overflow-x:auto;padding:16px 20px 24px;scroll-snap-type:x mandatory;-webkit-overflow-scrolling:touch;width:100%;max-width:600px;scrollbar-width:none}
.polaroid-strip::-webkit-scrollbar{display:none}
.polaroid{flex:0 0 auto;width:clamp(155px,42vw,195px);scroll-snap-align:center;background:#1a0830;border:1px solid rgba(255,255,255,.08);border-radius:4px;box-shadow:0 8px 32px rgba(0,0,0,.5);padding:10px 10px 30px;position:relative;transform:rotate(var(--rot));transition:transform .3s,box-shadow .3s;cursor:pointer;animation:polaroidIn .5s cubic-bezier(.34,1.56,.64,1) both;animation-delay:var(--delay)}
@keyframes polaroidIn{from{opacity:0;transform:rotate(var(--rot)) scale(.5) translateY(40px)}to{opacity:1;transform:rotate(var(--rot)) scale(1) translateY(0)}}
.polaroid:hover{transform:rotate(0deg) scale(1.07);box-shadow:0 16px 44px rgba(232,121,249,.3)}
.polaroid-inner{width:100%;aspect-ratio:1;border-radius:2px;display:flex;align-items:center;justify-content:center;font-size:clamp(52px,12vw,72px);background:linear-gradient(135deg,rgba(147,51,234,.2),rgba(236,72,153,.2))}
.polaroid-caption{position:absolute;bottom:7px;left:0;right:0;text-align:center;font-family:'Dancing Script',cursive;font-size:13px;color:rgba(249,168,212,.75);padding:0 8px;overflow:hidden;white-space:nowrap;text-overflow:ellipsis}
.polaroid-heart{position:absolute;top:-10px;right:-8px;font-size:20px;animation:hFloat 2s ease-in-out infinite;animation-delay:var(--delay)}
@keyframes hFloat{0%,100%{transform:translateY(0) rotate(-10deg)}50%{transform:translateY(-7px) rotate(10deg)}}

.fact-card-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:12px;max-width:500px;width:100%;margin-top:14px}
.fact-card{background:rgba(255,255,255,.05);border:1px solid rgba(255,255,255,.08);border-radius:18px;padding:16px 14px;cursor:pointer;transition:transform .3s,box-shadow .3s;perspective:600px}
.fact-card:hover{transform:translateY(-4px) scale(1.03);box-shadow:0 10px 28px rgba(232,121,249,.25)}
.fact-card .fc-emoji{font-size:30px;margin-bottom:6px;display:block}
.fact-card .fc-text{font-size:11px;color:rgba(255,255,255,.55);line-height:1.5}

/* ══════════════════════════════
   PAGE 4 — WISH UNLOCK
══════════════════════════════ */
#page4{background:transparent}
.wish-card{background:rgba(255,255,255,.05);backdrop-filter:blur(24px);border:1px solid rgba(255,255,255,.1);border-radius:28px;padding:clamp(28px,6vw,52px) clamp(22px,5vw,48px);max-width:440px;width:100%;text-align:center;box-shadow:0 28px 80px rgba(0,0,0,.5)}
.wish-q{font-family:'Playfair Display',serif;font-style:italic;font-size:clamp(20px,5vw,30px);color:#f9a8d4;margin-bottom:6px}
.wish-sub{font-size:13px;color:rgba(255,255,255,.4);margin-bottom:24px}
.wish-balls{display:flex;gap:16px;justify-content:center;flex-wrap:wrap;margin-bottom:20px}
.wish-ball{
  width:80px;height:80px;border-radius:50%;border:none;
  font-size:13px;font-weight:600;font-family:'Poppins',sans-serif;
  color:#fff;cursor:pointer;transition:transform .3s,box-shadow .3s;
  animation:wishBounce 2s ease-in-out infinite;
}
.wish-ball:nth-child(1){background:linear-gradient(135deg,#9333ea,#ec4899);animation-delay:0s;box-shadow:0 6px 20px rgba(147,51,234,.4)}
.wish-ball:nth-child(2){background:linear-gradient(135deg,#0891b2,#6366f1);animation-delay:.3s;box-shadow:0 6px 20px rgba(99,102,241,.4)}
.wish-ball:nth-child(3){background:linear-gradient(135deg,#d97706,#dc2626);animation-delay:.6s;box-shadow:0 6px 20px rgba(220,38,38,.4)}
@keyframes wishBounce{0%,100%{transform:translateY(0)}50%{transform:translateY(-9px)}}
.wish-ball:hover{transform:scale(1.14) translateY(-4px)}
.wish-reveal{background:rgba(232,121,249,.1);border:1px solid rgba(232,121,249,.3);border-radius:20px;padding:20px 22px;font-family:'Dancing Script',cursive;font-size:clamp(18px,5vw,24px);color:#f9a8d4;line-height:1.55;display:none;animation:wishIn .5s cubic-bezier(.34,1.56,.64,1) both}
@keyframes wishIn{from{opacity:0;transform:scale(.7) rotate(-5deg)}to{opacity:1;transform:scale(1) rotate(0)}}

/* ══════════════════════════════
   PAGE 5 — FINAL BLAST
══════════════════════════════ */
#page5{background:transparent}
.final-box{
  background:rgba(255,255,255,.04);
  backdrop-filter:blur(28px);
  border:1px solid rgba(232,121,249,.15);
  border-radius:32px;
  padding:clamp(32px,7vw,60px) clamp(22px,5vw,52px);
  max-width:460px;width:100%;text-align:center;
  box-shadow:0 0 0 1px rgba(232,121,249,.1),0 32px 100px rgba(0,0,0,.6);
  position:relative;overflow:hidden;
}
.final-box::before{content:'';position:absolute;inset:0;background:radial-gradient(ellipse 80% 50% at 50% 0%,rgba(232,121,249,.12),transparent);pointer-events:none}
.final-burst-emoji{font-size:60px;display:block;margin-bottom:10px;animation:spinBurst 1s cubic-bezier(.34,1.56,.64,1) both}
@keyframes spinBurst{from{opacity:0;transform:rotate(-180deg) scale(0)}to{opacity:1;transform:rotate(0) scale(1)}}
.final-name{font-family:'Dancing Script',cursive;font-size:clamp(30px,8vw,56px);background:linear-gradient(135deg,#fff 10%,#f9a8d4 45%,#e879f9 80%,#fbbf24 100%);-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;filter:drop-shadow(0 0 20px rgba(232,121,249,.5));line-height:1.2;margin-bottom:8px}
.final-tag{font-size:clamp(20px,5vw,28px);color:#fbbf24;font-weight:700;letter-spacing:.04em;margin-bottom:16px;filter:drop-shadow(0 0 10px rgba(251,191,36,.5))}
.final-hearts{font-size:28px;letter-spacing:10px;display:block;margin-bottom:18px;animation:hBeat 1.3s ease-in-out infinite}
@keyframes hBeat{0%,100%{transform:scale(1)}50%{transform:scale(1.15)}}
.final-msg{font-size:14px;color:rgba(255,255,255,.65);line-height:1.85;margin-bottom:22px}
.cake-tap{font-size:72px;cursor:pointer;display:block;margin:0 auto 10px;filter:drop-shadow(0 0 20px rgba(255,200,0,.6));animation:cakeWobble 2s ease-in-out infinite;user-select:none}
@keyframes cakeWobble{0%,100%{transform:rotate(-3deg)}50%{transform:rotate(3deg)}}
.cake-hint{font-size:12px;color:rgba(255,255,255,.35);letter-spacing:.08em;margin-bottom:20px;animation:pulseFade 2s ease-in-out infinite}
@keyframes pulseFade{0%,100%{opacity:.4}50%{opacity:1}}
.final-sign{font-family:'Dancing Script',cursive;font-size:20px;color:rgba(249,168,212,.8)}

/* ══ EFFECTS ══ */
.confetti-piece{position:fixed;pointer-events:none;z-index:9999;width:8px;height:8px;border-radius:2px;animation:cBurst 1.5s ease-out forwards}
@keyframes cBurst{0%{opacity:1;transform:translate(0,0) rotate(0)}100%{opacity:0;transform:translate(var(--tx),var(--ty)) rotate(var(--r))}}
.hfloat{position:fixed;pointer-events:none;z-index:9999;font-size:22px;animation:hUp 1.8s ease-out forwards}
@keyframes hUp{0%{opacity:1;transform:translateY(0) scale(1)}100%{opacity:0;transform:translateY(-160px) scale(1.4)}}
.sparkle{position:fixed;pointer-events:none;z-index:9998;font-size:15px;animation:spFade .9s ease-out forwards}
@keyframes spFade{0%{opacity:1;transform:scale(1)}100%{opacity:0;transform:scale(0) rotate(180deg)}}

/* ── LIGHTBOX ── */
#lightbox{position:fixed;inset:0;z-index:9999;background:rgba(5,0,15,.96);display:none;align-items:center;justify-content:center}
#lightbox.open{display:flex}
.lb-emoji-big{font-size:clamp(100px,28vw,160px);text-align:center;filter:drop-shadow(0 0 40px rgba(232,121,249,.6));animation:lbPop .4s cubic-bezier(.34,1.56,.64,1) both}
@keyframes lbPop{from{transform:scale(.3) rotate(-20deg)}to{transform:scale(1) rotate(0)}}
.lb-cap{font-family:'Dancing Script',cursive;font-size:clamp(18px,5vw,26px);color:#f9a8d4;text-align:center;margin-top:16px}
#lbClose{position:absolute;top:20px;right:20px;width:42px;height:42px;border-radius:50%;background:rgba(255,255,255,.1);border:none;color:#fff;font-size:20px;cursor:pointer}

@media(max-width:380px){.teddy-grid{grid-template-columns:repeat(2,1fr)}.wish-balls{gap:12px}.wish-ball{width:70px;height:70px}}
</style>
</head>
<body>

<canvas id="starCanvas"></canvas>
<div class="page-bg"></div>
<div class="orb orb1"></div>
<div class="orb orb2"></div>
<div class="orb orb3"></div>
<div id="petals"></div>

<button id="musicToggle">🎵</button>
<audio id="bgAudio" loop src="https://cdn.pixabay.com/audio/2022/05/27/audio_1808fbf07a.mp3" preload="auto"></audio>

<!-- LIGHTBOX -->
<div id="lightbox">
  <button id="lbClose" onclick="closeLB()">✕</button>
  <div id="lbContent" style="display:flex;flex-direction:column;align-items:center"></div>
</div>

<!-- ══════════════════════════════
     PAGE 1 — SURPRISE GIFT OPEN
══════════════════════════════ -->
<div class="page active" id="page1">
  <div class="surprise-wrap">
    <div class="top-tag">✦ shh… it's a surprise ✦</div>

    <div class="surprise-title">Hey there! 👀<br>Someone left a gift for you…</div>

    <div class="name-badge">🎂 Om Sharma 🎂</div>

    <div class="gift-stage" onclick="openSurprise()" id="giftStage">
      <div class="gift-ring"></div>
      <div class="gift-ring2"></div>
      <div class="gift-emoji" id="giftEmoji">🎁</div>
    </div>

    <div class="tap-hint" id="tapHintText">👆 Tap the gift to open!</div>

    <div class="funny-tagline">
      Warning: Opening this gift may cause<br>
      sudden happiness, uncontrollable smiling,<br>
      and mild embarrassment 😂
    </div>
  </div>
</div>

<!-- ══════════════════════════════
     PAGE 1B — REVEAL + TEDDIES
══════════════════════════════ -->
<div class="page" id="page1b">
  <div class="reveal-card">
    <div class="reveal-emoji-row">🎉 🎊 🥳</div>

    <div class="reveal-title">HAPPY BIRTHDAY<br>Om Sharma!! 🎂</div>

    <div class="neon-div"></div>

    <div class="reveal-funny">
      Bro, another year older and still going strong! 💪<br>
      We got you some <b style="color:#f9a8d4">very important friends</b> — tap them! 👇
    </div>

    <!-- TEDDY / CARTOON CHARACTERS -->
    <div class="teddy-grid">
      <div class="teddy-card" style="--td:.1s" onclick="teddyTap(this,'🧸','Classic Teddy','Your childhood called — it wants a hug! This is you every Sunday morning 😴')">
        <span class="t-emoji">🧸</span>
        <div class="t-name">Classic Teddy</div>
      </div>
      <div class="teddy-card" style="--td:.2s" onclick="teddyTap(this,'🐻','Chubby Bear','Looks innocent. Eats all the birthday cake. You know who this is 🎂😏')">
        <span class="t-emoji">🐻</span>
        <div class="t-name">Chubby Bear</div>
      </div>
      <div class="teddy-card" style="--td:.3s" onclick="teddyTap(this,'🦊','Sly Fox','The smartest one in the room. Also the most annoying. Happy Birthday, bhai 🦊😂')">
        <span class="t-emoji">🦊</span>
        <div class="t-name">Sly Fox</div>
      </div>
      <div class="teddy-card" style="--td:.4s" onclick="teddyTap(this,'🐼','Panda Bro','Eats. Sleeps. Exists. Absolute legend. This is your spirit animal on weekends 🐼💤')">
        <span class="t-emoji">🐼</span>
        <div class="t-name">Panda Bro</div>
      </div>
      <div class="teddy-card" style="--td:.5s" onclick="teddyTap(this,'🐯','Tiger Om','ROAR! Fearless, strong, and a little dramatic. Classic Om energy ⚡🐯')">
        <span class="t-emoji">🐯</span>
        <div class="t-name">Tiger Om</div>
      </div>
      <div class="teddy-card" style="--td:.6s" onclick="teddyTap(this,'🦁','Lion King','King energy only! You walk into a room and own it. Happy Birthday Your Majesty 👑🦁')">
        <span class="t-emoji">🦁</span>
        <div class="t-name">Lion King</div>
      </div>
    </div>

    <div class="msg-bubble" id="teddyMsg">Tap a character above!</div>

    <button class="glass-btn" onclick="goPage2()">📜 Read Your Roast Letter 😂</button>
    <button class="glass-btn glass-btn-outline" onclick="goPage3()">🎞️ Skip to Gallery</button>
  </div>
</div>

<!-- ══════════════════════════════
     PAGE 2 — FUNNY BDAY LETTER
══════════════════════════════ -->
<div class="page" id="page2">
  <div class="letter-wrap">
    <div class="letter-from">✦ a very official birthday letter ✦</div>
    <div class="letter-head">Dear Om Sharma,</div>
    <div class="letter-divline"></div>
    <div class="letter-body" id="letterBodyText"></div>

    <div class="fact-strip" style="margin-top:16px">
      <div class="fact-badge">🍕 Pizza Lover</div>
      <div class="fact-badge">😴 Sleep Champion</div>
      <div class="fact-badge">🎮 Gaming Pro</div>
      <div class="fact-badge">🤣 Makes Everyone Laugh</div>
      <div class="fact-badge">💪 Hidden Gym Guy</div>
      <div class="fact-badge">🧠 Secretly Genius</div>
    </div>

    <div class="letter-sign">With love (and a little roasting) 😂<br><span style="font-size:14px;font-family:'Poppins',sans-serif;color:rgba(249,168,212,.7)">— Your Family 💖</span></div>
  </div>

  <div style="max-width:480px;width:100%;margin-top:18px;display:flex;flex-direction:column;gap:10px;padding:0 4px">
    <button class="glass-btn" onclick="goPage3()">🎞️ See Memory Gallery</button>
    <button class="glass-btn glass-btn-outline" onclick="goPage1b()">⬅ Back</button>
  </div>
</div>

<!-- ══════════════════════════════
     PAGE 3 — CARTOON GALLERY
══════════════════════════════ -->
<div class="page" id="page3">
  <div class="gallery-top">
    <div style="font-size:28px">🎠</div>
    <div class="gallery-head">Om's Greatest Moments</div>
    <div class="gallery-sub">Tap any card to zoom in 🔍</div>
  </div>

  <div class="polaroid-strip" id="polaroidStrip">
    <!-- Built by JS -->
  </div>

  <div class="fact-card-grid" id="factCardGrid">
    <!-- Built by JS -->
  </div>

  <div style="max-width:500px;width:100%;margin-top:22px;padding:0 4px;display:flex;flex-direction:column;gap:10px">
    <button class="glass-btn" onclick="goPage4()">🎱 Unlock Your Wishes</button>
    <button class="glass-btn glass-btn-outline" onclick="goPage2()">⬅ Back</button>
  </div>
</div>

<!-- ══════════════════════════════
     PAGE 4 — 3 WISHES
══════════════════════════════ -->
<div class="page" id="page4">
  <div class="wish-card">
    <div style="font-size:32px;margin-bottom:10px">🪄</div>
    <div class="wish-q">3 Birthday Wishes</div>
    <div class="wish-sub">Pick one, Om Bhai — but choose wisely! 👆</div>

    <div class="wish-balls">
      <button class="wish-ball" onclick="pickWish(0,this)">Wish<br>#1<br>⭐</button>
      <button class="wish-ball" onclick="pickWish(1,this)">Wish<br>#2<br>🌙</button>
      <button class="wish-ball" onclick="pickWish(2,this)">Wish<br>#3<br>🔥</button>
    </div>

    <div class="wish-reveal" id="wishReveal"></div>
  </div>

  <div style="max-width:440px;width:100%;margin-top:18px;display:flex;flex-direction:column;gap:10px;padding:0 4px">
    <button class="glass-btn" onclick="goPage5()">🎂 See the Grand Finale!</button>
    <button class="glass-btn glass-btn-outline" onclick="goPage3()">⬅ Back</button>
  </div>
</div>

<!-- ══════════════════════════════
     PAGE 5 — GRAND FINALE
══════════════════════════════ -->
<div class="page" id="page5">
  <div class="final-box">
    <span class="final-burst-emoji">🎊</span>
    <div class="final-name" id="finalName">Om Sharma!</div>
    <div class="final-tag">🎂 HAPPY BIRTHDAY BHAI! 🎂</div>
    <span class="final-hearts">🧡 💛 ❤️</span>

    <div class="cake-tap" id="cakeTap" onclick="blowCake()">🎂</div>
    <div class="cake-hint" id="cakeHint">🌬️ Blow the candle, Birthday Boy!</div>

    <div class="final-msg" id="finalMsgBlock" style="display:none">
      Om bhai, you are the kind of person who makes every moment better. 🌟<br><br>
      Whether it's your nonsense jokes at midnight 😂, your legendary stubbornness 😤, or your secretly soft heart 🥹 — we love every weird part of you.<br><br>
      Today is YOUR day. Eat all the cake, break all the rules, and be your glorious self! 🎉
    </div>

    <div class="final-sign" id="finalSignText" style="display:none">
      With all the love in the world 💖<br>
      <span style="font-size:13px;font-family:'Poppins',sans-serif;color:rgba(255,255,255,.4)">— Your Family &amp; Friends 🎊</span>
    </div>
  </div>
</div>

<script>
/* ══ STAR FIELD ══ */
(function(){
  const c=document.getElementById('starCanvas'),ctx=c.getContext('2d');
  function resize(){c.width=window.innerWidth;c.height=window.innerHeight}
  resize();window.addEventListener('resize',resize);
  const stars=Array.from({length:200},()=>({x:Math.random()*window.innerWidth,y:Math.random()*window.innerHeight,r:.3+Math.random()*1.5,phase:Math.random()*Math.PI*2,speed:.002+Math.random()*.007}));
  function tick(t){
    ctx.clearRect(0,0,c.width,c.height);
    stars.forEach(s=>{const a=.25+.6*(.5+.5*Math.sin(t*s.speed+s.phase));ctx.beginPath();ctx.arc(s.x,s.y,s.r,0,Math.PI*2);ctx.fillStyle=`rgba(255,240,255,${a})`;ctx.fill()});
    requestAnimationFrame(tick);
  }
  requestAnimationFrame(tick);
})();

/* ══ PETALS ══ */
const petalE=['🌸','✨','💜','🌟','💫'];
const pc=document.getElementById('petals');
for(let i=0;i<12;i++){
  const p=document.createElement('div');p.className='petal';
  p.textContent=petalE[i%petalE.length];
  p.style.cssText=`left:${Math.random()*100}vw;font-size:${11+Math.random()*13}px;animation-duration:${7+Math.random()*9}s;animation-delay:-${Math.random()*10}s`;
  pc.appendChild(p);
}

/* ══ MUSIC ══ */
const audio=document.getElementById('bgAudio');
const mBtn=document.getElementById('musicToggle');
let playing=false;
function tryPlay(){audio.volume=.32;audio.play().then(()=>{playing=true;mBtn.textContent='🎵'}).catch(()=>{})}
mBtn.onclick=()=>{if(playing){audio.pause();playing=false;mBtn.textContent='🔇'}else{audio.play();playing=true;mBtn.textContent='🎵'}};
document.addEventListener('click',()=>{if(!playing)tryPlay()},{once:true});

/* ══ EFFECTS ══ */
function burst(x,y,n=32){
  const cols=['#e879f9','#f9a8d4','#c084fc','#fbbf24','#818cf8','#fff','#6ee7b7'];
  for(let i=0;i<n;i++){
    const el=document.createElement('div');el.className='confetti-piece';
    const a=Math.random()*360,d=90+Math.random()*150;
    el.style.cssText=`left:${x}px;top:${y}px;background:${cols[i%cols.length]};--tx:${Math.cos(a*Math.PI/180)*d}px;--ty:${Math.sin(a*Math.PI/180)*d}px;--r:${Math.random()*720}deg;border-radius:${Math.random()>.5?'50%':'2px'}`;
    document.body.appendChild(el);el.addEventListener('animationend',()=>el.remove());
  }
}
function floatH(x,y){
  ['💖','💛','🧡','💜','🎉'].forEach((e,i)=>{
    const h=document.createElement('div');h.className='hfloat';
    h.textContent=e;h.style.cssText=`left:${x-30+i*14}px;top:${y-10}px;animation-delay:${i*.1}s`;
    document.body.appendChild(h);h.addEventListener('animationend',()=>h.remove());
  });
}
function sparkleAt(e){
  if(e.target.closest('#lightbox')||e.target.closest('.teddy-card'))return;
  const s=document.createElement('div');s.className='sparkle';
  s.textContent=['✨','⭐','💫','🌟'][Math.floor(Math.random()*4)];
  s.style.cssText=`left:${e.clientX}px;top:${e.clientY}px`;
  document.body.appendChild(s);s.addEventListener('animationend',()=>s.remove());
}
document.addEventListener('click',sparkleAt);

/* ══ PAGE NAV ══ */
function showPage(id){
  document.querySelectorAll('.page').forEach(p=>p.classList.remove('active'));
  document.getElementById(id).classList.add('active');
  window.scrollTo({top:0,behavior:'smooth'});
}
function goPage1b(){showPage('page1b')}
function goPage2(){buildLetter();showPage('page2')}
function goPage3(){buildGallery();showPage('page3')}
function goPage4(){showPage('page4')}
function goPage5(){showPage('page5');tryPlay();startFinalBlast()}

/* ══ PAGE 1 — GIFT OPEN ══ */
function openSurprise(){
  const g=document.getElementById('giftEmoji');
  const stage=document.getElementById('giftStage');
  g.style.transition='transform .4s cubic-bezier(.34,1.56,.64,1)';
  g.style.transform='scale(1.25) rotate(10deg)';
  const r=stage.getBoundingClientRect();
  burst(r.left+r.width/2,r.top+r.height/2,40);
  floatH(r.left+r.width/2,r.top);
  document.getElementById('tapHintText').textContent='🎉 Woah! Opening…';
  setTimeout(()=>{
    for(let i=0;i<6;i++)setTimeout(()=>burst(Math.random()*window.innerWidth,Math.random()*window.innerHeight*.7,20),i*180);
    showPage('page1b');
  },700);
}

/* ══ TEDDY TAP ══ */
function teddyTap(el,emoji,name,msg){
  document.querySelectorAll('.teddy-card').forEach(c=>c.style.outline='');
  el.style.outline='2px solid rgba(232,121,249,.6)';
  const msgEl=document.getElementById('teddyMsg');
  msgEl.innerHTML=`<span style="font-size:28px">${emoji}</span><br><b style="color:#f9a8d4">${name}</b><br><span style="font-size:13px">${msg}</span>`;
  msgEl.style.display='block';
  const r=el.getBoundingClientRect();
  burst(r.left+r.width/2,r.top+r.height/2,22);
  floatH(r.left+r.width/2,r.top);
}

/* ══ FUNNY LETTER ══ */
function buildLetter(){
  document.getElementById('letterBodyText').innerHTML=`To the one and only <b style="color:#f9a8d4">Om Sharma</b>,

Congratulations! 🎉 You have successfully survived another year on planet Earth. This is a tremendous achievement and we are all very proud of you.

We remember the days when you were small, annoying, and always stealing the TV remote. You are still all of those things — but now you are also older. Time is wild. 🕐

Here are some official facts about Om Sharma:

🧸 <b>Age:</b> Old enough to know better, young enough to still be chaotic.

🦁 <b>Talent:</b> Can sleep through literally anything. An absolute gift.

🐯 <b>Life philosophy:</b> "Why do today what you can do tomorrow?" — truly ahead of his time.

🍕 <b>Diet:</b> Pizza, more pizza, and occasionally water.

🎮 <b>Weekend activity:</b> Gaming until 3am and then complaining about being tired.

But honestly bhai — you are the kind of person who makes every room brighter, every boring moment funnier, and every family gathering 10x more entertaining. 😂

We love you more than you probably deserve. (Just kidding. Mostly.) 🥹

On your birthday, may all your wishes come true — especially the ones you are too embarrassed to say out loud. 😏✨`;
}

/* ══ GALLERY ══ */
const polaroidData=[
  {emoji:'🧸',cap:'Baby Om Energy 🍼'},
  {emoji:'🐯',cap:'Tiger Mode: ON 🔥'},
  {emoji:'🦁',cap:'King of the House 👑'},
  {emoji:'🐼',cap:'Sunday Mood 💤'},
  {emoji:'🦊',cap:'Mastermind Hours 🧠'},
  {emoji:'🎮',cap:'3am Gaming Club 🎮'},
];
const factCards=[
  {emoji:'🍕',text:'Has never said no to pizza. Not even once in recorded history.'},
  {emoji:'😴',text:'Could sleep through a thunderstorm AND a birthday party.'},
  {emoji:'🤣',text:'Makes the most terrible jokes. We laugh anyway. Every time.'},
  {emoji:'💪',text:'Secretly strong. Pretends to be lazy. We see you, Om.'},
  {emoji:'🎂',text:'Gets emotional about cake. Completely valid. We support this.'},
  {emoji:'📱',text:'Phone battery always at 2%. Somehow always reachable. Mystery.'},
];
const ROTS=['-3deg','2deg','-2deg','3.5deg','-1.5deg','2.8deg'];

function buildGallery(){
  const strip=document.getElementById('polaroidStrip');
  strip.innerHTML='';
  polaroidData.forEach((d,i)=>{
    const pol=document.createElement('div');
    pol.className='polaroid';
    pol.style.cssText=`--rot:${ROTS[i%ROTS.length]};--delay:${i*.1}s`;
    pol.innerHTML=`<div class="polaroid-inner">${d.emoji}</div><div class="polaroid-caption">${d.cap}</div><div class="polaroid-heart" style="--delay:${i*.15}s">💜</div>`;
    pol.onclick=()=>{openLB(d.emoji,d.cap);const r=pol.getBoundingClientRect();burst(r.left+r.width/2,r.top+r.height/2,20)};
    strip.appendChild(pol);
  });

  const grid=document.getElementById('factCardGrid');
  grid.innerHTML='';
  factCards.forEach(f=>{
    grid.innerHTML+=`<div class="fact-card" onclick="factTap(this)"><span class="fc-emoji">${f.emoji}</span><div class="fc-text">${f.text}</div></div>`;
  });
}

function factTap(el){
  el.style.transform='scale(1.06)';
  const r=el.getBoundingClientRect();
  burst(r.left+r.width/2,r.top+r.height/2,16);
  setTimeout(()=>el.style.transform='',500);
}

/* ══ LIGHTBOX ══ */
function openLB(emoji,cap){
  document.getElementById('lbContent').innerHTML=`<div class="lb-emoji-big">${emoji}</div><div class="lb-cap">${cap}</div>`;
  document.getElementById('lightbox').classList.add('open');
  document.body.style.overflow='hidden';
}
function closeLB(){document.getElementById('lightbox').classList.remove('open');document.body.style.overflow=''}
document.getElementById('lightbox').addEventListener('click',e=>{if(e.target===document.getElementById('lightbox'))closeLB()});

/* ══ WISHES ══ */
const wishes=[
  `May every game you play this year end in VICTORY 🎮🏆\n(and may your WiFi never disconnect right before the final boss)`,
  `May there always be extra cheese on your pizza 🍕✨\nand may your phone battery NEVER drop below 20%`,
  `May this year bring you all the sleep you deserve 😴💤\n(which is approximately 14 hours per day, minimum)`,
];
let wishPicked=false;
function pickWish(idx,btn){
  if(wishPicked)return;wishPicked=true;
  const rev=document.getElementById('wishReveal');
  rev.textContent=wishes[idx];rev.style.display='block';
  btn.style.transform='scale(1.2)';btn.style.boxShadow='0 0 0 5px rgba(255,255,255,.2),0 14px 36px rgba(147,51,234,.6)';
  const r=btn.getBoundingClientRect();
  burst(r.left+r.width/2,r.top+r.height/2,28);
  floatH(r.left+r.width/2,r.top);
}

/* ══ FINAL PAGE ══ */
let cakeBlown=false;
function blowCake(){
  if(cakeBlown)return;cakeBlown=true;
  document.getElementById('cakeTap').textContent='🎆';
  document.getElementById('cakeHint').textContent='🎉 WISH GRANTED, OM BHAI!!';
  document.getElementById('finalMsgBlock').style.display='block';
  document.getElementById('finalSignText').style.display='block';
  for(let i=0;i<10;i++)setTimeout(()=>{burst(Math.random()*window.innerWidth,Math.random()*window.innerHeight*.8,28);floatH(Math.random()*window.innerWidth,window.innerHeight*.5)},i*220);
}

function startFinalBlast(){
  wishPicked=false;cakeBlown=false;
  document.getElementById('cakeTap').textContent='🎂';
  document.getElementById('cakeHint').textContent='🌬️ Blow the candle, Birthday Boy!';
  document.getElementById('finalMsgBlock').style.display='none';
  document.getElementById('finalSignText').style.display='none';
  setTimeout(()=>{
    for(let i=0;i<4;i++)setTimeout(()=>burst(Math.random()*window.innerWidth,Math.random()*window.innerHeight*.6,20),i*350);
  },400);
}
</script>
</body>
</html>
