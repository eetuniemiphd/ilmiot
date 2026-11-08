---
title: Artikkelit
permalink: /artikkelit/
eyebrow: Julkaisut
lead: "Analyysejä, taustoituksia ja kokemuksiin perustuvia kirjoituksia monimutkaisista ilmiöistä."
---
Artikkeleissa voidaan käsitellä seurattavia tapauksia tai itsenäisiä aiheita. Kirjoitusten tyyppi käy ilmi otsikon yhteydessä. Julkaisut perustuvat tarkistettuihin lähteisiin ja erottavat dokumentoidun tiedon kirjoittajan tulkinnasta.

{% assign articles = site.posts %}
{% if articles.size > 0 %}
<div class="listing">
{% for post in articles %}
<article class="list-card">
  {% if post.image %}
  <a class="list-card-media" href="{{ post.url | relative_url }}" aria-label="Lue artikkeli: {{ post.title | escape }}">
    <img src="{{ post.image | relative_url }}" alt="" width="1200" height="630" loading="lazy" decoding="async">
  </a>
  {% endif %}
  <div class="post-meta"><span class="pill">{{ post.content_type | default: 'Artikkeli' | escape }}</span><time datetime="{{ post.date | date: '%Y-%m-%d' }}">{{ post.date | date: '%-d.%-m.%Y' }}</time></div>
  <h2><a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></h2>
  {% if post.description %}<p>{{ post.description | escape }}</p>{% endif %}
  {% if post.related_case %}<p class="post-related">Liittyy seurantaan: <a href="{{ post.related_case | relative_url }}">{{ post.related_case_title | default: 'Tutustu seurantaan' | escape }}</a></p>{% endif %}
</article>
{% endfor %}
</div>
{% else %}
<div class="empty-state"><strong>Artikkelit julkaistaan tänne.</strong><p>Julkaistut artikkelit ilmestyvät automaattisesti myös etusivulle.</p></div>
{% endif %}
