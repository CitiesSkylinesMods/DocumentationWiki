# Working with Saved Games

Working with large saved games can be problematic, as they can contain dozens of mods you've not used before and
potentially thousands of assets you've not subscribed to.

This guide contains a few tips for dealing with that.

## Check LSM settings

If you've set LSM to skip prefabs, you might want to turn that off while testing the save.

## Using shared Steam account

This is by far the easiest way to test saves, but you need a spare gaming rig to do it.

* Set up a new Steam account on the other computer
* Family Share with your main account
* Install C:SL on the new account (free, due to family share)
* You now have a clean C:SL to test on 🎉

This way you can subscribe the save, subscribe to all its used assets and mods, enable all of them and not worry about
your existing mods and assets getting in the way. Afterward, you can just "Unsubscribe All" from the second account to
clear it back to vanilla ready for next session of saved game testing.

> For info on how to subscribe the save and it's assets/mods, see the "Using your own Steam account" section below.

Assuming the computer can handle it, you should be able to load the save without too much pain.

For huge saves, with loads of assets/mods, you might need to increase page file depending on how much RAM the computer
has.

## Using your own Steam account

If you only have one computer, well, things are more difficult. :(

### Create a "RESTORE" save game

Start a new game, and save it with name "RESTORE" (or similar).

This save keeps a record of all **enabled** mods and assets you had at the time it was created. That means you can use
it to get them back later.

Note: If you have a bunch of disabled assets/mods,
the [Mods Listing](https://steamcommunity.com/sharedfiles/filedetails/?id=588691634)
or [Assets and Mods Configuration](https://steamcommunity.com/sharedfiles/filedetails/?id=661393399) mods might be of
use.

At a later date, if you add more mods assets you can open the "RESTORE" and just save it again - it will update with all
the additional mods/assets you have at that time.

### Nuke your subscriptions

Unsubscribe all your subscriptions:

* Go to Steam Workshop
* In right sidebar, hover over **Your Files** drop-down and choose **Subscribed Items**
* Click the **Unsubscribe From All** button

Your game is now vanilla.

### Subscribe the saved game

When users [share their saved game](Share-your-Savegame-on-Steam.md) with us, they will provide a URL to that save game.

To subscribe you can do one of the following:

* **Web Browser:** (Recommended) Just go to the URL and click **Subscribe**
    * This requires your browser to be logged in to Steam, obviously
* **Steam Overlay:** Launch C:SL, then from main menu:
    * Press **Shift + Tab** to display Steam Overlay
    * Click the "Workshop" link near the top
    * It opens as a web page, and you can enter the URL at the top

### Install auto-mod enabler

* Subscribe [Auto-Enable Mods](https://steamcommunity.com/sharedfiles/filedetails/?id=903285221) mod.
* Enable it.

### Subscribe and enable its assets

* Go in to Content Manager > Saved games
* Find the saved game and click **Subscribe All**
* Wait for like 5 years or something

Note that if there's a huge number of assets, it's unlikely they'll all get subscribed in one go (there seems to be
something like 2.5k limit to how many it will do at once) - so you'll likely need several attempts to get all the assets
downloaded.

### Disable useless mods

The mod auto enabler should automatically enable any mods that get subscribed in the previous step.

From a testing perspective, some will not be required (disable them to reduce load time):

* Aesthetic / eye candy mods
* Radio stations / sound effects

You should also ask the player what mods they had enabled. The issue here is that their saved game tracks _all mods_ that
were subscribed, not the mods that were enabled. They might have a bunch of disabled mods that would conflict with their
enabled mods.

### Loading Screen Mod

* Subscribe Loading Screen Mod
* Enable it
* Set its options:
    * Disable **Load enabled assets**
    * Enable **Load used assets**
    * Optional: Enable **Save assets report**

This helps minimize the number of assets that get processed when loading the save.

### Page file

It is strongly recommended to have manually defined page file with following settings:

* Minimum size: 1 x RAM
* Maximum size: 2 x RAM

Sometimes you will need even bigger page file for the largest saves.

### Endure save game testing

Load the save game and see what happens. If it fails, you'll have to wade through your log file (I suggest creating a
shortcut link to the file, so you can easily open it from your desktop).

There's no easy way to deal with the issues that crop up, you just have to keep trying different things until it works.

### Reverting back

Just repeat the entire process only this time with your own "RESTORE" saved game.

## Attaching debugger

If you have coding skills, you can attach a debug session to the live game and set breakpoints, etc., to see exactly
what's going on under the hood. For more info see: [](Attaching-Debugger-to-Cities-Skylines.md).

## Credits

Thanks to everyone
who [contributed ideas](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues/111) for
this guide:

* krzychu124
* ntoff
* 1Tomber

And also HUGE thanks to the supplementary mods that help us test saved games on our main accounts!