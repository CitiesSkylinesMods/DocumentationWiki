![Untitled](https://user-images.githubusercontent.com/26344691/81202134-d2269400-8fce-11ea-9ec2-80e2d29b0ae7.png)

Setting up a roundabout in Traffic manager can be tricky. For your convenience TMPE offers ways to quickly setup a roundabout by setting the following rules (can be modified in [policies](Policies.md) [settings](Settings.md)) (see screenshot above):
* ban pedestrian crossing to the center of the roundabout (and optionally on the branches too)
* cars entering the roundabout must yield and keep clear of blocked junctions.
* cars on the roundabout enter blocked junction.
* dedicated exit lane on the roundabout.
* stay in lane on the roundabout.
* do not change lanes on the branches **too close** to the roundabout (this is useful if you have built you roundabout using roundabout builder and have a node that is too close to the roundabout).
* In the case of highway junction, "switch lanes while going through junction" rule is applied as a precaution against highway rules messing up your roundabout.
* parking bans on the roundabout and its branches (coming soon).
* put speed limit on the roundabout based on the size of the roundabout (coming soon).

### Hot key
* pressing `Control+Shift+Click` on roundabout applies all the rules above.
* pressing `Control+Shift+Click` again undoes all those changes (coming soon)
* For more control you can use [Adjust Roads](Adjust Roads) panel. This is particularly helpful in setting up magic roundabouts.
* Hold control to see persistent overlay of all relevant traffic rules across different TMPE tools.

### Semi Roundabout
Roundabout is a  one way road that forms a loop. If the oneway road does not form a loop, it is considered a semi roundabout. The traffic rules are similar except there is no dedicated exit lane. You can setup a semi-roundabout using:
* `Control+Shift+Click` on the semi-roundabout
* use [Adjust Roads](Adjust Roads) panel
* `Control+Click` on each entry of the roundabout.

![screenshot semi roundabout](https://user-images.githubusercontent.com/26344691/81376912-17e97680-910d-11ea-9279-fa71f263fa71.png)

### Notes
* adding the rule "switch lanes while going through junction" can cause traffic jam on the roundabout (except when highway rules are enabled). Its better that cars switch lanes before they arrive at roundabout so that they don't get in the way of upcoming cars.
* reducing speed limit on the roundabout might reduce car accidents in the real world, but does not reduce traffic jams in Cities skylines.

### See also:
 - Use [Hide crossings](https://steamcommunity.com/sharedfiles/filedetails/?id=1934023593) mod to hide zebra crossings on the roundabout (as in the screenshot)
 - Use [Roundabout builder](https://steamcommunity.com/sharedfiles/filedetails/?id=1625704117) mod to build roundabouts
 - Use [Pedestrian bridge builder](https://steamcommunity.com/sharedfiles/filedetails/?id=2030755273) mod to build pedestrian bridges over the roundabout with one click (as in the screenshot)