---
layout: page
title: Maar World
show_title: false
permalink: /index.html
full_width: false
header:
  theme: dark
  background: 'linear-gradient(135deg, rgba(0,0,0,1), rgba(0,0,0,.5))'
---

<!-- HERO (single rotating line, smooth slide+fade every 1.5s) -->
<div class="hero hero--center hero--statement rotating-hero single-line">
  <div class="hero__content">
    <div class="rotator rotator--single rotator-sync" aria-live="polite">
      <div class="rotator-viewport">
        <div class="rotator-track">
          <span class="rot-line">A space for fluid music‑making</span>
          <span class="rot-line">that moves beyond binaries,</span>
          <span class="rot-line">between physical and digital formats,</span>
          <span class="rot-line">a human–machine commonwealth,</span>
          <span class="rot-line">a blend of innovation and</span>
          <span class="rot-line">a continuation of tradition.</span>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- PHOTO SWIPER -->
<section class="section-block section-block--photos">
  <div style="max-width:1180px;margin:0 auto;padding:0 0.0rem;">
    <div class="swiper my-3 swiper-demo swiper-demo--image swiper-demo--home">
      <div class="swiper__wrapper">
        {% assign photo_captions = "
        2024_ss-1.jpeg:Emergent layering session,
        2024_ss-2.jpeg:Gesture capture + sonic response,
        2024_ss-3.jpeg:Collective listening micro‑ritual,
        2024_ss-4.jpeg:Interface prototyping table,
        2024_ss-5.jpeg:Transduction + tactile mapping,
        2024_ss-6.jpeg:Improvisation under orbital rules,
        2024_ss-7.jpeg:Hybrid instrument assembly,
        2024_ss-8.jpeg:Real‑time parameter negotiation,
        2024_ss-9.jpeg:Spatial focus & diffusion test,
        2024_ss-10.jpeg:Multichannel rehearsal fragment,
        2024_ss-11.jpeg:Embodied timing exploration,
        2024_ss-12.jpeg:Closing resonance capture
        " | split: "," %}
        {% for item in photo_captions %}
          {% assign parts = item | split: ":" %}
          {% assign filename = parts[0] | strip %}
          {% assign caption = parts[1] | default: "" | strip %}
          {% if filename != "" %}
          <div class="swiper__slide">
            <img class="lightbox-ignore" src="/img/collect-landing/{{ filename }}" alt="{{ caption | escape }}"/>
            <div class="slide-caption">{{ caption }}</div>
          </div>
          {% endif %}
        {% endfor %}
      </div>
      <div class="swiper__button swiper__button--prev fas fa-chevron-left"></div>
      <div class="swiper__button swiper__button--next fas fa-chevron-right"></div>
    </div>
  </div>
</section>

<!-- WORK IN PROGRESS -->
<section class="section-block section-block--wip">
  <div class="wip-section" style="max-width:960px;margin:0 auto;padding:0 1.25rem;">
    <div class="hero hero--center hero--statement rotating-hero single-line hero--wip">
      <div class="hero__content">
        <div class="rotator rotator--wip rotator-sync" aria-label="Work in progress translations" aria-live="polite">
          <div class="rotator-viewport">
            <div class="rotator-track">
              <span class="rot-line">Work in progress</span>
              <span class="rot-line">Trabajo en progreso</span>
              <span class="rot-line">Travail en cours</span>
              <span class="rot-line">Arbeit im Gange</span>
              <span class="rot-line">Lavoro in corso</span>
              <span class="rot-line">Trabalho em andamento</span>
              <span class="rot-line">Работа в процессе</span>
              <span class="rot-line">Prace w toku</span>
              <span class="rot-line">Werk in uitvoering</span>
              <span class="rot-line">Arbete pågår</span>
              <span class="rot-line">Çalışma devam ediyor</span>
              <span class="rot-line">العمل جارٍ</span>
              <span class="rot-line">कार्य प्रगति पर है</span>
              <span class="rot-line">工作进行中</span>
              <span class="rot-line">作業中</span>
              <span class="rot-line">Kazi inaendelea</span>
              <span class="rot-line">Umsebenzi uyaqhubeka</span>
              <span class="rot-line">Kei te haere tonu te mahi</span>
              <span class="rot-line">Rurayqa qhipaman ruwakusqa</span>
              <span class="rot-line">Ałchíní bee na’ídoolkah</span>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div style="display:grid;gap:1.6rem;">
      <div class="wip-card" style="background:#141820;padding:1.25rem 1.15rem;border:1px solid #232a33;border-radius:16px;">
        <h4 style="margin:.1rem 0 .55rem;font-size:1.15rem;">plantasia.space</h4>
        <p style="margin:0 0 .9rem;line-height:1.5;opacity:.9;">
          <strong>plantasia.space</strong> is a platform designed for interactive music releases. It simplifies the creation and customization of Orbiters and Entangled Worlds, and allows artists to upload music that users can listen to and remix in real time. The platform encourages innovation through playful music interaction and healthy sensory exploration.
        </p>
        <a href="https://plantasia.space" class="button button--outline button--rounded" style="font-size:.8rem;">Visit</a>
      </div>
      <div class="wip-card" style="background:#141820;padding:1.25rem 1.15rem;border:1px solid #232a33;border-radius:16px;">
        <h4 style="margin:.1rem 0 .55rem;font-size:1.15rem;">Orbits & Bodies</h4>
        <p style="margin:0 0 .9rem;line-height:1.5;opacity:.9;">Orbits and Bodies explores the entanglement of embodied gesture, astronomical data, and networked computation  in real‑time audiovisual space.</p>
        <a href="/lab/en/orbits-and-bodies.html" class="button button--outline button--rounded" style="font-size:.8rem;">Read</a>
      </div>
      <div class="wip-card" style="background:#141820;padding:1.25rem 1.15rem;border:1px solid #232a33;border-radius:16px;">
        <h4 style="margin:.1rem 0 .55rem;font-size:1.15rem;">Orbiters Orchestra</h4>
        <p style="margin:0 0 .9rem;line-height:1.5;opacity:.9;">Collaborative workshop instrument: card‑driven layering generating an emergent orbital score.</p>
        <a href="/lab/en/ip-orchestra" class="button button--outline button--rounded" style="font-size:.8rem;">Open</a>
      </div>
      <div style="display:flex;gap:.75rem;flex-wrap:wrap;justify-content:center;margin-top:1.25rem;">
        <a href="/lab" class="button button--primary button--rounded" style="background:#ff00de;border:none;">Lab</a>
        <a href="/landings" class="button button--outline-error button--rounded">Live</a>
        <a href="/bookings" class="button button--outline-info button--rounded">Bookings</a>
      </div>
    </div>
  </div>
</section>

<style>
/***** Unified vertical spacing (refined) *****/
.section-block { margin-top:2rem; }
@media (min-width:800px){ .section-block { margin-top:2.75rem; } }
/* First swiper immediately after hero: slightly tighter */
.section-block--photos { margin-top:1.25rem; }
/* WIP after photos keeps standard rhythm */
.section-block--wip { margin-top:1.25rem !important; }
/* Video swiper gets a bit more separation */
.section-block--videos { margin-top:3rem; }
@media (min-width:1000px){ .section-block--videos { margin-top:3.5rem; } }
</style>

<!-- VIDEO SWIPER MOVED TO BOTTOM -->
<section class="section-block section-block--videos">
  <div style="max-width:1180px;margin:0 auto;padding:0 1.25rem;">
    <div class="swiper my-3 swiper-demo swiper-demo--digital">
      <div class="swiper__wrapper">
        <div class="swiper__slide">
          <div class="video-frame">
            <video src="/img/collect-landing/digital-1.mp4" autoplay muted loop playsinline></video>
          </div>
        </div>
        <div class="swiper__slide">
          <div class="video-frame">
            <video src="/img/collect-landing/digital-2.mp4" autoplay muted loop playsinline></video>
          </div>
        </div>
        <div class="swiper__slide">
          <div class="video-frame">
            <video src="/img/collect-landing/digital-3.mp4" autoplay muted loop playsinline></video>
          </div>
        </div>
      </div>
      <div class="swiper__button swiper__button--prev fas fa-chevron-left"></div>
      <div class="swiper__button swiper__button--next fas fa-chevron-right"></div>
    </div>
  </div>
</section>

<!-- SWIPER INIT -->
<script>
  {%- include scripts/lib/swiper.js -%}
  (function(){
    function initSwiper(sel){
      if (typeof window.jQuery !== 'undefined' && window.jQuery(sel).swiper) {
        window.jQuery(sel).swiper({ animation:true });
      } else if (window.SwiperLite) {
        document.querySelectorAll(sel).forEach(function(el){
          new SwiperLite(el, { animation:true });
        });
      }
    }
    var SOURCES = (window.TEXT_VARIABLES && window.TEXT_VARIABLES.sources) || {};
    function start(){
      initSwiper('.swiper-demo--home');
      initSwiper('.swiper-demo--digital');
    }
    if (window.Lazyload && SOURCES.jquery){
      window.Lazyload.js(SOURCES.jquery, start);
    } else {
      document.addEventListener('DOMContentLoaded', start);
    }
  })();
</script>

<style>
  .swiper-demo--home,
  .swiper-demo--digital {
    --swiper-border-radius:18px;
    position:relative;
    border:1px solid #262d36;
    border-radius:var(--swiper-border-radius);
    overflow:hidden;
    background:#0d1014;
  }
  .swiper-demo--home .swiper__slide,
  .swiper-demo--digital .swiper__slide { position:relative; }

  .swiper-demo--home .swiper__slide img {
    width:100%; display:block; object-fit:cover;
  }

  .swiper-demo--digital .video-frame {
    width:100%;
    background:#000;
    display:flex;
    align-items:center;
    justify-content:center;
    padding:0;
  }
  .swiper-demo--digital .video-frame video {
    width:100%;
    height:auto;
    max-height:780px;
    object-fit:contain;
  }

  .swiper-demo--home .slide-caption {
    position:absolute;left:0;bottom:0;width:100%;
    padding:.6rem .85rem;font-size:.75rem;letter-spacing:.04em;line-height:1.25;
    background:linear-gradient(180deg,rgba(0,0,0,0) 0%,rgba(0,0,0,.65) 88%);
    color:#f5f6f7;
  }

  /* FIX: center icons in arrow buttons */
  .swiper-demo--home .swiper__button,
  .swiper-demo--digital .swiper__button {
    background:rgba(0,0,0,.45);
    backdrop-filter:blur(4px);
    color:#fff;
    width:42px;
    height:42px;
    font-size:16px;
    border-radius:50%;
    top:50%;
    transform:translateY(-50%);
    transition:.25s;
    display:flex;              /* center fix */
    align-items:center;        /* center vertically */
    justify-content:center;    /* center horizontally */
    line-height:1;             /* avoid vertical offset */
    padding:0;
  }
  .swiper-demo--home .swiper__button:hover,
  .swiper-demo--digital .swiper__button:hover {
    background:rgba(255,0,222,.75);
  }
  /* Optional: precise left/right placement */
  .swiper-demo--home .swiper__button--prev,
  .swiper-demo--digital .swiper__button--prev { left:10px; }
  .swiper-demo--home .swiper__button--next,
  .swiper-demo--digital .swiper__button--next { right:10px; }

  @media (min-width:920px){
    .swiper-demo--home { max-height:560px; }
    .swiper-demo--digital { max-height:none; }
  }
</style>

<!-- UPDATED (replace previous ROTATOR SCRIPT + related minor CSS improvements) -->
<script>
(function(){
  const DWELL = 3600; // ms each line fully visible
  const MOVE  = 680;  // ms transition
  const EASE  = 'cubic-bezier(.65,.05,.25,1)';
  const rotators = Array.from(document.querySelectorAll('.rotator-sync'));
  if(!rotators.length) return;

  function computeMaxHeight(r){
    const {track,viewport} = r.__rt;
    let maxH = 0;
    const prevT = track.style.transition;
    const prevX = track.style.transform;
    track.style.transition='none';
    track.style.transform='translateY(0)';
    for(const child of track.children){
      const h = child.getBoundingClientRect().height;
      if(h>maxH) maxH=h;
    }
    viewport.style.height = maxH + 'px';
    track.style.transition = prevT;
    track.style.transform  = prevX;
  }

  rotators.forEach(r=>{
    const viewport = r.querySelector('.rotator-viewport');
    const track    = r.querySelector('.rotator-track');
    if(!viewport||!track) return;
    r.__rt = {viewport,track,running:true};
    viewport.classList.add('rotator-init');
    // Wait for layout settle
    requestAnimationFrame(()=>{ computeMaxHeight(r); viewport.classList.remove('rotator-init'); });
    r.addEventListener('mouseenter',()=>r.__rt.running=false);
    r.addEventListener('mouseleave',()=>{ if(!r.__rt.running) r.__rt.running=true; });
  });

  function advance(r){
    if(!r.__rt.running) return;
    const {track} = r.__rt;
    const first = track.children[0];
    const next  = track.children[1];
    if(!first||!next) return;
    const h = first.getBoundingClientRect().height; // height locked by viewport
    track.style.transition = `transform ${MOVE}ms ${EASE}`;
    first.classList.add('fade-out');
    next.classList.add('fade-in');
    track.style.transform = `translateY(-${h}px)`;
    const done=()=>{
      track.removeEventListener('transitionend',done);
      track.style.transition='none';
      track.appendChild(first);
      track.style.transform='translateY(0)';
      first.classList.remove('fade-out');
      track.children[0].classList.remove('fade-in');
    };
    track.addEventListener('transitionend',done);
  }

  function tick(){ rotators.forEach(advance); }
  setTimeout(()=>{ tick(); setInterval(tick, DWELL); }, DWELL);

  let resizeTimer;
  window.addEventListener('resize', ()=>{
    clearTimeout(resizeTimer);
    resizeTimer = setTimeout(()=> rotators.forEach(computeMaxHeight), 140);
  });

  if(window.matchMedia('(prefers-reduced-motion: reduce)').matches){ rotators.forEach(r=>r.__rt.running=false); }
})();
</script>

<style>
/* Minor rotator viewport transition (shared) */
.rotator-viewport.rotator-init { opacity:0; }
.rotator-viewport { transition:opacity .35s ease; }
.rotator-viewport:not(.rotator-init){ opacity:1; }
</style>

<!-- ROTATOR STYLES (append / merge) -->
<style>
.rotating-hero.single-line { padding: 3.2rem 1rem 1.4rem; }
.rotator--single { max-width: 1040px; margin: 0 auto; text-align: center; position: relative; }
.rotator-viewport { overflow: hidden; position: relative; width: 100%; }
.rotator-track { display: flex; flex-direction: column; will-change: transform; }
/* Unified rotator line style (matches bottom rotator) */
.rotator--single .rot-line { font-size:1.55rem; line-height:1.3; font-weight:500; letter-spacing:.03em; color:#fff; padding:0; margin:0; opacity:1; transition:opacity .4s ease; text-wrap:balance; white-space:normal; }
@media (max-width:640px){ .rotating-hero.single-line { padding: 2.6rem 1rem 1rem; } .rotator--single .rot-line { font-size:1.28rem; } }
.rotator--single .rot-line.fade-out { opacity:0; transition:opacity .4s ease; }
.rotator--single .rot-line.fade-in { opacity:0; animation:fadeInLine .55s forwards; }
@keyframes fadeInLine { 0% { opacity:0; transform:translateY(6px);} 60% { opacity:1; transform:translateY(0);} 100% { opacity:1; transform:translateY(0);} }
.rotator--single:hover .rot-line, .rotator--single:focus-within .rot-line { filter:brightness(1.05); }
</style>

<style>
/* Page-specific overrides only (global spacing & rotator in custom.scss) */
.wip-section, .wip-section h4, .wip-card, .wip-card p { text-align:center; }
.wip-card a.button { display:inline-block; }
.section-block--wip { margin-top:1.25rem !important; }
.hero--wip { padding-top:0 !important; padding-bottom:.6rem; }
</style>

