---
title: Quest Erstellung
description: Guide um Quests zu erstellen
published: true
date: 2021-09-13T19:09:05.350Z
tags: erstellen, quest, quests
editor: markdown
dateCreated: 2021-09-07T19:11:28.370Z
---

# Basics
-  `/quest create` Öffnet den Quest Editor
 
 
#  Stages
 
1. Auf Schleimball drücken um eine neue Stage (Quest Abschnitt) zu erstellen
2. Aufgabenart auswählen
3. Ggf. geforderte Daten angeben

<div id="bring_back"></div>

#### Beispiel: "Items zurück bringen"

<br>
 <img src="/quests/bring_back_items_1.png" alt="stage-edit" width="300" style="margin-left: 20px"/>
 
-  Ein vorher erstelltes Item in das rote Feld ziehen oder auf das Feld klicken, um ein neues Item zu erstellen
<p>
<img src="/quests/bring_back_items_2.png" alt="stage-edit" width="300" style="margin-left: 20px"/>
</p>

- Für normale Items reicht es den Pfeil und das Redstone zu bedienen, um den Item-Typ und die Anzahl festzulegen
- Für komplexere Items empfiehlt es sich diese, wie bereits beschrieben, direkt in das Rote Feld zu ziehen
- Anschließend immer auf Speichern oder Bestätigen gehen
<p>
<img src="/quests/bring_back_items_3.png" alt="stage-edit" width="300" style="margin-left: 20px"/>
</p>

- Bei dieser Ansicht kann ein NPC erstellt werden oder ein bereits Existierender ausgewählt werden, zu welchem die Items gebracht werden sollen

> Tipp: Immer vorher erstellen und dann mit dem Stick zuweisen!
{.is-info}



## Stage einstellen

<p>
<img src="/quests/stage_overview_1.png" alt="stage-edit" width="300" style="margin-left: 20px"/>
</p>
<ul>
	<li>
	 <b>Kartoffel:</b> Hier kann eine Belohnung gesetzt werden, welche der Spieler nach Abschluss dieses 			Quest Abschnitts erhalten soll. Dies sind meistens Questitems welche für die nächste Stage
   	benötigt werden.
	</li>
	<li>
	 <b>Schild:</b> Ermöglicht es eine Beschreibung für den Schritt zu setzen. Diese wird dann im Quest Scoreboard angezeigt.
	</li>
	<li>
	 <b>Feder:</b> Wird benötigt um eine Startnachricht zu setzen. Diese wird vor Beginn der Stage dem Spieler angezeigt.
	</li>
	<li>
	 <b>Netherstern:</b> Damit können sogenannte Validierungsanforderungen definiert werden. Mehr dazu unter <a href="#validy">Validierungsanforderungen</a>
	</li>
  	<li>
	 <b>Kiste:</b> Im Fall: <a href="#bring_back"> Items zurückbringen</a>, können hier die Items im Nachhinein angepasst werden.
	</li>
    	<li>
	 <b>Farbstoff:</b> Damit können die Partikel und HD Lines ausgeschaltet werden, welche über dem NPC zu sehen sind.
	</li>
      	<li>
	 <b>Dorfbewohner Ei:</b> Hiermit kann der Ziel-Npc geändert werden.
	</li>
</ul>
<p>
<img src="/quests/stage_overview_2.png" alt="stage-edit" width="300" style="margin-left: 20px"/>
</p>
<ul>
	<li>
	 <b>Buch:</b> Ermöglicht es vor Stagebeginn einen Dialog zwischen Spieler und NPC zu erstellen.
	</li> 
  	<li>
	 <b>Papier:</b> ?
	</li> 
  	<li>
	 <b>Prismarin:</b> Siehe <a href="#comparison">Gegenstandsvergleich</a>
	</li> 
</ul>
<div id="validy"></div>

# Validierungsanforderungen
<p>

<img src="/quests/validy.png" alt="stage-edit" width="300" style="margin-left: 20px"/>
  </p>

- Mit Validierungsanforderungen ist es möglich Regeln zu definieren, welche eingehalten werden müssen um die Quest zu Starten oder eine Stage abzuschließen, bzw. Fortschritte machen zu können.

- **Quest Benötigt:** Erlaubt es andere Quests zu setzen, welche abgeschlossen sein müssen.
- **Erfahrungslevel:** Setzt ein minimal erforderliches Erfahrungslevel vorraus.
- **Berechtigungen:** Permissions welche der Spieler braucht. Diese können willkürlich ausgedacht, sondern übersichtlich geordnet sein. Sollten aber beschreibend sein und immer einen Punkt haben. Also z.B quest.kraeuter. In der Vergangenheit wurden sie nach den jeweiligen Events benannt und im  Verlauf freigeschaltet z.B. winter.1 
- **Punktestand:** Damit kann ein Punktestand in einem beliebigen Scoreboard vorausgesetzt werden.
- **Region:** Der Spieler muss um diese Regel zu erfüllen in der Region stehen.
- **Fertigkeitslevel:** Kann ein bestimmtes McMMO Level im gewählten Skill fordern. Hier gibt man zuerst den Skill an. z.B "Bergbau", anschließend das Level. z.B "100" und zuletzt den Vergleichsoperator. Heißt für kleiner Level 100 dann "less" für =100 "equal" und für >100 "greater.
Also z.B: Bergbau --> 100 --> greater
- **Geld**: Bestimmt ob der Spieler eine bestimme Geldmenge benötigt. Dabei wird kein Geld abgezogen.

<div id="comparison"></div>

# Gegenstandsvergleich
<br>
<img src="/quests/compare.png" alt="stage-edit" width="300" style="margin-left: 20px"/>

Beim Gegenstandsvergleich können Regeln festgelegt werden, welche beim Zurückbringen der Items akzeptiert werden müssen, um die Quest zu erfüllen.

1. Modus: Alle Komponenten müssen exakt gleich sein. Jegliche kleine Abweichung in den NBT Daten wird nicht angenommen
2. Modus: Alles außer die NBT Daten werden verglichen. NBT Daten sind zb: Max Enchant Level, Tags
3. Modus: Nur das Material ist wichtig, alles andere wird ignoriert.
4. Modus: Der Name wird beim Vergleich mit einbezogen.
5. Modus: Die Lore wird mit verglichen.
6. Modus: Prüft ob die Verzauberungen gleich sind.
7. Modus: Prüft ob die (Level) Kosten bei der Reparatur 

> Die Modi können miteinander kombiniert werden. Also z.B Modus 2 mit Modus 4 würde das Material und den Namen berücksichtigen.
{.is-info}

# Belohnungen

Belohnugen können zu Questbeginn, vor und nach jeder Stage und am Ende der Quest vergeben werden.
<br>
<img src="/quests/reward.png" alt="stage-edit" width="300" style="margin-left: 20px"/>
- Befehl ausführen. Hier können beliebige Konsolen Befehle eingegeben werden, welche ausgeführt werden sollen. Bei mehreren empfiehlt es sich eine kleine Verzögerung zwischen allen Befeheln zu haben.

- Belohnungsitems: Ein Item kann festgelegt werden als Belohnung. Zum Einstellen siehe <a href="#bring_back"> Items zurückbringen</a>, welches dem gleichen Prinzip folgt.
- Abschlussnachricht: Damit kann eine Letzte Nachricht gesetzt werden, welche ausgeführt werden soll. Es empfiehlt sich die Dialog Option stattdessen zu benutzen.
- Geldbelohnung: Ermöglicht es Geld zu senden.
- Berechtgungen: Damit können dem Spieler Permissions zugewiesen oder genommen zu werden.
- Teleportationsposition: Teleportiere den Spieler an einen Beliebigen Ort
- Erfahrung: Gebe dem Spieler Erfahrungspunkte oder Level
- Belohnung mit Vorraussetzung: Lässt eine bestimmte Belohung aus wenn eine gewisse Vorraussetzung nicht gegeben ist. Siehe <a href="#validy">Validierungsanforderungen</a>.
- Wait Reward: *?*
- Title Reward: Zeigt dem Spieler einen Schriftzug auf dem Bildschirm an.

# Finale Einstellung
<br>
<img src="/quests/quest_save.png" alt="stage-edit" width="300" style="margin-left: 20px"/>

### Farbstoff

1. Questlimit nicht zählen: *Benutzen wir nicht,*
2. Vom Spieler abbrechbar: Definiert ob der Spieler die Quest abbrechen kann. **Setzen wir immer auf "Ja"!**
3. Über Gui startbar: Regelt ob der Spieler überall mit /quests die Quest starten kann. **Wir setzen es immer auf *"Nein"*!**
4. Im Todesfall abbrechen: Wenn der Spieler stirbt wird die Quest abgebrochen.
5. Verstecken wenn Anforderungen nicht erfüllt: Zeigt die Quest im GUI nicht an wenn die Anforderungen für den Start nicht erfüllt sind. **Setzen wir immer auf "Ja"!**
6. Scoreboard: Bestimmt ob das Scoreboard den Queststatus anzeigen soll oder nicht. **Setzen wir immer auf "Ja"!**
7. Dynmap verstecken: Definiert ob der Start NPC einen Livemap Tag erhalten soll. **"Setzen wir immer auf "Verstecken"!**
8. Beitritt automatisch starten: Wenn der Spieler das erste Mal auf den Server joint wird die Quest gestartet
9. Wiederholbar: Sollte die Quest wiederholbar sein?. Wenn ja anschließend Cooldown in Minuten bearbeiten.



> Folgende Einstellungen **müssen** gesetzt werden:
**Ja:** Abbrechbar, Verstecken wenn nicht erfüllt, Scoreboard, Dynmap verstecken, Wiederholbar bei Dailys
**Nein:** Über GUI startbar, 
{.is-warning}


### Andere Einstellungen

- Namensschild: Setzt den Questnamen. **Pflichtfeld!**
- Buch: Item (Icon) der Quest. Die Quest wird mit diesem Item im Menü angezeigt.
- Bild: **NICHT ANFASSEN!!**
- Rote Scheibe: **NICHT ANFASSEN!!**
- Netherstern: <a href="#validy">Validierungsanforderungen</a>.
- Kiste: Questgruppe, **NICHT ANFASSEN!!**
- Papier rechts: Nachricht welche am Ende der Quest gesendet wird.
- Buch & Feder: Dialog welcher vor dem Queststart geführt werden soll.
- Dorfbewohner Ei: Lege einen NPC fest welcher die Quest starten soll.
- Papier links: Nachricht welche beim Queststart gesendet werden soll. **BÖSE! NICHT ANFASSEN!!**
- Startbelohnung: **AUCH NICHT ANFASSEN!!**
- Schild: Questbeschreibung welche in der GUI gezeigt wird. *Nicht wichtig*
- Goldbarren: Alle Änderungen speichern.









 

 
 