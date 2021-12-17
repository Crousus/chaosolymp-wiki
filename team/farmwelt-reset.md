---
title: Farmwelt Resetten
description: 
published: true
date: 2021-12-17T18:08:27.225Z
tags: 
editor: markdown
dateCreated: 2021-12-17T18:08:27.225Z
---

# Vorbereitung
- User informieren
- Backup anfertigen
- /whitelist on

# Overworld

1. Serverneustart
2. Wärend des Neustarts "world" aus dem Ordner löschen damit die Welt neu generiert
3. Welt mit /mv tp world betreten
4. Geeigneten Inselplatz in Spawnnähe finden
5. //schem load farminseln/overworld
6. pasten
7. /rg list
8. Regionen umsetzten (Bei der unten region viel Untergrund mitnehmen)
9. Eventuell rtp Radius in ChaosEssentials config anpassen (Restart notwendig)
10. Zu Spawnpostion begeben
11. /mv setspawn
12. /setworldspawn ~ ~ ~
13. /setwarp farmwelt
14. /worldborder set 4000 --> /worldborder set 10000 604800

# Nether

1. /mv delete world_nether
2. Welt mit /mv tp world_nether betreten
3. Geeigneten Inselplatz in Spawnnähe finden (Hier echt schwer)
4. //schem load farminseln/nether
7. /rg list
8. Regionen umsetzten (Bei der unten region viel Untergrund mitnehmen)
9. Eventuell rtp Radius in ChaosEssentials config anpassen (Restart notwendig)
10. /mv setspawn
11. /wb set 2000
12. /setwarp netherfarmwelt

# End

1. /mv delete world_the_end
2. Welt mit /mv tp world_the_end betreten
3. Geeigneten Inselplatz weit weg finden /tp 10000 100 10000
4. //schem load farminseln/end
7. /rg list
8. Regionen umsetzten (Bei der unten region viel Untergrund mitnehmen)
9. Eventuell rtp Radius in ChaosEssentials config anpassen (Restart notwendig)
10. /mv setspawn
11. /worldborder set 2000 --> /worldborder set 8000 900000
12. /setwarp end /setwarp endfarmwelt

# Abschluss

- DELETE FROM \`masuite_homes` WHERE server = 'farm'
- /whitelist off



