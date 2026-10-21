# BlockWelt

Ein Minecraft-ähnliches Voxel-Spiel, das komplett im Browser läuft (Three.js, eine einzige `index.html`).

## ▶️ Jetzt spielen: **[realjonified.github.io/Minecraft](https://realjonified.github.io/Minecraft/)**

Läuft direkt im Browser auf PC, Handy und Tablet, ohne Installation.

Inspiriert vom Original: **[Minecraft](https://www.minecraft.net/de-de)** von Mojang Studios. BlockWelt ist ein inoffizielles Fan-Projekt und steht in keiner Verbindung zu Mojang oder Microsoft.

## Starten

`index.html` doppelklicken – fertig. (Three.js wird per CDN geladen, eine Internetverbindung ist also nötig.)

Alternativ über einen lokalen Server:

```bash
python3 -m http.server
# dann http://localhost:8000 öffnen
```

Über GitHub Pages lässt sich das Spiel auch direkt online spielen (Settings → Pages → Branch auswählen).

## Spielmodi

- **🗡️ Überleben** (Standard für neue Welten): Du startest mit leerem Inventar und musst alles selbst abbauen und herstellen. Blöcke abbauen dauert je nach Härte (gedrückt halten, Risse zeigen den Fortschritt), Spitzhacke, Axt und Schaufel machen es schneller. Stein und Erze lassen nur mit der passenden Spitzhacke etwas fallen (Eisen braucht Stein, Gold/Diamant/Redstone/Smaragd brauchen Eisen, Obsidian braucht Diamant). Dazu Hungerleiste, Ertrinken, Fallschaden – und beim Tod fällt dein Inventar auf den Boden (5 Minuten Zeit, es wieder zu holen). Im Inventar gibt es ein 2×2-Crafting-Feld für Bretter, Stöcke und die Werkbank. Kein Fliegen.
- **🧱 Kreativ**: Alle Blöcke und Items unbegrenzt aus der Auswahl (sortiert nach 🧱 Bauen, 🌲 Natur, 🎨 Farben, 🏮 Deko, 🍎 Items, mit Suchfeld), sofortiges Abbauen, Fliegen (F oder zweimal Leertaste), unverwundbar.

Den Modus wählst du beim Erstellen einer neuen Welt oder jederzeit im Pausenmenü („Spielmodus“).

### Werkzeuge & Abbauzeiten

Spitzhacken, Äxte, Schaufeln, Hacken und Schwerter gibt es aus **Holz, Stein, Eisen, Gold, Diamant und Netherite**. Alle nutzen sich ab (Haltbarkeitsbalken unter dem Symbol) und gehen irgendwann kaputt.

| Spitzhacke | Stein abbauen | Erze (z. B. Eisen) | Kann abbauen | Haltbarkeit |
|---|---|---|---|---|
| Hand | 6 s (ohne Drop) | – | – | – |
| Holz | 6 s | – | Stein, Kohle | 59 |
| Stein | 4 s | 6 s | + Eisen, Lapis | 131 |
| Eisen | 3 s | 6 s | + Gold, Diamant, Redstone, Smaragd | 250 |
| Gold | 2 s | – | Stein, Kohle | 32 |
| Diamant | 1,5 s | 3 s | + Obsidian, Antiker Schutt | 1561 |
| Netherite | 1 s | 2 s | alles | 2031 |

Kein Block braucht länger als **6 Sekunden** zum Abbauen, auch nicht mit der Hand. Einzige Ausnahme ist **Obsidian**. Ohne passendes Werkzeug gibt es aber keinen Drop.

**Netherite:** Antiken Schutt tief im Nether (mit Diamantspitzhacke) abbauen → im Ofen zu Netheriteplatten schmelzen → 4 Platten + 4 Goldbarren = Netheritebarren → Diamant-Werkzeug oder -Rüstung + Netheritebarren in der Werkbank = Netherite-Version. Netherite verbrennt nicht in Lava.

### Rüstung

Helm, Brustpanzer, Beinschutz und Stiefel aus **Leder, Ketten, Eisen, Gold, Diamant und Netherite** – mit Rüstungspunkten und Härte wie im echten Minecraft. Anziehen per Rechtsklick mit der Rüstung in der Hand oder in den Rüstungsplätzen im Inventar. Die Rüstungsleiste erscheint über den Herzen. Rüstung schützt vor Monstern, Explosionen und Lava, aber nicht vor Fallschaden, Ertrinken oder Hunger, und nutzt sich bei Treffern ab. Netherite-Rüstung verringert außerdem den Rückstoß.

**Erste Schritte im Überleben:** Baum abbauen → im Inventar (E) Bretter, Stöcke und eine Werkbank herstellen → Holzspitzhacke → Stein abbauen → Steinwerkzeuge und Ofen → Erze suchen, schmelzen und Fleisch braten.

### Dörfer & Dorfbewohner

In der Oberwelt gibt es **Dörfer** mit Brunnen, Kieswegen, Laternen, Häusern (Werkbank, Ofen, Strohballen drin), Bibliotheken mit Bücherregalen und Feldern mit Kürbissen und Melonen. Neue Welten starten direkt im nächsten Dorf.

Die **Dorfbewohner** laufen im Dorf herum und bleiben stehen, wenn du näher kommst. **Rechtsklick** (Touch: 🧱) auf einen Dorfbewohner öffnet den **Handel**: Du bezahlst mit **Smaragden** (aus Smaragderz in den Bergen) oder verkaufst Dinge, um Smaragde zu bekommen. Je nach Beruf gibt es andere Angebote:

| Beruf | Kleidung | Kauft | Verkauft |
|---|---|---|---|
| Bauer | braun, Strohhut | Kürbisse, Melonen | Brot, Äpfel, Strohballen, Goldener Apfel |
| Bibliothekar | weiß | Bücherregale | Glas, Bücherregale, Leuchtstein, Enderperle, Enderauge |
| Schmied | grau, Schürze | Kohle, Eisenbarren | Eisenspitzhacke, Eisenschwert, Eisenbrustpanzer, Diamantspitzhacke |
| Geistlicher | lila | Verrottetes Fleisch, Goldbarren | Redstone, Lapislazuli, Leuchtstein, Enderperle |
| Metzger | hell, Schürze | rohes Fleisch, Kohle | gebratenes Fleisch, Steak |

Neu ist auch **Brot** (1 Strohballen = 3 Brot in der Werkbank).

### Betten & Schlafen

**Bett** herstellen: 3 Wolle (beliebige Farbe) oben + 3 Holzbretter unten in der Werkbank. Mit Rechtsklick (Touch: 🧱) auf den Boden stellen – das Kopfteil zeigt in deine Blickrichtung. In jedem kleinen Dorfhaus steht auch schon ein Bett.

- **Rechtsklick aufs Bett** setzt deinen **Wiedereinstiegspunkt**: Nach dem Tod wachst du neben deinem Bett auf (solange es noch steht).
- **Nachts** schläfst du darin ein und wachst am **Morgen** auf (im Überleben mit ein paar Herzen mehr). Sind Monster in der Nähe, kannst du nicht schlafen. Wirst du im Schlaf getroffen, wachst du auf.
- Wie im echten Minecraft: Im **Nether und End explodieren Betten**!

### 30 neue Blöcke

| Bauen | Natur | Deko |
|---|---|---|
| Kirsch-, Mangroven-, Bambus-, Karmesin- und Wirrbretter | Kirschholzstamm und **Kirschblätter** (rosa Kirschhaine in der Welt) | **Redstone-Lampe** (leuchtet) |
| Glatter und Gemeißelter Sandstein (mit Creeper-Gesicht) | Packeis und Blaueis | Ockerfarbenes Froschlicht (leuchtet) |
| Quarzziegel, Quarzsäule, Purpursäule | Karmesin-Nyzel und Wirr-Nyzel | Honigwabenblock |
| Rote Netherziegel, Tiefenschieferfliesen | Netherwarzen- und Wirrwarzenblock | **Schleimblock** – man federt darauf zurück und bekommt keinen Fallschaden |
| Geschnittener und Oxidierter Kupferblock | Roter Pilzblock | |
| Kohleblock, Roheisen- und Rohgoldblock | | |

Rezepte (Werkbank): 2×2 Quarzblöcke → 4 Quarzziegel · 2 Quarzblöcke übereinander → 2 Quarzsäulen · 2 Sandstein übereinander → Gemeißelter Sandstein · 2 Purpur übereinander → 2 Purpursäulen · 9 Eis → Packeis · 9 Packeis → Blaueis · 9 Kohle → Kohleblock (und zurück) · 9 Eisen-/Golderz → Roheisen-/Rohgoldblock · 2×2 Kupferblöcke → 4 Geschnittener Kupfer · Netherziegel + Netherwarzenblock → 2 Rote Netherziegel · 2×2 Tiefenschieferziegel → 4 Fliesen · 4 Redstone um Leuchtstein → Redstone-Lampe · Kirschholzstamm → 4 Kirschholzbretter.
Ofen: Sandstein → Glatter Sandstein · Roheisen-/Rohgoldblock → Eisen-/Goldblock · Kupferblock → Oxidierter Kupferblock.

### Sound & Musik

Alle Geräusche werden live im Browser erzeugt (keine Audiodateien): Abbauen, Setzen und Schritte klingen je nach Material (Stein, Holz, Erde, Sand, Kies, Glas, Laub, Wolle) verschieden. Dazu kommen Tiergeräusche (Schwein, Kuh, Schaf, Huhn), Zombies, Creeper-Zischen, Endermen, Ghasts, der Enderdrache und das „Hrmm“ der Dorfbewohner. Außerdem Explosionen, Essen, Aufsammeln, Platschen, Feuerzeug, Portale, Schaden und ruhige Klaviermusik ab und zu. Im Menü lassen sich **🔊 Sound** und **🎵 Musik** getrennt ein- und ausschalten.

## Features

- Unendliche, prozedural generierte Welt (Simplex-Noise mit Seed): Wiesen, Berge mit Schneegipfeln, Strände, Seen und Meere, Höhlen
- Bäume, die über Chunk-Grenzen hinweg wachsen
- **Hochauflösende 128×128-Pixel-Texturen** für alle Blöcke (Mobs mit 64×64), mit Mipmaps gegen Flimmern in der Ferne
- Über 150 Blöcke, u. a. Tropen-, Akazien- und Schwarzeichenholz, polierte Steine, Steinziegel-Varianten, Tiefenschiefer, Tuffstein, Calcit, Basalt, Schwarzstein, Prismarin, Seelaterne, Pilzlicht, Amethyst, Kupfer, Moos, Schwamm, Schlammziegel, Plattenspieler, Notenblock, 16 Farben Beton und 16 Farben Keramik. Dazu Erze (Kohle, Eisen, Gold, Redstone, Lapislazuli, Diamant, Smaragd), Edelsteinblöcke, Birke & Fichte, Bücherregal, Werkbank, Ofen, TNT, Kürbisse, Leuchtstein, 16 Wollfarben und mehr
- Auswahl & Inventar (Taste E bzw. 🎒): jeden Block und jedes Item aus der Auswahl nehmen und in Leiste/Rucksack legen
- Tiere droppen Beute (Fleisch, Leder, Wolle, Federn), Zombies verrottetes Fleisch, Creeper Schwarzpulver – einfach drüberlaufen zum Einsammeln
- Essen heilt (Rechtsklick bzw. 🧱 gedrückt halten). Goldener Apfel und der OP **Verzauberte Goldene Apfel** wie im echten Minecraft: Regeneration II, Absorption IV (goldene Herzen), Resistenz und Feuerresistenz
- **Werkbank** (Rechtsklick drauf): 3×3-Crafting mit Rezeptbuch – ein Tipp auf ein Rezept legt die Zutaten automatisch ein. Bretter, Stöcke, Werkbank, Ofen, Schwerter (Holz bis Diamant), Goldene Äpfel, TNT, Feuerzeug, Erzblöcke und mehr
- **Ofen** (Rechtsklick drauf): oben Zutat, unten Brennstoff (Kohle, Holzkohle, Holz). Brät Fleisch, schmilzt Erze zu Barren, Sand zu Glas, Bruchstein zu Stein, Holz zu Holzkohle … Der Ofen leuchtet, solange er brennt, und arbeitet auch weiter, wenn das Fenster zu ist
- Werkzeuge: Spitzhacke, Axt und Schaufel aus Holz, Stein, Eisen, Gold und Diamant
- Abgebaute Blöcke lassen im Überlebensmodus etwas fallen (Stein → Bruchstein, Kohleerz → Kohle, Diamanterz → Diamant, Kies → manchmal Feuerstein …)
- Schwerter machen mehr Schaden (Holz 5, Stein 6, Eisen 7, Diamant 8)
- TNT: abbauen zündet es, Explosionen lösen Kettenreaktionen aus (Obsidian ist sprengsicher)
- **Der Nether**: Rahmen aus Obsidian bauen (mind. 4×5), mit dem Feuerzeug anzünden, 2 Sekunden reinstellen. Dort warten Netherrack-Höhlen, ein riesiger Lavasee, Seelensand, Magmablöcke, Leuchtstein-Trauben, Netherquarz- und Nethergolderz. Ein Block im Nether entspricht 8 Blöcken in der Oberwelt; auf der anderen Seite wird automatisch ein Portal gebaut
- Nether-Mobs: Zombifizierte Piglins (friedlich, bis man einen schlägt – dann greift die ganze Gruppe an) und Ghasts, die Feuerbälle schießen. Feuerbälle kann man mit einem Schlag zurückschleudern!
- **Feuer**: Das Feuerzeug zündet jetzt richtiges Feuer an. Es frisst Holz, Laub, Wolle und Strohballen, springt über und zündet TNT. Auf Netherrack brennt es ewig, Wasser löscht es. Ghast-Feuerbälle setzen den Boden in Brand
- **Das End**: 12 Endportalrahmen als Ring (5×5 ohne Ecken) legen, in jeden ein Enderauge (Enderperle + Leuchtstein) setzen und ins Portal springen. Dort: schwebende Endstein-Insel über dem Nichts, Obsidian-Säulen mit Endkristallen und der **Enderdrache** mit Bossleiste. Kristalle zerstören (sie heilen den Drachen), Drachen besiegen – dann erscheinen Ausgangsportal und Drachenei
- **Endermen**: im End und selten nachts in der Oberwelt. Nicht in die Augen schauen! Sie teleportieren sich und droppen Enderperlen, die man werfen kann, um sich zu teleportieren
- Lava (auch tief in den Höhlen der Oberwelt) setzt dich in Brand – Feuerresistenz vom Verzauberten Goldenen Apfel schützt
- Neue Landschaft: Dschungel, Savannen mit Akazien, dunkle Wälder, Podsol in Nadelwäldern, grobe Erde, Tiefenschiefer ganz unten, Schwarzstein und Basalt im Nether
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
| Rechtsklick | Block setzen / Essen (gedrückt halten) / mit Dorfbewohnern handeln |
| E | Auswahl & Inventar |
| Mittelklick | Anvisierten Block in die Hotbar übernehmen |
| 1–9 / Mausrad | Block wechseln |
| F | Flugmodus an/aus |
| F3 | Debug-Infos (FPS, Position, Seed) |
| Esc | Pause |

Auf Handy und Tablet: Joystick links zum Laufen, Wischen zum Umsehen, ⛏ abbauen/schlagen, 🧱 platzieren, ⬆ springen, ⬇ runterfliegen, ✈ Flugmodus, 🎒 Auswahl & Inventar, ⏸ Pause. 🧱 mit Essen in der Hand gedrückt halten = essen.
