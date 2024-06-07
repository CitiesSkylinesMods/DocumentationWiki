> Verified: January 2022

The guidance below, mostly about vehicles and roads, is general-purpose - it also applies to unmodded vanilla game!

## Vehicles

### Vehicle Capacity

Do not make vehicles with overly large capacities. They should be in the same 'ball park' as [Vanilla capacities](Vanilla capacities).

For example, say you have a hearse with a capacity of 10 (vanilla) and there are 100 dead people: The AI will send out 10 hearses, and each will visit 10 buildings. Now, imagine a hearse with capacity 100: The game sends out 1 hearse, and it has to visit 100 buildings which takes much longer.

Excessively large capacities on public transport vehicles can cause them to get "stuck" in the boarding phase as the game does not extend boarding time based on number of people boarding. This also happens in base game, but seems to be exacerbated by mods such as IPT2, TLM. Realistic Walking Speed, Real Time, and potentially also TM:PE.

### Vehicle Speed

Don't make unusually fast or slow vehicles as it can confuse the AIs, even in vanilla game. Try and keep their speeds similar to their vanilla vehicle counterparts.

Boats in particular are very fussy:

* Boats that are too fast might clog shipping lanes, which in turn can somehow use up the vehicle limit and prevent other vehicles spawning (see: [Issue #317](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues/317))
* Also, if too fast, the boat can struggle to make turns as it keeps 'overshooting' where it's trying to get to; it can end up going round in circles!
* If a boat is too slow, it can struggle against strong water currents (the grey arrows you see in water info view; yes, the boat simulation is affected by them!).

But it can affect other vehicles too, for example [Issue #1115](https://github.com/CitiesSkylinesMods/TMPE/issues/1115): Industry & Commercial vehicles getting stuck at every industrial & commercial area.

Please note that TM:PE also affects vehicle speeds, mostly for road vehicles, in numerous ways:

* [Individual driving styles](Individual driving styles) (formerly called "Realistic Driving Speeds")
* [Reckless Drivers](Reckless-Drivers.md)
* [Road Conditions](Road Conditions)
* [Speed Limits](Speed-Limits.md) (of the road)

The speed you see vehicles moving in-game might be slower or faster than that defined by the vehicle asset due to the factors above.

### Flashing Vehicle LOD

This is a common problem with vehicle assets, and people often ask if it's TM:PE that's causing the problem.

It's not. See: [Vehicle LODs are flashing](Vehicle LODs are flashing)

Make sure your [**Illumination** (```_i```) and/or **Color** (```_c```) maps](https://cslmodding.info/asset/vehicle/) include indicators, brake lights, etc.

## Networks

### Medians aren't a barrier for vehicles

It was assumed that the ```NetInfo.m_CanCrossLanes``` setting was something to do with vehicles and road medians, however [this does not appear to be the case](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues/192). That property seems to be more about small roads (no medians) and determines whether vehicles can _cross oncoming traffic_ lanes to reach a destination (eg. a parking space) on the other side of the road.

Currently the only known way to prevent vehicles crossing medians is to use TM:PE lane arrows or lane connector tools to force vehicles to stay in lane at junctions, and relay this information to end-users via screenshots depicting what it should look like ([example 1](https://steamcommunity.com/sharedfiles/filedetails/?id=1327917624), [example 2](https://steamcommunity.com/sharedfiles/filedetails/?id=1718180429)).

We are attempting to implement something in TM:PE that will do this automatically; see: [Issue #504](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues/504)

If you know a better way to solve this issue, ideally in a way that works in unmodded games, please let us know!

## Roads with inverted lane directions

It's possible to create roads with inverted lane directions, however these can pose a challenge to pathfinding and some of the advanced features of TM:PE.

If you're creating such roads, please let us know if you run in to problems!

## Road speed limits

If your road or rails (including tram, metro, monorail) doesn't work with the [Speed Limits](Speed-Limits.md) tool, ensure the following criteria are met (items marked 📜 are reported in the [[TMPE.log]] file):

* Property `name` must _not_ be `null` or empty string 📜 
* Property `m_netAI` must _not_ be `null` 📜 
* The `m_netAI` must be one of the following (as of August 2019):
    * `RoadBaseAI`
    * `TrainTrackBaseAI`
    * `MetroTrackAI`
    * We are considering adding more in the future
    * AI warnings are only logged by `DEBUG` builds with debug switch `26` (`SpeedLimits`) enabled
* If the road requires DLC, the DLC must be active 📜 
* Property `m_vehicleTypes` must _not_ be `None` or only `Bicycle` 📜 
    * We might add support for bike paths in the future

If your road does not meet the above criteria, the speed limits tool will not recognise it.
* Property `name` must _not_ be `null` or empty string 📜 

## Parking lanes
If your road's parking lanes don't work with the [Parking Restrictions](Parking-Restrictions.md) tool, ensure the following criteria are met (items marked 📜 are reported in the [[TMPE.log]] file):

* The `m_direction` or `m_finalDirection` must be forward or backward 📜 
* errors are only logged by `DEBUG` builds with debug switch `2` (`BasicParkingAILog`) enabled

If your road does not meet the above criteria, the parking restrictions tool will not work as expected.

## See also

* [CSL modding info](https://cslmodding.info/) - excellent resource for asset creators
* [Loading Screen Mod - Guide](https://steamcommunity.com/workshop/filedetails/discussion/667342976/1636416951459546732/) - how to take best advantage of Loading Screen Mod (make sure you read the smaller guides at bottom too)
* [/r/CitiesSkylinesModding](https://www.reddit.com/r/CitiesSkylinesModding/) - reddit sub dedicated to C:SL modding
* TM:PE's [Troubleshooting](Troubleshooting) guide - covers a vast range of issues