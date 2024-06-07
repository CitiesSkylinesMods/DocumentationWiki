# Shiny Black Vehicle LODs
> Article verified: August 2019

## Symptoms

> **LOD** means **Level of Detail**. When you zoom out, the game uses simplified LOD models and textures for assets (cims, buildings, vehicles, etc) to reduce graphics workload.

* Some or all vehicle LODs have turned 'black' or 'shiny black'
* In addition, they may become more box-like (brick-shaped)
* Busses and other large vehicles seem to be more frequently affected

## Cause

The vehicles with 'shiny black' LODs aren't usually the problem assets; they are symptoms of some other broken asset that (and it doesn't even have to be the same type of vehicle).

This is caused by assets that have [invalid texture sizes](https://steamcommunity.com/workshop/filedetails/discussion/667342976/1639789306562159404/) (their dimensions _must_ be a power of two).

The load order (somewhat random) determines which other assets are adversely affected (those loaded after the broken asset). You might see the affected assets change over time due to this.

## Solution

1. Subscribe and enable [Loading Screen Mod](https://steamcommunity.com/sharedfiles/filedetails/?id=667342976) (LSM)
2. In LSM mod otions, enable **Check assets for errors** and make a note of the folder path shown above that option
3. Load your save game that has the black LOD issues
4. Exit to desktop

Next, go in to the folder you made a note of in step 2 above. You will see a `Reports` folder, which in turn contains a `LoadingScreenMod` folder. Locate the most recent `Assets report` file in that folder and open it in a browser.

* Look for any assets which have `Invalid texture size` (or similar) next to them
* Unsubscribe those assets (and please let the asset author know!)

Some known broken vehicles are listed in [](Broken-Vehicle-Assets.md). If you find more, please let us know and we'll add to the list!

## Was it Fixed?

If not, please let us know: [](Report-a-Bug.md)

Other problems? See: [](Troubleshooting.md)