# Orvia design tokens

Publieke, fontloze uitgang van **orvia-be/orvia-design-system** (privé).
Versie 1.0.0 — zie [CHANGELOG.md](CHANGELOG.md).

Overzicht: https://orvia-be.github.io/orvia-design-tokens/

| Bestand | Voor |
|---|---|
| `dist/tokens.css` | CSS custom properties |
| `dist/tokens.js` + `.d.ts` | JS/TS |
| `dist/tokens.json` | scripts, agents, documentgeneratie |
| `dist/office.json` | Word/PowerPoint-thema's (uitgerekende hex) |
| `logo/`, `icons/` | SVG-merkassets |

**Geen fontbestanden.** Conso en PP Agrandir zijn commercieel gelicentieerd.
Gebruik `--font-substitute-brand` (Archivo) en Inter voor cijfers.

Niet met de hand bewerken: deze repo wordt overschreven door `npm run publiceer`
in de bronrepo.
