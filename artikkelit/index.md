---
title: Artikkelit
description: "Eetu Niemen analyysejä, taustoituksia ja omiin kokemuksiin perustuvia kirjoituksia yhteiskunnasta, teknologiasta ja taloudesta."
permalink: /artikkelit/
eyebrow: Julkaisut
lead: "Kirjoitan siitä, miten järjestelmät toimivat, miksi tiettyihin ratkaisuihin päädytään ja mitä niistä seuraa."
---

Mitä kaupungin päätöksestä seurasi käytännössä? Mitä piensijoittaja saa tietää yhtiöstä, jonka osakkeilla ei käydä kauppaa pörssissä? Tällaisista kysymyksistä jutut usein lähtevät liikkeelle. Jos aiheesta on myös seuranta, jutun yhteydessä on linkki sinne. Seurannasta näet, mitä tapahtui aiemmin ja mitä asiasta on sittemmin saatu selville.

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
<div class="empty-state"><strong>Ensimmäiset artikkelit ovat tekeillä.</strong><p>Uudet kirjoitukset näkyvät myös etusivulla.</p></div>
{% endif %}