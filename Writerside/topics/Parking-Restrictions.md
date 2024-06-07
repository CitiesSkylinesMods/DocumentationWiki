# Parking Restrictions

> Verified: December 2021 - TM:PE 11.5.2

## Overview

Use this tool to toggle roadside parking lanes on or off.

## Usage

Choose **Parking Restrictions** on the [](Toolbar.md):

![Parking button](https://imgur.com/JgZQ7ke.png)

> Button missing? Enable **Parking Restrictions** in [](Maintenance.md) in [](Settings.md).

### Applicators

**Click an icon** to toggle the parking state of the associated lane.

|Allow|Deny |
|:---:|:---:|
|![Allow](https://imgur.com/HXSjolO.png)|![Deny](https://imgur.com/LMf5HwQ.png)|

Changes are applied instantly and any cars already parked there will teleport to other parking spaces nearby. However, some traffic that was planning to park in the area might still try parking, but will quickly notice the changes and look for alternate locations.

### Shortcuts

The following shortcuts are available when the Parking Restrictions tool is active...

Selection:

* `Esc` or `Right mouse click` - exit **Parking Restrictions** tool
    * Returns focus to the [](Toolbar.md) and enables its [](Adjust Roads) mode.

Basic applicators:

* `Click an icon` - toggle associated parking lane on/off
* `Shift`+`Click an icon` - toggle parking lane on/off between junctions

Camera / Overlays:

* `Mouse wheel` - zoom in or out
    * If you zoom out too far, overlays may disappear
* `PageDown` - underground view
    * This activates a simplified version of the [](Traffic Info View)
* `PageUp` - overground view

### Overlays

While the tool is active, icons show the state of nearby parking lanes:

(todo: image)

To see icons for distant roads, move the camera towards them. **Overlay transparency** can be set in [](General.md) in [](Settings.md).

When the tool is deactivated, overlays will be removed. A persistent overlay, which shows where parking is restricted whenever the [](Toolbar.md) is visible, can be enabled in [Overlays](Overlays.md) in [](Settings.md).

## FAQ

#### Does this affect frame rate or cause lag?
> Not directly, however if it results in cims needing to drive futher to find parking that will create more work for the pathfinder.

#### The mouse is hovering a parking icon but the lane doesn't highlight
> This is due to road asset that set parking lane `direction` to `Both`, rather than `Forward` or `Backward`. TM:PE settings currently can't handle the `Both` setting, so this is something we need to fix (see [Issue #827](https://github.com/CitiesSkylinesMods/TMPE/issues/827#issuecomment-613203413) for details).

#### When I alter my city, parked cars sometimes move in to disabled parking lanes
> This is due to the `direction` issue mentioned above. See [Issue #676](https://github.com/CitiesSkylinesMods/TMPE/issues/676) for more details.

#### What happens if I disable all roadside parking?
> * Cims will be limited to using parking spaces in buildings
> * If you have enabled [](Parking-AI.md), it might prevent cims reaching their destination
> * A lack of parking near public transport hubs and stations could prevent cims using them

#### Can I repurpose the parking lane in to something else?
> No, but we are thinking about it. See: [Issue #515](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues/515)

#### Some roads don't have parking icons?
> * The road has to support in-road parking lanes; there's no way to add parking to roads that don't support it.
> * Green 'parking allowed' icons aren't shown in the persistent summary [Overlays](Overlays.md); they only appear while the parking restrictions tool is active.
> * Parking icons disappear if the road is too far from the camera; move the camera closer to the road.

#### I have a one way road with parking on both sides, but only get one parking icon
> This is a known issue which will hopefully be fixed in future update; see: [Issue #516](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues/516)

#### Some vehicles still use the parking lanes
> [](Reckless-Drivers.md) ignore parking restrictions.

#### Does it work on [Parking Lot Roads](https://steamcommunity.com/sharedfiles/filedetails/?id=1285201733)?
> No. They use special 'building props': Use [Find It!](https://steamcommunity.com/sharedfiles/filedetails/?id=837734529) to add, [Move It!](https://steamcommunity.com/sharedfiles/filedetails/?id=1619685021) to move/copy, and bulldozer to delete. For better placement of Parking lots, try the [Parking Lot Snapping](https://steamcommunity.com/sharedfiles/filedetails/?id=2594569657) mod.

#### Can I remove parking spaces from buildings?
> Not with TM:PE.  You can try [BOB, the Tree and Prop Replacer](https://steamcommunity.com/sharedfiles/filedetails/?id=2197863850) which can remove parking props and parking markers from buildings.

#### Why don't parking meter props change?
> They're randomly placed during road creation or upgrade; they won't change to reflect parking availability. You can try [BOB, the Tree and Prop Replacer](https://steamcommunity.com/sharedfiles/filedetails/?id=2197863850) which can remove parking meter props from networks.

#### Why don't lane markings change?
> Lane markings are 'hard coded' in to the road design; they won't change to reflect parking availability. If you want full control over lane markings, you could try [Blank Roads 3](https://steamcommunity.com/workshop/filedetails/?id=2625740281) assets along with the [Intersections Marking Tool](https://steamcommunity.com/sharedfiles/filedetails/?id=2140418403) (it can be used on road segments too, not just junctions).

#### Why are only local residents parking here?
> The **Old Town** [](City and District Policies) cause that to happen.

## See Also

[](Settings.md):

* [](Parking-AI.md) - improved parking, particularly in large car parks
* [Overlays](Overlays.md) - toggle persistent overlay

[](Toolbar.md):

* [](Vehicle-Restrictions.md)
* [](Junction-Restrictions.md)

[Issue Tracker](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues):

* <a href="https://github.com/CitiesSkylinesMods/TMPE/labels/PARKING"><img alt="Issues" src="https://img.shields.io/github/issues/CitiesSkylinesMods/TMPE/PARKING?label=PARKING&logo=github" /></a>