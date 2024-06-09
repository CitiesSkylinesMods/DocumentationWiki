# Simulation error Array index is out of range

> Verified: January 2022 - TM:PE 11.5.2 / TM:PE 11.6
>
> **Notes:**
> * If the error is `IndexOutOfRangeException: Array index is out of range`, it might be caused
    by [](Broken-Road-Assets.md) (see that link for solutions).
> * All versions of Loading Screen Mod
    include [Safe Mode options](https://steamcommunity.com/workshop/filedetails/discussion/667342976/1626286205707786286/)
    that can _sometimes_ help recover from the "Array index" errors. See **Loading Screen Mod** section at bottom of
    this guide for details.

## Symptom

You will see this error on-screen - either while a saved game is loading, or in-game:

* `Simulation error: Array index is out of range.`

There are several variants, each caused by a different mod or sometimes broken workshop asset. You can determine which
one you have by searching for the above error message in your [**log file**](Share-your-Cities-Skylines-log-file.md) and
then checking what is on the next line...

## Cause / Solution

> There are so many different causes of the error that we created separate pages for most of them;
> click `Array Index - Symptom x` links, where available, for solutions to that specific error.

### Array Index - Symptom 1

* `at WG_PopOnly.CommercialBuildingAIMod ...`
* or something similar starting with `at WG_`
* ~~Symptom 1 has been fixed! Make sure you are using latest version
  of [WG Configurable Population Modifiers](https://steamcommunity.com/sharedfiles/filedetails/?id=652921941) mod.~~
* Update November 2021: Use
  the [Realistic Population Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2025147082&searchtext=realistic+population+revived)
  mod instead.

### Symptom 2

See [](Array-Index---Symptom-2.md)

* `at PassengerTrainAI.SimulationStep ...`
* or `at PassengerTrainAI.StartPathFind ...`
* or something similar starting with `at PassengerTrainAI`
* or `at MetroOverhaul.Detours.PassengerTrainAIDetour.StartPathFind`

### Symptom 3

See [](Array-Index---Symptom-3.md)

* `at TransportLine.GetNextStop ...`
* followed by `at BusAI.ArriveAtTarget ...`

### Symptom 4

See [](Array-Index---Symptom-4.md)

* `at WaterSimulation.LockWaterSource ...`
* `at ImprovedPublicTransport2.Detour.VehicleManagerMod.ReleaseWaterSource ...`

### Symptom 5

See [](Array-Index---Symptom-5.md)

* `at BuildingThemes.Detour.ZoneBlockDetour ...`

### Symptom 6

See [](Array-Index---Symptom-6.md)

* `at BuildingAI.EnsureCitizenUnits ...`

### Symptom 7

See [](Array-Index---Symptom-7.md)

* `at CargoInfoMod.CargoData.Count ...`

### Symptom 8

See [](Array-Index---Symptom-8.md)

* `at UnlockManager.Unlocked ...`

### Symptom 9

See [](Array-Index---Symptom-9.md)

* `Node is not connected to segment`
* `Warning #: ExtSegmentEndManager.GetIndex(#, #): Node is not connected to segment.`

### Symptom 10

See [](Array-Index---Symptom-10.md)

* `at TerrainModify.ApplyQuad ...`
* `at TerrainModify.UpdateAreaImplementation ...`

### Symptom 11

See [](Array-Index---Symptom-11.md)

* `at TerrainManager.GetSurfaceCell ...`
* `Parameter name: index` followed by `at System.Collections.Generic.List ...`

### Symptom 12

See [](Array-Index---Symptom-12.md)

* `at GeneratedScrollPanel.IntializeUIAssetFilters`

### Symptom 13

See [](Array-Index---Symptom-13.md)

* `at TransportLineAI.CheckNodePosition`

### Symptom 14

See [](Array-Index---Symptom-14.md)

* `at EPTUI2.UITransportLineRow.Update`

### Array Index - Symptom 15

* `at TransportLine.GetNextStop`
* [#867](https://github.com/CitiesSkylinesMods/TMPE/issues/867): If the stack trace mentions aircraft or helicopters or
  blimps, it's likely due to building an airport/helipad/depot outside the central 25 tile area.

### Array Index - Symptom 16

* `NetManager+Data.Deserialize`
* [#1195](https://github.com/CitiesSkylinesMods/TMPE/issues/1195): Likely caused by outdated mods or broken road assets.
* Use LSM "Safe Mode" (detailed further down this page) which can sometimes recover a broken save.
* Use [Compatibility Report](https://steamcommunity.com/sharedfiles/filedetails/?id=2633433869) mod which can help track
  down broken mods and suggest better alternatives.

## General Solutions

There are some other things you can try...

### Checking for broken mods and assets

Use [Compatibility Report](https://steamcommunity.com/sharedfiles/filedetails/?id=2633433869) mod from Steam Workshop -
it can help track down broken mods and suggest better alternatives.

Also, check the Steam Guide
on [Finding Broken and Bloated Workshop Subscriptions](https://steamcommunity.com/sharedfiles/filedetails/?id=1846793796)
which can help track down other broken mods and assets.

### Loading Screen Mod: Safe Mode

Some array index errors can be fixed using the "Safe Mode" options in Loading Screen Mod:

1. Exit game to desktop
2. Subscribe and enable [Loading Screen Mod](https://steamcommunity.com/sharedfiles/filedetails/?id=667342976) (LSM)
3. In its mod options:
    * Enable the optimization/sharing options to reduce RAM use (will make games load faster)
    * Enable the safe mode options
4. Now load your save - LSM will do everything it can to beat those errors

In some cases it might only work once, but the error will come back on the next load. If that happens, you'll have to
try and track down what specifically is causing the error and fix it at source.

## Was it Fixed?

* Please post details of your error on the workshop page of the mod or asset causing the problem
* You can often get help on the
  official [Cities: Skylines Discord server](https://discordapp.com/channels/263634513861541888/513313798875119657).
* If you use **More Vehicles mod** please note that lots of other mods aren't compatible as they generally hard-code the
  vehicle limit. The "Compatibility Report" mod will often tell you if that is the case.
    * TM:PE versions 10.21.1, 11.0 and later are all compatible with More Vehicles.
* If you think it's caused by TM:PE, please [](Report-a-Bug.md) (TM:PE users only, please - we can't help debug other
  mods, sorry) and we'll investigate.

Other problems? See: [](Troubleshooting.md)