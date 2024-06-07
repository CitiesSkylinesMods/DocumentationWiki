# Broken Road Assets

> Article verified: June 2019

> If you haven't already done so, subscribe and
> enable [Loading Screen Mod](https://steamcommunity.com/sharedfiles/filedetails/?id=667342976) - it loads maps much
> faster, reduces RAM consumption for better in-game performance, and fixes a load of common workshop bugs.

We have identified some road assets which are broken (the assets themselves are broken).

### General

* ~~The _Basic Road_ in **[OST2 Stock Road Pack](https://steamcommunity.com/sharedfiles/filedetails/?id=1672263805)** by
  Mr.Yawnie is broken. Therefore, remove the complete pack.~~ Should be fixed
* **[Reverse 4 Lane Highway B](https://steamcommunity.com/sharedfiles/filedetails/?id=1802966295)
  ** - `NullReferenceException` in the asset deserialiser
* **[Small four lane road reversed](https://steamcommunity.com/sharedfiles/filedetails/?id=1867586141)
  ** - `NullReferenceException` in the asset deserialiser
* **[Bridge building station+passJP1L](https://steamcommunity.com/sharedfiles/filedetails/?id=1843040605)
  ** - `NullReferenceException` in the asset deserialiser

### Requires Mass Transit DLC

> These roads will break if you don't have **Mass Transit DLC**; either buy the DLC or unsubscribe the roads

* *
  *[Realist HWY Ramp Project RHT(right hand traffic)](https://steamcommunity.com/sharedfiles/filedetails/?id=1908620939)
  ** - requires Mass Transit DLC
* *
  *[Realist HWY Ramp Project LHT (left hand traffic)](https://steamcommunity.com/sharedfiles/filedetails/?id=1913487091)
  ** - requires Mass Transit DLC
* Related error: [[Exception: BuildingInfo ..._Data failed]]

### Bus Roads

Issues with bus routing or bus stops:

* **[Two Lane One-Way Car and Bus Road](https://steamcommunity.com/sharedfiles/filedetails/?id=1518295774)**
  > * [#34](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues/34): When a junction
      is added, the lane textures swap over (bus lane looks like normal lane, normal lane looks like bus lane)

* **[Metrobus](https://steamcommunity.com/sharedfiles/filedetails/?id=1563428928)**
  > * [#30](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues/30#issuecomment-461050231):
      Bus routes are able to cross over the median (see also: [](Vehicles-driving-over-medians.md))
  > * [#34](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues/34): When a junction
      is added, the positioning of bus lanes seems to move

* *
  *[Six-Lane Road with Bike and Bus Lanes, Decorative Grass](https://steamcommunity.com/sharedfiles/filedetails/?id=1226063060)
  **
  > * Unconfirmed reports that cims can't use bus stops on this road due to the grass verge / bike lane

### Interchanges

Unsubscribe these:

* **[5 way Clover Full Capacity Final](https://steamcommunity.com/workshop/filedetails/?id=932939897)**
  > * `IndexOutOfRangeException: Array index is out of range.`
* **[Skye's 3 Way Stack Intersection](https://steamcommunity.com/sharedfiles/filedetails/?id=1141090282)**
  > * `EndOfStreamException: Failed to read past end of stream.`

### Pedestrian networks

* **Pedestrian Suspension Bridge** (no longer in workshop; asset id: 418352365)
  > * [Very large LOD texture](https://steamcommunity.com/workshop/filedetails/discussion/667342976/1639789306562181099/)
      will cause problems on weak graphics cards and could cause severe degradation of other LODs