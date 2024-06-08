# Toggle Traffic Lights

> Verified: February 2020 - TM:PE 11.0

## Overview

Use this tool to quickly toggle traffic lights at a junction.

## Usage

This tool can be applied to:

* Road junction nodes (may also work with transition nodes, but unreliable)
* Train junction nodes

Notably, it can _not_ be applied to:

* Level crossings - traffic lights are mandatory
* Timed traffic lights - they are protected to avoid accidental deletion

### Activate

Choose **Toggle Traffic Lights** on the [](Toolbar.md):

![Toggle Traffic Lights tool](btnToggleTL.png)

You can set a keyboard shortcut to activate the tool in the [Key Bindings](Keybinds.md) in [](Settings.md).

### Overlays

While the tool is active, suitable junctions will have icons depicting whether junctions have traffic lights:

(todo: image)

To see icons for more distant roads and tracks, scroll the camera towards them. Depending on camera position, you might
need to zoom in a little. You can set the **Overlay Transparency** in [](General.md) in [](Settings.md).

When the tool is deactivated, overlays will be removed.

You can enable a persistent summary overlay for [](Timed-Traffic-Lights.md), which is visible
whenever the [](Toolbar.md) is visible, in [Overlays](Overlays.md) in [](Settings.md).

### Icons

|  Icon  | Meaning                     |
|:------:|:----------------------------|
| (todo) | No traffic light            |
| (todo) | Normal traffic light        |
| (todo) | [](Timed-Traffic-Lights.md) |

### customize

While the tool is active, click on a traffic light to toggle it on/off.

> Use the [](Timed-Traffic-Lights.md) tool to add/remove timed traffic lights.

### Shortcuts

Camera / Overlays:

* **Mouse wheel** - zoom in or out
    * If you zoom out too far, icons may disappear
* **PageDown** - underground view
    * This also activates a simplified version of the [](Traffic-Info-View.md)!
* **PageUp** - overground view

Selection:

* **Esc** - exit Toggle Traffic Lights tool

Basic applicators:

* **Click an icon** - toggle the traffic light on/off

Bulk applicators:

* **Remove all existing traffic lights** in [](Maintenance.md) in [](Settings.md) - remove all **normal**
  traffic lights
    * Does _not_ remove [](Timed-Traffic-Lights.md)

### Deactivate

Press **Esc** or switch to any other tool when you're finished.

## Notes

The tool is very similar to *
*[Info Views > Traffic Routes > Junctions](https://skylines.paradoxwikis.com/Roads#Traffic_Routes)** but with the
advantage of not being able to accidentally delete [](Timed-Traffic-Lights.md) which can be
time-consuming to program.

> [](Reckless-Drivers.md) ignore traffic lights!

## FAQ

#### Does it affect frame rate or cause lag?

> No. It's just an easy way to do something the game already does.

#### Traffic lights aren't appearing at the junction

> This can happen on custom road assets if they don't include traffic light props; check with the asset author.
> Highways, in particular, rarely have traffic lights as they will be expecting on/off ramps instead.

#### There's different styles of traffic lights at my junction!

> The traffic light props are defined by the road or track asset. If you have two different assets it's possible that
> they have different traffic light styles.

## See Also

[](Settings.md):

* [](Policies.md) - toggle automatic traffic lights where applicable
* [](Maintenance.md) - bulk delete all normal traffic lights on the map

[](Toolbar.md):

* [](Timed-Traffic-Lights.md)
* [Manual Traffic Lights](Manual-Traffic-Lights.md)
* [](Junction-Restrictions.md)
* [](Lane-Arrows.md)
* [](Lane-Connectors.md)