> Verified: February 2020

> This is one cause of the [Simulation error Array index is out of range](Simulation error Array index is out of range) error.

## Symptom

You will see this error, or similar, on screen and in the log file:

* `Simulation error: Array index is out of range.`

In the [**log file**](./Share-your-Cities-Skylines-log-file) search to find the error above. On the line after that error, you should see something starting with one of the following:

* `at TerrainManager.GetSurfaceCell ...` (usually occurs when exiting game)

or

* `Parameter name: index` followed by `at System.Collections.Generic.List ...` (usually occurs when loading a game)

(Thanks to krzychu124 for discovering the cause of these errors!)

## Cause

These errors are _not_ caused by TM:PE.

They seem to be caused by using the "Unlock All Tiles" button in the options screen of **81 Tiles** mod.

_We recommend manually unlocking tiles (ie. purchasing them one by one) in-game to avoid these errors._

## Solution

If the log file contains the following line:

* `at TerrainManager.GetSurfaceCell ...`

...then you _should_ be able to just exit to desktop, relaunch the game and load your save normally.

However, if the log file contains the line below:

* `Parameter name: index` followed by `at System.Collections.Generic.List ...`

...your save game is likely broken beyond repair.

However... [There is a chance](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues/679#issuecomment-583938343) that disabling 81 Tiles mod, but leave it subscribed, will allow you to get your game running again, albeit limted to 9 tiles (or 25 tiles if you use a mod like [Purchase It!](https://steamcommunity.com/sharedfiles/filedetails/?id=1612287735)).

> It might even be possible (not tested) to save under new name, exit to desktop, then relaod Cities: Skylines and re-enable the 81 Tiles mod (make sure to turn any 25 Tiles mods off first though!) and relaod the save? Give it a try and if it works please let us know as it will help lots of people!

## Fixed?

If not, see other causes of [Simulation error Array index is out of range](Simulation error Array index is out of range).

Other issues? See: [Troubleshooting](Troubleshooting)