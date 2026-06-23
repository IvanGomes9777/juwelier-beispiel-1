RING-FOTO HIER ABLEGEN
======================

Datei:  ring.png

Die Hero-Variante "sektion-1-hero-v6.html" lädt automatisch ./assets/ring.png.

Empfehlung:
- Transparenter Hintergrund (PNG mit Alpha) sieht auf dem dunklen Hero am besten aus.
- Ein weißer Hintergrund wird beim Aufruf über einen Webserver (http) automatisch
  entfernt. Beim direkten Doppelklick (file://) kann der Browser die Pixel aus
  Sicherheitsgründen nicht lesen; dann wird das Foto unverändert gezeigt. Für die
  saubere Freistellung daher entweder ein transparentes PNG verwenden oder die Datei
  über einen lokalen Server öffnen:
      cd demos && python3 -m http.server 8000
      Browser: http://localhost:8000/sektion-1-hero-v6.html

Fehlt die Datei, zeigt die Hero-Variante einen eleganten CSS-Platzhalter-Ring.
