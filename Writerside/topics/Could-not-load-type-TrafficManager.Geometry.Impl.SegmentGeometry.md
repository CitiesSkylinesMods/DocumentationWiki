# Could not load type TrafficManager.Geometry.Impl.SegmentGeometry

> Verified: January 2020 - TM:PE 11.0

## Symptom

You see an error on-screen or in the [log file](Share-your-Cities-Skylines-log-file.md) like this:

* `Could not load type 'TrafficManager.Geometry.Impl.SegmentGeometry' from assembly ...`

## Cause

It's caused by [Advanced Junction Rule](https://steamcommunity.com/sharedfiles/filedetails/?id=1647686914) mod which has
now been removed from the Steam Workshop.

Unlike assets, when a mod is removed from workshop it doesn't get automatically deleted from your local hard disk. You
will need to remove it manually.

## Solution

* Open **Main Menu > Content Manager > Mods**
* Find and remove **Advanced Junction Rule** mod (click small "[x]" button)
* Exit to desktop, then reload the game

## Was it Fixed?

If not, please [](Report-a-Bug.md).

Other issues? See: [](Troubleshooting.md)