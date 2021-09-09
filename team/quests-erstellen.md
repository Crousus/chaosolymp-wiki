---
title: Quests Erstellung
description: Guide um Quests zu erstellen
published: true
date: 2021-09-09T21:11:06.857Z
tags: erstellen, quest, quests
editor: markdown
dateCreated: 2021-09-07T19:11:28.370Z
---

# Basics
-  `/quest create` Öffne den Quest Editor
 
 
#  Stages
 
1. Auf Schleimball drücken um eine neue Stage (Quest Abschnitt) zu erstellen
2. Aufgabenart auswählen
3. Ggf. geforderte Daten angeben

<div id="bring_back"></div>

#### Beispiel Items zurück bringen

<br>
 <img src="/quests/bring_back_items_1.png" alt="stage-edit" width="300" style="margin-left: 20px"/>
 
-  Item in das rote Feld ziehen, oder auf das Feld klicken, um ein Item einzustellen
<p>
<img src="/quests/bring_back_items_2.png" alt="stage-edit" width="300" style="margin-left: 20px"/>
</p>

- Für normale Items reicht es den Pfeil und das Redstone zu bedienen, um Item Typ und die Anzahl festzulegen
- Für komplexere Items empfiehlt es sich diese wie bereits beschrieben direkt in das Rote Feld zu ziehen
- Anschließend immer auf Speichern oder Bestätigen gehen
<p>
<img src="/quests/bring_back_items_3.png" alt="stage-edit" width="300" style="margin-left: 20px"/>
</p>

- Bei dieser Ansicht kann ein NPC erstellt werden oder ein existierender gesetzt werden zu welchem die Items gebracht werden soll

> Immer vorher erstellen und dann mit dem Stick zuweisen!
{.is-info}



## Stage einstellen

<p>
<img src="/quests/stage_overview_1.png" alt="stage-edit" width="300" style="margin-left: 20px"/>
</p>
<ul>
	<li>
	 <b>Kartoffel:</b> Hier kann eine Belohnung gesetzt werden, welche der Spieler nach Abschluss dieses 			Quest Abschnitts erhalten soll. Das sind meistens Questitems welche für die nächste Stage
   	benötigt werden.
	</li>
	<li>
	 <b>Schild:</b> Ermöglicht es eine Beschreibung für den Schritt zu setzen. Diese wird dann im Quest Scoreboard angezeigt
	</li>
	<li>
	 <b>Feder:</b> Wird benutzt um eine Startnachricht zu setzen. Diese wird vor dem Beginn der Stage dem Spieler gezeigt
	</li>
	<li>
	 <b>Netherstern:</b> Damit können sogenannte Validierungsanforderungen definiert werden. Mehr dazu unter <a href="#validy">Validierungsanforderungen</a>
	</li>
  	<li>
	 <b>Kiste:</b> Im Fall <a href="#bring_back">Items zurückbringen</a> können hier die Items im Nachhinein angepasst werden.
	</li>
    	<li>
	 <b>Farbstoff:</b> Damit können die Partikel und HD Lines ausgeschaltet werden, welche über dem NPC zu sehen sind
	</li>
      	<li>
	 <b>Dorfbewohner Ei:</b> Für die Änderung des Ziel NPCs
	</li>
</ul>
<p>
<img src="/quests/stage_overview_2.png" alt="stage-edit" width="300" style="margin-left: 20px"/>
</p>
<ul>
	<li>
	 <b>Buch:</b> Ermöglicht es vor Stage beginn einen Dialog zwischen Spieler und NPC zu erstellen
	</li> 
  	<li>
	 <b>Papier:</b> Keine Ahnung	
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

- Mit Validierungsanforderungen ist es möglich Regeln zu definieren, welche eingehalten werden müssen um die Quest zu Starten oder eine Stage abschließen bzw Fortschritte machen zu können

- **Quest Benötigt:** Erlaubt es andere Quests zu setzen, welche abgeschlossen sein müssen.
- **Erfahrungslevel:** Setzt das minimal erforderliche Erfahrungslevel vorraus
- **Berechtigungen:** Permissions welche der Spieler braucht. Diese können willkürlich ausgedacht sein. Sollten aber deskriptiv sein und immer einen Punkt haben. Also z.b quest.kraeuter
- **Punktestand:** Damit kann ein Punktestand in einem beliebigen Scoreboard vorausgesetzt werden können
- **Region:** Der Spieler muss um diese Regel zu erfüllen in der Region stehen
- **Fertigkeitslevel:** Kann ein bestimmtes McMMO Level im gewählten Skill fordern. Hier gibt man zuerst den Skill an. z.B "Bergbau", anschließend das Level. z.B "100" und zuletzt den Vergleichsoperator. Heitß für kleiner Level 100 dann "less" für =100 "equal" und für >100 "greater
- **Geld**: Bestimmt ob der Spieler eine bestimme Geldmenge benötigt. Dabei wird kein Geld abgezogen

<div id="comparison"></div>

# Gegenstandsvergleich





 

 
 