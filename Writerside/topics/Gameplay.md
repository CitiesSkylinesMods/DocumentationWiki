# Gameplay Settings

> Verified: March 2022 - TM:PE 11.6.5.1

[Settings](Settings.md): [General](General.md) | **Gameplay**
| [Policies](Policies.md) | [Overlays](Overlays.md) | [Maintenance](Maintenance.md)
| [Keybindings](Keybinds.md)

## Overview

Use these [settings](Settings.md) to make traffic more realistic.

## Settings

### Vehicle Behaviour

_Use these options to control some key aspects of vehicle behaviour throughout your city..._

#### Reckless drivers percentage

* Determines the percentage of vehicles that become [Reckless Drivers](Reckless-Drivers.md)
* Set to Holy City (0%) to disable

#### Individual driving styles

> In TM:PE v10.20 and earlier, this option was called [Realistic Speeds](Realistic-Speeds.md).

* When enabled, each driver will have a slightly different driving style:
    * They may drive slightly faster or slower than the speed limit
    * They will choose different places to make lane changes
* For best results with lane changes, enable the **Advanced Vehicle AI** and set **Dynamic Lane Selection** slider to a
  non-zero value.
* See: [Individual Driving Styles](Individual-Driving-Styles.md)

#### Road condition has a bigger impact on vehicle speed

> This feature requires **Snowfall DLC**

* When enabled:
    * Poorly maintained roads will cause vehicles to slow down (all biomes)
    * Wet/flooded roads will cause vehicles to slow down (non-winter biomes)
*

See: [Road Conditions](Road-Conditions.md), [Snow Info View](Snow-Info-View.md), [Road Maintenance Info View](Road-Maintenance-Info-View.md)

#### Disable despawning

> Vehicle **despawning** is a feature of the vanilla game, and causes vehicles to disappear if they get stuck in traffic
> too long. While that helps reduce traffic jams, it's not very realistic.

* When enabled, this prevents vehicles from "despawning"
* See: [Toggle Despawn](Toggle-Despawn.md)

#### Filter Disable despawning vehicle types

> These filters only apply when **Disable Despawning** is active. This feature was added in TM:PE 11.6.5.1.

* Allows you to allow _some_ vehicle types to always despawn
* See: [Toggle Despawn](Toggle-Despawn.md)

### Advanced Vehicle AI

_Use these options to improve road lane usage throughout your city..._

#### Enable Advanced AI

* Vehicles will try and avoid congested routes
* Lanes usage is more evenly distributed
* See: [Advanced AI](Advanced-AI.md)

#### Dynamic lane selection

* Determines the rate at which vehicles will change lanes on long roads
* See: [Dynamic Lane Selection](Dynamic-Lane-Selection.md)

### Parking AI

_Use this option to make car parking behaviour mandatory and more realistic..._

#### Enable more realistic parking

* If enabled:
    * Prevents "magic pocket cars" (where cims magically have a car after getting off the bus, for example)
    * Encourages cims to actually find a parking space near their destination
    * Encourages cims to return to their car to drive home afterward
* See: [Parking AI](Parking-AI.md)

### Public Transport

_Use this option to make cims behave more realistically at stations..._

#### Prevent unnecessary transfers at public transport stations

* If enabled, adds a pathfinding cost when a cim switches from one public transport route to another
* This reduces the chance that cims will try to use public transport to get from one side of a station to another!
* See: [Prevent unnecessary transfers](Prevent-Unnecessary-Transfers.md)

## FAQ

#### Do these settings affect frame rate or cause lag?

> The following settings, if enabled, can cause lag on old computers or big cities with lots of vehicles:
> * **Dynamic lane selection**
> * **Parking AI**

#### Which settings are best for full lane usage?

> * Enable **Individual driving styles** and **Advanced vehicle AI**
> * Experiment with the **Dynamic lane selection** (DLS) setting
> * Note that DLS often works best when the slider is somewhere in the middle, because reasons.

## See Also

[Settings](Settings.md):

* [Policies](Policies.md)
* [Global Configuration](Global-Configuration.md) - if you want to fine-tune gameplay values

[Toolbar](Toolbar.md):

* [Parking Restrictions](Parking-Restrictions.md)
* [Speed Limits](Speed-Limits.md)
* [Toggle Despawn](Toggle-Despawn.md)

[TM:PE v10.x Wiki](https://tmpe.viathinksoft.com/wiki):

* [Gameplay options](https://tmpe.viathinksoft.com/wiki/index.php?title=Options#Gameplay)

[Issue Tracker](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues):

* <a href="https://github.com/CitiesSkylinesMods/TMPE/labels/SETTINGS"><img alt="Issues" src="https://img.shields.io/github/issues/CitiesSkylinesMods/TMPE/SETTINGS?label=SETTINGS&logo=github" /></a>