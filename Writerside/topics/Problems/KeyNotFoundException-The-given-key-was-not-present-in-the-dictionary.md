# KeyNotFoundException The given key was not present in the dictionary

> Article verified: August 2019

## Symptom

> Note: This error occurs when exiting the game, so you can safely choose to ignore it if desired.

You see an error on-screen or in the log file like this:

* `KeyNotFoundException: The given key was not present in the dictionary.`

## Cause

This error is _not_ caused by TM:PE.

It's caused by mods that do not properly maintain their Harmony patch/redirect state.

> **Update (August 2019):**  
> Adding NExt 2 or MOM 9 (not sure which yet) seems to trigger this error, especially on lots of the "\<verb> It!" mods.
> So, if you're seeing multiple mods reporting the `KeyNotFoundException` try disabling NExt/MOM (
> see: [](How-to-remove-workshop-networks.md)) and see if that helps.

## Solution

In the [log file](Share-your-Cities-Skylines-log-file.md), see if you recognize any mod names, for example (we've
highlighted the lines in red):

```
  KeyNotFoundException: The given key was not present in the dictionary.
    at System.Collections.Generic.Dictionary`2[System.String,System.Reflection.Emit.LocalBuilder].get_Item (System.String key) [0x00000] in <filename unknown>:0 
    at Harmony.MethodPatcher.EmitCallParameter (System.Reflection.Emit.ILGenerator il, System.Reflection.MethodBase original, System.Reflection.MethodInfo patch, System.Collections.Generic.Dictionary`2 variables, Boolean allowFirsParamPassthrough) [0x00000] in <filename unknown>:0 
    at Harmony.MethodPatcher+<>c__DisplayClass20_0.<AddPostfixes>b__1 (System.Reflection.MethodInfo fix) [0x00000] in <filename unknown>:0 
    at Harmony.CollectionExtensions.Do[MethodInfo] (IEnumerable`1 sequence, System.Action`1 action) [0x00000] in <filename unknown>:0 
    at Harmony.MethodPatcher.AddPostfixes (System.Reflection.Emit.ILGenerator il, System.Reflection.MethodBase original, System.Collections.Generic.List`1 postfixes, System.Collections.Generic.Dictionary`2 variables, Boolean passthroughPatches) [0x00000] in <filename unknown>:0 
    at Harmony.MethodPatcher.CreatePatchedMethod (System.Reflection.MethodBase original, System.String harmonyInstanceID, System.Collections.Generic.List`1 prefixes, System.Collections.Generic.List`1 postfixes, System.Collections.Generic.List`1 transpilers) [0x00000] in <filename unknown>:0 
-  Rethrow as Exception: Exception from HarmonyInstance "com.klyte.commons.ElectricRoadsOverrides"
    at Harmony.MethodPatcher.CreatePatchedMethod (System.Reflection.MethodBase original, System.String harmonyInstanceID, System.Collections.Generic.List`1 prefixes, System.Collections.Generic.List`1 postfixes, System.Collections.Generic.List`1 transpilers) [0x00000] in <filename unknown>:0 
    at Harmony.PatchFunctions.UpdateWrapper (System.Reflection.MethodBase original, Harmony.PatchInfo patchInfo, System.String instanceID) [0x00000] in <filename unknown>:0 
    at Harmony.PatchProcessor.Unpatch (System.Reflection.MethodInfo patch) [0x00000] in <filename unknown>:0 
    at Harmony.HarmonyInstance.Unpatch (System.Reflection.MethodBase original, System.Reflection.MethodInfo patch) [0x00000] in <filename unknown>:0 
    at Harmony.HarmonyInstance+<>c__DisplayClass11_1.<UnpatchAll>b__1 (Harmony.Patch patchInfo) [0x00000] in <filename unknown>:0 
    at Harmony.CollectionExtensions.Do[Patch] (IEnumerable`1 sequence, System.Action`1 action) [0x00000] in <filename unknown>:0 
    at Harmony.CollectionExtensions.DoIf[Patch] (IEnumerable`1 sequence, System.Func`2 condition, System.Action`1 action) [0x00000] in <filename unknown>:0 
    at Harmony.HarmonyInstance.UnpatchAll (System.String harmonyID) [0x00000] in <filename unknown>:0 
-   at Klyte.ElectricRoads.Overrides.Redirector`1[T].OnDestroy () [0x00000] in <filename unknown>:0 
```

In the stack trace above you can see some details of the mod that caused it: `ElectricRoads`

Note that the mod name could appear anywhere in the stack trace, but it's usually around the middle or end.

Important:

* If **only one mod is affected**, it's highly likely that is the source of the problem.
* However, if **multiple mods are affected**, the root cause is likely a different mod.

If the issue is affecting multiple mods, search your log file for the first occurrence of `0Harmony.dll`, you'll see
something like this (note: this is just random example and not indicative of a broken mod):

```
Loading ...\steamapps\workshop\content\255710\1192503086\0Harmony.dll  [Mods - Internal]
```

Remember that second long number, we might need it later to identify the mod.

A few lines below, you should see something like this:

```
  Non platform assembly: data-000000001FFD0770 (this message is harmless)
  Fallback handler could not load library E:/Steam Lib/steamapps/common/Cities_Skylines/Cities_Data/Mono/data-000000001FFD0770.dll
+ Assembly 0Harmony, Version=1.2.0.1, Culture=neutral, PublicKeyToken=null loaded.  [Mods - Internal]
```

If you see `Version` of `1.2.0.1` or above, it's probably not the cause of the problem (version `1.2.0.1` is what most
mods use currently).

If it's a lower number, then it is likely the cause of the problem, so now we need to work out which mod is
loading `0Harmony.dll`. To do that, use that long number we from earlier to construct a Steam Workshop URL like this:

```
https://steamcommunity.com/sharedfiles/filedetails/?id=1192503086
```

That will show you which mod is loading the Harmony library. Note that the mod used in this example is likely not the
cause of the problem, we're just using it to illustrate how to determine which mod loads Harmony library.

Anyway, once you've identified which mod is causing it:

* Completely unsubscribe the mod
* Exit to desktop to flush the mod code from RAM
* Let the mod author know about the error and hopefully they will fix it

## Was it Fixed?

If not, and you believe the issue is caused by TM:PE, please let us know: [](Report-a-Bug.md)

Other issues? See: [](Troubleshooting.md)