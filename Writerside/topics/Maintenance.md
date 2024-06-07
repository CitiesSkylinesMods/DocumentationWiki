# Maintenance Settings

> Verified: March 2022 - TM:PE 11.6.5.1

[](Settings.md): [](General.md) | [](Gameplay.md)
| [](Policies.md) | [Overlays](Overlays.md) | **Maintenance**
| [Key Bindings](Keybinds.md)

## Overview

Use these [](Settings.md) to perform some maintenance tasks, and also to enable or disable [](Toolbar.md)
features.

## Settings

### Tools

_These are just some general tools you may find useful on occasion..._

#### Reset stuck cims and vehicles

* Finds then removes any 'stuck' cims and vehicles, and gives them a straight "ignore everything" path to their
  destination, so they can safely reach it
* A less-destructive alternative to the [Clear Traffic](Clear-Traffic.md) tool

#### Remove all existing traffic lights

* Removes all traffic lights on the map
* To prevent more being automatically added, _disable_ **Automatically add traffic lights if applicable**
  in [](Policies.md)

#### Reset speed limits

> This option currently only appears in `DEBUG` builds of the mod tht developers use.

* Reverts all speed limits to their default values

### Activated features

_Use these options to enable or disable TM:PE features that appear on the main [](Toolbar.md)..._

> Mod features will automatically be enabled if you enable another option that requires them (such
> as [Overlays](Overlays.md) or [](Policies.md)). Likewise, disabling a mod feature will automatically disable any
> options that rely on that feature.

* [](Priority-Signs.md)
* [](Timed-Traffic-Lights.md) - this option is not available in asset editors, but is available in
  map/scenario editor
* [](Speed-Limits.md)
* [](Vehicle-Restrictions.md)
* [](Parking-Restrictions.md)
* [](Junction-Restrictions.md)
* [](Lane-Connectors.md)

### Despawn

_Use these options to immediately despawn one or more categories of vehicles in your city..._

> This group of options only appears in-game. It won't appear if you access the options screen from Main Menu or from
> within Content Editors.

* Select what you want to despawn, then click the `Despawn` button.
* There is some overlap between categories; for example `Road Vehicles` includes `Service vehicles` and
  some `Public Transport vehicles`, etc.
* See also: [Clear Traffic](Clear-Traffic.md) and [Toggle Despawn](Toggle-Despawn.md)

### Configuration

> Note: Global options in [](General.md) in [](Settings.md) don't currently update when global config is
> reloaded/reset.

_Use these buttons to update the global configuration..._

#### Reload global configuration

* Reloads [Global Configuration](Global-Configuration.md) file from disk
* Useful if you make changes while the game is running

#### Reset global configuration

* Reset [Global Configuration](Global-Configuration.md) file to default values
* Deleting the config file has the same effect

## FAQ

#### Do these settings affect frame rate or cause lag?

> * If you are struggling with low frame rate or lag, disabling unused features could help improve performance
> * There are many other factors (assets, mods, page file, etc.) that reduce frame rate or cause lag; for more
    information, see: [Performance Tuning Guide](https://steamcommunity.com/sharedfiles/filedetails/?id=465790009)

> * The **Activated features** can cause some lag, as each tool adds a little extra workload to the game; see the
    documentation pages of the tools for more details.

#### Does disabling a feature remove settings of that feature?

> * No. Settings will be retained and will still be stored in save games. If you later re-enable the tool, it's previous
    settings will continue to work as before.

#### Some features can't be disabled?

> Some features are just customisations of the vanilla game functionality and are always enabled:
> * [Toggle traffic lights](Toggle-Traffic-Lights.md)
> * [](Lane-Arrows.md)
> * [Toggle despawn](Toggle-Despawn.md)
> * [Clear traffic](Clear-Traffic.md)

## See also

[](Settings.md):

* [Global Configuration](Global-Configuration.md)

Old [TM:PE v10.x Wiki](https://tmpe.viathinksoft.com/wiki):

* [Maintenance options](https://tmpe.viathinksoft.com/wiki/index.php?title=Options#Maintenance)

[Issue Tracker](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues):

* <a href="https://github.com/CitiesSkylinesMods/TMPE/labels/SETTINGS"><img alt="Issues" src="https://img.shields.io/github/issues/CitiesSkylinesMods/TMPE/SETTINGS?label=SETTINGS%26logo=github" /></a>
