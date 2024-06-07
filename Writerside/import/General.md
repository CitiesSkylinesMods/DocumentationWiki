> Verified: March 2022 - TM:PE 11.6.5.1

[Settings](Settings): **General** | [Gameplay](Gameplay) | [Policies](Policies) | [Overlays](Overlays) | [Maintenance](Maintenance) | [Keybinds](Keybinds)

## Overview

Use these [settings](settings) to set general options such as language, user inteface, simulation, and mod compatibility checks.

## Settings

### Localisation

_Use these options to apply regional language and icon themes to TM:PE..._

#### Select language

* Defaults to same language as the game, but you can choose a different language if desired
* For a list of current translations, see: [Languages](Languages). To contribute translations, see: [Localisation](Localisation).

#### Display speed limits as MPH instead of km/h

* If enabled, the [Speed Limits](Speed Limits) tool will work in **Miles Per Hour** instead of **km/h**

#### Road signs theme

> Want to add a new themes? See **Images** section in [Contributing](Contributing) guide.

* Select a country-specific style for road signs
* This effects overlay icons for multiple tools, including:
    * [Speed Limits](Speed Limits)
    * [Priority Signs](Priority Signs)
    * [Parking Restrictions](Parking Restrictions)
* It only affects user interface; it does not alter roadside props

### Interface

_Use these options to further customise the TM:PE user interface..._

#### Lock main menu button position

* If enabled, it locks the position of the button that shows/hides the [Toolbar](Toolbar). Otherwise, you can drag it around the screen.
* Has no effect if you've put the button in [Unified UI](Unified UI).

#### Lock main menu position

* If enabled, the position of the [Toolbar](Toolbar) cannot be changed. Otherwise, you can drag the toolbar around the screen.

#### Use UnifiedUI

> This option added in TM:PE 11.6.1. For earlier verisons, you can use the "Grabber" tool in Unified UI mod.

* When selected, the main menu button moves in to the [Unified UI](Unified UI) panel (requires [UnifiedUI mod](https://steamcommunity.com/sharedfiles/filedetails/?id=2255219025))

#### User interface scale

> TM:PE v11.1.1 replaced the **Compact main menu** option with this **UI Scaling** option. Subsequent versions made more panels respect the setting, including the [Speed Limits](Speed Limits) panel in v11.6.2. As of v11.6.1 TM:PE is also fully compatible with [UI Resolution mod](https://steamcommunity.com/sharedfiles/filedetails/?id=2487213155).

* You can use the slider to shrink or grow the size of UI panels
* The main menu button size is always set the same size as the vanilla Info Views button.
    * Unless you've moved it in to [Unified UI](Unified UI) in which case its size is controlled by UUI mod.

#### Window opacity

* Use this slider to set opacity of all TM:PE panels and windows, including the [Toolbar](Toolbar).
* Lower value = more transparent, higher value = more solid.

#### Overlay opacity

> The older **Overlay Transparency** slider was replaced by the new **Overlay Opacity** slider in TM:PE 11.6.5.1.

* Use this option to set the transparency of icon overlays that appear on the map
* Lower value = less transparent, higher value = more transparent.
* See also: [Overlays](Overlays) [settings](settings).

#### Enable tutorial messages

* If enabled, advisor tutorials will be shown the first time you use each tool on the [Toolbar](Toolbar)
* You can still click the "(?)" advisor help button in-game to show tutorials at any time
* See also: [Hints Panel](Hints Panel)

### Simulation

_Use these options to cusomise vehicle simulation detail and updates..._

#### Simulation accuracy

* Sets how much CPU time is allocated to process vehicles approaching junctions with:
    * [Timed Traffic Lights](Timed Traffic Lights)
    * [Junction Restrictions](Junction Restrictions)
    * [Priority Signs](Priority Signs)
* The higher the value, the more accurate the simulation but also the higher the CPU workload.
* High settings may cause lag and performance issues on older computers.

#### Apply AI changes right away

> This option was previously called **Customisations come in to effect immediately** and has been completely removed in TM:PE 11.6.5.1 (changes will always come in to effect immediately now).

* If enabled, the routes of _existing_ vehicles will be recalculated (from their current position) whenever you alter:
    * [Junction Restrictions](Junction Restrictions)
    * [Lane Arrows](Lane Arrows)
    * [Lane Connectors](Lane Connectors)
    * [Vehicle Restrictions](Vehicle Restrictions)
    * Notably, it doesn't apply to [Highway Junction Rules](Highway Junction Rules) or [Speed Limits](Speed Limits).
* If disabled, vehicles will continue along their route as normal without being notified of changes:
    * If they run in to a problem (eg. desired lane change no longer available), their route will be recalculated at that point.
    * Vehicles spawned _after_ you make changes will always be aware of those changes.

### Compatibility

_Use these options to customise the inbuilt mod compatibility checker..._

#### Scan for known incompatible mods on startup

* If enabled, TM:PE will scan for mods it knows are incompatible on startup
* If any are found, a panel will be shown asking you to unsubscribe them
* Conflicts will always be logged to the [[TMPE.log]] file, regardless of this setting

#### Ignore disabled mods

* If enabled, the startup scan will ignore any mods which are disabled
* Only applies if the **Scan for known incompatibel mods on startup** option is enabled

#### Notify me if there is an unexpected mod conflict

* If enabled, a warning will be shown if another mod overwrites or conflcits with TM:PE code
* Conflicts will always be logged to the [[TMPE.log]] file, regardless of this setting
* See also: [Incompatible Mods](Incompatible Mods)

## FAQ

#### Do these settings alter frame rate or cause lag?

> The **Simulation accuracy** can have a significant effect on in-game frame rate due to increased CPU workload, particularly on **Medium**, **High**, or **Very High** setting.

## See Also

[Settings](Settings):

* [Global Configuration](Global Configuration) - advanced fine-tuning of TM:PE

[TM:PE v10.x Wiki](https://tmpe.viathinksoft.com/wiki):

* [General options](https://tmpe.viathinksoft.com/wiki/index.php?title=Options#General)

[Issue Tracker](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues):

* <a href="https://github.com/CitiesSkylinesMods/TMPE/labels/SETTINGS"><img src="https://img.shields.io/github/issues/CitiesSkylinesMods/TMPE/SETTINGS?label=SETTINGS&logo=github" /></a>