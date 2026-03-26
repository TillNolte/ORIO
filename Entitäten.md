# Entitäten

• Computer
• Nutzer
• Ort
• Medium
• Laufplan
• Kampagne
• Windows-Version
• Role = Operator / Viewer

Attribute

    • Computer 
        ○ Hostname
        ○ IP-Adresse
        ○ Suchindex (abgeleitet aus Hostname und IP-Adresse)
        ○ Betriebssystem
            ▪ Windows 11
            ▪ Version (25H2)
        ○ Windows-Version (FK)
        ○ Typ
            ▪ PC
            ▪ Laptop
            ▪ Server
        ○ Notiz
        ○ Ort (FK)
        ○ Zielversion (optional)
        ○ Wirksame Zielversion (abgeleitet aus Gerät oder globaler Standard-Zielversion)
        ○ Dokumentation unvollständig
        ○ Dokumentationshinweis
        ○ Hostname-IP-Abgleich
            ▪ Ergebnis (stimmig/abweichend)
            ▪ Kommentar
            ▪ Prüfzeitpunkt
        ○ Dublettenkennzeichnung
            ▪ Ist mögliche Dublette
            ▪ Erkennungsgrund (Hostname/IP/beides)
        ○ Dublettenentscheidung
            ▪ Ist korrekter Datensatz
            ▪ Maßnahme Alternativdatensatz (korrigiert/hinweis)
            ▪ Hinweistext
            ▪ Entscheidungszeitpunkt
            ▪ Operator (FK)
        ○ Letzte Schnellaktion
            ▪ Aktion
            ▪ Ergebnis (erfolgreich/fehlgeschlagen)
            ▪ Hinweistext
            ▪ Zeitpunkt
        ○ Aktive Kampagne (FK, optional)
        ○ Kampagnenzuordnungsverlauf [1:n]
            ▪ Kampagne (FK)
            ▪ Startzeitpunkt
            ▪ Endzeitpunkt
            ▪ Operator (FK)
    • Nutzer
        ○ Benutzertyp
            ▪ Ausbilder
            ▪ Auszubildender
        ○ Computer (FK)
        ○ Ort (FK)
        ○ Notiz
    • Role = Operator
        ○ Vorname
        ○ Nachname
        ○ E-Mail-Adresse
        ○ Kennwort
        ○ Ausbildungsberuf
            ▪ FISI
            ▪ FPIT
        ○ Notiz
    • Ort
        ○ Name
        ○ Straße
        ○ Postleitzahl
        ○ Gebäude
        ○ Etage
        ○ Raum
        ○ Reihe
        ○ Notiz
    • Medium
        ○ Bezeichnung
        ○ Pfad
        ○ Notiz
        ○ Erstelldatum
    • Laufplan
        ○ Bezeichnung
        ○ Geplantes Startdatum
        ○ Geplantes Enddatum
        ○ Startdatum
        ○ Enddatum (Automatisch gesetzt)
        ○ Operator (FK) [m:n]
        ○ Computer (FK) [m:n]
            ▪ Bearbeitet
                • Ja
                • Nein
            ▪ Update-Art
                • Feature-Update
                • Qualitätsupdate
                • Pflichtfeld, für Bestandsdaten mit Default-Wert
            ▪ Zielversion (wirksam)
            ▪ Notiz
            ▪ Erfolgreich
                • Ja
                • Nein
            ▪ Update abgebrochen
                • Ja
                • Nein
            ▪ Aktualisierungsdatum
            ▪ Operator (FK)
        ○ Medium (FK)
        ○ Notiz
        ○ ist abgeschlossen
    • Kampagne
        ○ Name
        ○ Beschreibung
        ○ Zielversion
        ○ Update-Art
        ○ Geplantes Startdatum (optional)
        ○ Geplantes Enddatum (optional)
        ○ Ist aktiv
        ○ Erstelldatum
        ○ Aktualisierungsdatum
        ○ Notiz
        ○ Fortschritt (abgeleitet)
            ▪ Gesamtgeräte
            ▪ Aktualisiert
            ▪ Offen
            ▪ Fehlerhaft
            ▪ Ausgeschlossen
    • Windows-Version
        ○ Name
        ○ Release-Bezeichnung
        ○ Build
        ○ Ist aktiv
        ○ Erstelldatum
        ○ Aktualisierungsdatum
        ○ Notiz
