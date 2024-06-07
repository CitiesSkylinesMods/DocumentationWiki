> Verified: December 2021 - TM:PE 11.6.1 TEST

## Overview

This guide explains how to create new country-specific themes for icons shown in TM:PE [Speed Limits](Speed Limits) tool and persistent [overlays](overlays).

## Icons

* Icons are **200 x 200 px**. Rectangular shapes are allowed, for example Canadian and US signs are rectangular.
* File formats:
    * For best results, send us vector images; use [Inkscape](https://inkscape.org/) (free open source vector editor). See [`roadsigns-default.svg`](https://github.com/CitiesSkylinesMods/TMPE/blob/master/TLM/TLM/Resources/SignThemes/SpeedLimitDefaults/roadsigns-default.svg) for an example.
    * Alternatively, send us PNG files. For examples of round signs see [UK theme](https://github.com/CitiesSkylinesMods/TMPE/tree/master/TLM/TLM/Resources/SignThemes/MPH_UK), for rectangular signs see [USA theme](https://github.com/CitiesSkylinesMods/TMPE/tree/master/TLM/TLM/Resources/SignThemes/MPH_US).
    * You can find all existing themes in our [source repository](https://github.com/CitiesSkylinesMods/TMPE/tree/master/TLM/TLM/Resources/SignThemes). 
* We require an icon for each of the speeds supported by TM:PE, named accordingly:
    * `0.png` denotes "unlimited speed" which is usually a circle with a dash across it (in most countries); in-game it's often used on rail networks
    * For **miles per hour**, the signs come in **5..90** range, named like `5.png`, `10.png`, .. `90.png` in steps of 5 MPH.
    * For **kilometres per hour**, the signs come in **5..140** range, named like `5.png`, `10.png`, .. `140.png` in steps of 5 km/h.
* A theme can be marked as supporting MPH or km/h, or both if applicable.

Once you've made your icons, compress them in a zip file (in recent versions of Windows, you can select the files, right-click and choose `Send To` > `Compressed (Zipped) Folder`).

## Send us the file / get help

Once you're done, or if you need any help, let us know via [Discord chat](https://discord.gg/faKUnST), or [create a **Translation** issue](https://github.com/CitiesSkylinesMods/TMPE/issues/new/choose) in our tracker (if you have `.zip` file, drag it in to the message box to upload it).

## See also

[Settings](Settings):

* [General](General) - select language to use

[Contributing](Contributing):

* [Localisation](Localisation) - help us localise TM:PE
* [Priority Signs Icon Themes](Priority Signs Icon Themes) - localise UI for [Priority Signs](Priority Signs)
* [Timed Traffic Light Buttons](Timed Traffic Light Buttons) - localise UI for [Timed Traffic Lights](Timed Traffic Lights)