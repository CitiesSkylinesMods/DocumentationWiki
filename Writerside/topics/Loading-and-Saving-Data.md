# Loading and Saving Data

> ### **Note:** This page describes code that has not yet been merged into the `master` branch.

There are two ways to load and save data, depending on the history and condition of the code you are working with. Both
involve the organization of data into an object model for saving. However, they differ as follows:

1. The preferred method, a fully persistable object model, involves the creation of structures that can be read from a
   manager, then later written back to the manager. In other words, it is a complete round-trip process.
2. An alternate method, which we will call the half-baked persistable model, involves objects that can be read from a
   manager, but cannot be written back. This is used with managers whose design is unfriendly the creation of a fully
   persistable object model, such as `TrafficLightSimulationManager`.

## Fully Persistable Model

When possible, a manager should provide a set of internal methods returning structures containing simple fields,
designed to remain stable through underlying code changes. And a corresponding set of methods should accept those
structures and use them to reconfigure itself to the state originally described.

`JunctionRestrictionsManager` is the reference implementation for this approach. Note that there is no attempt to create
a complete representation of the manager's state in a single hierarchy of objects. Rather, the save and load code loop
through the items individually. This is because we are not performing true serialization, but are instead using a more
primitive copying process.

Ideally, the manager will use these structures internally, as `JunctionRestrictionsManager` does. If this is not
possible, it is probably best to go with a half-baked persistable model. A manager should not be involved in data
conversion.

## Half-Baked Persistable Model

When a manager's design is unfriendly to a fully persistable model, the alternative is to define interfaces based on its
native object model, which it can implement to offer some stability for save data. This is the approach taken
in `TrafficLightSimulationManager`. This is a complex example, and will be replaced by a simpler one in the future.

The save code uses this object model as a basis for structuring the save data and naming its elements and attributes.
The load code uses it as a reference point for general structure, element and attribute names, but does not actually
load data into these objects. Instead, it loads the data as arguments to the manager's preexisting setup methods.

## Versioning

The load/save code includes a versioning framework, but it is not needed for the initial conversion to this strategy.
The very existence of the new type of save data is itself an implicit versioning indicator.

At this time, [#1392](https://github.com/CitiesSkylinesMods/TMPE/issues/1392) will be the first known use of versioning,
and therefore may serve as the reference implementation when complete. However, due to the size of that project,
something else may come first.