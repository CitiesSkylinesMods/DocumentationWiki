# System.IO.IOException Win32 IO returned 112

## Symptom

You might see an error on-screen like:

```
The Mod (steam path) [CSUtil.CameraControl.dll, CSUtil.Commons.dll, TMPE.GenericGameBridge.dll,
TMPE.CitiesGameBridge.dll, TrafficManager.dll] has caused an error [ModException]
```

Or in the log file you might seen an error mentioning [[TMPE.log]] similar to this:

```
System.IO.IOException: Win32 IO returned 112. Path: ...\TMPE.log
  at System.IO.FileStream.FlushBuffer ...
```

## Cause

Your disk is full.

> Note: In rare cases it can be a variant of [[System.Reflection.TargetInvocationException TMPE.log is denined]]

## Solution

Free up space on the disk where [[TMPE.log]] is stored.

The log file doesn't need much space, but Cities: Skylines certainly does - so you should free up as much space as
possible by deleting unwanted files. There are plenty of disk "Cleaner" apps available that can automatically delete
unnecessary files (such as temp files and localisation files) which will free several gigabytes of space.

> Note:
> * A similar error can sometimes be caused if you incorrectly moved the game to a different
    drive: [[System.Reflection.TargetInvocationException TMPE.log is denined]] (or variants of that error, eg. "Sharing
    violation")
> * Check you used the correct way of moving the game. See: [](Moving-the-game-to-a-different-disk-drive.md)

## Was it Fixed?

If not, please let us know: [](Report-a-Bug.md)

Other issues? See: [](Troubleshooting.md)