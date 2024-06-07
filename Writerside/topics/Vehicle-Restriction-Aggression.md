# Vehicle Restriction Aggression

Use this feature to adjust the 'strength' of vehicle restrictions.

## Overview

When you set vehicle restrictions on roads or rails, the game interprets that as a penalty applied to those vehicles
when they are planning routes. The penalty deters restricted vehicles from using the route, but it doesn't prevent them
from using the route.

The **Vehicle Restriction Aggression** setting lets you set how harsh the penalty is. Use it wisely.

### Enable

Before you can use this feature, you must enable **Vehicle Restrictions** in the [](Maintenance.md).

### Customise

In the [](Policies.md), choose the desired **Vehicle Restriction Aggression** from the list (default setting is
**Medium**):

| Level  |  Penalty |
|--------|---------:|
| Low    |       10 |
| Medium |      100 |
| High   |     1000 |
| Strict | Infinity |

> For reference, in the vanilla game:
>
> * **Old Town** policy has a penalty of 5
> * **Heavy Traffic Ban** policy has a penalty of 10.

For beginners, we recommend using **Low** or **Medium** level. For advanced users, we recommend using the **Medium**
level, lol.

### Notes

The penalty influences how likely a vehicle is to obey or disobey your vehicle restrictions.

The **Strict** level virtually removes the restricted lanes from the road or rail network for that type of vehicle, even
those driven by [](Reckless-Drivers.md).

The penalty is cumulative from one road segment to the next; if you apply the restriction along an entire stretch of
road (multiple segments) it will stack up as the vehicle considers each subsequent segment on that road.

Due to technical reasons, path-finding stops if penalty costs get too high - the route is considered infeasible. **If
there's no alternate route to the destination, the vehicle won't even spawn!** You can mitigate this issue by providing
alternate routes, or reducing the aggression level.

Bear in mind that lots of other things add penalties to the routes, such as the policies mentioned above, but also
traffic lights, switching between modes of transport, toll booths and so on.

Commercial and industry buildings require road access for delivery vans and trucks. Service and emergency vehicles
require access to all kind of buildings. If you're using **High** or **Strict** aggression level, don't restrict the
outermost lanes of roads that those vehicles need to use, otherwise they won't be able to find a path and you'll get
problem notification bubbles.

## FAQ

**Does this affect frame rate or cause lag?**

> Very little; the game already has to process penalties during pathfinding. However, in very large cities, or on potato
> computers, the effect may be noticeable.

## See also

* [](Vehicle-Restrictions.md)