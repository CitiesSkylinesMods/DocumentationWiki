> Article verified: June 2019

# Symptom

* Bus routes are taking huge detours rather than shortest route
* Bus routes aren't taking advantage of bus lanes

# Cause

There are numerous causes for these symptoms, including [Broken Road Assets](Broken Road Assets), bad road customisations, your [Settings](Settings.md), or even [Incompatible Mods](Incompatible Mods).

We are investigating two possible bugs in TM:PE:

* [#19](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues/19): Vehicles not crossing road to enter building on other side (eg. bus terminals)
* [#30](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues/30): Inner bus lane not being used

# Solution

Try these things in this order:

1. Unsubscribe any roads on this list: [Broken Road Assets](Broken Road Assets).
2. In [Policies](Policies.md) settings, set **Vehicle restrictions aggression** to **Low**.
    * Did that fix it? If so, make sure there aren't any [vehicle restrictions](Vehicle-Restrictions.md) blocking the desired route
    * Note: There are other things it could have fixed, which you should also check, see: [Vehicle Restriction Aggression](Vehicle Restriction Aggression)
3. Check the [Speed Limits](Speed-Limits.md) applied to bus lanes and adjacent normal road lanes:
    * If the normal lanes are faster, busses will prefer them
    * Try making bus lanes +10 faster than the normal road lanes
4. Busses might need more places to change lanes in order to reach a bus lane:
    * In [Policies](Policies.md) settings, enable **Busses may ignore lane arrows**
    * At junctions along the route:
        * If you use [Lane Connectors](Lane-Connectors.md), make sure they facilitate the required lane changes
        * If you use [Timed Traffic Lights](Timed-Traffic-Lights.md), make sure they have 'green time' for the required route
        * In [Junction Restrictions](Junction-Restrictions.md), enable **Vehicles going straight on may change lanes** (you can set this as default for all junctions in [Policies](Policies.md) settings)
    * If the bus still can't reach the desired lane, see: [Flexible Bus Routing](Flexible Bus Routing)

# Fixed?

If not, please let us know: [Report a Bug](Report a Bug)

Other problems? See: [Troubleshooting](Troubleshooting)