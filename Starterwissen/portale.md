---
title: Portale
description: Erstelle Portale und verbinde die Welt
published: true
date: 2022-01-01T15:46:31.440Z
tags: portal, survival
editor: markdown
dateCreated: 2022-01-01T15:03:03.954Z
---

# Portals

## Erstellung eines Portales

1. Besorge dir zwei Endportalrahmen (diese gibt es im Servershop für 1499L pro Stück).

2. Erstelle das Ursprungsportal mittels `/portal create <Portalname>` (dieser muss pro Portal individuell sein). Beachte dabei, dass du auf dem entsprechenden Endportalrahmen stehst.

3. Erstelle das Zielportal mittels `/portal create <Portalname>`. Dies darf nicht der gleiche Portalname wie in Schritt 2 sein.

4. Verknüpfe die beiden Portale mit `/portal link <Ursprungsportalname oder ID> <Zielportalname oder ID>`. Wenn das Portal bidirektional funktionieren soll, muss dieser Schritt auch in der umgekehrten Richtung durchgeführt werden.

5. Nun kannst du dich in das darausenstandene Endportal stellen und dich mittels deiner Schleichtaste teleportieren.

## Weitere Optionen

### Löschen

Du möchtest dein Portal nicht mehr haben oder an eine andere Stelle verschieben?

Dann stell dich in dein Portal und nutze `/portal remove`. Der Endportalrahmen wird dann an der Stelle aufsammelbar sein.

### Privat / Öffentlich

Standardmäßig erstellst du ein öffentliches Portal. Um das Portal nur von dir nutzbar zu machen nutze bitte `/portal modify <Portalname oder ID> public false`.

Dies kann mit `/portal modify <Portalname oder ID> public true` wieder rückgängig gemacht werden.

### Umbenennen eines Portals

Um dein Portal umzubenennen nutze `/portal modify <Portalname oder ID> name <Neuer Name>`.

### Anzeigename

Du möchtest einen coolen Portalnamen beim Teleport angezeigt bekommen, der sogar Farbcodes enthalten kann?

Dann nutze `/portal modify <Portalname oder ID> display-name <Anzeigename>`.

#### Beispiel

- `/portal modify sample_portal display-name &bTeststadt`

