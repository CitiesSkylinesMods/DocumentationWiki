# Floating Cyclists and Discarded Bicycles

> Verified: April 2022 - TM:PE 11.6.5.2

## Symptoms

[#1472](https://github.com/CitiesSkylinesMods/TMPE/issues/1472): You see discarded bicycles and the cyclists are "
hovering" down the road without their bike:

![Floating cyclist](picFloatingCyclist_bug.png)

> This article is specifically about cyclists/bikes. If you are seeing floating cars/trucks,
> see [](Floating-vehicles.md) instead.

## Cause

It appears load sequence of certain mod causes this issue:

* [Realistic Walking speed](https://steamcommunity.com/sharedfiles/filedetails/?id=1412844620)
* [Optimized Outside Connections](https://steamcommunity.com/sharedfiles/filedetails/?id=1721492498)

Both of these mods usually work fine, however sometimes they conflict depending on which mod loads first. It's possible
there is also some other mod which affects them, but we've not been able to track it down.

## Solution

First, try this:

1. Exit game to desktop
2. _Unsubscribe_ one of the mods listed above
    * Don't just _disable_ the mod, it needs _unsubscribing_!
3. Launch the game to see if the problem is fixed
4. If not, repeat steps 1-3 above but unsubscribe the other mod

If that fixes the problem, try resubscribing the mods - they'll usually work fine.

If you are still having problems, try
the [Loading Order Mod (LOM)](https://steamcommunity.com/sharedfiles/filedetails/?id=2620852727) which ensures mods load
in a known-working sequence.

## Was it Fixed?

If not, try unsubscribing other mods, particularly any listed
in [Issue #1472](https://github.com/CitiesSkylinesMods/TMPE/issues/1472) - if you find another mod that causes the
problem please leave a comment in that issue.

Other issues? See: [](Troubleshooting.md)