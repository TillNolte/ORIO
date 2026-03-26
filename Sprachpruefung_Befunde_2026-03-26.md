# Sprachpruefung ORIO (2026-03-26)

Scope:
- Alle fachlichen Markdown-Dokumente im Repository
- Beads-Textquellen: `.beads/issues.jsonl`, `.beads/backup/issues.jsonl`, `.beads/backup/events.jsonl`, `.beads/backup/comments.jsonl`, `.beads/backup/labels.jsonl`, `.beads/config.yaml`

Hinweis:
- Ergebnis gewuenscht als reine Fehlerliste mit Fundstellen.
- Dokumentkorrekturen aus Abschnitt A wurden umgesetzt.

## Statusstand (nach Umsetzung von Punkt 1 und 2)

- Abschnitt A (Dokumente): 13 von 13 Befunden behoben.
- Abschnitt B (Beads): weiterhin offen (betrifft vor allem Backup-/Historienquellen unter `.beads/backup/`).
- Notationsvereinheitlichung: US-Referenzen in `Epics/*.md` und `Use_Cases/*.md` auf Format `US-<Nummer>` umgestellt.

## A) Dokumente (Markdown) - verifizierte Befunde

### Hoch
1. `Use_Storys.md:62`
   - Original: `Fehlerstatus pro Geraet setz bar`
   - Befund: Rechtschreibung (`setz bar` -> `setzbar`).

2. `User_Stories/User_Story_07.md:7`
   - Original: `Fehlerstatus pro Geraet setz bar`
   - Befund: Duplikat desselben Rechtschreibfehlers.

3. `Use_Storys.md:347`
   - Original: `moechte ich das bekannte Informationen automatisch vorbelegt werden,`
   - Befund: Grammatik (Artikel/Konstruktion fehlerhaft).

4. `User_Stories/User_Story_36.md:4`
   - Original: `moechte ich das bekannte Informationen automatisch vorbelegt werden,`
   - Befund: Duplikat desselben Grammatikfehlers.

5. `Use_Storys.md:431`
   - Original: `moechte ich dass die Geraetesperre ...`
   - Befund: Interpunktion/Kommasetzung (`..., dass ...`).

6. `User_Stories/User_Story_45.md:4`
   - Original: `moechte ich dass die Geraetesperre ...`
   - Befund: Duplikat desselben Interpunktionsfehlers.

### Mittel
7. `Entitaeten/Entitaet_Role_Operator.md:5`
   - Original: `E-Mail Adresse`
   - Befund: Schreibweise uneinheitlich; normnah `E-Mail-Adresse`.

8. `Entitaeten.md:34`
   - Original: `E-Mail Adresse`
   - Befund: Gleiche Schreibweisen-Inkonsistenz.

9. `Use_Storys.md:89`
   - Original: `Anzahl aktualisierter vs. nicht aktualisierter Geraete`
   - Befund: Stil/Sprachmischung (`vs.`) uneinheitlich im sonst deutsch-formalen Stil.

10. `User_Stories/User_Story_10.md:7`
    - Original: `Anzahl aktualisierter vs. nicht aktualisierter Geraete`
    - Befund: Duplikat derselben Stilabweichung.

11. `Use_Storys.md:110` und `Use_Storys.md:119`
    - Original: Reihenfolge `User Story 14` vor `User Story 13`
    - Befund: Konsistenzbruch in numerischer Story-Reihenfolge.

### Niedrig
12. `Entitaeten.md` und Ordner `Entitaeten/`
    - Original: Gemischte Umlaut-/ae-Schreibweise in Benennung.
    - Befund: Benennungskonsistenz auf Repo-Ebene nicht einheitlich.

13. `Epics/Epic_E01.md:7` und `Use_Cases/UC-01.md:7`
    - Original: `US 1` (mit Leerzeichen) vs. `US1` (ohne Leerzeichen)
    - Befund: Referenznotation nicht einheitlich.

## B) Beads-Issues / Events / Labels - verifizierte Befunde

### Hoch
1. `.beads/backup/issues.jsonl:3` (Issue `ORIO-44x.10`)
   - Original-Auszug: `spA¤ter`, `enthA¤lt`, `GerA¤tehistorie`, `a€¢`
   - Befund: Deutliche Encoding-Artefakte (mojibake), beeintraechtigen Lesbarkeit.

2. `.beads/backup/issues.jsonl:27` (Issue `ORIO-59t.4`)
   - Original-Auszug: `A?berblicken`, `GerA?te`, `mA?glich`, `a??`
   - Befund: Weitere Encoding-Artefakte in Story-Beschreibung/AK.

3. `.beads/backup/events.jsonl:905` (Issue `ORIO-9i8.3`, old_value)
   - Original-Auszug: `GerA?te`, `mA?ssen`, `a??`
   - Befund: Encoding-Artefakte im historischen Event-Payload.

### Mittel
4. `.beads/backup/issues.jsonl:17` und `.beads/backup/issues.jsonl:24`
   - Original: `fuer`, `Frueherkennung`, `ermoeglichen`
   - Befund: `ue/oe/ae`-Transliteration in Altdaten, waehrend aktive Datensaetze in `.beads/issues.jsonl` Umlaute in UTF-8 nutzen. Das ist eine Konsistenzabweichung zwischen Quellen.

5. `.beads/backup/issues.jsonl:63` und `.beads/backup/issues.jsonl:66`
   - Original: `Geraeteliste`
   - Befund: Schreibweisenmix gegenueber der Umlautform in aktiven Issues (z. B. `Geraeteliste` in Backup vs Umlautform in `.beads/issues.jsonl`).

### Niedrig
6. `.beads/backup/comments.jsonl`
   - Befund: Datei ist leer (kein sprachlicher Inhalt pruefbar).

7. `.beads/backup/labels.jsonl`
   - Befund: Labels sind ueberwiegend technisch/englisch (`duplicate`, `user-story`, `implementation`) und konsistent; kein direkter Rechtschreibfehler festgestellt.

## C) Kurzes Fazit

- Die inhaltlich wichtigsten Dokumentfehler liegen in `Use_Storys.md` und den korrespondierenden Dateien unter `User_Stories/` (duplizierte Fehler).
- Bei Beads sind die groessten Qualitaetsprobleme in den Backup-Dateien (`.beads/backup/issues.jsonl`, `.beads/backup/events.jsonl`) und wirken wie Encoding-/Importartefakte.
- Die aktive Datei `.beads/issues.jsonl` ist im Vergleich deutlich sauberer kodiert und sprachlich konsistenter.