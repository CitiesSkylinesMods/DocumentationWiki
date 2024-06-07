> Article verified: June 2019

# Symptom

Both of these must be true:

* While loading a savegame, an error message appears:
    * `Simulation error: Object reference not set`
* On reviewing your [log file](Share-your-Cities-Skylines-log-file.), the stack trace mentions:
    * `RoadBaseAI.CanEnableTrafficLights`

> Some other error? Try: [Object reference not set to an instance of an object](Object reference not set to an instance of an object)

# Cause

This is a bug in the game itself, not TM:PE.

This problem occurs when your savegame includes a road asset which is no longer available, usually a result of one of the following:

* You unsubscribed a road asset
* You unsubscribed a mod that provided the road asset (such as Network Extensions)
* The author of a road asset (or mod that provided one) deletes their workshop item, which also removes it from your game

# Solution

* Quick fix: Subscribe and enable [Safenets](https://steamcommunity.com/sharedfiles/filedetails/?id=1620588636) mod
* Otherwise, see: [How to remove workshop networks](How to remove workshop networks)

# Fixed?

If not, it's likely your save game is lost, sorry.

Something else? See: [Troubleshooting](Troubleshooting)