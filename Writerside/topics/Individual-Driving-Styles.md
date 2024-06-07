> Verified: January 2022 - TM:PE 11.5.2 / TM:PE 11.6

> In TM:PE v10.20 and earlier, this feature was called **Realistic speeds**. In TM:PE v10.21 it was renamed to **Individual Driving Styles** due to additional features being added.

Use this feature to give each cim their own unique driving style.

## Overview

In the vanilla game, the only difference between drivers is the vehicle asset they drive. While the vehicle asset defines some factors such as breaking, acceleration and maximum speed, it's effects on traffic are still minimal.

To make traffic more realistic, TM:PE can give each cim their own unique driving style. It determines:

* Their driving speed preferences (above/below speed limit)
* Their lane changing habits (frequent/rare lane changes)

## Usage

Enable the **Individual driving styles** option in [Gameplay](Gameplay.md) [settings](Settings.md).

Once activated, the feature is automatically applied to all drivers. The feature can be disabled at any time by turning off the option in Gameplay settings.

For even more realism, you could also activate the following options:

* [Reckless Drivers](Reckless-Drivers.md)
* [Road Conditions](Road Conditions)
* [Dynamic Lane Selection](Dynamic-Lane-Selection.md)

## Notes

When the feature is activated, each cim is given a unique 'pseudo-random seed' which will determine their driving speeds and lane changing habits.

#### Lane changes

The driving style of a cim determines when and where they will make lane changes. It helps reduce "single lane bunching", particularly near junctions ([Dedicated Turning Lanes](Dedicated Turning Lanes) also help with that).

The effect is applied in the pathfinder and, if activated, the [Advanced Vehicle AI](Advanced Vehicle AI) - specifically its [Dynamic Lane Selection](Dynamic-Lane-Selection.md) (DLS) feature. DLS further reduces lane bunching along long stretches of road, however it adds extra workload to the CPU which might be problematic on older computers.

#### Driving speed

The speed a cim drives at is determined by several factors. It can be summarised as: Maximum speed modified by individual driving style. The effect of the individual driving style is dependent on the category of vehicle being driven.

This means that if two cims were to drive the same vehicle asset, on the same road, in the same [Road Conditions](Road Conditions), they would both drive at different speeds.

#### Maximum speeds

Maximum vehicle speeds are determined by roads and vehicles:

* Roads: [Speed limits](Speed-Limits.md) and, if activated, the [Road conditions](Road conditions)
    * [Reckless drivers](Reckless-Drivers.md) ignore speed limits
* Vehicles: Maximum speed defined by the vehicle asset
    * [Advanced Vehicle Options](https://steamcommunity.com/sharedfiles/filedetails/?id=1548831935) mod can be used to view/alter the vehicle speed
    * If vehicles assets are made too fast, it can adversely affect the AIs

The lowest value is chosen. For example, if a vehicle can travel at 100 km/h, but the speed limit is 30 km/h, then the maximum speed is 30 km/h.

#### Vehicle categories

The vehicle category defines a scale of speed modification. The individual driving style determines the point on that scale that a cim will use.

| Category             | Speed modification |
| :---                 | :---:              |
| Heavy vehicles       | -10% .. ±0%        |
| [Reckless Drivers](Reckless-Drivers.md) | +10% .. +60%       |
| All other vehicles   | -20% .. +30%       |

Note: Emergency vehicles will behave like reckless drivers when they are responding to an emergency (as indicated by flashing lights and sirens).

## FAQ

#### Does this reduce frame rate or cause lag?
> On its own, the effect is minimal, even in large cities.
>  
> However, if you activate the [Dynamic Lane Selection](Dynamic-Lane-Selection.md) feature, the effects will be much more noticeable - especially in large cities.

#### What are "Heavy Vehicles"?
> * Ships (cargo, ferry)
> * Aircraft (cargo, passenger, blimp, balloon)
> * Helicopters (police, fire, ambulance, disaster recovery)
> * Meteors (requires [Natural Disasters DLC](https://store.steampowered.com/app/515191/Cities_Skylines__Natural_Disasters/?curator_clanid=6625556))
> * Tornados (requires [Natural Disasters DLC](https://store.steampowered.com/app/515191/Cities_Skylines__Natural_Disasters/?curator_clanid=6625556))
> * Space Ships (eg. ChirpX)

## See also

[Settings](Settings.md):

* [Gameplay](Gameplay.md)

[Toolbar](Toolbar.md):

* [Speed Limits](Speed-Limits.md)

Guides:

* [Reckless Drivers](Reckless-Drivers.md)
* [Road Conditions](Road Conditions)
* [Dynamic Lane Selection](Dynamic-Lane-Selection.md)