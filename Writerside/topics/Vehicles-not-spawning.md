> Verified: February 2022 - TM:PE 11.6.4.8

> Note: Make sure you are using TM:PE 11.6.4.8 or later as it fixed a bug that could cause this problem.

# Symptoms

Any of the following:

* Outside traffic not spawning at highway outside connections
* [Vehicle Count Flickering Between 1 and 0](Vehicle Count Flickering Between 1 and 0) on building info panels
* Vehicles spawn, but quickly disappear (despawn)
* One or more buildings never spawn vehicles
* Buildings spawn only a few vehicles, but never reach their full capacity
* Industry trucks not spawning _(first casualty of hitting the vehicle limit!)_

# Causes

There are many possible causes for this, including:

* Bad road configuration
* Insufficient service budget
* Vehicle management mods doing strange things
* Missing workshop assets
* Stuck vehicles (rare but devastating)
* Vehicle limit (16384 maximum) reached - this can also be due to "stuck vehicles"
* Sharp bends or broken roads
* ...

# Solutions

### Make sure there are no broken nodes

* Subscribe and enable [Broken Nodes Detector](https://steamcommunity.com/sharedfiles/filedetails/?id=1777173984)
* Read mod description page to learn how to use it

### TM:PE users: Try these first...

* In [Policies](Policies.md) settings, set **[Vehicle restriction aggression](Vehicle restriction aggression)** to **Low**
    * If that fixed it, your [Vehicle Restrictions](Vehicle-Restrictions.md) and/or [Speed Limits](Speed-Limits.md) are the problem
    * A route that's too slow or incurs too many restriction penalties will prevent routing
* Check your [Lane Connectors](Lane-Connectors.md) and [Lane Arrows](Lane-Arrows.md) - can vehicles reach their destinations? ([example](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues/256))
    * Sometimes drawing a temporary bus route can help find problems
* Likewise, check any [Traffic Lights](Traffic Lights) - do they have 'green time' for the required route?

### Still not working? Check vehicle and citizen limits:

Install a mod that lists game limits and check Vehicle, Citizen, and Path limits:
    * [Watch It](https://steamcommunity.com/sharedfiles/filedetails/?id=1643902284) - enable it's "Game Limits" option then click the button on its toolbar to show the game limits screen
    * [Extended Managers Library](https://steamcommunity.com/sharedfiles/filedetails/?id=2696146165) - press `Ctrl`+`L` in-game to show its limits panel
    * **Note:** Don't use [Show Limits](https://steamcommunity.com/sharedfiles/filedetails/?id=494094728) or [Show More Limits](https://steamcommunity.com/sharedfiles/filedetails/?id=531738447) mods; they are older and do not list all game limits.

* **Vehicle limit reached?**
    * TM:PE users: Use the [Clear Traffic](Clear-Traffic.md) tool, and also the **Despawn... buttons** found in [Maintenance](Maintenance.md) [settings](Settings.md). This will eradicate any "stuck vehicles".
    * Use [Rebalanced Industries](https://steamcommunity.com/sharedfiles/filedetails/?id=1562650024) mod to reduce amount of industry traffic, especially in farms and forestry areas.
    * Use [Optimised Outside Connections](https://steamcommunity.com/sharedfiles/filedetails/?id=1721492498) mod to ensure cargo vehicles are more fully filled with cargo.
    * Use [Advanced Vehicle Options](https://steamcommunity.com/sharedfiles/filedetails/?id=1548831935) to increase capacity of vehicles. Don't go crazy - AIs get confused if the capacity is too big (see: [Vanilla Capacities](Vanilla Capacities)).
    * Use [Crazy Tourist Fix](https://steamcommunity.com/sharedfiles/filedetails/?id=1759269367) mod prevent tourists getting stuck in your city.
    * Certain [City and District Policies](City and District Policies) increase or decrease traffic
    * If you have a decent computer, you could try [More Vehicles Mod](https://steamcommunity.com/sharedfiles/filedetails/?id=1764208250) which increases the vehicle limit
* **Citizen limit reached?**
    * Use [Hide It, Bobby](https://steamcommunity.com/sharedfiles/filedetails/?id=2513657277) or [Remove All Animals](https://steamcommunity.com/sharedfiles/filedetails/?id=1706704781) mods to despawn animals (which count towards citizen limit)
    * Use [Rebalanced Industries](https://steamcommunity.com/sharedfiles/filedetails/?id=1562650024) mod to reduce number of outdoor workers in industry areas.
    * Use [Crazy Tourist Fix](https://steamcommunity.com/sharedfiles/filedetails/?id=1706337219) mod prevent tourists getting stuck in your city.
    * Certain [City and District Policies](City and District Policies) increase or decrease number of citizens in your city

There's also some information in [this Steam discussion](https://steamcommunity.com/app/255710/discussions/0/1638661595064078533) about vehicle limits that might be of use.

### Still not working? Check transport, buildings and city/district policies:

> Note: You can skip this section if your problem is relating to tracked vehicles (train, tram, monorail, metro)

* **Are growables also not spawning?**
    * See: [Broken District Styles](Broken District Styles)
* **Ensure direct road connection between source and destination:**
    * Check for things like 1-way roads that might limit available routes
    * Check for breaks in the road (especially if using mods like "Move It!" or similar)
    * Make sure there are no excessively sharp bends in the road (especially if using anarchy mods)
    * Check there aren't any really small segments (those can break vehicle AIs, particularly for busses)
    * Tip: Try drawing a bus route from source to destination to see if the route is viable
        * If it's not the road might be broken, or one-way section blocking traffic?
        * Check for sharp bends, or segments that aren't properly connected
        * Consider just rebuilding the road from scratch with smooth curves
* **Check your [City and District Policies](City and District Policies):**
    * In particular those (in link above) relating to **Vehicle Restrictions**, **Transport Preferences** and **Services**
    * If a policy that restricts vehicles blocks a route, build a bypass road to provide affected vehicles with an alternate route
* **Ensure buildings are within 2 units (small zoning squares) of a road:**
    * If they are further away, they will not connect to the road.
    * That means the pathfinder won't be able to route vehicles to or from them
* **Ensure buildings have valid spawn points:**
    * [Building Spawn Points](https://steamcommunity.com/sharedfiles/filedetails/?id=2511258910) mod allows you to edit spawn point positions, and warns if they are not valid.
    * [Spawn Points Fix](https://steamcommunity.com/sharedfiles/filedetails/?id=820157360) mod automatically fixes some spawn point issues in train stations and airports
* **Ensure buildings have residents / employees:**
    * Residential buildings must have people living in them before they will spawn vehicles
    * Industry, office and commercial must have employees before they will become fully operational
    * Not meeting building requirements (services, etc) can cause problems
    * For example, industry needs more than just transport - it needs medical, fire, etc.
    * Use [Show It!](https://steamcommunity.com/sharedfiles/filedetails/?id=1556715327) mod to see exactly what your buildings require
* **Are there road blockages causing traffic jams?**
    * Is there a train jam clogging up a level crossing?
    * Check for flooded or destroyed roads, collapsed or burning buildings, etc?
    * These will block roads for most traffic (eg. floods block all traffic; fires block some traffic)

### Still not working? Check budgets, mods and assets:

* Remove any [Broken Vehicle Assets](Broken Vehicle Assets) and [Broken Road Assets](Broken Road Assets)
* Use [Compatibility Report](https://steamcommunity.com/sharedfiles/filedetails/?id=2633433869) mod to scan for any broken/outdated mods; it will also suggest better alternatives
* **Outside connections:**
    * [Cargo Info](https://steamcommunity.com/sharedfiles/filedetails/?id=1072157697) mod is broken since Industries DLC; prevents vehicles spawning on highways and causes [Array Index - Symptom 7](Array Index - Symptom 7) error.
    * Non-highway roads require the [Any Road Outside Connections](https://steamcommunity.com/sharedfiles/filedetails/?id=883332136) mod to work (and it will take some minutes after creating the connection before it starts working)
    * Non-vanilla rail tracks cannot be used as outside connections; ensure last few segments of rail outside connections are made with vanilla rail tracks, not workshop tracks
    * See also: [Outside connections not working](Outside connections not working)
* **Check [service budgets](https://skylines.paradoxwikis.com/Economy#Budget):**
    * A budget lower than 100% will reduce the number of vehicles that can spawn from service buildings
    * [Total Autobudget](https://steamcommunity.com/sharedfiles/filedetails/?id=1541897355) mod can sometimes cause problems (it's recently been improved but try without it)
    * Try setting a budget of 100% or more (for day and night) and see if that helps
* **Check building workers:**
    * Not enough workers? Ensure you have sufficient education services for your city size.
* **Check building capacity:**
    * Most service buildings have a capacity - once they are full, they won't spawn more vehicles until they start to empty
    * Some buildings, like cemeteries and garbage dumps must be manually emptied (button on their building info panel)
    * Even buildings like recycling plants and crematoriums can fill up if demand is too high
    * If all your buildings are full, you need more buildings or much higher budgets.
* **Check vehicle assets are available:**
    * If you use vehicle assets from the workshop, check they are still subscribed and working
    * Sometimes asset creator deletes their asset and it will disappear from the game
    * If you skip vanilla vehicles using Loading Screen Mod, ensure you have workshop alternatives subscribed
* **Mods that limit, restrict or control spawning:**
    * [Advanced Vehicle Options (**AVO**)](https://steamcommunity.com/sharedfiles/filedetails/?id=1548831935) ([older version](https://steamcommunity.com/sharedfiles/filedetails/?id=442167376)):
        * There are two versions of AVO - only use one, _unsubscribe_ the other
        * In AVO mod options, _turn off_ the "Disable warning at map loading" option
        * Ensure the enabled vehicles are still available
    * [District Service Limit 3](https://steamcommunity.com/sharedfiles/filedetails/?id=1181352643) (DSL3):
        * Check districts still exist
        * For each service building, check it can reach its districts by road
        * Remember that service buildings still have a distance limit
        * If the only available building is out of range of a location that needs serving, no vehicle will spawn
        * Use [Customize It!](https://steamcommunity.com/sharedfiles/filedetails/?id=1369729955) mod and look for a property containing the word "Radius" - increase the value if necessary.
        * In DLS3 mod options, _turn off_ all options except the first one ("Service buildings...") and, optionally, the last one ("Display...)
        * If you want cims to shop locally, etc., use the [Real Time](https://steamcommunity.com/sharedfiles/filedetails/?id=1420955187) mod.
    * [Service Vehicles Manager 2](https://steamcommunity.com/sharedfiles/filedetails/?id=1632320836) or [Service Vehicle Selector 2](https://steamcommunity.com/sharedfiles/filedetails/?id=934994075):
        * Ensure chosen vehicles are still available
* **Check vehicle capacities:**
    * You can use the Advanced Vehicle Options (AVO) mod to check capacities
    * If you use workshop vehicles, check that they don't have stupidly large capacities
    * If the capacity is much greater than vanilla vehicles, it will confuse the AI, for example:
      > Your hearse has capacity of 10, and the city has 100 dead people.  
      > The game will spawn 10 hearses and each will visit 10 different buildings (Good!).  
      > If your hearse has capacity of 100, the game will spawn one hearse and it will have to visit 100 buildings (Bad!).
    * See: [Vanilla capacities](Vanilla capacities)
* **Check vehicle speeds:**
    * If vehicles are too fast (either defined in the asset, or altered with AVO), it confuses the game
    * This issue particularly affects ships (example: [Red fishing boat](https://steamcommunity.com/sharedfiles/filedetails/?id=1107521505))
    * Use AVO mod to inspect vanilla vehicles to see what speed they use, and then ensure workshop vehicles are in the same sort of speed range
* **[Industries DLC](https://store.steampowered.com/app/715194/Cities_Skylines__Industries/) vehicles don't have a dedicated service assignment:**
    * This applies mainly to farming and mining industry vehicles of following types:
        * Delivery Truck
        * Delivery Truck with Trailer
        * Delivery Van
        * Livestock Truck with Trailer
    * Do not deactivate these vehicles from spawning, as your own placed industries will never spawn any vehicle. The community needs to develop alternate vehicles with correct vehicle service, so that these vehicles can be replaced in future.
* **Custom "unique factories" might require specific vehicle assets:**
    * Check the "Required Items" on the details page of the asset.

# Fixed?

If not, do any of the following apply?

* [Vehicle Count Flickering Between 1 and 0](Vehicle Count Flickering Between 1 and 0)
* [Outside connections not working](Outside connections not working)
* [Hearses not spawning](Hearses not spawning)
* [Busses not spawning from depots](Busses not spawning from depots)
* [Tracked vehicles not routing or spawning](Tracked vehicles not routing or spawning)

Still not fixed? Please let us know: [Report a bug](Report a bug)

Something else? See: [Troubleshooting](Troubleshooting)