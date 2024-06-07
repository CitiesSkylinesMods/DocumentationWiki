> Article verified: January 2020

> This is one cause of the [Simulation error Array index is out of range](Simulation error Array index is out of range) error.

## Symptom

You will see this error on screen or in log file:

* `Simulation error: Array index is out of range.`

In the [**log file**](./Share-your-Cities-Skylines-log-file), find that error and beneath it you should see:

* `at WaterSimulation.LockWaterSource ...`

## Cause

Known causes of this error:

* [Immersive Water](https://steamcommunity.com/sharedfiles/filedetails/?id=1115699323)
    * The log file will probably contain: `at WaterFacilityAI.HandleWaterSource ...`
* [Climate Control](https://steamcommunity.com/sharedfiles/filedetails/?id=629713122) conflicts with IPT2
    * The log file might contain: `at ImprovedPublicTransport2.Detour.VehicleManagerMod.ReleaseWaterSource ...`
    * For background information, see [this topic](https://steamcommunity.com/app/255710/discussions/0/1649919326320915422/) or [this topic](https://steamcommunity.com/app/255710/discussions/0/1643166649094694336/).
* [More Vehicles](https://steamcommunity.com/sharedfiles/filedetails/?id=1764208250) conflicts with IPT2
    * The log file might contain: `at ImprovedPublicTransport2.Detour.VehicleManagerMod.ReleaseWaterSource ...`
    * For background information, see [Issue #450](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues/450)

> Note: Your log file might also include something like this:
>  
> * `  at TrafficManager.Custom.AI.CustomCommonBuildingAI.CustomSimulationStep ...`
>  
> While `TrafficManager` is mentioned in the extended error message, it's not the cause of the error, just affected by it. 

## Solution

If you were using **Immersive Water** mod:

* Unsubscribe Immersive Water mod
* Exit to desktop, then relaunch the game

If you were using **Climate Control** mod:

* Unsubscribe Climate Control mod
* Exit to desktop, then relaunch the game

If you were using **More Vehicles** mod:

* The save will not work without More Vehicles mod as it has already changed to the new vehicle limit
* You'll have to unsubscribe IPT2 and any other mods that can't handle larger vehicle limit
* I'm not currently aware of any way to revert back to the vanilla vehicle limit (although you could try LSM Safe Mode described below)

If problems persist, try using LSM Safe Mode options :

* Subscribe and enable [Loading Screen Mod](https://steamcommunity.com/sharedfiles/filedetails/?id=667342976) (LSM)
* In LSM mod options, enable the "Safe Mode" options then load your save game
    * This tries to avoid and ignore errors, and will also try clearing lists of vehicles and cims, fix broken roads, etc.
* If it works, save the game under a new file name, then exit to desktop - next time you load it up it should work fine

## Fixed?

If not, see other causes of [Simulation error Array index is out of range](Simulation error Array index is out of range).

Other issues? See: [Troubleshooting](Troubleshooting)