# Junction Restrictions

> This documentation is under construction

## Overview

Use this tool to customise traffic policies at road junctions (including those with tram tracks and level crossings).

## Usage

Choose **Junction Restrictions** on the [](Toolbar.md):

![Junction restrictions](btnJunctionRestrictions.png)

> Button missing? Enable **Junction Restrictions** in [](Maintenance.md) in [](Settings.md).

You can set a keyboard shortcut to activate the tool in the [Key Bindings](Keybinds.md) in [](Settings.md).

### Applicators

[](Select-a-Junction.md) you want to customise; a detailed overlay will show available options and their current state:

![Junction Restrictions](picJunctionRestrictions_junction.png)

**Click an icon** to toggle its current state (on or off).

### Icons

Junction nodes:

|                                                                   Icon                                                                    | Purpose                                    |
|:-----------------------------------------------------------------------------------------------------------------------------------------:|:-------------------------------------------|
| ![Allow Enter Blocked Junction](picJunctionRestrictions_ebsAllow.png) ![Deny Enter Blocked Junction](picJunctionRestrictions_ebsDeny.png) | Allow/Deny [](Enter-Blocked-Junctions.md). |
|        ![Allow Switch Lanes](picJunctionRestrictions_switchAllow.png) ![Deny Switch Lanes](picJunctionRestrictions_switchDeny.png)        | Allow/Deny [](Lane-Changes.md).            |
|               ![Allow U-Turn](picJunctionRestrictions_uturnAllow.png) ![Deny U-Turn](picJunctionRestrictions_uturnDeny.png)               | Allow/Deny [](U-Turns.md).                 |

Junction, bend, and transition nodes:

|                                                          Icon                                                           | Purpose                                 |
|:-----------------------------------------------------------------------------------------------------------------------:|:----------------------------------------|
| ![Allow Crossing](picJunctionRestrictions_crossingAllow.png) ![Deny Crossing](picJunctionRestrictions_crossingDeny.png) | Allow/Deny [](Pedestrian-Crossings.md). |

Junctions with traffic lights (icon shown depends on which side of the road traffic drives on):

|                                                               Icon                                                                | Purpose                                            |
|:---------------------------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------|
|  ![Allow Turn Left on Red](picJunctionRestrictions_tlorAllow.png) ![Deny Turn Left on Red](picJunctionRestrictions_tlorDeny.png)  | Allow/Deny **Left** [](Turn-on-Red.md) (LHT/RHD).  |
| ![Allow Turn Right on Red](picJunctionRestrictions_trorAllow.png) ![Deny Turn Right on Red](picJunctionRestrictions_trorDeny.png) | Allow/Deny **Right** [](Turn-on-Red.md) (RHT/LHD). |

### Shortcuts

The following shortcuts are applicable when the Junction Restrictions tool is active...

Selection:

* `Click junction` - select the junction
    * Any previously selected junction will be deselected
    * You can now use basic applicators
* `Right-click anywhere` - deselect current junction
    * If no junction selected, it will exit the Junction Restrictions tool as if you pressed `Esc`
* `Esc` - exit Junction Restrictions tool
    * This returns focus to the [](Toolbar.md) and enables its [](Adjust-Roads.md) mode.

Basic applicators:

> These change junction restrictions for the selected junction. Set city-wide defaults in [](Policies.md)
> in [](Settings.md).

* `Click a restriction icon` - toggle it on/off

Bulk applicators:

* See [](High-Priority-Roads.md)

Camera / Overlays:

* `Mouse wheel` - zoom in or out
    * If you zoom out too far, overlays may disappear
* `PageDown` - underground view
    * This also activates a simplified version of the [](Traffic-Info-View.md)
* `PageUp` - overground view

### Overlays

While the tool is active, summary overlays are displayed on the map. To reduce clutter, these overlays only show where
changes have been made:

(todo: image)

To see the restrictions for more distant roads and rails, scroll the camera towards them. Depending on camera position,
you might need to zoom in a little.

You can set the transparency of overlays in [](General.md) in [](Settings.md).

When the tool is deactivated overlays will be removed. You can enable a persistent summary overlay, which is visible
whenever the [](Toolbar.md) is visible, in [Overlays](Overlays.md) in [](Settings.md).

### Refresh

When you make changes, only vehicles spawned _after_ that point will be aware of them.

To make existing vehicles aware of changes, enable **Customisations come in to effect immediately** in [](General.md)
in [](Settings.md). This may add some momentary lag on old potato computers or on big cities.

Alternatively, you can use the [Clear Traffic](Clear-Traffic.md) tool to remove all existing traffic from the map,
leaving only newly spawned traffic that is aware of your changes.

## FAQ

**Does it affect frame rate or cause lag?**
> Not usually. However, if you start disabling pedestrian crossings, it can cause more work for the pathfinder which may
> cause performance issues on larger cities.

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

* <a href="https://github.com/CitiesSkylinesMods/TMPE/labels/JUNCTION RESTRICTIONS"><img alt="Issues" src="https://img.shields.io/github/issues/CitiesSkylinesMods/TMPE/JUNCTION RESTRICTIONS?label=JUNCTION RESTRICTIONS%26logo=github" /></a>