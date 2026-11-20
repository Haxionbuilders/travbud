# TravBud Project Documentation & AI Continuity Log
## VERSION 4.4 — 100% ONLINE SEARCH & GOOGLE-MAPS STYLE SYSTEM — 2026-11-21

---

## 🔍 WHAT IS TRAVBUD?

**TravBud** is a single-page travel and mobility platform:
- **Live Deployment URL:** https://haxionbuilders.github.io/travbud/
- **GitHub Repository:** https://github.com/Haxionbuilders/travbud
- **GitHub Pages Branch:** `main` (root `/`)
- **Repository Rules:** [`GEMINI.md`](./GEMINI.md) (Enforced build invariants & security)

### Source References:
- `refrence and sources/TRavBud-group-trips-wizard (10).zip`: Original reference project containing `MobilityHub.tsx` and `Trips.tsx` with live Photon & OpenStreetMap integrations.
- `refrence and sources/build_clean.js`: Production build script with automated AST checks.
- `refrence and sources/index.html`: Production single-page distribution file.

---

## 🌐 100% ONLINE MAPS & SEARCH ENGINE (v4.4 Production Upgrade)

As requested, all offline map constraints and static place lookups have been replaced with the live online search and mapping engine from `TRavBud-group-trips-wizard (10).zip`:

### 1. Online Place Autocomplete via Photon API (Komoot / OpenStreetMap)
- **Engine:** `https://photon.komoot.io/api/?q={query}&limit=6&lang=en`
- **Book & Mobility Combobox (`Eu`):**
  - As the user types in From / To fields, queries the live Photon API in real-time.
  - Returns real places with names, districts, states, countries, and exact latitude/longitude.
  - Matches local railway stations (`CGY`, `ERS`, `TCR`, etc.) AND any global location simultaneously.
  - If no station matches, provides instant `Use "[Typed Place]"` fallback.
- **Group Trips Wizard (`n1` in `Yx`):**
  - Place search upgraded from offline `Wx(G)` array to live Photon API.
  - Search any town, city, landmark, or station in India or worldwide.

### 2. Live Street Maps (OpenStreetMap & Leaflet)
- **Book & Mobility Route Map (`ww` & `Sw`):**
  - Replaced offline TopoJSON grid with live OpenStreetMap street tiles (`https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png`).
  - Street-level zoom up to level 19 with zoom controls.
  - Real road and rail polylines and interactive pin markers.
  - Badge updated to `"Online Map · OpenStreetMap Live"`.
- **Group Trips Route Map:**
  - Added live interactive Leaflet route map inside the vehicle selection step (`t === "vehicle"`).
  - Displays route from Origin to Destination with custom pins and auto-fitted bounds.
- **Live Fares & Search:**
  - Dedicated modal route map with live tiles and real distances.

### 3. Verified Architecture & Zero Syntax Errors
- All 8 script blocks validated through Node AST parser (`node --check` and `vm.Script`).
- 100% clean, error-free production build.

---

## 🔒 SECURITY & SECRETS HYGIENE
- GitHub PAT tokens are strictly redacted (`ghp_[REDACTED]`) in all committed files.

*Log updated by Antigravity AI Agent — Version 4.4 Final*
