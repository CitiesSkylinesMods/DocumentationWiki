# 👴 Modified Path Finding

> 👴 This article's content is old, copied from the original Wiki at https://tmpe.viathinksoft.com/wiki/

## Introduction

When enabled, TM:PE modifies the base path-finding algorithm in order to allow for the provided features to work
correctly.

The following list of functions integrate into the modified algorithm:

* Vehicle restrictions: During path-finding, costs for using restricted road segments are raised to either lower the
  probability or to prevent traversal of such segments.
* Junction restrictions:
    * If crossing a street at a given location is prohibited for citizens, path-finding does not take the crossing in
      question into account.
    * If vehicles are allowed to perform U-turns, path-finding accounts for this degree of freedom.
* Bus lane reservation: TM:PE increases the cost of using bus lanes for regular vehicles.
* Buses may ignore lane arrows: When this option is enabled, path-finding allows busses to ignore lane arrows (though
  they are still advised to obey them where possible)
* Heavy trucks prefer outer lanes on highways: When this option is enabled, trucks tend to use the outermost lane on
  highways. This is achieved by artificially raising traversal costs for inner highway lanes (for heavy vehicles only,
  of course).
* Speed limits: Speed limits directly affect segment traversal costs. For example, choosing a segment with a speed limit
  of 50 assigned costs is twice as expensive as choosing one with a speed limit of 100.
* Advanced Vehicle AI: When activated, the Advanced Vehicle AI selects roads with lower average traffic volume,
  randomizes lane selection for better traffic spread and introduces costs for changing lane and for performing U-turns.

## Cost calculation scheme

The path-finding algorithm calculates costs for traversing a certain road segment according to the following scheme:

1. Apply vehicle restriction costs (factor depends on vehicle restrictions aggression; low: 10, medium: 100, high: 1000,
   strict: +infinite).
2. Apply vanilla car ban policies (Old Town factor: 5, Heavy Traffic Ban factor: 10).
3. Apply costs for using/not using transport lanes (Bus on transport lane factor: 0.1, regular vehicle on transport lane
   factor: 10).
4. Apply costs for large vehicles using inner lanes on highways (only if the respective option is activated, see
   Options; factor: between 1 and 2).
5. (only if Advanced Vehicle AI is enabled) Apply costs for randomized lane selection in front of junctions and highway
   transitions (randomly, either 1 or 2).
6. (only if Advanced Vehicle AI is enabled) Apply costs derived from traffic measurements (between 1 and 5).
7. (only if Advanced Vehicle AI is enabled) Apply lane changing costs (base cost factor: 1.5, multi-lane cost factor:
   2).
8. (only if Advanced Vehicle AI is enabled) Multiply with the number of lanes to change.
9. Multiply resulting value with the length of the considered road segment.
10. Divide resulting value by the current speed limit.

## See also

* [](L-Vehicle-Routing.md)
* [](L-Advanced-AI.md)  
