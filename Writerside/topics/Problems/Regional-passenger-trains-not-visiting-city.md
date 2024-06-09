# Regional Passenger Trains not Visiting City
> Article verified: August 2019

## Symptom

* Out-of-town passenger trains are not visiting the city

## Cause

Three main causes (more covered in **Solutions** section below):

* Stations not set-up properly
* TM:PE [[Vehicle Restrictions] blocking their routes
* Modded train tracks used for outside connection

## Solutions

The most common cause is incorrectly configured train stations:

* Click the passenger train station
* On the info panel, make sure it allows outside trains

TM:PE vehicle restrictions can cause problems if incorrectly used:

* Make sure you haven't limited the passenger train tracks to cargo trains.

Passenger trains can only enter the map via vanilla rail tracks:

* Modded tracks don't trigger the game to create the fake train station at edge of map:
    * Make sure there are at least 5 segments of vanilla rail tracks at edge of map
    * The vanilla segments have to be long enough to accommodate the fake train station
    * From that point onwards, you can use modded train tracks in the rest of your city
* Note that cargo trains can still enter and leave the map because they don't require that fake station ;)

There are some other causes:

* Make sure you've not used cargo station - they can't accept passenger trains!
* If you've restricted vehicle spawning (using mods like AVO or IPT2) ensure the selected vehicles still exist and can spawn
* Check your transport budgets, and also your road/rail budgets
* Mods like Real Time might alter the frequency of train visits or change the ratio of visits between day and night

## Was it Fixed?

If not, see:

* [](Tracked-vehicles-not-routing-or-spawning.md)
* [](Cims-not-using-public-transport.md)
* [](Vehicles-not-spawning.md)

Other issues? See: [](Troubleshooting.md)