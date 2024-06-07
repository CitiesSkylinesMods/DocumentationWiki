# ArgumentNullException Argument cannot be null

> Verified: February 2020 - TM:PE 11.0

## Symptom

> See also: Similar [](System.ArgumentNullException-''-with-1-arguments.md)

An error is shown on screen or in log file:

* `ArgumentNullException: Argument cannot be null.`

Additionally, in the log file, the stack trace will contain references to one or both of these:

* `VehicleEffects` or `ExtraVehicleEffects`

## Cause

This can be caused by the [Vehicle Effects](https://steamcommunity.com/sharedfiles/filedetails/?id=780720853)
or [Extra Vehicle Effects](https://steamcommunity.com/sharedfiles/filedetails/?id=815103125) mods if they encounter
invalid asset settings file.

## Solution

It doesn't seem to cause any problems and can be ignored.

## Was it Fixed?

If not, probably best to ask about it in Steam discussion forum or on the mod workshop pages.

Other issues? See: [](Troubleshooting.md)