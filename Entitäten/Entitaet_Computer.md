# • Computer

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
