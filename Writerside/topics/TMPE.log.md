# TMPE.log

> > Verified: January 2022 — TM:PE 11.5.2 / TM:PE 11.6.2

## Overview

The `TMPE.log` is an additional log file that's created when TM:PE is active.

The contents of the log are usually mundane, just lists of the routine tasks TM:PE performs when starting up and
shutting down. However, sometimes it will contain additional information about errors, particularly mod conflicts, that
won't be listed in the [main game log file](Share-your-Cities-Skylines-log-file.md).

## File location

**On Windows:**

> `<SteamFolder>\SteamApps\common\Cities_Skylines\Cities_Data\TMPE.log`

Note: The `<SteamFolder>` is usually found at `C:\Program Files (x86)\Steam`.

**On Mac:**

Navigate to:

> `Users/username/Library/Application Support/Steam/steamapps/common/Cities_Skylines`

Then right-click `Cities` and choose **Show Package Options** (Yosemite users: Choose **Open in new tab** instead, then
click on the new tab), then you can find the log file in:

> `Contents/TMPE.log`

**On Linux:**

> `~/.local/share/Steam/steamapps/common/Cities_Skylines/Cities_Data/TMPE.log`

**Custom log file location:**

> Note: Only tested on Windows, might not work on Linux/Mac?

As of TM:PE 11.6.2 we check for the `-LogFile` command line parameter. If specified, `TMPE.log` will be placed in the
specified folder. For details see [PR #1151](https://github.com/CitiesSkylinesMods/TMPE/pull/1151).

## Sharing

See: [Sharing your log](Share-your-Cities-Skylines-log-file.md#sharing-your-log-file)

## Identifying mod conflicts

If another mod conflicts with TM:PE, details will appear in the `TMPE.log`. You'll see something like this:

```
[Info] @ 2322974790 ThreadingExtension.OnBeforeSimulationFrame: First frame detected. Detours checked. Result: 2 missing detours
[Error] @ 2322980450 Traffic Manager: President Edition detected an incompatibility with another mod! You can continue playing but it's NOT recommended. Traffic Manager will not work as expected. See TMPE.log for technical details.
   at CSUtil.Commons.Log.LogToFile(System.String log, LogLevel level)
   at CSUtil.Commons.Log.Error(System.String s)
   at TrafficManager.ThreadingExtension.OnBeforeSimulationFrame()
   at ThreadingWrapper.OnBeforeSimulationFrame()
   at SimulationManager.SimulationStep()
   at SimulationManager.SimulationThread()

[Info] @ 2322991320 The following methods were overriden by another mod:
	ResidentAI.GetVehicleInfo with 4 parameters (ResidentAI, Assembly-CSharp, Version=0.0.0.0, Culture=neutral, PublicKeyToken=null)
	TouristAI.GetVehicleInfo with 4 parameters (TouristAI, Assembly-CSharp, Version=0.0.0.0, Culture=neutral, PublicKeyToken=null)
```

In the example above, another mod has altered the `ResidentAI.GetVehicleInfo` and `TouristAI.GetVehicleInfo` methods in
such a way that TM:PE wasn't able to apply its own alterations to those methods.

We also highly recommend using
the [Compatibility Report](https://steamcommunity.com/sharedfiles/filedetails/?id=2633433869) mod which scans all your
mods and identifies any that are outdated/incompatible.