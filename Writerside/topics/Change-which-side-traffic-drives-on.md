# Change Side The Traffic Drives On 

> Article verified: October 2019

## Symptom

Cars are driving on wrong side of road.

## Cause

You forgot to change driving direction when starting a new game.

## Solution

1. Subscribe and enable [Mod Tools](https://steamcommunity.com/sharedfiles/filedetails/?id=450877484)
2. Load your save, then pause the game (`spacebar` key)
    * If using TM:PE, click the **Clear Traffic** button on the TM:PE menu bar
3. Press `Ctrl`+`E` to open Scene Explorer
4. Find `SimulationManager` in the list, expand it if necessary
5. Look for `m_metaData` and set `m_invertTraffic` property to:
    * `true` = traffic drives on left
    * `false` = traffic drives on right
6. Save the game (under new file name)
7. Exit to desktop, then relaunch Cities: Skylines
8. You can unsubscribe Mod Tools if you no longer need it
9. Reload the save - traffic might freak out a bit for the first few minutes
    * If using TM:PE, check over all your road customisations to make sure they are still valid

## Solved?

If not, it's likely due to some mods not updating themselves when the driving side changes and you're only option will be to start a new game, sorry.

Other issues? See: [Troubleshooting](Troubleshooting)