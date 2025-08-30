---
layout: article   # use a simple layout if archive layout is broken
title: Lab
permalink: /lab
show_title: false
---

# <span class="material-symbols-outlined" style="font-size:48px;vertical-align:middle;">science</span> Lab

<div class="hero hero--dark" style='height:200px; background-image:url("/img/lab/genesis-lab.jpg");'>
  <div class="hero__content"></div>
</div>

#### Step into a time lab.

A public bitacora to share new and old creations...
Keep track of how ideas change over time and relate, kind of like watching a plant grow from a tiny seed to a big, beautiful tree.

Filter posts in:
<a class="button button--outline-error button--rounded" href="/lab?tag=EN">English</a>
<a class="button button--outline-error button--rounded" href="/lab?tag=ES">Spanish</a>

<hr>

{% include article-list.html
   articles=site.lab
   group_by='year'
   show_date=true
   show_excerpt=true
   show_cover=false
   excerpt_truncate=200 %}

<script>
(function(){
  const params = new URLSearchParams(window.location.search);
  const tag = params.get('tag');
  if(!tag) return;
  document.querySelectorAll('.archive-item').forEach(li=>{
    const tags = (li.getAttribute('data-tags')||'').split(' ');
    if(!tags.includes(tag)) li.style.display='none';
  });
})();
</script>



