# Broken transport routes
> Article verified: June 2019

## Symptoms

Any of the following:

* After loading a game, routes are broken
* When altering my roads or rails, routes break
* Stops appearing in weird places
* Unable to remove broken stops

## Causes

Certain things cause the game to recalculate transport routes:

* Add or bulldoze roads or tracks
    * This includes creating new junctions, using upgrade tool to change type of road/track, etc.
* Add or bulldoze a station
* Using 'Move It' mod to alter buildings, roads or tracks
* Disasters that destroy buildings, roads or tracks
* Probably a bunch of other stuff too

When any of those happen, the game will check any bus, tram, monorail, train and metro routes in the vicinity to see if they are still viable. If not, the game will make a "best guess" decision as to how to alter the route, for example it might route a bus (and bus stops) down a different road.

Click the image below to watch a YouTube video of the game automatically re-routing bus lines:

[![Game reroutes a bus line](picBrokenTransportRoutes_youtube.jpg)](http://www.youtube.com/watch?v=hq_of4ahRAs)

Sometimes this process goes horribly wrong, or no viable alternate route can be found. In particular, if you bulldoze a road or station that contains a stop, that stop might "orphaned" which prevents makes it impossible to move for both you and the game.

## Solutions / Workarounds

Usually moving the stops either side of the broken part of the route will fix the issue:

* Open the transport menu and select the type of transport associated with the broken route
* Choose the 'add stop' tool that you used when initially creating the route
* You can left-click and drag existing stops to move them, this usually updates the route
    * You might need to do this with stops either side of the broken part of the route
* You can delete unwanted stops by right-clicking them

If a route is so horribly broken that it's beyond repair, you can delete it as follows:

* Go in to the public transport info view
* A colorful panel appears showing the different transport types and their usage
* Click the magnifying glass for the transport type that's got the problem
* You get a list of routes for that transport type -> delete the broken route

If you have some time, click the image below for a YouTube video showing how to deal with broken routes:

[![Fixing routes](picFixingRoutes_youtube.jpg)](http://www.youtube.com/watch?v=V40FuyQywGs)

Sometimes it's caused by a broken node (vanilla game bug):

* Subscribe and enable [Broken Node Detector](https://steamcommunity.com/sharedfiles/filedetails/?id=1777173984)
* Read mod description on the workshop page for the mod to learn how to use it

## Was it Fixed?

If not, please let us know: [](Report-a-Bug.md)

Other issues? See: [](Troubleshooting.md)