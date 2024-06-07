> Article verified: December 2021 - TM:PE 11.5.2

## Symptom

* After unsubscribing a workshop network, save games no longer load
* This can also happen in the author of that network removes it from workshop or deletes their Steam account

> "Workshop networks" mean any road, rail, metro, tram or monorail, or any specialised networks derived from them, that you have subscribed to in the Steam Workshop - either as an _asset_ or a _mod containing the assets_.

## Cause

These issues are _not_ caused by TM:PE.

If you placed a workshop network (or a building that contains one) in your city (or a map/scenario file), you won't be able to load it if the network is missing.

Luckily there's some mods and workshop assets that can usually get you back up and running :)

> Tip: After applying either of the solutions below, use the [Broken Nodes Detector](https://steamcommunity.com/sharedfiles/filedetails/?id=1777173984) mod to check for side-effects of network removal (such as broken transport lines, stops, and ghost nodes). If you use TM:PE it's probably also worth using the [Clear Traffic](Clear-Traffic.md) button to remove all existing traffic, and also check for any broken junction settings (particularly broken [Lane Connectors](Lane-Connectors.md)).

## Solution 1 - Replace before removing

> Use this solution if you are planning to remove certain networks from a city that still loads.

* Subscribe and enable [Loading Screen Mod](https://steamcommunity.com/sharedfiles/filedetails/?id=2731207699) (LSM)
    * Make sure it's "Sharing" options are all enabled to minimise RAM consumption while loading
* Subscribe and enable [RON, the network replacer](https://steamcommunity.com/sharedfiles/filedetails/?id=2405917899) (RON) mod.
    * If you want to replace **Network Extensions 2** (NExt2) mod with normal roads, subscribe [NExt replacement assets](https://steamcommunity.com/sharedfiles/filedetails/?id=2585558081).
    * If you want to replace **Metro Overhaul Mod** (MON) tracks with normal tracks, subscribe [MOM replacement assets](https://steamcommunity.com/workshop/filedetails/?id=2744697433).
* Load your save
* Use the RON mod to replace networks as necessary
    * Read the instructions on RON workshop page or watch (youtube) [RON video tutorial](https://www.youtube.com/watch?v=tXdqPqvp7Uk).
* Save game under new file name
* Exit to desktop, unsubscribe the unwanted networks (mods or assets) you no longer use

If the new savegame no longer works, use LSM to generate missing asset report (set in mod options prior to loading the savegame) and subscribe any missing networks, then repeat the process.

## Solution 2 - How to fix a broken savegame

If your save game fails to load, due to missing NExt or MOM networks:

* Subscribe and enable [Loading Screen Mod](https://steamcommunity.com/sharedfiles/filedetails/?id=2731207699) (LSM):
    * In it's mod options, enable the **Safe Mode** options which help recover from errors during loading
    * For more details: [Finding Broken & Bloated Assets](https://steamcommunity.com/sharedfiles/filedetails/?id=1846793796)
* Subscribe and enable [Safenets](https://steamcommunity.com/sharedfiles/filedetails/?id=1620588636) mod:
    * This will overcome most issues with missing networks
    * Specifically, it tries to fix: [Simulation error Object reference not set](Simulation error Object reference not set) (the `RoadBaseAI.CanEnableTrafficLights` error)
* Subscribe and enable [RON, the network replacer](https://steamcommunity.com/sharedfiles/filedetails/?id=2405917899) (RON) mod:
    * If you want to replace **Network Extensions 2** (NExt2) mod with normal roads, subscribe [NExt replacement assets](https://steamcommunity.com/sharedfiles/filedetails/?id=2585558081).
    * If you want to replace **Metro Overhaul Mod** (MON) tracks with normal tracks, subscribe [MOM replacement assets](https://steamcommunity.com/workshop/filedetails/?id=2744697433).
    * It should automatically replace old networks from the mods with the newly subscribed workshop assets during the loading process.
* Try loading your game...

If the save loads properly, save it under a new file name, then exit to desktop. It should work fine after that.

#### Missing networks?

If the save still fails to load, enable the reporting options in LSM mod, then try again. The LSM report contains a section about "Nets" or "Networks" which lists any missing network assets. Clicking on the links will take you to the workshop page where you can subscribe the asset and that might get your game running again (if so, refer to Solution 1 to remove those networks from the map then you can try unsubscribing them again).

#### Required items missing?

If it's still not loading, you might be missing some 'Required Items' that are necessary for your other mods/assets to work. This is particularly common with things like train, metro and tram stations, but it can affect other buildings too. The required items are listed in the sidebar on workshop mod and asset pages...

To work out which workshop mod or asset might be affected, look in your [log file](Share-your-Cities-Skylines-log-fil.) for `netinfo` errors like the following:

> If you see this, look for an asset name on the preceding lines in the log file then check its workshop page
> ```
> NullReferenceException: Object reference not set to an instance of an object
> at PrefabCollection`1[NetInfo] ...
> ```

> If you see something like this, the number before the asset name is the workshop id:
> ```
> Custom Assets: 800515680.Lindblum International Airport_Data: NetInfo missing
>   at BuildingInfo.InitializePrefab () [0x00000] in <filename unknown>:0
> ```
> In the example above, you could navigate to https://steamcommunity.com/sharedfiles/filedetails/?id=800515680 to view the workshop page

> If you see this, it's not a problem and you can ignore it:
> ```
> Custom Assets: 1213488864.Pedestrian Slope2: Duplicate prefab name
>   at PrefabCollection`1[NetInfo].InitializePrefabImpl
> ```
> LSM detects and removes duplicates to reduce RAM consumption so this is actually a good thing.

Once you identify a building that has a missing network, you can either:

* Unsubscribe the building, or
* Look in its 'Required Items' list (on workshop page) and subscribe any networks you're missing

After doing that for all buildings, try loading the save again. If it works, save under new name and then it's up to you what you do with those buildings you just fixed/removed.

## Fixed?

If not, it's possible one of your mods is broken by missing networks. Most commonly it will be a mod that specifically deals with networks, such as MOM, Railway Replacer, Catenary Replacer, etc. Try disabling them, then exit to desktop, then relaunch game and try loading the save.

Other issues? See: [Troubleshooting](Troubleshooting)