# Vehicle LODs are flashing

> Verified: February 2020 - TM:PE 11.0

## Symptom

> **LOD** means **Level of Detail**. When you zoom out, the game uses simplified LOD models and textures for assets (
> cims, buildings, vehicles, etc.) to reduce graphics workload.

One or more of the following symptoms can occur:

* When breaking, entire vehicle flashes
* When turning, half (sometimes all) the vehicle flashes
* When responding to emergencies, the vehicle flashes

> Shiny black LODs? See: [](Shiny-Black-Vehicle-LODs.md)

## Cause

This is almost always caused by the LOD texture not having the correct colours for brake lights, indicators or emergency
lights.

In many cases, asset authors will use basic tools to shrink down textures, effectively resizing the texture images. This
causes some blurring, which in turn can change the colours used to depict where indicators and break lights are.

> **Asset creators:** Fix your LODs! Specifically the [**Illumination** (```_i```) and/or **Color
** (```_c```) maps](https://cslmodding.info/asset/vehicle/).

When the game can't find the colours its looking for, it flashes all or part of the vehicle. This is likely done as a
reminder to the asset creator to fix their LOD texture, but it seems some creators release their vehicle without
realizing there's a problem.

If all vehicle LODs are flashing, it's likely that the game had to rescale textures. This is either due to having too
many assets (their textures can't fit in VRAM) or due to user choosing low quality textures in graphics settings.

## Solution

> Don't want to unsubscribe vehicles/assets? If your GPU can handle
> it: [Disable LODs!](https://steamcommunity.com/sharedfiles/filedetails/?id=561888259)

Some, but not all, vehicles flashing?

* Unsubscribe any [](Broken-Vehicle-Assets.md)
* If you find a flashing vehicle not on that list:
    * Please let us know! [](Report-a-Bug.md)
    * Unsubscribe it
* Please leave a comment on the asset workshop page so author and other users know it has a problem

All vehicles flashing?

* Subscribe and activate the [Loading Screen Mod](https://steamcommunity.com/workshop/filedetails/?id=667342976) - it
  greatly reduces RAM and VRAM consumption, especially if you have lots of assets
* Still having problems? You'll have to unsubscribe some assets, sorry.
    * Use the [Mesh Info](https://steamcommunity.com/sharedfiles/filedetails/?id=453956891) mod to find poorly optimized
      assets and unsubscribe those first!
    * Can't kick your asset
      addiction? [Try this technique](https://steamcommunity.com/sharedfiles/filedetails/?id=449998850)!

## Was it Fixed?

If not, please let us know: [](Report-a-Bug.md)

Other problems? See: [](Troubleshooting.md)