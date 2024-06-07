# Speed Limits

> Under construction
>
> ### This documentation is for **TM:PE 11.6.2 and later**
>
> If you are using TM:PE 11.5.2 STABLE, or TM:PE 11.6.1 TEST, or older versions, please refer to the old
> documentation: [[Speed Limits 11.5]]

## Overview

Use this tool to set speed limits for **road** and **tracked** (metro, train, monorail, tram, trolleybus) networks.

## Usage

Choose **Speed Limits** on the [](Toolbar.md):

![Speed limit button](btnSpeedLimits.png)

> Button missing? Enable **Speed Limits** in [](Maintenance.md) in [](Settings.md).

You can set a keyboard shortcut to activate the tool in the [Key Bindings](Keybinds.md) in [](Settings.md).

### Applicators

The speed palette controlls the various modes of the speed limits tool, and determines what speed will be set when
clicking speed icons on the map.

![Speed Palette](picSpeedLimits_paletteNew.png)

> Reposition it by dragging the title bar. Change the size and opacity of the palette in [](General.md)
> in [](Settings.md).

#### Mode buttons

These buttons determine how speeds are applied.

|                                          Button                                           | Purpose                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     ![Segment mode](picSpeedLimits_segment.png) ![Lane mode](picSpeedLimits_lane.png)     | Toggles between **Segment** vs. **Lane** mode. <br /><br /> The button shows the current mode; clicking it changes to the other mode. <br /><br /> See **Setting Speeds** section for details.                   |
| ![Override mode](picSpeedLimits_override.png) ![Default mode](picSpeedLimits_default.png) | Toggles between **Speed Overrides** vs. **Default Speeds** mode. <br /><br /> The button shows the current mode; clicking it changes to the other mode. <br /><br /> See **Default Speeds** section for details. |
|              ![MPH](picSpeedLimits_mph.png) ![km/h](picSpeedLimits_kmph.png)              | Toggles between **Miles Per Hour** (MPH) and **Kilometers per Hour** (km/h) mode. <br /><br /> See **Icon Themes** section for details.                                                                          |

#### Speed bar buttons

These buttons choose the speed to be applied.

| Button | Purpose                                                                           |
|:------:|:----------------------------------------------------------------------------------|
| (todo) | Reset speed to default. <br /><br /> See **Reset Speeds** section for details.    |
| (todo) | Choose speed to apply. <br /><br /> See **Setting Speeds** section for details.   |
| (todo) | Choose unlimited speed. <br /><br /> See **Unlimited Speed** section for details. |

### Default Speeds

Default speeds are represented by green circular speed icons:

![Default speed icon](picSpeedLimits_defaultIcon.png)

Default speeds are defined by network assets (roads, tracks, etc.), but you can customise them if desired:

1. Activate default speeds mode (button lit)  
   ![Default mode](picSpeedLimits_default.png)
2. Select desired speed on the Speed Bar
3. Click a speed icon on the map to apply that speed

This will set the default speed for all elevations (ground, elevated, bridge, slope, tunnel) of that network asset.

### Setting Speeds

Lane and segment speed overrides are shown in your chosen speed icon theme (see **Icon Themes** section for details):

![Various Speeds](picSpeedLimits_example.png)

To change a speed:

1. Choose **Segment** or **Lane** mode  
   ![Segment mode](picSpeedLimits_segment.png) ![Lane mode](picSpeedLimits_lane.png)
2. Select desired speed on the Speed Bar
3. Click a speed icon on the map to apply that speed

> Note: When setting the speed of a tram track that's part of a road, both the road and the tram track will be set to
> the same speed.

### Unlimited Speed

Setting a network, segment or lane to this speed removes its speed limit, allowing vehicles to reach their maximum
speed.

This is particularly useful if you're using high speed train tracks.

> You can customise vehicle speeds
> using [Advanced Vehicle Options](https://steamcommunity.com/sharedfiles/filedetails/?id=1548831935)
> or [Customise It Extended](https://steamcommunity.com/sharedfiles/filedetails/?id=1806759255) mod.

### Reset Speeds

To reset customised speeds to default values:

1. Select the **Reset** button on the speed bar  
   (todo: image)
2. Click a speed icon on the map to revert it to default speed

> If you are in default speeds mode, resetting will restore the speed defined by the network asset.

### Shortcuts

The following shortcuts are applicable when the Speed Limits tool is active...

Selection:

* `Esc` or `Right mouse click` - exit Speed Limits tool
    * Returns focus to the [](Toolbar.md) and enables its [](Adjust-Roads.md) mode.

Modes:

> You can set speeds while using temporary mode toggles.

* `Ctrl/Cmd` - temporarily toggle between segment vs. lane mode
* `Alt` - temporarily toggle between default vs. override mode

Speeds:

> These select/change speed on the speed bar.

* `Alt`+`0-9` - pick speed (eg. `Alt`+`1` = 10, `Alt`+`6` = 60, etc.)
* `-` or `Numpad -` - reduce picked speed (e.g. if speed bar is `50`, it will change to `45`)
* `=` or `Numpad +` - increase picked speed
* `/` - pick unlimited speed
* `Delete` or `Backspace` - speed reset tool

Applicators:

* `Click a speed icon` - change network/segment/lane speed to the speedbar speed
* `Shift`+`Click a speed icon` - change speed and apply that change along the route
    * This is only applicable in segment/lane speed override mode.

Bulk Applicators:

* [](Roundabout-Policies.md) - set speed, based on curvature, for entire roundabout

Camera / Overlays:

* `Mouse wheel` - zoom in or out
    * If you zoom out too far, icons may disappear
* `PageDown` - underground view
    * This also activates a simplified version of the [](Traffic-Info-View.md)
* `PageUp` - overground view

### Overlays

While the tool is active, icons indicate speeds (relevant to current tool mode) of nearby roads and tracks:

![Speeds overlay](picSpeedLimits_speedsOverlay.png)

To see icons for distant roads/tracks, move the camera towards them. **Overlay transparency** can be set
in [](General.md) in [](Settings.md).

When the tool is deactivated, overlays will be removed. A persistent overlay, which shows speed limits whenever
the [](Toolbar.md) is visible, can be enabled in [Overlays](Overlays.md) in [](Settings.md).

### Icon Themes

The icon theme is set via [](General.md) in [](Settings.md) and determines the visual appearance of overlay icons and
also the units to use - either `km/h` (kilometers per hour) or `MPH` (miles per hour) scale, depending on the theme.

> The game uses its own speed units, which are neither `km/h` nor `mph`.
> See [`Constants.cs`](https://github.com/CitiesSkylinesMods/TMPE/blob/master/TLM/TLM/Constants.cs) for details on how
> we
> convert between game units and real units.

| Style        |                   Example                   |      Units      |
|:-------------|:-------------------------------------------:|:---------------:|
| American     |     ![American](picSpeedLimits_usa.png)     |       MPH       |
| Brazilian    |   ![Brazilian](picSpeedLimits_brazil.png)   |      km/h       |
| British      |      ![British](picSpeedLimits_uk.png)      |       MPH       |
| Canadian     |   ![Canadian](picSpeedLimits_canada.png)    |      km/h       |
| French       |    ![French](picSpeedLimits_france.png)     |      km/h       |
| German       |    ![German](picSpeedLimits_germany.png)    | km/h <br /> MPH |
| Indonesian   | ![Indonesian](picSpeedLimits_indonesia.png) |      km/h       |
| Japanese     |    ![Japanese](picSpeedLimits_japan.png)    |      km/h       |
| South Korean | ![South Korean](picSpeedLimits_sKorea.png)  |      km/h       |
| Swedish      |    ![Swedish](picSpeedLimits_sweden.png)    |      km/h       |

> Want to contribute an icon theme for your country? See: [](Speed-Limit-Icon-Themes.md)

## FAQ

> Q: Does it affect frame rate or cause lag?
>> A: No. The vanilla game already has to check speeds for each network segment; this tool just alters the speeds.

> Q: Some drivers ignore speed limits
>> A: The following vehicles can ignore speed limits:
>> * Emergency vehicles when their sirens are active (responding to emergency)
>> * [](Reckless-Drivers.md); if **Reckless driving** enabled in [](Gameplay.md)
>> * Evacuation [Buses](Buses.md); if **Evacuation buses may ignore traffic rules** enabled in [](Policies.md)

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