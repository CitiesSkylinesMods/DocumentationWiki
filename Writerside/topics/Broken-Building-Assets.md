# Broken Building Assets

> Article verified: October 2019

> If you haven't already done so, subscribe and
> enable [Loading Screen Mod](https://steamcommunity.com/sharedfiles/filedetails/?id=667342976) - it loads maps much
> faster, reduces RAM consumption for better in-game performance, and fixes a load of common workshop bugs.

## Game breaking

These can crash the game or throw up errors in-game:

* [Bumpa's Motel (Ploppable, 2x4)](https://steamcommunity.com/sharedfiles/filedetails/?id=451397681) - `BrokenAssetException` (
  LOD has too many vertices)
* [Bumpa's Motel (Growable, 4x4)](https://steamcommunity.com/sharedfiles/filedetails/?id=451400763) - `System.IO.EndOfStreamException`
* [Cemetery Block 8x8 01](https://steamcommunity.com/sharedfiles/filedetails/?id=601914510) - `BrokenAssetException` (
  LOD has too many vertices)
* [Cemetery Block 8x8 02](https://steamcommunity.com/sharedfiles/filedetails/?id=601914878) - `BrokenAssetException` (
  LOD has too many vertices)
* [Cemetery Block 8x8 03](https://steamcommunity.com/sharedfiles/filedetails/?id=601915213) - `BrokenAssetException` (
  LOD has too many vertices)
* [Cemetery Block 8x8 04](https://steamcommunity.com/sharedfiles/filedetails/?id=601915518) - `BrokenAssetException` (
  LOD has too many vertices)
* ~~[Dump National Hotel](https://steamcommunity.com/sharedfiles/filedetails/?id=527008015) - `System.NullReferenceException`
    * Asset author states that this require After Dark and also PloppableRICO.~~
* [Eurocorner 11 L3 3x3](https://steamcommunity.com/sharedfiles/filedetails/?id=804986196) - `System.BadImageFormatException`
* [Gas Station](https://steamcommunity.com/sharedfiles/filedetails/?id=1131926009) - `ArgumentException: Offset and length were out of bounds` -
  this is the most horribly broken asset I've ever seen.
* [LRT - Tram Station (Center Platform)](https://steamcommunity.com/sharedfiles/filedetails/?id=1564762222) - many users
  report placement issues, and it also seems to confuse Move It mod. Also, it's possible cause of "Array Index Out Of
  Range" errors (not confirmed, but we've had reports that removing this specific station resolved that issue for one
  user).
* [Phen - Cresentsun (LVL5) (growable)](https://steamcommunity.com/sharedfiles/filedetails/?id=422739257) - `InvalidDataException`
* [regency_corner_restaurant](https://steamcommunity.com/sharedfiles/filedetails/?id=1122848011) - `System.FormatException`
* [RTGApartment building2a L4 4x4](https://steamcommunity.com/sharedfiles/filedetails/?id=834639760) - `BrokenAssetException` (
  LOD has too many vertices)
* [Sagrada Familia (2026), Barcelona, CATALUNYA - Left side (1/2)](https://steamcommunity.com/sharedfiles/filedetails/?id=479191043) - `BrokenAssetException` (
  LOD has too many vertices)
* [Sagrada Familia (2026), Barcelona, CATALUNYA - Right side (2/2)](https://steamcommunity.com/sharedfiles/filedetails/?id=479191809) - `BrokenAssetException` (
  LOD has too many vertices)
* [Skytree with Complex](https://steamcommunity.com/sharedfiles/filedetails/?id=1478663564) - `BrokenAssetException` (
  LOD has too many vertices)
* [Small Hanger no Reqs](https://steamcommunity.com/sharedfiles/filedetails/?id=438937962) - `System.IO.InvalidDataException`
* ~~[XXL Solar Power Sub Station](https://steamcommunity.com/sharedfiles/filedetails/?id=1565619102) - `NULL asset`~~ -
  Removed from workshop

## Bad asset configs

These broken assets are usually filtered out by the loading process, but you should unsubscribe them to avoid any
problems:

* [Antwerp Central Station](https://steamcommunity.com/sharedfiles/filedetails/?id=480362170)
  and [updated version](https://steamcommunity.com/sharedfiles/filedetails/?id=489654912) - `Invalid dimensions`
* [Chlorine Treatment Plant](https://steamcommunity.com/workshop/filedetails/?id=466760694) - `Water facility cannot have water consumption or sewage accumulation`
    * Fixed version: [Chlorine Treatment Plant](https://steamcommunity.com/sharedfiles/filedetails/?id=810730321)
* [Etihad Tower-Abu Dhabi](https://steamcommunity.com/sharedfiles/filedetails/?id=1494819715) - `Invalid dimensions`
* [Guangzhou(Canton) CTF Finance Centre](https://steamcommunity.com/sharedfiles/filedetails/?id=692327582) - `Invalid dimensions`
*
~~[Hiraya_00](https://steamcommunity.com/sharedfiles/filedetails/?id=418205510) - `FormatException: Invalid DDS Image: failed to load`~~ -
Removed from Workshop
*
~~[HSBC Tower](https://steamcommunity.com/sharedfiles/filedetails/?id=421304643) - `Private building cannot include roads or other net types`~~ -
Removed from Workshop
* [Massachusets state house](https://steamcommunity.com/sharedfiles/filedetails/?id=965492462) - `Invalid dimensions`
* [Tree Foundation Owner's HQ](https://steamcommunity.com/sharedfiles/filedetails/?id=457132578) - `Private building cannot include roads or other net types`
* [Tropical Villa](https://steamcommunity.com/sharedfiles/filedetails/?id=1543164365) - `Private building cannot include roads or other net types`
* [Volleyball Court](https://steamcommunity.com/workshop/filedetails/?id=971132208) - `wants to be a sub-building for itself`

> Yeah, I know those `Invalid dimensions` buildings could be revived with Larger Footprints mod, but that mod is
> obsolete. The assets need updating to unique buildings or sub-buildings.

## Graphics glitches

LOD issues:

> Note: Some vehicle assets cause similar problems, see: [](Broken-Vehicle-Assets.md)

* [International Finance Center GuangZhou](https://steamcommunity.com/sharedfiles/filedetails/?id=1633845925) - invalid
  LOD texture size
* [Providence performing arts center](https://steamcommunity.com/sharedfiles/filedetails/?id=1507892576) - invalid LOD
  texture size

Causes buildings to flicker:

* Moorfield House - It was a pack of houses, now removed from workshop. Steam Workshop ID was
  1416566861 ([more info](https://steamcommunity.com/app/255710/discussions/0/1748980761791722336/?ctp=4))

## Minor glitches

These 'work' but have minor problems that you can probably live with:

* [American Eclectic 8A L3 4x2](https://steamcommunity.com/sharedfiles/filedetails/?id=652166164):
    * Growable building is larger than it's defined footprint
    * If there are roads (or anything else) behind the building, its back garden will cover them when the building
      spawns
    * There also seems to be an issue that prevents the building levelling up (max level 3)

## Tips

* The [Loading Screen Mod](https://steamcommunity.com/sharedfiles/filedetails/?id=667342976) has an option to **Check
  assets for errors** which is very useful for finding broken assets!
* To find bloated building assets, which can reduce frame rate and cause lag, use
  the [Mesh Info mod](https://steamcommunity.com/sharedfiles/filedetails/?id=453956891).