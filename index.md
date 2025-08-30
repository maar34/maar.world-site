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

<!-- HERO -->
<div class="hero hero--center" style="padding:3.8rem 1rem 2.25rem;">
  <div class="hero__content">
    <h1 style="font-size:2.65rem;font-weight:800;letter-spacing:.035em;margin:0 0 1rem;background:linear-gradient(90deg,#ff00de,#ffa600);-webkit-background-clip:text;color:transparent;">
      Maar World
    </h1>
    <p style="font-size:1.2rem;max-width:760px;margin:0 auto 1.25rem;line-height:1.5;">
      A space for fluid music-making that moves beyond binaries, between physical and digital formats, a human–machine commonwealth, a blend of innovation and a continuation of tradition.
    </p>
  </div>
</div>

<!-- PHOTO SWIPER -->
<section style="padding:.75rem 0 0;">
  <div style="max-width:1180px;margin:0 auto;padding:0 1.25rem;">
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
<section style="padding:1.25rem 0 0;">
  <div style="max-width:960px;margin:0 auto;padding:0 1.25rem;">
    <h2 style="font-size:1.65rem;margin:.5rem 0 1rem;">Work in Progress</h2>
    <div style="display:grid;gap:1.6rem;">
      <div style="background:#141820;padding:1.25rem 1.15rem;border:1px solid #232a33;border-radius:16px;">
        <h3 style="margin:.1rem 0 .55rem;font-size:1.15rem;">plantasia.space</h3>
        <p style="margin:0 0 .9rem;line-height:1.5;opacity:.9;">
          <strong>plantasia.space</strong> is a platform designed for interactive music releases. It simplifies the creation and customization of Orbiters and Entangled Worlds, and allows artists to upload music that users can listen to and remix in real time. The platform encourages innovation through playful music interaction and healthy sensory exploration.
        </p>
        <a href="https://plantasia.space" class="button button--outline-primary button--rounded" style="font-size:.8rem;">Visit</a>
      </div>
      <div style="background:#141820;padding:1.25rem 1.15rem;border:1px solid #232a33;border-radius:16px;">
        <h3 style="margin:.1rem 0 .55rem;font-size:1.15rem;">Orbits & Bodies</h3>
        <p style="margin:0 0 .9rem;line-height:1.5;opacity:.9;">Orbits and Bodies explores the entanglement of embodied gesture, astronomical data, and networked computation  in real‑time audiovisual space.</p>
        <a href="/lab/en/orbits-and-bodies.html" class="button button--outline-primary button--rounded" style="font-size:.8rem;">Read</a>
      </div>
      <div style="background:#141820;padding:1.25rem 1.15rem;border:1px solid #232a33;border-radius:16px;">
        <h3 style="margin:.1rem 0 .55rem;font-size:1.15rem;">Interplanetary Players Orchestra</h3>
        <p style="margin:0 0 .9rem;line-height:1.5;opacity:.9;">Collaborative workshop instrument: card‑driven layering generating an emergent orbital score.</p>
        <a href="/lab/en/ip-orchestra" class="button button--outline-primary button--rounded" style="font-size:.8rem;">Open</a>
      </div>
          <div style="display:flex;gap:.75rem;flex-wrap:wrap;justify-content:center;margin-top:1.25rem;">
      <a href="/lab" class="button button--primary button--rounded" style="background:#ff00de;border:none;">Lab</a>
      <a href="/landings" class="button button--outline-error button--rounded">Live</a>
      <a href="/bookings" class="button button--outline-info button--rounded">Bookings</a>
    </div>
    </div>
  </div>
</section>

<!-- VIDEO SWIPER MOVED TO BOTTOM -->
<section style="padding:2.5rem 0 0;">
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

<div class="p-5"></div>

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

