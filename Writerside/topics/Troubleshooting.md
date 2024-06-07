# 👉 Troubleshooting

> Verified: March 2022 - TM:PE 11.6.5.2

> # Check the Compatibility Report first
>
> About 50% of the error reports we get are due to old / broken / incompatible mods.
> The [Compatibility Report](https://steamcommunity.com/sharedfiles/filedetails/?id=2633433869) mod is the fastest way
> to
> find known problems with your mods - it's a collaboration between end-users and mod developers to help navigate the
> vast
> array of mods that are out there.

## Known bugs

We have replicated the following bugs and have temporary workarounds:

* [#277](https://github.com/CitiesSkylinesMods/TMPE/issues/277) (vanilla game bug): Vehicles despawning near recently
  altered roads or rails
    * Caused by
      a [bug in vanilla game](https://forum.paradoxplaza.com/forum/index.php?threads/cities-skylines-steam-vibrating-node-replicable-bug.1187861/)
      which CO are investigating
    * How to fix - see: [](How-to-remove-ghost-nodes-and-broken-nodes.md)
* [#273](https://github.com/CitiesSkylinesMods/TMPE/issues/273) (vanilla game bug): Tourists unable to leave via 2-way
  outside connections
    * Try the [Crazy Tourists Fix](https://steamcommunity.com/sharedfiles/filedetails/?id=1759269367) mod
* [#244](https://github.com/CitiesSkylinesMods/TMPE/issues/244): Changing roads (adding junctions, upgrading, etc.)
  breaks nearby transport routes.
    * Caused by Network Extensions 2 (NExt2)
    * How to fix - replace NExt2 roads with normal road asset replicas: [](How-to-remove-workshop-networks.md)

> Tip: Our feature documentation pages often have an "Issues" link at the bottom which will display currently known
> problems and ideas for that feature.

## General

* [](How-to-remove-workshop-networks.md) -- Roads, tracks, MOM, NExt2, etc.
    * [RON - Replace Our Networks](https://steamcommunity.com/sharedfiles/filedetails/?id=2405917899) mod is highly
      recommended
* Mods:
    * [](Incompatible-Mods-List.md) (mods that are incompatible with TM:PE)
    * [Online list of game breaking mods](https://docs.google.com/spreadsheets/d/1mVFkj_7ij4FLzKs2QJaONNmb9Z-SRqUeG6xFGqEX1ew/htmlview)
    * [](Recommended-Mod-Substitutions.md) -- our recommendations
* Assets:
    * [](Broken-Road-Assets.md), [](Broken-Vehicle-Assets.md), [](Broken-Building-Assets.md), [](Broken-Prop-Assets.md), [](Broken-District-Styles.md)
    * Vehicles: [Vehicle LODs are flashing](Vehicle-LODs-are-flashing.md), [](Shiny-Black-Vehicle-LODs.md)
    * [](Notes-for-Asset-Creators.md), [](Vanilla-capacities.md)
    * Lemonster's [List of broken assets and mods](https://steamcommunity.com/sharedfiles/filedetails/?id=1814220327) (
      Steam Workshop Collection)
* [](How-to-remove-ghost-nodes-and-broken-nodes.md)
* [](Moving-the-game-to-a-different-disk-drive.md)

> Where did "Error Messages" section go? I've moved it to bottom of page as none of those errors are caused by TM:PE.

## Content manager / Mod options / Settings

* [](TMPE-mod-options-lost.md) (or not saving/loading) in the mod options screen
* [](Subscribed-mod-not-showing-in-game.md)
* [](No-Enable-button-in-Content-Manager.md)
* [](Mods-missing-in-Content-Manager.md) (also applicable to assets)
* [](Road-and-Rail-customisations-lost.md) (lane arrows, traffic lights, restrictions, etc.)

## Public transport, and Cargo trains

* [](Allow-Intercity-Trains-button-not-working.md)
* [](Broken-transport-routes.md)
* [](Buses-are-using-weird-routes.md)
* [](Buses-Not-Spawning-From-Depots.md) -- may also be applicable for tracked vehicles
* [](Cims-not-using-public-transport.md)
* [](Cims-wait-for-taxi-in-middle-of-road.md)
* [](Intercity-buses-not-working.md)
* [](Tracked-vehicles-not-routing-or-spawning.md) — trains, metros, trams, monorail
* [](Regional-passenger-trains-not-visiting-city.md)
* [](Tracked-vehicles-not-routing-or-spawning.md) — trains, metros, monorails, trams
* [](Train-network-clogged-with-near-empty-cargo-trains.md)
* [](Transport-vehicles-stuck-on-boarding.md)

## Services

* [](Vehicle-Count-Flickering-Between-1-and-0.md) — most commonly seen on service buildings, but can also affect
  industries, etc.
* [](Hearses-not-spawning.md) — dead people not being collected
* [](Helicopters-and-trucks-from-wrong-depots.md) - e.g. fire helicopter spawns from
  a road-based fire station, or trucks spawning from helipads

## Cims / Vehicles / Outside connections

* [](Cims-stuck-at-crosswalks.md)
* [](How-do-I-turn-off-dummy-traffic.md) — the 'fake' traffic that just drives in and out
  of city
* [](Industry-and-Commercial-vehicles-not-working.md)
* [](Industry-resources-collection-and-delivery-issues.md)
* [](Intercity-buses-not-working.md)
* [](Floating-cyclists-and-discarded-bicycles.md)
* [](Floating-vehicles.md)
* [](Outside-connections-not-working.md)
* [](Population-stuck-at-0.md)
* [](Red-cars-everywhere.md)
* [](Vehicles-not-spawning.md) -- industry, services, public transport

## Roads & Tracks

* [](Cars-driving-through-red-traffic-lights.md)
* [](Change-which-side-traffic-drives-on.md)
* "Blue Void":
    * [](Blue-void-showing-near-roads.md) — also applies to paths, tracks, etc.
    * [](Blue-void-roads-or-tracks.md) - usually after placing buildings that contain road/tracks
    * [](Section-of-road-becomes-blue-void.md) - often happens after renaming a road / changing route
* [](Bulldozing-road-causes-vehicles-to-despawn-nearby.md)
* [](Flickering-blue-road-building-guides.md)
* [](Flying-Trees.md)
* [](Lane-arrow-and-connector-not-loading.md)
* [](Road-LODs-look-ugly-or-glitching.md) - can also cause massive "terrain spikes" on the map
* [](Road-texture-flickers,-or-terrain-showing-through-roads.md) - also applies to paths, tracks, etc.
* Mod [](Roads-United-Core.md) - can break toll roads
* [](Terrain-and-Roadside-Grass-Turned-White.md)
* [](Toll-Booths-not-working.md)
* [](Traffic-on-highways-not-behaving-properly.md)
* [](Vehicles-driving-over-medians.md)
* [](Zoning-not-working-on-roads.md)

## UI (User Interface)

* [](Buttons-missing-in-asset-editor.md)
* [](Clicking-button-makes-text-dissapear.md)
* [](Electricity-lines-and-water-pipes-missing.md)
* [](Interface-text-missing.md) (usually on the timed traffic lights panel)
* [](Lane-Arrows-buttons-missing-arrows.md)
* [](Middle-Mouse-Button-Rotation-Not-Working.md)
* [](No-audio.md)
* [](Policies-panel-missing.md)
* [](Road-names-distorted.md)
* [](TMPE-overlays-not-showing.md)

## Recently Fixed Bugs

These issues should now be fixed (if not, let us know):

* [](Traffic-lights-turning-white.md) - BP fixed the "More Flags" mod in August 2019
* [](Mod-options-screen-not-showing-properly.md)
* [](Options-screen-showing-wrong-options-for-selected-mod.md)
* [#259](https://github.com/CitiesSkylinesMods/TMPE/issues/259): "Looking for parking" infinite loop / vehicle stuck in
  road looking for parking
* [#225](https://github.com/CitiesSkylinesMods/TMPE/issues/225): Lane changes at toll booths - fixed in TM:PE v10.21
* [#817](https://github.com/CitiesSkylinesMods/TMPE/issues/817) (Linux/Mac): Game crashes while loading, or stuck on
  pause after loading.

## Error messages

None of these are caused by TM:PE, but we list them here as it's useful resource for anyone encountering them.

* [](boost-filesystem-path.md)
* [](ArgumentException-An-element-with-the-same-key-already-exists-in-the-dictionary.md)
* [](ArgumentNullException-Argument-cannot-be-null.md)
* **[](Could-not-get-memory-for-large-allocation.md)** - not enough RAM or page file too small!
* [](Could-not-load-global-config-System.TypeLoadException.md)
* [](Could-not-load-type-TrafficManager.Geometry.Impl.SegmentGeometry.md)
* **[](Could-not-load-type-TrafficManager.Traffic.Data.VehicleState.md)**
* [](Exception-BuildingInfo-..._Data-failed.md) - and also `Custom Assets: ..._Data: NetInfo missing`
* [](Field-.PathUnit.m_vehicleTypes-not-found.md) `System.MissingFieldException`
* [](FileNotFoundException-Could-not-load-file-or-assembly-'TrafficManager'.md)
* [](FormatException-Invalid-Image-Format.md)
* [](GetColors()-format-not-supported-System.NotImplementedException.md)
* [](InitD3D11RenderColorSurface.md) 
* [](Invalid-list-detected.md)
* [](KeyNotFoundException-The-given-key-was-not-present-in-the-dictionary.md)
* **[](Object-reference-not-set-to-an-instance-of-an-object.md)**
    * Sometimes it might say `NullReferenceException` (same error, just logged differently)
    * See also: [](Ploppable-RICO-errors.md)
* **[](Simulation-error-Array-index-is-out-of-range.md)**
* [](Simulation-error-Cannot-cast-from-source-type-to-destination-type.md)
* [](Simulation-error-Division-by-zero.md)
* [](Simulation-error-EndDeserialize(GameAreaManager)-tag-mismatch.md)
* [](Simulation-error-Object-reference-not-set.md) (`RoadBaseAI.CanEnableTrafficLights`)
* [](Simulation-failed-Deserialisation-tag-mismatch.md)
* [](System.ArgumentNullException-''-with-1-arguments.md)
* [](System.IO.IOException.md) which might be shown as:
    * `System.IO.IOException: Sharing violation`
    * `System.Reflection.TargetInvocationException`
* [](System.IO.IOException-Win32-IO-returned-112.md)
    * On screen, you might see something like `The Mod ... [.dll files] has caused an error`
* [](System.StackOverflowException.md) (also sometimes without the `System.` bit)
* [](System.Reflection.TargetInvocationException-TMPE.log-is-denined.md) - or any other `TMPE.log` error
* [](The-class-PropVehCount.PropVehCount-could-not-be-loaded.md)
* `Look rotation viewing vector is zero` - triggered by Vehicle Effects mod? Causes in-game lag due to log file spamming
  during gameplay.

## Stuff Lost in Time

*[](Simulation-error-ProceduralObjects-error.md)