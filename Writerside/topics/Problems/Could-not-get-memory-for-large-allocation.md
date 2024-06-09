# Could not Get Memory for Large Allocation
> Verified: February 2020 - TM:PE 11.0

## Symptom

You see an error in the game log file:

* `Could not get memory for large allocation`

The error will often be repeated, for example:

```
DynamicHeapAllocator allocation probe 1 failed - Could not get memory for large allocation 699064.
DynamicHeapAllocator allocation probe 1 failed - Could not get memory for large allocation 33554428.
DynamicHeapAllocator allocation probe 2 failed - Could not get memory for large allocation 699064.
DynamicHeapAllocator allocation probe 2 failed - Could not get memory for large allocation 33554428.
```

## Cause

You have run out of RAM, or your swap/page file is too small.

The store page states the game will run in 4 GB RAM, that's a joke. Base game needs 8 GB to run reliably, and ideally you should have 16 GB or more.

## Solution

Open the [Performance Tuning Guide](https://steamcommunity.com/sharedfiles/filedetails/?id=465790009) and read following sections:

* RAM and Page file
* Loading Screen Mod
* DLC, Assets and Mods

Those sections will give you some ideas on how to reduce RAM consumption and what to do if that still doesn't work.

## Was it Fixed?

If not, either buy more RAM or start unsubscribing bloated assets.

Other problems? See: [](Troubleshooting.md)