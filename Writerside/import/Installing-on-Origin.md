> Verified: June 2023 - TM:PE 11.8.0.0

The version of Cities: Skylines on [EA Origin](https://www.origin.com/gbr/en-us/store/cities-skylines/cities-skylines) doesn't have Steam Workshop, so you'll need to manually download and install the mod.

## 1. Update game

Make sure you have the latest version of the game. You can do this by turning on auto-update feature in Origin:

> ![Origin auto-update](https://user-images.githubusercontent.com/1386719/60513570-811f8280-9ccf-11e9-8f34-845aa09e0d56.png)

## 2. Downloads

You will need to download two mods - Harmony, and TM:PE.

### Harmony

TM:PE needs the latest stable release of Harmony.

In your browser, go to the [Harmony Releases page](https://github.com/boformer/CitiesHarmony/releases/latest) and follow the instructions there to download and install it.

### TM:PE

* Go to our releases page: <a href="https://github.com/CitiesSkylinesMods/TMPE/releases/latest"><img src="https://img.shields.io/github/v/release/CitiesSkylinesMods/TMPE?label=Origin - TM:PE&color=F56C2D&logo=origin&logoColor=F56C2D" /></a>
* Click the **Assets** link at the bottom of that page
* Download the **`TrafficManager_<verison>_STABLE.zip`** (for example: `TrafficManager_`<a href="https://github.com/CitiesSkylinesMods/TMPE/releases/latest"><img src="https://img.shields.io/github/v/release/CitiesSkylinesMods/TMPE?label= &color=313131" /></a>`_STABLE.zip` or whatever the latest version is)

## 3. Install

Find the `Mods` folder, it's usually something like:

```shell
<OriginFolder>\CitiesSkylines\Files\Mods\
```

_The `<OriginFolder>` is usually found at `C:\Program Files(x86)\Origin Games`_

Inside that `Mods` folder, create two new folders:

* `TrafficManager` - for TM:PE
* `CitiesHarmony` - for Harmony

Make sure the folder names are correct, including the capitalisation! Other mods look for those exact folder names as it's the only way mods can identify each other when not running in Steam version of the game.

Next, double-click the zips you downloaded to view their contents (should be a load of `.dll` files) and copy those files in to the folders.

## 4. Enable the mod

* Launch **Cities: Skylines**
* Choose **Main Menu > Content Manager > Mods**
* Find **Harmony** and **Enable** it (you only need to do this once)
* Find **TM:PE** and **Enable** it (you only need to do this once)

## Updating the mod

Because there's no Steam Workshop integration, you'll have to manually update the mod - this is particularly important after any updates to Cities: Skylines app.

To update, just download the latest version of TM:PE and copy the new `.dll` files to the `\Cities Skylines\Files\Mods\TrafficManager` folder, overwriting the old files.

Don't forget to check for updates to the Harmony mod too!