# DLP Priority

Eine iPhone-optimierte PWA zum Erfassen und Verwalten von Rueckkehrzeiten fuer Priority-Karten im Disneyland Paris.

## Enthalten

- Hauptuebersicht mit aktuellster und naechster Rueckkehrzeit
- mehrere Priority-Karten als Reiter
- vergangene, aktuelle und geplante Zeiten
- Karte anlegen, umbenennen und loeschen
- Zeiten hinzufuegen, bearbeiten und Erinnerungen ein-/ausschalten
- PWA-Manifest und Service Worker
- iPhone-Home-Screen-Icon in `icons/`
- ohne Build-Schritt direkt auf Vercel deploybar

## Auf GitHub laden

1. Neues GitHub-Repository anlegen.
2. Den Inhalt dieses Ordners in das Repository hochladen.
3. Darauf achten, dass `index.html` im Hauptverzeichnis liegt.

Beispiel mit Git:

```bash
git init
git add .
git commit -m "DLP Priority initial version"
git branch -M main
git remote add origin https://github.com/DEIN-NAME/DEIN-REPO.git
git push -u origin main
```

## Auf Vercel deployen

1. In Vercel **Add New Project** waehlen.
2. Das GitHub-Repository importieren.
3. Framework-Preset auf **Other** oder **Static** setzen.
4. Build Command leer lassen.
5. Output Directory leer lassen.
6. Deploy starten.

Vercel kann die statische App direkt ausliefern. `vercel.json` sorgt dafuer, dass der Service Worker nicht unnoetig lange aus dem Cache geladen wird.

## Auf dem iPhone installieren

1. Die Vercel-Adresse in Safari oeffnen.
2. Teilen antippen.
3. **Zum Home-Bildschirm** waehlen.
4. Mit **Hinzufuegen** bestaetigen.

Das Icon stammt aus `icons/icon-180.png` und wird ueber `apple-touch-icon` eingebunden. Das Manifest stellt zusaetzlich die PWA-Informationen fuer kompatible Browser bereit.

## Hinweis zu Notifications

Die Vorschau kann die Browser-Berechtigung anfordern. Zuverlaessige Erinnerungen im Hintergrund, auch wenn Safari nicht geoeffnet ist, benoetigen fuer die produktive Version noch einen Push-Dienst und eine serverseitige Speicherung der Zeiten. Die statische Vercel-Version ist dafuer vorbereitet, enthaelt aber bewusst noch keinen geheimen API-Schluessel und keinen externen Push-Provider.
