# UC-01 Geräteübersicht anzeigen

Akteur: Operator, Viewer, Teamleiter

Ziel: Liste aller Geräte inkl. Status, Version, Standort anzeigen.

Deckt ab: US1, US3, US5, US21, US22, US41, US53, US57

UC-02 Geräte suchen, filtern und sortieren

Akteur: Operator, Viewer, Teamleiter

Ziel: Geräte über Suche (Hostname/IP) finden, auch über Teilbegriffe; Treffer bei Eingabe direkt aktualisieren; nach Standort/Status/Version/Typ filtern und sortieren.

Deckt ab: US1, US3, US5, US50, US53, US57, US62, US65

UC-03 Gerätebestand importieren und validieren

Akteur: Operator

Ziel: CSV/Excel importieren, Pflichtfelder prüfen, fehlerhafte Datensätze anzeigen und ausschließen.

Deckt ab: US2, US35, US61

UC-04 Gerätedaten pflegen und korrigieren (inkl. Versionierung)

Akteur: Operator (Viewer nur lesend)

Ziel: Gerätedaten nachträglich bearbeiten, Änderungen versioniert speichern und begründen.

Deckt ab: US35, US36, US39, US40, US61

UC-05 Dubletten erkennen und bereinigen

Akteur: Operator

Ziel: mögliche Dubletten kennzeichnen, korrekten Datensatz festlegen, Entscheidung historisieren.

Deckt ab: US55, US56

UC-06 Hostname–IP-Abgleich prüfen und dokumentieren

Akteur: Operator

Ziel: manuelle Prüfung der Zuordnung Hostname/IP; Ergebnis als stimmig/abweichend dokumentieren; Abweichungen kommentieren.

Deckt ab: US58

Update-Ermittlung und Update-Stand
UC-07 Windows-Version/Build automatisch ermitteln (PowerShell)

Akteur: Operator

Ziel: OS-Version/Build automatisch erfassen und im Gerät speichern; Update-Pflicht ableiten.

Deckt ab: US4, US36

UC-08 Zielversion und Windows-Versionen konfigurieren

Akteur: Teamleiter, Administrator (je nach Rollenmodell)

Ziel: Zielversion global und/oder pro Gerät verwalten; Windows-Versionen über konfigurierbaren Katalog pflegen; globale Standard-Zielversion als Fallback nutzen; Filterbarkeit nach Windows-Version in Reports sicherstellen.

Deckt ab: US5, US62, US63

UC-09 Update-Art erfassen und auswerten

Akteur: Operator (erfassen), Teamleiter (auswerten)

Ziel: Feature-/Qualitätsupdate als Pflichtfeld dokumentieren; Sichtbarkeit in Historie/Übersicht/Export sicherstellen; Bestandsdaten per Default-Wert kompatibel halten; Filter und separate Zählungen nach Update-Art bereitstellen.

Deckt ab: US64, US65, US66

Update-Dokumentation, Status, Ablauf
UC-10 Bearbeitung starten, bearbeiten-Status setzen, Update-Dauer erfassen

Akteur: Operator

Ziel: Beginn der Bearbeitung dokumentieren (Startzeit), „PC bearbeitet“ pflegen, Dauer berechnen, ggf. korrigieren (mit Begründung).

Deckt ab: US21, US51, US40

UC-11 Update als abgeschlossen markieren (mit Nachprüfung)

Akteur: Operator

Ziel: Abschluss nur nach bestätigter Zielversion setzen; Zeitstempel/Operator speichern; Kommentar optional.

Deckt ab: US6, US22, US33, US51

UC-12 Update abbrechen und Prozess neu starten

Akteur: Operator

Ziel: Abbruch als eigener Zustand; „Update abgeschlossen“ zurücksetzen; Neustart setzt Gerät wieder auf „offen“, Historie bleibt.

Deckt ab: US25, US26, US33, US34

UC-13 Standardablauf (SOP) anzeigen und im Protokoll referenzieren

Akteur: Operator

Ziel: festen Update-Standardablauf als Referenz in der App anzeigen.

Deckt ab: US20

UC-14 Update-Quelle festlegen und protokollieren (USB)

Akteur: Operator

Ziel: Update-Quelle ist fest „USB“, wird in Protokoll/Historie/Export dokumentiert.

Deckt ab: US17, US18

UC-15 Speicherplatz prüfen und Update blockieren, wenn zu wenig

Akteur: Operator

Ziel: Bei „ISO lokal speichern“ Speicherplatz prüfen; bei Unterschreitung warnen und Fortsetzung verhindern; Ergebnis dokumentieren.

Deckt ab: US15, US16

UC-16 Post-Update-Checkliste durchführen und Abschluss speichern

Akteur: Operator

Ziel: Checkliste nach Update anzeigen; Punkte abhaken; Abschlussstatus mit Zeitstempel/Operator speichern.

Deckt ab: US23, US24

UC-17 Schnellaktionen ausführen und Feedback anzeigen

Akteur: Operator

Ziel: Statusänderungen (bearbeitet/abgeschlossen/abgebrochen) per 1 Klick; sofortige visuelle Rückmeldung; Statusänderung ohne Neuladen sichtbar; bei Fehlern klarer Hinweis und kein unbeabsichtigter Statuswechsel.

Deckt ab: US59, US60, US21, US22, US25

Fehler, Ausschluss, Historie, Anhänge, Benachrichtigungen
UC-18 Fehler/Probleme erfassen, klassifizieren und historisieren

Akteur: Operator

Ziel: Fehlerstatus setzen, Beschreibung erfassen, Fehlerklasse verpflichtend, Auswirkungen auf „Update abgeschlossen“.

Deckt ab: US7, US27, US28, US29, US30, US31, US33, US34, US38

UC-19 Lösungsvorschläge zu Fehlerklassen anzeigen

Akteur: Operator

Ziel: Für bekannte Fehlerklassen passende Hinweise anzeigen (nur informativ).

Deckt ab: US32

UC-20 Medien/Anhänge zu Fehlern hochladen und anzeigen

Akteur: Operator (Viewer/Teamleiter lesen)

Ziel: Fotos/Screenshots bei Fehlern anhängen, dem Fehler zuordnen und in Historie anzeigen.

Deckt ab: US37

UC-21 Gerät als „Update ausgeschlossen“ markieren und begründen

Akteur: Operator

Ziel: expliziten Ausschlussstatus setzen; Begründung verpflichtend; nicht als updatepflichtig; sichtbar in Übersicht/Historie/Export.

Deckt ab: US13, US14, US19, US31

UC-22 Update-Historie pro Gerät anzeigen

Akteur: Operator, Viewer, Teamleiter

Ziel: Timeline mit Datum, Operator, Status, Kommentar; fehlgeschlagen/abgebrochen bleibt sichtbar.

Deckt ab: US9, US33, US39, US40, US45

UC-23 In-App-Benachrichtigungen bei Fehlern verwalten

Akteur: System (erzeugen), Operator (nutzen), Viewer/Teamleiter (sehen)

Ziel: Bei Fehlerstatus Notification erzeugen; offene Fälle Übersicht; Link zur Geräteansicht.

Deckt ab: US8

Reports, Dashboards, Auswertungen
UC-24 Dashboard/Übersichten anzeigen (gesamt, pro Standort, pro Kampagne)

Akteur: Operator, Viewer, Teamleiter

Ziel: Fortschritt/Statuszahlen anzeigen; nach Standort/Kampagne filtern; Auto-Aktualisierung; Teamleiter-Übersicht standardmäßig read-only; Kampagnenfortschritt unabhängig und vergleichbar berechnen.

Deckt ab: US10, US47, US49, US50, US54, US68

UC-25 Reports exportieren (CSV/Excel) inkl. Filter

Akteur: Operator, Teamleiter

Ziel: Export mit Gerätedaten, Status, Zeitpunkten, Operator, Update-Quelle, Update-Art; Filter vor Export.

Deckt ab: US11, US18, US19, US48, US65

UC-26 Durchschnittliche Update-Dauer berechnen und anzeigen

Akteur: Teamleiter

Ziel: Durchschnitt aus abgeschlossenen Updates; Filter nach Standort/Gerätetyp; ausgeschlossen/abgebrochen nicht zählen.

Deckt ab: US52, US51

UC-27 Bearbeitungshistorie pro Operator anzeigen

Akteur: Teamleiter

Ziel: Wer hat welche Geräte wann mit welchem Ergebnis bearbeitet; filterbar; exportierbar.

Deckt ab: US48

Rollen & paralleles Arbeiten / Sperren
UC-28 Rollen und Rechte verwalten (RBAC) inkl. Audit

Akteur: Administrator

Ziel: Rollen (Admin/Operator/Viewer/Teamleiter) verwalten; Rechte steuern; Änderungen protokollieren.

Deckt ab: US12, US46

UC-29 Paralleles Arbeiten ermöglichen (gerätebezogene Änderungen)

Akteur: Operator

Ziel: mehrere Operatoren gleichzeitig; Änderungen isoliert pro Gerät; keine gegenseitige Beeinflussung.

Deckt ab: US42

UC-30 Gerätebearbeitung sperren, Bearbeiter anzeigen, Sperre aufheben

Akteur: Operator (System setzt Sperre), Administrator/Teamleiter (optional entsperren)

Ziel: Beim Start sperren; anderer darf nur lesen; aktiven Bearbeiter anzeigen; Sperre bei Abschluss/Abbruch lösen; Historie führen.

Deckt ab: US43, US44, US45

Kampagnen
UC-31 Update-Kampagnen anlegen und verwalten

Akteur: Teamleiter

Ziel: Kampagnen mit Name/Beschreibung/Zielversion/Update-Art; nicht zwingend zeitlich begrenzt.

Deckt ab: US66, US68

UC-32 Gerät einer aktiven Kampagne zuordnen und Wechsel historisieren

Akteur: Operator

Ziel: Gerät genau einer aktiven Kampagne zuordnen; Wechsel mit automatischem Abschluss der vorherigen Zuordnung; Historisierung mit Zeitbezug und Operator.

Deckt ab: US67

UC-33 Unvollständige Dokumentationen erkennen und kennzeichnen

Akteur: Operator, Teamleiter

Ziel: Pflichtfelder prüfen; Speichern ohne technische Blockade ermöglichen; Status „Dokumentation unvollständig“ setzen; Filter bereitstellen.

Deckt ab: US35, US41, US61
