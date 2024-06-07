# Zoning not Working on Roads

> Article verified: June 2019

## Symptom

One or more of the following symptoms may occur:

* No zoning squares next to roads
* Zoning works on some roads, but not others
* When adding new roads, zoning isn't appearing
* Zoning isn't being updated when I alter my roads
* When I upgrade, move or change my roads, zoning disappears

These issues will prevent you from zoning (residential, industry, commercial, office) or placing certain buildings that
need to snap to a road.

## Cause

There are numerous causes for this issue:

* Some roads do not create zoning by design (e.g. highways)
* Placing super-long stretches of road can break zoning
* Mods can disable zoning

## Solutions

First, check if it's specific to certain roads - if some types of roads create zoning, but others do not, then it's
likely that one of your roads does not create zoning. For example, highways do not create zoning. Just use a different
type of road.

> **Asset Creators:** For details of how to set zoning in the asset editor,
> see: [CSL Modding Info](https://cslmodding.info/asset/network/)

If you place huge long stretches of road in a single action, sometimes the zoning won't work. The solution to this is to
rebuild the road in small chunks (say 5-10 segments at a time); you will see instantly if the zoning returns. Otherwise,
it's not road length problem.

The following mods are broken or obsolete - unsubscribe them:

* [New Roads for Network Extensions 2](https://steamcommunity.com/sharedfiles/filedetails/?id=929114228) - this beaks
  zoning on all roads
    * If you are using the roads in your game, **you have to bulldoze or replace them, save, and only then unsubscribe**
      the mod, otherwise your save will be broken (as game won't know what to do with the weird roads anymore)
    * You can use [Road Removal Tool](https://steamcommunity.com/sharedfiles/filedetails/?id=1243740191) to automate
      that task
* [Network Extensions Project](https://steamcommunity.com/sharedfiles/filedetails/?id=478820060) - breaks game,
  use [Network Extensions 2](https://steamcommunity.com/sharedfiles/filedetails/?id=812125426) instead
    * If you are using the NEP roads in your game, **you have to bulldoze or replace them, save, and only then
      unsubscribe** the mod, otherwise your save will be broken (as game won't know what to do with the weird roads anymore)
    * You can use [Road Removal Tool](https://steamcommunity.com/sharedfiles/filedetails/?id=1243740191) to automate
      that task
* [Toggle Zoning](https://steamcommunity.com/sharedfiles/filedetails/?id=415782697)
* [Disable Zone Check](https://steamcommunity.com/sharedfiles/filedetails/?id=821539759) -
  use [Plop the Growables](https://steamcommunity.com/sharedfiles/filedetails/?id=924884948) instead
* [Road Assistant](https://steamcommunity.com/sharedfiles/filedetails/?id=417926819)
* [Mark-a-Route](https://steamcommunity.com/sharedfiles/filedetails/?id=1548749050) (and any older versions) - reported
  to break zoning

The following mods can alter zoning on new or existing roads - check their settings and make sure you've not
accidentally left them in "no zoning" mode:

* [Advanced Road Anarchy (Updated for 1.11)](https://steamcommunity.com/sharedfiles/filedetails/?id=433567230) - turn it
  off and rebuild the road to see if that fixes problem
* [Fine Road Anarchy](https://steamcommunity.com/sharedfiles/filedetails/?id=802066100) - when clipping is disabled, new
  roads won't update existing zones
* [Grid be Gone](https://steamcommunity.com/sharedfiles/filedetails/?id=1540147921) - check you've not hidden the grid!
* [Network Extensions 2](https://steamcommunity.com/sharedfiles/filedetails/?id=812125426) - disable the zoning feature
  in mod options; or make sure you're not using the keyboard shortcut by accident
* [No Pillars (v1.1+ compatible)](https://steamcommunity.com/sharedfiles/filedetails/?id=463845891) - check zoning is
  enabled
* [Zoning toolset (toggle+upgrade tool)](https://steamcommunity.com/sharedfiles/filedetails/?id=592076973)

Note: If a mod has disabled zoning, and you then alter a zoned road (e.g. upgrade, reverse lane direction, or tweak it
with Move It! mod, create a junction with a new road), it will lose its existing zoning, and it's only later that you
notice the buildings have despawned.

> **Tip:** If you just don't like seeing the zoning squares, use the **Grid be Gone** mod to hide them rather than
> disabling zoning.

## Was it Fixed?

If not, please check through your other mods and also check their workshop pages to see if other users have raised
issues.

Other problems? See: [](Troubleshooting.md)