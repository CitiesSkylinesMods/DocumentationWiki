# System.Reflection.TargetInvocationException TMPE.log is denied

> Article verified: February 2022 - TM:PE 11.6.5.7

> Note to TM:PE team: Check the folder path for stuff like `DODI-Repacks` which indicates pirated copy of the game.

## Symptom

This issue is most common on Windows for users who have tried moving the game to a different drive:

* A `System.Exception` error is shown in the game (or sometimes a `System.IO.IOException` error)
* On inspecting [your log file](Share-your-Cities-Skylines-log-file.md), you find something
  mentioning `TMPE.log is denied`

Example log messages (folder path truncated for sake of brevity):

```
System.Reflection.TargetInvocationException: Exception has been thrown by the target of an invocation. --->
System.TypeInitializationException: An exception was thrown by the type initializer for TrafficManager.State.GlobalConfig --->
System.UnauthorizedAccessException: Access to the path "...\Steam\steamapps\common\Cities_Skylines\Cities_Data\TMPE.log" is denied.
```

or:

```
System.Reflection.TargetInvocationException: Exception has been thrown by the target of an invocation. --->
System.UnauthorizedAccessException: Access to the path "...\Steam\steamapps\common\Cities_Skylines\Cities_Data\TMPE.log" is denied.
```

In rare cases you might get a `System.IO.IOException` with a log file showing things like:

```
System.IO.IOException: Sharing violation on path D:\SteamLibrary\steamapps\common\Cities_Skylines\Cities_Data\TMPE.log
at System.IO.FileStream..ctor (System.String path, FileMode mode, FileAccess access, FileShare share, Int32 bufferSize, Boolean anonymous, FileOptions options) [0x00000] in <filename unknown>:0 
```

## Cause & Solution

For all error messages above (including `System.Reflection...`), please see: [](System.IO.IOException.md)