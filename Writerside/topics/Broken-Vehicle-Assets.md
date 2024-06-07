# Broken Vehicle Assets
> Article verified: September 2022 - TM:PE 11.7.0

> If you haven't already done so, subscribe and enable [Loading Screen Mod](https://steamcommunity.com/sharedfiles/filedetails/?id=667342976) - it loads maps much faster, reduces RAM consumption for better in-game performance, and fixes a load of common workshop bugs.

### Finding broken assets

We've listed several known broken assets in the sections below, but if you want to check yourself see this Steam guide: [Finding Broken & Bloated Workshop Subscriptions](https://steamcommunity.com/sharedfiles/filedetails/?id=1846793796).

* The [Loading Screen Mod](https://steamcommunity.com/sharedfiles/filedetails/?id=667342976) has an option to **Check assets for errors** which is very useful for finding broken assets!
* To find bloated vehicle assets, which can reduce frame rate and cause lag, use the [Mesh Info mod](https://steamcommunity.com/sharedfiles/filedetails/?id=453956891).

If you find additional broken assets, please edit this wiki page and add them to the relevant section.

### Potentially game breaking

* [727-200 Freighter UPS](https://steamcommunity.com/sharedfiles/filedetails/?id=1562199538) - broken LOD aci followed by crash to dekstop

### Vehicle LODs Turn White

> It usually happens at night, when vehicle lights come on. This is caused by broken textures in the asset; the asset author will need to recreate their LOD.

* [Retro Trains Pack - West Coast Freight](https://steamcommunity.com/sharedfiles/filedetails/?id=1397356782)
* [Mercedes-Benz Vito - Posti](https://steamcommunity.com/sharedfiles/filedetails/?id=1650043050)
* [Supermarket Delivery Trucks + Props No DLC Required v2](https://steamcommunity.com/sharedfiles/filedetails/?id=2185859125)

### Vehicle LODs Turn Black

Troubleshooting guide: [](Shiny-Black-Vehicle-LODs.md)

> This is caused by assets that have [invalid texture sizes](https://steamcommunity.com/workshop/filedetails/discussion/667342976/1639789306562159404/) (their dimensions _must_ be a power of two). The [Loading Screen Mod](https://steamcommunity.com/sharedfiles/filedetails/?id=667342976) has option to **Check assets for errors** which will tell you if you have any assets with this issue.

> Thanks to **thale5** for the diagnostic tools in Loading Screen Mod, and REV0 for using it to test loads of train assets.

* ~~[BR 187 - BLS/Wascosa (8Cars)](https://steamcommunity.com/sharedfiles/filedetails/?id=1557982704)~~ - FIXED!
* ~~[Alstom Euroduplex - TGV Carmillon](https://steamcommunity.com/sharedfiles/filedetails/?id=1269154707) (and also variants with different numbers of cars)~~ - Removed from Workshop
    * Solution: Unsubscribe asset
    * New versions of this train can be found in [France Vehicles collection](https://steamcommunity.com/workshop/filedetails/?id=1210339919)
* ~~[BR 187 - Railpool/ZACENS Oil Mixed](https://steamcommunity.com/sharedfiles/filedetails/?id=1559332186) (and also variants with different numbers of cars)~~ - FIXED!
* [DB BR101 EuroCity (SBB 12 Cars)](https://steamcommunity.com/sharedfiles/filedetails/?id=1635423025)
* ~~[Deutsche Bahn Intercity 2 (5Cars)](https://steamcommunity.com/sharedfiles/filedetails/?id=1548586669)~~ - FIXED!
* [DR 232 Demag Molten Iron](https://steamcommunity.com/sharedfiles/filedetails/?id=1377524690) (and also variants with different numbers of cars)
    * There might be working alternate versions in [Ludmilla collection](https://steamcommunity.com/workshop/filedetails/?id=1344154587)
* [JR East series E231-500 (11 Cars)](https://steamcommunity.com/sharedfiles/filedetails/?id=1692260417)
* [SBB Re 460 EuroCity (12 Cars)](https://steamcommunity.com/sharedfiles/filedetails/?id=1635422665)
* [Small Boat](https://steamcommunity.com/sharedfiles/filedetails/?id=667891104) - confirmed to cause issue
* ~~[Small Ship](https://steamcommunity.com/sharedfiles/filedetails/?id=931760630) - derived from the 'Small Boat' asset above, so possibly has the same issue~~
* [STADLER EURODUAL DIESEL MOD Passenger Train (Concept)](https://steamcommunity.com/sharedfiles/filedetails/?id=1424374795)
* [Stadler KISS - Caltrain (4Cars)](https://steamcommunity.com/sharedfiles/filedetails/?id=1292613603) - REVO will update asset to fix (October 2019)
* [Stadler KISS - Caltrain (6Cars)](https://steamcommunity.com/sharedfiles/filedetails/?id=1290545737) - REVO will update asset to fix (October 2019)
* [Stadler KISS - Generic/Factory (5Cars)](https://steamcommunity.com/sharedfiles/filedetails/?id=1292357726) - REVO will update asset to fix (October 2019)
* ~~[Taurus Cargo](https://steamcommunity.com/sharedfiles/filedetails/?id=457431411)~~ - FIXED!
* ~~[Tobu 500 Series (3/6 Cars) "Revaty"](https://steamcommunity.com/sharedfiles/filedetails/?id=1854555434)~~ - FIXED!
* [TRAXX Cargo (MRCE)](https://steamcommunity.com/sharedfiles/filedetails/?id=611092038)
* [TRAXX Coil cargo (DB BR185)](https://steamcommunity.com/sharedfiles/filedetails/?id=639383797)

> October 2019: REV0 is currently updating all his train vehicle and prop assets to fix the LOD sizes.

### Vehicle LODs Flashing:

Troubleshooting guide: [Vehicle LODs are flashing](Vehicle-LODs-are-flashing.md)

> If you still want to use the vehicle, you could try an extreme option: [Disable LODs!](https://steamcommunity.com/sharedfiles/filedetails/?id=1680642819)

* [Royal Mail Van Transit](https://steamcommunity.com/sharedfiles/filedetails/?id=1549566008)
* [Saab 900 Pack 3 Cars](https://steamcommunity.com/sharedfiles/filedetails/?id=2089434425) (Utoftfighter sadly don't have the source files anymore. Perhaps he will recreate them someday)
* We'll list more as we find them

### Distorted LODs:

> If you still want to use the vehicle, you could try an extreme option: [Disable LODs!](https://steamcommunity.com/sharedfiles/filedetails/?id=1680642819)  

* [NS Mercedes Sprinter Ambulance](https://steamcommunity.com/sharedfiles/filedetails/?id=447824501)
    * Working alternative: [D3S Mercedes-Benz Sprinter NLAmbulance (W906) '2006](https://steamcommunity.com/sharedfiles/filedetails/?id=454671605)

### Bloated Assets:

> To find bloated assets, which can reduce frame rate and cause lag, use the [Mesh Info mod](https://steamcommunity.com/sharedfiles/filedetails/?id=453956891).

* [Audi TT](https://steamcommunity.com/sharedfiles/filedetails/?id=449730427) - huge LOD (1800 tris!)

### Breaks vehicle spawning:

If you see [](Helicopters-and-trucks-from-wrong-depots.md):

> Asset authors: If your vehicle exhibits this bug, try reconstructing it and re-upload to workshop (thanks Ninjanoobslayer for the tip!)

* ~~[2018 Red Rosenbauer Commander Pumper](https://steamcommunity.com/sharedfiles/filedetails/?id=1942782674)~~ FIXED!

If vehicles stop spawning ([Issue #317](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues/317)):

* Alfa Romeo 164
    * Asset id: 453021816 (no longer in workshop)
* NoMads Semi class F
    * Asset id: 450619803 (no longer in workshop)
    * Solution: Unsubscribe it
* Red Fishing Boat
    * Asset id: 1107521505 (no longer in workshop)
    * The boat is too fast, which seems to confuse the cargo ship AI. As a result, it blocks shipping lanes and somehow uses up all the available vehicle limit which in turn prevents other vehicles from spawning.
    * Solution: Use "Advanced Vehicle Options" mod to slow it down; if that doesn't work, unsubscribe it
* Blue Fishing Boat
    * Asset id: 1107517568 (no longer in workshop)
    * Same issue as the Red Fishing Boat above.
* Tugboat
    * Asset id: 1107513981 (no longer in workshop)
    * Same issue as the fishing boats above.
* VW Golf GTI 2010
    * Asset id: 450652597 (no longer in workshop)
    * Solution: Unsubscribe it
    * There is a [fixed version](https://steamcommunity.com/sharedfiles/filedetails/?id=456120777), but it's bloated and may cause lag or fps drop

There are many other cuases of vehicles not spawning:

* [](Vehicles-not-spawning.md)