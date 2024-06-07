Just pondering...

## NetLane

The 🍦 vanilla `NetLane.m_flags` member is a `ushort` containing 16 bits. Can we concatenate a 🚦 TM:PE custom `ushort` flags on to it, creating a 32-bit `uint` word?

In theory it should be as simple as (pseudo-code): `lane_flags = lane.m_flags | tmpeLane.flags`.

In the table below, I list the 32 bits (1-indexed) and their purpose. As you can see, this combines the following features:

* Vanilla flags
* Vehicle restrictions
* Parking restrictions
* Lane customisations (see #515)

More could be added if a 64-bit word was used, and I think that would be useful to consider; we could encode lots of useful info in the flags, for example:

* Whether the lane exits by segment start/end node (two flags, so if direction is both, both flags would be set)
* Lane speed limit as an index (or value if sufficient bits available)
* Anything that can reduce calculations required for vehicle AIs and pathfinder

While moving to 64-bit might seem excessive, particularly for lanes, it could significantly reduce the number of data sources required and would make code much more legible. In addition, the save/load process could potentially be greatly simplified in to just 3 main collections (the flags for lanes, segments and nodes).

|bit |from |name                      |meaning                    |
|---:|:---:|:---                      |:---                       |
|    |🍦   |`None`                    |                           |
|`1` |🍦   |`Created`                 |Created; can use.          |
|`2` |🍦   |`Deleted`                 |Deleted; do not use.       |
|`3` |🍦   |`Inverted`                |?                          |
|`4` |🍦   |`JoinedJunction`          |?                          |
|    |🍦   |`JoinedJunctionInverted`  |`Inverted|JoinedJunction`  |
|`5` |🍦   |`Forward`                 |Arrow forward              |
|`6` |🍦   |`Left`                    |Arrow left                 |
|`7` |🍦   |`Right`                   |Arrow right                |
|`8` |🍦   |`Merge`                   |Arrow merge                |
|    |🍦   |`LeftForward`             |`Left|Forward`             |
|    |🍦   |`LeftRight`               |`Left|Right`               |
|    |🍦   |`ForwardRight`            |`Forward|Right`            |
|    |🍦   |`LeftForwardRight`        |`Left|Forward|Right`       |
|`9` |🍦   |`Stop`                    |Bus stop                   |
|`10`|🍦   |`Stop2`                   |Tram stop                  |
|    |🍦   |`Stops`                   |`Stop|Stop2`               |
|`11`|🍦   |`YieldStart`              |                           |
|`12`|🍦   |`YieldEnd`                |                           |
|`13`|🍦   |`StartOneWayLeft`         |                           |
|`14`|🍦   |`StartOneWayRight`        |                           |
|`15`|🍦   |`EndOneWayLeft`           |                           |
|`16`|🍦   |`EndOneWayRight`          |                           |
|    |🍦   |`StartOneWayLeftInverted` |`Inverted|StartOneWayLeft` |
|    |🍦   |`StartOneWayRightInverted`|`Inverted|StartOneWayRight`|
|    |🍦   |`EndOneWayLeftInverted`   |`Inverted|EndOneWayLeft`   |
|    |🍦   |`EndOneWayRightInverted`  |`Inverted|EndOneWayRight`  |
|`17`|🚦   |`AllowCars`               |Allow passenger cars       |
|`18`|🚦   |`AllowTaxis`              |                           |
|`19`|🚦   |`AllowCargo`              |Allow cargo trucks/trains  |
|`20`|🚦   |`AllowPassenger`          |Allow PT vehicles          |
|`21`|🚦   |`AllowServices`           |Allow city service vehicles|
|`22`|🚦   |`AllowEmergency`          |Allow emergency services   |
|`23`|🚦   |`AllowLocal`              |Allow local vehicles       |
|`24`|🚦   |`AllowCity`               |Allow city vehicles        |
|`25`|🚦   |`AllowRegional`           |Allow regional vehicles    |
|`26`|🚦   |`ParkingForward`          |Allow parking forward lane |
|`27`|🚦   |`ParkingBackward`         |Allow parking backward lane|
|`28`|🚦   |`BikeLane`                |                           |
|`29`|🚦   |`BusLane`                 |                           |
|`30`|🚦   |`TaxiRank`                |                           |
|`31`|🚦   |`LoadingBay`              |                           |
|`32`|🚦   |`ParkingLane`             |                           |

## NetSegment

todo

## NetNode

todo