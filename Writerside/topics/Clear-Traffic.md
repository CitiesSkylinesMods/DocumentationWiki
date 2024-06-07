# Clear Traffic

> Verified: January 2022 - TM:PE 11.6.4.4

## Overview

Use this to despawn (remove) all vehicles in your city.

## Usage

When used, this tool will:

* Despawn all active vehicles (see **FAQ** section for a full list)
* Reset traffic statistics (traffic flows, average lane speeds...)

It does not:

* Despawn parked cars - you can **Remove parked vehicles** in [](Maintenance.md) in [](Settings.md)
* Despawn cims - you can **Reset stuck cims and vehicles** in [](Maintenance.md) in [](Settings.md)

### Activate

Click **Clear Traffic** on the [](Toolbar.md):

![Clear Traffic tool](https://imgur.com/Kt069B0.png)

You will see a confirmation dialog asking if you are sure:

* If you confirm, the traffic and statistics will be cleared.
    * Vehicles, including public transport, will then gradually respawn.
* If you cancel, nothing will happen

### Despawn individual vehicle or cim

1. **Click the vehicle** - its info panel is displayed
2. **Click (todo: image)** - despawn the vehicle or cim

## FAQ

#### Does this affect frame rate or cause lag?
> Temporarily. There might be some lag if large numbers of vehicles need to respawn (lots of work for pathfinder).

#### Which vehicles are affected?

Read more: [Which vehicles are affected?](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues/35)

> These are removed:
> * Bicycles, busses, taxis
> * Cars, motorcycles, vans, trucks, lorries
> * Emergency, maintenance and service vehicles
> * Trains (passenger and cargo), trams, metros, monorails, cable cars
> * Planes (cargo and passenger), Hot air balloons, blimps, helicopters
> * Ships (cargo and passenger), ferries
> * Meteors, tornados (requires [Natural Disasters DLC](https://store.steampowered.com/app/515191/Cities_Skylines__Natural_Disasters/))
>  
> These are **not** removed:
> * Pedestrians and their pets
> * Industry workers (eg. farmers, miners...)
> * Service workers and animals (eg. disaster recovery teams and their dogs, firemen...)
> * Birds, livestock (farm animals) and other wildlife (deer, dolphins...)

#### Can I despawn specific categories of vehicles?
> Yes - use the filtered `Despawn` tool in [](Maintenance.md) in [](Settings.md).

## See Also

[](Settings.md):

* [](Gameplay.md) - toggle despawn
* [](Maintenance.md) - few additional reset/remove tools

[](Toolbar.md):

* [Toggle Despawn](Toggle-Despawn.md)