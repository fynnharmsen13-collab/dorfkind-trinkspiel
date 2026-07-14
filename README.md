# 🚜 Dorfkind – Das Trinkspiel

Ein deutsches Trinkspiel mit Dorf-Charme, das eine Gruppe einen ganzen Abend bei Laune hält.
Gebaut als **self-contained PWA**: reines HTML/CSS/Vanilla-JS, **kein Build-Step**, läuft komplett **offline**.

## Was ist das?
Trecker, Feuerwehrfest, Dorfdisco, Bolzplatz, Güllewagen und Vokuhila – der ganze Landjugend-Humor in einer App fürs Handy. 6 Spielmodi, über 240 einzigartige Karten/Aussagen, verspielter Landidylle-Look (Bier-Amber, Heu-Gold, Feldgrün), haptisches Feedback und flüssige Karten-Animationen.

## Modi
1. **🍺 Hauptdeck** (Kernmodus) – endloser Kartenstapel, gewichtete Mischung aller Kategorien, kein schnelles Wiederholen. Tippen oder wischen = nächste Karte.
2. **🙈 Ich hab noch nie …** (Dorf-Edition)
3. **👉 Wer würde eher …**
4. **⏱️ Kategorien** – reihum aufzählen, mit optionalem Timer.
5. **💣 Tick-Tick-Bumm** – Handy rumgeben, versteckter Timer (10–40 s), beim Bumm in der Hand = trinken.
6. **📜 Regel-Karten** – Dauer-Regeln für den ganzen Abend; aktive Regeln jederzeit über die 📜-Leiste sichtbar.

## Einstellungen
- **Zahm-Modus** (filtert derbere/persönlichere Karten)
- **Trink-Intensität** (mild / normal / heftig – skaliert die Schluck-Mengen)
- **Vibration** an/aus
- **Spieler verwalten** (2–12)
- **Reset**

## Starten
- **Am PC:** Einfach `index.html` im Browser öffnen. Läuft direkt, auch offline.
- **Aufs Handy holen (empfohlen):**
  1. Dateien auf einen kleinen Webserver/Webspace legen **oder** lokal per `python -m http.server` im Ordner starten und die Adresse am Handy öffnen (gleiches WLAN).
  2. Im Handy-Browser über das Teilen-/Menü-Symbol **„Zum Home-Bildschirm hinzufügen"** wählen.
  3. Ab dann startet „Dorfkind" wie eine echte App im Vollbild und funktioniert **offline**.
- Reines Datei-Öffnen (`file://`) funktioniert ebenfalls; nur der Service-Worker-Offline-Cache greift erst über `http(s)://` – die App selbst braucht ohnehin kein Netz.

## Dateien
- `index.html` – die komplette App (Logik, Content, Design, alles inline)
- `manifest.webmanifest` – PWA-Manifest
- `sw.js` – Service Worker (Offline-Cache)
- `icons/icon-192.svg`, `icons/icon-512.svg` – App-Icons

## Content-Umfang
- Hauptdeck: **130** Karten über 8 Kategorien (Trinken, Aufgabe, Ansage, Gruppe, Duell, Wahrheit, Abstimmung, Wildcard)
- Ich hab noch nie: **44** · Wer würde eher: **32** · Kategorien: **28** · Dauer-Regeln: **16**

Speicherort: `D:\Projekte\Dorfkind-Trinkspiel\` · Zustand wird in `localStorage` gespeichert.
