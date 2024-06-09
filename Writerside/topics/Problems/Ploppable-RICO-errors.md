# Ploppable RICO errors

> Verified: January 2022 - TM:PE v11.5.2 / TM:PE 11.6

## Update

**There is now a new _bug fixed_ and improved version of the Ploppable RICO
mod: [RICO revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2016920607)**.

Please try that first as it resolves most Ploppable RICO errors and has many other significant improvements over the
older mod!

## Symptom

On-screen or in the log file, you'll see errors like one of the following:

* `Object reference not set to an instance of an object [System.NullReferenceException]`
* `Simulation error: Object reference not set to an instance of an object`
* `NullReferenceException: Object reference not set to an instance of an object`

In the log file, where full error details are shown, look for _**one or more**_ of these errors in the stack traces:

* `at BuildingAI.CheckUnlocking ....`
* `at PloppableRICO ....`
* `at ToolBase.OnEnable ....`
* `PloppableRICO.PloppableTool ....`
* `at RealTime.Simulation.Statistics ....`

If you see _any_ of those, then the issue is caused by Ploppable RICO assets/configurations.

If you don't see them, then it will be some other cause - see: [](Object-reference-not-set-to-an-instance-of-an-object.md)

## Cause

There are two variants as follows:

1. The error is usually caused by Ploppable RICO assets that are missing some required item - usually a prop or a road.
   Note that the asset will work fine for any users that have all the props/roads/etc required for the asset.
2. It can sometimes be caused by incorrectly configured RICO settings for an asset, usually a missing construction cost,
   which can trigger errors in mods such as Real Time (you'll likely see `RealTime.Simulation.Statistics` in the error
   logs).

## Solution

To find the breaking assets, look for errors like those shown below (ignore the `+` and `-` below, I'm just using them
to highlight relevant lines):

Variant 1:

> ```
> + InitPrefab Failed920507824.Barn 04 - RICO_Data
>  
> (Filename: C:/buildslave/unity/build/artifacts/generated/common/runtime/DebugBindings.gen.cpp Line: 51)
> 
> - NullReferenceException: Object reference not set to an instance of an object
>   at ToolBase.OnEnable () [0x00000] in <filename unknown>:0 
> UnityEngine.GameObject:Internal_AddComponentWithType(Type)
> UnityEngine.GameObject:AddComponent(Type)
> UnityEngine.GameObject:AddComponent()
> PloppableRICO.PloppableTool:Initialize()
> PloppableRICO.Loading:OnLevelLoaded(LoadMode)
> LoadingWrapper:OnLevelLoaded(UpdateMode)
> <LoadLevelComplete>c__Iterator9:MoveNext()
> LoadingManager:Update()
> ```
>
> We want the line that starts with **`InitPrefab Failed`**, for example:
>
> `InitPrefab Failed920507824.Barn 04 - RICO_Data`

Variant 2:

> ```
> + 897729711.Savelovskiy_City_Davis_Data Button Destroyed
>  
> (Filename: C:/buildslave/unity/build/artifacts/generated/common/runtime/DebugBindings.gen.cpp Line: 51)
> 
> - NullReferenceException: Object reference not set to an instance of an object
> - at PloppableRICO.PloppableCommercial.GetConstructionCost () [0x00000] in <filename unknown>:0 
>   at BuildingAI.GetLocalizedTooltip () [0x00000] in <filename unknown>:0 
>   at PrefabInfo.GetLocalizedTooltip () [0x00000] in <filename unknown>:0 
>   at PloppableRICO.PloppableTool.DrawBuildingButton (.BuildingInfo BuildingPrefab, System.String type) [0x00000] in <filename unknown>:0 
> UnityEngine.DebugLogHandler:Internal_LogException(Exception, Object)
> UnityEngine.DebugLogHandler:LogException(Exception, Object)
> UnityEngine.Logger:LogException(Exception, Object)
> UnityEngine.Debug:LogException(Exception)
> PloppableRICO.PloppableTool:DrawBuildingButton(BuildingInfo, String)
> PloppableRICO.PloppableTool:PopulateAssets()
> PloppableRICO.PloppableTool:Initialize()
> PloppableRICO.Loading:OnLevelLoaded(LoadMode)
> LoadingWrapper:OnLevelLoaded(UpdateMode)
> <LoadLevelComplete>c__Iterator9:MoveNext()
> LoadingManager:Update()
> ```
>
> We want the line that starts with a long number followed by **`.`**, for example:
>
> `897729711.Savelovskiy_City_Davis_Data Button Destroyed`

So, as you can see, in both variants of the error, there's an asset mentioned a few lines before. We want the long
number so we can construct a URL to the workshop page.

The base URL is: `https://steamcommunity.com/sharedfiles/filedetails/?id=`

The long number should be added to the end of that base URL.

Using the assets mentioned in the examples above, the URLs would be:

* `InitPrefab Failed920507824.Barn 04 - RICO_Data` becomes:
  > https://steamcommunity.com/sharedfiles/filedetails/?id=920507824
* `897729711.Savelovskiy_City_Davis_Data Button Destroyed` becomes:
  > https://steamcommunity.com/sharedfiles/filedetails/?id=897729711

The put the link in your browser, and you'll find the broken asset. Unsubscribe it and it should fix the problem.

Note that for **Variant 2** you might be able to fix the asset if you created a local RICO setting for it:

* Look for the `LocalRICOSettings.xml` file, it's usually
  in `C:\Program Files (x86)\Steam\steamapps\common\Cities_Skylines`
* You can delete it, which will get rid of all local RICO settings (should fix the errors)
* Or you can edit it to fix the values:
    * Edit in a text editor (see [](Text-Editors.md) for a list of compatible text editors)
    * Look for `construction-cost=""` or `construction-cost="0"`...
    * Change it to any positive number, for example `construction-cost="10"`
    * Save the file
* In either case, exit the game to desktop after making changes, then reload and see if it's fixed.

## Was it Fixed?

If not, it's likely a different cause of the error, see: [](Object-reference-not-set-to-an-instance-of-an-object.md)

Other issues? See: [](Troubleshooting.md)