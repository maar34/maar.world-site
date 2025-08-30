---
layout: article
show_title: false
permalink: /bookings
titles:
  # @start locale config
  en      : &EN       DJ set + Live set = Hybrid set 
  en-GB   : *EN
  en-US   : *EN
  en-CA   : *EN
  en-AU   : *EN

  # @end locale config
key: live-set-information
---

# <span class="material-symbols-outlined" style="font-size:48px;vertical-align:middle;">speaker_group</span> Bookings

𝐵𝓇𝓊𝓃𝒶 𝒢𝓊𝒶𝓇𝓃𝒾𝑒𝓇𝒾

<a href="/img/pdf/English-EPK_Bruna_Guarnieri.pdf" rel="EPK" target="_blank">Download EPK (PDF)</a>

<!-- Correct PDF embed (removed stray space in filename, added fallback + responsive wrapper) -->
<div class="pdf-embed pdf-preview">
  <object
    data="/img/pdf/English-EPK_Bruna_Guarnieri.pdf#toolbar=0"
    type="application/pdf"
    aria-label="Electronic Press Kit PDF"
    width="100%"
    height="1500px">
      <iframe
        src="/img/pdf/English-EPK_Bruna_Guarnieri.pdf"
        title="EPK PDF"
        style="width:100%;height:1400px;border:none;">
      </iframe>
      <p>Your browser cannot display embedded PDFs.
        <a href="/img/pdf/English-EPK_Bruna_Guarnieri.pdf">Download the EPK</a>.
      </p>
  </object>
  <div class="pdf-fallback" aria-hidden="true" style="display:none;">
    <a class="button button--outline-info button--rounded" style="font-size:.75rem;" target="_blank" rel="noopener" href="/img/pdf/English-EPK_Bruna_Guarnieri.pdf">Open / Download EPK (PDF)</a>
  </div>
</div>

**Performance:** Live AV, Live, Hybrid, DJ set.  
**Genres:** Regenerative Music / Union of world genres / You choose the genre, I choose the style :)  
**Artist using:** Sensors, controllers, synths, custom Max software, Ableton Live, Traktor.  
Live AV includes custom Max Software and Synths. 

<h3>Hybrid (Live + DJ) sets</h3>

From thirty minutes to four hours: sonic or audiovisual journeys through classical elements, expeditions to solar systems, exoplanets, and stars.

Each concept appears under musical moods ranging from ambient and downtempo to house and techno, always adapting to the moment. Soundscapes and voices bring narrative strands. Over a decade assembling an archive of soundscapes, poetry, testimonies, native South American chants, radio signals, and eclectic music to connect people and cultures through sound.

<div class="form-container" style="margin-top:72px;">
  <h3>Contact</h3>
  <p>Send a booking inquiry.</p>
  <form
    action="https://formspree.io/f/mqkrdkde"
    method="POST"
    class="contact-form">
    <label>
      Your name:
      <input type="text" name="name" required>
    </label>
    <label>
      Your email:
      <input type="email" name="email" required>
    </label>
    <label>
      Your message:
      <textarea name="message" rows="6" required></textarea>
    </label>
    <button type="submit">Send</button>
  </form>
</div>

<div class="p-5"></div>

<style>
  .pdf-embed object,
  .pdf-embed iframe {
    box-shadow: 0 0 0 1px #222, 0 6px 28px -8px rgba(0,0,0,.6);
    border-radius: 8px;
    background:#111;
  }
  @media (max-width: 820px){
    .pdf-embed object,
    .pdf-embed iframe { height: 1100px !important; }
  }
  @media (max-width:640px){
    .pdf-embed object { display:none; }
    .pdf-embed .pdf-fallback { display:block !important; text-align:center; margin:1rem 0 0; }
    a[rel="EPK"] { display:none !important; } /* hide duplicate link on mobile */
  }
  .contact-form label {
    display:block;
    font-size:.85rem;
    letter-spacing:.05em;
    margin:0 0 .75rem;
  }
</style>