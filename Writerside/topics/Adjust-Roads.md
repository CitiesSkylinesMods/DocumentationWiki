# Adjust Roads

> Verified: December 2021 - TM:PE 11.5.2

## Overview

Use these tools to create [Priority Routes](Priority Routes), [High Priority Roads](High Priority Roads), and optimise medium/large [Roundabouts](Roundabouts).

## Usage

The bulk applicators are accessed from the **Adjust Roads** panel:

![Adjust Roads Panel](https://imgur.com/J3UAixh.png)

To open the panel, either:

* Open the TM:PE [Toolbar](Toolbar.md), then click the road/roundabout you want to customise
    * This only works if none of the TM:PE tools are active; if you are in a tool, exit it first.
* Or, click the _name_ of the road/roundabout you want to customise
    * This is a shortcut for opening the [Traffic Routes](Traffic-Routes-Info-View.) info view, then selecting the **Adjust Roads** tab, then clicking the road/roundabout you want to customise :)

### Applicators

Click the desired button to apply changes to the route:

| Button | Purpose | Customisations |
| :---: | :--- | :--- |
| ![Delete Button](https://imgur.com/yAZDkkq.png) | Deletes all customisations along the route (_except_ vehicle restrictions and timed traffic lights). | |
| ![Stop Button](https://imgur.com/FYLtZgW.png) | Toggle **Stop** signs on/off along [Priority Routes](Priority Routes). | [Priority Signs](Priority-Signs.md) |
| ![Yield Button](https://imgur.com/1l6roVW.png) | Toggle **Yield** signs on/off along [Priority Routes](Priority Routes). | [Priority Signs](Priority-Signs.md) |
| ![High Priority Button](https://imgur.com/uxnCXGD.png) | Toggle [High Priority Roads](High Priority Roads) policies on/off along a route. | [Priority Signs](Priority-Signs.md), [Lane Arrows](Lane-Arrows.md), [Junction Restrictions](Junction-Restrictions.md) |
| ![Roundabout Button](https://imgur.com/9UKwrmp.png) | Toggle [Roundabout Policies](Roundabout Policies) on/off on a roundabout. | [Priority Signs](Priority-Signs.md), [Lane Connectors](Lane-Connectors.md), [Junction Restrictions](Junction-Restrictions.md), [Speed Limits](Speed-Limits.md), [Parking Restrictions](Parking-Restrictions.md) |
| ![Adjust Road Button](https://imgur.com/0k5ZaU6.png) | Select/alter the route (see next section) | |

Note:

* Clicking the button a second time will remove the customisations (TM:PE 11.6 or later).
* The roundabout button will only be enabled if the route consists entirely of one-way road.
* To ensure customisations are applied, the features must be enabled in [Maintenance](Maintenance.md) [settings](Settings.md).

### Setting the route

The selected route is indicated by a thick green bar along the road or roundabout.

> If you opened the **Adjust Roads** panel via the TM:PE [Toolbar](Toolbar.md), the route will only be shown when the mouse hovers an applicator button.

If you want to alter the route:

1. Click the **Adjust Road** button:  
![Adjust Road Button](https://imgur.com/0k5ZaU6.png)
2. Click any road/roundabout to set it as the route
3. Drag the green circles to extend or alter the route:
    * The large circles at the ends of the green bar define start/end points
    * The smaller circle, somewhere in the middle, can anchor the route to a specific road

![Example Route](https://user-images.githubusercontent.com/26344691/81401282-ab37a180-9137-11ea-81a8-09b09c8397d2.png)

### Renaming the route

All segments of the route are given the same road name, which is shown in the _title bar_ of the **Adjust Roads** panel.

To change the road name:

1. Click the current name in the title bar
2. Alter the name as desired
3. Press **Return** to save changes

> You can rename any network this way - including quays, paths and power lines!

### Shortcuts

The following shortcuts are applicable when the **Adjust Roads** panel is active...

Selection:

* `Click a road/roundabout` - Select route
    * Any previously selected route will be deselected
    * You can now use applicators
* `Esc` - exit **Adjust Roads** panel

Camera / Overlays:

* `Mouse wheel` - zoom in or out
    * If you zoom out too far, overlays may disappear

### Overlays

While the **Adjust Roads** panel is open, multiple TM:PE [Overlays](Overlays.md) will be visible, such as speed limits, lane connectors, and priority signs. To reduce clutter, these overlays only show where changes have been made:

![Overlays](https://user-images.githubusercontent.com/1386719/150238814-172b89e6-ac62-45aa-8ac1-aa99e9427848.jpg)

To see overlays for more distant roads, scroll the camera towards them. Depending on camera position, you might need to zoom in a little.

You can set the transparency of overlays in [General](General.md) [settings](Settings.md). When the **Adjust Roads** panel is closed, overlays will be removed.

## FAQ

**Some vehicles ignore the customisations**

> * [Reckless Drivers](Reckless-Drivers.md) ignore most traffic policies.
> * Vehicles which are already driving aren't notified about changes by default:
>     * Enable **Apply AI changes right away** in [General](General.md) [settings](Settings.md) if you want immediate updates.
> * Short road segments entering junctions can confuse the vehicle AIs (eg. not enough time to yeild/stop):
>     * Use [Broken Nodes Detector](https://steamcommunity.com/sharedfiles/filedetails/?id=1777173984) mod to locate them
>     * Increasing the length of the segment usually fixes it, and setting a lower speed for the segment also sometimes works

**Does it affect frame rate or cause lag?**

> Not directly; the bulk applicators are just alternate ways to apply customisations. Some of those customisations, however, might cause a little lag (see their wiki pages for more details).

**After changing the route (green bar), my roads disappeared!**

> This is either a game bug or broken workshop road assets. For more details, and how to fix, see: [Section of road becomes blue void](Section of road becomes blue void).

## See Also

[Toolbar](Toolbar.md):

* [Junction Restrictions](Junction-Restrictions.md)
* [Lane Connectors](Lane-Connectors.md)
* [Parking Restrictions](Parking-Restrictions.md)
* [Priority Signs](Priority-Signs.md) - has similar bulk applicators
* [Speed Limits](Speed-Limits.md)

[Settings](Settings.md):

* [Policies](Policies.md) - configure high priority road and roundabout policies

Guides:

* Info views:
    * [Traffic Routes](Traffic-Routes-Info-View.)
* Roads:
    * [Priority Routes](Priority Routes)
    * [High Priority Roads](High Priority Roads)
    * [Roundabouts](Roundabouts)

[Issue Tracker](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues):

* <a href="https://github.com/CitiesSkylinesMods/TMPE/labels/MASS EDIT"><img alt="Issues" src="https://img.shields.io/github/issues/CitiesSkylinesMods/TMPE/MASS EDIT?label=MASS EDIT&logo=github" /></a>