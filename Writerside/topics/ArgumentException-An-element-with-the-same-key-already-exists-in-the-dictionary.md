# ArgumentException An element with the same key already exists in the dictionary

## Symptom

You see an error on-screen or in log file like:

* `ArgumentException: An element with the same key already exists in the dictionary.`

## Cause

This occurs when a mod tries to store a value as a key in a dictionary lookup table, but the dictionary already contains
a key with that value.

It can be caused by errors in the mod, or sometimes having multiple versions of the same mod subscribed.

## Solutions

In the log file, look for the full error message which will usually start with the `ArgumentException` error and then be
followed by several lines starting with `at ...`.

If you see `FineRoadAnarchy.ModInfo:.ctor()` or `FineRoadTool.ModInfo:.ctor()` in the error message, it is almost
certain that you have either two versions of Fine Road Anarchy and/or Fine Road Tool mods subscribed. To fix, completely
unsubscribe the older versions of the mod (don't just disable them).

## Was it Fixed?

If not, please share your log file in support forums and hopefully someone will be able to help.

Other issues? See: [](Troubleshooting.md)