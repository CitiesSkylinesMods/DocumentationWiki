# Array Index - Symptom 10

> Article verified: January 2020

> This is one cause of the [](Simulation-error-Array-index-is-out-of-range.md) error.

## Symptom

You will see this error, or similar, on screen and in the log file:

* `Simulation error: Array index is out of range.`

In the [**log file**](Share-your-Cities-Skylines-log-file.md) search to find the error above. On the line after that
error, you should see something starting with:

* `at TerrainModify.ApplyQuad ...`

or

* `at TerrainModify.UpdateAreaImplementation ...`

## Cause

We suspect this is caused by the outdated and game-breaking mods, namely:

* **[Building Anarchy](https://steamcommunity.com/sharedfiles/filedetails/?id=912329352)**
    * Instead of Building Anarchy mod, you should use combination of
      both [Ploppable RICO Revisited](https://steamcommunity.com/sharedfiles/filedetails/?id=2016920607) (activate
      relevant settings in RICO options before loading a save!)
      and [Find It!](https://steamcommunity.com/sharedfiles/filedetails/?id=837734529) mods. Alternatively Find It! in
      combination with [Plop the Growables](https://steamcommunity.com/sharedfiles/filedetails/?id=924884948) also
      works.
* **[Terraform Tool 0.9](https://steamcommunity.com/sharedfiles/filedetails/?id=411095553)**
    * Instead of Terraform Tool 0.9 mod, you should use either vanilla terraform tools (in the Landscaping menu
      in-game), or, optionally, subscribe and enable
      the [Extra Landscaping Tools](https://steamcommunity.com/sharedfiles/filedetails/?id=502750307) mod which adds a
      few extra features.
* **[Terrain Generator](https://steamcommunity.com/sharedfiles/filedetails/?id=453425585)**
    * Instead of Terrain Generator mod, use either vanilla terraform tools (in the Landscaping menu in-game), or,
      optionally, subscribe and enable
      the [Extra Landscaping Tools](https://steamcommunity.com/sharedfiles/filedetails/?id=502750307) mod to sculpt
      terrain in-game or map editor

Other possible causes (not verified but worth considering):

* It could also be due to one or more mods not being compatible with 81 Tiles mod. Many older mods assume that your
  whole city will be within the central 25 tiles.
* Old mods that alter zoning around roads -- see also: [](Array-Index---Symptom-5.md)

## Solution

* Completely unsubscribe **Building Anarchy**, **Terraform Tool** and **Terrain Generator** mods
    * Don't just disable them; they need to be completely removed so unsubscribe them
* Exit game to desktop
* Relaunch game and see if the error has gone

There might be some left-over side effects due to faulty terrain glitches or broken buildings on the map in your save
game. If that is the case:

* If you haven't already done so, subscribe and
  enable [Loading Screen Mod](https://steamcommunity.com/sharedfiles/filedetails/?id=667342976) (LSM)
* In its mod options, enable the Safe Mode options
* Load your save game
* Assuming it works:
    * Broken building should just automatically despawn
    * If there are terrain glitches, use "Smooth" or "Flatten Terrain" tool to fix (you can find those tools in the
      Landscaping menu in-game).
* Save the game _under a new file name_
* Exit to desktop, relaunch then load the new save file - should now hopefully work properly :)

## Was it Fixed?

If not, see other causes of [](Simulation-error-Array-index-is-out-of-range.md).

Other issues? See: [](Troubleshooting.md)