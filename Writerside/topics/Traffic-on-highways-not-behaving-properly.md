> Article verified: June 2019

# Symptom

One or more of the following may occur:

* Vehicles aren't using all lanes on the highway
* I activated **Enable highway-specific lane merging/splitting rules** but nothing changed
* I made changes to my highway but vehicles are ignoring it
* Traffic jams due to merging at last node before a junction

# Causes

> Note:
>  
> **For performance reasons, changes to highways do not update existing vehicles. Only vehicles spawned after the change will be aware of it.**
> 
> The **Customisations come in to effect immediately** option in [](General.md) **does not apply to highways!**
>  
> You have to wait for newly spawned vehicles to see the effect of changes. You can use [Clear Traffic](Clear-Traffic.md) tool to remove old vehicles.

These symptoms are usually caused by incorrect mod settings, or not realising that highway traffic doesn't update until new vehicles spawn.

# Solution

If traffic is not using all lanes:

* **Enable Advanced AI** in [](Gameplay.md) - this makes all traffic use more lanes
* You can then use **Dynamic lane selection** (DLS) in [](Gameplay.md) for even more lane changes

When using DLS, you might see traffic jams caused by vehicles all trying to use the middle lane just before junctions:

* Alter the DLS slider to under 50% (values of 30%-40% seem to work well on most cities)
* We are working on improving DLS to avoid this issue (see [#263](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues/263))

If traffic is not behaving properly at highway junctions:

* **Enable highway-specific lane merging/splitting rules** in [](Policies.md)

# Fixed?

If not, please let us know: [Report a Bug](Report a Bug)

Other problems? See: [Troubleshooting](Troubleshooting)