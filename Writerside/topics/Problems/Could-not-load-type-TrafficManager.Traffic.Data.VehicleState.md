# Could not load type TrafficManager.Traffic.Data.VehicleState
> Verified: February 2020

## Symptom

You see an error on-screen or in the [log file](Share-your-Cities-Skylines-log-file.md) like this:

* `Could not load type 'TrafficManager.Traffic.Data.VehicleState' from assembly ...`

This happens if you upgrade from TMPE v10.x to v11.x.

## Cause

It's caused by **CSUR_TMPE_Laneconnector_Fix** mod which is now obsolete.

Note: The mod is not in the Steam Workshop and seems to have been part of a closed beta test for new CSUR roads.

## Solution

* Open **Main Menu > Content Manager > Mods**
* Find and remove **CSUR_TMPE_Laneconnector_Fix** mod (click small "[x]" button)
* Exit game to desktop, then relaunch game

> Tip: If you are using CSUR, try the [CSUR ToolBox](https://steamcommunity.com/sharedfiles/filedetails/?id=1959342332) mod which fixes a number of issues related to those roads.

## Was it Fixed?

If not, [please contact **authors of CSUR project**](https://steamcommunity.com/sharedfiles/filedetails/?id=1959216109) for assistance.

Other issues? See: [](Troubleshooting.md)