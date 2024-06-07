# High Priority Roads

> Under construction
>
> Note: A similar feature exists for roundabouts, see: [](Roundabout-Policies.md)

## Overview

[](Priority-Routes.md) utilise [](Priority-Signs.md) to minimise disruption caused by joining traffic. But there is an
even worse form of disruption: Traffic and pedestrians crossing multiple lanes, including oncoming traffic, to reach the
other side of the road.

High Priority Roads tackle those problem head-on:

* They ban 'far-side turns' so vehicles can't cut across oncoming traffic
    * Use [](Collector-Roads.md) or [](Traffic-Lights.md) to allow traffic to reach the other side
* They ban pedestrian crossings on the road
    * Use pedestrian bridges/tunnels to allow cims to reach the other side

The result is essentially a minor arterial road capable of carrying moderate-to-large volumes of traffic at fairly high
speed:

![Customized Road Example](picHighPriorityRoads_example.png)

> The road pictured above was visually customised with
> the [Continues Junction Median](https://steamcommunity.com/sharedfiles/filedetails/?id=2104976832)
> and [Hide TMPE Crosswalks](https://steamcommunity.com/sharedfiles/filedetails/?id=1934023593) mods.

## Usage

The default **High Priority Roads** traffic policies are listed below; you can change them in [](Policies.md)
in [](Settings.md):

* [](Priority-Signs.md):
    * Joining traffic must **Yield** (you can change to **Stop**)
    * Priority road traffic always has **Priority**
* [](Junction-Restrictions.md):
    * **Pedestrian crossings** - disallowed (build some pedestrian bridges!)
    * **Enter blocked junction** - disallowed for side-roads (always allowed for vehicles on the priority road)
* [](Lane-Arrows.md):
    * Prevent vehicles crossing oncoming traffic
    * You will need [](Collector-Roads.md) to allow vehicles to reach other side of priority road

> The related features must be enabled in [](Maintenance.md) in [](Settings.md) for them to be applied.

### Applicators

Choose the applicator that best suits your needs...

### Adjust Roads panel

The [](Adjust-Roads.md) panel (see link for details) allows you to define your own route.

1. Select/customise a route
2. Click the **High Priority Road** button to apply your policies to the route  
   ![High Priority Button](btnStreetDoubleLine.png)
    * Click the button a second time to remove the customisations

### Priority Signs tool

The [](Priority-Signs.md) tool chooses the route for you (see **Route Detection** section below):

* `Ctrl/Cmd`+`Click a junction` - applies your policies to the selected junction only
    * Use the shortcut a second time to remove the customisations
* `Ctrl/Cmd`+`Shift`+`Click a junction` - applies you policies along the entire route
    * Use the shortcut a second time to remove the customisations
    * If the junction is on a roundabout, it will apply [](Roundabout-Policies.md) instead.

### Route Detection

When using the Priority Signs shortcuts, the route will be determined based on the roads connected to the junction:

* A small road joins a bigger road (regardless of junction angle)
* A two-way road splits into two one-way roads (Y-junction or "fork")
* A road forms a T-junction with a one way road (like a roundabout junction)

Also, where applicable, Yield signs will automatically be removed to improve traffic flow.

The image bellow shows 3 applications of High priority road. Clicking on each part of the image bellow gives you more
information about that setup.

[![screenshot B2](picHighPriorityRoads_example2.png)](High-Priority-Roads.md#2-split-road-fork-y-junction)
[![screenshot B3](picHighPriorityRoads_example3.png)](High-Priority-Roads.md#1-alley-joins-a-main-road-see-screenshot-above)
[![screenshot B4](picHighPriorityRoads_example4.png)](High-Priority-Roads.md#3-highway-roundabout-overpass)

### 1. alley joins a main road (see screenshot above).

### Warning: You will need a collector road

Be careful not cut your city in half. For example in the screenshot bellow if you set the highlighted road as high
priority road, cars to the south (notice the compass in the image) of the main road cannot go west and cars to the north
of the main road cannot go east. Also, pedestrians cannot cross the highlighted main road.
![screenshot A2w](picHighPriorityRoads_collectorRoad.png)

As is the case in the real world you need to create a collector road (
see https://steamcommunity.com/sharedfiles/filedetails/?id=522776740 Traffic 102 - Road Hierarchy and Zoning):
![Screenshot (1047)](picHighPriorityRoads_collectorRoad2.png)

At the intersection of the collector road and main road, remember to remove high priority rules you set up earlier.

- [](Lane-Arrows.md) tool: use Control+click on the junction.
- [](Junction-Restrictions.md) tool: Select the junction and press delete to clear high priority rules
- Optionally you can set up a traffic light.

Now cars can use the collector road to take the far turn and pedestrians can use it to cross to the other side.

### 2. Split road (Fork- Y junction):

![Screenshot (1032)](picHighPriorityRoads_yFork.png)

### 3. highway/roundabout overpass

![Screenshot (1030)](picHighPriorityRoads_overpass.png)

Note that in addition to all the rules discussed before, the incoming ramp (see red arrow) does NOT yield or keep clear
of the main road. This only happens if [](Lane-Arithmetic.md) is observed. It would be fitting to
use [](Lane-Connectors.md) [](Stay-in-Lane.md) as well to get the lane connections show in the screenshot.

## How rules are applied at road's end

`Shift+click` shortcut - which sets up priority signs - can mess up your roundabout if its resides at road's end.
`Ctrl+Shift+Click` does NOT have this problem. As you can see from the screenshot bellow it understands there is a
roundabout at roads end and does not mess up the roundabout. The two nodes at road ends marked by red circle in the
screenshot bellow are treated differently than the intermediate nodes to avoid said problem.
![Screenshot (992)](picHighPriorityRoads_end.png)

### FAQ:

> Q: Why Roundabout offers dedicated turning lane but high priority road does not?
>
>> A: allocating dedicated turning lane will cause most cars to drive on the innermost lane (TODO explain why?). So not
>> a good idea

> Q: High priority road feature is not working for me
>
>> A: High priority road feature looks at the road's width/lanes in order to decide which road is high priority and
>> which road is alley. if all the roads are the same size, high priority road gets confused as to which road is the main
>> road. Coming soon: When setting up high priority road along a route, The highlighted path is considered high priority.

> Q: How did you create the continuous junction median in the screenshot?
> 
>> A: the road with continues junction median in the first screenshot is
>> from [this asset](https://steamcommunity.com/sharedfiles/filedetails/?id=1319965985&searchtext=continues+junction+median).
>> I am also working on a future mod to do this automatically on vanilla roads.

## See Also

[](Toolbar.md):

* [](Junction-Restrictions.md)
* [](Lane-Arrows.md)
* [](Priority-Signs.md)

[](Settings.md):

* [](Policies.md) - configure high priority road policies

Guides:

* Roads:
    * [](Priority-Routes.md)
    * [](Roundabouts.md)

[Issue Tracker](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues):

* <a href="https://github.com/CitiesSkylinesMods/TMPE/labels/MASS EDIT"><img alt="Issues" src="https://img.shields.io/github/issues/CitiesSkylinesMods/TMPE/MASS EDIT?label=MASS EDIT%26logo=github" /></a>
