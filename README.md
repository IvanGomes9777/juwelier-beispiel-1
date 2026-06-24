# MAISON VEYRA — Düsseldorf

Interaktive Juwelier-Startseite (Haute Joaillerie): helle, editoriale Gestaltung mit
einem echten **3D-Ring** (Three.js / GLB), Seitenleisten-Navigation mit Flyout-Vorschau,
Kollektions-Grid und Termin-Buchung.

## Struktur
- `index.html` — die komplette Startseite (HTML, CSS und JS inline, standalone).
- `assets/jewelery_ring_diamonds.glb` — 3D-Ringmodell für den Hero.
- `vercel.json` — Deployment-Konfiguration (Vercel).

## Funktionen
- **3D-Hero:** Ring drehbar (OrbitControls, autoRotate), Metallwechsel
  (Gelb-/Weiß-/Roségold/Platin), RoomEnvironment-Reflexionen, ACESFilmic.
  Foto-Fallback, wenn kein WebGL.
- **Termin buchen:** barrierefreier Dialog (Fokus-Falle, ESC, Validierung,
  Bestätigung). Aktuell clientseitige Demo, in Produktion an das Atelier anbinden.
- **Navigation:** Sidebar mit Flyout-Vorschau (Desktop), Vollbild-Menü (mobil).

## Hinweise
- Three.js wird per CDN (jsDelivr) geladen; ES-Module brauchen http(s)
  (läuft auf Vercel/Server, nicht per `file://`-Doppelklick).
- Produktion: GLB komprimieren (Draco/meshopt), lokale Fonts (`next/font` o. ä.),
  Termin-Formular serverseitig anbinden, Rechtstexte/Datenschutz ergänzen.
