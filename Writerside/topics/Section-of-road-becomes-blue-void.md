# Section of Road Becomes Blue Void

> Verified: March 2022 - TM:PE 11.6.5.1

## Symptom

A section of road turns in to blue void, usually while defining the road in **Traffic Routes > Adjust Roads** info view.

![Image](https://i.imgur.com/x8mzV89.png)

> Similar issue (not caused by "Adjust Roads" info view): [](Blue-void-showing-near-roads.md)

## Cause

This issue is very rare, and actual causes aren't yet known. It's not caused by TM:PE (testing with and without TM:PE
made no difference).

From initial experimentations, this issue seems to be caused by some combination of the following:

* Roads with very large numbers of tress/props (such as UK Roads Revived: Rural Roads)
* Roads that are outside the central 25 Tile area
* Roads that are high-up on a mountain
* Blue void might start near a junction where one of the roads consists only of a very tiny segment of road

## Solution

In Routes info view > Adjust Roads tab, examine the road. If one end is blue void grab the green circle at the end of
the 'road path' line and drag it to where the road is no longer blue void.

![Image](https://i.imgur.com/ONBX7y0.png)

That _should_ sort it out, as shown in image above. Sometimes bulldozing / upgrading / replacing the road will fix it
too.

## Was it Fixed?

If not, see if any of these guides help:

* [](Blue-void-showing-near-roads.md) - also applies to paths, tracks, etc
* [](Blue-void-roads-or-tracks.md) - when placing buildings that contain road/track
* [](Road-texture-flickers,-or-terrain-showing-through-roads.md)

Other issues? See: [](Troubleshooting.md)