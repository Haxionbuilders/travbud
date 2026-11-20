# 🌍 TravBud — Smart Travel & Mobility Platform

<div align="center">
  <img src="travbud-logo.jpg" alt="TravBud Logo" width="220" style="border-radius: 16px; box-shadow: 0 10px 30px rgba(0, 113, 227, 0.4);" />
  <h3>Unified Mobility & Intelligent Journey Platform</h3>
  <p>Seamlessly plan, book, and explore journeys across India and worldwide. Compare multi-modal fares, navigate with live OpenStreetMap street tiles, search any place with online geocoding, and carry verified NUMob digital QR boarding passes.</p>

  <p>
    <a href="https://haxionbuilders.github.io/travbud/"><strong>🚀 Launch Live Web App »</strong></a> •
    <a href="./PROJECT_DOCUMENTATION_AND_AI_LOGS.md"><strong>📋 Full AI & Engineering Logs »</strong></a> •
    <a href="./GEMINI.md"><strong>🛡️ Workspace Invariants »</strong></a>
  </p>

  [![Deployment Status](https://img.shields.io/badge/GitHub%20Pages-Live%20%26%20Built-brightgreen.svg?style=flat-square)](https://haxionbuilders.github.io/travbud/)
  [![License](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](LICENSE)
  [![Platform](https://img.shields.io/badge/Platform-Desktop%20%7C%20Tablet%20%7C%20Mobile-0071e3.svg?style=flat-square)]()
  [![Theme](https://img.shields.io/badge/Theme-Deep%20Navy%20Dark-07192f.svg?style=flat-square)]()
  [![OpenStreetMap](https://img.shields.io/badge/Maps-OpenStreetMap%20%7C%20Leaflet-16a34a.svg?style=flat-square)](https://www.openstreetmap.org/)
</div>

---

## 🌟 Key Features

### 🔍 1. 100% Online Place Search & Geocoding
- **Live Photon Engine (`photon.komoot.io`):** Instant autocomplete for any village, town, railway station, airport, or landmark globally.
- **Unified Combobox (`Eu`):** Live suggestion dropdown matching local Kerala transit hubs (e.g. *Changanassery*, *Thiruvalla*, *Ernakulam*, *Thrissur*) alongside real-time worldwide search results.
- **Custom Place Fallback:** Instant `Use "[Typed Place]"` button allows booking to or from any custom destination without getting blocked.

### 🗺️ 2. Google-Maps Style Live Street Maps
- **OpenStreetMap & Leaflet Integration:** Full street-level map tiles rendered directly in "Book & Mobility" (`Mw` / `Sw`), replacing static offline shapes.
- **Interactive Routing:** Real polyline route drawing, custom origin/destination pin markers with tooltips, and dynamic zoom up to **zoom 19**.
- **Group Trips Route Map:** Live route visualization automatically embedded into the vehicle selection step of the Group Trips wizard.
- **Dedicated Modal Map:** High-resolution route inspector available from the Live Fares tab.

### ✈️ 3. Dedicated "Live Fares" Tab
- **Multi-Modal Estimator:** Instant realistic price and duration estimates across **Bus**, **Train**, **Cab / Taxi**, and **Flight** based on real road distances.
- **Live Wikipedia Guide:** Fetches live destination summaries and high-definition photography on demand.
- **Live Weather Integration:** Real-time temperature and weather conditions via the Open-Meteo REST API.
- **Quick Destination Chips:** One-tap presets for Munnar, Alappuzha, Thekkady, Wayanad, Changanassery, Delhi, Goa, Dubai, and more.

### 🎫 4. Dedicated "Orders & Passes" Tab with Scannable QR Codes
- **NUMob Digital Passes:** Pre-loaded and user-created digital boarding passes across Rail (`Parasuram Express`), Cab (`Hire-a-Bud Sedan`), Bus (`KSRTC Fast Passenger`), and Flight (`Air India`).
- **Functioning QR Codes:** Interactive scannable QR passes generated in real time (`qrcodejs`) containing PNR, passenger info, route, seat/berth, and validity.
- **Print & PDF Export:** Formatted one-click print view designed for mobile and desktop printing.

### 🎨 5. Responsive UI & Dark Mode Invariants
- **Zero White Background Flashes:** Deep Navy Dark Theme (`#07192f` / `#0b1329`) enforced at the root HTML level.
- **Custom Proportional Logo:** Displays the user's custom TravBud emblem at its native `1.83:1` aspect ratio without squishing or distortion.
- **Curated Photography:** High-resolution travel imagery across all 20 featured destinations (verified 200-OK Unsplash photography).
- **Responsive Layout:** Adaptive layouts optimized for smartphones (<640px), tablets (640px–1024px), and desktops (>1024px).

---

## 🚀 Live Demo

The latest production build is deployed and hosted on GitHub Pages:  
👉 **[https://haxionbuilders.github.io/travbud/](https://haxionbuilders.github.io/travbud/)**

---

## 🛠️ Tech Stack & Services

| Layer | Technologies |
|---|---|
| **Core Framework** | Single-page bundled React 18, Vite runtime |
| **Styling & Design** | Tailwind CSS, Glassmorphic navy containers, custom SVG icons |
| **Interactive Maps** | Leaflet.js 1.9.4, OpenStreetMap tile servers (`tile.openstreetmap.org`) |
| **Geocoding & Search** | Photon API (Komoot / OpenStreetMap Nominatim data) |
| **Live APIs** | Wikipedia REST API (summaries & media), Open-Meteo (live weather) |
| **Digital Passes** | QRCode.js (dynamic vector matrix rendering) |
| **Deployment** | GitHub Pages, automated AST syntax checking (`node --check`) |

---

## 📋 Documentation & AI Continuity Logs

For developers and AI pair programmers working on this repository, complete architectural breakdowns, component variable tables, and step-by-step changelogs are documented in:

* 📄 **[PROJECT_DOCUMENTATION_AND_AI_LOGS.md](./PROJECT_DOCUMENTATION_AND_AI_LOGS.md)**
* 🛡️ **[GEMINI.md](./GEMINI.md)** — Workspace invariants, secret hygiene, AST validation gates, and HTML lexer safety rules.

---

## 💻 Local Quickstart

To run the application locally:

```bash
# 1. Clone repository
git clone https://github.com/Haxionbuilders/travbud.git
cd travbud

# 2. Open in browser (no build step or server required)
# Simply double-click index.html or serve using any static server:
npx serve .
```

---

<div align="center">
  <sub>Built with ❤️ for travelers across India and beyond. © 2026 TravBud Mobility Platform.</sub>
</div>
