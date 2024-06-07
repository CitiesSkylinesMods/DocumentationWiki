> Article verified: February 2020

> This is one cause of the [Simulation error Array index is out of range](Simulation error Array index is out of range) error.

## Symptom

You will see this error:

* `Simulation error: Array index is out of range.`

In the [**log file**](./Share-your-Cities-Skylines-log-file), you'll see one of the following below the error:

* `at PassengerTrainAI.SimulationStep ...`
* or `at PassengerTrainAI.StartPathFind ...`
* or something similar starting with `at PassengerTrainAI`
* or `at MetroOverhaul.Detours.PassengerTrainAIDetour.StartPathFind`

## Cause

This appears to be caused by the [Metro Overhaul Mod](https://steamcommunity.com/sharedfiles/filedetails/?id=816260433).

> WARNING: Don't just unsubscribe MOM; go through procedure in the Solution section first.

It appears that MOM is not correctly handling deletion of metro assets or routes (we don't know enough about MOM to say for sure). For background information, see [Issue #82](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues/82), also see [Steam discussion](https://steamcommunity.com/app/255710/discussions/0/1750147885670168992/).

> Your log file might also include something like this:
>  
> * `  at TrafficManager.Custom.AI.CustomTrainAI.CustomSimulationStep`
>  
> While `TrafficManager` is mentioned in the extended error message, it's not the cause of the error, just affected by it.

## Solution

> Do NOT just unsubscribe MOM, as that will cause loads of other errors. The bullet points below suggest a way to recover from the error without unsubscribing. However, if you want to unsubscribe MOM, do it properly - see: [How to remove workshop networks](How to remove workshop networks). Note that unsubscribing probably won't fix the error.

First, try this:

* Subscribe and enable [Loading Screen Mod](https://steamcommunity.com/sharedfiles/filedetails/?id=667342976) (LSM)
* In LSM mod options, enable the [Safe Mode](https://steamcommunity.com/workshop/filedetails/discussion/667342976/1626286205707786286/) settings
* Load your save
* If it works, save **under new name**, exit game to desktop, then relaunch and it should be fine after that (until MOM breaks again)

If that doesn't work, however:

* Enable **Ghost Mode** in MOM mod options
* Load the save that has the problem
    * All MOM stuff will be disabled due to Ghost Mode
* Save the game **under new name**
* Exit to desktop
* Re-launch the game and load the newly created save

If that doesn't work:

* Exit to desktop
* Launch Cities: Skylines again
* Load a savegame that was created _before_ you encountered the error

If it still doesn't work, you'll have to ask the developers of MOM mod for help.

## Fixed?

If not, see other causes of [Simulation error Array index is out of range](Simulation error Array index is out of range).

Other issues? See: [Troubleshooting](Troubleshooting)