# Lane Arrows

> Verified: December 2021 — TM:PE 11.5.2

## Overview

Lane arrows can be used to organize traffic flow across road junctions and level crossings.

> Arrows only affect normal road traffic. To customize tracked junctions, use [](Lane-Connectors.md) instead.

## Usage

Choose **Lane Arrows** on the [](Toolbar.md) ![Lane arrows tool](btnLaneArrows.png){style="inline"}

You can set a keyboard shortcut to activate the tool in the [Key Bindings](Keybinds.md) in [](Settings.md).

### Applicators

> See the **Shortcuts** section below for more applicators!

1. **Click a road segment at a junction** to edit it.
2. A panel appears showing arrows for each lane:  
   ![](picLaneArrows_ui.png){style="block"}
   > In the image above, traffic entering from **Lane 1** must turn left, while **Lane 2** can go straight ahead or
   right.
3. **Click arrow buttons** to toggle direction on/off for the associated lane.

### Limitations

Lane arrows can't be changed on junctions using:

* [](Lane-Connectors.md)
    * Lane connectors take precedence over lane arrows.
* [](Highway-Junction-Rules.md)
    * See: **Enable highway-specific lane merging/splitting rules** in [](Policies.md) in [](Settings.md)
    * You can use [](Lane-Connectors.md) to override such junctions

### Vehicle Routing

Vehicles calculate their route _before_ starting their journey. As a result, when you change lane arrows, only vehicles
spawned _after_ that point will be aware of your changes.

To force existing vehicles to calculate new routes when you make changes, enable **Apply AI changes right away**
in [](General.md) in [](Settings.md).

### Shortcuts

The following shortcuts are applicable when the Lane Arrows tool is active...

Selection:

* `Click a segment entering a junction` — choose segment to customize
    * Any previously selected segment wil be deselected
* `Right-click anywhere` — deselect current segment
    * If no segment selected: Exit the **Lane Arrows** tool as if you pressed `Esc`
* `Esc` — exit **Lane Arrows** tool
    * Returns focus to the [](Toolbar.md) and enables its [](Adjust-Roads.md) mode.

Basic Applicators:

> These are applied to the currently selected segment.

* `Click an arrow button` - toggle the direction on/off
* `Delete` or `Backspace` - reset selected segment arrows to default state

Bulk applicators:

> See [](Dedicated-Turning-Lanes.md) guide for more information.

* `Alt`+`Click segment entering a junction` - Automatically configure turning lanes for that segment
    * Repeat the shortcut to cycle through alternate configurations
* `Control`+`Click a junction` - Give all roads at the junction a turning lane
    * Same as `Alt`+`Click`, but configures all segments entering the junction
    * Repeat the shortcut to cycle through alternate configurations
* [](Priority-Signs.md) bulk applicators can add turning lanes for an entire route

Camera / Overlays:

> The Lane Arrows tool does not have any overlays.

* `Mouse wheel` - zoom in or out
* `PageDown` - underground view
    * This activates a simplified version of the [](Traffic-Info-View.md)
* `PageUp` - overground view

## Notes

Unlike [](Lane-Connectors.md), which explicitly link an incoming lane to one or more outgoing lanes, the lane arrows
just set a _general direction_.

(todo: image)

You could think of this as an arc drawn around the edge of the junction, and depending on the lane arrow the arc will be
mostly to the left, ahead, right, or a mixture of those. Any road containing outgoing lanes that is within the arc is
seen as a valid exit from the junction.

## FAQ

#### Does it affect frame rate or cause lag?

> No. Vanilla game already has lane arrows, we just change where they point.

#### Vehicles are ignoring the changes I made

> * Vehicles responding to emergencies ignore lane arrows
> * [](Reckless-Drivers.md) will sometimes ignore lane arrows
> * Passenger, sightseeing and evacuation buses can ignore lane arrows, if enabled to do so...

#### Lane arrows are causing buses to take strange routes

> Buses often need extra flexibility to reach their next stop. In [Policies](Policies.md) in [Settings](Settings.md):
> * Enable **Buses may ignore lane arrows** for passenger and sightseeing buses
> * Enable **Evacuation buses may ignore traffic rules** for emergency evacuation buses

#### Painted road arrows are not reflecting my changes

> The arrows painted on the road surface are determined by the road asset, not TM:PE. Some roads have missing arrows, or
> don't show arrows at all, or show incorrect arrows (particularly if the asset was designed for traffic driving on the
> other side of the road).

#### When I load my city, my lane arrow customizations are gone

> Try unpausing the game. See [](Lane-arrow-and-connector-not-loading.md) for details.

#### Can I customize the painted road arrows?

> Yes, use [BOB, the Tree and Prop Replacer](https://steamcommunity.com/sharedfiles/filedetails/?id=2197863850) mod (or
> similar):
> 1. Open BOB and select a road
> 2. Set replacements for the arrows:  
     > ![Arrow Decals](picLaneArrows_decals.png)
>
> Note that some roads may have different names for the arrows (the arrows are toggled by hidden flags, not by name).

## See Also

[](Toolbar.md):

* [](Priority-Signs.md) -- bulk applicators can set lane arrows
* [](Lane-Connectors.md) -- a more powerful way to control traffic routes through junctions
* [](Junction-Restrictions.md) -- additional settings for junctions

[](Settings.md):

* [](Policies.md) - allow buses to ignore lane arrows

Guides:

* [](Nodes,-Segments,-Lanes.md)
* [](Dedicated-Turning-Lanes.md)

[Issue Tracker](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues):

* <a href="https://github.com/CitiesSkylinesMods/TMPE/labels/LANE ROUTING"><img alt="Issues" src="https://img.shields.io/github/issues/CitiesSkylinesMods/TMPE/LANE ROUTING?label=LANE ROUTING%26logo=github" /></a>