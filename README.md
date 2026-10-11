# Flight Level Rechner

Offline-fähiger Flight-Level-Rechner (FL ↔ Fuß ↔ Meter) mit Ost-/Westkurs-Regel und RVSM-Tabellen.

## Als Android-App installieren (PWA)

1. Dateien auf einem HTTPS-Server hosten (z. B. GitHub Pages).
2. Auf dem Android-Gerät Chrome öffnen und die Seite aufrufen.
3. Menü → „Zum Startbildschirm hinzufügen“ / „App installieren“.
4. Die App erscheint wie eine native App, funktioniert offline.

## Lokale Nutzung

Einfach `index.html` im Browser öffnen (funktioniert auch offline, sobald einmal geladen).

## Technik

- Reine HTML/CSS/JS – kein Framework
- Service Worker für Offline-Betrieb
- Manifest für Installierbarkeit als PWA
- ICAO-Standard: 1 ft = 0,3048 m, Standarddruck 1013,25 hPa

## Mit Capacitor als native APK bauen (optional)

```bash
npm install -g @capacitor/cli
npx cap init "Flight Level" com.example.flightlevel --web-dir .
npx cap add android
npx cap sync
# Dann in Android Studio öffnen und bauen
```
