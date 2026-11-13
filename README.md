# Eetu Niemi — Ilmiöt

Julkisiin lähteisiin perustuvia artikkeleita ja pysyviä seurantoja monimutkaisista ilmiöistä.

**Sivusto:** https://ilmiot.eetuniemi.fi

**Monimutkaiset asiat ymmärrettäviksi.**

Ilmiöt on Eetu Niemen riippumaton analyysi- ja seurantajulkaisu.

Julkaisu kokoaa hajallaan olevaa julkista tietoa ymmärrettäviksi kokonaisuuksiksi sekä tarkastelee teknologian, päätöksenteon, talouden ja yhteiskunnallisten järjestelmien toimintaa ja vaikutuksia.

**Verkkosivusto:** [ilmiot.eetuniemi.fi](https://ilmiot.eetuniemi.fi)

## Sisältö

Julkaisussa on kolme keskeistä sisältömuotoa:

- **Artikkelit:** analyysejä, taustoituksia ja kokemuksiin perustuvia kirjoituksia.
- **Seurannat:** pitkäkestoisten tapausten dokumentointia, aikajanoja, päätöksiä ja lähdekoosteita.
- **Selittävät kaaviot:** visuaalisia esityksiä järjestelmistä, riippuvuuksista, päätöksenteosta ja tapahtumaketjuista.

Tavoitteena ei ole mahdollisimman nopea uutisointi, vaan huolellisesti lähteistetty kokonaiskuva.

## Toimitukselliset periaatteet

Julkaisun keskeiset periaatteet:

1. Ensisijaisesti alkuperäiset ja julkisesti tarkistettavat lähteet.
2. Dokumentoitujen tosiasioiden, eri toimijoiden väitteiden, analyysin ja avoimien kysymysten erottaminen.
3. Järjestelmien ja päätöksenteon tarkastelu henkilökohtaisen syyllistämisen sijaan.
4. Tietojen tarkistaminen ennen julkaisua.
5. Virheiden avoin korjaaminen ja olennaisten muutosten dokumentointi.
6. Henkilötietojen tarpeellisuuden ja yksityisyydensuojan huomioiminen.
7. Mahdollisten henkilökohtaisten ja ammatillisten sidonnaisuuksien ilmoittaminen.

Tekoälyä voidaan käyttää aineiston jäsentämiseen ja tekstin työstämiseen, mutta se ei ole julkaistavien tietojen lähde.

Tarkemmat periaatteet julkaistaan sivustolla: [Toimitukselliset periaatteet](https://ilmiot.eetuniemi.fi/periaatteet/).

## Tekninen toteutus

Sivusto toteutetaan seuraavilla teknologioilla:

- GitHub Pages – julkaisu ja hosting
- Jekyll – staattisen sivuston muodostaminen
- Markdown – artikkelit ja sisältösivut
- YAML – seurantojen tapahtumat ja lähderekisterit
- HTML ja CSS – ulkoasu sekä kaavioiden esittäminen

- Etusivu näyttää automaattisesti uusimman artikkelin ja seuraavat kuusi.
- `/artikkelit/` listaa julkaistut artikkelit uusimmasta alkaen.
- Artikkelit kirjoitetaan `_posts/YYYY-MM-DD-slug.md` -tiedostoiksi.
- Seurannat, lähdeluettelot ja YAML-pohjainen aikajana säilyvät entisellään.
- RSS-syöte: `/feed.xml` ja sivukartta: `/sitemap.xml` rakennetaan automaattisesti.
- Ei CMS:ää, tietokantaa tai JavaScript-riippuvuutta.

Paikallisesti:

```sh
bundle install
bundle exec jekyll serve
```

Sivusto ei käytä julkaisijan lisäämää kävijäanalytiikkaa, mainosseurantaa tai seurantapikseleitä.

## Tekijänoikeudet ja käyttöehdot

© 2026 Eetu Niemi.

Julkaisun alkuperäisten artikkelien, tekstien, kuvien ja kaavioiden oikeudet pidätetään, ellei yksittäisen aineiston yhteydessä ilmoiteta muuta.

Lähdeasiakirjojen, lainatun aineiston ja kolmansien osapuolten materiaalien oikeudet kuuluvat niiden oikeudenhaltijoille.

Julkinen GitHub-repositorio ei tarkoita, että sen journalistinen sisältö olisi vapaasti uudelleenjulkaistavissa. Tekijänoikeuslain sallimat käytöt, kuten asianmukainen siteeraaminen, ovat erikseen mahdollisia.

## Julkaisija

**Eetu Niemi**

[Henkilökohtainen verkkosivusto](https://eetuniemi.fi)

Ilmiöt julkaistaan henkilökohtaisena ja riippumattomana sisältöalueena.
