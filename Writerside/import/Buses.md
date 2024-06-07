> Verified: January 2022 - TM:PE 11.5.2 / TM:PE 11.6

This guide covers the various bus services in your city, and looks at how to optimise them using a mixture of TM:PE, vanilla game and DLC features.

## Overview

Buses are an important component of any public transport system becuase they are extremely flexible, both in terms of capacity and routing.

> Trivia: [Is it 'Buses' or 'Busses'?](https://www.merriam-webster.com/words-at-play/plural-of-bus)

In Cities: Skylines, there are five main types of bus:

* **Passenger buses** - used by cims and tourists to travel around the city
    * **Biofuel bus** (Green Cities DLC) - just a normal bus that's quieter
    * **School bus** (Campus DLC) - literally just a normal bus, painted yellow
* **Trolleybus** (Sunset Harbor DLC) - similar to a bus, but needs roads with overhead wires
* **Sightseeing bus** (Park Life DLC) - used by tourists to travel to city attractions
* **Evacuation bus** (Natural Diasters DLC) - used by cims and tourists to travel to emergency shelters
* **Intercity bus** (Sunset Harbor DLC) - a special bus that links to outside connections
    * Only stops at intercity bus stations/terminals
    * Doesn't have a depot
    * Buses choose their own route to/from outside connection

All buses (except intercity) share some common features:

* They spawn from a depot and then travel to their bus route
* They visit each stop on the route in turn, and keep doing that until the end of their shift
* Then they return to their depot and despawn

## Depots

Depots are special buildings which spawn buses. There are four main types of depot:

* **Bus depots** & **Biofuel bus depots** spawn passenger buses
    * Normal and biofuel buses can spawn from each depot (unless you use mods like IPT2 or TLM)
* **Trolleybus depots** spawn passenger trolleybuses
    * The entire route must have overhead wires connecting to the depot building
    * The depot is treated as the first stop on the route
* **Sightseeing bus depots** spawn sightseeing busses
* **Emergency shelters** spawn evacuation busses
    * The shelter is treated as the first stop on the route

Buses will always spawn from the depot nearest the first stop defined on the route. However, once spawned the bus will choose and travel to a random stop on the line (this helps spread out buses at the start of a shift).

## Routes

> In this guide, _routes_ means _transport lines_ (not the 'journeys' shown in Traffic Routes info view).

Buses loop around a predefined route consisting of two or more stops, visiting each stop in turn.

The last stop must always connect back to the first stop, ensuring the route forms a loop. Between each stop the pathfinder finds the best route to the next stop.

> Tip: When editing routes, you can drag stops to move them or right-click to delete them.

Routes have several settings which you can customise:

* **Line color** - Most vehicles will change color to match the line color
* **Type of bus** - Specifies which specific type of bus to use for a given route
* **Number of busses** - Determined by number of stops, line budget and day/night budgets
* **Day vs. Night** - A route can operate during day, night or both

To customise a route:

* Open **Info Views > Transport Routes** and click the magnifying glass on the relevant row
* Alternatively, click any bus on the road and choose **Line Details** from it's info panel

Note that on the line details screen, you can click individual stops to see more information about them, and even rename them.

> **Mods:** [IPT](https://steamcommunity.com/sharedfiles/filedetails/?id=928128676) or [TLM](https://steamcommunity.com/sharedfiles/filedetails/?id=1312767991) (only one, not both) provide more advanced route customisation options.

## Desirable routes

Differnet types of bus have different definitions of "desirable route", which in turn determines their popularity:

#### Passenger bus/trolleybus (residents and tourists):

* Travel between home, work, shops and leisure
* Connect to other transport routes (bus, train, ferry, etc)
    * Don't forget to link to stations where tourists enter/leave the city
* Ideally have two routes along the same path, but going in different directions
    * Example: Cim travels from home to work, and then from work to home
* The [Public Transport Info View](Public Transport Info View) shows buildings that are difficult to reach via public transport
* The [Traffic Routes Info View](Traffic Routes Info View) helps find where cims are travelling to

#### Intercity buses (outside connection):

* Trvel between your city and the outside world
* Stations/terminals should ideally be placed near:
    * Major transport hubs in your city
    * Tourist areas
    * Town/City centres

#### Sightseeing buses (tourists):

* Travel between beauty spots in your city
* The Tourism Info View shows beauty spots

#### Evacuation busses:

* Collect cims from high population areas
* Cims near the shelter can walk to shelter; no need for stops near the shelter

> Tip: Use pedestrian/boke paths to create shortcuts for pedestrians and cyclists to reach stops more quickly.

## Bus jams

> This issue does not apply to evacuation busses, because their depot (the emergency shelter) only serves a single route.

Passenger and sightseeing bus depots can service multiple bus routes, and each route can have multiple busses on it, so there is a risk of "bus jams" at the start/end of shifts; the depot can become jammed with busses.

There are several ways to overcome such issues:

* Use bus lanes to prevent other road vehicles from delaying busses
* Don't place the first stop of two or more lines in the same spot
* Spread several depots around your city so they service different lines

## Bus lanes

Bus lanes allow busses (and often taxis, emergency and service vehicles) to avoid getting stuck in traffic jams caused by other road vehicles. The vanilla game has several bus roads, and there are huge numbers of additional roads in the Steam Workshop.

You will sometimes find cars and trucks using bus lanes, particularly near junctions where they use them as a turning lane; this can disrupt your bus services. To fix that, you can **Ban private cars and trucks on bus lanes** in [Policies](Policies) settings.

Bus lanes are preferred when routing between spots on a bus route. However, if a normal lane provides a much faster/shorter alternative, the bus will use that lane instead. Use [Vehicle Restrictions](Vehicle Restrictions) to discourage buses from using undesirable routes.

> Tip: [Vehicle Restrictions](Vehicle Restrictions) can be used to create fake bus lanes (by banning cars/trucks from a normal lane), however those lanes won't be seen as 'preferred' lanes like proper bus lanes; there's no guarantee that buses will use them.

## Lane changes

Busses will often need to change lanes several times to achieve the most direct route to their next stop. If there aren't enough opportunities for them to change lane, they could be forced to take a more complex (and slower) route.

> ![Cumbersome bus route](https://i.imgur.com/3Boqd3y.png)  
> The bus travelling from A to B couldn't change lane, so it had to take a detour!

If [Lane Arrows](Lane Arrows) are causing problems, enable **Busses may ignore lane arrows** in [Policies](Policies) settings to make bus routing more flexible.

For evacuation buses, enabling **Evacuation busses may ignore traffic rules** in [Policies](Policies) settings makes them behave like [Reckless Drivers](Reckless Drivers) that ignore lane arrows, priority signs, speed limits and even traffic lights - they'll do whatever it takes to save lives!

You can also provide more places where vehicles can change lanes by adding additional nodes to your road network:

* Add a junction by connecting a road to an existing road; this creates a junction node. Then delete the newly added road; the junction node turns in to a middle node, where vehicles can change lane.
* Alternatively, and more easily, install [Network Multitool](https://steamcommunity.com/sharedfiles/filedetails/?id=2560782729) mod which includes a tool for adding nodes.
* For more information on nodes, see: [[Nodes, Segments, Lanes]]

## Turning points

Sometimes busses need to turn around and travel back in the opposite direction. There's three ways they can do that:

* At a junction that allows [U-turns](U-turns)
* Driving round the block or a roundabout (going through several junctions)
* At the end of a cul-de-sac (dead-end road)

If a bus has to travel a long way to reach a turning point, it becomes less desirable due to increased travel time. Adding a suitable turning point will make the route shorter, which in turn will make the route more desirable.

## Waiting times

If cims have to wait a long time for the bus, or the bus route is slow at getting them to where they want to go, the popularity of the route will decrease; cims will then find alternatives - cars!

To fix that:

* Reduce travel times with **bus lanes**, **lane changing points** and **turning points**
* Use the **Line Details** screen to find under-used stops, then remove them
* Add more busses to the route (increase budgets) to reduce waiting times
    * This can backfire in heavy traffic as the extra buses will exacerbate traffic jams
* Maybe the bus is too crowded - use a bus with higher passenger capacity

## Bus stations, terminals and hubs

If you want to connect two or more routes, simply have stops on each route near or at the same location. Note, however, that the patfinder adds a small penalty when a cim or tourist has to change between routes.

Alternatively, use a bus station building - cims can transfer between bus routes with practically no penalty.

If you want to transfer between different transport types (eg. bus and ferry), use a transport hub. These are essentially harbors or stations that have an integral bus station.

## Other guides

We found these guides useful too:

* [Tips and How-To's: Buses](https://steamcommunity.com/sharedfiles/filedetails/?id=1186534752) (Steam Guide)
* [How to make realistic/good looking bus network](https://steamcommunity.com/sharedfiles/filedetails/?id=1262357386) (Steam Guide)

## Useful mods

* [Anxiety Reducer](https://steamcommunity.com/sharedfiles/filedetails/?id=1766839841) - reduce route popularity penalty caused by transport delays
* [Customize It Extended](https://steamcommunity.com/sharedfiles/filedetails/?id=1806759255) - customise stats of buses and depots
* [Express Bus Services](https://steamcommunity.com/sharedfiles/filedetails/?id=2262054175) - buses skip empty stops
* [Intercity Bus Control](https://steamcommunity.com/sharedfiles/filedetails/?id=2499771767) - allows you to control which bus terminals and stations will be visited by intercity buses.
* [Intercity Bus Stop](https://steamcommunity.com/sharedfiles/filedetails/?id=2049510825) (asset) - a small intercity bus stop for detailers
* [Real Time](https://steamcommunity.com/sharedfiles/filedetails/?id=1420955187) - cims abandon journeys that are taking too long
* [Stops & Stations](https://steamcommunity.com/sharedfiles/filedetails/?id=1776052533) - cims avoid overcrowded stops
* [Ticket Price Customizer](https://steamcommunity.com/sharedfiles/filedetails/?id=1393820309) - change prices of passenger transport services
* [Transit Vehicle Spawn Delay](https://steamcommunity.com/sharedfiles/filedetails/?id=2654110611) - adds a delay between each vehicle spawned from a depot
* [Trolleybus Trailer AI](https://steamcommunity.com/sharedfiles/filedetails/?id=2275749683) - allows articulated trolleybus trailers to have poles
* [IPT](https://steamcommunity.com/sharedfiles/filedetails/?id=928128676) (basic) _or_ [TLM](https://steamcommunity.com/sharedfiles/filedetails/?id=1312767991) (advanced) - extends functionality of public transport lines

## FAQ

**Does this affect frame rate or cause lag?**
> No. If you optimise your bus routes (use bus lanes, ensure enough lane changes can be made, etc.) you can acutally _reduce_ CPU load by making pathfinding easier between stops.

**Can busses ignore [Lane Connectors](Lane Connectors)?**
> No. If you use lane connectors, busses must always adhere to those regardless of policy settings.

## Troubleshooting

Having problems? See these troubleshooting guides:

* [Busses are using weird routes](Busses are using weird routes)
* [Busses not spawning from depots](Busses not spawning from depots)
* [Cims not using public transport](Cims not using public transport)
* [Intercity buses not working](Intercity buses not working)
* [Transport vehicles stuck on boarding](Transport vehicles stuck on boarding)

> Tip: You can find and remove broken routes and stops with the [Broken Nodes Detector](https://steamcommunity.com/sharedfiles/filedetails/?id=1777173984) mod.

## See Also

[Settings](Settings):

* [Policies](Policies) - set policies for busses and junctions

[Toolbar](Toolbar):

* [Vehicle Restrictions](Vehicle Restrictions)
* [Lane Arrows](Lane Arrows)
* [Lane Connectors](Lane Connectors)
* [Junction Restrictions](Junction Restrictions)

Advanced:

* [Vehicle Restriction Aggression](Vehicle Restriction Aggression)
* [[Nodes, Segments, Lanes]]