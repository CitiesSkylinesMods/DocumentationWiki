> Verified: January 2022 - TM:PE 11.5.2 / TM:PE 11.6
>  
> **Notes:**
> * If the error is `IndexOutOfRangeException: Array index is out of range`, it might be caused by [](Broken road assets) (see that link for solutions).
> * All versions of Loading Screen Mod include [Safe Mode options](https://steamcommunity.com/workshop/filedetails/discussion/667342976/1626286205707786286/) that can _sometimes_ help recover from the "Array index" errors. See **Loading Screen Mod** section at bottom of this guide for details.

## Symptom

You will see this error on-screen - either while a savegame is loading, or in-game:

* `Simulation error: Array index is out of range.`

There are several variants, each caused by a different mod or sometimes broken workshop asset. You can determine which one you have by searching for the above error message in your [**log file**](Share-your-Cities-Skylines-log-file.) and then checking what is on the next line...

## Cause / Solution

> There are so many differnt causes of the error that we created separate pages for most of them; click `Array Index - Symptom x` links, where available, for solutions to that specific error.

Array Index - Symptom 1:

* `at WG_PopOnly.CommercialBuildingAIMod ...`
* or something similar starting with `at WG_`
* ~~Symptom 1 has been fixed! Make sure you are using latest version of [WG Configurable Population Modifiers](https://steamcommunity.com/sharedfiles/filedetails/?id=652921941) mod.~~
* Update November 2021: Use the [Realistic Population Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2025147082&searchtext=realistic+population+revived) mod instead.

[Array Index - Symptom 2](Array Index - Symptom 2):

* `at PassengerTrainAI.SimulationStep ...`
* or `at PassengerTrainAI.StartPathFind ...`
* or something similar starting with `at PassengerTrainAI`
* or `at MetroOverhaul.Detours.PassengerTrainAIDetour.StartPathFind`

[Array Index - Symptom 3](Array Index - Symptom 3):

* `at TransportLine.GetNextStop ...`
* followed by `at BusAI.ArriveAtTarget ...`

[Array Index - Symptom 4](Array Index - Symptom 4):

* `at WaterSimulation.LockWaterSource ...`
* `at ImprovedPublicTransport2.Detour.VehicleManagerMod.ReleaseWaterSource ...`

[Array Index - Symptom 5](Array Index - Symptom 5):

* `at BuildingThemes.Detour.ZoneBlockDetour ...`

[Array Index - Symptom 6](Array Index - Symptom 6):

* `at BuildingAI.EnsureCitizenUnits ...`

[Array Index - Symptom 7](Array Index - Symptom 7):

* `at CargoInfoMod.CargoData.Count ...`

[Array Index - Symptom 8](Array Index - Symptom 8):

* `at UnlockManager.Unlocked ...`

[Array Index - Symptom 9](Array Index - Symptom 9):

* `Node is not connected to segment`
* `Warning #: ExtSegmentEndManager.GetIndex(#, #): Node is not connected to segment.`

[Array Index - Symptom 10](Array Index - Symptom 10):

* `at TerrainModify.ApplyQuad ...`
* `at TerrainModify.UpdateAreaImplementation ...`

[Array Index - Symptom 11](Array Index - Symptom 11):

* `at TerrainManager.GetSurfaceCell ...`
* `Parameter name: index` followed by `at System.Collections.Generic.List ...`

[Array Index - Symptom 12](Array Index - Symptom 12):

* `at GeneratedScrollPanel.IntializeUIAssetFilters`

[Array Index - Symptom 13](Array Index - Symptom 13):

* `at TransportLineAI.CheckNodePosition`

[Array Index - Symptom 14](Array Index - Symptom 14):

* `at EPTUI2.UITransportLineRow.Update`

Array Index - Symptom 15:

* `at TransportLine.GetNextStop`
* [#867](https://github.com/CitiesSkylinesMods/TMPE/issues/867): If the stack trace mentions aircraft or helicopters or blimps, it's likely due to building a airport/helipad/depot outside of the central 25 tile area.

Array Index - Symptom 16:

* `NetManager+Data.Deserialize`
* [#1195](https://github.com/CitiesSkylinesMods/TMPE/issues/1195): Likely caused by outdated mods or broken road assets.
* Use LSM "Safe Mode" (detailed further down this page) which can sometimes recover a broken save.
* Use [Compatibility Report](https://steamcommunity.com/sharedfiles/filedetails/?id=2633433869) mod which can help track dowmn broken mods and suggest better alternatives.

## General Solutions

There are some other things you can try...

### Checking for broken mods and assets

Use [Compatibility Report](https://steamcommunity.com/sharedfiles/filedetails/?id=2633433869) mod from Steam Workshop - it can help track dowmn broken mods and suggest better alternatives.

Also, check the Steam Guide on [Finding Broken and Bloated Workshop Subscriptions](https://steamcommunity.com/sharedfiles/filedetails/?id=1846793796) which can help track down other broken mods and assets.

### Loading Screen Mod: Safe Mode

Some array index errors can be fixed using the "Safe Mode" options in Loading Screen Mod:

1. Exit game to desktop
2. Subscribe and enable [Loading Screen Mod](https://steamcommunity.com/sharedfiles/filedetails/?id=667342976) (LSM)
3. In it's mod options:
    * Enable the optimisation/sharing options to reduce RAM use (will make games load faster)
    * Enable the safe mode options
4. Now load your save - LSM will do everything it can to beat those errors

In some cases it might only work once, but the error will come back on the next load. If that happens, you'll have to try and track down what specifically is causing the error and fix it at source.

## Fixed?

* Please post details of your error on the workshop page of the mod or asset causing the problem
* You can often get help on the official [Cities: Skylines Discord server](https://discordapp.com/channels/263634513861541888/513313798875119657).
* If you use **More Vehicles mod** please note that lots of other mods aren't compatible as they generally hard-code the vehicle limit. The "Compatibility Report" mod will often tell you if that is the case.
    * TM:PE versions 10.21.1, 11.0 and later are all compatible with More Vehicles.
* If you think it's caused by TM:PE, please [Report a bug](Report a bug) (TM:PE users only, please - we can't help debug other mods, sorry) and we'll investigate.

Other problems? See: [Troubleshooting](Troubleshooting)