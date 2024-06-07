# Incompatible Mods List

> Verified: March 2022 - TM:PE 11.6.5.1

> This page is intended for TM:PE support team who maintain the incompatible mods list.  
> If you are an end-user (subscriber), see [](Incompatible-Mods.md) page instead.

## Overview

TM:PE has three ways to detect mod incompatibilities:

* A pre-defined list of known incompatible mods
* Any other build of TM:PE will be treated as incompatible
* Automatic detection of code conflicts when applying code patches/redirects

This guide is for the former, the list of known incompatible mods.

The [`ModsCompatibilityChecker`](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/blob/master/TLM/TLM/Util/ModsCompatibilityChecker.cs)
class loads the list of known mod incompatibilities, then compares it to the users' mod subscriptions. If incompatible
mod are detected
the [`IncompatibleModsPanel`](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/blob/master/TLM/TLM/UI/IncompatibleModsPanel.cs)
is shown.

## File location and format

The [`incompatible_mods.txt`](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/blob/master/TLM/TLM/Resources/incompatible_mods.txt)
defines the known incompatible mods.

Entries in the file specify the workshop id and mod name, separated by a semicolon `;`. For example:

```
626024868;Traffic++ V2
407335588;No Despawn Mod
```

Notes:

* Every line in the file must list a single mod
* The last line in the file must not be blank
* TM:PE is only interested in the workshop id (the number before the first semi-colon on a line)
* The mod name just helps with maintaining the file (aid human readability)

## Adding a mod to the list

With over a million subscribers, adding a mod to the TM:PE incompatible mod list can cripple subscriptions to that mod.

As such, every attempt must be made to avoid adding mods to the list.

Ask yourself:

* Does it really merit adding this mod to the list?
* Is it really causing a big problem for us or end users?

If the incompatibility is likely to be temporary, a better alternative might be to have that incompatibility added to
the [Compatibility Report mod](https://steamcommunity.com/sharedfiles/filedetails/?id=2633433869) which gets more
frequent updates.

If you are sure the mod needs to be on the list:

* Create a page in the [Troubleshooting](Troubleshooting) guide to help users solve or work around with the issue
* Contact the mod author, to see if the situation can be resolved
* Only if the mod conflict can't be resolved, add to the incompatible mods list

## Removing mods from the list

Don't remove a mod from the list just because it no longer exists in the workshop:

* The game doesn't always remove the local copy of a mod, even if it's deleted on the workshop
* As such, we need to keep removed mods on the incompatible list permanently

If a mod is about to become compatible, don't remove it from the list until it both _is_ compatible and has also been
updated in the workshop. Only after the workshop contains an updated (compatible) version of a mod should it be removed
from the list.

## The list isn't a silver bullet

The mod checker feature can be a source of friction with the community, so we added options to [](General.md)
in [](Settings.md) that allow users to disable it completely, or ignore disabled mods. This means that mod
incompatibility issues may still arise, even for known incompatible mods.

The [Troubleshooting](Troubleshooting) guide should always be first place to look when users report any errors or
issues.

## Changes in TM:PE v11

In version 11 and above, the incompatible mod checker will always run, even if user has disabled it:

* A list of all subscribed mods is added to `TMPE.log`, showing:
    * Name and workshop ID are shown
    * `(local)` = `...\Cities_Skylines\Addons\Mods` folder
    * `!` indicates incompatible mod
    * `*` indicates enabled mod
* If duplicate instances of TM:PE are subscribed:
    * A warning panel will be shown to user even if they disabled mod checker
    * The updated mod checker now successfully detects all other TM:PE instances

As such, the `TMPE.log` is now more useful for support purposes.

In TM:PE 11.6, an additional list of game-breaking mods was added (in source code of the mod checker) which works by
comparing the mod _name_ rather than it's workshop ID.
