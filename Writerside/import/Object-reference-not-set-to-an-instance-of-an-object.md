> Verified: April 2020
>  
> Note: **Loading Screen Mod** "Safe Mode" options can sometimes recover from the error - see bottom of this page for details.

## Symptoms

You see an error on-screen like the following:

* `Object reference not set to an instance of an object [System.NullReferenceException]`

Or, you might see either on-screen or in your log file an error like:

* `Simulation error: Object reference not set to an instance of an object`

Or:

* `NullReferenceException: Object reference not set to an instance of an object`

## Cause

Currently, TM:PE is not reported to cause this error.

This is caused when a mod tries to access a game object (usually) that no longer exists. It's very common error, but we'll try and document some solutions to known causes below...

## Solutions

First:

* Open the **[log file](./Share-your-Cities-Skylines-log-file)** in notepad or some other [Text Editors](Text Editors)
* Search for `Object reference not set`

What we're interested in is the stuff that appears on the next few lines after the error message. That stuff will _usually_ be several lines starting with `  at`. Look for any of the following strings in that text: 

* `AssetIcons.IconModifier.PatchIcons`:
    * Caused by game-breaking [Improved Asset Icons](https://steamcommunity.com/sharedfiles/filedetails/?id=508195208) or [Improved Asset Icons (alternative)](https://steamcommunity.com/sharedfiles/filedetails/?id=747836519) mod - completely unsubscribe it/them.
    * Related error: [FormatException Invalid Image Format](FormatException Invalid Image Format)
    * A good alternative is the reliable [Find It](https://steamcommunity.com/sharedfiles/filedetails/?id=837734529) mod.
* `Building.PlayAudio`, or
* `Building.CalculateGroupData`:
    * Caused by game-breaking [Control Building Level Up 0.4](https://steamcommunity.com/sharedfiles/filedetails/?id=410535198) mod - completely unsubscribe the mod
    * Check if there is a `RoadBaseAI.CanEnableTrafficLights` error in your log file; if so the [Safenets](https://steamcommunity.com/sharedfiles/filedetails/?id=1620588636) mod might fix both errors.
* `PloppableRICO`, or
* `ToolBase.OnEnable`, or
* `BuildingAI.CheckUnlocking`, or
* `RealTime.Simulation.Statistics`...:
    * [Usually caused](https://steamcommunity.com/app/255710/discussions/0/1639789306556401437/?ctp=4) by the [Ploppable RICO mod](https://steamcommunity.com/sharedfiles/filedetails/?id=586012417) or building assets that have Ploppable RICO definitions.
    * See: [Ploppable RICO errors](Ploppable RICO errors) for how to fix
    * Make sure you don't have game-breaking **Building Anarchy** mod as that can cause similar errors.
* `IINS.PROPFINETUNING.PropFineTuner.Done`:
    * Unsubscribe [Prop Fine Tune](https://steamcommunity.com/sharedfiles/filedetails/?id=685747254)
    * You could use keyboard shortcuts in [Move It!](https://steamcommunity.com/sharedfiles/filedetails/?id=1619685021) mod options to get similar functionality ;)
* `MaZy.AutobulldozeMod`:
    * Unsubscribe [Automatic Bulldoze Simple Edition](https://steamcommunity.com/sharedfiles/filedetails/?id=1393966192)
    * A better alternative is [Bulldoze It!](https://steamcommunity.com/sharedfiles/filedetails/?id=1627986403)
* `RoadBaseAI.CanEnableTrafficLights`:
    * This error happens when your save (or a building you have subscribed) contains a road, rail or other transport asset that is not avaialble
        * Sometimes triggers side-effects, eg. `Building.PlayAudio` or `Building.CalculateGroupData` errors
    * Can often be fixed with [Safenets](https://steamcommunity.com/sharedfiles/filedetails/?id=1620588636) mod
        * See also [How to remove workshop networks](How to remove workshop networks)
    * More info and fixes: [Simulation error Object reference not set](Simulation error Object reference not set)
* `WaterSimulation.ReleaseWaterWave`:
    * Possibly caused by [Ragnarok](https://steamcommunity.com/sharedfiles/filedetails/?id=811352708), [Natural Disasters Overhaul](https://steamcommunity.com/sharedfiles/filedetails/?id=1801953480) or some other mod that alters natural disasters (particularly the tsunami "tidal wave").
    * Solution: Launch a meteorite in to the water where the Tsunami was happening. This has to be the best bug fix ever found. Thanks to steam user Darky for the tip!
* `Rainfall.Hydraulics.updateDistrictAndDrainageGroup`:
    * Caused by [Rainfall](https://steamcommunity.com/sharedfiles/filedetails/?id=698395457) mod, most likely due to missing [required assets](https://steamcommunity.com/workshop/filedetails/?id=698408622).
    * Could be due to conflicts between Rainfall and other mods (namely any that affect water, weather or disasters).
* `ColossalFramework.UI.UIComponent.RebuildComponentOrder`:
    * If the stack trace in log mentions `at NetPicker`, it's the [Net Picker](https://steamcommunity.com/sharedfiles/filedetails/?id=1612012531) mod
* `VehicleEffects.VehicleEffectsMod`:
    * If the error mentions `OnLevelUnloading` some other mod broke the loading process; not vehicle effects.
    * Otherwise, it's issue with [Vehicle Effects](https://steamcommunity.com/sharedfiles/filedetails/?id=780720853) or [Extra Vehicle Effects](https://steamcommunity.com/sharedfiles/filedetails/?id=815103125) mod(s) trying to apply effects to a vehicle that does not exist. Solution: Remove any unnecessary effects mods (eg. train sound effects or whatever) or find and resubscribe the missing asset. For vanilla or DLC vehicles, check they aren't in `skip.txt` of Loading Screen Mod.
* `VanillaGarbageBinBlocker.PropManagerDataPatch.Prefix`:
    * This error occurs if you have [Garbage Bin Controller](https://steamcommunity.com/sharedfiles/filedetails/?id=1386697922) mod, but you skipped the `Garbage Bin` prefab with Loading Screen Mod's `skip.txt` file. Solution: Don't skip `Garbage Bin`.
* `NetTool.TestNodeBuilding`:
    * Possibly a network mod by Elektrix?
* `RadioPanel.AssignStationToButton`, or
* `TreeInstance.PopulateGroupData`:
    * Seems to be caused by Nursing Homes for Senior Citizens mod
* `VehicleManager.SimulationStepImpl`:
    * The save game was created with More Vehicles mod active, which increase vehicle limts.
    * If More Vehicles mod is later disabled or removed, the save will break
    * To fix: Re-enable More Vehicles mod.

> There are reports that **Service Vehicles Manager** also causes object reference errors, although we haven't seen a log file to confirm.

## Ploppabe RICO

I've moved this to its own guide: [Ploppable RICO errors](Ploppable RICO errors)

## Loading Screen Mod: Safe Mode

Sometimes the errors can be fixed using the "Safe Mode" options in Loading Screen Mod:

1. Exit game to desktop
2. Subscribe and enable [Loading Screen Mod](https://steamcommunity.com/sharedfiles/filedetails/?id=667342976) (LSM)
3. In it's mod options:
    * Enable the optimisation/sharing options to reduce RAM use (will make games load faster)
    * Enable the safe mode options
4. Now load your save - LSM will do everything it can to beat those errors

Sometimes it just won't solve the problem, or it will only save it once but then the error comes back on subsequent loads. If that's the case, it's almost certainly a broken asset, missing asset or broken mod.

## Old causes of error

All these should now be fixed, but just keeping here for reference:

* ~~`TransportStationAI.IsIntercity`:~~
    * ~~Bug in vanilla game due to Sunset Harbor update~~ FIXED in 1.13.0-f8!
    * Old buildings, that were created before "sub buildings" feature was added to game (mostly those made before 29th November 2016) have a `null` value for their sub buildings property.
    * You can fix all those buildings with the [IsIntercity Fix](https://steamcommunity.com/sharedfiles/filedetails/?id=2037862156) mod :)

## Fixed?

If not:

* If you think it's TM:PE that causes the error, please let us know: [Report a bug](Report a bug) (we're crazy busy so it may take a while for us to investigate)
* You could check for broken assets - see: [Finding Broken and Bloated Assets](https://steamcommunity.com/sharedfiles/filedetails/?id=1846793796)
* Seek help in [Steam discussion forums](https://steamcommunity.com/app/255710/discussions/) or [Cities Skylines Discord Server](https://discordapp.com/channels/263634513861541888/513313798875119657). Remember to [share your log file](./Share-your-Cities-Skylines-log-file)!

Other issues? See: [Troubleshooting](Troubleshooting)