> Verified: June 2023 - TM:PE 11.8.0.0

The version of Cities: Skylines on [Epic Games](https://www.epicgames.com/store/en-US/p/cities-skylines) doesn't have Steam Workshop, so you'll need to manually download and install the mod.

## 1. Update game

Make sure you have the latest version of the game - TM:PE only works on latest game version.

## 2. Downloads

You will need to download two mods - Harmony, and TM:PE.

### Harmony

In your browser, go to the [Harmony Releases page](https://github.com/boformer/CitiesHarmony/releases/latest) and follow the instructions there to download and install it.

### TM:PE

* Go to our releases page: <a href="https://github.com/CitiesSkylinesMods/TMPE/releases/latest"><img src="https://img.shields.io/github/v/release/CitiesSkylinesMods/TMPE?label=EPIC - TM:PE&color=313131&logo=epicgames&logoColor=F56C2D" /></a>
* Click the **Assets** link at the bottom of that page
* Download the **`TrafficManager_<verison>_STABLE.zip`** (for example: `TrafficManager_`<a href="https://github.com/CitiesSkylinesMods/TMPE/releases/latest"><img src="https://img.shields.io/github/v/release/CitiesSkylinesMods/TMPE?label= &color=313131" /></a>`_STABLE.zip` or whatever the latest version is)

## 3. Install

Find your mods folder, it's usually something like:

```shell
Windows:
C:\Users\<your name>\AppData\Local\Colossal Order\Cities_Skylines\Addons\Mods

MacOS:
~/Library/Application Support/Colossal Order/Cities_Skylines/Addons/Mods

Linux:
/home/<username>/.local/share/Colossal Order/Cities_Skylines/Addons/Mods
```
**DO NOT PLACE MODS IN `<game_installation_directory>\Cities_Skylines\Files\Mods` DIRECTORY. MOST OF THEM WON'T WORK PROPERTLY WHEN PLACED THERE.**

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

To update, just download the latest version of TM:PE and copy the new `.dll` files to the `TrafficManager` folder (delete the old files first). Don't forget to check for updates to the Harmony mod too (in the `CitiesHarmony` folder)!