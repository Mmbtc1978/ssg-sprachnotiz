# SSG Cockpit (Stand 17.11.2026)

Installierbare Web-App: Dashboard, Steckbriefe, Gewerke und Sprachnotiz in einer App.
Alle Report- und Steckbriefdaten sind erfundene Beispieldaten (Datenstand 2027-03), Hausnamen neutral.

## Dateien (alle sechs gehören zusammen in denselben Ordner)

| Datei | Zweck |
|---|---|
| `index.html` | die App (ersetzt die bisherige index.html im Repo) |
| `manifest.webmanifest` | Name, Farben und Icons für die Installation |
| `sw.js` | Zwischenspeicher, damit die App ohne Netz startet |
| `icon-192.png`, `icon-512.png`, `icon-maskable-512.png` | App-Icons |

## Einbau

1. Im GitHub-Repo `ssg-sprachnotiz` „Add file › Upload files“, alle sechs Dateien hochladen, „Commit changes“.
2. Ein bis zwei Minuten warten, dann die bekannte Adresse am Handy in Chrome öffnen und einmal neu laden.
3. Menü (drei Punkte) › „App installieren“ bzw. „Zum Startbildschirm hinzufügen“. Auf der Übersicht erscheint dafür auch ein eigener Knopf.

API-Key und Einstellungen bleiben erhalten, solange die Adresse dieselbe ist.

## Vorführung

Mikrofon-Knopf › „Beispieldiktat einsetzen“ › „Strukturieren“ › „In Steckbrief übernehmen“. Das Beispiel läuft ohne Internet.
Eigenes Diktat braucht Internet und den API-Key. Zurücksetzen: Zahnrad › „Sprachnotizen zurücksetzen“.

## Bei späteren Änderungen

In `sw.js` die Zeile `const CACHE = "ssg-cockpit-v1"` hochzählen (v2, v3 …), damit das Handy die neue Fassung lädt.

## Echte Hausnamen

Nur lokal am Gerät: Zahnrad › Häuser, je Zeile `H02;Name`. Die Namen stehen dann nicht im öffentlichen Repo.
