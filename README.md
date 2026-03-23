# ORIO

ORIO ist ein Projekt zur strukturierten Planung, Durchfuehrung und Dokumentation von Windows-Update-Rollouts in einer Geraetelandschaft.

## Ziel

Das Projekt schafft Transparenz ueber den Update-Status aller Geraete, reduziert manuelle Fehler und unterstuetzt Teams bei einer nachvollziehbaren, priorisierten Abarbeitung.

## Inhalte im Repository

- `Use_Storys.md`: Gesamtliste der User Stories
- `Epics.md`: Fachliche Gruppierung der User Stories in Epics
- `Use_Cases/`: Detaillierte Use Cases
- `User_Stories/`: Einzelbeschreibungen je User Story
- `Entitaeten/` und `Entitaeten.md`: Fachliche Entitaeten
- `.beads/`: Issue-Tracking-Daten fuer `bd` (beads)

## Arbeitsweise (Issue Tracking mit bd)

Dieses Projekt nutzt `bd` fuer Aufgabenverwaltung.

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
3. `bd prime` ausfuehren, um aktuellen Workflow-Kontext zu sehen
4. Mit `bd ready` die naechste umsetzbare Aufgabe auswaehlen

## Aktueller Stand

Die aus den User Stories abgeleiteten Implementierungsaufgaben wurden als `bd`-Tasks (`IT-01` bis `IT-30`) angelegt und Epics (`E1` bis `E13`) zugeordnet.

