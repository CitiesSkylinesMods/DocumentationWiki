> Verified: December 2021 - TM:PE 11.5.2

Use this feature to make road conditions have a bigger impact on traffic speed.

## Overview

The **Snowfall DLC** introduced new game mechanics relating to road condition: Maintenance and Snow.

#### Road Maintenance (all map biomes):

* Road Maintenance depot sends out trucks to maintain your roads
* Well maintained roads allow vehicles to travel _slightly faster_
* [Road Maintenance Info View](Road Maintenance Info View) shows road state

#### Snow Coverage (only Winter biomes):

* Snow covered roads cause vehicles to travel _more slowly_
    * Studded Tires policy reduces the speed penalty
* Snow Dumps send out trucks to clear away the snow
* [Snow Info View](Snow Info View) shows road state

There are, however, two notable features missing:

* Poorly maintained roads don't incur a speed penalty
* On non-Winter biomes, water on roads doesn't incur a speed penalty

You can instruct TM:PE to add those missing features...

## Usage

Choose the **Road condition has a bigger impact on vehicle speed** in [Gameplay](Gameplay.md) [settings](Settings.md):

* Once activated, the feature is automatically applied to all roads on the map.
* The feature can be disabled at any time by turning off the option in Gameplay settings.

## Notes

The maximum speed for a road segment is based on [Speed limits](Speed-Limits.md) which are then increased or decreased depending on the road conditions as shown in the tables below.

#### Non-winter biomes

| Road wetness | Road condition | Resulting speed modifier |
| :---:        | :---:          | :---                     |
| Dry          | Maintained     | ±0 %                     |
| Wet          | Maintained     | -25 %, max. 100 km/h     |
| Dry          | Unmaintained   | -25 %, max. 80 km/h      |
| Wet          | Unmaintained   | -43.75 %, max. 80 km/h   |

You can reduce road wetness using the **Pumping** service, and improve road condition using the **Road Maintenance** service.

#### Winter biome

| Snow coverage | Road condition |Studded Tires policy | Resulting speed modifier |
| :---:         | :---:          | :---:               | :---                     |
| None          | Maintained     | Enabled/Disabled    | ±0 %                     |
| Covered       | Maintained     | Enabled             | max. 40 km/h             |
| Covered       | Maintained     | Disabled            | max. 20 km/h             |
| None          | Unmaintained   | Enabled/Disabled    | -25%, max. 80 km/h       |
| Covered       | Unmaintained   | Enabled             | -43.75%, max. 40 km/h    |
| Covered       | Unmaintained   | Enabled             | -43.75%, max. 20 km/h    |

You can reduce snow coverage using the **Snow Plough** service, and improve road condition using the **Road Maintenance** service.

#### Individual driving styles

> Note: This option was called **Realistic driving speeds** in TM:PE version 10.20 and earlier.

If [Individual Driving Styles](Individual Driving Styles) is enabled, its speed calculations are applied _after_ the road condition calculations above. However, at any time it is guaranteed that the resulting speed limit does not fall below 10 km/h.

## FAQ

#### Does it affect framerate or cause lag?
> Slightly, but barely noticeable - even on big cities.

#### Does it affect train/tram/monorail/metro tracks?
> Not currently.

#### Does it affect pedestrians and cyclists?
> Not currently.

#### Does it affect ships and aircraft?
> Not currently.

#### Does it affect breaking and acceleration?
> Not directly, but by changing speeds it affects the amount of breaking and acceleration required by vehicles.

## See also

[Settings](Settings.md):

* [Gameplay](Gameplay.md) - option: **Road condition has a bigger impact on vehicle speed**

Info Views:

* [Road Maintenance](Road-Maintenance-Info-View.)
* [Snow](Snow-Info-View.)

Cities: Skylines official wiki:

* [Road maintenance](https://skylines.paradoxwikis.com/Roads#Maintenance)
* [Snow](https://skylines.paradoxwikis.com/Weather#Snow)

Old TM:PE wiki:

* [Road condition has a bigger impact on vehicle speed](https://tmpe.viathinksoft.com/wiki/index.php?title=Road_condition_has_a_bigger_impact_on_vehicle_speed)