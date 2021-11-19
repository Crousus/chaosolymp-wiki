---
title: Logblock
description: Wie benutzt man Logblock
published: true
date: 2021-11-19T21:35:49.018Z
tags: logblock, rollback, griefing
editor: markdown
dateCreated: 2021-11-19T21:35:49.018Z
---

# Allgemeine Infos
Das originale Wiki mit allen Infos findet man hier: https://github.com/LogBlock/LogBlock/wiki/Commands

Guides können logs nur einsehen. Als Supporter besitzt man Vollzugriff.

- Logs können Guides mit einer Holzspitzhacke prüfen. Diese bekommen man `/lb tool`
- Supporter können den Toolblock verwenden. Ihr erhaltet diesen mit `/lb toolblock`

# Parameter

Die meisten Logblock Befehle können mit Parametern spezifiziert werden.

Orginal: https://github.com/LogBlock/LogBlock/wiki/Params <p>

##### player <player\>
Grenzt den Befehl auf einen bestimmten Spieler ein.

##### since/before <Zeit\>

Grenzt den Befehl auf ein Zeitfenster ein. Dabei kann man einen dieser Zeitoperatoren benutzen:

- 1s = 1 Sekunde
- 1h = 1 Stunde
- 1d = 1 Tag
- 1m = 1 Monat
> **since**: ist die Zeit von jetzt rückwirkend bis zum angegebenen Zeitpunkt.
> **before**: ist die Zeit vor dem angegeben Zeitpunkt.
> Beide Parameter können genutzt werden um die Zeit von beiden Seiten einzuschränken


###### sel / area
Schränkt den Befehl auf ein Gebiet ein.


- `area <radius>` Bezieht sich auf den Bereich um dich herum
- `sel` Bezieht sich auf deine WorldEdit Selektion. Es gehen hierbei nur cuboid selekionen. Also kein poly!

### Typ

Spezifiziert was gesucht werden soll.

###### destroyed / created

Es werden nur zerstörungs Aktionen oder Plazierungen beachtet.

###### entities 

Möchte man nicht Blöcke sondern entities ansehen so muss man das hiermit angeben.

Beispiel:

`/lb lookup entities area 20` 
- Zeigt kills von Mobs in einem 20 Block radius an

`/lb rb entities area 20 since 3d`
- Holt alle Mobs im radius von 20 Blöcken, welche in den letzten 3 Tagen gestorben sind wieder zuzrück






# Rollback

Um einen Rollback zu machen, müsst ihr zuerst einige Dinge feststellen.

- Welcher Bereich ist betroffen? --> Mit Holzaxt selektieren
- Die Taten welchen Spielers sollen zurückgesetzt werden?
- Wie weit liegt das z.b Griefing zurück?

Der Befehl:

`/lb rb <parameter>`
`/lb rollback sel player <spieler> since <zeit>`

Ein Beispiel:

`/lb rollback sel player Crousus since 3d`
- Setzt die Aktionen der letzten 3 Tage des Spielers Crousus im selektierten Bereich zurück

> Immer die Blockanzahl prüfen bevor ihr `/yes` eingebt! Ist die zahl verdächtig hoch, prüft euren Befehl und die selektion, dass ihr nicht zu viel rollbackt!
{.is-warning}


# Clearlog

Mit dem clearlog können Logeinträge wieder gelöscht werden.

Befehl:

`/lb clearlog <parameter>`

> Wenn ihr Gebäude verschiebt, oder löscht und am alten Ort nichts mehr bleibt, könnt ihr die Logs löschen. Am besten mit Worldedit Auswahl und `/lb clearlog sel`
{.is-info}








