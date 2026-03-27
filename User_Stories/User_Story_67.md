# User Story 67: Geräte mehreren Kampagnen zuordnen

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
