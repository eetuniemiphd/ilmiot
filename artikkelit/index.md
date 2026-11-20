---
title: Artikkelit
description: "Eetu Niemen analyysejä ja taustoituksia teknologiasta, taloudesta, työelämästä ja yhteiskunnallisesta päätöksenteosta."
permalink: /artikkelit/
eyebrow: Julkaisut
lead: "Kirjoitan siitä, miten järjestelmät toimivat, miksi tiettyihin ratkaisuihin päädytään ja mitä niistä seuraa."
---

Miksi kaupungin digihankkeissa törmätään vuodesta toiseen samoihin ongelmiin? Mitä piensijoittaja voi saada selville listaamattomasta yhtiöstä? Miten organisaatiouudistus näkyy työn arjessa? Entä mistä tietää, eteneekö julkistettu investointi tiedotetta pidemmälle?

Etsin vastauksia pääosin julkisista lähteistä. Oma kokemus auttaa joskus huomaamaan, mitä kannattaa kysyä. Jos aiheesta on myös oma seuranta, linkitän siihen artikkelista. Seurannasta näet, mitä tapahtui, mitä sen jälkeen on selvinnyt ja mikä on vielä auki.

{% assign articles = site.posts %}
{% if articles.size > 0 %}
<div class="listing">
{% for post in articles %}
<article class="list-card">
  {% if post.cover_image %}
  <a class="list-card-media" href="{{ post.url | relative_url }}" aria-label="Lue artikkeli: {{ post.title | escape }}">
    <img src="{{ post.cover_image | relative_url }}" alt="" width="1200" height="630" loading="lazy" decoding="async">
  </a>
  {% endif %}
  <div class="post-meta">
    <span class="pill">{{ post.content_type | default: 'Artikkeli' | escape }}</span>
    <time datetime="{{ post.date | date: '%Y-%m-%d' }}">{{ post.date | date: '%-d.%-m.%Y' }}</time>
  </div>
  <h2><a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></h2>
  {% if post.description %}<p>{{ post.description | escape }}</p>{% endif %}
  {% if post.related_case %}
  <p class="post-related">Liittyy seurantaan: <a href="{{ post.related_case | relative_url }}">{{ post.related_case_title | default: 'Tutustu seurantaan' | escape }}</a></p>
  {% endif %}
</article>
{% endfor %}
</div>
{% else %}
<div class="empty-state">
  <strong>Ensimmäiset artikkelit ovat tekeillä.</strong>
  <p>Uudet kirjoitukset näkyvät myös etusivulla.</p>
</div>
{% endif %}