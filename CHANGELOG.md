# Changelog

Een release = een versieverhoging in `package.json` + een regel hier (BES-036 punt 2).

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
