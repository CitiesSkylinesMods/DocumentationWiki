# Hearses not Spawning
> Verified: February 2022 - TM:PE 11.6.4.8

## Symptom

You might see one or more of these symptoms:

* Lots of dead people all over city
* No hearses spawning form cemeteries or crematoriums
* Hearses spawn but immediately despawn (disappear)

## Causes

There are several causes for these issues, including:

* Water pollution causing mass deaths
* Cemeteries are full to max capacity
* Hearses unable to reach dead people
* Mods preventing hearses from spawning

## Solutions

If there are huge numbers of dead people:

* Check that you don't have polluted drinking water
    * This is the most common cause of large scale death
    * If a water tower is on polluted land, it will produce polluted water = mass deaths
    * If a water pump is in a polluted river, same problem
    * Some mods hide pollution colours making it really hard to see where problem is
    * You can still see pollution on the [pollution info view](https://skylines.paradoxwikis.com/Info_views#Pollution)
    * Watch this [YouTube video tutorial](https://www.youtube.com/watch?v=K7eToC5RpoA) to see how to deal with pollution
* Make sure your cemeteries aren't full
    * Full cemeteries can't accept any more dead people
    * You have to empty them in to a crematorium:
        * Click cemetery to show its building info panel
        * Click the "Empty" button to start emptying cemetery
    * You need at least one crematorium to empty the bodies in to
    * Once empty, you need to manually switch back to normal mode:
        * Click the "Empty" button again to turn off empty mode
        * Cemetery will start collecting dead people again
    * You can automate this process using the [Empty It!](https://steamcommunity.com/sharedfiles/filedetails/?id=1661072176) mod
    * Alternatively only build crematoriums, and you won't need to worry about emptying cemeteries
* Note that crematoriums can also fill up if you send too many dead people there
    * If this happens, you'll need more cemeteries or crematoriums
* If problems persist, it might be problem with hearses...

If hearses aren't spawning, or despawning quickly afterward, or there are just not enough of them:

* Make sure there isn't a road blockage causing a massive traffic jam
    * Do you have a train jam on a level crossing?
    * Is there a flooded road causing a traffic jam?
    * Is there a collapsed road that needs repairing? (Natural Disasters DLC)
    * Is there a fire or collapsed building next to a road? (causes road to be marked blocked until resolved)
* If you use a Hearse AI mod:
    * Disable it (in Content Manager)
    * Exit to desktop, then restart the game
    * Are things any better?
* Hearses should have capacity of 2-10 corpses:
    * Any more will confuse the AIs leading to big problems
    * You can check capacity using [Advanced Vehicle Restrictions (AVO)](https://steamcommunity.com/sharedfiles/filedetails/?id=1548831935) mod
    * See [](Vanilla-capacities.md) for detailed explanation
    * If in doubt, unsubscribe any custom hearse assets and see if that fixes problem
* Check that you don't have any mods which prevent deaths:
    * No deaths = no hearses.
    * Some mods which cause problems:
        * [Pollution, Death, and Garbage Remover](https://steamcommunity.com/sharedfiles/filedetails/?id=769744928)
        * [No Deathcare](https://steamcommunity.com/sharedfiles/filedetails/?id=803074771)
* Don't use "Hearse AI" mods:
    * At the time of writing (July 2019) they are all horribly broken
    * Unsubscribe them completely and then exit to desktop to flush them from RAM

## Was it Fixed?

If still problems with hearses, see this guide: [](Vehicles-not-spawning.md)

Other problems? See: [](Troubleshooting.md)