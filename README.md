# HappyXploreBd — My Travel Story

Track which of Bangladesh's 64 districts (and upazilas) and which countries you have visited. Bangla and English. No login — data stays in your browser.

## Features
- Interactive map of 64 districts / 544 upazila-thana areas (real boundaries, embedded — no import needed)
- Click a district (or switch to *Upazila view* and click upazilas) to mark it visited
- District panel: upazila checklist, famous products (★ = official GI), places to visit, official district website
- Rotatable 3D-style globe (drag to spin, wheel to zoom, click a country to mark it visited) plus a flat world map, country search, continent stats
- Photocard Studio: 4 templates, 3 aspect ratios, PNG / JPG / PDF export
- Profile photo (resized locally), JSON backup/restore, reset with confirmation
- Full-screen maps, zoom, drag-to-pan, Bangla/English toggle

## Run locally
No build step. It is a single static page.

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy on GitHub Pages
1. Push this folder to a GitHub repository (branch `main`).
2. *Settings → Pages → Build and deployment → Source: GitHub Actions*.
3. The included workflow (`.github/workflows/pages.yml`) publishes the site on every push.
(Alternatively choose *Deploy from a branch* → `main` / root.)

## Data and your privacy
- Everything is stored in your browser (`localStorage` / IndexedDB). Clearing site data deletes it.
- Data does **not** follow you across devices. Use **Profile & Data → Export JSON**, then **Import JSON** on the other device.
- No accounts, no analytics.

## External services (loaded at runtime)
Google Fonts, cdnjs (jsPDF, d3, topojson), jsDelivr (Datamaps world shapes). If the world shapes fail to load (no internet / CDN blocked), the World tab shows a message asking you to reload.

## Known limitations
- 544 map areas = upazilas plus metropolitan thanas. A few official upazilas have no separate shape in the source data.
- The 118 shapes with no district in the source were assigned by name + location; 28 were placed manually (e.g. Bakalia → Chattogram, Boalia → Rajshahi). Please review `index.html` data if you need survey-grade accuracy.
- Boundaries are simplified for web use; district border lines are incomplete where source polygons do not share vertices.
- "Famous for" and "Places to visit" are short lists from the sources in `ATTRIBUTION.md`, not a complete cultural database. District history, festivals and crafts are not included yet.
- The world map list (~177 countries) omits some small countries.

## Credits
Developed by **Md Farhadul Islam (মো ফরহাদুল ইসলাম)** — https://wolfbackcse.github.io/My_Portfolio/

## Licence
Code: MIT (replace `<YOUR NAME>` in `LICENSE`, e.g. with Md Farhadul Islam). Data: see `ATTRIBUTION.md` — geoBoundaries requires attribution (CC BY 4.0).
