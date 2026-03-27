# Use-Stories (68)

User Story 1: Geräteliste mit Update-Status anzeigen
Als Operator
möchte ich eine zentrale Übersicht aller Windows-Clients mit aktuellem Update-Status sehen,
damit ich gezielt entscheiden kann, welche Geräte noch aktualisiert werden müssen.
Akzeptanzkriterien:
    • Geräteübersicht zeigt Hostname, OS-Version, Build, IP-Adresse, Gerätetyp und Standort
    • Update-Status (z. B. „Nicht aktualisiert“, „In Arbeit“, „25H2 abgeschlossen“) ist sichtbar
    • Filter nach Standort, Gerätetyp und Status sind möglich

User Story 2: Gerätebestand importieren
Als Operator
möchte ich eine Liste aller PCs importieren können,
damit ich eine zentrale Datenbasis für die Updateplanung habe.
Akzeptanzkriterien:
    • Import von CSV/Excel-Dateien möglich
    • Pflichtfelder: Hostname, Standort, Gerätetyp
    • Fehlerhafte Datensätze werden angezeigt und nicht importiert

User Story 3: Geräte nach Standort organisieren
Als Operator
möchte ich Geräte nach Standort oder Raum filtern können,
damit ich Updates vor Ort effizient planen kann.
Akzeptanzkriterien:
    • Standort/Raum ist pro Gerät gepflegt
    • Filter- und Sortierfunktion nach Standort vorhanden
    • Standort wird in Reports übernommen

User Story 4: Windows-Version per PowerShell prüfen
Als Operator
möchte ich die aktuelle Windows-Version eines Geräts automatisch per PowerShell prüfen,
damit ich nicht manuell mit winver arbeiten muss.
Akzeptanzkriterien:
    • PowerShell-Skript ermittelt OS-Version und Build
    • Ergebnis wird im Gerätedatensatz gespeichert
    • Erkennbar, ob Gerät updatepflichtig ist

User Story 5: Geräte mit veralteter Version hervorheben
Als Operator
möchte ich Geräte mit einer älteren Windows-Version visuell hervorheben,
damit ich Prioritäten setzen kann.
Akzeptanzkriterien:
    • Geräte unterhalb von 25H2 sind klar markiert
    • Definition der Zielversion (25H2) ist zentral konfigurierbar
    • Sortierung nach Versionsstand möglich

User Story 6: Update manuell als abgeschlossen markieren
Als Operator
möchte ich ein Gerät nach erfolgreichem Update als „25H2 aktualisiert“ markieren,
damit ich den Fortschritt dokumentieren kann.
Akzeptanzkriterien:
    • Nachprüfung der Version (Build) kann dokumentiert werden
    • Datum, Uhrzeit und Operator werden automatisch gespeichert
    • Optionaler Kommentar (z. B. Raum, Besonderheiten)

User Story 7: Update-Probleme dokumentieren
Als Operator
möchte ich Fehler oder Probleme während eines Updates erfassen,
damit ich sie später nachvollziehen und beheben kann.
Akzeptanzkriterien:
    • Fehlerstatus pro Gerät setzbar
    • Freitextfeld zur Fehlerbeschreibung vorhanden
    • Fehler bleiben in der Gerätehistorie sichtbar

User Story 8: Benachrichtigung bei Update-Fehlern
Als Operator
möchte ich bei einem Update-Fehler benachrichtigt werden,
damit ich zeitnah reagieren kann.
Akzeptanzkriterien:
    • In-App- oder E-Mail-Benachrichtigung bei Fehlerstatus
    • Fehlerübersicht mit offenen Fällen vorhanden
    • Verknüpfung zur betroffenen Geräteansicht

User Story 9: Update-Historie pro Gerät einsehen
Als Operator
möchte ich die vollständige Update-Historie eines Geräts sehen,
damit ich alle Änderungen nachvollziehen kann.
Akzeptanzkriterien:
    • Chronologische Timeline pro Gerät
    • Jeder Eintrag enthält Datum, Operator, Status und Kommentar
    • Fehlgeschlagene Updates bleiben sichtbar

User Story 10: Update-Status-Dashboard anzeigen
Als Operator
möchte ich ein Dashboard mit dem Gesamtstatus aller Geräte sehen,
damit ich den Fortschritt schnell überblicken kann.
Akzeptanzkriterien:
    • Anzahl aktualisierter gegenüber nicht aktualisierten Geräten
    • Anzeige nach Standort möglich
    • Automatische Aktualisierung der Daten

User Story 11: Reports exportieren
Als Operator
möchte ich Update-Daten als Excel- oder CSV-Datei exportieren,
damit ich sie extern weiterverwenden oder archivieren kann.
Akzeptanzkriterien:
    • Export enthält Gerätedaten, Update-Status, Zeitpunkte und Operator
    • Filter (z. B. Zeitraum, Standort) vor Export möglich
    • Excel- und CSV-Format unterstützt

User Story 12: Rollenbasierte Zugriffssteuerung
Als Administrator
möchte ich Benutzerrollen mit unterschiedlichen Rechten verwalten,
damit ich Zugriff und Verantwortlichkeiten steuern kann.
Akzeptanzkriterien:
    • Rollen: Admin, Operator, Viewer
    • Rechte beeinflussen Sichtbarkeit und Bearbeitungsmöglichkeiten
    • Änderungen werden protokolliert

User Story 13: Geräte als „Update ausgeschlossen“ markieren
Als Operator
möchte ich Geräte als „Update ausgeschlossen“ markieren können,
damit ich alte PCs, die ersetzt werden müssen, klar vom Update-Prozess ausschließe.
Akzeptanzkriterien:
    • Es gibt einen expliziten Status „Update ausgeschlossen“
    • Ausgeschlossene Geräte werden nicht als updatepflichtig angezeigt
    • Der Ausschlussstatus ist in der Geräteübersicht sichtbar
    • Ein Kommentar (z. B. „Gerät zu alt – Ersatz geplant“) ist verpflichtend

User Story 14: Begründung für Update-Ausschluss dokumentieren
Als Operator
möchte ich beim Ausschließen eines Geräts den Grund dokumentieren,
damit ich später nachvollziehen kann, warum kein Update durchgeführt wurde.
Akzeptanzkriterien:
    • Beim Setzen des Status „Update ausgeschlossen“ ist ein Begründungsfeld erforderlich
    • Begründung wird dauerhaft im Gerätedatensatz gespeichert
    • Begründung ist im Export und in der Historie sichtbar

User Story 15: Speicherplatzprüfung vor lokalem ISO-Kopieren
Als Operator
möchte ich vor dem Kopieren der ISO-Datei prüfen können, ob genügend Speicherplatz vorhanden ist,
damit ich Update-Abbrüche aufgrund von Platzmangel vermeide.
Akzeptanzkriterien:
    • Prüfung erfolgt nur, wenn „ISO lokal speichern“ ausgewählt wird
    • Mindestfreier Speicherplatz: 8.637.632 KB
    • Ergebnis wird klar angezeigt („Ausreichend“ / „Nicht ausreichend“)
    • Prüfungsergebnis wird dokumentiert

User Story 16: Warnhinweis bei unzureichendem Speicherplatz
Als Operator
möchte ich bei zu wenig Speicherplatz einen klaren Warnhinweis erhalten,
damit ich das Update nicht versehentlich starte.
Akzeptanzkriterien:
    • Deutlicher Warnhinweis bei Unterschreitung des Mindestplatzes
    • Update-Fortsetzung ist ohne ausreichenden Speicherplatz nicht möglich
    • Hinweis enthält den benötigten und den verfügbaren Speicherplatz

User Story 17: Update-Quelle „USB-Stick“ festlegen
Als Operator
möchte ich die Update-Quelle eindeutig auf „USB-Stick“ festlegen,
damit der Update-Prozess standardisiert und fehlerfrei abläuft.
Akzeptanzkriterien:
    • Update-Quelle ist fest auf „USB-Stick“ definiert
    • Andere Update-Quellen sind nicht auswählbar
    • Die verwendete Update-Quelle wird im Update-Protokoll dokumentiert

User Story 18: USB-basierte Updates eindeutig kennzeichnen
Als Operator
möchte ich erkennen können, dass ein Update per USB durchgeführt wurde,
damit ich den Prozess später nachvollziehen kann.
Akzeptanzkriterien:
    • Update-Protokoll enthält den Eintrag „Update-Quelle: USB“
    • Information ist in der Gerätehistorie sichtbar
    • Export enthält die Update-Quelle

User Story 20: Standardablauf für Windows-Update dokumentieren
Als Operator
möchte ich einen fest definierten Standardablauf für Windows-Updates nutzen,
damit ich jeden PC nach dem gleichen, nachvollziehbaren Prozess aktualisiere.
Akzeptanzkriterien:
    • Der Standardablauf besteht aus:
        1. Prüfen der installierten Windows-Version
        2. Anschließen des USB-Sticks mit ISO
        3. Öffnen der ISO-Datei
        4. Ausführen der inplace.cmd
        5. Erneute Versionsprüfung nach dem Update
    • Der Ablauf ist als Referenz in der Applikation hinterlegt
    • Der Ablauf ist für alle Operatoren identisch

User Story 19: Ausgeschlossene Geräte im Reporting berücksichtigen
Als Operator
möchte ich ausgeschlossene Geräte im Reporting separat sehen,
damit ich den tatsächlichen Update-Fortschritt korrekt bewerten kann.
Akzeptanzkriterien:
    • Reports unterscheiden zwischen:
        ○ aktualisiert
        ○ offen
        ○ fehlgeschlagen
        ○ update ausgeschlossen
    • Ausgeschlossene Geräte verfälschen nicht die Update-Quote
    • Filter „Ausgeschlossene Geräte anzeigen“ vorhanden

User Story 21: Bearbeitungsstatus eines PCs erfassen
Als Operator
möchte ich dokumentieren können, ob ein PC bearbeitet wurde (Ja/Nein),
damit ich erkenne, welche Geräte bereits angefasst wurden.
Akzeptanzkriterien:
    • Feld „PC bearbeitet“ mit den Werten Ja / Nein
    • Der Status ist in der Geräteübersicht sichtbar
    • Änderung des Status wird mit Datum und Operator gespeichert

User Story 22: Abschlussstatus „Update fertig“ erfassen
Als Operator
möchte ich dokumentieren können, ob ein PC vollständig auf 25H2 aktualisiert wurde,
damit ich den Update-Erfolg eindeutig festhalten kann.
Akzeptanzkriterien:
    • Feld „Update abgeschlossen“ mit den Werten Ja / Nein
    • „Ja“ darf nur gesetzt werden, wenn die Zielversion (25H2) bestätigt wurde
    • Abschlussstatus ist in Übersicht und Reporting sichtbar

User Story 23: Post-Update-Checkliste anzeigen
Als Operator
möchte ich nach einem Update eine Checkliste angezeigt bekommen,
damit ich sicherstelle, dass alle erforderlichen Nacharbeiten erledigt sind.
Akzeptanzkriterien:
    • Checkliste wird nach dem Update angezeigt
    • Inhalte der Checkliste sind vordefiniert
    • Jeder Punkt kann als erledigt markiert werden
    • Die Checkliste ist optional, aber empfohlen

User Story 24: Abschluss der Checkliste dokumentieren
Als Operator
möchte ich den Abschluss der Post-Update-Checkliste dokumentieren,
damit ich nachvollziehen kann, dass das Gerät vollständig geprüft wurde.
Akzeptanzkriterien:
    • Status „Checkliste abgeschlossen: Ja/Nein“
    • Zeitstempel und Operator werden gespeichert
    • Status ist in der Gerätehistorie sichtbar

User Story 25: Abgebrochenes Update kennzeichnen
Als Operator
möchte ich ein Update als „abgebrochen“ kennzeichnen können,
damit klar ist, dass der Prozess nicht erfolgreich abgeschlossen wurde.
Akzeptanzkriterien:
    • Status „Update abgebrochen“ verfügbar
    • Abbruchstatus setzt „Update abgeschlossen“ automatisch auf „Nein“
    • Optionaler Kommentar zum Abbruch möglich

User Story 26: Neustart des Update-Prozesses erzwingen
Als Operator
möchte ich nach einem Abbruch den Update-Prozess vollständig neu starten,
damit der Standardablauf wieder von Anfang an eingehalten wird.
Akzeptanzkriterien:
    • Bei Neustart werden vorherige Update-Versuche nicht als abgeschlossen gewertet
    • Historie zeigt frühere Abbrüche weiterhin an
    • Der PC gilt wieder als „nicht aktualisiert“

User Story 27: Fehler während des Updates erfassen
Als Operator
möchte ich während oder nach einem Update einen Fehler erfassen können,
damit ich Probleme nachvollziehbar dokumentiere.
Akzeptanzkriterien:
    • Fehler kann einem Gerät eindeutig zugeordnet werden
    • Fehlererfassung ist auch nachträglich möglich
    • Fehler wird in der Gerätehistorie gespeichert
    • Gerät gilt nach Fehlererfassung nicht als „Update abgeschlossen“

User Story 28: Fehler klassifizieren
Als Operator
möchte ich jeden Fehler klassifizieren können,
damit ich Probleme systematisch auswerten kann.
Akzeptanzkriterien:
    • Folgende Fehlerklassen stehen zur Auswahl:
        ○ Speicherplatz nicht ausreichend
        ○ Gerät nicht in der Domäne
        ○ Keine Verbindung zum Unternehmensnetz (WLAN/Ethernet)
        ○ Gerät zu alt (Ersatz notwendig)
    • Genau eine Fehlerklasse ist verpflichtend
    • Fehlerklasse ist in Übersicht und Export sichtbar

User Story 29: Fehler „Gerät nicht in der Domäne“ dokumentieren
Als Operator
möchte ich dokumentieren können, dass ein Gerät nicht in der Domäne ist,
damit klar ist, warum das Update nicht durchgeführt werden konnte.
Akzeptanzkriterien:
    • Fehlerklasse „Gerät nicht in der Domäne“ auswählbar
    • Optionaler Kommentar möglich
    • Gerät wird als „Fehlerhaft“ gekennzeichnet

User Story 30: Fehler „Keine Verbindung zum Unternehmensnetz“ dokumentieren
Als Operator
möchte ich festhalten können, dass ein Gerät keine Verbindung zum Unternehmensnetz hat,
damit der Update-Abbruch nachvollziehbar ist.
Akzeptanzkriterien:
    • Fehlerklasse „Keine Verbindung (WLAN/Ethernet)“
    • Auswahl, ob WLAN oder Ethernet betroffen ist (optional)
    • Fehler wird historisiert

User Story 31: Fehler „Gerät zu alt“ erfassen
Als Operator
möchte ich ein Gerät als technisch zu alt kennzeichnen können,
damit klar ist, dass kein Update mehr durchgeführt wird.
Akzeptanzkriterien:
    • Fehlerklasse „Gerät zu alt“
    • Gerät kann zusätzlich automatisch als „Update ausgeschlossen“ markiert werden
    • Begründung ist verpflichtend

User Story 32: Lösungsvorschläge zu bekannten Fehlern anzeigen
Als Operator
möchte ich bei bekannten Fehlern einen Lösungsvorschlag sehen,
damit ich weiß, was konkret zu tun ist.
Akzeptanzkriterien:
    • Lösungsvorschläge werden nur für bekannte Fehlerklassen angezeigt
    • Beispiele:
        ○ „Gerät in Domäne aufnehmen“
        ○ „Netzwerkverbindung herstellen“
        ○ „Speicherplatz freigeben“
    • Lösungsvorschläge sind rein informativ (keine Automatisierung)

User Story 33: Mehrere Update-Versuche dokumentieren
Als Operator
möchte ich mehrere Update-Versuche pro Gerät dokumentieren können,
damit ersichtlich ist, dass ein Gerät wiederholt Probleme hatte.
Akzeptanzkriterien:
    • Jeder Update-Versuch erzeugt einen eigenen Historieneintrag
    • Frühere Fehler bleiben sichtbar
    • Nur der letzte Versuch bestimmt den aktuellen Status

User Story 34: Abgebrochene Updates gesondert behandeln
Als Operator
möchte ich abgebrochene Updates klar von technischen Fehlern unterscheiden,
damit der weitere Umgang eindeutig ist.
Akzeptanzkriterien:
    • Abbruch ist kein klassifizierter Fehler
    • Abbruch setzt den PC wieder auf „offen“
    • Technische Fehler behalten ihren Fehlerstatus

User Story 35: Pflichtfelder für Gerätedokumentation erzwingen
Als Operator
möchte ich verpflichtende Gerätedaten erfassen müssen,
damit jede Dokumentation vollständig und vergleichbar ist.
Akzeptanzkriterien:
    • Folgende Felder sind verpflichtend:
        ○ Hostname
        ○ OS-Version
        ○ Build
        ○ IP-Adresse
        ○ PC-Typ (Laptop / Stand-PC)
        ○ Räumlichkeit
        ○ Zeitpunkt des letzten Updates
    • Ein Gerät kann nicht als „bearbeitet“ oder „Update abgeschlossen“ markiert werden, solange Pflichtfelder fehlen
    • Fehlende Pflichtfelder werden visuell hervorgehoben

User Story 36: Pflichtfelder automatisch vorbelegen
Als Operator
möchte ich, dass bekannte Informationen automatisch vorbelegt werden,
damit ich manuelle Eingaben und Fehler reduziere.
Akzeptanzkriterien:
    • OS-Version, Build und IP-Adresse können automatisch ermittelt werden
    • Automatisch ermittelte Werte sind als solche gekennzeichnet
    • Manuelle Korrektur ist möglich (mit Begründung)

User Story 38: Hinweis auf fehlende Fehlerbeschreibung anzeigen
Als Operator
möchte ich einen Hinweis erhalten, wenn ein Fehler ohne Beschreibung erfasst wird,
damit die Dokumentation aussagekräftig bleibt.
Akzeptanzkriterien:
    • Bei Fehlererfassung ohne Textbeschreibung erscheint ein Hinweis
    • Hinweis empfiehlt das Hinzufügen eines Screenshots/Fotos
    • Fehler kann trotzdem gespeichert werden (keine Blockade)

User Story 37: Screenshots oder Fotos bei Fehlern anhängen
Als Operator
möchte ich bei schwer beschreibbaren Fehlern Fotos oder Screenshots anhängen können,
damit Probleme besser nachvollziehbar sind.
Akzeptanzkriterien:
    • Anhänge sind nur bei Fehlerstatus möglich
    • Unterstützte Dateitypen: Bildformate (z. B. JPG, PNG)
    • Anhänge sind dem konkreten Fehler zugeordnet
    • Anhänge sind in der Gerätehistorie sichtbar

User Story 40: Korrekturen begründen müssen
Als Operator
möchte ich bei nachträglichen Änderungen eine Begründung angeben müssen,
damit nachvollziehbar ist, warum Daten angepasst wurden.
Akzeptanzkriterien:
    • Begründungsfeld ist bei Korrekturen verpflichtend
    • Begründung enthält Zeitstempel und Operator
    • Begründung ist in der Historie sichtbar

User Story 39: Gerätedaten nachträglich korrigieren
Als Operator
möchte ich fehlerhafte oder ungenaue Gerätedaten nachträglich korrigieren können,
damit die Dokumentation korrekt bleibt.
Akzeptanzkriterien:
    • Bearbeitung ist erlaubt, wenn:
        ○ Pflichtangaben fehlen oder
        ○ ein Eingabefehler gemacht wurde
    • Änderungen werden versioniert gespeichert
    • Ursprüngliche Werte bleiben nachvollziehbar

User Story 42: Paralleles Arbeiten mehrerer Operatoren ermöglichen
Als Operator
möchte ich parallel mit anderen Operatoren in der Applikation arbeiten können,
damit mehrere PCs gleichzeitig aktualisiert und dokumentiert werden können.
Akzeptanzkriterien:
    • Mehrere Operatoren können gleichzeitig angemeldet sein
    • Aktionen eines Operators beeinträchtigen andere Geräte nicht
    • Änderungen werden gerätebezogen gespeichert

User Story 41: Unvollständige Dokumentationen kennzeichnen
Als Operator
möchte ich unvollständig dokumentierte Geräte erkennen können,
damit ich sie gezielt nachbearbeiten kann.
Akzeptanzkriterien:
    • Status „Dokumentation unvollständig“
    • Automatische Prüfung auf fehlende Pflichtfelder
    • Filter „Unvollständig dokumentiert“ verfügbar

User Story 44: Gerät während Bearbeitung sperren
Als Operator
möchte ich ein Gerät automatisch sperren, sobald ich mit der Bearbeitung beginne,
damit kein anderer Operator gleichzeitig Änderungen vornimmt.
Akzeptanzkriterien:
    • Gerät wird beim Start der Bearbeitung gesperrt
    • Andere Operatoren können das Gerät nur lesen
    • Sperrstatus ist klar sichtbar

User Story 43: Aktiven Bearbeiter eines Geräts anzeigen
Als Operator
möchte ich sehen, welcher Operator gerade an einem Gerät arbeitet,
damit Doppelarbeit vermieden wird.
Akzeptanzkriterien:
    • Name des aktuell arbeitenden Operators wird am Gerät angezeigt
    • Anzeige ist in der Geräteübersicht und Detailansicht sichtbar
    • Anzeige aktualisiert sich in Echtzeit oder bei Seitenaktualisierung

User Story 45: Sperre nach Abschluss oder Abbruch aufheben
Als Operator
möchte ich, dass die Gerätesperre nach Abschluss oder Abbruch automatisch aufgehoben wird,
damit andere Operatoren weiterarbeiten können.
Akzeptanzkriterien:
    • Sperre wird aufgehoben bei:
        ○ „Update abgeschlossen“
        ○ „Update abgebrochen“
    • Historie enthält, wer das Gerät wann gesperrt hat
    • Manuelles Entsperren ist nur für berechtigte Rollen möglich

User Story 46: Rolle „Teamleiter“ definieren
Als Administrator
möchte ich eine Rolle „Teamleiter“ definieren,
damit Übersicht und operative Mitarbeit kombiniert möglich sind.
Akzeptanzkriterien:
    • Rolle „Teamleiter“ existiert zusätzlich zu Operator
    • Teamleiter kann:
        ○ Geräte bearbeiten (wie Operator)
        ○ Reports und Übersichten einsehen
    • Rolle ist einem Benutzer eindeutig zugeordnet

User Story 47: Übersicht für Teamleiter bereitstellen
Als Teamleiter
möchte ich eine Gesamtübersicht über den Update-Fortschritt sehen,
damit ich den Status aller Geräte und Operatoren kenne.
Akzeptanzkriterien:
    • Übersicht zeigt:
        ○ Anzahl offener, bearbeiteter, abgeschlossener Geräte
        ○ Aktive Operatoren
    • Filter nach Standort möglich
    • Übersicht ist standardmäßig read-only für Teamleiter
    • Schreibende Aktionen sind erst nach explizitem Wechsel in den Bearbeitungsmodus möglich

User Story 48: Bearbeitungshistorie pro Operator anzeigen
Als Teamleiter
möchte ich sehen können, welcher Operator welche Geräte bearbeitet hat,
damit Arbeit nachvollziehbar und fair verteilt ist.
Akzeptanzkriterien:
    • Historie zeigt Operator, Gerät, Zeitpunkt und Ergebnis
    • Filter nach Operator möglich
    • Daten sind exportierbar

User Story 49: Gesamtfortschritt aller Updates anzeigen
Als Operator
möchte ich den Gesamtfortschritt aller Windows-Updates sehen,
damit ich weiß, wie viele Geräte bereits aktualisiert sind und wie viele noch offen sind.
Akzeptanzkriterien:
    • Anzeige der Anzahl:
        ○ aktualisierter Geräte
        ○ offener Geräte
        ○ fehlerhafter Geräte
        ○ ausgeschlossener Geräte
    • Fortschritt wird automatisch berechnet
    • Keine Zielvorgaben oder Deadlines notwendig

User Story 50: Fortschritt pro Standort vergleichen
Als Operator
möchte ich den Update-Fortschritt pro Standort vergleichen können,
damit ich erkenne, wo noch besonders viele Geräte offen sind.
Akzeptanzkriterien:
    • Fortschritt wird pro Standort angezeigt
    • Vergleich basiert auf:
        ○ Gesamtanzahl Geräte
        ○ Anzahl aktualisierter Geräte
    • Darstellung tabellarisch oder grafisch
    • Standorte sind eindeutig definiert

User Story 51: Dauer eines Updates erfassen
Als Operator
möchte ich die Dauer eines Updates erfassen können,
damit der zeitliche Aufwand nachvollziehbar ist.
Akzeptanzkriterien:
    • Startzeitpunkt wird beim Beginn der Bearbeitung gesetzt
    • Endzeitpunkt wird bei „Update abgeschlossen“ gesetzt
    • Dauer wird automatisch berechnet
    • Manuelle Korrektur ist möglich (mit Begründung)

User Story 52: Durchschnittliche Update-Dauer anzeigen
Als Teamleiter
möchte ich die durchschnittliche Dauer von Updates sehen,
damit ich den Aufwand realistisch einschätzen kann.
Akzeptanzkriterien:
    • Durchschnittliche Dauer wird über abgeschlossene Updates berechnet
    • Filter nach:
        ○ Standort
        ○ Gerätetyp (Laptop / Stand-PC)
    • Ausgeschlossene und abgebrochene Updates werden nicht berücksichtigt

User Story 53: Offene Geräte priorisiert anzeigen
Als Operator
möchte ich offene Geräte priorisiert angezeigt bekommen,
damit ich effizient weiterarbeiten kann.
Akzeptanzkriterien:
    • Sortierung nach:
        ○ noch nicht bearbeitet
        ○ Fehlerstatus
        ○ zuletzt bearbeitet
    • Ausgeschlossene Geräte werden standardmäßig ausgeblendet
    • Filter sind kombinierbar (z. B. Standort + Status)

User Story 54: Transparenter Fortschritt ohne Enddatum
Als Teamleiter
möchte ich den Fortschritt ohne festen Endtermin nachvollziehen können,
damit der Fokus auf kontinuierlicher Verbesserung liegt.
Akzeptanzkriterien:
    • Keine Pflicht zur Eingabe von Zielen oder Deadlines
    • Fortschritt basiert ausschließlich auf realen Statusdaten
    • Historische Entwicklung (z. B. „vor 2 Wochen im Vergleich zu heute“) ist einsehbar
    • Vergleichswerte basieren auf gespeicherten Verlaufs-Snapshots der Ist-Daten

User Story 56: Doppelte Geräte manuell korrekt zuordnen
Als Operator
möchte ich bei doppelten Geräten entscheiden können, welcher Datensatz korrekt ist,
damit die Dokumentation bereinigt wird.
Akzeptanzkriterien:
    • Operator kann einen Datensatz als „korrekt“ markieren
    • Der andere Datensatz kann:
        ○ korrigiert oder
        ○ mit einem Hinweis versehen werden
    • Entscheidung wird in der Historie dokumentiert
    • Entscheidung enthält Zeitstempel und verantwortlichen Operator

User Story 55: Doppelte Geräte erkennen und kennzeichnen
Als Operator
möchte ich potenziell doppelte Geräte erkennen können,
damit ich diese gezielt überprüfen und korrekt dokumentieren kann.
Akzeptanzkriterien:
    • Geräte mit identischem oder ähnlichem Hostnamen und/oder IP-Adresse werden als „mögliche Dublette“ gekennzeichnet
    • Beide Datensätze bleiben zunächst erhalten
    • Kennzeichnung ist in der Geräteübersicht sichtbar
    • Kennzeichnung enthält den Erkennungsgrund (Hostname, IP-Adresse oder beides)

User Story 57: Geräte über Suche finden
Als Operator
möchte ich Geräte über eine Suchfunktion finden können,
damit ich schnell den richtigen PC identifiziere.
Akzeptanzkriterien:
    • Suche nach:
        ○ Hostname
        ○ IP-Adresse
    • Suchergebnisse werden sofort angezeigt
    • Suche funktioniert auch bei Teilbegriffen
    • Suche kann Hostname und IP-Adresse unabhängig voneinander oder kombiniert auswerten

User Story 58: Übereinstimmung von Hostname und IP prüfen
Als Operator
möchte ich prüfen können, ob ein Hostname zur angegebenen IP-Adresse passt,
damit Fehlzuordnungen vermieden werden.
Akzeptanzkriterien:
    • Anzeige von Hostname und IP-Adresse in der Geräteansicht
    • Möglichkeit zur manuellen Überprüfung durch den Operator
    • Abweichungen können kommentiert werden
    • Ergebnis der Prüfung ist als „stimmig“ oder „abweichend“ dokumentierbar

User Story 59: Schnellaktionen für häufige Statusänderungen
Als Operator
möchte ich häufig genutzte Status mit einem Klick ändern können,
damit ich schneller arbeiten kann.
Akzeptanzkriterien:
    • Schnellaktionen für:
        ○ „PC bearbeitet: Ja/Nein“
        ○ „Update abgeschlossen: Ja/Nein“
        ○ „Update abgebrochen“
    • Aktionen sind direkt in der Geräteübersicht verfügbar
    • Änderungen werden sofort gespeichert
    • Jede Schnellaktion wird mit Zeitpunkt und Operator protokolliert

User Story 60: Rückmeldung nach Schnellaktionen anzeigen
Als Operator
möchte ich nach einer Schnellaktion eine visuelle Rückmeldung erhalten,
damit ich sicher bin, dass die Aktion erfolgreich war.
Akzeptanzkriterien:
    • Kurze Bestätigung (z. B. Icon oder Hinweis)
    • Fehler bei Speicherung werden klar angezeigt
    • Statusänderung ist sofort sichtbar
    • Bei erfolgreicher Schnellaktion wird der neue Status ohne Neuladen in der Übersicht angezeigt
    • Bei fehlgeschlagener Schnellaktion bleibt der vorherige Status erhalten

User Story 61: Speichern ohne technische Pflichtprüfungen ermöglichen
Als Operator
möchte ich Einträge auch ohne technische Pflichtprüfungen speichern können,
damit meine Arbeit nicht blockiert wird.
Akzeptanzkriterien:
    • Keine automatischen Blockaden beim Speichern
    • Fehlende oder unklare Angaben können später ergänzt werden
    • Unvollständige Datensätze werden gekennzeichnet (siehe frühere Stories)
    • Bei fehlenden Angaben wird ein Hinweis angezeigt, das Speichern bleibt jedoch möglich

User Story 62: Unterstützung mehrerer Windows-Versionen
Als Operator
möchte ich verschiedene Windows-Versionen in der Applikation verwalten können,
damit die App nicht nur für Windows 11 25H2 nutzbar ist.
Akzeptanzkriterien:
    • Windows-Versionen sind nicht fest im Code hinterlegt
    • Neue Versionen (z. B. zukünftige Windows-11- oder Windows-12-Versionen) können konfiguriert werden
    • Geräte sind eindeutig einer Windows-Version zugeordnet
    • Reports können nach Windows-Version gefiltert werden
    • Geräte verwenden eine Version aus dem konfigurierbaren Versionskatalog

User Story 63: Zielversion pro Gerät definieren
Als Operator
möchte ich pro Gerät eine Ziel-Windows-Version festlegen können,
damit unterschiedliche Update-Ziele parallel unterstützt werden.
Akzeptanzkriterien:
    • Zielversion ist pro Gerät auswählbar
    • Standard-Zielversion kann global definiert werden
    • Zielversion ist in Übersicht, Historie und Export sichtbar
    • Wenn keine gerätespezifische Zielversion gesetzt ist, gilt die globale Standard-Zielversion

User Story 64: Update-Art erfassen
Als Operator
möchte ich unterschiedliche Update-Arten dokumentieren können,
damit Feature-Updates und Qualitätsupdates unterscheidbar sind.
Akzeptanzkriterien:
    • Update-Art ist ein Pflichtfeld:
        ○ Feature-Update
        ○ Qualitätsupdate
    • Update-Art ist in Historie, Übersicht und Export sichtbar
    • Bestehende Updates bleiben kompatibel (Default-Wert)
    • Für bestehende Datensätze ohne Update-Art wird beim Laden ein Default-Wert verwendet

User Story 65: Auswertung nach Update-Art ermöglichen
Als Teamleiter
möchte ich Updates nach Update-Art auswerten können,
damit ich Transparenz über durchgeführte Maßnahmen habe.
Akzeptanzkriterien:
    • Filter nach Update-Art verfügbar
    • Separate Zählung von Feature- und Qualitätsupdates
    • Export berücksichtigt Update-Art
    • Auswertung kann pro Standort und Zeitraum gefiltert werden
    • Kennzahlen und Export verwenden dieselbe Filterlogik

User Story 66: Update-Kampagnen anlegen
Als Teamleiter
möchte ich Update-Kampagnen anlegen können,
damit mehrere Update-Vorhaben parallel organisiert werden können.
Akzeptanzkriterien:
    • Kampagne hat:
        ○ Namen
        ○ Beschreibung
        ○ Zielversion
        ○ Update-Art
    • Name, Beschreibung, Zielversion und Update-Art sind Pflichtfelder
    • Start- und Enddatum sind optional
    • Geräte können einer Kampagne zugeordnet werden
    • Eine Kampagne ist nicht zwingend zeitlich begrenzt
    • Nach dem Speichern ist die Kampagne auch ohne Datumsangaben sofort für Zuordnung und Vergleich verfügbar

User Story 67: Geräte mehreren Kampagnen zuordnen
Als Operator
möchte ich Geräte einer Update-Kampagne zuordnen können,
damit Updates strukturiert abgearbeitet werden.
Akzeptanzkriterien:
    • Ein Gerät kann genau einer aktiven Kampagne zugeordnet sein
    • Kampagnenwechsel ist möglich
    • Kampagnenzuordnung ist historisiert
    • Bei Kampagnenwechsel wird die bisherige aktive Zuordnung automatisch beendet
    • Historie enthält mindestens: Gerät, Kampagne, Startzeitpunkt, Endzeitpunkt, Operator
    • Mehrfachzuordnungen eines Geräts entstehen nur historisch, nie als parallele aktive Zuordnungen

User Story 68: Fortschritt pro Update-Kampagne anzeigen
Als Teamleiter
möchte ich den Fortschritt einer Update-Kampagne sehen,
damit ich den Status mehrerer Kampagnen vergleichen kann.
Akzeptanzkriterien:
    • Fortschritt zeigt:
        ○ Gesamtgeräte
        ○ Aktualisiert
        ○ Offen
        ○ Fehlerhaft
        ○ Ausgeschlossen
    • Fortschritt ist unabhängig von anderen Kampagnen
    • Vergleich mehrerer Kampagnen möglich
    • Kennzahlen werden je Kampagne ausschließlich aus den der Kampagne aktiv zugeordneten Geräten berechnet
    • Vergleichsansicht zeigt Kampagnen nebeneinander mit identischen Kennzahlen
    • Jedes aktiv zugeordnete Gerät fließt pro Kampagne genau einmal in die Kennzahlen ein
