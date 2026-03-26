# Entitäten

• Computer
• Nutzer
• Ort
• Medium
• Laufplan
• Kampagne
• Role = Operator / Viewer

Attribute

    • Computer 
        ○ Hostname
        ○ IP-Adresse
        ○ Betriebssystem
            ▪ Windows 11
            ▪ Version (25H2)
        ○ Typ
            ▪ PC
            ▪ Laptop
            ▪ Server
        ○ Notiz
        ○ Ort (FK)
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
            ▪ Notiz
            ▪ Erfolgreich
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
