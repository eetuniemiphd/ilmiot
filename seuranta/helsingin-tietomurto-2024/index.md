---
layout: case
case_key: helsingin_tietomurto
title: Helsingin tietomurto 2024
description: "Helsingin vuoden 2024 tietomurron tapahtumien, päätösten, tutkintojen ja avoimien kysymysten seuranta."
lead: "Yksi paikka tapauksen tapahtumaketjulle, alkuperäislähteille ja avoimille kysymyksille."
permalink: /seuranta/helsingin-tietomurto-2024/
---

{% assign dossier = site.data.cases.helsingin_tietomurto %}
{% assign recent_changes = dossier.changes | sort: 'date' | reverse %}
{% assign latest_change = recent_changes | first %}
<section class="status-panel">
  <div><span class="micro-label">TILANNE</span><strong>{{ dossier.status | escape }}</strong><p>Seurannan vaihe näkyy tässä automaattisesti YAML-tiedostosta.</p></div>
  <div><span class="micro-label">UUSIN MUUTOS</span>
    {% if latest_change %}<strong>{{ latest_change.description | escape }}</strong><p>{{ latest_change.date | date: '%-d.%-m.%Y' }} · <a href="#paivityshistoria">Katso päivityshistoria</a></p>
    {% else %}<strong>Rakenteen perustaminen</strong><p>1.11.2026 · Aloitussivut avattu ilman tarkistamattomia faktaväitteitä.</p>{% endif %}
  </div>
</section>

## Mikä on tämän seurannan tarkoitus?

Tähän kokonaisuuteen kootaan vuoden 2024 Helsingin tietomurtoon liittyvät keskeiset tapahtumat, viranomaisasiakirjat, päätökset ja selvitykset sekä niitä koskevat avoimet kysymykset. Tavoitteena on tehdä pitkästä tapahtumaketjusta helposti seurattava ja lähteiden avulla tarkistettava.

## Mitä seurannassa tarkastellaan?

- **Tapahtumaketju:** mitä tapahtui ja milloin tieto tuli julkiseksi.
- **Päätökset ja vastuut:** mitä toimijat ovat kertoneet, päättäneet tai selvittäneet.
- **Korjaustoimet:** mitä toimenpiteitä on dokumentoitu ja mitä niiden toteutuksesta tiedetään.
- **Avoimet kysymykset:** mistä ei ole vielä julkaistu riittävää tietoa.

Nämä ovat **tutkimuksen teemoja**, eivät väitteitä siitä, että tiettyä tapahtumaa tai toimenpidettä olisi jo todennettu.

## Dokumentoidut havainnot

Tähän lisätään ensimmäinen tarkistettu yhteenveto, kun alkuperäislähteet on käyty läpi. Keskeisissä väitteissä viitataan yksilöityihin lähteisiin.

## Avoimet kysymykset

Tällä hetkellä seurannan tutkimuskysymyksiä ovat esimerkiksi:

1. Millainen tapahtumaketju käy ilmi julkisista asiakirjoista?
2. Mitä tapahtuman syistä, vaikutuksista ja korjaustoimista on dokumentoitu?
3. Mitkä päätökset tai selvitykset muuttavat aiempaa tilannekuvaa?
4. Mitä tietoja julkisista lähteistä ei löydy tai ei voida varmistaa?

## Päivityshistoria {#paivityshistoria}

{% include change-log.html data=site.data.cases.helsingin_tietomurto %}

<div class="callout-links"><a href="{{ '/seuranta/helsingin-tietomurto-2024/aikajana/' | relative_url }}"><strong>Aikajana</strong><span>Tapahtumat päivämäärineen ja lähteineen ↗</span></a><a href="{{ '/seuranta/helsingin-tietomurto-2024/lahteet/' | relative_url }}"><strong>Lähteet</strong><span>Yksilöity asiakirja- ja viiterekisteri ↗</span></a></div>
