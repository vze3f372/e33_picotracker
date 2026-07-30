# Pictos, Luminas & Weapons Tracker -- Expedition 33

A comprehensive single-page checklist and reference for every **Picto**, **Weapon**, and **Achievement/Trophy** in *Clair Obscur: Expedition 33*. Track what you've found, search by name/effect/location, filter by stat/rarity/character, sync across devices -- all in a game-styled UI.

**Live site:** <https://vze3f372.github.io/e33_pictotracker/>

---

## What's Inside

- **210 Pictos** -- all 193 base-game + 17 from the Verso's Drafts (Thank You Update) DLC, with full stats, effect, LP cost, and location
- **117 Weapons** -- each with character assignment, element, max power, scaling ranks, passives, location, and DLC tag
- **55 Achievements/Trophies** -- with rarity (Platinum/Gold/Silver/Bronze), secret/missable tags
- **Checklists** -- click any card to mark it collected; state saves to your browser via localStorage
- **Search** -- filters pictos by name, effect, or location; weapons by name, character, or location; achievements by name or description
- **Filters** -- per-tab filters for All / Collected / Missing, plus stat (Pictos), character (Weapons), and rarity (Achievements)
- **Progress bars** -- completion percentage for each category
- **Platinum auto-lock** -- the Platinum trophy auto-checks when all 54 others are complete and cannot be toggled manually
- **Cross-device sync** -- send your progress between devices via Firebase Firestore REST API (no SDK); auto-generated sync code with 15-second background polling
- **Info tab** -- system explainer for Pictos, Luminas, Lumina Points, stat/cost reference tables, and a Sync setup guide
- **Tabbed interface** -- Info / Pictos / Weapons / Achievements; active tab persists across refreshes
- **iOS home screen support** -- full-screen, black-translucent status bar, apple-touch-icon

---

## Visual Style

The site draws from the game's **Belle Epoque** meets **chiaroscuro** aesthetic:
- Dark, oil-painted backgrounds with radial glow gradients
- Gold accents, ornamental dividers, and decorative fleurons
- Official game logo at the hero for the title treatment
- **Cinzel** for all headings
- **IM Fell Double Pica** for body text
- **EB Garamond** for descriptions and flavour text
- **Bebas Neue** for numbers, **Abril Fatface** for display stats
- Frameless card layout with subtle borders

---

## How to Maintain

All data lives in `index.html` in three arrays:

- `PICTO_DATA` -- 210 pictos with name, stats, effect, LP cost, location, DLC flag
- `WEAPON_DATA` -- 117 weapons with name, character, element, power, scalings, passives, location, DLC flag
- `ACHIEVEMENT_DATA` -- 55 achievements with name, description, rarity, secret/missable flags

```js
// Picto entry
{name:"Picto Name", stats:["Health","Speed"], effect:"Effect description.",
 cost:5, location:"Area -- where to find it", dlc:false}

// Weapon entry
{name:"Weapon Name", c:"Gustave/Verso", elem:"Fire", pow:168,
 sc:["A","C","B","D","S"], p:["Passive 1","Passive 2","Passive 3"],
 loc:"Area -- where to find it", dlc:false}

// Achievement entry
{n:"Achievement Name", d:"Description of how to unlock.", r:"gold", s:true, m:false}
```

To add, remove, or correct an entry, just edit one line. No build step, no database.

---

## Deploy

The site is a single static HTML file plus a few asset PNGs -- zero dependencies. It's configured for **GitHub Pages** from the `main` branch root. Any push to `main` auto-deploys.

---

## Disclaimer

*Clair Obscur: Expedition 33* (c) Sandfall Interactive / Kepler Interactive. This is an unofficial fan project. Data sourced from community guides and verified against in-game information.

---

## Changelog

| Date | Change |
|---|---|
| 2026-07-31 | Achievements tracker (55 trophies, rarity filters, platinum auto-lock, search, Check All/Clear All); fixed sync for deliberate empty state; moved footer below all tabs; Opera Speed Dial icon support; muted/unchecked card styling |
| 2026-07-30 | Weapons tracker (117 weapons, character filter, scaling badges, element tags, passives); cross-device sync via Firebase REST API; Info tab with reference panels and Sync guide; tab reorder (Info first); repo renamed to e33_pictotracker |
| 2026-07-29 | Initial release -- 210 pictos, search, checklist, DLC support |
