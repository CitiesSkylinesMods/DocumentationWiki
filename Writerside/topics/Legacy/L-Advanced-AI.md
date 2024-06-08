# 👴 Advanced AI

> 👴 This article's content is old, copied from the original Wiki at https://tmpe.viathinksoft.com/wiki/

## Introduction

The Advanced Vehicle AI is a feature that integrates into the [](L-Modified-Path-Finding.md)
algorithm that is shipped with TM:PE. The main intentions are

1. to improve overall road usage,
2. to spread traffic to the available lanes more evenly, and
3. to prevent unnecessary lane changes from happening too frequently.

When activated, the AI calculates the route a vehicle will take just before the moment it
starts driving. The traffic situation at this moment is taken into consideration while the
route is being planned. However, once a path is established and the vehicle is en route no
further adaptations are made. Read [](L-Dynamic-Lane-Selection.md) to learn how to enable real-time
route adaptations.

## Road usage optimization

In the background TM:PE constantly observes traffic volumes and average speeds for each
built road segment and for each direction. The Advanced Vehicle AI uses this information
to construct speed-optimal paths. Like in every ordinary path-finding algorithm, each road
segment gets a unique cost assigned that represents the estimated time for an average vehicle
to traverse it. Based on this notion, roads that optimize the estimated traversal time are
favored by the algorithm.

### Prevention of feedback effects

The algorithm incorporates mechanisms to avoid feedback effects. These effects can occur when
congested road segments are first avoided by the AI but then lead to secondary congestions
because new vehicles are forced to take detours in order to avoid the first congested road.
If no countermeasures were taken secondary congestions in turn would again lead to congestion
of the first road in question.

During the calculation of the cost factors that are derived from traffic measurements a
randomized portion is added to/subtracted from the taken measurements to prevent those kinds of effects.

## Lane spread optimization

During path-finding at every :term:`junction` and highway :term:`transition` that the vehicle may traverse
a new randomized value is generated. This value determines the lane that the vehicle favors
the most in order to traverse the respective road segments. This mechanism allows for a
better spread of vehicles among the available lanes.

## Lane change restrictions

The AI calculates up to two cost factors for every considered lane change.

1. The first (base) cost factor amounts to a value that is proportional to the number of lanes to change.
2. The second cost factor is added upon the first factor. It is set to a non-zero value if a
   multi-lane change is being considered during path-finding.

Both cost factors control the tendency of vehicles to change lanes. However, their values are not
necessarily proportional to the probability of a lane change to occur on a given road segment.

> See also: [](L-Modified-Path-Finding.md)
 