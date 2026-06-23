# Demo-Bau-Spezifikation — Premium-Juwelier (Richtung A: Luxury Minimal)

Diese Datei ist die verbindliche Grundlage für **alle** Demo-HTML-Dateien unter `/demos`.
Jede Datei ist **standalone** (per Doppelklick offline lauffähig), inline CSS + JS,
Three.js nur per importmap von CDN, Fonts per `<link>` (nur Demo-Phase).

## Anti-Slop (nicht verhandelbar)
- Kein `background-clip:text` Gradient-Text als Headline-Trick.
- Kein Default-Glassmorphism (`backdrop-blur` + halbtransparentes Weiß) als Reflex.
- Kein „Eyebrow-Label + Nummer" auf jeder Sektion (`01 — ÜBER UNS`).
- Keine farbigen Seitenstreifen-Border links an Cards.
- Keine Buzzwords („revolutionär", „nahtlos", „maßgeschneidert für Sie").
- **Keine em-dashes (—) in sichtbarer Copy.** Stattdessen Halbgeviertstrich mit Leerzeichen, Komma oder Doppelpunkt.
- Kontrast überall ≥ 4.5:1. Gold nie als Fließtext auf dunkel unter 4.5:1.
- Max. 3 Schriftfamilien. Display via `clamp()`, max ≤ 6rem (außer 1 bewusste Statement-Headline).
- Farben in OKLCH.

## Design-Tokens (in jede Datei als :root kopieren)
```css
:root{
  --obsidian:    oklch(0.16 0.006 270);
  --ink:         oklch(0.21 0.008 270);
  --offwhite:    oklch(0.96 0.004 90);
  --muted:       oklch(0.72 0.01 90);
  --gold:        oklch(0.72 0.10 85);
  --gold-bright: oklch(0.82 0.09 82);
  --gold-deep:   oklch(0.58 0.09 78);
  --platinum:    oklch(0.80 0.008 250);
  --hairline:    oklch(0.30 0.01 270 / 0.6);
  --focus:       oklch(0.82 0.09 82);
}
```

## Typografie
- Display/Headline: **Cormorant Garamond** (NICHT Playfair).
- Body/UI: **Inter** (oder Manrope).
- Preise: `font-variant-numeric: tabular-nums`.
- Demo-Fonts per `<link>` von Google Fonts erlaubt; Code-Kommentar: „PROD: next/font lokal".

## Responsive-Pflicht (jede Datei)
- Mobile-First, fluid `clamp()`-Typo, KEINE px-Fonts.
- Hero: `min-height: 100svh` (Fallback `100vh`).
- Touch-Ziele ≥ 44px. Kein horizontales Scrollen (320px–4K).
- Grids: `repeat(auto-fit, minmax(...))`. Bilder/Canvas mit `aspect-ratio` gegen CLS.
- `@media (prefers-reduced-motion: reduce)`: Animation/autoRotate/Partikel aus.
- Schlanke Top-Nav nur wo sinnvoll (Wordmark + minimale Links + „Termin"-Button).

## 3D / Interaktion (Three.js r170+ per importmap)
- Procedural Objekte (Goldring + Diamant, Uhr aus Primitiven). `MeshPhysicalMaterial`
  (Gold: metalness 1, roughness ~0.15; Diamant: transmission/clearcoat, ior 2.4).
- Environment: `RoomEnvironment` + `PMREMGenerator`. `ACESFilmicToneMapping`.
- `pixelRatio = Math.min(devicePixelRatio, 2)`. rAF bei `visibilitychange` pausieren.
- `try/catch` + CSS-Fallback wenn kein WebGL.
- Mobile-Footgun: bei `matchMedia('(pointer:coarse)')` OrbitControls-Drag aus (nur autoRotate),
  Canvas `touch-action: pan-y`. Text-Overlay `pointer-events:none`, Buttons `pointer-events:auto`.
- importmap CDN: `https://unpkg.com/three@0.170.0/build/three.module.js` + `.../examples/jsm/`.

## Compliance-Kommentare im Code (wo relevant)
- Marken (Rolex etc.): nur **Text-Wortmarken**, keine echten Logos nachbauen. Kommentar:
  `<!-- COMPLIANCE: Nur nominative Textnennung. Offizielle Konzessionär-Module in PROD einsetzen. -->`
- Goldankauf: GwG-Hinweis (Identifizierungspflicht ab Schwelle: Edelmetall/Altgold ab 2.000 € Bargeld,
  Schmuck/Uhren ab 10.000 €). Kein „anonymer Ankauf".
- Karte (Standort): DSGVO — Consent-Gate / statische Karte, kein direktes Google-Maps-iframe ohne Consent.

## Copy-Sprache
Deutsch, gehoben, nicht geschwollen. Keine Buzzwords, keine em-dashes.
Marke im Demo: „MAISON AURÉLIE" (Platzhalter-Wordmark). Stadt-Platzhalter: „Düsseldorf".

## Dateibenennung
`sektion-<n>-<name>-v<k>.html` (z. B. `sektion-1-hero-v1.html`).
Jede Datei oben im `<head>` ein Kommentarblock: Variantenname, tragende Idee, Technik, Produktionspfad.

## Definition of Done (pro Datei)
Responsiv 320–4K · reduced-motion ok · ohne WebGL/JS sauber degradiert · Touch ≥ 44px ·
Kontrast ≥ 4.5:1 · Fokus sichtbar · semantisches HTML/ARIA · pixelRatio gecappt · keine CLS · Compliance-Kommentare.
