# Lane Connectors

> Verified: January 2021 - TM:PE 11.5.2 / TM:PE 11.6

## Overview

Use this tool to customise the allowed routes traffic can take at junctions and nodes.

> Tip: If you want a simpler alternative, use [Lane Arrows](Lane-Arrows.md) instead.

## Usage

This tool can be applied to nodes and junctions on:

* Roads
* Tram tracks
* Metro tracks
* Rail tracks
* Monorail tracks
* Level crossings

### Activate

Choose **Lane Arrows** on the [Toolbar](Toolbar.md):

![Lane Connector tool](https://imgur.com/fhxfKzv.png)

Button missing? Enable **Lane Connectors** in [Maintenance](Maintenance.md) [settings](Settings.md).

You can set a keyboard shortcut to activate the tool in the [Key Bindings](Keybinds.md) [settings](Settings.md).

### Overlays

While the tool is active, detailed overlays will show all nodes customised with lane connectors:

(todo: image)

To see the lane connectors for more distant nodes, scroll the camera towards them. Depending on camera position, you might need to zoom in a little.

Unlike most other overlays, lane connectors don't currently support transparency settings.

When the tool is deactivated, overlays will be removed. You can enable a persistent detailed overlay, which is visible whenever the [Toolbar](Toolbar.md) is visible, in [Overlays](Overlays.md) [settings](Settings.md).

### Customise

(todo - see Shortcuts for now as it summarises it)

### Shortcuts

The following shortcuts are applicable when the Lane Arrows tool is active...

Camera / Overlays:

* **Mouse wheel** - zoom in or out
    * If you zoom out too far, overlays may disappear
* **PageDown** - underground view
    * This also activates a simplified version of the [Traffic Info View](Traffic Info View)!
* **PageUp** - overground view

Selection:

* **Click a node** - select node to customise
    * Any previously selected node will be deselected
    * You can now use basic and bulk applicators
* **Right click anywhere** - deselects currently selected lane or node
* **Esc** - exit Lane Connectors tool

Basic applicators:

* **Click an incoming lane** - select the incoming lane
    * You can now click outgoing lanes
* **Click an outgoing lane** - add or remove connector to/from current incoming lane
* **Del** or **Backspace** - reset all lane connectors

Bulk applicators:

* [Stay In Lane](Stay In Lane) (hot key is **Control+S**)

### Refresh

Vehicles calculate their path before starting their journey. As a result, when you make changes to lane connectors, only vehicles spawned _after_ that point will be aware of the changes.

To force a refresh, you can:

* Enable **Customisations come in to effect immediately** in [General](General.md) [settings](Settings.md) to force vehicles to automatically recalculate their paths when lane connectors change.
    * This may add some momentary lag on old potato computers or on big cities.
* Or use the [Clear Traffic](Clear-Traffic.md) tool to remove all existing traffic from the map, leaving only newly spawned traffic that is aware of your changes. This causes less lag, but you have to do it every time.

### Deactivate

Press **Esc** or switch to any other tool when you're finished.

## Notes

Unlike [Lane Arrows](Lane-Arrows.md), which set a general direction that an incoming lane can exit by, lane connectors explicitly link to one or more outgoing lanes in any direction. Essentially, you are hard-wiring the paths that can be taken through the junction.

If an incoming lane does not connect to any outgoing lanes, it will be treated as a "lane arrow" lane - the game will deicde which outgoing lanes it can connect to.

If an outgoing lane is not connected to any incoming lanes then it is likely that no traffic can enter it, unless there is a suitable "lane arrow" incoming lane. Inaccessible outgoing lanes can wreak havoc in your city if they prevent vehicles reaching a destination.

If you have enabled **Enable highway-specific lane merging/splitting rules** in [Policies](Policies.md) [settings](Settings.md), and you override a highway junction with lane connectors, the highway rules will automatically be disabled for that junction and it will act like a normal city road junction - for all lanes at the junction, including any that aren't connected. We recommend either connecting all lanes at a highway junction, or no lanes, in order to avoid unexpected vehicle behaviour.

## FAQ

#### Does it affect frame rate or cause lag?
> Not really. The game already has to route through junctions, we just change the possible routes. However, if you go crazy with the tool you could force vehicles to take longer routes, which means more work for the pathfinder.

#### When I load my city, my lane connector customisations are gone
> Try unpausing the game. See [Lane arrow and connector not loading](Lane arrow and connector not loading) for details.

#### Can I allow buses to ignore lane connections to avoid them taking detours?
> No. Unlike [Lane Arrows](Lane-Arrows.md), the lane connectors are very strict and must be obeyed by all buses.

#### Can any vehicles ignore lane connections?
> * Only emergency vehicles which are _responding to an emergency_ can ignore lane connectors.
> * All other vehicles, including  [Reckless Drivers](Reckless-Drivers.md) and buses, must strictly obey the lane connectors at all times.

## See Also

[Toolbar](Toolbar.md):

* [Lane Arrows](Lane-Arrows.md) - a simpler and more flexible alternative to lane connectors
* [Junction Restrictions](Junction-Restrictions.md) - additional settings for junctions

[Issue Tracker](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues):

* <a href="https://github.com/CitiesSkylinesMods/TMPE/labels/LANE ROUTING"><img alt="Issues" src="https://img.shields.io/github/issues/CitiesSkylinesMods/TMPE/LANE ROUTING?label=LANE ROUTING&logo=github" /></a>