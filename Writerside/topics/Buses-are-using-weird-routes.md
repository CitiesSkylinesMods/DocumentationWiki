# Buses are Taking Weird Routes

> Article verified: June 2019

## Symptom

* Bus routes are taking huge detours rather than the shortest route
* Bus routes aren't taking advantage of bus lanes

## Cause

There are numerous causes for these symptoms, including [](Broken-Road-Assets.md), bad road customizations,
your [](Settings.md), or even [](Incompatible-Mods.md).

We are investigating two possible bugs in TM:PE:

* [#19](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues/19): Vehicles not
  crossing road to enter building on other side (e.g. bus terminals)
* [#30](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues/30): Inner bus lane not
  being used

## Solution

Try these things in this order:

1. Unsubscribe any roads on this list: [](Broken-Road-Assets.md).
2. In [](Policies.md), set **Vehicle restrictions aggression** to **Low**.
    * Did that fix it? If so, make sure there aren't any [](Vehicle-Restrictions.md) blocking the desired route
    * Note: There are other things it could have fixed, which you should also check,
      see: [](Vehicle-Restriction-Aggression.md)
3. Check the [](Speed-Limits.md) applied to bus lanes and adjacent normal road lanes:
    * If the normal lanes are faster, buses will prefer them
    * Try making bus lanes +10 faster than the normal road lanes
4. Buses might need more places to change lanes in order to reach a bus lane:
    * In [](Policies.md), enable **Busses may ignore lane arrows**
    * At junctions along the route:
        * If you use [](Lane-Connectors.md), make sure they facilitate the required lane changes
        * If you use [](Timed-Traffic-Lights.md), make sure they have 'green time' for the required route
        * In [](Junction-Restrictions.md), enable **Vehicles going straight on may change lanes** (you can set this as
          default for all junctions in [](Policies.md))
    * If the bus still can't reach the desired lane, see: [](Flexible-Bus-Routing.md)

## Was it Fixed?

If not, please let us know: [](Report-a-Bug.md)

Other problems? See: [](Troubleshooting.md)