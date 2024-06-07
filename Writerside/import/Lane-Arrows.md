> Verified: December 2021 - TM:PE 11.5.2

## Overview

Lane arrows can be used to organise traffic flow across road junctions and level crossings.

> Arrows only affect normal road traffic. To customise tracked junctions, use [Lane Connectors](Lane Connectors) instead.

## Usage

Choose **Lane Arrows** on the [Toolbar](Toolbar):

![Lane arrows tool](https://imgur.com/y9KjHFD.png)

You can set a keyboard shortcut to activate the tool in the [Keybinds](Keybinds) [settings](settings).

### Applicators

> See the **Shortcuts** section below for more applicators!

1. **Click a road segment at a junction** to edit it.
2. A panel appears showing arrows for each lane:  
    ![Lane Arrows](https://user-images.githubusercontent.com/1386719/146688808-4f8882a7-ba22-4073-9d41-7eca7034c335.png)  
    > In the image above, traffic entering from **Lane 1** must turn left, while **Lane 2** can go straight ahead or right.
3. **Click arrow buttons** to toggle direction on/off for the associated lane.

### Limitations

Lane arrows can't be changed on junctions using:

* [Lane Connectors](Lane Connectors)
    * Lane connectors take precedence over lane arrows.
* [Highway Junction Rules](Highway Junction Rules)
    * See: **Enable highway-specific lane merging/splitting rules** in [Policies](Policies) [settings](settings)
    * You can use [Lane Connectors](Lane Connectors) to override such junctions

### Vehicle Routing

Vehicles calculate their route _before_ starting their journey. As a result, when you change lane arrows, only vehicles spawned _after_ that point will be aware of your changes.

To force existing vehicles to calculate new routes when you make changes, enable **Apply AI changes right away** in [General](General) [settings](settings).

### Shortcuts

The following shortcuts are applicable when the Lane Arrows tool is active...

Selection:

* `Click a segment entering a junction` - choose segment to customise
    * Any previously selected segment wil be deselected
* `Right-click anywhere` - deselect current segment
    * If no segment selected: Exit the **Lane Arrows** tool as if you pressed `Esc`
* `Esc` - exit **Lane Arrows** tool
    * Returns focus to the [Toolbar](Toolbar) and enables its [Adjust Roads](Adjust Roads) mode.

Basic Applicators:

> These are applied to the currently selected segment.

* `Click an arrow button` - toggle the direction on/off
* `Delete` or `Backspace` - reset selected segment arrows to default state

Bulk applicators:

> See [Dedicated Turning Lanes](Dedicated Turning Lanes) guide for more information.

* `Alt`+`Click segment entering a junction` - Automatially configure turning lanes for that segment
    * Repeat the shortcut to cycle through alternate configurations
* `Control`+`Click a junction` - Give all roads at the junction a turning lane
    * Same as `Alt`+`Click`, but configures all segments entering the junction
    * Repeat the shortcut to cycle through alternate configurations
* [Priority Signs](Priority Signs) bulk applicators can add turning lanes for an entire route

Camera / Overlays:

> The Lane Arrows tool does not have any overlays.

* `Mouse wheel` - zoom in or out
* `PageDown` - underground view
    * This activates a simplified version of the [Traffic Info View](Traffic Info View)
* `PageUp` - overground view

## Notes

Unlike [Lane Connectors](Lane Connectors), which explictitly link an incoming lane to one or more outgoing lanes, the lane arrows just set a _general direction_.

(todo: image)

You could think of this as an arc drawn around the edge of the junction, and depending on the lane arrow the arc will be mostly to the left, ahead, right, or a mixture of those. Any road containing outgoing lanes that is within the arc is seen as a valid exit from the junction.

## FAQ

#### Does it affect frame rate or cause lag?
> No. Vanilla game already has lane arrows, we just change where they point.

#### Vehicles are ignoring the changes I made
> * Vehicles responding to emergencies ignore lane arrows
> * [Reckless Drivers](Reckless Drivers) will sometimes ignore lane arrows
> * Passenger, sightseeing and evacuation buses can ignore lane arrows, if enabled to do so...

#### Lane arrows are causing buses to take strange routes
> Buses often need extra flexibility to reach their next stop. In [Policies](Policies) [settings](settings):
> * Enable **Busses may ignore lane arrows** for passenger and sightseeing buses
> * Enable **Evacuation busses may ignore traffic rules** for emergency evacuation buses

#### Painted road arrows are not reflecting my changes
> The arrows painted on the road surface are determined by the road asset, not TM:PE. Some roads have missing arrows, or don't show arrows at all, or show incorrect arrows (particularly if the asset was designed for traffic driving on the other side of the road).

#### When I load my city, my lane arrow customisations are gone
> Try unpausing the game. See [Lane arrow and connector not loading](Lane arrow and connector not loading) for details.

#### Can I customise the painted road arrows?
> Yes, use [BOB, the Tree and Prop Replacer](https://steamcommunity.com/sharedfiles/filedetails/?id=2197863850) mod (or similar):
> 1. Open BOB and select a road
> 2. Set replacements for the arrows:  
>     ![Arrow Decals](https://user-images.githubusercontent.com/1386719/146689817-030b086a-aa30-4b31-bf7b-c58753009b8e.png)
>  
> Note that some roads may have different names for the arrows (the arrows are toggled by hidden flags, not by name).

## See Also

[Toolbar](Toolbar):

* [Priority Signs](Priority Signs) -- bulk applicators can set lane arrows
* [Lane Connectors](Lane Connectors) -- a more powerful way to control traffic routes through junctions
* [Junction Restrictions](Junction Restrictions) -- additional settings for junctions

[Settings](Settings):

* [Policies](Policies) - allow buses to ignore lane arrows

Guides:

* [[Nodes, Segments, Lanes]]
* [Dedicated Turning Lanes](Dedicated Turning Lanes)

[Issue Tracker](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues):

* <a href="https://github.com/CitiesSkylinesMods/TMPE/labels/LANE ROUTING"><img src="https://img.shields.io/github/issues/CitiesSkylinesMods/TMPE/LANE ROUTING?label=LANE ROUTING&logo=github" /></a>