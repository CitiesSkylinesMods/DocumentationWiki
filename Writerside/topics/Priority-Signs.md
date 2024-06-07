# Priority Signs

> Verified: December 2021 - TM:PE 11.5.2

## Overview

Use priority signs to define who has right of way at junctions of roads, tracks, and level crossings.

This allows you to improve traffic flow on a busy route, at the expense of increased congestion/disruption to the other
routes at the junction. For more information, see [](Priority-Routes.md).

## Usage

Choose **Priority Signs** on the [](Toolbar.md):

![Priority Signs tool](https://imgur.com/Txc7Oqd.png)

> Button missing? Enable **Priority Signs** in [](Maintenance.md).

You can set a keyboard shortcut to activate the tool in the [Key Bindings](Keybinds.md) in [](Settings.md).

### Applicators

[](Select-a-Junction.md) to customise. You'll see a spot over each road entering the junction:

> If the icons don't appear, try moving/zooming the camera closer to selected junction

|                     Icon                     | Purpose                                                                                                                        |
|:--------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------------------|
| ![Empty spot](https://imgur.com/xLNF3ZD.png) | Placeholder for a priority sign. <br /><br /> Click to cycle through the signs (Priority > Yield > Stop > back to Priority...) |
|  ![Priority](https://imgur.com/P6OJc3b.png)  | **Priority** - traffic on this route has right of way when entering the junction.                                              |
|   ![Yield](https://imgur.com/97UNtLt.png)    | **Yield / Give Way** - traffic must slow down and only enter the junction if there are no priority vehicles waiting to enter.  |
|    ![Stop](https://imgur.com/QfXBx82.png)    | **Stop** - similar to Yield, but traffic must _always_ come to a complete stop even if the junction is clear.                  |
|                 (todo: icon)                 | **Reset** - clears all the priority signs at the junction.                                                                     |

> ProTip: Start by setting aside road to **Yield**; all empty spots will get **Priority** signs

### Shortcuts

The following shortcuts are applicable when the Priority Signs tool is active...

Selection:

* `Click a junction` - select the junction
    * Any previously selected junction will be deselected
    * You can now apply basic applicators
* `Esc` or `Right mouse click` - exit Priority Signs tool
    * This returns focus to the [](Toolbar.md) and enables its [](Adjust-Roads.md) mode.

Applicators:

> These apply to a selected or previously customised junction.

* `Click a priority sign icon` - cycle through priority signs (Priority > Yield > Stop > back to Priority...)

Overlays:

> Note: If you click with `Shift` and/or `Control` pressed, bulk applicators (see next section) will be applied.

* `Shift` - highlight route the mouse is over
    * It will try going "straight ahead" at junctions
    * On one-way roads, it will try and find roundabouts / semi-roundabouts
    * If no suitable ongoing route is found, the route will terminate at that junction
* `Control` - show persistent summary overlays for [](Junction-Restrictions.md) and [](Speed-Limits.md)

Bulk applicatators:

> These apply customisations along the highlighted route, which is shown as soon as you press `Shift` key (so you can
> check the route before clicking).

* `Shift`+`Click a segment` - apply priority signs to junctions along the route
    * Repeat the shortcut to cycle through various configurations of priority signs
* `Ctrl`+`Click a junction` - apply [](High-Priority-Roads.md) policies to that junction
    * Use the shortcut a second time to remove the customisations
* `Ctrl`+`Shift`+`Click a segment` - depends on the route:
    * If route is a roundabout (loop of one-way roads) or semi-roundabout:
        * Applies [](Roundabout-Policies.md)
    * If not a roundabout:
        * Applies [](High-Priority-Roads.md) policies
        * If a junction on roundabout is encountered, that junction will have [](Roundabout-Policies.md) applied
    * Use the shortcut a second time to remove the customisations

Camera:

* `Mouse wheel` - zoom in or out
    * If you zoom out too far, icons may disappear
* `PageDown` - underground view
* `PageUp` - overground view

### Overlays

While the tool is active, summary overlays show which junctions have been customised:

![](https://user-images.githubusercontent.com/1386719/145757519-a3dea2d4-5b14-4e8f-bf79-5e2f1e104943.png)

To see customisations for more distant roads and tracks, move the camera towards them. Depending on camera position, you
might need to zoom in a little. You can set the **Overlay Transparency** in [](General.md) in [](Settings.md).

When the tool is deactivated, overlays will be removed. You can enable a persistent summary overlay, which is visible
whenever the Toolbar is visible, in [Overlays](Overlays.md) in [](Settings.md).

### Icon Themes

Depending on your languge settings (see [](General.md) in [](Settings.md)), TM:PE can show locaised signs.

Currently available localisations:

* American (`en` / `us`) - these signs are shown by default should localised signs not be available
* Chinese (`zh`)
* English (`gb`) - pending [Issue #1251](https://github.com/CitiesSkylinesMods/TMPE/issues/1251)
* Welsh (`cy`) - pending [Issue #1251](https://github.com/CitiesSkylinesMods/TMPE/issues/1251)

### Refresh

When you make changes, only vehicles spawned _after_ that point will be aware of them.

To make existing vehicles aware of changes, enable **Customisations come in to effect immediately** in [](General.md)
in [](Settings.md). This may add some momentary lag on old potato computers or on big cities.

Alternatively, use the [Clear Traffic](Clear-Traffic.md) tool to delete all existing vehicles; it puts less strain on
CPU, so it's faster than the option above if you have old computer or big city.

## Notes

> **Confusion** causes hesitation. **Hesitation** causes delays. **Delays** cause traffic jams.

When traffic from multiple roads is entering a junction, there can be confusion over who gets to enter the junction
first. On low-volume junctions, it's usually not a problem. But as junctions get busier, that uncertainty starts to
cause traffic jams.

To overcome this issue, there is a general priority rule even when no priority signs are used. It depends on which side
of the road traffic drives on:

* Vehicles drive on Left? Traffic approaching from the right has priority.
* Vehicles drive on the Right? Traffic approaching from the left has priority.

However, these basic traffic rules aren't always sufficient. For exmaple, consider this junction:

(todo: image)

If there's vehiles waiting to enter from each road at the same time, who gets to go first? If _Jim Street_ is a busier
route than _Bob Street_, how do we ensure that _Jim_ gets priority over _Bob_? Priority signs remove the confusion:

(todo: image)

Now, taffic can flow much more freely along _Jim Street_ because it knows it has priority. Although _Bob Street_ has to
wait a bit longer, we've improved overall traffic flow for the majority of vehicles in the area.

## FAQ

#### Does this affect frame rate or cause lag?

> Yes, especially on large cities or old computers. Managing traffic at junctions is computationally expensive.

#### I Control + Clicked but nothing happened

> If the tool can't determine which is the main road vs. side roads, it won't do anything.

#### What happens if Yield or Stop traffic waits too long?

> If traffic on a Yield or Stop road is sat waiting too long, they'll eventually get annoyed and just drive in to the
> junction. If you notice this happening a lot, first try reconfiguring your priority signs to see if that hepls. If it's
> still not working, it's time to invest in some [](Traffic-Lights.md)!

#### I altered my roads but customisations didn't update

> If you make changes to your roads, it's difficult for TM:PE to determine what to do, so it does nothing. It's why we
> highlight junctions and routes when using the tools - you're actually deciding what to do and the highligts are just
> visual encouragement for you to do that work ;)

#### Some vehicles seem to ignore the rules!

> * [](Reckless-Drivers.md) ignore priority rules
> * Emergency vehicles, while responding to emergencies, can ignore the rules
> * Evacuation buses can ignore priority signs if **Evacuation buses may ignore traffic rules** is enabled
    in [](Policies.md) in [](Settings.md)
> * Traffic lights cause priority signs to be ignored unless **Vehicles follow priority rules at junctions with timed
    traffic lights** is enabled in [](Policies.md) in [](Settings.md)
> * If a road or rail segment entering the junction is too short, there isn't enough room for vehicles to slow down
    properly, and they will drive in to the junction before AI has time to stop them

## See Also

[](Toolbar.md):

* [](Adjust-Roads.md) - has similar bulk applicators
* [](Traffic-Lights.md)
* [](Junction-Restrictions.md)

[](Settings.md):

* [](Policies.md)
* [Overlays](Overlays.md)
* [Global Configuration](Global-Configuration.md) - contains fine-tuning parameters for priority signs

Guides:

* Roads:
    * [](Priority-Routes.md)
    * [](High-Priority-Roads.md)
    * [](Roundabouts.md)

[](Contributing.md):

* [](Priority-Signs-Icon-Themes.md) - localise icons for priority signs

[Issue Tracker](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues):

* <a href="https://github.com/CitiesSkylinesMods/TMPE/labels/PRIORITY SIGNS"><img alt="Issues" src="https://img.shields.io/github/issues/CitiesSkylinesMods/TMPE/PRIORITY SIGNS?label=PRIORITY SIGNS%26logo=github" /></a>