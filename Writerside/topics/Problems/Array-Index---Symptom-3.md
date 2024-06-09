# Array Index - Symptom 3

> Article verified: November 2021

> This is one cause of the [](Simulation-error-Array-index-is-out-of-range.md) error.

## Symptom

You will see this error:

* `Simulation error: Array index is out of range.`

In the [**log file**](Share-your-Cities-Skylines-log-file.md), you'll see the following below the error:

* `at TransportLine.GetNextStop ...`
* followed by `at BusAI.ArriveAtTarget ...`

## Cause

This appears to be caused by older versions
of [Transport Lines Manager](https://steamcommunity.com/sharedfiles/filedetails/?id=1312767991) mod. For background
information, see [this topic](https://steamcommunity.com/app/255710/discussions/0/1333474229067283692/).

## Solution

* Make sure you are using latest version of TLM

If that doesn't help:

* Unsubscribe TLM mod
* Exit to desktop, then relaunch the game

Note: Sometimes the [Broken Nodes Detector](https://steamcommunity.com/sharedfiles/filedetails/?id=1777173984) mod will
help fix the problem. Or you could
try [Loading Screen Mod](https://steamcommunity.com/sharedfiles/filedetails/?id=667342976) (
LSM) [Safe Mode options](https://steamcommunity.com/workshop/filedetails/discussion/667342976/1626286205707786286/).

## Was it Fixed?

* If you are still getting same error, ask for help on TLM workshop page.
* If you are getting different "Array Index" error, see: [](Simulation-error-Array-index-is-out-of-range.md).
* Other issues? See: [](Troubleshooting.md)