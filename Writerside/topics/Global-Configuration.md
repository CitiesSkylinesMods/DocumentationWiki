# Global Config File

> Verified: February 2020 - TM:PE 11.0

## Overview

The **`TMPE_GlobalConfig.xml`** contains numerous parameters, many of which are not shown in the
mod [](Settings.md) UI. You can change these parameters to fine-tune TM:PE to your requirements.

You can find the file in the following path (maybe different depending on where you installed the game):

> `C:\Program Files (x86)\Steam\steamapps\common\Cities_Skylines`

The log file is split into several sections as listed below:

* [General Settings](#general-settings)
* [`Debug`](#debug) (only in developer `DEBUG` builds)
* [`AdvancedVehicleAI`](#advancedvehicleai)
* [`DynamicLaneSelection`](#dynamiclaneselection)
* [`Main`](#main)
* [`Gameplay`](#gameplay)
* [`ParkingAI`](#parkingai)
* [`PathFinding`](#pathfinding)
* [`PriorityRules`](#priorityrules)
* [`TimedTrafficLights`](#timedtrafficlights)

Each section contains parameters relating to a
specific [`ConfigData` class](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/tree/master/TLM/TLM/State/ConfigData)
within TM:PE.

## Changing values

> Default values shown are correct as of TM:PE v11.0-alpha6 (August 2019)

If editing the file, make sure you use a plain text editor, not a word processor. For more information,
see: [](Text-Editors.md)

Note that TM:PE only performs basic type checking on values. If you specify invalid value types, or values outside the
specified range, you will get errors.

### General Settings

There are a few top-level keys containing general settings...

| Parameter      |                                                                                   Range <br /> <sup>Type</sup> <br /> `Default`                                                                                    | Notes                                                                                                                                                                                                                        |
|:---------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `Version`      |                                                                                 1 → +∞  <br /> <sup>integer</sup> <br /> _current_                                                                                 | The config file format version number; increments whenever we make alterations to the format.                                                                                                                                |
| `LanguageCode` | [`AvailableLanguageCodes`](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/blob/master/TLM/TLM/UI/Localization/Translation.cs#L91) <br /> <sup>string</sup> <br /> _game language_ | A two-letter [ISO 639-1 code](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) depicting the selected locale. If the key is not present, or the value empty, TM:PE will use whatever the base game language is set to. |

Note: We also provide some support for non-standard language codes used by popular game translation mods; we transpose
them in to ISO 639-1 equivalents. For more details
see [PR #534](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/pull/534).

### `Debug`

> TODO: Update links

This section is only applicable to `DEBUG` builds of TM:PE and controls the output of debug logging to the [[TMPE.log]]
file.

For more information, see:

* Build instructions
* Logging documentation

### `AdvancedVehicleAI`

This section describes configuration parameters that are used by the [Advanced Vehicle AI](L-Advanced-AI.md).

| Parameter                           | Range <br /> <sup>Type</sup> <br /> `Default`  | Notes                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------|:----------------------------------------------:|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `LaneRandomizationJunctionSel`      |  1 → +∞  <br /> <sup>integer</sup> <br /> `3`  | At every `n`<sup>th</sup> junction (where `n` is the parameter value), the AI randomly selects a favorite lane for the vehicle that a path-calculation is being performed for.                                                                                                                                                              |
| `LaneRandomizationCostFactor`       |  0 → +∞  <br /> <sup>float  </sup> <br /> `1`  | During lane selection randomization, the AI assigns this cost value to a lane with a probability of 50%. In the remaining 50%, a lane is not assigned any additional costs.                                                                                                                                                                 |
| `LaneChangingBaseMinCost`           | 1 → +∞  <br /> <sup>float  </sup> <br /> `1.1` | Minimum cost factor, applied to path costs for every considered lane change.                                                                                                                                                                                                                                                                |
| `LaneChangingBaseMaxCost`           | 1 → +∞  <br /> <sup>float  </sup> <br /> `1.5` | Maximum cost factor, applied to path costs for every considered lane change.                                                                                                                                                                                                                                                                |
| `LaneChangingJunctionBaseCost`      |  1 → +∞  <br /> <sup>float  </sup> <br /> `2`  | Cost factor, applied to path costs for every considered lane change in front of junctions.                                                                                                                                                                                                                                                  |
| `JunctionBaseCost`                  | 0 → +∞  <br /> <sup>float  </sup> <br /> `0.1` | Cost factor, applied to path costs for every highway interchange considered during path-finding.                                                                                                                                                                                                                                            |
| `MoreThanOneLaneChangingCostFactor` |  1 → +∞  <br /> <sup>float  </sup> <br /> `2`  | Cost factor, applied to path costs for every considered multi-lane change.                                                                                                                                                                                                                                                                  |
| `TrafficCostFactor`                 |  0 → +∞  <br /> <sup>float  </sup> <br /> `4`  | At every junction considered during path-finding, this cost factor is multiplied with the inverted (slightly randomized) mean speed of the current segment.                                                                                                                                                                                 |
| `LaneDensityRandInterval`           | 0 → 100 <br /> <sup>integer</sup> <br /> `20`  | Segment mean speeds that are queried during path-finding are randomized before multiplying with the set `TrafficCostFactor`. This value defines the zero-centered randomization interval (e.g. if the value is set to `20`, it is equally likely that _10%_ are _added to_ or _subtracted from_ the current segment's relative mean speed). |
| `MaxTrafficBuffer`                  | 1 → +∞  <br /> <sup>integer</sup> <br /> `10`  | Real-time traffic measurements collects [mean](https://en.wikipedia.org/wiki/Mean) speeds of up to `n` vehicles (where `n` is the parameter value). If the threshold is reached, collected mean speeds are forgotten and a fresh measurement cycle begins.                                                                                  |

### `DynamicLaneSelection`

This section describes configuration parameters that are used by [Dynamic Lane Selection](Dynamic-Lane-Selection.md).

> TODO: Fill in missing info and better describe recently added parameters.

| Parameter                            | Range <br /> <sup>Type</sup> <br /> `Default`  | Notes                                                                                                                                                                                                                                             |
|:-------------------------------------|:----------------------------------------------:|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `MaxReservedSpace`                   | 0 → +∞  <br /> <sup>float  </sup> <br /> `0.5` | Maximum amount of space that is allowed to be reserved by other vehicles on the lane right behind the next candidate lane. If the space reservation exceeds this value, DLS ignores the candidate lane if a lane change is necessary to reach it. |
| `MaxRecklessReservedSpace`           | 0 → +∞  <br /> <sup>float  </sup> <br /> `10`  | Like above, but this value is used by reckless drivers only.                                                                                                                                                                                      |
| `LaneSpeedRandInterval`              |  0 → 100 <br /> <sup>integer</sup> <br /> `5`  | Randomization interval for artificially modifying measured lane speeds (the same principle as in `AdvancedVehicleAI` → `LaneDensityRandInterval` is used here.                                                                                    |
| `MaxOptLaneChanges`                  |  1 → +∞  <br /> <sup>integer</sup> <br /> `2`  | Maximum number of future lane changes to consider within the 5-segment window.                                                                                                                                                                    |
| `MaxUnsafeSpeedDiff`                 | 0 → +∞  <br /> <sup>float  </sup> <br /> `0.4` | Maximum allowed difference between current cruise speed and measured speed on next candidate lane if the lane change that is necessary to switch to the candidate lane was classified as unsafe.                                                  |
| `MinSafeSpeedImprovement`            | 0 → +∞  <br /> <sup>integer</sup> <br /> `25`  | Minimum speed improvement (absolute velocity) necessary to consider the candidate lane during the evaluation of egoistic lane transitions.                                                                                                        |
| `MinSafeTrafficImprovement`          | 0 → +∞  <br /> <sup>integer</sup> <br /> `20`  | Minimum traffic flow improvement (in %) necessary to consider the candidate lane during the evaluation of altruistic lane transitions.                                                                                                            |
| `VolumeMeasurementRelSpeedThreshold` | 0 → 150 <br /> <sup>integer</sup> <br /> `50`  | Minimum measured relative vehicle speed necessary when traffic volume starts to affect lane changing decisions.                                                                                                                                   |
| `MinMaxReservedSpace`                |      ? <br /> <sup>float</sup> <br /> `0`      | Minimum maximum allowed reserved space on previous vehicle lane (for regular drivers).                                                                                                                                                            |
| `MaxMaxReservedSpace`                |      ? <br /> <sup>float</sup> <br /> `5`      | Maximum value for Maximum allowed reserved space on previous vehicle lane (for regular drivers).                                                                                                                                                  |
| `MinMaxRecklessReservedSpace`        |     ? <br /> <sup>float</sup> <br /> `10`      | Minimum maximum allowed reserved space on previous vehicle lane (for reckless drivers).                                                                                                                                                           |
| `MaxMaxRecklessReservedSpace`        |     ? <br /> <sup>float</sup> <br /> `50`      | Maximum maximum allowed reserved space on previous vehicle lane (for reckless drivers).                                                                                                                                                           |
| `MinLaneSpeedRandInterval`           |   0 → 100 <br /> <sup>float</sup> <br /> `0`   | Minimum lane speed randomization interval.                                                                                                                                                                                                        |
| `MaxLaneSpeedRandInterval`           |  0 → 100 <br /> <sup>float</sup> <br /> `25`   | Maximum lane speed randomization interval.                                                                                                                                                                                                        |
| `MinMaxOptLaneChanges`               |     ? <br /> <sup>integer</sup> <br /> `1`     | Minimum maximum number of considered lane changes.                                                                                                                                                                                                |
| `MaxMaxOptLaneChanges`               |     ? <br /> <sup>integer</sup> <br /> `3`     | Maximum maximum number of considered lane changes.                                                                                                                                                                                                |
| `MinMaxUnsafeSpeedDiff`              |     ? <br /> <sup>float</sup> <br /> `0.1`     | Minimum maximum allowed speed difference for unsafe lane changes (in game units).                                                                                                                                                                 |
| `MaxMaxUnsafeSpeedDiff`              |      ? <br /> <sup>float</sup> <br /> `1`      | Maximum maximum allowed speed difference for unsafe lane changes (in game units).                                                                                                                                                                 |
| `MinMinSafeSpeedImprovement`         |      ? <br /> <sup>float</sup> <br /> `5`      | Minimum minimum required speed improvement for safe lane changes (in game units).                                                                                                                                                                 |
| `MaxMinSafeSpeedImprovement`         |     ? <br /> <sup>float</sup> <br /> `30`      | Maximum minimum required speed improvement for safe lane changes (in game units).                                                                                                                                                                 |
| `MinMinSafeTrafficImprovement`       |      ? <br /> <sup>float</sup> <br /> `5`      | Minimum minimum required traffic flow improvement for safe lane changes (in %).                                                                                                                                                                   |
| `MaxMinSafeTrafficImprovement`       |     ? <br /> <sup>float</sup> <br /> `30`      | Maximum minimum required traffic flow improvement for safe lane changes (in %).                                                                                                                                                                   |

### `Main`

This section describes configuration parameters that are used by the main module.

| Parameter                               |       Range <br /> <sup>Type</sup> <br /> `Default`        | Notes                                                                                                                                                                                                                        |
|:----------------------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `MainMenuButtonX`                       |  0 → +∞        <br /> <sup>integer</sup>     <br /> `464`  | Main menu button X position.                                                                                                                                                                                                 |
| `MainMenuButtonY`                       |  0 → +∞        <br /> <sup>integer</sup>     <br /> `10`   | Main menu button Y position.                                                                                                                                                                                                 |
| `MainMenuButtonPosLocked`               | true\|false   <br /> <sup>boolean</sup>     <br /> `false` | Specifies if the main menu button position should be fixed.                                                                                                                                                                  |
| `MainMenuX`                             |  0 → +∞        <br /> <sup>integer</sup>     <br /> `85`   | Main menu X position.                                                                                                                                                                                                        |
| `MainMenuY`                             |  0 → +∞        <br /> <sup>integer</sup>     <br /> `60`   | Main menu Y position.                                                                                                                                                                                                        |
| `MainMenuPosLocked`                     | true\|false   <br /> <sup>boolean</sup>     <br /> `false` | Specifies if the main menu position should be fixed.                                                                                                                                                                         |
| `DisplayedTutorialMessages`             |  _list_        <br /> <sup>string list</sup> <br /> `""`   | Tutorial messages that have already been shown to the player.                                                                                                                                                                |
| `EnableTutorial`                        | true\|false   <br /> <sup>boolean</sup>     <br /> `true`  | Specifies if tutorial messages should be shown to the player.                                                                                                                                                                |
| `TinyMainMenu`                          | true\|false   <br /> <sup>boolean</sup>     <br /> `true`  | Specifies if a more compact main menu should be used.                                                                                                                                                                        |
| `GuiTransparency`                       |  0 → 100       <br /> <sup>integer</sup>     <br /> `30`   | Window transparency.                                                                                                                                                                                                         |
| `OverlayTransparency`                   |  0 → 100       <br /> <sup>integer</sup>     <br /> `40`   | Overlay transparency.                                                                                                                                                                                                        |
| `ShowCompatibilityCheckErrorMessage`    | true\|false   <br /> <sup>boolean</sup>     <br /> `false` | If `true`, a warning message will be displayed if an [unexpected mod conflict](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/wiki/Incompatible-mods#unexpected-mod-conflicts) is detected. |
| `ScanForKnownIncompatibleModsAtStartup` | true\|false   <br /> <sup>boolean</sup>     <br /> `true`  | If `true`, a dialog will be displayed listing subscribed [known incompatible mods](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/wiki/Incompatible-mods#known-incompatibilities).          |
| `IgnoreDisabledMods`                    | true\|false   <br /> <sup>boolean</sup>     <br /> `true`  | If `true`, disabled mods will be ignored while checking for known incompatible mods.                                                                                                                                         |
| `DisplaySpeedLimitsMph`                 | true\|false   <br /> <sup>boolean</sup>     <br /> `false` | If `true`, speed limits will be displayed in Miles Per Hour (MPH) rather than km/h.                                                                                                                                          |
| `MphRoadSignStyle`                      |          <sup>enumeration</sup> <br /> `SquareUS`          | Determines which speed limit sign style to use (only applies if `DisplaySpeedLimitsMph` is `true`).                                                                                                                          |

See:
_[MphSignStyle](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/blob/master/TLM/TLM/UI/SubTools/SpeedLimits/MphSignStyle.cs)_

### `Gameplay`

This section describes configuration parameters that are used the Gameplay module.

| Parameter                | Range <br /> <sup>Type</sup>    <br /> `Default` | Notes                                                         |
|:-------------------------|:------------------------------------------------:|:--------------------------------------------------------------|
| `VehicleTimedRandModulo` |   0 → ? <br /> <sup>integer</sup> <br /> `10`    | Modulo value for time-varying vehicle behavior randomization. |

### `ParkingAI`

This section describes configuration parameters that are used by the [](Parking-AI.md).

| Parameter                                | Range <br /> <sup>Type</sup> <br /> `Default`  | Notes                                                                                                                                                                                                                                                                                                    |
|:-----------------------------------------|:----------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ParkingSpacePositionRand`               | 1 → +∞  <br /> <sup>integer</sup> <br /> `32`  | Randomization radius for manipulating the point where the search for available parking spaces starts. Randomization is performed to allow road-side parking spaces on the opposite site of the road to be considered during parking space search.                                                        |
| `VicinityParkingSpaceSelectionRand`      |  1 → +∞  <br /> <sup>integer</sup> <br /> `4`  | For every found candidate parking space, a random number between `0` and `VicinityParkingSpaceSelectionRand - 1` is generated. If the drawn number is `0`, the parking space is skipped. This procedure is applied in order to prevent vehicles from only selecting the closest parking space available. |
| `MaxParkingAttempts`                     | 1 → +∞  <br /> <sup>float</sup>   <br /> `10`  | Maximum number of parking attempts to perform. Vehicles despawn if the number of attempts exceeds this value.                                                                                                                                                                                            |
| `MaxParkedCarInstanceSwitchSqrDistance`  |  0 → +∞  <br /> <sup>float</sup>   <br /> `6`  | Squared distance between a parked car and the pedestrian that enters the car, at which the car entering procedure is executed.                                                                                                                                                                           |
| `MaxBuildingToPedestrianLaneDistance`    | 0 → +∞  <br /> <sup>float</sup>   <br /> `96`  | Maximum allowed distance between building parking spaces and the nearest pedestrian lanes. Building parking spaces that are located too far away from pedestrian paths are not considered in order to prevent pedestrians from floating over long distances.                                             |
| `MaxParkedCarDistanceToHome`             | 0 → +∞  <br /> <sup>float</sup>   <br /> `256` | Maximum acceptable distance between parked vehicles and their owner's home. If the parked vehicle is located further away from home than this value, car owners will be forced to use the car when returning home in order to relocate it to a position that lies closer.                                |
| `MaxParkedCarDistanceToBuilding`         | 0 → +∞  <br /> <sup>float</sup>   <br /> `512` | Maximum acceptable distance between parked vehicles and the current target building. If the distance between target building and source location is smaller than this value the owner citizen prefers to walk or to use public transportation to reach the target.                                       |
| `PublicTransportDemandIncrement`         | 1 → +∞  <br /> <sup>integer</sup> <br /> `10`  | If a citizen is unable to reach a specific target building by means of walking, driving or public transport, the _public transport demand_ of both the source and target buildings are increased by this value.                                                                                          |
| `PublicTransportDemandWaitingIncrement`  |  1 → +∞  <br /> <sup>integer</sup> <br /> `3`  | If the maximum acceptable time a citizen waits for a public transport vehicle to arrive at a stop (e.g. a bus stop) is exceeded, the citizen starts searching for alternative routes to the current target building and public transport demand of the target building is increased by this value.       |
| `PublicTransportDemandDecrement`         |  1 → +∞  <br /> <sup>integer</sup> <br /> `1`  | Public transport demand associated with buildings is continuously diminished by this value.                                                                                                                                                                                                              |
| `PublicTransportDemandUsageDecrement`    |  1 → +∞  <br /> <sup>integer</sup> <br /> `7`  | If a citizen succeeds in finding a path to a target building that includes using public transportation, the _public transport demand_ of both the source and target buildings are diminished by this value.                                                                                              |
| `ParkingSpaceDemandDecrement`            |  1 → +∞  <br /> <sup>integer</sup> <br /> `1`  | Parking space demand associated with buildings is continuously diminished by this value.                                                                                                                                                                                                                 |
| `MinSpawnedCarParkingSpaceDemandDelta`   | -∞ → +∞ <br /> <sup>integer</sup> <br /> `-5`  | When a parked car is spawned near the source building, parking space demand is either decreased or increased, depending on the distance between the parked car and the source building. This value reflects the maximum penalty or minimum reward used for modifying the demand value.                   |
| `MaxSpawnedCarParkingSpaceDemandDelta`   |  -∞ → +∞ <br /> <sup>integer</sup> <br /> `3`  | As above. This value reflects the minimum penalty or maximum reward used for modifying the demand value.                                                                                                                                                                                                 |
| `MinFoundParkPosParkingSpaceDemandDelta` | -∞ → +∞ <br /> <sup>integer</sup> <br /> `-5`  | When a parking space is found near the target building, the _parking space demand_ is either decreased or increased, depending on the distance between the parked car and the target building. This value reflects the maximum penalty or minimum reward used for modifying the demand value.            |
| `MaxFoundParkPosParkingSpaceDemandDelta` |  -∞ → +∞ <br /> <sup>integer</sup> <br /> `3`  | As above. This value reflects the minimum penalty or maximum reward used for modifying the demand value.                                                                                                                                                                                                 |
| `FailedParkingSpaceDemandIncrement`      |  1 → +∞  <br /> <sup>integer</sup> <br /> `5`  | If no parking space can be found near the target building, the _parking space demand_ is increased by this value.                                                                                                                                                                                        |
| `FailedSpawnParkingSpaceDemandIncrement` | 1 → +∞  <br /> <sup>integer</sup> <br /> `10`  | If no parking space can be found near the source building, the _parking space demand_ is increased by this value.                                                                                                                                                                                        |

### `PathFinding`

This section describes configuration parameters that are used by the modified path-finding algorithm.

| Parameter                                | Range <br /> <sup>Type</sup> <br /> `Default`  | Notes                                                                                                                                                                                                                                                                           |
|:-----------------------------------------|:----------------------------------------------:|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `PublicTransportLanePenalty`             |  1 → +∞ <br /> <sup>float</sup>   <br /> `10`  | Represents the cost multiplier that is used to keep regular traffic away from transport lanes (see Bus lane reservation).                                                                                                                                                       |
| `PublicTransportLaneReward`              | 0 → 1  <br /> <sup>float</sup>   <br /> `0.1`  | Represents the (inverted) cost multiplier that is used to keep public transport on the respective transport lanes (see Bus lane reservation).                                                                                                                                   |
| `HeavyVehicleMaxInnerLanePenalty`        | 0 → +∞ <br /> <sup>float</sup>   <br /> `0.5`  | Represents the maximum cost multiplier that is used to keep heavy vehicles away from inner lanes on highways (see Heavy trucks prefer outer lanes on highways).                                                                                                                 |
| `HeavyVehicleInnerLanePenaltySegmentSel` |  1 → +∞ <br /> <sup>integer</sup> <br /> `3`   | Randomization value that controls the ratio of segments where the inner lane penalty is applied for heavy vehicles.                                                                                                                                                             |
| `IncompatibleLaneDistance`               |  0 → +∞ <br /> <sup>integer</sup> <br /> `2`   | Represents the cost factor that is applied to lane changes that are normally not allowed due to incompatible lane arrow configurations. It is used to advice busses to use compatible lanes even if they are allowed to ignore lane arrows (see Busses may ignore lane arrows). |
| `UturnLaneDistance`                      |  0 → +∞ <br /> <sup>integer</sup> <br /> `2`   | Represents the cost factor that is applied to u-turns. It is used to minimize the number of performed u-turns (only relevant, if the option Vehicles may do u-turns at junctions is activated)                                                                                  |
| `MaxWalkingDistance`                     | 0 → +∞ <br /> <sup>float</sup>   <br /> `2500` | Represents the maximum walking distance, in meters (base game default: `1000`). For reference, [a zoning square ("cell") is 8 meters](https://cslmodding.info/scale/).                                                                                                          |
| `PublicTransportTransitionMinPenalty`    |  0 → +∞ <br /> <sup>float</sup>   <br /> `0`   | Minimum penalty applied to path costs whenever a cim switches between different public transport lines.                                                                                                                                                                         |
| `PublicTransportTransitionMaxPenalty`    | 0 → +∞ <br /> <sup>float</sup>   <br /> `100`  | Maximum penalty applied to path costs whenever a cim switches between different public transport lines.                                                                                                                                                                         |

### `PriorityRules`

This section describes configuration parameters that are used for [](Priority-Signs.md).

| Parameter                 |   Range <br /> <sup>Type</sup> <br /> `Default`   | Notes                                                                                                                                                                                                   |
|:--------------------------|:-------------------------------------------------:|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `MaxPriorityCheckSqrDist` |   0 → +∞ <br /> <sup>float</sup>   <br /> `225`   | Maximum squared distance between other vehicles and the junction center point. If the vehicle is yet further away from the junction, it is not considered as a possibly conflicting vehicle.            |
| `MaxPriorityApproachTime` |   0 → +∞ <br /> <sup>float</sup>   <br /> `15`    | Maximum junction approach time difference between queried vehicle and other vehicles. If two vehicles will reach a junction at completely different moments priority rule checking is skipped for them. |
| `MaxPriorityWaitTime`     |   0 → +∞ <br /> <sup>integer</sup> <br /> `100`   | Maximum waiting time in front of yield/stop signs. If the waiting time exceeds this value, priority rule checking is temporarily disabled for the vehicle in question.                                  |
| `MaxYieldVelocity`        | > 0.0 → +∞ <br /> <sup>float</sup>   <br /> `2.5` | Maximum vehicle velocity when approaching a Yield sign. See note below table for how to convert to/from km/h.                                                                                           |
| `MaxStopVelocity`         | > 0.0 → +∞ <br /> <sup>float</sup>   <br /> `0.1` | Maximum vehicle velocity when approaching a Stop sign. See note below table for how to convert to/from km/h.                                                                                            |

> The `MaxYieldVelocity` and `MaxStopVelocity` can be converted to km/h by multiplying their value by `8`. For example,
> if the specified velocity was `2.5` then that equates to `2.5 * 8` which is `20` km/h. If you want to convert km/h
> value
> in to velocity value, just divide the km/h by `8`.

> EDIT: On further investigation it looks like the value above might be `5` (ish) instead of `8`; we need to do more
> digging in to the code to find out for sure.

### `TimedTrafficLights`

This section describes configuration parameters that are used by [](Timed-Traffic-Lights.md).

| Parameter          |   Range <br /> <sup>Type</sup> <br /> `Default`    | Notes                                                                                                                                                                                                                                                                                                                                                                                                         |
|:-------------------|:--------------------------------------------------:|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `FlowWaitCalcMode` |        <sup>enumeration</sup> <br /> `Mean`        | Vehicle counting method to use. Mean: The average number of waiting/driving vehicles is being used as for comparison. Total: The sum of all waiting/driving vehicles is being used for comparison.                                                                                                                                                                                                            |
| `FlowToWaitRatio`  | 0 → +∞       <br /> <sup>float</sup>  <br /> `0.8` | Default traffic light sensitivity.                                                                                                                                                                                                                                                                                                                                                                            |                                                                                                                                                                                                                                                                                                                                                                            
| `SmoothingFactor`  | 0 → 1        <br /> <sup>float</sup>  <br /> `0.1` | Smoothing factor for updating the number of waiting/driving vehicles. Used to prevent counting spikes from happening during adaptive traffic light phases. For every vehicle counting, the previous number of waiting/driving vehicles is multiplied with the smoothing factor. The current number of waiting/driving vehicles is then multiplied with `1 - SmoothingFactor` and finally added to the result. | 

See:
_[FlowWaitCalcMode](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/blob/master/TLM/TMPE.API/Traffic/Enums/FlowWaitCalcMode.cs)_

## See also

[](Settings.md):

* [](Maintenance.md) - has options to reload/reset the global configuration

Old wiki:

* [Global Configuration](https://tmpe.viathinksoft.com/wiki/index.php?title=Global_configuration)
