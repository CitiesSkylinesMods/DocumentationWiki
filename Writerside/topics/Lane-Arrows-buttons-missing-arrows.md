# Lane Arrows Buttons Missing Arrows
> Article verified: October 2019

## Symptom

> This issue only affects TM:PE versions 10.21.1 and earlier

* When using the [](Lane-Arrows.md) tool, the arrows are missing from buttons like so:

![Missing arrows](picLegacyLaneArrows_bug.png)

## Cause

This issue can occur on older graphics cards when using Open GL graphics mode.

For background information, see [this topic](https://steamcommunity.com/workshop/filedetails/discussion/583429740/2944710017702561668/).

## Solution

In Steam, remove the `-force-glcore` [launch option](https://steamcommunity.com/sharedfiles/filedetails/?id=466981085).

If you still have general issues with graphics, try the following:

1. Update your graphics drivers direct from graphics card vendor website
2. Add the `-force-d3d9` launch option (forces DirectX 9 graphics mode)

## Was it Fixed?

If not, please let us know: [](Report-a-Bug.md)

Other issues? See: [](Troubleshooting.md)