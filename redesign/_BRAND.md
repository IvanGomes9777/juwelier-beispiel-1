# VEYRA — Markenspezifikation (Redesign)

> Arbeitsstand. Marke frei gewählt (Platzhalter-Rebrand), kann jederzeit ersetzt werden.

## Identität
- **Name / Wortmarke:** VEYRA (lang: MAISON VEYRA)
- **Standort:** Düsseldorf · Königsallee
- **Positionierung:** Haute Joaillerie & Horlogerie — feiner Schmuck, Trauringe nach Maß, ausgewählte Uhren
- **Sprache:** Deutsch (primär), französische Luxus-Akzente (Maison, Haute Joaillerie, Atelier)
- **Tonalität:** elegant-modern, cinematisch — Cartier-Eleganz × smartdevicetec-Erlebnis
- **Claim:** „Im Licht gefasst." · FR: „Le sens de la lumière."

## Designsystem (Tokens)

### Light-Modus (Boutique/Editorial)
- `--paper` #F7F2E9 · `--paper-2` #ECE3D4 · `--ink` #16130F
- `--muted` #6E665A · `--gold` #B68A3E · `--line` rgba(22,19,15,.13)

### Dark-Modus (Cinématique/Hero)
- `--bg` #0B0B0D · `--bg-2` #121216 · `--fg` #EFE9DF
- `--muted-d` #8A867E · `--gold-d` #C9A45B · `--line-d` rgba(239,233,223,.16)

### Typografie
- **Display (Serif):** Cormorant Garamond / Fraunces — Headlines, Wortmarke
- **Body (Sans):** Inter / Manrope
- **Akzent (Mono):** JetBrains Mono — Zahlen, Index „№ 01/05", technische Labels (smartdevice-Feel)

### Motion
- Easing `cubic-bezier(.22,1,.36,1)`, Dauer 240–500ms
- Loading-Intro, Sektions-Index, magnetische CTAs, transparent→solid Header
- Immer `prefers-reduced-motion` respektieren

## Referenzen (Inspiration)
- cartier.com / Watches & Wonders — mehrstufiger Header, Mega-Menü, Serif-Eleganz
- smartdevicetec.com — Loading, Zähler, cinematisch (**Leit-Erlebnis**)
- jurijewelry.com / ino.jewelry — Editorial-Minimal, Live-Edelmetallpreis, Shop-Logik
- webgi-jewelry.vercel.app — 3D-Konfigurator, Material-Selektor

## Bilder
Vorerst Unsplash-Platzhalter (themenpassend, URLs auf HTTP 200 geprüft). Später echte Produktfotos.

## Aufbau (Section-by-Section, je 5 Varianten zur Auswahl)
1. Navbar ✓ (`redesign/navbars/`) — Empfehlung: Cinématique × Maison
2. Hero (`redesign/hero/`)
3. Kollektionen / Vitrine
4. Trauringe / Konfigurator
5. Atelier / Manufaktur
6. Uhren
7. Trust / Bewertungen
8. Boutique / Standort / Kontakt
9. Footer
