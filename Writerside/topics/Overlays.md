> Verified: March 2022 - TM:PE 11.6.5.1

[Settings](Settings): [General](General) | [Gameplay](Gameplay) | [Policies](Policies) | **Overlays** | [Maintenance](Maintenance) | [Keybinds](Keybinds)

## Overview

Use these [settings](settings) to create persistent overlays:

* They will be visible whenever the [Toolbar](Toolbar) is visible
* To reduce clutter, only non-default customisations are shown
* They are not interactive, unless the associated tool is active

## Settings

### Tool overlays:

_Use these options to choose which overlays are shown..._

* [Priority Signs](Priority Signs)
* [Timed Traffic Lights](Timed Traffic Lights)
* [Speed Limits](Speed Limits)
* [Vehicle Restrictions](Vehicle Restrictions)
* [Parking Restrictions](Parking Restrictions)
* [Junction Restrictions](Junction Restrictions)
* Connected Lanes = [Lane Connectors](Lane Connectors)

### Developer overlays:

> These overlays are not intended for normal gameplay; they are very slow.

_Use these overlays to show information about [[Nodes, Segments, Lanes]]..._

* **Nodes and Segments** - displays IDs of nodes and segments on the map
* **Lanes** - displays IDs and other details of lanes on the map

### Pathfinder overlays:

_Use this option to display number of queued tasks in the pathfinding manager..._

* **Path Find Stats** - unlike other overlays, pathfinder stats are shown in green text under the main [Toolbar](Toolbar).

### Debug overlays:

> These overlays are only available in `DEBUG` builds of the mod used by developers.

* **Vehicles**
* **Citizens**
* **Buildings**

## FAQ

**Do they affect framerate or cause lag?**
> Yes, but only while the [Toolbar](Toolbar) is visible. The debug overlays, in particular, are extremely slow.

**An enabled overlay doesn't show**
> * Ensure corresponding features are enabled in [Maintenance](Maintenance).
> * The [Toolbar](Toolbar) must be visible to see the overlays.
> * Distant overlays are hidden; move camera closer to reveal them.

**Some icons disappear from overlays if associated tool is not active**
> * To reduce clutter and reduce lag, only _non-default_ customisations are shown (anything using default values is hidden).
> * If a tool is active (on the [Toolbar](Toolbar)), its associated overlay will always show full detail.

## See also

[TM:PE v10.x Wiki](https://tmpe.viathinksoft.com/wiki):

* [Overlays options](https://tmpe.viathinksoft.com/wiki/index.php?title=Options#Overlays)

[Issue Tracker](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues):

* <a href="https://github.com/CitiesSkylinesMods/TMPE/labels/SETTINGS"><img src="https://img.shields.io/github/issues/CitiesSkylinesMods/TMPE/SETTINGS?label=SETTINGS&logo=github" /></a>