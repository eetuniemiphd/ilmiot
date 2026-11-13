---
layout: case
case_key: helsingin_tietomurto
title: Helsingin tietomurto 2024
description: "Helsingin kaupungin vuoden 2024 tietomurron seuranta: tapahtumien aikajana, alkuperäislähteet, selvitykset, päätökset ja avoimet kysymykset."
lead: "Mitä Helsingin kaupungin tietomurrosta tiedettiin, kun se tuli julki? Mitä sen jälkeen on selvinnyt?"
permalink: /seuranta/helsingin-tietomurto-2024/
---

{% assign dossier = site.data.cases.helsingin_tietomurto %}
{% assign recent_changes = dossier.changes | sort: 'date' | reverse %}
{% assign latest_change = recent_changes | first %}
<section class="status-panel">
  <div><span class="micro-label">TILANNE</span><strong>{{ dossier.status | escape }}</strong><p>Päivitän seurantaa, kun asiasta saadaan uutta olennaista tietoa, jonka voi tarkistaa.</p></div>
  <div><span class="micro-label">UUSIN MUUTOS</span>
    {% if latest_change %}<strong>{{ latest_change.description | escape }}</strong><p>{{ latest_change.date | date: '%-d.%-m.%Y' }} · <a href="#paivityshistoria">Katso päivityshistoria</a></p>
    {% else %}<strong>Seuranta avattu</strong><p>1.11.2026 · Ensimmäinen lähteisiin perustuva yhteenveto on tekeillä.</p>{% endif %}
  </div>
</section>

## Mitä tässä seurannassa selvitän?

Aikajanalle kokoan tapahtumat ja sen, milloin niistä kerrottiin julkisuudessa. Päätöksistä ja selvityksistä etsin vastauksia siihen, miten vastuut oli järjestetty ennen tietomurtoa, mitä tietomurron syistä ja vaikutuksista on saatu selville ja mitä sen jälkeen on tehty.

## Mitä asiasta tiedetään?

Helsingin kaupungin kasvatuksen ja koulutuksen toimiala havaitsi tietomurron 30.4.2024. Ensimmäisessä tiedotteessaan 2.5. kaupunki kertoi oppijoiden ja henkilöstön käyttäjätunnuksista ja sähköpostiosoitteista. Yksitoista päivää myöhemmin se kertoi hyökkääjän saaneen myös henkilötunnuksia, osoitetietoja ja aineistoa toimialan verkkolevyiltä.

Riippumaton tutkintaryhmä arvioi, että hyökkääjä kopioi noin kaksi teratavua tietoa, johon sisältyi arviolta 750 000 asiakirjaa. Tarkkaa luetteloa kopioiduista tiedostoista ei saatu selville. Tutkinta nosti esiin epäselvät ylläpitovastuut, puutteet hälytysten seurannassa ja sen, että verkkolevylle oli kertynyt tietoja vuosien ajan.

[Lue analyysi: Hälytys syntyi, mutta tieto ei kulkenut]({{ '/artikkelit/helsingin-tietomurto-analyysi/' | relative_url }}).

[Aikajanalle]({{ '/seuranta/helsingin-tietomurto-2024/aikajana/' | relative_url }}) kokoan tapahtumat ja sen, milloin niistä kerrottiin julkisuudessa.

## Kysymykset, joihin etsin vastausta

1. Milloin tietomurto tapahtui, milloin se havaittiin ja milloin siitä kerrottiin julkisuudessa?
2. Miten järjestelmän ylläpito ja tietoturvasta huolehtiminen oli järjestetty?
3. Mitä tietomurron syistä ja vaikutuksista voidaan varmistaa julkisista lähteistä, ja mikä jää niiden perusteella auki?
4. Mitä tietomurron jälkeen päätettiin korjata, ja mitä korjausten toteutumisesta tiedetään?

## Päivityshistoria {#paivityshistoria}

{% include change-log.html data=site.data.cases.helsingin_tietomurto %}

<div class="callout-links"><a href="{{ '/seuranta/helsingin-tietomurto-2024/aikajana/' | relative_url }}"><strong>Aikajana</strong><span>Tapahtumat päivämäärineen ja lähteineen ↗</span></a><a href="{{ '/seuranta/helsingin-tietomurto-2024/lahteet/' | relative_url }}"><strong>Lähteet</strong><span>Asiakirjat ja muut seurannan lähteet ↗</span></a></div>