# 34 יישובים חדשים ביהודה ושומרון — מפה אינטראקטיבית

An interactive map of 34 planned new settlements in Judea and Samaria (West Bank), built with Leaflet.js and ESRI ArcGIS data services.

**Live site:** [netanelgit.github.io/New_Settlement](https://netanelgit.github.io/New_Settlement/)

---

## Features

- **34 settlement markers** — each with name, region, location, and description
- **Region filter pills** — filter by North Samaria, Green Line, Binyamin, Jericho/Jordan Valley, Judea
- **Sidebar list** — searchable, grouped by region, click to fly to marker
- **Satellite basemap** — ESRI World Imagery with Hebrew place labels
- **ABC Areas layer** — toggle overlay of Oslo Accord zones (Area A, B, C, H1, H2)
- **State Land layer** — toggle overlay of state land classifications
- **Responsive** — works on mobile and desktop

---

## Layers

### ABC Areas
Sourced from the Civil Administration of Judea and Samaria (המינהל האזרחי).

| Code | Name | Color |
|------|------|-------|
| A | שטח A — Full PA control | Orange |
| B | שטח B — Joint control | Yellow |
| Reserve | שמורה | Green |
| H1 | Hebron — PA | Blue |
| H2 | Hebron — Israel | Purple |

**Service URL:**
```
https://services7.arcgis.com/LNelXmPD58p66zmN/ArcGIS/rest/services/ABCarea/FeatureServer/0
```

### State Land (אדמות מדינה)
| Type | Name |
|------|------|
| 2 | אדמות מדינה אחרי 98 |
| 4 | אדמות מדינה אחרי 2004 |
| 5 | אדמות מדינה טאבו |

**Service URL:**
```
https://services7.arcgis.com/LNelXmPD58p66zmN/arcgis/rest/services/מפת_חופש_המידע_מעודכנת_24_7_24_WFL1/FeatureServer/42
```

---

## Tech Stack

| Library | Version | Purpose |
|---------|---------|---------|
| [Leaflet.js](https://leafletjs.com/) | 1.9.4 | Map rendering |
| [esri-leaflet](https://esri.github.io/esri-leaflet/) | 3.0.12 | ArcGIS FeatureServer layers |
| ESRI World Imagery | — | Satellite basemap |
| ESRI World Boundaries | — | Hebrew label overlay |

---

## Project Structure

```
New_Settlement/
├── index.html      # Single-file app — all HTML, CSS, JS
├── preview.png     # OG image for social media sharing
└── README.md
```

---

## Running Locally

No build step required. Just open `index.html` in a browser:

```bash
# Option 1 — direct open
open index.html

# Option 2 — local server (avoids any CORS issues)
npx serve .
# or
python -m http.server 8080
```

---

## Deployment

Hosted on **GitHub Pages** from the `main` branch root.

To update: push any change to `main` and the site rebuilds automatically within ~30 seconds.
