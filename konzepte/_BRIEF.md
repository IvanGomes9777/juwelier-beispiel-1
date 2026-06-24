# Konzept-Brief — 5 Design-Richtungen (Neustart)

Ziel: **5 unterscheidbare Gesamt-Design-Richtungen** für die Juwelier-Website, damit der
Kunde **Farbe, Layout und Typografie** beurteilen kann. Jede Richtung = **eine standalone
HTML-Datei** unter `/konzepte`, offline per Doppelklick lauffähig.

## Gleiche Struktur in jeder Datei (für fairen Vergleich)
1. **Sticky Top-Nav:** Wordmark „MAISON AURÉLIE" + Links (Trauringe · Uhren · Schmuck · Manufaktur) + „Termin"-Button (≥44px).
2. **Hero:** kurze Eyebrow, große Headline (richtungs-spezifische Copy), Lede-Satz, primärer CTA „Trauring-Beratung" + sekundärer Ghost-Link, dazu eine gestaltete Visual-Fläche (CSS-Motiv/Platzhalter mit `aspect-ratio`, klar als Platzhalter markiert; PROD: Makrofoto).
3. **Designsystem-Kachel „Auf einen Blick":** Farbmuster-Reihe (Swatch + Name + Hex), Typo-Specimen (Display-Sample groß, Body-Sample, sichtbare Größen-Skala), kurze Notiz zur Akzent-Nutzung. **Das ist das Herzstück zum Farb-/Typo-Urteil.**
4. **Beispiel-Sektion:** richtungs-spezifisches Layout (z. B. 3 Kollektions-Cards Uhren/Schmuck/Trauringe ODER editorialer Split), zeigt Layout-Charakter.
5. **Mini-Footer:** NAP-Platzhalter (MAISON AURÉLIE · Königsallee 1 · 40212 Düsseldorf) + Rechts-Links-Platzhalter (Impressum · Datenschutz · AGB).

## Qualitätsregeln (alle Dateien)
- Mobile-First, fluid `clamp()`-Typo, **keine px-Fonts**, responsiv **320px–4K**, kein horizontales Scrollen.
- Touch-Ziele ≥44px, Kontrast **≥4.5:1**, sichtbare `:focus-visible`-States, semantisches HTML + ARIA.
- `@media (prefers-reduced-motion: reduce)` respektieren. Interaktion dezent (Hover/Reveal), **kein** schweres 3D in dieser Phase.
- Bilder/Visuals mit `aspect-ratio` gegen CLS.
- Max. **3 Schriftfamilien**. Display via `clamp()`. Preise/Zahlen `font-variant-numeric: tabular-nums`.
- Fonts in der Demo per Google-Fonts-`<link>` erlaubt; Kommentar „PROD: next/font lokal".

## Anti-Slop (nicht verhandelbar)
- Kein `background-clip:text`-Gradient-Headline-Trick.
- Kein Default-Glassmorphism (`backdrop-blur` + halbtransparentes Weiß) als Reflex.
- Kein „Eyebrow-Label + Nummer" (`01 — ÜBER UNS`).
- Keine farbigen Seitenstreifen-Border links an Cards.
- Keine Buzzwords („revolutionär", „nahtlos", „maßgeschneidert für Sie").
- **Keine em-dashes (—) in sichtbarer Copy.** Stattdessen Halbgeviertstrich mit Leerzeichen, Komma oder Doppelpunkt. (Auch nicht im `<title>`.)

## Kopf jeder Datei
HTML-Kommentarblock: Richtungsname, Stimmung/Idee, Farb- und Font-Wahl, wann diese Richtung passt.

## Sprache
Deutsch, gehoben, nicht geschwollen. Marke „MAISON AURÉLIE", Stadt „Düsseldorf".

## Dateibenennung
`konzept-<n>-<slug>.html`.
