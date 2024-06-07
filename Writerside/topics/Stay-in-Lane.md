# Stay In Lane

### Usage

to use the stay-in-lane feature: Select the [](Lane-Connectors.md) tool, select a node and then press the stay-in-lane
hotkey (Default Hotkey for stay in lane is `CTRL+S` but hotkey can be modified in options). This cycles through
the following configurations:

1. All lanes in both directions can go directly ahead only
2. (2 way road only) Lanes in one direction go directly ahead, the other direction has its connectors removed
3. (2 way road only) Like 2 above, but with the opposite direction
4. All lane connections are removed

### limitation

Only nodes with 4 or fewer segments are supported.

### Application:

The pictures bellow show several scenarios in which stay in lane is applicable.

### Node with two segments:

![Screenshot (1018)](picStayInLane_nodeTwoSegments.png)

### Split segment:

![Screenshot (1024)](picStayInLane_splitSegment.png)

### Alley to main road/highway intersection:

![Screenshot (1025)](picStayInLane_alley.png)

### highway ramps:

![Screenshot (1019)](picStayInLane_highwayRamp.png)

### highway roundabout Overpass

![Screenshot (1023)](picStayInLane_overpass.png)

### Connected from inner side

![Screenshot (1028)](picStayInLane_fromInnerSide.png)
