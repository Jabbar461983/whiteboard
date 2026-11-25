# Pro & Kontra Board

Digitales Whiteboard für Workshops: Mitarbeitende erfassen per Smartphone (QR-Code) grüne Pro- und rote Kontra-Post-its, das Board bündelt sie live. Export als PDF (A4 quer).

## Veröffentlichen auf GitHub Pages (ca. 5 Minuten)

1. Auf github.com ein neues Repository anlegen, z. B. `pro-kontra-board` (Public).
2. `index.html` hochladen («Add file → Upload files» → «Commit changes»).
3. «Settings → Pages»: Source «Deploy from a branch», Branch `main`, Ordner `/ (root)` → «Save».
4. Nach ca. 1 Minute läuft die App unter `https://<dein-github-name>.github.io/pro-kontra-board/`.

## Ablauf im Workshop

1. Seite öffnen → Titel eingeben → «Neues Board erstellen».
2. Board auf den Beamer, «Mehr → QR-Code gross anzeigen».
3. Mitarbeitende scannen, geben einmal ihren Namen ein, wählen Pro/Kontra und senden.
4. Karten anklicken, um sie zu bearbeiten, umzufärben oder zu löschen (Rückgängig möglich).
5. «PDF exportieren» → im Druckdialog «Als PDF sichern» wählen. Tipp: «Hintergrundgrafiken» aktivieren, damit die Farben mitgedruckt werden.

Wer den **Board-Link** hat («Mehr → Board-Link kopieren»), kann Titel und Karten bearbeiten. Der QR-Code führt auf die Erfassungsansicht.

## Technik & Datenschutz

- Eine einzige Datei, kein Server, kein Login.
- Nachrichten laufen über den kostenlosen Relay **ntfy.sh**. Alle Inhalte werden vorher im Browser mit AES-128-GCM verschlüsselt. Der Schlüssel steckt nur im Link nach dem `#` und wird nie an einen Server übertragen.
- ntfy.sh hält Nachrichten 12 Stunden. Das Board speichert zusätzlich lokal im Browser und sendet beim Öffnen fehlende Karten automatisch neu. Für längere Aufbewahrung: «Mehr → Board sichern (Datei)» bzw. «Board laden».
- Gratis-Limit von ntfy.sh: ca. 250 Nachrichten pro Tag und IP-Adresse. Im Firmen-WLAN teilen sich alle eine IP. Bei grossen Gruppen besser mobile Daten nutzen.
- Eigener ntfy-Server möglich: Link mit `?srv=https://dein-ntfy-server` aufrufen.
- Schrift: SBB Web Light vom SBB-CDN (Fallback: Helvetica/Arial).
