> Article verified: March 2022 - TM:PE 11.6.5.1

# Symptom

In **Content Manger > Mods**:

* there are no mods listed, or
* a recently subscribed mod isn't listed

This guide is also applicable to the `Content Manager > Assets` screen too if it suffers same problem.

# Cause

This bug is _not_ caused by TM:PE.

It is likely a temporary workshop error or problem with another mod.

# Solution

Try each of these in turn; if it starts working you can stop.

* Completely **log out** of your Steam client account, then log back in again.
    * Exit Cities: Skylines (exit to desktop)
    * In Steam client, click your profile link (top right corer of window)
    * Log out
    * Then exit Steam client, and relaunch it
    * Log in
* You need Steam to be in **online mode** for mods to work; they disappear in [offline mode](https://support.steampowered.com/kb_article.php?ref=3160-agcb-2555)
    * Lots of mods, particularly the more advanced ones, _need_ to be run online because it's how they detect other mods for compatibility purposes
* Make sure you aren't using the `--noWorkshop` or `--disableMods` [launch parameters](https://steamcommunity.com/sharedfiles/filedetails/?id=466981085)
    * If you are, remove them, then relaunch the game
* In Steam Workshop, **make sure you are * NOT * subscribed** to these two mods:
    * [Improved Assets Panel](http://steamcommunity.com/sharedfiles/filedetails/?id=417430545) - unsubscribe!
    * [Improved Mods Panel](http://steamcommunity.com/sharedfiles/filedetails/?id=416033610) - unsubscribe!
    * Or any other versions of those mods
* In **Content Manager > Mods**, press **F5** to refresh the page.
* Exit the game and reload:
    * Depending on Steam settings (or server issues), subscribed items might not download while the game is running
    * Disabling mods such as [Less Steam](https://steamcommunity.com/sharedfiles/filedetails/?id=812107110), [Skip Intro](https://steamcommunity.com/sharedfiles/filedetails/?id=1665106193) or [NoIntro](https://steamcommunity.com/sharedfiles/filedetails/?id=1675213439) might also help in rare cases
* [Change Download Region](https://support.steampowered.com/kb_article.php?ref=9498-WPDF-3220)
* [Refresh Steam Files](https://support.steampowered.com/kb_article.php?ref=3134-TIAL-4638) then [Verify Game Cache](https://support.steampowered.com/kb_article.php?ref=2037-QEUH-3335)
* Did you move the game to a different disk drive?
    * See: [How to move the game to a different disk drive](How to move the game to a different disk drive)
* Make sure there are no files in the folder `...\Colossal Order\Cities_Skylines\Addons\ColorCorrections`
    * Broken LUTs can cause content manager to fail

# Fixed?

If problems persist, probably best to ask the internet.

Other issues? See: [Troubleshooting](Troubleshooting)