# Removing Ghost Nodes and Broken Nodes
> Verified: January 2022 - TM:PE 11.5.2 / TM:PE 11.6

## Overview

This guide explains how to fix two node-related problems which can adversely affect vehicles, pathfinding and mods.

### Ghost Nodes

> This issue is usually caused by bugs in anarchy mods; luckily it is trivial to fix!

Ghost nodes are a rare issue that might cause [](Simulation-error-Array-index-is-out-of-range.md) errors while in-game.

For more details, see: [](Array-Index---Symptom-9.md)

### Broken Nodes

> This is a [bug in vanilla game](https://forum.paradoxplaza.com/forum/index.php?threads/cities-skylines-steam-vibrating-node-replicable-bug.1187861/) which we have made Paradox and CO aware of.

Broken nodes are another rare error, and they cause vehicles to despawn - usually after altering your roads, rails or paths.

## How to fix

* If you haven't already done so, install **Broken Nodes Detector** mod:
    * Exit game to desktop
    * Subscribe [**Broken Nodes Detector**](https://steamcommunity.com/sharedfiles/filedetails/?id=1777173984) mod
    * Relaunch the game and enable the mod (Main Menu > Content Manager > Mods > Broken Nodes Detector > Enable)
    * Reload your save
* In-game, press `Ctrl` + `0` (zero) to open the detector
    > ![Broken node detector](https://imgur.com/5KYclfW.png)

To fix **Ghost Nodes**:

* Click **Remove Ghost Nodes**
* That's it! :)

To fix **Broken Nodes**:

* Click **Run Detector**
    * Wait for it to scan the map
* If a broken node is detected, it will be highlighted on the map:
    * Either move (with Move It mod) or bulldoze the highlighted path, road or rail
    * Afterwards, run the dector again and repeat the process until there are no more broken nodes