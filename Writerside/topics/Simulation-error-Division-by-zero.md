# Simulation error Division by zero

## Symptom

On-screen or in the log file you will see an error like:

* `Simulation error: Division by zero`

This will often crash the game.

## Cause

We have not yet identified the cause, but it is likely caused by a mod or incompatibility between mods.

The error will sometimes include `at TrafficManager.Custom.AI ...`. While TM:PE might be mentioned, it's not the cause
of the error, it's just affected by the error.

## Solution

None at present

We are currently investigating the following mods:

* **Enhanced District Services** (very likely)
* **Real City** (very likely)
* Mod Tools (unlikely)
* Extended Asset Editor (unlikely)
* Stops and Stations
* More Advanced District Snapping (unlikely)
* More Advanced Info Views (unlikely)
* Backward Compatibility: New Roads For Network Extension 2
* Historical Districts
* More Advanced Toolbar
* Trailer Variation Loader
* Enhanced Zoom
* Control Building Level Up
* Cargo Info Mod
* Prop It Up
* CSL Map View
* Extended Control Panel
* WG Citizen Edit (bad values in XML could cause issue)
* WG Realistic Population and Consumption (bad values in XML could cause issue)
* Ploppable RICO, or workshop definitions for it (bad values in XML could cause issue)
* CSL More Graphs
* Profitable Tourism
* Employment Details
* Favorite Cims
* Better Bulldozer
* Demand Master
* Traffic Report Mod
* Mayoral City Service Info
* "DB WLS" font for Procedural Objects

If you have some of those, try disabling them, exit to desktop (to flush them from RAM), then reload your save to see if
it works. If you find a mod that causes the problem, please let us know!

## Was it Fixed?

If not... meh.

Other issues? See: [](Troubleshooting.md)