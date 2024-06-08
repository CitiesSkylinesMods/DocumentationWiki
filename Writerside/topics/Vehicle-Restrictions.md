# Vehicle Restrictions

> Verified: December 2021 - TM:PE 11.5.2

## Overview

Use this tool to separate vehicle categories in to different lanes on your **roads** and **train tracks**.

## Usage

Choose **Vehicle Restrictions** on the [](Toolbar.md):

![Vehicle Restrictions tool](btnVehicleRestrictions.png)

> Button missing? Enable **Vehicle Restrictions** in [](Maintenance.md) in [](Settings.md).

### Applicators

**Click a road or rail segment** to edit the vehicle restrictions for each lane:

![](picVehicleRestrictions_example.png)

> If the icons don't appear, try moving/zooming the camera closer to selected segment.

Clicking the icons toggle between **allowed** vs. **discouraged** states, for example:

|                     Allowed Car                     |                    Discouraged Car                     |
|:---------------------------------------------------:|:------------------------------------------------------:|
| ![Allowed](picVehicleRestrictions_privateAllow.png) | ![Discouraged](picVehicleRestrictions_privateDeny.png) |

### Icons

Roads:

|                          Icon                           | Vehicles                                                             |
|:-------------------------------------------------------:|----------------------------------------------------------------------|    
|     ![Car](picVehicleRestrictions_privateAllow.png)     | **Cars**  - passenger cars and motorbikes                            |                            
|       ![Bus](picVehicleRestrictions_busAllow.png)       | **Buses** - passenger, sightseeing and evacuation buses              |              
|      ![Taxi](picVehicleRestrictions_taxiAllow.png)      | **Taxis**                                                            |                                                            
|     ![Truck](picVehicleRestrictions_truckAllow.png)     | **Trucks** - all types of industry trucks and vans                   |                   
|   ![Service](picVehicleRestrictions_serviceAllow.png)   | **Services** - all services including emergency services             |             
| ![Emergency](picVehicleRestrictions_emergencyAllow.png) | **Emergencies** - Vehicles responding to emergencies (active sirens) | 

Trains:

| Icon                                                 | Vehicles                                       |
|------------------------------------------------------|------------------------------------------------|
| ![Passenger](picVehicleRestrictions_trainAllow.png)  | **Passenger Trains** - both local and regional |
| ![Cargo](picVehicleRestrictions_cargoTrainAllow.png) | **Cargo Trains** - both local and regional     |

### Vehicle Routing

Vehicles calculate their route _before_ starting their journey. As a result, when you change restrictions, only vehicles
spawned _after_ that point will be aware of your changes.

To force existing vehicles to calculate new routes when you make changes, enable **Apply AI changes right away**
in [](General.md) in [](Settings.md).

### Shortcuts

The following shortcuts are applicable when the Vehicle Restrictions tool is active...

Selection:

* `Click a segment of road/rail` - choose segment to customize
    * Any previously selected segment will be deselected
* `Right-click anywhere` - deselect current segment
    * If no segment selected: Exit the **Vehicle Restrictions** tool as if you pressed `Esc`
* `Esc` - exit **Vehicle Restrictions** tool
    * Returns focus to the [](Toolbar.md) and enables its [](Adjust-Roads.md) mode.

Basic applicators:

> These are applied to the currently selected segment.

* `Click a vehicle icon` - toggle the restriction on/off
* `Shift`+`Click a vehicle icon` - toggle restriction on/off and apply that change along the route

Camera / Overlays:

* `Mouse wheel` - zoom in or out
    * If you zoom out too far, icons may disappear
* `PageDown` - underground view
    * This activates a simplified version of the [](Traffic-Info-View.md)
* `PageUp` - overground view

### Overlays

While the tool is active, icons summarize vehicle restrictions on nearby roads/tracks:

![Summary Icons](picVehicleRestrictions_summary.png)

To see icons for distant roads/tracks, move the camera towards them. **Overlay transparency** can be set
in [](General.md) in [](Settings.md).

When the tool is deactivated overlays will be removed. A persistent overlay, which summarizes vehicle restrictions
whenever the [](Toolbar.md) is visible, can be enabled in [Overlays](Overlays.md) in [](Settings.md).

## Notes

This tool is designed to provide fine-tuning of traffic restrictions, for example:

* Prevent trucks driving through residential areas
* Make passenger trains choose a different rail track
* Stop trucks cargo using inner lane of highways
* Prevent cars and trucks from using bus lanes
  > It's better to use [](Bus-Lane-Restrictions.md) to achieve this

Remember to provide alternate routes for vehicles, otherwise they might not be able to reach their destination.

* [](Reckless-Drivers.md) ignore vehicle restrictions
* Emergency vehicles, when responding to an emergency (red/blue lights flashing), also ignore vehicle restrictions

### How it works

* Restriction = pathfinding _penalty_
* [](Vehicle-Restriction-Aggression.md) sets penalty magnitude
* Penalties are cumulative for a route
* Pathfinder tries to avoid incurring penalties
* If penalty is too high, and no alternative routes, the route is cancelled
    * This prevents vehicle spawning (or, if already spawned, the vehicle will despawn)

### Service Coverage

> Note: Some of these mods might be out of date;
> use [Compatibility Report](https://steamcommunity.com/sharedfiles/filedetails/?id=2633433869) to check.

If you want to limit coverage of service buildings, use these mods instead:

* [Service Radius Adjuster](https://steamcommunity.com/sharedfiles/filedetails/?id=785237088)
  or [Customize It: Extended!](https://steamcommunity.com/sharedfiles/filedetails/?id=1806759255):
    * Control the travel distance a building will service
* [Real Time](https://steamcommunity.com/sharedfiles/filedetails/?id=1420955187):
    * Lets you control where cims shop (e.g. local to where they live/work), etc.

## FAQ

> Q: Does it affect frame rate or cause lag?
>> A: Yes, a little; it adds extra work for the pathfinder especially if you use the feature extensively. If that's a
> > problem, you can disable the feature in [](Maintenance.md).

> Q: Some traffic is unexpectedly avoiding my roads
>> * Check [](Lane-Arrows.md), [](Lane-Connectors.md), [](Traffic-Lights.md), [](Speed-Limits.md), and [](Settings.md),
     all of which affect vehicle route pathfinding.
>> * Fires and disasters will block roads to most traffic (emergency services can still get through).
>> * [](City-and-District-Policies.md) can impose additional restrictions

> Q: Which city/district policies cause vehicle restrictions?
> A: See: [](City-and-District-Policies.md)

> Q: Pedestrian and cycle paths don't show icons
>> A: Currently, this tool only supports road and train networks.

> Q: Can I block specific vehicle assets?
>> A: Not with TM:PE, but other mods can control which vehicles will be spawned:
>> * [Advanced Vehicle Options](https://steamcommunity.com/sharedfiles/filedetails/?id=1548831935)
>> * [Service Vehicle Selector](https://steamcommunity.com/sharedfiles/filedetails/?id=934994075)
     or [Service Vehicles Manager](https://steamcommunity.com/sharedfiles/filedetails/?id=1632320836)
>> * [Improved Public Transport](https://steamcommunity.com/sharedfiles/filedetails/?id=928128676)
     or [Transport Lines Manager](https://steamcommunity.com/sharedfiles/filedetails/?id=1312767991)

> Q: Cyclists?
>> * No, but it's being considered,
     see: [Issue #18](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues/18)
>> * You can use [](City-and-District-Policies.md): **Encourage biking** and/or **Bike ban on sidewalks**

> Q: Regional vs. local traffic?
>> * No, but it's being considered, for trains,
     see: [Issue #158](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues/158)
>> * You can use [Optimized Outside Connections](https://steamcommunity.com/sharedfiles/filedetails/?id=1721492498)
     and/or [Advanced Outside Connection](https://steamcommunity.com/sharedfiles/filedetails/?id=2053500739) mods to
     reduce outside traffic
>> * You can use the vanilla **Allow intercity trains** option on Passenger Station info panels
>> * You can use [Intercity Bus Control](https://steamcommunity.com/sharedfiles/filedetails/?id=2499771767) to control
     whether normal bus stations can accept intercity buses.

> Q: Restrict annoyingly large camper vans and caravans?
>> A: No, the game treats them as normal cars. 😞

> Q: Differentiate between van, truck, trailer?
>> A: No, but it's being considered,
> > see: [Issue #141](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues/141).
> > You can gain some control via [No Big Truck](https://steamcommunity.com/sharedfiles/filedetails/?id=2069057130)
> > which controls what sort of buildings a big truck can visit (read description of that mod carefully).

> Q: Split out different industries?
>> A: No, it would cause massive issues for industry supply chains.

## See also

[](Toolbar.md):

* [](Parking-Restrictions.md)
* [](Junction-Restrictions.md)

[](Settings.md):

* [](General.md) - should changes take effect immediately?
* [](Policies.md) - should bus lanes automatically restrict cars & trucks?
* [Overlays](Overlays.md) - toggle persistent overlay

[Issue Tracker](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues):

* <a href="https://github.com/CitiesSkylinesMods/TMPE/labels/VEHICLE RESTRICTIONS"><img alt="Issues" src="https://img.shields.io/github/issues/CitiesSkylinesMods/TMPE/VEHICLE RESTRICTIONS?label=VEHICLE RESTRICTIONS%26logo=github" /></a>