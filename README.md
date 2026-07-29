# 🎨 Pictos & Luminas — Expedition 33 Checklist

A comprehensive single-page checklist and reference for every **Picto** in *Clair Obscur: Expedition 33*. Track what you've found, search by name/effect/location, filter by stat or DLC — all in a game-styled UI.

**Live site:** <https://vze3f372.github.io/e33_picotracker/>

---

## What's Inside

- **210 Pictos** — all 193 base-game + 17 from the Verso's Drafts (Thank You Update) DLC
- **Checklist** — click any card to mark it collected; state saves to your browser
- **Search** — filters by name, effect text, or location
- **Filters** — All / Collected / Missing / HP / SPD / DEF / CRT / DLC
- **Progress bar** — shows completion at a glance
- **System explainer** — how Pictos, Luminas, and Lumina Points work
- **Stat & cost tables** — quick reference for builds

---

## Visual Style

The site draws from the game's **Belle Époque** meets **chiaroscuro** aesthetic:
- Dark, oil-painted backgrounds
- Gold accents and ornamental dividers
- **Cinzel** for headings, **IM Fell Double Pica** for body text
- **EB Garamond** for descriptions and flavour text
- **Bebas Neue** for numbers, **Abril Fatface** for display stats
- Subtle glow gradients and frameless cards

---

## How to Maintain

All data lives in a single `PICTO_DATA` array at the top of `index.html`:

```js
{name:"Picto Name", stats:["Health","Speed"], effect:"Effect description.",
 cost:5, location:"Area — where to find it", dlc:false}
```

To add, remove, or correct a picto, just edit one line. No build step, no database.

---

## Deploy

The site is a single static HTML file — zero dependencies. It's configured for **GitHub Pages** from the `main` branch root. Any push to `main` auto-deploys.

---

## Disclaimer

*Clair Obscur: Expedition 33* © Sandfall Interactive / Kepler Interactive. This is an unofficial fan project. Data sourced from community guides and verified against in-game information.

---

## Changelog

| Date | Change |
|---|---|
| 2026-07-29 | Initial release — 210 pictos, search, checklist, DLC support |
