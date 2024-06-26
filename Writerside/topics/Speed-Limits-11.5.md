# Speed Limits (11.5.2 and earlier)

> Verified: December 2021 - TM:PE 11.5.2

> # This documentation is for **TM:PE 11.5.2 and earlier**.
>
> If you are using **TM:PE 11.6 or later**, please refer to the new documentation: [](Speed-Limits.md)

## Overview

Use this tool to set custom speed limits for roads and tracks.

## Usage

This tool can be applied to:

* Roads
* Tram tracks
* Monorail tracks
* Metro tracks
* Train tracks

### Activate

Choose **Speed Limits** on the [](Toolbar.md):

![Speed limit button](btnSpeedLimits.png)

Button missing? Enable **Speed Limits** in [](Maintenance.md) in [](Settings.md).

You can set a keyboard shortcut to activate the tool in the [Key Bindings](Keybinds.md) in [](Settings.md).

### Overlays

While the tool is active, detailed overlays show the current speeds of all roads and tracks on the map:

![Speeds overlay](picSpeedLimits_speedsOverlay.png)

To see speeds for more distant roads and tracks, scroll the camera towards them. Depending on camera position, you might
need to zoom in a little. You can set the **Overlay Transparency** in [](General.md) in [](Settings.md).

When the tool is deactivated, overlays will be removed. You can enable a persistent summary overlay, which is visible
whenever the [](Toolbar.md) is visible, in [Overlays](Overlays.md) in [](Settings.md).

### customize

When the tool is active, you'll see a palette containing available speed options:

![Speed palette](picSpeedLimits_palette.png)

To change speeds, copy them from the palette and paste them on to icons on the map:

* **Copy:** Click button on panel
* **Paste:** Click icon on map

> Note: When setting the speed of a tram track that's part of a road, both the road and the tram track will be set to
> the same speed.

### Shortcuts

The following shortcuts are applicable when the Speed Limits tool is active...

Camera / Overlays:

* **Mouse wheel** - zoom in or out
    * If you zoom out too far, icons may disappear
* **PageDown** - underground view
    * This also activates a simplified version of the [](Traffic-Info-View.md)!
* **PageUp** - overground view

Selection:

* **Ctrl** (or **Cmd** on Macs) - toggle between direction and lane-wise mode
* **Esc** - exit Speed Limits tool

Basic applicators:

* **Click a sign** - change speed (to whatever you selected on speed palette)
* **Shift + Click a sign** - change speed and apply that change along the route

### Extras

The palette has some other options:

* **Default speed limits:** Allows you to set default speed limits for roads and rails.
  > *
  See [old documentation](https://tmpe.viathinksoft.com/wiki/index.php?title=Speed_limits#Default_speed_limits_per_road_type)
  for current implementation
  > * See [Issue #12](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues/12) for
      discussion of improvements
* **Show lane-wise speed limits:** When enabled, you can set the speed for each lane individually.
* **Display speed limits as MPH instead of km/h:** When enabled, speeds will be shown in miles per hour
  > You can also customize the icon style in [](General.md) in [](Settings.md).

### Refresh

Traffic will automatically adapt to changed speed limits, usually after a few seconds but could be longer on big cities
or potato computers.

Why the delay? To simulate so many vehicles, the game uses a trick called "Leader Vehicles"; when there's a group of
vehicles driving the same route, all the computationally expensive calculations of the leader are reused by the
followers. So if the leader already drove on the segment(s) at the old speeds, the followers will do the same.

### Deactivate

Press **Esc** or switch to any other tool when you're finished.

## FAQ

> Q: Does it affect frame rate or cause lag?
>> A: No. The vanilla game already has to check road and rail speeds for each network segment, TM:PE just redirects
> > those checks to a different list.

> Q: Some drivers ignore speed limits
>> A: The following vehicles can ignore speed limits:
>> * Emergency vehicles when their sirens are active (responding to emergency)
>> * [](Reckless-Drivers.md); if **Reckless driving** enabled in [](Gameplay.md)
>> * Evacuation [](Buses.md); if **Evacuation buses may ignore traffic rules** enabled in [](Policies.md)

> Q: Pedestrian and cycle paths don't get speed icons
>> A: Use these mods to control their speeds:
>> * [Advanced Vehicle Options](https://steamcommunity.com/sharedfiles/filedetails/?id=1548831935) - set speed of the
     bicycle 'vehicles' (they appear in Citizen category)
>> * [Realistic Walking Speed](https://steamcommunity.com/sharedfiles/filedetails/?id=1412844620) - set speed of
     pedestrians (works well with [RealTime](https://steamcommunity.com/sharedfiles/filedetails/?id=1420955187) mod)

## See Also

[](Settings.md):

* [](General.md) - choose MPH speed icon style (British, German, USA)
* [Key Bindings](Keybinds.md) - choose shortcut to activate tool

Advanced:

* [](Reckless-Drivers.md)
* [](Road-Conditions.md)

[Issue Tracker](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues):

* <a href="https://github.com/CitiesSkylinesMods/TMPE/labels/SPEED LIMITS"><img alt="Issues" src="https://img.shields.io/github/issues/CitiesSkylinesMods/TMPE/SPEED LIMITS?label=SPEED LIMITS%26logo=github" /></a>