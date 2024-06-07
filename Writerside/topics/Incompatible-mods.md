# Incompatible Mods

> Verified: March 2022 - TM:PE 11.6.5.1

> We very strongly recommend using
> the [Compatibility Report mod](https://steamcommunity.com/sharedfiles/filedetails/?id=2633433869)
> * It detects broken / incompatible / outdated mods
> * It recommends alternatives and fixes
>
> [![Compatibility Report](picCompatibilityReport.jpeg)](https://steamcommunity.com/sharedfiles/filedetails/?id=2633433869)

## Overview

We take every effort to make TM:PE compatible with other mods, but due to the nature of modding conflicts may still
occur.

As of TM:PE 11.0, we transitioned to Harmony library which improves compatibility with other mods. For TM:PE 11.6, and
later, we use the main [Harmony Mod](https://steamcommunity.com/sharedfiles/filedetails/?id=2040656402) like most other
mods.

## Incompatible mod detection

When it loads, TM:PE performs several automatic checks to detect incompatible mods.

#### Known incompatibilities

> **TM:PE Team:** See details on how to maintain the [Incompatible Mods List](Incompatible-Mods-List.md)

When you launch Cities: Skylines app, or first enable TM:PE, we scan to see if you have any already-identified
incompatible mods subscribed. If any are found, an on-screen warning is shown which allows you to unsubscribe them.

You can customise how the mod checker works in [General](General.md) [settings](Settings.md).

#### Unexpected mod conflicts

If TM:PE subsequently detects that another mod has altered game code it uses, even if it doesn't know what that mod is,
it will display an on-screen warning after starting a new game or loading an existing game.

You can choose whether to show the on-screen warning in [General](General.md) [Settings](Settings.md).

#### Log File TMPE.log

Details of any incompatibilities, whether known or unexpected, can be found in the [TMPE.log](TMPE.log.md) file.

## Broken or obsolete mods / assets

For tracking down other broken mods and assets, see this Steam
Guide: [Finding Broken & Bloated Workshop Subscriptions](https://steamcommunity.com/sharedfiles/filedetails/?id=1846793796)

We also highly recommend subscribing and enabling
the [Compatibility Report](https://steamcommunity.com/sharedfiles/filedetails/?id=2633433869) mod which helps identify
any other broken mods you have and suggests better alternatives.