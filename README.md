# ORIO

ORIO ist ein Projekt zur strukturierten Planung, Durchführung und Dokumentation von Windows-Update-Rollouts in einer Gerätelandschaft.

## Ziel

Das Projekt schafft Transparenz über den Update-Status aller Geräte, reduziert manuelle Fehler und unterstützt Teams bei einer nachvollziehbaren, priorisierten Abarbeitung.

## Inhalte im Repository

- `Use_Storys.md`: Gesamtliste der User Stories
- `Epics.md`: Fachliche Gruppierung der User Stories in Epics
- `Use_Cases/`: Detaillierte Use Cases
- `User_Stories/`: Einzelbeschreibungen je User Story
- `Entitäten/` und `Entitäten.md`: Fachliche Entitäten
- `.beads/`: Issue-Tracking-Daten für `bd` (beads)

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

## Schnellstart

1. Repository klonen
2. Im Projektordner arbeiten
3. `bd prime` ausführen, um aktuellen Workflow-Kontext zu sehen
4. Mit `bd ready` die nächste umsetzbare Aufgabe auswählen

## Aktueller Stand

Die User Stories aus `Use_Storys.md` sind als `bd`-Tasks (`US-01` bis `US-68`) unter den Epics (`E1` bis `E13`) angelegt. Die früheren `IT-*`-Implementierungsaufgaben bleiben im Tracker nur noch als ersetzte Referenz erhalten.
