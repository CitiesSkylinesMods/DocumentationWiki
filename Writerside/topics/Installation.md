# Installation

> Verified: June 2023 - TM:PE 11.8.0.0

**Exit the game** first, then follow these steps...

## 1. Subscribe and enable TM:PE

> **Only have one version of TM:PE _subscribed/installed_ at a time.**
>  
> Completely unsubscribe/remove all other versions of TM:PE, otherwise you get save/load bugs.

You can use TM:PE on the following game portals:

* **Steam** (Windows / Mac / Linux):
    * Subscribe only one: <a href="https://steamcommunity.com/sharedfiles/filedetails/?id=1637663252"><img src="https://img.shields.io/github/v/release/CitiesSkylinesMods/TMPE?label=stable&color=7cc17b&logo=steam&logoColor=F5F5F5" /></a> <a href="https://steamcommunity.com/sharedfiles/filedetails/?id=2489276785"><img src="https://img.shields.io/github/v/release/CitiesSkylinesMods/TMPE?include_prereleases&label=test&color=f7b73c&logo=steam&logoColor=F5F5F5" /></a>
    * Enable the mod in **Main Menu > Content Manager > Mods**
* **GeForce Now**:
    * **EDIT: Apparently GeForce Now platform no longer allows mods to be used :(**
    * You must launch the game from Steam within GF Now (use **Steam** procedure above)
    * If the mod doesn't download, [Change Steam Download Region](https://support.steampowered.com/kb_article.php?ref=9498-WPDF-3220) then [Verify Integrity of Game Files](https://support.steampowered.com/kb_article.php?ref=2037-QEUH-3335)
* **Other portals**:
    * [Installing on Epic Games](Installing-on-Epic-Games.md)
    * [Installing on Origin](Installing-on-Origin.md)
* Downloads for manual installation:
    * Download **Harmony**: <a href="https://github.com/boformer/CitiesHarmony/releases"><img src="https://img.shields.io/github/v/release/boformer/CitiesHarmony?label=downloads&include_prereleases&logo=buffer" /></a>
    * Download **TM:PE**: <a href="https://github.com/CitiesSkylinesMods/TMPE/releases"><img src="https://img.shields.io/github/v/release/CitiesSkylinesMods/TMPE?label=downloads&include_prereleases&logo=buffer" /></a>

Unfortunately, the following game portals don't allow code mods:

* **Console** (Xbox, PS4, Switch) - no support for mods
* **Windows 10 Edition** (Xbox live) - it's the Xbox version of the game

## 2. Unsubscribe incompatible mods

When TM:PE is first enabled, and also each time you launch Cities: Skylines app, it will scan for [Incompatible Mods](Incompatible-mods.md) and display a warning if any are found.

* If incompatible mods are found, you should unsubscribe them.
    * You can customise how this feature works in [General](General.md) [Settings](Settings.md).
    * See [this Workshop topic](https://steamcommunity.com/workshop/filedetails/discussion/1637663252/1678063648163943780/) for details of incompatible mods
    * Removing mods which add roads or tracks must be done carefully: [How to remove workshop networks](How-to-remove-workshop-networks.md)
    * See also: [Recommended mod substitutions](Recommended-Mod-Substitutions.md), [Community database of mod incompatibilities](https://docs.google.com/spreadsheets/d/1mVFkj_7ij4FLzKs2QJaONNmb9Z-SRqUeG6xFGqEX1ew/htmlview#)
* **After unsubscribing any mods, _always_ exit to desktop and then relaunch the game to ensure they are fully flushed from RAM.**

You're now ready to start a game! Use the [Toolbar](Toolbar.md) to customise your roads.

## FAQ

**If I unsubscribe TM:PE will my save games break?**
> You can safely remove TM:PE at any time, save games will still work without it

**Does it reduce frame rate or cause lag?**
> Yes, some of its features can cause fps drop or lag, and it will be worse on large cities:
> * The documentation page for each feature includes an FAQ with more specific details
> * Unwanted features can be disabled im [Maintenance](Maintenance.md) [Settings](Settings.md)
> * See also: [C:SL Performance Tuning Guide](https://steamcommunity.com/sharedfiles/filedetails/?id=1637663252)

## Problems?

* See: [Troubleshooting](Troubleshooting.md)