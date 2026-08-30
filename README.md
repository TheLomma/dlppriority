# DLP Priority

Eine iPhone-optimierte PWA zum Erfassen und Verwalten von Rückkehrzeiten für Priority-Karten im Disneyland Paris.

## Projektstruktur

- `index.html` – Web-App
- `manifest.webmanifest` – Installation als PWA
- `sw.js` – Offline-Grundfunktionen
- `vercel.json` – Vercel-Konfiguration
- `icons/icon-180.png` – iPhone-Home-Screen-Icon
- `icons/icon-192.png` und `icons/icon-512.png` – PWA-Icons
- `icons/favicon-32.png` – Browser-Favicon
- `assets/dlp-priority-logo.png` – Original-Logo in hoher Auflösung; wird zusätzlich oben in der App angezeigt

## Änderungen am Logo in GitHub übernehmen

Wenn das Repository bereits existiert, lade mindestens diese Dateien hoch und überschreibe die vorhandenen Versionen:

1. `assets/dlp-priority-logo.png` neu hinzufügen.
2. `icons/icon-180.png` ersetzen.
3. `icons/icon-192.png` ersetzen.
4. `icons/icon-512.png` ersetzen.
5. `icons/favicon-32.png` ersetzen.
6. `index.html` ersetzen.

`manifest.webmanifest`, `sw.js` und `vercel.json` können unverändert bleiben.

## Einfachster Weg über die GitHub-Weboberfläche

1. Repository auf GitHub öffnen.
2. **Add file** → **Upload files** wählen.
3. Die genannten Dateien bzw. den Ordner `assets` auswählen.
4. Darauf achten, dass die Ordnerstruktur erhalten bleibt: `assets/...` und `icons/...`.
5. Unten **Commit changes** wählen.

## Alternative: gesamtes Projekt ersetzen

Du kannst auch den gesamten Inhalt dieses Pakets in dein Repository hochladen. `index.html` muss im Hauptverzeichnis liegen.

## Vercel aktualisieren

Wenn Vercel bereits mit GitHub verbunden ist, startet der neue Deployment normalerweise automatisch nach dem Commit. Falls nicht:

1. Vercel öffnen.
2. Dein Projekt öffnen.
3. **Deployments** → **Redeploy** wählen.
4. Nach dem neuen Deployment die URL in Safari öffnen.

## Logo auf dem iPhone sehen

1. Die aktualisierte Vercel-URL in Safari öffnen.
2. Falls das alte Symbol angezeigt wird, die Web-App vom Home-Bildschirm entfernen.
3. Die Seite in Safari neu laden.
4. Teilen → **Zum Home-Bildschirm** → **Hinzufügen**.

Das iPhone verwendet dafür `icons/icon-180.png` über `apple-touch-icon`. Das Manifest enthält zusätzlich die 192px- und 512px-Versionen.

## Hinweis zu Erinnerungen

Die Oberfläche und die PWA-Struktur sind vorbereitet. Zuverlässige Push-Erinnerungen im Hintergrund, wenn Safari vollständig geschlossen ist, benötigen für die produktive Version noch einen Push-Dienst und serverseitige Speicherung.
