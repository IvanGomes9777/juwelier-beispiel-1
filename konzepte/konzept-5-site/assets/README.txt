RING-FOTO HIER ABLEGEN
======================

Datei:  ring.png   (in diesem Ordner: konzept-5-site/assets/ring.png)

Der Hero von index.html laedt automatisch ./assets/ring.png mit Pointer-Tilt,
Gold-Glint und Diamant-Funkeln.

- Am besten ein PNG mit transparentem Hintergrund.
- Weisser Hintergrund wird beim Aufruf ueber einen lokalen Server (http)
  automatisch per Rand-Flood-Fill entfernt (die hellen Diamant-Facetten bleiben).
  Beim reinen Doppelklick (file://) kann der Browser die Pixel aus Sicherheits-
  gruenden nicht lesen, dann wird das Foto unveraendert gezeigt. Fuer das beste
  Ergebnis offline daher ein transparentes PNG verwenden, oder lokal servern:

      cd konzepte/konzept-5-site
      python3 -m http.server 8000
      Browser: http://localhost:8000/

Fehlt die Datei, zeigt der Hero einen eleganten CSS-Platzhalter-Ring.
