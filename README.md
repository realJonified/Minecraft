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
- **Werkbank** (Rechtsklick drauf): 3×3-Crafting mit Rezeptbuch – ein Tipp auf ein Rezept legt die Zutaten automatisch ein. Bretter, Stöcke, Werkbank, Ofen, Schwerter (Holz bis Diamant), Goldene Äpfel, TNT, Feuerzeug, Erzblöcke und mehr
- **Ofen** (Rechtsklick drauf): oben Zutat, unten Brennstoff (Kohle, Holzkohle, Holz). Brät Fleisch, schmilzt Erze zu Barren, Sand zu Glas, Bruchstein zu Stein, Holz zu Holzkohle … Der Ofen leuchtet, solange er brennt, und arbeitet auch weiter, wenn das Fenster zu ist
- Abgebaute Blöcke lassen etwas fallen (Stein → Bruchstein, Kohleerz → Kohle, Diamanterz → Diamant, Kies → manchmal Feuerstein …)
- Schwerter machen mehr Schaden (Holz 5, Stein 6, Eisen 7, Diamant 8)
- TNT: abbauen zündet es, Explosionen lösen Kettenreaktionen aus (Obsidian ist sprengsicher)
- **Der Nether**: Rahmen aus Obsidian bauen (mind. 4×5), mit dem Feuerzeug anzünden, 2 Sekunden reinstellen. Dort warten Netherrack-Höhlen, ein riesiger Lavasee, Seelensand, Magmablöcke, Leuchtstein-Trauben, Netherquarz- und Nethergolderz. Ein Block im Nether entspricht 8 Blöcken in der Oberwelt; auf der anderen Seite wird automatisch ein Portal gebaut
- Nether-Mobs: Zombifizierte Piglins (friedlich, bis man einen schlägt – dann greift die ganze Gruppe an) und Ghasts, die Feuerbälle schießen. Feuerbälle kann man mit einem Schlag zurückschleudern!
- **Feuer**: Das Feuerzeug zündet jetzt richtiges Feuer an. Es frisst Holz, Laub, Wolle und Strohballen, springt über und zündet TNT. Auf Netherrack brennt es ewig, Wasser löscht es. Ghast-Feuerbälle setzen den Boden in Brand
- **Das End**: 12 Endportalrahmen als Ring (5×5 ohne Ecken) legen, in jeden ein Enderauge (Enderperle + Leuchtstein) setzen und ins Portal springen. Dort: schwebende Endstein-Insel über dem Nichts, Obsidian-Säulen mit Endkristallen und der **Enderdrache** mit Bossleiste. Kristalle zerstören (sie heilen den Drachen), Drachen besiegen – dann erscheinen Ausgangsportal und Drachenei
- **Endermen**: im End und selten nachts in der Oberwelt. Nicht in die Augen schauen! Sie teleportieren sich und droppen Enderperlen, die man werfen kann, um sich zu teleportieren
- Lava (auch tief in den Höhlen der Oberwelt) setzt dich in Brand – Feuerresistenz vom Verzauberten Goldenen Apfel schützt
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
