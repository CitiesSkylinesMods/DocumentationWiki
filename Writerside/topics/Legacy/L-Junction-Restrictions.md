# 👴 Junction Restrictions

> 👴 This article's content is old, copied from the original Wiki at https://tmpe.viathinksoft.com/wiki/

## Introduction

With the Junction restrictions tool you can set up certain rules governing vehicle behavior at selected junctions. These
options are:

* Allow/disallow lane changing for vehicles going straight on: By default, vehicles stay on their lane while crossing
  the junction. By activating this option, you allow vehicles going straight (that means they neither turn left nor
  right) to change lanes while crossing the junction.
* Allow/disallow U-turns: If activated, vehicles approaching the junction from the selected segment may turn around.
  U-turns are only performed on lanes having a left arrow (right-hand traffic) / right arrow (left-hand traffic)
* Allow/disallow vehicles to enter a blocked junction: This option is useful e.g. if the next road segment after a
  junction is very short. Without activating this option, vehicles do not enter the junction if the road behind it is
  blocked. By activating this option you disable this check. Vehicles will then enter the junction even if the road
  behind is blocked by traffic.
* Allow/disallow pedestrians to cross the street: By default, pedestrians may cross the road at every junction. This
  tool allows you to prohibit them from doing so. Note that this tool does not actually remove the crosswalk texture
  since this is technically not possible.
* Allow/disallow turn-on-red (only available for junctions with traffic lights): Activate this option to allow vehicles
  to yield at red traffic lights when turning right (right-hand traffic) / left (left-hand traffic). When two one-way
  streets cross (one incoming and one outgoing one-way) this option is also available for non-preferred turns (left turns
  for right-hand traffic / right turns for left-hand traffic).

## Setup

Follow these steps:

1. Click on the ![](btnMain.png){style="inline"} button.
2. Click on the ![](btnJunctionRestrictions.png){style="inline"} button.
3. Click on the junction that you want to manage.
4. Click on the appropriate icon to enable/disable one of the features described above.

![](picJunctionRestrictions_junction.png){style="block"}
_Visible overlay after a junction was selected_

## Icons

The choices explained above are depicted by following symbols:

| Icon                              |                         Description                         |
|:----------------------------------|:-----------------------------------------------------------:|
| ![](picLegacyJR_laneChange.png)   | Allow/disallow lane changing for vehicles going straight on |        
| ![](picLegacyJR_uTurn.png)        |                   Allow/disallow u-turns                    |        
| ![](picLegacyJR_blockedEnter.png) |     Allow/disallow vehicles to enter a blocked junction     |        
| ![](picLegacyJR_crossing.png)     |       Allow/disallow pedestrians to cross the street        |        
| ![](picLegacyJR_laneChange.png)   |           Allow/disallow vehicles to turn on red            |        

> ☝️ All settings except the third and last one (allow vehicles to enter a blocked junction, allow
> vehicles to turn on red) affect newly spawned vehicles/pedestrians only unless the appropriate
> option is activated (see section Options & advanced features for further information). This means
> it may take some minutes before all vehicles and pedestrians correctly obey your set restrictions.

> ☝️ When you create a U-turn connection with the lane connector tool U-turns are automatically
> allowed at the respecting road segment. Clicking on the U-turn symbol does not have any effect in
> this case. You need to remove the U-turn lane connection first in order to disallow U-turns at the segment.

> ☝️ [](Reckless-Drivers.md) ignore junction restrictions.

## See Also

[](L-Vehicle-Routing.md)
