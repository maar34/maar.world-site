---
layout: landing
title: Orbiters 
cover: /img/docs/covers/int-players-cover.jpeg
excerpt: >
      Imagine turning your browser into a turntable from outer space. 
permalink: /orbiters
full_width: false
show_date: false
public: true
header:
  theme: dark
article_header:
  height: 30vh
  theme: ocean
  background_color: '#203028' 
  background_image:
    src: /img/interplanetary-players/433-decks.gif
---

  <div class="p-4"></div>
  <div class="grid">
    <div class="cell cell--12">

<div class="hero hero--center" style="background-color: #000000;">
  <div class="hero__content">
  <p>Orbiters — previously called Interplanetary Players</p>  
</div>
</div>

<div class="hero hero--center" style="background-color: #000000;">
  <div class="hero__content">
    <h3>Start your journey</h3>
  </div>
</div>

<!-- Swiper init (updated) -->
<script>
  {%- include scripts/lib/swiper.js -%}
  (function(){
    var SOURCES=(window.TEXT_VARIABLES&&window.TEXT_VARIABLES.sources)||{};
    function init(sel){ if(window.jQuery && jQuery(sel).swiper){ jQuery(sel).swiper({animation:true}); } }
    function start(){ init('.swiper-demo--orbiters'); }
    if(window.Lazyload && SOURCES.jquery){ window.Lazyload.js(SOURCES.jquery,start); } else { document.addEventListener('DOMContentLoaded',start);} 
  })();
</script>

<!-- Primary Swiper (separated layout) -->
<div class="swiper my-3 swiper-demo swiper-demo--image swiper-demo--orbiters swiper--tall swiper--separated">
  <div class="swiper__wrapper">
    <!-- Slide 1 -->
    <div class="swiper__slide orb-slide">
      <h3 class="orb-step">I</h3>
      <div class="orb-media"><img class="lightbox-ignore" src="/img/interplanetary-players/07_ip-card.jpg" alt="Layering cards"/></div>
      <div class="orb-desc">Explore music like never before: layer sounds with controls that change based on the cards you play, creating rich and original sound experiences.</div>
    </div>
    <!-- Slide 2 -->
    <div class="swiper__slide orb-slide">
      <h3 class="orb-step">II</h3>
      <div class="orb-media"><img class="lightbox-ignore" src="/img/interplanetary-players/10_ip-transit.png" alt="Transit mapping"/></div>
      <div class="orb-desc">Intuitively remix music—sound creation becomes playful and accessible for everyone, with or without prior experience.</div>
    </div>
    <!-- Slide 3 -->
    <div class="swiper__slide orb-slide">
      <h3 class="orb-step">III</h3>
      <div class="orb-media"><img class="lightbox-ignore" src="/img/interplanetary-players/08_ip-max-24.jpg" alt="Workshop patch"/></div>
      <div class="orb-desc">We are at the beginning of this journey—<a href="https://maar.world/subscribe" target="_blank">stay connected</a> to follow the evolution of Orbiters Orchestra.</div>
    </div>
  </div>
  <div class="swiper__button swiper__button--prev fas fa-chevron-left"></div>
  <div class="swiper__button swiper__button--next fas fa-chevron-right"></div>
</div>
</div>
</div>

<style>
/* Orbiter swiper separated layout styles (mirrors workshop pages) */
.swiper--tall { max-height:none; }
@media (min-width:920px){ .swiper--tall { max-height:820px; } }
.swiper--tall .swiper__slide img { height:100%; object-fit:cover; }
.swiper--separated .slide-caption { display:none !important; }
.orb-slide { display:flex; flex-direction:column; align-items:center; gap:1.1rem; padding:1rem 1rem 1.6rem; }
.orb-step { font-size:1.25rem; font-weight:600; letter-spacing:.18em; background:rgba(0,0,0,.35); padding:.45rem .85rem .5rem; border-radius:8px; backdrop-filter:blur(4px); box-shadow:0 0 0 1px rgba(0,0,0,.4),0 2px 6px -2px rgba(0,0,0,.6); margin:0; }
.orb-media { width:100%; max-width:880px; }
.orb-media img { width:100%; height:auto; display:block; border-radius:8px; }
.orb-desc { max-width:880px; font-size:.95rem; line-height:1.5; opacity:.92; text-align:center; margin:0 auto; }
@media (min-width:900px){ .orb-step { font-size:1.35rem; } }
@media (max-width:860px){ .orb-step { font-size:1.3rem; } .orb-desc { font-size:.87rem; } .orb-slide { gap:.9rem; padding:.85rem .85rem 1.3rem; } }
@media (max-width:480px){ .orb-step { font-size:1.1rem; padding:.4rem .75rem .45rem; } .orb-desc { font-size:.8rem; } }
</style>

<div class="p-5"></div>

<!-- Existing sections preserved below -->
<section class="grid">
  <article class="cell cell--12">
    <div class="hero hero--center hero--dark" style='background-color: #000000;'>
      <div class="hero__content">
        <h3>Control the Sound:</h3>
        <div class="container">
          <iframe src="https://play.maar.world/?g=335&s=1&c=0" class="responsive-iframe" title="Control the Sound Interactive" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
        </div>
        <p>Please unmute your device and press the PLAY ▶️ button. Adjust the sound by moving the XYZ KNOBS up or down until you like what you hear. If you want to go back to the original sound, press the hexagonal ⬢ buttons to reset the knobs to their equilibrium.</p>
      </div>
    </div>
    <div class="hero hero--center hero--dark" style='background-color: #000000;'>
      <div class="hero__content">
        <h3>Explore Regenerative Modes:</h3>
        <div class="container">
          <iframe src="https://play.maar.world/?g=8&s=0&c=21" class="responsive-iframe" title="Explore Regenerative Modes Interactive" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
        </div>
        <p>Experiment with 7 unique modes, creating with real data from exoplanets and their transits and orbits across different time scales. Leave the button pressed to get hints about these parameters.</p>
      </div>
    </div>
  </article>
</section>

<div class="p-5"></div>

<div class="grid">
  <div class="cell cell--12">
    <!-- Section 1: Innovative Tradition -->
    <div class="hero hero--center hero--dark" style='background-color: #000;'>
      <div class="hero__content">
        <h3>Innovative Tradition</h3>
        <img src="/img/interplanetary-players/maar-world-banner-ovni.jpg" alt="Innovative Tradition" style="max-width: 100%; height: auto; margin-top: 20px;">
        <p>Discover the different cards effects as if you're adjusting a spaceship's experience.</p>
      </div>
    </div>
    <!-- Section 2: An Extended Harmony of the Spheres -->
    <div class="hero hero--center hero--dark" style='background-color: #000;'>
      <div class="hero__content">
        <h3>An Extended Harmony of the Spheres</h3>
        <img src="/img/interplanetary-players/Planetary_Musical_Scales_from_Harmony_of_the_Worlds.jpg" alt="Harmony of the Spheres" style="max-width: 100%; height: auto; margin-top: 20px;">
        <p>Sync your remix with the movement of the Kepler-47 star system. It's like mixing soundscapes with a touch of stardust, opening a new spectrum of possibilities for jamming with the cosmos.</p>
        <img src="/img/interplanetary-players/Kepler_Space_Telescope.png" alt="Kepler telescope" style="max-width: 100%; height: auto; margin-top: 20px;">
      </div>
    </div>
  </div>
</div>


