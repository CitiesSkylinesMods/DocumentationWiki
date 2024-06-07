# Highway Junction Rules
> Under construction

Use this feature to make highway traffic more realistic.

### Overview

This feature implements two key changes to the way your highways work:

1. Vehicles can only change one lane at a time (emergency vehicles are exempt from this rule)
2. Vehicles are forced to stay in their lane when entering or exiting the highway

### Enable

Activate **Enable highway specific lane merging/splitting rules** in the [](Policies.md) in [](Settings.md).

### Customise

Once the feature is enabled, it applies to all highways automatically. However, for best results you should make the following additional customisations...

**Lane parity**

At junctions, the number of incoming lanes should be equal to the number of outgoing lanes:

(todo: images)

In the image above:

* The junction on the left is optimal - 4 lanes enter, and 4 lanes leave.
* The junction on the right is sub-optimal - 4 lanes enter, but only 3 lanes leave. This will impair traffic flow.

The same applies to highway exits. For example, if a 3 lane highway has a 1 lane exit ramp, the remaining highway should only have 2 lanes.

**Speed parity**

On highway junctions:

* **Entries** should have **acceleration lanes** which allow traffic to **speed up** as it joins the highway
* **Exits** should have **deceleration lanes** which allow vehicles to **slow down** as they leave the highway

These speed changes help avoid collisions between traffic travelling at different speeds.

To do this, use the [](Speed-Limits.md) tool to create a **speed gradient** along the highway ramp. The end nearest the highway should be fastest, and the end nearest your normal road system should be slower.

(todo: image)

As vehicles drive up an entry ramp, their speed should increase. As they drive down an exit ramp, their speed should decrease.

## FAQ

**Does this reduce frame rate or cause lag?**
> Very little.

**I've enabled the setting but nothing seems to change**
> Due to the large amount of traffic on highways, a decision was made not to instantly update it (it would cause huge numbers of path finder operations). So you'll have to wait a while for new vehicles to spawn to see the effects. Alternatively, you could [Clear Traffic](Clear-Traffic.md) to remove all the existing traffic that's using the old rules.

**Why can't I use the [](Lane-Arrows.md) tool?**
> When highway rules are active, the lane arrows are automatically set and can't be changed. However, you can still use [](Lane-Connectors.md) and/or the [](Lane Changes) features if you need to apply some further customisations.

**Vanilla highway roads are somewhat limited, what are the alternatives?**
> There are many highway, expressway, motorway, freeway, and national road assets in the Steam Workshop; notably, many have fully rendered tunnels and asymmetric variants for entry/exit lanes. Some of our favourites are:
> * [Vanilla+ Roads: Highways](https://steamcommunity.com/workshop/filedetails/?id=2124252245) (these match perfectly the style of vanilla highways)
> * [Highway over a concrete wall](https://steamcommunity.com/workshop/filedetails/?id=1336987320)
> * [Concrete Highways](https://steamcommunity.com/workshop/filedetails/?id=1888581095)
> * [中国高速 Langshao China Expressway](https://steamcommunity.com/workshop/filedetails/?id=1292187026)
> * [CSUR](https://steamcommunity.com/workshop/filedetails/?id=1423096565) (advanced users only!)
> * [UK Road Project: Motorways](https://steamcommunity.com/sharedfiles/filedetails/?id=1718180429)
> * [Euro Highways](https://steamcommunity.com/sharedfiles/filedetails/?id=2682923095)
> * [Mike's Expressways](https://steamcommunity.com/workshop/filedetails/?id=2536122197)
> * [Hangang Expressway](https://steamcommunity.com/workshop/filedetails/?id=2017707792)
> * [North American Freeways](https://steamcommunity.com/workshop/filedetails/?id=2277553422)

## See Also

[](Toolbar.md):

* [](Lane-Arrows.md)
* [](Lane-Connectors.md)
* [](Junction-Restrictions.md)

[](Settings.md):

* [](Policies.md)

Guides:

* [Dedicated Turning Lanes](Dedicated Turning Lanes)
* [Heavy Truck Highway Rules](Heavy Truck Highway Rules)
* [](High Priority Roads)
* [](Roundabout Policies)