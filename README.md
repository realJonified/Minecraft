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
- Über 65 Blöcke mit eigenen 16×16-Pixel-Texturen: Erze (Kohle, Eisen, Gold, Redstone, Lapislazuli, Diamant, Smaragd), Edelsteinblöcke, Birke & Fichte, Bücherregal, Werkbank, Ofen, TNT, Kürbisse, Leuchtstein, 16 Wollfarben und mehr
- Auswahl & Inventar (Taste E bzw. 🎒): jeden Block und jedes Item aus der Auswahl nehmen und in Leiste/Rucksack legen
- Tiere droppen Beute (Fleisch, Leder, Wolle, Federn), Zombies verrottetes Fleisch, Creeper Schwarzpulver – einfach drüberlaufen zum Einsammeln
- Essen heilt (Rechtsklick bzw. 🧱 gedrückt halten). Goldener Apfel und der OP **Verzauberte Goldene Apfel** wie im echten Minecraft: Regeneration II, Absorption IV (goldene Herzen), Resistenz und Feuerresistenz
- TNT: abbauen zündet es, Explosionen lösen Kettenreaktionen aus (Obsidian ist sprengsicher)
- Erzadern, Granit/Diorit/Andesit, Kies- und Tonböden im Meer, Sandstein unter Stränden
- Spielerphysik mit Schwerkraft, Springen, Kollision, Schwimmen und Sprinten
- Flugmodus
- Tiere: Schweine, Kühe, Schafe und Hühner laufen in kleinen Herden herum und flüchten, wenn man sie schlägt
- Monster in der Nacht: Zombies jagen dich (und verbrennen in der Sonne), Creeper schleichen sich an und explodieren
- Lebensanzeige mit Herzen, Fallschaden, Regeneration, Tod und Wiederbeleben
- Friedlicher Modus im Menü („Monster: Aus“)
- Touch-Steuerung für Handy und Tablet (Joystick, Wischen zum Umsehen, Buttons)
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
| Linksklick | Block abbauen / Tier oder Monster schlagen (gedrückt halten für mehrere) |
| Rechtsklick | Block setzen / Essen (gedrückt halten) |
| E | Auswahl & Inventar |
| Mittelklick | Anvisierten Block in die Hotbar übernehmen |
| 1–9 / Mausrad | Block wechseln |
| F | Flugmodus an/aus |
| F3 | Debug-Infos (FPS, Position, Seed) |
| Esc | Pause |

Auf Handy und Tablet: Joystick links zum Laufen, Wischen zum Umsehen, ⛏ abbauen/schlagen, 🧱 platzieren, ⬆ springen, ⬇ runterfliegen, ✈ Flugmodus, 🎒 Auswahl & Inventar, ⏸ Pause. 🧱 mit Essen in der Hand gedrückt halten = essen.
