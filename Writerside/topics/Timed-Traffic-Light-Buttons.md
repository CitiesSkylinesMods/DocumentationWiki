# Timed Traffic Light Buttons

## Overview

The [](Timed-Traffic-Lights.md) UI includes some button images which can be translated to other
languages if desired; this article explains how.

## Images

There are 4 icons as detailed below:

> The `xx` in the filename should be replaced with the 2-letter language code (TM:PE team can do that for you if you are
> unsure of which code to use).

|                      Icon                      | File name                  | Dimensions  | Notes                                                                                                                               |
|:----------------------------------------------:|:---------------------------|:-----------:|:------------------------------------------------------------------------------------------------------------------------------------|
|         ![Counter](btnTTL_counter.png)         | `light_counter_xx.png`     | 103 x 95 px | Text should be centered at top of button. Bottom half of button should be blank (the current step number is overlaid in that area). |
|         ![Light Mode](btnTTL_mode.png)         | `light_mode_xx.png`        | 103 x 95 px | Text should be centered in middle of button.                                                                                        |
|  ![Pedestrian Mode 1](btnTTL_pedModeAuto.png)  | `pedestrian_mode_1_xx.png` | 73 x 70 px  | Text should be centered in middle of yellow area. Bottom part of button should be transparent as it overlays other UI elements.     |
| ![Pedestrian Mode 2](btnTTL_pedModeManual.png) | `pedestrian_mode_2_xx.png` | 73 x 70 px  | Text should be centered in middle of yellow area. Bottom part of button should be transparent as it overlays other UI elements.     |

Sadly we don't yet have blank templates for those images; just copy/paste blank section of the image over the existing
text.

> TM:PE devs: The filename is determined
>
via [`LoadTexturesWithTranslation()`](https://github.com/CitiesSkylinesMods/TMPE/blob/master/TLM/TLM/UI/Textures/TrafficLightTextures.cs);
> as long as correct locale is in the resource filename, it should work as expected.

## Send us the file / get help

Once you're done, or if you need any help, let us know via [Discord chat](https://discord.gg/faKUnST), or [create a *
*Translation** issue](https://github.com/CitiesSkylinesMods/TMPE/issues/new/choose) in our tracker.

## See also

[](Settings.md):

* [](General.md) - select language to use

[](Contributing.md):

* [](Localisation.md) - help us localize TM:PE
* [](Speed-Limit-Icon-Themes.md) - country-specific speed limit icons