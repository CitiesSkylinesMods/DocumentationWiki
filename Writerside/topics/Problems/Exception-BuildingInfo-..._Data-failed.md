# Exception BuildingInfo ..._Data failed

Will finish this later but just jotting down some notes for now so I don't forget...

If you see stuff like this, usually a road asset, or asset containing a road asset, it's due to missing DLC such as Mass
Transit, Industries or After Dark.

```
Custom Assets: 1908620939.Hwy3-4-2-2_On-Ramp_Data: NetInfo missing
at (wrapper dynamic-method) BuildingInfo.InitializePrefab_Patch1 (object) <0x02b10>
at PrefabCollection`1<BuildingInfo>.InitializePrefabImpl (string,BuildingInfo,string) <0x00298>
  [Core]
 
(Filename: C:/buildslave/unity/build/artifacts/generated/common/runtime/DebugBindings.gen.cpp Line: 51)

[LSM] Asset failed: 1908620939.Hwy3-4-2-2_On-Ramp_Data
Exception: BuildingInfo 1908620939.Hwy3-4-2-2_On-Ramp_Data failed
  at LoadingScreenMod.AssetLoader.Initialize[BuildingInfo] (.BuildingInfo info) [0x00000] in <filename unknown>:0 
  at LoadingScreenMod.AssetLoader.LoadImpl (ColossalFramework.Packaging.Asset assetRef) [0x00000] in <filename unknown>:0 
  at LoadingScreenMod.AssetLoader+<LoadCustomContent>d__27.MoveNext () [0x00000] in <filename unknown>:0 
UnityEngine.DebugLogHandler:Internal_LogException(Exception, Object)
UnityEngine.DebugLogHandler:LogException(Exception, Object)
UnityEngine.Logger:LogException(Exception, Object)
UnityEngine.Debug:LogException(Exception)
LoadingScreenMod.AssetLoader:AssetFailed(Asset, Package, Exception)
LoadingScreenMod.<LoadCustomContent>d__27:MoveNext()
LoadingManager:Update()
```