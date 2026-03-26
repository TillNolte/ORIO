# ORIO

ORIO ist ein Projekt zur strukturierten Planung, Durchführung und Dokumentation von Windows-Update-Rollouts in einer Gerätelandschaft.

Lizenz: Creative Commons BY-NC 4.0 (siehe `LICENSE`).

## Ziel

Das Projekt schafft Transparenz über den Update-Status aller Geräte, reduziert manuelle Fehler und unterstützt Teams bei einer nachvollziehbaren, priorisierten Abarbeitung.

## Zielgruppe

Diese Dokumentation richtet sich an Teams, die Windows-Update-Rollouts planen, koordinieren, umsetzen und nachverfolgbar dokumentieren.

## Scope

In Scope:
- Fachliche Beschreibung von Anforderungen, Abläufen und Arbeitspaketen rund um Update-Rollouts
- Strukturierung über Epics, User Stories und Use Cases
- Aufgabensteuerung mit `bd` (beads)

Out of Scope:
- Ausführbare Softwarekomponenten oder Automatisierungsskripte in diesem Repository
- Technische Betriebsdokumentation einzelner Tools außerhalb des hier definierten Fachkontexts

## Inhalte im Repository

- `Use_Storys.md`: Gesamtliste der User Stories
- `Epics.md`: Fachliche Gruppierung der User Stories in Epics
- `Use_Cases/`: Detaillierte Use Cases
- `User_Stories/`: Einzelbeschreibungen je User Story
- `Entitäten/` und `Entitäten.md`: Fachliche Entitäten
- `.beads/`: Issue-Tracking-Daten für `bd` (beads)

Hinweis zur Benennung: Im Repository existieren sowohl `Entitäten.md` als auch der Ordner `Entitaeten/`. Diese Schreibweise ist aktuell historisch gewachsen.

## Lesereihenfolge (empfohlen)

1. `Use_Storys.md` - Überblick über alle Stories
2. `Epics.md` - Fachliche Bündelung und Priorisierung
3. `Use_Cases/` - Ablauf- und Interaktionssicht
4. `User_Stories/` - Detaillierte Einzelanforderungen
5. `Entitäten.md` und `Entitaeten/` - Fachobjekte und Begriffe

## Voraussetzungen

- Git installiert
- `bd` (beads) installiert und im PATH verfügbar
- Schreibrechte im Repository (für Issue- und Dokumentationspflege)

Optional:
- GitHub-Zugang für Zusammenarbeit über Remote-Repository

## Arbeitsweise (Issue Tracking mit bd)

Dieses Projekt nutzt `bd` für Aufgabenverwaltung.

Wichtige Befehle:

```bash
bd ready
bd show <id>
bd update <id> --status in_progress
bd close <id>
bd sync
```

Zur Erstinitialisierung (falls noch nicht erfolgt):

```bash
bd onboard
```

## Schnellstart

1. Repository klonen
2. Im Projektordner arbeiten
3. `bd prime` ausführen, um aktuellen Workflow-Kontext zu sehen
4. Mit `bd ready` die nächste umsetzbare Aufgabe auswählen

## Beitrag leisten (Contribution)

1. Aufgabe mit `bd ready` auswählen
2. Details mit `bd show <id>` prüfen
3. Status auf `in_progress` setzen
4. Fachliche Änderungen in den passenden Markdown-Dateien umsetzen
5. Änderungen in Git committen und mit `bd sync` abgleichen
6. Aufgabe mit `bd close <id>` abschließen

Empfehlung vor Abschluss:
- Konsistenz der Begriffe in `User_Stories/`, `Use_Cases/`, `Epics.md` und Entitäten-Dokumenten prüfen
- Verweise auf IDs (`US-*`, `UC-*`, `E*`) gegenprüfen

## Haeufige Stolperfallen

- Uneinheitliche Begriffe zwischen User Stories, Use Cases und Entitaeten
	Gegenmassnahme: Vor dem Abschluss zentrale Begriffe in allen betroffenen Dateien querpruefen.
- Falsche oder fehlende ID-Referenzen (`US-*`, `UC-*`, `E*`)
	Gegenmassnahme: Jede neu eingefuegte Referenz einmal gegen die Quelldatei pruefen.
- Aufgabe in `bd` begonnen, aber Status nicht aktualisiert
	Gegenmassnahme: Direkt nach Start `bd update <id> --status in_progress` ausfuehren.
- Aenderungen gemacht, aber nicht mit `bd` synchronisiert
	Gegenmassnahme: Nach Commit `bd sync` in den Standardablauf aufnehmen.
- Verwechslung bei historisch gewachsener Benennung (`Entitäten.md` vs. `Entitaeten/`)
	Gegenmassnahme: Beim Verlinken bewusst auf den exakten Dateinamen bzw. Ordnernamen achten.

## Aktueller Stand

Die User Stories aus `Use_Storys.md` sind als `bd`-Tasks (`US-01` bis `US-68`) unter den Epics (`E1` bis `E13`) angelegt. Die früheren `IT-*`-Implementierungsaufgaben bleiben im Tracker nur noch als ersetzte Referenz erhalten.

## Kontakt

Repository Owner: TillNolte

## Lizenz

Die Inhalte dieses Repositorys stehen unter der Lizenz `Creative Commons BY-NC 4.0`.

Kurz gesagt:
- Weitergabe und Bearbeitung sind erlaubt
- Namensnennung ist erforderlich
- Kommerzielle Nutzung ist nicht erlaubt

Details siehe `LICENSE` oder:
https://creativecommons.org/licenses/by-nc/4.0/