# Priority Signs Icon Themes

## Overview

This guide explains how to create new country-specific icons for TM:PE [](Priority-Signs.md) tool and its persistent
overlays.

## Icons

There are three files which can be localized:

> The `xx` in the filename should be replaced with the ISO 2-letter country code (in lowercase).

| Filename               | Notes                                                                                                                     |
|:-----------------------|:--------------------------------------------------------------------------------------------------------------------------|
| `sign_priority_xx.png` | **Priority** sign - vehicles entering by the road have right of way over lower priority ("yield" and "stop") traffic.     |
| `sign_yeld_xx.png`     | **Yield** sign - vehicles must slow down and only enter the junction if safe to do so; otherwise they must stop and wait. |
| `sign_stop_xx.png`     | **Stop** sign - vehicles must stop completely and wait for space before entering junction.                                |

* Icons are **200 x 200 px**.
* File Formats:
    * For best results, send us vector images; use [Inkscape](https://inkscape.org/) (free open source vector editor).
    * Alternatively, send us PNG files.
    * You can find existing icons in
      our [source repository](https://github.com/CitiesSkylinesMods/TMPE/tree/master/TLM/TLM/Resources/RoadUI).
* If your country doesn't have a specific sign (e.g. many countries don't have **Priority** sign) you don't need to
  provide one; the default sign can be used instead.
* Once you've made your icons, compress them in a `zip` file (in recent versions of Windows, you can select the files,
  right-click and choose `Send To` > `Compressed (Zipped) Folder`).

## Send us the file / get help

Once you're done, or if you need any help, let us know via [Discord chat](https://discord.gg/faKUnST), or [create a *
*Translation** issue](https://github.com/CitiesSkylinesMods/TMPE/issues/new/choose) in our tracker (if you have `.zip`
file, drag it in to the message box to upload it).

## See also

[](Settings.md):

* [](General.md) - select language to use

[](Contributing.md):

* [](Localisation.md) - help us localize TM:PE
* [](Speed-Limit-Icon-Themes.md) - localize UI for [](Speed-Limits.md)
* [](Timed-Traffic-Light-Buttons.md) - localize UI
  for [](Timed-Traffic-Lights.md)