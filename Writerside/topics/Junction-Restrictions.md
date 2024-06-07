# Junction Restrictions

> This documentation is under construction

## Overview

Use this tool to customise traffic policies at road junctions (including those with tram tracks and level crossings).

## Usage

Choose **Junction Restrictions** on the [](Toolbar.md):

![Junction restrictions](https://imgur.com/KDDmUbj.png)
 
> Button missing? Enable **Junction Restrictions** in [](Maintenance.md) in [](Settings.md).

You can set a keyboard shortcut to activate the tool in the [Key Bindings](Keybinds.md) in [](Settings.md).

### Applicators

[Select a junction](Select a junction) you want to customise; a detailed overlay will show available options and their current state:

![Junction Restrictions](https://user-images.githubusercontent.com/1386719/146278228-bfabe0aa-d588-4734-9e0f-1692e4b4a4ee.png)

**Click an icon** to toggle its current state (on or off).

### Icons

Junction nodes:

| Icon  | Purpose |
| :---: | :---    |
| ![Allow Enter Blocked Junction](https://imgur.com/0eVCJuH.png) ![Deny Enter Blocked Junction](https://imgur.com/duJO1QZ.png) | Allow/Deny [](Enter Blocked Junctions). |
| ![Allow Switch Lanes](https://imgur.com/chCdtd7.png) ![Deny Switch Lanes](https://imgur.com/ogINO6r.png) | Allow/Deny [](Lane Changes). |
| ![Allow U-Turn](https://imgur.com/WrcpoKL.png) ![Deny U-Turn](https://imgur.com/Rfqca7L.png) | Allow/Deny [](U-Turns). |

Junction, bend, and transition nodes:

| Icon  | Purpose |
| :---: | :---    |
| ![Allow Crossing](https://imgur.com/3pHHufv.png) ![Deny Crossing](https://imgur.com/907BIzf.png) | Allow/Deny [](Pedestrian Crossings). |

Junctions with traffic lights (icon shown depends on which side of the road traffic drives on):

| Icon  | Purpose |
| :---: | :---    |
| ![Allow Turn Left on Red](https://imgur.com/TkeYuJG.png) ![Deny Turn Left on Red](https://imgur.com/15IuDg3.png) | Allow/Deny **Left** [Turn on Red](Turn on Red) (LHT/RHD). |
| ![Allow Turn Right on Red](https://imgur.com/GYo4GqF.png) ![Deny Turn Right on Red](https://imgur.com/BxJDYLT.png) | Allow/Deny **Right** [Turn on Red](Turn on Red) (RHT/LHD). |

### Shortcuts

The following shortcuts are applicable when the Junction Restrictions tool is active...

Selection:

* `Click junction` - select the junction
    * Any previously selected junction will be deselected
    * You can now use basic applicators
* `Right-click anywhere` - deselect current junction
    * If no junction selected, it will exit the Junction Restrictions tool as if you pressed `Esc`
* `Esc` - exit Junction Restrictions tool
    * This returns focus to the [](Toolbar.md) and enables its [](Adjust Roads) mode.

Basic applicators:

> These change junction restrictions for the selected junction. Set city-wide defaults in [](Policies.md) in [](Settings.md).

* `Click a restriction icon` - toggle it on/off

Bulk applicators:

* See [](High Priority Roads)

Camera / Overlays:

* `Mouse wheel` - zoom in or out
    * If you zoom out too far, overlays may disappear
* `PageDown` - underground view
    * This also activates a simplified version of the [](Traffic Info View)
* `PageUp` - overground view

### Overlays

While the tool is active, summary overlays are displayed on the map. To reduce clutter, these overlays only show where changes have been made:

(todo: image)

To see the restrictions for more distant roads and rails, scroll the camera towards them. Depending on camera position, you might need to zoom in a little.

You can set the transparency of overlays in [](General.md) in [](Settings.md).

When the tool is deactivated overlays will be removed. You can enable a persistent summary overlay, which is visible whenever the [](Toolbar.md) is visible, in [Overlays](Overlays.md) in [](Settings.md).

### Refresh

When you make changes, only vehicles spawned _after_ that point will be aware of them.

To make existing vehicles aware of changes, enable **Customisations come in to effect immediately** in [](General.md) in [](Settings.md). This may add some momentary lag on old potato computers or on big cities.

Alternatively, you can use the [Clear Traffic](Clear-Traffic.md) tool to remove all existing traffic from the map, leaving only newly spawned traffic that is aware of your changes.

## FAQ

**Does it affect frame rate or cause lag?**
> Not usually. However, if you start disabling pedestrian crossings, it can cause more work for the pathfinder which may cause performance issues on larger cities.

**I clicked on a rail junction but no icons appear?**
> Currently, only **Level Crossings** (a junction where rail tracks intersect a road) are supported.

## See Also

[](Toolbar.md):

* [](Lane-Arrows.md)
* [](Lane-Connectors.md)
* [](Priority-Signs.md)
* [](Traffic-Lights.md)

[](Settings.md):

* [](Policies.md) - set default junction restrictions

Advanced:

* [](Reckless-Drivers.md) - they ignore junction restrictions

[Issue Tracker](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues):

* <a href="https://github.com/CitiesSkylinesMods/TMPE/labels/JUNCTION RESTRICTIONS"><img alt="Issues" src="https://img.shields.io/github/issues/CitiesSkylinesMods/TMPE/JUNCTION RESTRICTIONS?label=JUNCTION RESTRICTIONS&logo=github" /></a>