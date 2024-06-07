# Policies Settings

> Verified: March 2022 - TM:PE 11.6.5.1

[](Settings.md): [](General.md) | [](Gameplay.md) | **Policies**
| [Overlays](Overlays.md) | [](Maintenance.md) | [Keybindings](Keybinds.md)

## Overview

Use these [](Settings.md) to set the _default_ transport and road customisation policies in your entire city.

Most policies can be overridden for individual lanes, junctions or roads using the features of
the [](Toolbar.md).

## Settings

### At Junctions

_Use these options to set default traffic policies at road junctions..._

#### Busses may ignore lane arrows

> In TM:PE 11.6.5.1 and later, this option is enabled by default for new cities.

* When enabled, [Buses](Buses.md) can ignore [](Lane-Arrows.md), making bus routes more flexible
* Note: Buses must always obey [](Lane-Connectors.md), regardless of this setting

#### Vehicles may enter blocked junctions

* Determines whether vehicles can [](Enter-Blocked-Junctions.md)
* Override any junction with [](Junction-Restrictions.md) tool

#### Vehicles may do U-turns at junctions

* Allow vehicles to do [](U-Turns.md) at junctions
* Override any junction with [](Junction-Restrictions.md) tool

#### Vehicles may turn at red traffic lights

* Allow vehicles to [](Turn-on-Red.md) in to a _near-side_ road:
    * Depending on which side traffic drives on, it can turn in that direction
    * Example: If traffic drives on the right, it's a right turn
* Override any junction with [](Junction-Restrictions.md) tool

#### Also apply to left & right turns between one-way streets

* Allows vehicles to [](Turn-on-Red.md) in to a _far-side_ road:
    * Depending on which side traffic drives on, it can turn in the opposite direction
    * Example: If traffic drives on the right, it's a left turn
    * Only applied if the destination is a **one-way road**
    * They must stop and wait for clear path before making the turn
* Requires the incoming road to have **Turn on Red** enabled

#### Vehicles going straight on may change lanes at junctions

* Allows vehicles going straight ahead at a junction to make [](Lane-Changes.md)
* Override any junction with [](Junction-Restrictions.md) or [](Lane-Connectors.md)
  tools

#### Vehicles follow priority rules at junctions with timed traffic lights

* Makes vehicles yield at unprotected turning lights.
* See: [](Priority-Signs.md) and [](Unprotected-Turns.md)

#### Automatically add traffic lights if applicable

* If enabled, traffic lights will automatically be added to big junctions
* Override any junction with [](Traffic-Lights.md) tools

#### Dedicated turning lanes

> It may take _a few minutes_ before changes to this setting take effect.

* If enabled, roads entering junctions will be given [](Dedicated-Turning-Lanes.md), where
  feasible
* Override any junction with [](Lane-Arrows.md) or [](Lane-Connectors.md) tools

### On Roads

#### Vehicle restrictions aggression

* Set the pathfinding penalty incurred by [](Vehicle-Restrictions.md)
* See: [](Vehicle-Restriction-Aggression.md)

#### Ban private cars and trucks on bus lanes

> Note: Vehicles will still be able to use bus lane when spawning, delivering, or arriving at destination.

* When enabled, only [Buses](Buses.md) can use bus lanes
* If disabled: Override any bus lanes with [](Vehicle-Restrictions.md) tool

#### At a segment to segment transition, only the smaller segment gets crossings

> For definition of **transition nodes**, see [](Nodes,-Segments,-Lanes.md)

* Normally **transition nodes** will get two pedestrian crossings, one for each segment
* When enabled, this option removes the crossing from the larger road
* If both roads are the same size, neither crossing is removed

### On Highways

_Use these options to control vehicles on highways and ramps..._

#### Enable highway-specific lane merging/splitting rules

* Force [](Highway-Junction-Rules.md) on all highway roads
* Override any junction with [](Lane-Connectors.md) tool

#### Heavy vehicles prefer outer lanes on highways

* Encourage large vehicles to use outside lane on highways
* See: [](Heavy-Truck-Highway-Rules.md)

### In Case of Emergency

> This section is only shown if you
> have [Natural Disasters DLC](https://store.steampowered.com/app/515191/Cities_Skylines__Natural_Disasters/).

_Use this option to give evacuation buses more flexibility during disasters..._

#### Evacuation busses may ignore traffic rules

* Allows evacuation buses to ignore the rules and possibly save more people
* For more information, see: [Buses](Buses.md)

### High priority roads

_Use these options to customise the [](High-Priority-Roads.md) bulk applicators..._

> Important: Provide [](Collector-Roads.md) (or tunnels/bridges) to enable cims and vehicles to reach the
> other side of a high priority road.

#### Allow pedestrian crossings on main road

* Determines whether pedestrians can cross over the priority road
* If disabled, cims will need another way to cross (bridge, traffic lights...)
* Override any junction with [](Junction-Restrictions.md) tool

#### Allow cars to take far turn from/into main road (not recommended)

* Determines whether vehicles can cut across oncoming traffic on the priority road
* If disabled, vehicles will need another way to reach the other side (traffic
  lights, [](Collector-Roads.md)...)
* Override any junction with [](Lane-Arrows.md) or [](Lane-Connectors.md) tools

#### Allow cars on yield road to enter blocked main road

> This option is _ignored_ if you enable **Use stop signs when entering main road**.

* If enabled, traffic entering via **Yield** [](Priority-Signs.md)
  can [](Enter-Blocked-Junctions.md)
    * Reduces congestion on side-roads, but disrupts priority road traffic
    * Vehicles already on the priority road can always enter blocked junctions
* Override any junction with [](Junction-Restrictions.md) tool

#### Use stop signs when entering main road

* If enabled, side-roads use **Stop** signs instead of **Yield** signs
    * Reduces disruption of priority road traffic, but increases congestion on side-roads
* Override any junction with [](Priority-Signs.md) tool

### Roundabouts

Use these options to customise the [](Roundabout-Policies.md) bulk applicators...

> Note: If [](High-Priority-Roads.md) bulk applicators encounter a roundabout, they'll use these
> settings at the roundabout junction.

#### Pedestrians shall not cross to the center of roundabout

* Removes pedestrian crossings that connect to center of roundabout
* Override any junction with [](Junction-Restrictions.md) tool

#### Pedestrians shall not cross the roads approaching the roundabout

* Removes pedestrian crossings that cross roads entering/leaving the roundabout
* Override any junction with [](Junction-Restrictions.md) tool

#### Stay in lane inside the roundabout

* Discourage vehicles from changing lanes in the roundabout
* Override any junction/node with [](Lane-Connectors.md) tool

#### Stay in lane on the roads approaching the roundabout

* Prevent lane changes at nodes close to the roundabout
* Forces traffic to get in correct lane sooner
* Override any junction/node with [](Lane-Connectors.md) tool

#### Allocate dedicated exit lanes

* Dedicate outer lane of roundabout to traffic leaving at next exit
    * This improves lane utilisation and flow inside the roundabout
* Override any junction/node with [](Lane-Connectors.md) tool

#### Add priority signs on the roundabout junction

* Vehicles in the roundabout have priority over vehicles entering the roundabout
* Override any junction with [](Priority-Signs.md) tool

#### Yielding vehicles keep clear of blocked roundabout

* Traffic entering via **Yield** [](Priority-Signs.md) will not be able
  to [](Enter-Blocked-Junctions.md)
* Override any junction with [](Junction-Restrictions.md) tool

#### Assign realistic speed limits to roundabouts

* If enabled, the speed limits on roundabouts will be adjusted based on road curvature
    * This is just to make roundabout traffic look more realistic

#### Put parking ban inside roundabouts

* If enabled, any parking lanes on the roundabout itself (1-way roads) will be disabled
* Override any segment with [](Parking-Restrictions.md) tool

#### Put parking bans on roundabout branches

* If enabled, parking lanes on roads at junctions on the roundabout will be disabled
* Override any segment with [](Parking-Restrictions.md) tool

## FAQ

#### Do these settings affect frame rate or cause lag?

> * Not directly; policies just change global defaults for the [](Toolbar.md) tools.
> * See documentation of each tool for specific details.

#### What happens if I change the policies later in the game?

> * Roads, junctions, etc., which were using default values will be updated
> * However, custom settings (via [](Toolbar.md)) will be retained

## See Also

Guides:

* [](City-and-District-Policies.md)

[TM:PE v10.x Wiki](https://tmpe.viathinksoft.com/wiki) (old documentation):

* [Policies & Restrictions options](https://tmpe.viathinksoft.com/wiki/index.php?title=Options#Policies_.26_Restrictions)

[Issue Tracker](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues):

* <a href="https://github.com/CitiesSkylinesMods/TMPE/labels/SETTINGS"><img alt="Issues" src="https://img.shields.io/github/issues/CitiesSkylinesMods/TMPE/SETTINGS?label=SETTINGS%26logo=github" /></a>
