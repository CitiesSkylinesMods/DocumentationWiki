# 👴 Global Configuration

> 👴 This article's content is old, copied from the original Wiki at https://tmpe.viathinksoft.com/wiki/

## Introduction

Besides the set of saved game-specific options that players may change via the user interface,
TM:PE uses an XML-based configuration to retrieve global parameter values. These values are used
to fine-tune the different the mod has to offer.

> ⚠️ When changing the global configuration, be careful to keep parameter values within their
> domain of definition. TM:PE does not perform excessive parameter checking for global configuration parameters.

## Location

The global configuration is stored in the file `TMPE_GlobalConfig.xml`. The configuration file
resides in the `.../steamapps/common/Cities_Skylines` directory.

## Structure

At the DOM root level, most of the XML nodes partition the configuration into different sections.
Each section contains configuration parameters for a specific feature. Currently, the following
section nodes are present:

| Section              | Description                                                                                                                                 |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| Debug                | (only present if the mod was built in Debug mode) Contains generic parameters that are used to analyze certain features during development) |
| AdvancedVehicleAI    | Advanced Vehicle AI parameters                                                                                                              |
| DynamicLaneSelection | Dynamic Lane Selection parameters                                                                                                           |
| Main                 | General parameters                                                                                                                          |
| ParkingAI            | Parking AI parameters                                                                                                                       |
| PathFinding          | Path-finding parameters                                                                                                                     |
| PriorityRules        | Priority rule parameters                                                                                                                    |
| TimedTrafficLights   | Timed traffic lights parmeters                                                                                                              |

## Sections

The following subsections describe the different configuration parameters.

### Advanced Vehicle AI

This section describes configuration parameters that are used by the [](../Advanced-Vehicle-AI.md).

| Parameter                         | Domain of definition   | Description                                                                                                                                                                                                                                                                                                                         |
|-----------------------------------|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LaneRandomizationJunctionSel      | 1..+∞ (integer)        | At every nth junction (where n is the parmeter value), the AI randomly selects a favorite lane for the vehicle that a path-calculation is being performed for.                                                                                                                                                                      |
| LaneRandomizationCostFactor       | 0..+∞ (floating-point) | During lane selection randomization, the AI assigns this cost value to a lane with a probability of 50 %. In the remaining 50 %, a lane is not assigned any additional costs.                                                                                                                                                       |
| LaneChangingBaseMinCost           | 1..+∞ (floating-point) | Minimum cost factor, applied to path costs for every considered lane change.                                                                                                                                                                                                                                                        |
| LaneChangingBaseMaxCost           | 1..+∞ (floating-point) | Maximum cost factor, applied to path costs for every considered lane change.                                                                                                                                                                                                                                                        |
| LaneChangingJunctionBaseCost      | 1..+∞ (floating-point) | Cost factor, applied to path costs for every considered lane change in front of junctions.                                                                                                                                                                                                                                          |
| JunctionBaseCost                  | 0..+∞ (floating-point) | Cost factor, applied to path costs for every highway interchange considered during path-finding.                                                                                                                                                                                                                                    |
| MoreThanOneLaneChangingCostFactor | 1..+∞ (floating-point) | Cost factor, applied to path costs for every considered multi-lane change.                                                                                                                                                                                                                                                          |
| TrafficCostFactor                 | 0..+∞ (floating-point) | At every junction considered during path-finding, this cost factor is multiplied with the inverted (slightly randomized) mean speed of the current segment.                                                                                                                                                                         |
| LaneDensityRandInterval           | 0..100 (integer)       | Segment mean speeds that are queried during path-finding are randomized before multiplying with the set TrafficCostFactor. This value defines the zero-centered randomization interval (e.g. if the value is set to 20, it is equally likely that 10 % are added to or substracted from the current segment's relative mean speed). |
| MaxTrafficBuffer                  | 1..+∞ (integer)        | Real-time traffic measurements collects means speeds of up to n vehicles (where n is the parameter value). If the threshold is reached, collected mean speeds are forgotten and a fresh measurement cycle begins.                                                                                                                   |

### Dynamic Lane Selection

This section describes configuration parameters that are used by [](L-Dynamic-Lane-Selection.md).

| Parameter                          | Domain of definition   | Description                                                                                                                                                                                                                                       |
|------------------------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MaxReservedSpace                   | 0..+∞ (floating-point) | Maximum amount of space that is allowed to be reserved by other vehicles on the lane right behind the next candidate lane. If the space reservation exceeds this value, DLS ignores the candidate lane if a lane change is necessary to reach it. |
| MaxRecklessReservedSpace           | 0..+∞ (floating-point) | Like above, but this value is used by reckless drivers only.                                                                                                                                                                                      |
| LaneSpeedRandInterval              | 0..100 (integer)       | Randomization interval for artificially modifying measured lane speeds (the same principle as in AdvancedVehicleAI → LaneDensityRandInterval is used here.                                                                                        |
| MaxOptLaneChanges                  | 1..+∞ (integer)        | Maximum number of future lane changes to consider within the 5-segment window.                                                                                                                                                                    |
| MaxUnsafeSpeedDiff                 | 0..+∞ (floating-point) | Maximum allowed difference between current cruise speed and measured speed on next candidate lane if the lane change that is necessary to switch to the candidate lane was classified as unsafe.                                                  |
| MinSafeSpeedImprovement            | 0..+∞ (integer)        | Minimum speed improvement (absolute velocity) necessary to consider the candidate lane during the evaluation of egoistic lane transitions.                                                                                                        |
| MinSafeTrafficImprovement          | 0..+∞ (integer)        | Minimum traffic flow improvement (in %) necessary to consider the candidate lane during the evaluation of altruistic lane transitions.                                                                                                            |
| VolumeMeasurementRelSpeedThreshold | 0..150 (integer)       | Minimum measured relative vehicle speed necessary when traffic volume starts to affect lane changing decisions.                                                                                                                                   |

### Main

This section describes configuration parameters that are used by the main module.

| Parameter                          | Domain of definition | Description                                                                             |
|------------------------------------|----------------------|-----------------------------------------------------------------------------------------|
| MainMenuButtonX                    | 0..+∞ (integer)      | Main menu button X position.                                                            |
| MainMenuButtonY                    | 0..+∞ (integer)      | Main menu button Y position.                                                            |
| MainMenuButtonPosLocked            | false/true (boolean) | Specifies if the main menu button position should be fixed.                             |
| MainMenuX                          | 0..+∞ (integer)      | Main menu X position.                                                                   |
| MainMenuY                          | 0..+∞ (integer)      | Main menu Y position.                                                                   |
| MainMenuPosLocked                  | false/true (boolean) | Specifies if the main menu position should be fixed.                                    |
| DisplayedTutorialMessages          | (list of string)     | Tutorial messages that have already been shown to the player.                           |
| EnableTutorial                     | true/false (boolean) | Specifies if tutorial messages should be shown to the player.                           |
| TinyMainMenu                       | true/false (boolean) | Specifies if a more compact main menu should be used.                                   |
| GuiTransparency                    | 0..100 (int)         | Window transparency                                                                     |
| OverlayTransparency                | 0..100 (int)         | Overlay transparency                                                                    |
| ShowCompatibilityCheckErrorMessage | true/false (boolean) | Specifies if an error message should be displayed when a mod compatibility is detected. |

### ParkingAI

This section describes configuration parameters that are used by the [](L-Parking-AI.md).

| Parameter                              | Domain of definition   | Description                                                                                                                                                                                                                                                                                        |
|----------------------------------------|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ParkingSpacePositionRand               | 1..+∞ (integer)        | Randomization radius for manipulating the point where the search for available parking spaces starts. Randomization is performed to allow road-side parking spaces on the opposite site of the road to be considered during parking space search.                                                  |
| VicinityParkingSpaceSelectionRand      | 1..+∞ (integer)        | For every found candidate parking space, a random number between 0 and ParkingSpacePositionRand - 1 is generated. If the drawn number is zero, the parking space is skipped. This procedure is applied in order to prevent vehicles from only selecting the closest parking space available.       |
| MaxParkingAttempts                     | 1..+∞ (floating-point) | Maximum number of parking attempts to perform. Vehicles despawn if the number of attempts exceeds this value.                                                                                                                                                                                      |
| MaxParkedCarInstanceSwitchSqrDistance  | 0..+∞ (floating-point) | Squared distance between a parked car and the pedestrian that enters the car, at which the car entering procedure is executed.                                                                                                                                                                     |
| MaxBuildingToPedestrianLaneDistance    | 0..+∞ (floating-point) | Maximum allowed distance between building parking spaces and the nearest pedestrian lanes. Building parking spaces that are located too far away from pedestrian paths are not considered in order to prevent pedestrians from floating over long distances.                                       |
| MaxParkedCarDistanceToHome             | 0..+∞ (floating-point) | Maximum acceptable distance between parked vehicles and their owner's home. If the parked vehicle is located further away from home than this value, car owners will be forced to use the car when returning home in order to relocate it to a position that lies closer.                          |
| MaxParkedCarDistanceToBuilding         | 0..+∞ (floating-point) | Maximum acceptable distance between parked vehicles and the current target building. If the distance between target building and source location is smaller than this value the owner citizen prefers to walk or to use public transportation to reach the target.                                 |
| PublicTransportDemandIncrement         | 1..+∞ (integer)        | If a citizen is unable to reach a specific target building by means of walking, driving or public transport, public transport demand of both the source and target buildings are increased by this value.                                                                                          |
| PublicTransportDemandWaitingIncrement  | 1..+∞ (integer)        | If the maximum acceptable time a citizen waits for a public transport vehicle to arrive at a stop (e.g. a bus stop) is exceeded, the citizen starts searching for alternative routes to the current target building and public transport demand of the target building is increased by this value. |
| PublicTransportDemandDecrement         | 1..+∞ (integer)        | Public transport demand associated with buildings is continuously diminished by this value.                                                                                                                                                                                                        |
| PublicTransportDemandUsageDecrement    | 1..+∞ (integer)        | If a citizen succeeds in finding a path to a target building that includes using public tranportation, public transport demand of both the source and target buildings are diminished by this value.                                                                                               |
| ParkingSpaceDemandDecrement            | 1..+∞ (integer)        | Parking space demand associated with buildings is continuously diminished by this value.                                                                                                                                                                                                           |
| MinSpawnedCarParkingSpaceDemandDelta   | -∞..+∞ (integer)       | When a parked car is spawned near the source building, parking space demand is either decreased or increased, depending on the distance between the parked car and the source building. This value reflects the maximum penalty or minimum reward used for modifying the demand value.             |
| MaxSpawnedCarParkingSpaceDemandDelta   | -∞..+∞ (integer)       | As above. This value reflects the minimum penalty or maximum reward used for modifying the demand value.                                                                                                                                                                                           |
| MinFoundParkPosParkingSpaceDemandDelta | -∞..+∞ (integer)       | When a parking space is found near the target building, parking space demand is either decreased or increased, depending on the distance between the parked car and the target building. This value reflects the maximum penalty or minimum reward used for modifying the demand value.            |
| MaxFoundParkPosParkingSpaceDemandDelta | -∞..+∞ (integer)       | As above. This value reflects the minimum penalty or maximum reward used for modifying the demand value.                                                                                                                                                                                           |
| FailedParkingSpaceDemandIncrement      | 1..+∞ (integer)        | If no parking space can be found near the target building, parking space demand is increased by this value.                                                                                                                                                                                        |
| FailedSpawnParkingSpaceDemandIncrement | 1..+∞ (integer)        | If no parking space can be found near the source building, parking space demand is increased by this value.                                                                                                                                                                                        |

### Path Finding

This section describes configuration parameters that are used by the
[](L-Modified-Path-Finding.md).

| Parameter                              | Domain of definition   | Description                                                                                                                                                                                                                                                                     |
|----------------------------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PublicTransportLanePenalty             | 1..+∞ (floating-point) | Represents the cost multiplier that is used to keep regular traffic away from transport lanes (see Bus lane reservation).                                                                                                                                                       |
| PublicTransportLaneReward              | 0..1 (floating-point)  | Represents the (inverted) cost multiplier that is used to keep public tranport on the respective transport lanes (see Bus lane reservation).                                                                                                                                    |
| HeavyVehicleMaxInnerLanePenalty        | 0..+∞ (floating-point) | Represents the maximum cost multiplier that is used to keep heavy vehicles away from inner lanes on highways (see Heavy trucks prefer outer lanes on highways).                                                                                                                 |
| HeavyVehicleInnerLanePenaltySegmentSel | 1..+∞ (integer)        | Randomization value that controls the ratio of segments where the inner lane penalty is applied for heavy vehicles.                                                                                                                                                             |
| IncompatibleLaneDistance               | 0..+∞ (integer)        | Represents the cost factor that is applied to lane changes that are normally not allowed due to incompatible lane arrow configurations. It is used to advice busses to use compatible lanes even if they are allowed to ignore lane arrows (see Busses may ignore lane arrows). |
| UturnLaneDistance                      | 0..+∞ (integer)        | Represents the cost factor that is applied to u-turns. It is used to minimize the number of performed u-turns (only relevant, if the option Vehicles may do u-turns at junctions is activated)                                                                                  |
| MaxWalkingDistance                     | 0..+∞ (floating-point) | Represents the maximum walking distance (base game default: 1000)                                                                                                                                                                                                               |
| PublicTransportTransitionMinPenalty    | 0..+∞ (floating-point) | Minimum penalty applied to path costs whenever a cim switches between different public transport lines.                                                                                                                                                                         |
| PublicTransportTransitionMaxPenalty    | 0..+∞ (floating-point) | Maximum penalty applied to path costs whenever a cim switches between different public transport lines.                                                                                                                                                                         |

### Priority Rules

This section describes configuration parameters that are used by the :doc:`priority rules <prioritySigns>` engine.

| Parameter               | Domain of definition   | Description                                                                                                                                                                                             |
|-------------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MaxPriorityCheckSqrDist | 0..+∞ (floating-point) | Maximum squared distance between other vehicles and the junction center point. If the vehicle is yet further away from the junction, it is not considered as a possibly conflicting vehicle.            |
| MaxPriorityApproachTime | 0..+∞ (floating-point) | Maximum junction approach time difference between queried vehicle and other vehicles. If two vehicles will reach a junction at completely different moments priority rule checking is skipped for them. |
| MaxPriorityWaitTime     | 0..+∞ (integer)        | Maximum waiting time in front of yield/stop signs. If the waiting time exceeds this value, priority rule checking is temporarily disabled for the vehicle in question.                                  |

### Timed Traffic Lights

This section describes configuration parameters that are used by :doc:`trafficLightsTimed`.

| Parameter        | Domain of definition          | Description                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FlowWaitCalcMode | Mean/Total (enumeration)      | Vehicle couting method to use. Mean: The average number of waiting/driving vehicles is being used as for comparison. Total: The sum of all waiting/driving vehicles is being used for comparison.                                                                                                                                                                                                           |
| FlowToWaitRatio  | 0..+∞ (floating-point number) | Default traffic light sensitivity.                                                                                                                                                                                                                                                                                                                                                                          |
| SmoothingFactor  | 0..1 (floating-point number)  | Smoothing factor for updating the number of waiting/driving vehicles. Used to prevent counting spikes from happening during adaptive traffic light phases. For every vehicle counting, the previous number of waiting/driving vehicles is multiplied with the smoothing factor. The current number of waiting/driving vehicles is then multiplied with 1 - SmoothingFactor and finally added to the result. |

## Applying changes

If you choose to modify the file you have to reload it through the options dialog in order
for the new settings to become effective.

* Click on the gear icon in the upper right corner of your screen or press Escape.
* In the pause menu click on Options.
* In the left navigation pane, select Traffic Manager: President Edition.
* Switch to the Maintenance tab.
* Click on Reload global configuration.

## Factory reset

At anytime you can reset all configuration parameters to their default values.
Click on 'Reset global configuration' button found in the Maintenance tab.
