# Lane Arithmetic

Answer provided on Reddit by /u/quick20minadventure:

> The number of incoming lanes and outgoing lanes should be equal at all highway junctions.

So, cities skylines has a complex, but not complex enough AI for cars. There are a couple of problems with it, like...

1. The algorithm decides the path from start to finish and the path includes lane details as well. So, the car will
   follow the exact path. Even if there are 5 lanes next to them going to exact the same location, they'll not use it.

2. The algorithm also results in the outer lane being used most often in the highways, because a) almost all exits on
   highways are on the outer side and b) cars get into the lane where they need to exit as soon as possible as per
   algorithm. So, they'll get ready to turn right 1000 miles before their exit comes, which is unrealistic. Basically
   everyone will be using outer most lane if all your exits are on that lane.

The solution to this problem is to make sure that all your turning lanes are going to be dedicated turning lanes. That
is, you can not stay in the outer lane and not turn. Dedicated turning lanes work really well with this game's AI.

Another aspect is merging. If you have 2 lanes merging with 2 lanes, it should be 4 lane road. Otherwise, cars will have
to wait for traffic to pass before they can start moving. This is simple enough concept, that is applicable in real life
as well.

These two combined are typically called 'lane mathematics' which can be summarized as:
**The number of incoming lanes and outgoing lanes should be equal at all highway junctions.**

This will make sure that the game automatically generates dedicated turning lanes and your merging is very smooth and
cars don't have to wait before they can move.

You don't always need to follow this, and you can use TMPE which allows for two good options.

1. Individual driving style which means people will get ready to turn/move to turning lane at different times (This
   happens by changing the routes that are decided at the start of the journey)

2. Dynamic lane selection, which means if traffic is jammed, people will change lanes to go ahead, their routes are
   dynamic.

