# TravBud Project Documentation & AI Continuity Log
## VERSION 4.3 — LIVE ONLINE MAPS & COMPLETE BUG REPAIR — 2026-11-21

---

## 🔍 WHAT IS TRAVBUD?

**TravBud** is a single-page travel and mobility platform hosted at:
- **Live site**: https://haxionbuilders.github.io/travbud/
- **GitHub repo**: https://github.com/Haxionbuilders/travbud
- **GitHub Pages branch**: `main` (root `/`)
- **Repository Rules**: [`GEMINI.md`](./GEMINI.md) (Enforced build invariants & security)

### Source files:
| File | Purpose |
|------|---------|
| `refrence and sources/TravBud-Widget-Reader-Tickets (1).html` | Original raw reference HTML (preserved) |
| `refrence and sources/_source_logo_patched.html` | High-fidelity intermediate base with verified syntax |
| `refrence and sources/build_clean.js` | Production build pipeline — compiles, transforms, and runs AST checks |
| `refrence and sources/index.html` | Compiled distribution output |
| `refrence and sources/travbud-logo.jpg` | Proportional user logo (1024×558, 1.83:1 aspect ratio) |
| `deploy/` | Git deployment directory (linked to remote origin) |

---

## 🗺️ GOOGLE-MAPS STYLE ONLINE MAPS EVERYWHERE (v4.3 Update)

Previously, TravBud used a static offline TopoJSON map that only had rough boundaries and limited pre-calculated routes. Per user request, the mapping engine has been upgraded across all modules:

1. **Book & Mobility Module (`Mw` & `Sw`):**
   - Replaced offline TopoJSON grid with live **OpenStreetMap / Leaflet tile layers**.
   - Displays real streets, highways, towns, rivers, transit hubs, and landmarks across India and worldwide.
   - Zoom level upgraded to **zoom 19** with smooth zoom controls and responsive pinch-to-zoom on mobile.
   - Polyline route drawing and station markers render on actual roads and railways.
   - Badge updated from `"Offline map · bundled data"` to `"Online Map · OpenStreetMap Live"`.

2. **Group Trips Module (`Yx`):**
   - Added interactive route map component during vehicle selection and pass preview.
   - Dynamic markers placed on user-selected Origin and Destination with interactive popup tooltips.
   - Automatically computes route bounds and fits map view with comfortable padding.

3. **Live Fares & Search Module (`TbLiveFaresPage`):**
   - "View Online Map" opens a dedicated modal view with Leaflet live street tiles and interactive route polylines.
   - Works for any city, station, or custom place globally.

---

## 📋 REPAIRED BUGS & ENHANCEMENTS SUMMARY

1. ✅ **Station Autocomplete Bug ("No match for Changanassery"):**
   - Added Changanassery (`CGY`), Thiruvalla (`TRVL`), Mavelikara (`MVLK`), Kayamkulam (`KYJ`), Aluva (`AWY`), Angamaly (`AFK`), Chalakudy (`CKI`), Haripad (`HAD`), Thalassery (`TLY`), Vadakara (`VDK`), and Payyanur (`PAY`).
   - Upgraded combobox `Eu`: if a typed place does not match existing stations, an instant `Use "[Place]"` option allows selecting any custom location globally.
2. ✅ **Dedicated Tabs Architecture:**
   - "Live Fares" and "Orders & Passes" integrated cleanly into the navigation array (`bu`) and React switcher.
   - No overlay collisions with Book & Mobility or other pages.
3. ✅ **Working NUMob Boarding Passes & QR Codes:**
   - Fully functioning scannable QR passes encoded with JSON itinerary and passenger details.
   - Clean printable pass format with auto-trigger print dialog.
4. ✅ **Syntax & HTML Lexer Safety:**
   - Corrected extra `)` in `q8` logo component.
   - Replaced nested script tags in print templates with native `<body onload="window.print()">` to prevent premature HTML parser termination.
   - AST validation check (`node --check` and `vm.Script`) enforced for 100% zero-error builds.
5. ✅ **Design & Performance Invariants:**
   - Permanent deep navy dark theme (`#07192f`) enforced on `<html>` and initial state.
   - Verified 200-OK high-resolution Unsplash travel photography across all 20 destinations.
   - Proportional 1.83:1 logo rendering across desktop, tablet, and mobile headers.

---

## 🔒 SECURITY & SECRETS HYGIENE
- GitHub PAT tokens are strictly redacted (`ghp_[REDACTED]`) in all committed documentation, code, and commit logs to comply with GitHub Push Protection rules.

*Log updated by Antigravity AI Agent — Version 4.3 Production Ready*
