# Agent-Anweisungen

Dieses Projekt verwendet **bd** (beads) für das Issue-Tracking. Führe `bd onboard` aus, um zu starten.

## Schnellreferenz

```bash
bd ready              # Verfügbare Arbeit finden
bd show <id>          # Issue-Details anzeigen
bd update <id> --status in_progress  # Arbeit übernehmen
bd close <id>         # Arbeit abschließen
bd vc status          # Dolt-basierte beads-Änderungen prüfen
bd vc commit -m "update beads data"  # beads-Änderungen committen, falls nötig
```

## Landung Abschließen (Sitzungsende)

**Beim Beenden einer Arbeitssitzung** MÜSSEN alle folgenden Schritte abgeschlossen werden. Die Arbeit ist NICHT fertig, bis `git push` erfolgreich war.

**VERBINDLICHER ABLAUF:**

1. **Issues für verbleibende Arbeit anlegen** - Erstelle Issues für alles, was nachverfolgt werden muss
2. **Qualitätsprüfungen ausführen** (wenn Code geändert wurde) - Tests, Linter, Builds
3. **Issue-Status aktualisieren** - Abgeschlossene Arbeit schließen, laufende Arbeit aktualisieren
4. **IN DAS REMOTE PUSHEN** - Das ist VERPFLICHTEND:

   ```bash
   git pull --rebase
   bd vc status
   bd vc commit -m "update beads data"  # falls bd-Änderungen ausstehen
   git push
   git status  # MUSS "up to date with origin" anzeigen
   ```

5. **Aufräumen** - Stashes leeren, Remote-Branches bereinigen
6. **Verifizieren** - Alle Änderungen sind committed UND gepusht
7. **Übergabe** - Kontext für die nächste Sitzung bereitstellen

**KRITISCHE REGELN:**

- Die Arbeit ist NICHT fertig, bis `git push` erfolgreich war
- NIEMALS vor dem Push stoppen - sonst bleiben Änderungen lokal liegen
- NIEMALS sagen "ready to push when you are" - DU musst pushen
- Falls Push fehlschlägt, Problem beheben und erneut versuchen, bis es klappt
