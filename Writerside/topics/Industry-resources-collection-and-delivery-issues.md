> Verified: February 2022 - TM:PE 11.6.4.8

## Symptoms

One or more of these issues may occur:

* Trucks aren't collecting raw resources from extraction buildings
* Trucks aren't delivering raw resources to production buildings
* Trucks aren't spawning from industry buildings (including storage and warehouses)
* Industry vehicles not working outside central 25 Tile area

## Causes

* [Adjustable Business Consumption](https://steamcommunity.com/sharedfiles/filedetails/?id=1108715012) mod can cause problems with industry (regardless of whether you use TM:PE), in particular it can prevent trucks spawning from storage and warehouse buildings.

Older causes which have since been fixed:

* [#85](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues/85): "Ban cars/trucks on bus lanes" causes issues with industry
    * This is fixed in TM:PE v11.6.4.8 (PR #1381) and later
    * The issue was caused by the **Ban private cars and trucks on bus lanes** option in [Policies](Policies.md) settings
* [#1097](https://github.com/CitiesSkylinesMods/TMPE/issues/1097): Industries vehicles not working outside central 25 Tile area
    * This is fixed in TM:PE v11.6 and later
    * It was caused by pathfinding issues outside central 25 Tile area
    * 81 Tiles mod has also includes the same bugfix

## Solutions

* Make sure your're using TM:PE v11.6.4.8 or later
* If you use [Adjustable Business Consumption](https://steamcommunity.com/sharedfiles/filedetails/?id=1108715012) mod, disable it, exit to desktop
    * The problem should be solved next time you load your city
* If vehicles aren't spawning, see: [Vehicles not spawning](Vehicles not spawning)

# Fixed?

If not, please let us know: [Report a Bug](Report a Bug)

Other problems? See: [Troubleshooting](Troubleshooting)