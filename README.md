# Kicker Crew – Tischkicker-Statistik

Eine kleine Handy-Web-App für vier Spieler. Sie kann als App zum Startbildschirm hinzugefügt werden.

## Funktionen
- Ergebnisse für Einzel (1 gegen 1) und Doppel (2 gegen 2) erfassen
- Spiele, Siege, Niederlagen, Unentschieden und Gewinnquote pro Spieler anzeigen
- Doppel-Siege werden jedem Spieler des Siegerteams gutgeschrieben
- Spielverlauf und einzelne Spiele löschen
- Namen ändern
- Daten als JSON exportieren und wieder importieren
- Daten werden lokal im Browser gespeichert

## Schnell starten
1. Entpacke den ZIP-Ordner auf einem Computer.
2. Öffne `index.html` in einem Browser zum Testen.
3. Für die Installation auf dem Handy muss die App über HTTPS oder einen lokalen Entwicklungsserver bereitgestellt werden. Service Worker/Offline-Funktion funktionieren nicht beim direkten Öffnen der Datei.
4. Eine einfache Möglichkeit: lade die drei Dateien (`index.html`, `manifest.json`, `sw.js`) auf einen statischen Hostingdienst wie GitHub Pages oder Netlify hoch.
5. Öffne die veröffentlichte HTTPS-Adresse auf deinem Handy:
   - Android/Chrome: Menü ⋮ → „App installieren“ oder „Zum Startbildschirm hinzufügen“
   - iPhone/Safari: Teilen → „Zum Home-Bildschirm“
6. Starte die App über das neue Symbol.

## Wichtige Hinweise
- Die Daten liegen auf dem Gerät und im Browser, nicht in einer gemeinsamen Online-Datenbank. Wenn mehrere Freunde dieselbe Live-Statistik auf ihren eigenen Handys sehen sollen, braucht es eine Backend-Datenbank.
- Exportiere gelegentlich eine JSON-Sicherung. Browserdaten löschen kann die gespeicherten Spiele entfernen.
- Bei einem Unentschieden wird kein Sieg vergeben. Die Gewinnquote = Siege / gespielte Matches × 100.
- Für die Doppelstatistik wird jedes Match für jeden beteiligten Spieler gezählt.
