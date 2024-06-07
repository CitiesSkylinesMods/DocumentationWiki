> Article verified: June 2019  
> TM:PE 10.21 fixes the lane changing issue mentioned below

> Cars changing lanes at toll booths? See: [Issue #225](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues/225)

# Symptoms

Usually all these symptoms appear together:

* Cars aren't paying at toll booths
* Cars drive slow though toll booths rather than stopping even though the ["Automated Toll" policy](https://skylines.paradoxwikis.com/Policies) is disabled
* Toll booth info panel shows "Out of order" (or "Außer Betrieb" in German language, etc.)

# Causes

This is caused by other mods, even when you aren't using TM:PE.

> Note: Older versions of TM:PE did have a Toll Booth bug like this, but it got fixed (in version 1.10.14).

# Solutions

> Huge thanks to **SirKroitz** and **FireController1847** for [tracking down the source of this bug](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues/269)!

Try disabling these mods, then restart Cities: Skylines, and see if that resolves the issue:

* [Roads United Core+](https://steamcommunity.com/sharedfiles/filedetails/?id=726005715)
    * Note: We haven't had any reports about the issue being caused by `Roads United Core 2.0` but it is also a likely cause of the bug
    * It might be limited to [this US Roads skin](https://steamcommunity.com/sharedfiles/filedetails/?id=726004927)
    * If so, the same issue might apply to other skins as well
* [Road Options (Road Colors Changer ++)](https://steamcommunity.com/sharedfiles/filedetails/?id=932192868)

# Fixed?

If not, please let us know: [Report a bug](Report a bug)

Other issues? See: [Troubleshooting](Troubleshooting)