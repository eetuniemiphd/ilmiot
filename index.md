---
title: Etusivu
description: "Eetu Niemi — Ilmiöt. Artikkeleita, analyysejä ja julkisiin lähteisiin perustuvaa seurantaa monimutkaisista ilmiöistä."
permalink: /
layout: default
---
<section class="editorial-intro" aria-labelledby="intro-heading">
  <p class="eyebrow">EETU NIEMI · ILMIÖT</p>
  <h1 id="intro-heading">Seurantaa ja <em>analyysiä.</em></h1>
  <p class="lead">Julkisiin lähteisiin perustuvia artikkeleita ja pitkäkestoista seurantaa monimutkaisista ilmiöistä, järjestelmistä ja päätöksistä.</p>
</section>

{% assign articles = site.posts %}
{% if articles.size > 0 %}
  {% assign newest = articles.first %}
  <section class="latest-article" aria-labelledby="latest-heading">
    <div class="section-heading"><div><p class="eyebrow">UUSIN JULKAISU</p><h2 id="latest-heading" class="visually-hidden">Uusin artikkeli</h2></div></div>
    <article class="headline-article{% if newest.image %} has-image{% endif %}">
      {% if newest.image %}
      <a class="headline-media" href="{{ newest.url | relative_url }}" aria-label="Lue artikkeli: {{ newest.title | escape }}">
        <img src="{{ newest.image | relative_url }}" alt="" width="1200" height="630" decoding="async">
      </a>
      {% endif %}
      <div class="headline-copy">
        <div class="post-meta"><span class="pill">{{ newest.content_type | default: 'Artikkeli' | escape }}</span><time datetime="{{ newest.date | date: '%Y-%m-%d' }}">{{ newest.date | date: '%-d.%-m.%Y' }}</time></div>
        <h2><a href="{{ newest.url | relative_url }}">{{ newest.title | escape }}</a></h2>
        {% if newest.description %}<p>{{ newest.description | escape }}</p>{% endif %}
        <a class="text-link" href="{{ newest.url | relative_url }}">Lue artikkeli <span aria-hidden="true">↗</span></a>
      </div>
    </article>
  </section>

  {% assign next_articles = articles | slice: 1, 6 %}
  {% if next_articles.size > 0 %}
  <section class="home-section" aria-labelledby="recent-heading">
    <div class="section-heading"><div><p class="eyebrow">ARTIKKELIT</p><h2 id="recent-heading">Viimeisimmät kirjoitukset</h2></div><a href="{{ '/artikkelit/' | relative_url }}">Kaikki artikkelit <span aria-hidden="true">↗</span></a></div>
    <div class="post-grid">
      {% for post in next_articles %}
      <article class="post-card">
        {% if post.image %}
        <a class="post-card-media" href="{{ post.url | relative_url }}" aria-label="Lue artikkeli: {{ post.title | escape }}">
          <img src="{{ post.image | relative_url }}" alt="" width="1200" height="630" loading="lazy" decoding="async">
        </a>
        {% endif %}
        <div class="post-meta"><span>{{ post.content_type | default: 'Artikkeli' | escape }}</span><time datetime="{{ post.date | date: '%Y-%m-%d' }}">{{ post.date | date: '%-d.%-m.%Y' }}</time></div>
        <h3><a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></h3>
        {% if post.description %}<p>{{ post.description | escape }}</p>{% endif %}
      </article>
      {% endfor %}
    </div>
  </section>
  {% endif %}
{% else %}
  <section class="home-section" aria-labelledby="recent-heading">
    <div class="section-heading"><div><p class="eyebrow">ARTIKKELIT</p><h2 id="recent-heading">Viimeisimmät kirjoitukset</h2></div></div>
    <p class="section-intro">Ensimmäiset artikkelit julkaistaan niiden valmistuttua. Uudet kirjoitukset tulevat tälle etusivulle automaattisesti.</p>
  </section>
{% endif %}
<section class="home-section follow-section" aria-labelledby="seurannat-heading">
  <div class="section-heading"><div><p class="eyebrow">JATKUVA SEURANTA</p><h2 id="seurannat-heading">Seurannat</h2></div><a href="{{ '/seuranta/' | relative_url }}">Kaikki seurannat <span aria-hidden="true">↗</span></a></div>
  <a class="feature-card" href="{{ '/seuranta/helsingin-tietomurto-2024/' | relative_url }}">
    <div><span class="pill">Valmistelussa</span><h3>Helsingin tietomurto 2024</h3><p>Tapahtumien, selvitysten, päätösten ja avoimien kysymysten dokumentoitu seurantarunko. Lähteisiin perustuva sisältö täydentyy tutkimustyön jälkeen.</p></div>
    <span class="feature-arrow" aria-hidden="true">↗</span>
  </a>
</section>
<section class="method-banner"><div><p class="eyebrow">JULKAISUPERIAATE</p><h2>Dokumentoi ensin. Tulkitse vasta sitten.</h2></div><p>Lähteet, väitteet, oma analyysi ja avoimet kysymykset erotetaan toisistaan. <a href="{{ '/periaatteet/' | relative_url }}">Lue toimitukselliset periaatteet ↗</a></p></section>
