# Changelog

Een release = een versieverhoging in `package.json` + een regel hier (BES-036 punt 2).

## 1.1.0 — 2026-10-23

De merksites komen erbij: `finforward.be` en `planet-talent.com` worden in Astro
herbouwd en halen hun letters voortaan hier.

**Toegevoegd**
- `brand-font.planet-talent.{heading,body}` — Comfortaa / Open Sans, uit het
  Planet Talent-brandbook (2018), bevestigd tegen de live site.
- `brand-font.fin-forward.{heading,body}` — Poppins / Montserrat. Keuze van Koen
  op 2026-10-23: vervangt `proxima-nova` (Adobe Typekit), waarvan de licentie aan
  een kit én een domein hangt. Beide nieuwe letters zijn vrije Google-fonts.

**Niet gewijzigd**
- De kleuren van beide merken (`brand-own.*`) blijven zoals ze stonden: ze zijn op
  2026-10-23 gemeten tegen de live sites en kloppen (FF `#00674c`/`#fff36d`,
  PT `#242365`/`#c00f82`). Het brandbook noemt een ander geel (`#ebc522`) dan
  `partner.planet-talent` (`#f8cd41`); beslissing van Koen: **de bestaande
  website is leidend**, dus ongemoeid gelaten.

## 1.0.0 — 2026-10-06

Eerste versie. Het merk staat voor het eerst in git, tool-onafhankelijk.

**Toegevoegd**
- `tokens/` in DTCG-formaat: 151 tokens over vier bestanden (kleur, typografie,
  layout, semantisch). Drie lagen: basis → semantisch, met de betekenislaag
  bewust buiten deze repo.
- `brand/merk.md`, `brand/beeld-en-iconen.md`, `brand/afnemers.md` — de regels die
  een token niet kan uitdrukken, inclusief de gemeten contrastwaarden.
- `build/build.js` — Style Dictionary v4 met vijf uitgangen: `tokens.css`,
  `tokens.js`, `tokens.d.ts`, `tokens.json`, `office.json`.
- `scripts/drift-check.mjs` — vergelijkt elke hexwaarde in `orvia-be/orvia-website`
  met `tokens/`. Eerste run: 13 hexwaarden op de website, allemaal gedekt.
- `assets/`: 8 webfonts (264 KB), 5 logo's, 21 lijniconen.
- `LICENSE-FONTS.md` — wat mag en niet mag met Conso en PP Agrandir.

**Bron**: Orvia Design System-export uit Claude Design (2026-09-21), gebouwd uit
`orvia-be/orvia-website` (sync 2026-08-18), aangevuld met `orvia-max`.

**Bewust niet meegenomen**
- De tien merkfoto's (~18 MB). Die staan al in `orvia-website/public/images`,
  byte voor byte identiek. De *regel* over beeldtoon staat in `brand/`.
- De 17 componenten en 3 templates uit de bundel: een recreatie van de website,
  geen gedeelde bibliotheek.
- De tone of voice: hoort in `orvia-context` → `orvia-communicatie`.
