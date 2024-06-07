# The class PropVehCount.PropVehCount could not be loaded

> Verified: February 2020

## Symptoms

You see errors on-screen or in the log file like this:

* `The class PropVehCount.PropVehCount could not be loaded, used in PropVehCount`

or

* `The class PropVehCount.MyBehaviour could not be loaded, used in PropVehCount`

Usually both are shown one after the other.

## Cause

It's the [AutoLineBudget](https://steamcommunity.com/sharedfiles/filedetails/?id=1767246646) mod.

The mod also seems to be using a very old version of .Net Framework (v2; game uses v3.5) and is published as a "Camera
Script" rather than a "Mod".

It is possibly due to conflict with another mod that alters transport line budgets, such as an auto-budget mod, or mods
such as IPT (Improved Public Transport) or TLM (Transport Lines Manager). However, considering the mod is somehow in
the "Cinematic Cameras" category we suspect the error is in the AutoLineBudget mod itself.

## Solution

* Exit game to desktop
* Unsubscribe the mod

## Was it Fixed?

If not, check to see if you have other versions of the mod (maybe different workshop ID than the one linked above).

Other issues? See: [](Troubleshooting.md)