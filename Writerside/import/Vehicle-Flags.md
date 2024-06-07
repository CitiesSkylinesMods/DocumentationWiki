> Verified: April 2022 - TM:PE 11.6.5.2

## Overview

This article contains some info on what the various vehicle flags do.

⚠️ Note that some vehicles, particularly aircraft, use flags in unexpected ways.

> Please edit more info in if you have it.

### `Vehicle.Flags`

| Flag               | Value          | Purpose |
| :---               | :---           | :---    |
| `Created`          | `0x1`          | |
| `Spawned`          | `0x2`          | |
| `Deleted`          | `0x4`          | |
| `Inverted`         | `0x8`          | [Inverts (rotate 180°) the vehicle; used for train trailer rotation](https://cslmodding.info/asset/vehicle/#sub-mesh-flag-inverted). |
| `TransferToTarget` | `0x10`         | |
| `TransferToSource` | `0x20`         | |
| `Emergency1`       | `0x40`         | <ul><li>[Emergency vehicle lights flashing](https://github.com/CitiesSkylinesMods/TMPE/issues/1229#issuecomment-996881397).</li><li>`BlimpAI`: [Show alternate adverts](https://cslmodding.info/asset/vehicle/#sub-mesh-flag-emergency1).</li></ul> |
| `Emergency2`       | `0x80`         | <ul><li>[Emergency vehicle on-scene](https://github.com/CitiesSkylinesMods/TMPE/issues/1229#issuecomment-996881397) (eg. collecting corpse, tackling fire, pumping water, etc).</li><li>`BlimpAI`: [Show alternate adverts](https://cslmodding.info/asset/vehicle/#sub-mesh-flag-emergency2).</li></ul>|
| `WaitingPath`      | `0x100`        | |
| `Stopped`          | `0x200`        | [Vehicle is stopped / not moving](https://cslmodding.info/asset/vehicle/#sub-mesh-flag-stopped).|
| `Leaving`          | `0x400`        | Active for trains that are about to leave station, but haven't started moving yet. |
| `Arriving`         | `0x800`        | Active for trains arriving at a station but not yet stopped. Active for taxis which have a passenger on board. |
| `Reversed`         | `0x1000`       | Active for train/monorail engine which is travelling backwards. |
| `TakingOff`        | `0x1000`       | <ul><li>`TrolleybusAI`: Right Pole</li><li>`AircraftAI`, `HelicopterAI`: Taking off</li></ul> |
| `Flying`           | `0x4000`       | `AircraftAI`, `BalloonAI`, `BlimpAI`, `HelicopterAI`: Flying. |
| `Landing`          | `0x8000`       | <ul><li>`TrolleybusAI`: Left pole</li><li>`AircraftAI`, `HelicopterAI`: Landing</li></ul> |
| `WaitingSpace`     | `0x10000`      | |
| `WaitingCargo`     | `0x20000`      | `CargoShipAI`, `CargoTrainAI`, `CargoTruckAI`, `TaxiAI`: Waiting for cargo. |
| `GoingBack`        | `0x40000`      | Vehicle returning to place of origin. |
| `WaitingTarget`    | `0x80000`      | |
| `Importing`        | `0x100000`     | Set for vehicles which are importing goods, even when they are returning to facility. |
| `Exporting`        | `0x200000`     | Set for vehicles which are exporting goods, even when they are returning to facility. |
| `Parking`          | `0x400000`     | Road vehicle is moving to a parking spot. |
| `CustomName`       | `0x800000`     | Active if the vehicle has been given a custom name (eg. by [Customize It: Extended](https://steamcommunity.com/sharedfiles/filedetails/?id=1806759255) mod, or by editing name in vehicle info panel title bar). |
| `OnGravel`         | `0x1000000`    | Enables road vehicle dust effect. Set by segment `NetInfo.m_setvehicleflags` (see later). |
| `WaitingLoading`   | `0x2000000`    | Set for cargo trains at station while being loaded with cargo. |
| `Congestion`       | `0x4000000`    | [Force despawn to reduce traffic jams](https://github.com/CitiesSkylinesMods/TMPE/issues/1229#issuecomment-996881397). |
| `DummyTraffic`     | `0x8000000`    | The vehicle is dummy traffic. |
| `Underground`      | `0x10000000`   | Vehicle is travelling underground. Set by segment `NetInfo.m_setvehicleflags` (see later). |
| `Transition`       | `0x20000000`   | Slope segments set this flag. Set by segment `NetInfo.m_setvehicleflags` (see later). |
| `InsideBuilding`   | `0x40000000`   | |
| `LeftHandDrive`    | `int.MinValue` | |

### `Vehicle.Flags2`

| Flag               | Value          | Purpose |
| :---               | :---           | :---    |
| `Floating`         | `0x1`          | Vehicle is swept away by water (eg. tsunami). Will eventually despawn unless it lands on dry land. |
| `Blown`            | `0x2`          | Vehicle is sucked in to a tornado/chirpnado. Will eventually despawn unless dropped from tornado. |
| `Yielding`         | `0x4`          | |
| `EndStop`          | `0x8`          | |


## `NetInfo.m_setvehicleflags`

When vehicles are travelling along a network prefab, they adopt any flags set in `NetInfo.m_setvehicleflags`.

It's mainly used to set the following `Vehicle.Flags`:

* `OnGravel` - gravel roads cause vehicles to show dust effect
* `Underground` - ?
* `Transition` - ?

## See also

* [CSL Modding: Sub-mesh flags](https://cslmodding.info/asset/vehicle/#sub-mesh-flags)