> Article verified: August 2019

# Symptoms

* Cims aren't using public transport
* Specifically:
    * Vehicles are working fine and going between stops,
    * But cims aren't waiting at the stops; they're not using the transport service, or only a very small number use it.

> Vehicles not spawning, or problems routing? See:
>  
> * [Busses not spawning from depots](Busses not spawning from depots)
> * [Tracked vehicles not routing or spawning](Tracked vehicles not routing or spawning) -- metros, trains, trams, monorail

# Cause

This can be caused by:

* Lack of comprehension of game mechanics
* Mod-related issues
* Problems with the stops or route

# Solutions

### Game mechanics

If you provide good transport service, cims are more likely to use PT. That means they need to be able to find good public transport from where they live (residential areas) to where they work (offices, industry, commerce), shop (commerce), get educated (schools, universities, campuses) and play (parks, unique buildings, monuments, etc).

* TM:PE highlights problems with public transport on the [](Public Transport Info View).
* TM:PE highlights problems with parking (cims often drive to stations) on the [](Traffic Info View)
* [Real Time](https://steamcommunity.com/sharedfiles/filedetails/?id=1420955187) mod highlights which buildings cims are struggling to reach on the [Traffic Routes Info View](Traffic Routes Info View)

### Mods:

Mods which change budgets can cause lots of problems:

* [AutoLineBudget](https://steamcommunity.com/sharedfiles/filedetails/?id=1767246646) - known to cause severe problems
* Any other mods which affect transport budgets (eg. [Total Autobudget](https://steamcommunity.com/sharedfiles/filedetails/?id=1541897355))

If the budget mod has features for setting which budgets it controls, prevent it from controlling transport budgets. If it doesn't let you do that, disable or unsubscribe it then exit to desktop and then reload the game to see what happens.

Some mods change public transport preferences of cims, either directly or based on transport cost, for example:

* [Ticket Price Customizer](https://steamcommunity.com/sharedfiles/filedetails/?id=1393820309) mod?
* [Resident Travel Rebalance](https://steamcommunity.com/sharedfiles/filedetails/?id=541673195)

Try disabling mods like that, exit to desktop and then reload the game to see what happens.

### Roads:

* Roads with pavements are essential for your transit infrastructure
    * No pavement = pedestrians can't navigate the road (or even park on it in most cases)
* Highways and some other roads don't have pedestrian pavements
    * There might be some workshop high way assets that have pavements?
* Elevated roads generally do not support 'stops' on transport routes
    * [Elevated Stops Enabler](https://steamcommunity.com/sharedfiles/filedetails/?id=634913093) removes that limitation

### Transport buildings:

> Train stations, bus depots, harbours, airports, metro entrances, etc...

* Building must be within 2 zoning tiles of a road to connect to the road
* If the road has no pavement, pedestrians can't access the building and thus won't use the transport
* Some workshop assets are broken
    * Some buildings don't define spawn points where cims enter and leave the building
    * Subscribe and enable [Spawn Points Fix](https://steamcommunity.com/sharedfiles/filedetails/?id=820157360) to solve that

### Vehicles

* Check passenger capacity of vehicles using [Advanced Vehicle Options](https://steamcommunity.com/sharedfiles/filedetails/?id=1548831935) mod, and compare with [Vanilla Capacities](Vanilla Capacities)
* A much larger capacity than vanilla can confuse the transport AIs and they do all sorts of weird things
    > Example: For busses and trains they'll often get "stuck" when cims try to board the vehicle
* A smaller capacity is generally not a problem as far as we can tell, although sometimes the AI might overfill a vehicle
    > Example: If you had a small transit van bus with a capacity of 12, the game will put up to 15 people in it - but it still works

### Converter mods:

* If you use 'Converter' mods to change transport type of buildings or vehicles, check the settings:
    > Example: Did you convert stations to metro stations for use with Metro Overhaul Mod (MOM) and then later remove the MOM mod?
    >  
    > Example: Did you convert some trains to trams and then later disable the Snowfall DLC?

### Traffic Manager: President Edition (TM:PE):

* Make sure you are using TM:PE 10.21.1 or later; earlier versions had bad bugs in Parking AI
* In [](Policies.md), set **Vehicle restrictions aggression** to **Low** - if that works, your [](Vehicle-Restrictions.md) are causing the problem.
* Check your [](Junction-Restrictions.md) - in particular, disabled pedestrian crossings can sometimes [confuse the pathfinder](https://github.com/VictorPhilipp/Cities-Skylines-Traffic-Manager-President-Edition/issues/168)

### [Metro Overhaul Mod](https://steamcommunity.com/sharedfiles/filedetails/?id=816260433) (MOM) users:

* Note: MOM v9 has now been released so the suggestions below might not work any more.
* Make sure your metro stations are _shorter_ than 192 meters long (try default 144m)
* If they are longer it sometimes breaks the AI and cims will stop using the station
* Check any pedestrian path connections that might be needed for the station
* If problems persist with MOM, contact the author of MOM

# Fixed?

If not:

* You might have hit vehicle or citizen limits, see: [Vehicles not spawning](Vehicles not spawning)
* If you feel it's an issue with TM:PE, please let us know: [Report a bug](Report a bug)

Something else? See: [Troubleshooting](Troubleshooting)