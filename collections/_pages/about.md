---
layout: articles
permalink: /about
show_title: false
show_date: false
titles:
  # @start locale config
  en      : &EN       About
  en-GB   : *EN
  en-US   : *EN
  en-CA   : *EN
  en-AU   : *EN

key: page-about
---

<header class="page-header">
  <h1><span class="material-symbols-outlined" aria-hidden="true" style="font-size:48px;vertical-align:middle;">looks</span> About</h1>
</header>

<div class="bio-wrapper">
  <div class="bio-grid">
    <div class="bio-image">
      <img src="/img/about/bruna-profile.webp" alt="Bruna Guarnieri portrait"/>
    </div>
    <div class="bio-content">
      <h4>Connecting artists and listeners with novel tools for future music co‑creation.</h4>

      <p>Maar World is a record label for a new era of music listening and making. Currently developing new formats for music distribution of independent artists, merging physical and digital releases, music making and listening.</p>

      <h4>Founder</h4>

      <p>My name is 𝐵𝓇𝓊𝓃𝒶 𝑀𝒶𝒶𝓇 𝒢𝓊𝒶𝓇𝓃𝒾𝑒𝓇𝒾 𝒞𝑜𝓁𝒶𝓈𝓈𝑜. I am a sound artist and engineer working at the intersection of art, science and technology. After studying Sound Design and Engineering in Montevideo and Santiago de Chile, I collaborated on sound and interaction design for large-scale installations across the Americas and Europe. Highlights include the 2021 AI & Music S+T+ARTS Festival Hackathon award, sound design for national pavilions at major expos and the lead development of artist-run initiatives such as <a href="http://headbrothers.com" target="_blank" rel="noopener">Head Brothers</a> and <a href="http://headbrothers.com/exoplanetas" target="_blank" rel="noopener">Exoplanetas</a>. Over a decade I have assembled an archive of soundscapes, poetry, testimonies, native South American chants, radio signals and eclectic music to create experiences that connect people and cultures through sound.</p>

    </div>
  </div>
</div>

<style>
/* Page header */
.page-header { max-width: calc(var(--site-content-max, 1000px)); margin: 1.25rem auto 0; padding: 0 1.35rem; }
.page-header h1 { font-size:1.6rem; margin:0 0 .6rem; display:flex; align-items:center; gap:.6rem; }

/* Scoped bio layout */
.bio-wrapper { max-width: calc(var(--site-content-max, 1000px)); margin: 0.75rem auto 1.25rem; padding: 1.35rem; border-radius: 14px; background: linear-gradient(180deg, rgba(255,255,255,0.01), rgba(255,255,255,0.005)); box-shadow: 0 6px 30px -12px rgba(0,0,0,.6); }
.bio-grid { display:flex; gap:1.5rem; align-items:flex-start; }
.bio-image { flex:0 0 320px; max-width:320px; }
/* oval portrait */
.bio-image img{ width:100%; height:auto; display:block; border-radius: 50% / 45%; border:8px solid #f5f5f5; box-shadow: inset 0 0 12px rgba(255,255,255,0.5), 0 10px 30px -12px rgba(0,0,0,.6); background: radial-gradient(circle at 30% 30%, #fff,#ddd,#aaa); }
.bio-content h4{ margin:.1rem 0 .9rem; font-weight:600; color: #e9e9e9; }
.bio-content p{ margin:0 0 .9rem; line-height:1.6; color: #dcdcdc; font-size:1rem; }

/* tag inline links inside bio keep contrast */
.bio-content a{ color: #ff00de; text-decoration:underline; }

@media (max-width:960px){ .bio-grid{ gap:1rem; } .bio-image{ flex:0 0 240px; max-width:240px; } }
@media (max-width:680px){ .page-header { padding:0 .85rem; } .bio-grid{ flex-direction:column; align-items:center; text-align:left; } .bio-image{ max-width:200px; margin:0 auto; } .bio-wrapper{ padding:1rem; } .page-header h1{ font-size:1.35rem; } }
</style>
