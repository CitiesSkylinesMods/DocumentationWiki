# 👴 Parking AI

> 👴 This article's content is old, copied from the original Wiki at
> https://tmpe.viathinksoft.com/wiki/index.php?title=Parking_AI

## Introduction

You may have noticed that cims sometimes spawn a car at their current position or that cars suddenly disappear (
especially noticeable at public transport stations). This (mis)behavior is also known as "using pocket cars". The reason
is that cims do not care much about parking spaces. If a free parking space lies in the close vicinity where cims want
to get rid of their car everything is fine. But the base game does not come anywhere near real-life behavior when
talking about parking and returning to/using a parked vehicle. This is the point where the Parking AI comes into play.

Instead of having a ready-to-use car in their pockets, after enabling the checkbox Enable more realistic parking cims
ordinarily try to park their car before reaching their target (up to 10 times, then they give up). If cims decide to use
their car to go somewhere they also first walk to their parked car, enter it and then continue their journey (In the
base game they would only enter their car if it coincidentally lied along their designated route).

## Getting a new car

The game does not know functional car dealerships (so sad!). In the base game

* spawning a pocket car, and
* originating from an outside connection

are the only possible ways to get a brand-new car. Since spawning a pocket car is not an option any more, after
activating the Parking AI new cars are instead spawned on free parking spaces near the starting position.

## Parking space demand

The traffic info view (click on the ![](btnTrafficInfoView.png){style="inline"} button) assists you in building the
right amount of parking lots/garages. It shows where additional parking spaces are required (buildings with high parking
space demand are highlighted with red color).

![](picLegacyParkingAI_demand.png){style="block"}
_Parking space demand shown in traffic info view_

## Public transport demand

Since not every cim owns a car (think of children!) access to public transport is vital. The public transport info
view (click on the ![](btnTransportInfoView.png){style="inline"} button) shows you which buildings require a public
transport connection. By clicking on the Switch view button you may switch between outgoing and incoming demand view.
Outgoing demand of a building increases whenever cims currently located inside that particular building try to reach
another building but fail to do so because public transport is unavailable for them. The incoming demand view highlights
buildings that are tried to be reached by cims with means of public transportation but are not properly connnected to
your public transport network.

![](picLegacyParkingAI_demandPT.png){style="block"}
_The green subway line is not connected with both subway stations. Residential buildings in the vicinity show outgoing
public transport demand._

## Detailed process description

The following [activity diagram](https://en.wikipedia.org/wiki/Activity_diagram) shows how the Parking AI internally
works.

![](picLegacyParkingAI_activityDiagram.png){style="block"}
_Activity diagram showing the operation principle of the Parking AI feature_

The process implemented by Parking AI can be roughly divided into the following stages:

1. During initial planning a path between the starting position (source) and the destination building (target) is being
   established. Analysis of the initial path's properties then determines the next actions that shall be performed.
2. If initial planning decides that a walking route to a parked car is required a respective path is calculated. Then,
   depending on the citizen's type (tourist or resident) either
    1. a direct car route to target or
    2. a car route to a parking space within the vicinity of the target is established. The search for available parking
       spaces repeats if citizens arrive at parking places that have been occupied by other vehicles in the meantime.
3. During the final stage a walking route to the target is calculated.

### Initial planning

Initial checks determine if

* a path from source to target is calculated and that all available transport modes are considered (e.g. taking the bus,
  driving a car, walking) or
* if usage of private cars should be enforced.

The general aim here is to make sure that cars are not parked too far away from their owner's home. Cars may otherwise
become abandoned if path-finding decides to prefer public transport over private car usage when citizens try to get back
to their home building.

If an initial path is found it is analyzed based on several aspects: If the path contains a car section (a path segment
where citizens would require to use a private car) and the citizen is allowed to use it (only adults and small
percentage of teenagers may own private cars) it is then checked if the citizen already owns a car. If true, an
additional check decides if private car usage is justified based on economic aspects: If the distance between parked car
and target is too small the system may decide to disallow private car usage for the route. If the citizen does not own a
car a new parked car is spawned within the vicinity of the starting position.

### Walking route to parked car

If a suitable walking path towards the parked car could be established the citizen starts walking. After entering the
car the process decides if either

1. a direct path to the target or
2. a parking space within the target's neighborhood

shall be targeted next. Parking AI makes the assumption that tourists do not know of appropriate parking spaces
beforehand: They initially head towards the target building directly. Since residents ought to be familiar with all the
parking possibilities that your city has to offer they plan their routes accordingly while taking available parking
spaces into account. If no walking path between the source building and parked car can be established the parked car
de-spawns.

If no walking path between the source building and parked car can be established the parked car de-spawns.

### Direct car route to target

Direct car paths are calculated as in the base game. However, the key difference lies in what happens when the car
reaches its destination: When the Parking AI is active both residents and tourists start searching for a suitable
parking space in the vicinity of the target building if no search has been performed yet.

### Car route to parking space

A possible parking location has to fulfill several requirements in order to be considered by the Parking AI:

* It must be unoccupied: Of course, only free parking spaces are considered.
* It must lie close enough to the target: Only parking spaces within a certain distance from the destination are
  considered.
* It must be accessible for pedestrians: Since citizens will leave their car after reaching a parking spot there needs
  to be at least one path between the parking space and the destination building that supports pedestrians. For example,
  if a target building can only be reached via highway roads the respective parking space is not being considered since
  citizens are unable to walk on highways.

If a parking location has been identified and all conditions above match a car path to the parking spot is calculated.

As soon as the car arrives at the parking space the first condition above is checked again: If the chosen parking spot
has being occupied by another car in the meantime a new search is performed. This step may repeat up to a maximum of
N (default: 10) times. If the maximum amount of parking attempts is reached a fallback process kicks in which de-spawns
the car and teleports the citizen either to the destination building or back home.

### Walking route to target

During the final stage Parking AI calculates the remaining path to the target. Only walking and means of public
transportation are considered. When citizens reach their destination the process ends.

## Performance impact

Be aware that the Parking AI requires additional computational power to perform its tasks.

* Additional path-finding has to be performed.
* Additional effort is invested in finding free parking spaces.

You may notice slower simulation speed and/or temporarily stopping vehicles on weaker systems. 
