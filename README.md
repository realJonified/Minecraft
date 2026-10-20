# BlockWelt

Ein Minecraft-ähnliches Voxel-Spiel, das komplett im Browser läuft (Three.js, eine einzige `index.html`).

## Starten

`index.html` doppelklicken – fertig. (Three.js wird per CDN geladen, eine Internetverbindung ist also nötig.)

Alternativ über einen lokalen Server:

```bash
python3 -m http.server
# dann http://localhost:8000 öffnen
```

Über GitHub Pages lässt sich das Spiel auch direkt online spielen (Settings → Pages → Branch auswählen).

## Features

- Unendliche, prozedural generierte Welt (Simplex-Noise mit Seed): Wiesen, Berge mit Schneegipfeln, Strände, Seen und Meere, Höhlen
- Bäume, die über Chunk-Grenzen hinweg wachsen
- Blöcke abbauen und setzen (Gras, Erde, Stein, Bruchstein, Bretter, Holz, Glas, Ziegel, Sand, Laub, Schnee)
- Spielerphysik mit Schwerkraft, Springen, Kollision, Schwimmen und Sprinten
- Flugmodus
- Tag/Nacht-Zyklus mit Sonne, Mond und ziehenden Wolken
- Ambient Occlusion für den typischen weichen Schatten-Look
- Alle Texturen werden prozedural im Code gezeichnet (keine Bilddateien)
- Automatisches Speichern im Browser (localStorage): Welt-Änderungen, Position, Uhrzeit

## Steuerung

| Taste | Aktion |
|---|---|
| W A S D | Laufen |
| Maus | Umsehen |
| Leertaste | Springen / Schwimmen / Hochfliegen |
| Shift | Sprinten / Runterfliegen |
| Linksklick | Block abbauen (gedrückt halten für mehrere) |
| Rechtsklick | Block setzen |
| Mittelklick | Anvisierten Block in die Hotbar übernehmen |
| 1–9 / Mausrad | Block wechseln |
| F | Flugmodus an/aus |
| F3 | Debug-Infos (FPS, Position, Seed) |
| Esc | Pause |
