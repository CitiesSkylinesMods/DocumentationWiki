> Article verified: July 2019

# Symptom

> Note: If it's the mod [](Settings.md) (mod options screen) that are lost, see [TMPE mod options lost](TMPE mod options lost) instead.

* In-game road/rail customisations (lane arrows, traffic lights, restrictions, etc.) are not loading/saving properly

# Cause

This is usually due to having two or more versions of TM:PE subscribed at the same time, even if only one is active.

> For detailed technical information, see [Issue #211](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues/211)

There are other causes, such as incorrectly moving Steam library to a different drive, mod conflicts, etc., however those will exhibit more obvious game stopping errors when launching the game or loading a game.

# Solutions

* Make sure you only have **one version** of TM:PE subscribed
    * Disabling mods is not sufficient, you _must_ completely unsubscribe them
    * Do this from **Content Manager > Mods**, or from **Steam Workshop**
* Make sure you don't have any [](Incompatible Mods)
    * If you do, unsubscribe those as well
* After changing mod subscriptions, always exit the game to desktop to flush old code from RAM

> Note: Mod settings are _per save_, so you'll need to load a save to see them

If problems persist, check for recent updates that might have caused the problem:

1. In Steam client, select **Workshop** tab
2. In the sidebar, select **Subscribed Items** from the **Your Files** menu
3. On the page that appears, change **Date Subscribed** to **Date Updated** in the sidebar

That will show you what's been updated recently, with the most recent items at the top:

* If TM:PE is in that list, it's likely a bug in the update: [Report a bug](Report a bug)
* If it's some other mod, it might be a conflict:
    * Try disabling that mod (then exit to desktop to flush from RAM) and try again
    * If problem is resolved, contact the author of that mod to let them know

If there's nothing obvious causing the issue, it might be a game update:

* Game updates are mentioned on [Steam "myapps" page](https://store.steampowered.com/updated/myapps/), [News tab on Steam](https://steamcommunity.com/app/255710/allnews/), [Announcements on Pardox Forums](https://forum.paradoxplaza.com/forum/index.php?forums/official-information-announcements.878/), [r/CitiesSkylines](https://www.reddit.com/r/CitiesSkylines/), etc.
* TM:PE will warn you if it detects a game update:
    * It's likely we will already know about the bug and are working on a fix
    * But please let us know anyway as you might spot a bug we don't know about

# Fixed?

If not, please let us know: [Report a bug](Report a bug)

Other issues? See: [Troubleshooting](Troubleshooting)