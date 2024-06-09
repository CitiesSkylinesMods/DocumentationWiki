# 👴 Junction and Transition Routing

> 👴 This article's content is old, copied from the original Wiki at https://tmpe.viathinksoft.com/wiki/

## Introduction

When TM:PE is active it modifies the way vehicles traverse junctions in order

    to improve throughput and traffic distribution and
    to increase realism.

## Terminology

In order to understand how TM:PE's lane transition schemes work, you must first understand what the terms [inner & outer
lanes, junctions](Nodes,-Segments,-Lanes.md), and transitions mean in this context.

## Lane Transition Schemes

TM:PE implements five different lane transition schemes for junctions and transitions:

* One-to-one,
* Innermost lane splits,
* Symmetric split,
* Innermost lanes merge, and
* Crisscross merge.

They are explained in the following sections.

### One To One

The simplest transition scheme is called one-to-one. It applies only at junctions where the amount of incoming lanes
equals the amount of outgoing lanes for a certain direction. The image below illustrates a situation where this is the
case.

![](picLegacyJunctionTransitionRouting_1to1.png){style="block"}
_One-to-one lane transition scheme_

With one-to-one lane mapping each incoming lane feeds exactly one outgoing lane.

### Inner Lane Splits

At junctions where there exist more outgoing lanes than incoming lanes for a certain direction and the number of
outgoing lanes is not divisible by the number of incoming lanes the innermost lane splits transition scheme applies. The
image below illustrates a situation where this is the case.

![Inner lane splits](picLegacyJunctionTransitionRouting_innerLaneSplits.png){style="block"}
_Innermost lane splits lane transition scheme_

The innermost lane splits scheme first applies one-to-one matching to all lanes except for the innermost lane (green &
red arrow). The remaining lane (light blue arrow) is then divided up such that it feeds all remaining outgoing.

### Symmetric Split

The symmetric split transition scheme is applied to junctions where the number of outgoing lanes is divisible by the
number of incoming lanes for a certain direction. The image below illustrates a situation where this is the case.

![](picLegacyJunctionTransitionRouting_symmetricSplit.png){style="block"}
_Symmetric split lane transition scheme_

When the symmetric split scheme is selected all incoming lanes feed an equal number of outgoing lanes. Incoming lanes
are divided up evenly to all outgoing lanes in a certain direction.

### Innermost Lanes Merge

At junctions where there exist less outgoing lanes than incoming lanes for a certain direction the innermost lanes merge
transition scheme applies. The image below illustrates a situation where this is the case.

![](picLegacyJunctionTransitionRouting_innermostMerge.png){style="block"}
_Innermost lanes merge lane transition scheme_

Starting with the outermost incoming lane the one-to-one scheme is applied until every outgoing lane is mapped to
exactly one incoming lane. The remaining incoming lanes are then mapped to the innermost outgoing lane.

### Crisscross Merge

The crisscross merge lane transition scheme is applied at highway transitions only. Depending on the number of incoming
and outgoing lanes, lanes either merge

* in a zig-zag style pattern or
* in a second, two-phased pattern where central lanes proceed straight on and lanes at the edges merge towards the
  center.

The images below illustrate all current possible highway transitions where the criss-cross scheme is being applied.

![](picLegacyJunctionTransitionRouting_crisscross1.png){style="block"}
_Crisscross lane transition scheme for highway transitions (3-to-2, 4-to-2, 4-to-3, 5-to-2, 5-to-3, and 5-to-4 lane
transition points)_

![](picLegacyJunctionTransitionRouting_crisscross2.png){style="block"}
_Crisscross lane transition scheme for highway transitions (6-to-2, 6-to-3, 6-to-4, and 6-to-5 lane transition points)_

The two merging types are applied following circumstances:

* The zigzag merging scheme is applied if the number of incoming lanes is odd and the number of outgoing lanes is even,
  or vice versa.
* The two-phased merging scheme is applied if the number of incoming and the number outgoing lanes are both odd or even.

## See Also

[](L-Vehicle-Routing.md)
