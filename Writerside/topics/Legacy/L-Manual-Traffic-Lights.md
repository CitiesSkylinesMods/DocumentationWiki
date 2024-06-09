# 👴 Manual Traffic Lights

> 👴 This article's content is old, copied from the original Wiki at https://tmpe.viathinksoft.com/wiki/

## Introduction

The first step to become a real traffic president is to take control of your traffic lights. The Manual traffic light
mode lets you play around and get used to the awkward user interface.

## Setup

You can temporarily control a junction's lights by following these steps:

1. Click on the ![](btnMain.png){style="inline"} button.
2. Click on the ![](btnManualTL.png){style="inline"} button.
3. Click on the junction that you want to control.
4. For every road segment connected to the junction (except for outgoing one-ways) you now see one big traffic light and
   one small one. The big traffic light tells the cars coming from this road segment if they have to wait (red) or if
   they may go (green). The small traffic light works the same way but is intended for the pedestrians crossing the
   street. On the right side of each traffic light you see two boxes: A counter and a Change Mode button. We will
   explain both shortly.
5. You can toggle the vehicle traffic light (the big one) by clicking on it. You will notice that after you click on a
   vehicle traffic light the pedestrian light will also change. That is the case as long as the pedestrian light is in
   Auto mode.
6. When you click on the little yellow header of the pedestrian light you toggle the pedestrian light mode. As mentioned
   before, pedestrian lights in Auto mode will automatically switch according to the vehicle light state. In Manual mode
   you are able to freely control when pedestrians may go and when they are not allowed to.
7. When you click on the Change Mode button you can define if vehicles going to different directions are controlled by
   their own traffic light.
8. The counter value roughly represents the number of seconds passed since the light switched to its current state.

After leaving the Manual traffic lights mode all traffic lights at the regarding junction are reset such that the game
engine again takes control over them.

![](picLegacyManualTL.png){style="block"}
_Manually controllable traffic lights help you to become familiar with the user interface. Not less, not more._

## Hints & remarks

* Keep in mind that if you want to use directional lights (e.g. separate lights for left, forward & right) you will also
  need separate lanes for these directions (see [](Lane-Arrows.md)).
* [](Reckless-Drivers.md) ignore traffic lights.

## See also

* [](Timed-Traffic-Lights.md)