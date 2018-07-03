---
layout: post
title:  "Charge And Conquest 2 - Top Down Game in Unity"
author: "Steven"
---

Charge and Conquest 2 is a top down shooter that takes the mechanics from various popular games such as Dynasty Warriors series, Battlerite, and Company of Heroes. 

The player starts from one side of the map, and the goal is to conquer the entire map. However, there are enemies that block your goal. Both side of the game will havetroops (Small AI) that engage each other to gain territory over the other. Two A.I. bosses will defend their territory, and you will have to defeat them to reach your goal. 

The overall setting of the game takes place in the World War II era where a civil war is happening between factions. The player spawns as the commander of the rebel army, and has to charge and conquer the territory in order to put an end to the civil war. Players will be able to fight against two different boss that will slow down his march against peace, and command his troops to conquer with him. 

[See On Github](https://github.com/tucci/comp442-compiler)

## Mechanics
- Top down shooting
- Capture Points
- Squad based A.I
- Lane/Group mechanics


## AI Programming
- Waypoint Tactics (Cover points, Ambush Points)
- Behaviour Trees and State Machines
- Pathfinding
- Context sensitive tactics per ai/group

## Group AI
- Squad Formation(Group up, Ungroup mechanics)
- Squad leader commands group
- Ability to focus fire on one target, or spread out fire

## 3 Different NPCS
- Minion/Solider
- Tank
- Helicopter


## The Outcome

{: .row}


![]({{site.url}}/assets/charge_conquest2/title_screen.png){: .col-12}
Title Screen

![]({{site.url}}/assets/charge_conquest2/top_down_cover.jpg){: .col-12}
Top Down Map Layout with Capture Points

![]({{site.url}}/assets/charge_conquest2/top_down_lanes.jpg){: .col-12}
Red Team Lane Branching

![]({{site.url}}/assets/charge_conquest2/group_formation.png){: .col-12}
Grouping with squad

![]({{site.url}}/assets/charge_conquest2/pathfinding.png){: .col-12}
Pathfinding On Map

![]({{site.url}}/assets/charge_conquest2/waypoints.png){: .col-12}
Waypoint System. Each yellow box is either a cover point or ambush point

![]({{site.url}}/assets/charge_conquest2/coverpoints.png){: .col-12}
Waypoint Searching

<iframe class="col-12" width="1423" height="622" src="https://www.youtube.com/embed/IPaKDSmjazY" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
Demo Video