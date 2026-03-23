Entitäten

• Computer
• Nutzer
• Ort
• Medium
• Laufplan
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
        ○ E-Mail Adresse
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
            ▪ Notiz
            ▪ Erfolgreich
                • Ja
                • Nein
            ▪ Aktualisierungsdatum
            ▪ Operator (FK)
        ○ Medium (FK)
        ○ Notiz
        ○ ist abgeschlossen