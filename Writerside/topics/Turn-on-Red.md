# Turn On Red

> Verified: December 2021 - TM:PE 11.5.2

## Overview

Use these features to allow vehicles to perform [](Unprotected-Turns.md) while stopped at red [](Traffic-Lights.md):

* This can help reduce congestion on the road waiting at the red traffic lights
* However, it increases risk of accidents should traffic entering on a green light also wish to enter the same road

## Usage

> To use these features, both **Junction Restrictions** and **Turn on Red** must be enabled in [](Maintenance.md)
> in [](Settings.md).

There are two kinds of **Turn on Red**...

### Near-side turns

The main **Turn on Red** policy controls **near-side** unprotected turns.

A near-side turn means the first road on the same side that traffic drives on (eg. if traffic drives on the right, they
can turn right).

### Far-side turns

The secondary **One-way roads** policy, if enabled, automatically applies wherever the main **Turn on Red** policy is
applied; it enables far-side unprotected turns, but only between one-way roads (the vehicle must enter from, and exit
to, a one-way road).

A far-side turn means the first road on the opposite side that traffic drives on (eg. if traffic drives on the right,
they can turn left - but only if it's from/to one-way roads).

### Appicators

To set **city-wide defaults** for **near-side turns**:

1. Open [](Maintenance.md) in [](Settings.md)
2. Set **Vehicles may turn at red traffic lights** to the desired state

To set **junction-specific** overrides for **near-side turns**:

1. Open the [](Toolbar.md)
2. Select the [](Junction-Restrictions.md) tool  
   ![Junction Restrictions](btnJunctionRestrictions.png){style="inline"}
3. Select the junction to customise
4. Toggle the **Turn on Red** icons to the desired state (allow/deny)  
   ![Allow Turn Right on Red](picJunctionRestrictions_trorAllow.png){style="inline"}
   ![Deny Turn Right on Red](picJunctionRestrictions_trorDeny.png){style="inline"}

> The arrows on the icons above will point the other way if you're on a map where traffic drives on the left.

To also allow **far-side turns** between **one-way roads**:

1. Open [](Maintenance.md) in [](Settings.md)
2. Enable **Also apply to left & right turns between one-way streets** option
3. Any road where **Turn on Red** is enabled can now also make far-side turns between one-way roads

For best results, you should also create some [](Dedicated-Turning-Lanes.md) at the junctions where you allow **turn on
red**, otherwise traffic wishing to turn will get stuck behind traffic waiting to go straight on at the light.

## FAQ

> Q: Does it affect frame rate or cause lag?
>> A: It can do, particularly on larger cities with lots of traffic lights (even if most of them don't have turn on red, the
>> mod still has to check every frame).

> Q: Does **Turn on Red** work with normal traffic lights or does it need [](Timed-Traffic-Lights.md)?
>> A: It works on both normal and timed traffic lights.

> Q: Is there a way to make traffic lights indicate when vehicles can turn on red?
>> A: The traffic lights which come with vanilla game don't have any 'turn on red' signals.
>>
>> However, it's possible to achieve with some workshop assets and mods:
>> 1. Subscribe traffic light assets which include **turn on red** signals, for example:
>>   * [Clus' Traffic Lights](https://steamcommunity.com/sharedfiles/filedetails/?id=2032407437)
>>   * Are there any others? Edit this page and link them please :)
>> 2. Subscribe and enable
     either [Traffic Lights Replacer](https://steamcommunity.com/linkfilter/?url=https://tlr.cgameworld.com/documentation/pack-creation/) (
     right-hand traffic only)
     or [BOB, the tree and prop replacer](https://steamcommunity.com/sharedfiles/filedetails/?id=2197863850&searchtext=bob) (
     works on left- and right-hand traffic).
>> 3. Replace the traffic lights on the road with props that contain 'turn on red' signals. Whenever the traffic light
     goes red, the 'turn on red' signal will light up (note the green arrow on the left):  
>> ![Green arrow](picTurnOnRed_extraSection.png)

> Q: How to create traffic light props with 'turn on red' indicators?
>> A: Use
>> the [illumination texture](https://tlr.cgameworld.com/documentation/pack-creation/#how-to-make-traffic-light-props)
>> green light mask; it lights up when the traffic lights turn red.

> Q: Is there a way to do flashing yellow?
>> A: Not currently (if you know otherwise, let us know!).

## See also

[](Toolbar.md):

* [](Junction-Restrictions.md)
* [](Traffic-Lights.md)

[](Settings.md):

* [](Policies.md) - set city-wide defaults
* [](Maintenance.md) - enable/disable the features

Wikipedia:

* [](https://en.wikipedia.org/wiki/Turn_on_red)