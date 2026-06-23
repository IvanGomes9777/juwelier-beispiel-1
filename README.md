# MAISON AURÉLIE — Premium-Juwelier (Demo-Phase)

Interaktive, 3D-getriebene Juwelier-/Uhren-/Schmuck-Website, gebaut Sektion für Sektion.
Diese Phase liefert **Skizzen als eigenständige HTML-Dateien** (offline per Doppelklick lauffähig),
bevor eine Richtung nach Next.js / React Three Fiber überführt wird.

## Überblick

- **9 Sektionen × 5 Varianten = 45 Demos** unter [`/demos`](./demos).
- Übersichtsgalerie: [`demos/index.html`](./demos/index.html) — alle Varianten verlinkt.
- Verbindliche Bau-Spezifikation: [`demos/_SPEC.md`](./demos/_SPEC.md) (Tokens, Anti-Slop, Responsive, Compliance).

| # | Sektion | Dateien |
|---|---------|---------|
| 1 | Hero | `sektion-1-hero-v1..v5.html` |
| 2 | Marken / Konzessionär | `sektion-2-marken-v1..v5.html` |
| 3 | Kollektionen | `sektion-3-kollektionen-v1..v5.html` |
| 4 | Trauringe + Beratungstermin | `sektion-4-trauringe-v1..v5.html` |
| 5 | Manufaktur / Meisteratelier | `sektion-5-manufaktur-v1..v5.html` |
| 6 | Service | `sektion-6-service-v1..v5.html` |
| 7 | Bewertungen / Trust | `sektion-7-trust-v1..v5.html` |
| 8 | Standort / Kontakt | `sektion-8-standort-v1..v5.html` |
| 9 | Footer | `sektion-9-footer-v1..v5.html` |

## Designrichtung

Richtung A — Luxury Minimal: Obsidian/Tiefschwarz, Champagner-Gold, Cormorant Garamond (Display)
+ Inter (Body). Farben in OKLCH. Anti-Slop-Disziplin: kein Gradient-Text-Trick, kein
Default-Glassmorphism, keine em-dashes in sichtbarer Copy.

## Qualität pro Datei

Responsiv 320px–4K, kein horizontales Scrollen, Touch ≥ 44px, Kontrast ≥ 4.5:1,
`prefers-reduced-motion` respektiert, 3D mit WebGL-Fallback (try/catch) und gecapptem `pixelRatio`.

## Compliance (im Code kommentiert)

- **Marken-CI:** echte Markennamen nur als **Text** (nominative Nennung). Keine Logos nachgebaut;
  offizielle Konzessionär-Module folgen in Produktion.
- **GwG (Goldankauf):** Identifizierungshinweis ab Bargeld-Schwelle (Edelmetall/Altgold ab 2.000 €,
  Schmuck/Uhren ab 10.000 €), kein anonymer Ankauf.
- **DSGVO (Karte):** kein Drittanbieter-Embed vor Consent; Platzhalter + Click-to-load.

## Produktions-Transfer (nächster Schritt)

Festgelegte Varianten werden zu Next.js-Komponenten (App Router, TypeScript, Tailwind, shadcn/ui),
vanilla Three.js zu R3F + Drei wo sinnvoll, `motion/react`, lokale Fonts via `next/font`.
Demo-Fonts laufen per CDN-`<link>` — in Produktion lokal einbinden.
