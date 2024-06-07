# Outside Connections not Working
> Verified: January 2022

## Symptoms

* Outside connections not working properly; some examples:
    * Vehicles not entering by highway
    * Vehicles aren't using some, but not all highway connections
    * Vehicles using highways but nobody moves in to city (see also: [](Population-stuck-at-0.md))
    * No cargo vehicles entering the city (see also: [](Vehicles-not-spawning.md))
    * Aircraft not entering city
    * Aircraft enter city, but won't land
    * Ships not using harbours
    * Inter-city trains not spawning
    * Inter-city trains not stopping at stations
    * [](Intercity-buses-not-working.md)

> If you came here looking for ways to make highway traffic behave more naturally / correctly, try: [](Traffic-on-highways-not-behaving-properly.md)

## Causes

There's lots of things that can break outside connections, let's just skip to solutions...

## Solutions

### Incompatible mods

These mods are known to cause issues:

* [Cargo Info](https://steamcommunity.com/sharedfiles/filedetails/?id=1072157697) - prevents vehicles spawning on highways, also causes [](Simulation-error-Array-index-is-out-of-range.md) error. 
* [81 Tiles](https://steamcommunity.com/sharedfiles/filedetails/?id=576327847) (all variants) - doesn't currently support intercity buses outside central 25 tile area
    * Quistar is working on new implementation of 81 Tiles mod that might fix this as part of his Extended Managers Library

### General outside connection issues

> You'll need to disable the edge fog to see the outside connections clearly (use [Hide It!](https://steamcommunity.com/sharedfiles/filedetails/?id=1591417160) or [Clouds and Fog Toggler](https://steamcommunity.com/sharedfiles/filedetails/?id=523824395) mod to achieve that).

* Outside connections must have green arrows at edge of map:
    * If _arrows are missing_, the connection is broken...
    * **Roads:** Only highway roads can be used by default
        * Use [Any Road Outside Connections](https://steamcommunity.com/sharedfiles/filedetails/?id=883332136) to overcome that limitation
        * Zoned roads don't work; use [Zoning Adjuster](https://steamcommunity.com/sharedfiles/filedetails/?id=2389414419) to disable zoning while placing the outside connection.
        * Two-way roads break intercity buses; see: [](Intercity-buses-not-working.md)
    * **Rail:** Some custom rail tracks don't work as outside connections
        * The outside connection must be made from special _station_ track
        * If you connect vanilla train track to outside, game automatically replaces with station track
        * Custom tracks (workshop assets) probably won't work; replace with few segments of vanilla track
        * If station track segment is too small, use Move It mod to stretch it, or bulldoze and rebuild
    * **Ferry:** These can not be used for outside connections (use ship harbours instead)
    * **Blimps, Helicopter, Air tours:** These can not be used for outside connections (use airports instead)
    * **Tram, monorail and metro:** These can not be used for outside connections (use train stations instead)
* Connections showing "no power" or "no water" notifications at edge of map are broken:
    * This can happen on any type of outside connection (for example: [Aircraft](https://steamcommunity.com/app/255710/discussions/0/2605804632895237772/), [Highways](https://steamcommunity.com/app/255710/discussions/0/1648792158808470212/))
    * Often caused by old [Ploppable RICO](https://steamcommunity.com/sharedfiles/filedetails/?id=586012417) mod; replace it with newer [Ploppable RICO Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2016920607) mod.
* Too many connections:
    * Each type of connection (road, rail, aircraft, ships) has a limit on how many connections of that type can exist
    * Use [Unlimited Outside Connections](https://steamcommunity.com/sharedfiles/filedetails/?id=497033453) to overcome that limitation
* Did you create your own connections?
    * If so, it sometimes takes a while for the game to start using them
    * Sometimes you might need to save, quit to desktop, then reload for changes to take effect

### General station / port / hub issues

> In this section we use the term _'station'_ to collectively refer to train stations, ship harbours/docks/ports, airports, and transport hubs

* The station must be connected to your city by road
    * Some stations ([like this](https://steamcommunity.com/sharedfiles/filedetails/?id=1194296555)) require pedestrian path connection instead
    * Some stations are designed to work more effectively when connected to train (e.g. Cargo harbours) or metro (e.g. International airport)
* Broken workshop assets:
    * Stations must contain spawn points to function correctly
    * Use [Spawn Points Fix](https://steamcommunity.com/sharedfiles/filedetails/?id=820157360) or [Building Spawn Points](https://steamcommunity.com/sharedfiles/filedetails/?id=2511258910) to repair
* Passenger stations:
    * Click the station, and on the info panel you'll see an **Inter-city** option
        * To get similar option on bus stations, use [Intercity Bus Control](https://steamcommunity.com/sharedfiles/filedetails/?id=2499771767) mod
    * If you want inter-city vehicles to use that station, you must enable the option

> New users should be aware that there are two types of station, passenger and cargo, which can only receive passengers or cargo respectively.

### Highways

In addition to general issues listed above, check for these issues:

* Broken connection between highways and your city roads:
    * Most highways are two separate 1-way roads; one incoming and one outgoing
    * Make sure _both_ connect to your city road network
    * If in doubt, connect both highway roads with a bit of 2-way normal road and see if that helps
* One way roads preventing vehicles from reaching their destination:
    * Unless you know how to properly use one-way roads, it's best to avoid them.
    * Activate the road building tool, and you'll see white arrows on any one-way roads - replace them with 2-way roads

### Trains

In addition to general issues listed earlier, check for these issues:

* One-way tracks preventing vehicles from reaching their destination:
    * Unless you know how to properly use one-way tracks, it's best to avoid them.
    * Activate the track building tool, and you'll see white arrows on any one-way tracks - replace them with 2-way tracks
* Outside connection platform not connected:
    * Inter-city trains always use the same platform, chosen by the game
    * If that platform isn't connected to outside connection the trains can't use the station
    * Simple solution: Connect all station tracks to the outside connection
    * Once you see which platform they use, you can disconnect the others if desired

> There are some reports that tracks should have outside connection at both ends to work properly. Having done some testing, this doesn't seem to change anything.

### Passenger Ships

In addition to general issues listed earlier, check for these issues:

* Not connected to shipping lane:
    * When placing harbour, you should see a purple line extending out in to the sea
    * If that line isn't there then the harbour isn't connected to a ship lane and no ships can use it
* Broken ship routes:
    * They can be hard to spot (because it's a dashed line, not a solid line)
    * Sharp bends or gaps in the route can cause problems
    * Use [More Network Stuff](https://steamcommunity.com/sharedfiles/filedetails/?id=512314255) to repair routes if required

### Aircraft

In addition to general issues listed earlier, check for these issues:

* Not connected to aircraft route:
    * When placing airports, you will see a warning if the airport isn't in range of an aircraft route
    * If the airport can't connect to the route, planes can't use the airport
* Broken runways or taxiways
    * The airplane AI is easily confused
    * Used curved paths, not sharp corners (jumbo jets don't handle corners very well)
    * Runways and taxiways are usually (always?) one-way - make sure planes can go from runway to terminal and back to runway again
* Broken aircraft routes:
    * They can be hard to spot (because it's a dashed line, not a solid line)
    * Sharp bends or gaps in the route can cause problems
    * Use [More Network Stuff](https://steamcommunity.com/sharedfiles/filedetails/?id=512314255) to repair routes if required

## Was it Fixed?

If not, try:

* [](Vehicles-not-spawning.md)
* [](Population-stuck-at-0.md)
* [](Tracked-vehicles-not-routing-or-spawning.md)
* [](Cims-not-using-public-transport.md)

Other issues? See: [](Troubleshooting.md)