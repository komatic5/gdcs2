---
title: Scale
weight: 310
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Tiny** (2-4 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- The scale trigger changes the size of objects set from their individual centers or center point.
- You can multiply or divide an object’s size
- Changing only one of the axis in ScaleX/Y allows you to squash or stretch objects.
- With Relative Scale, the trigger uses the center group ID as a reference to scale.

{{< /callout >}}

** **
# 1: Features

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1g8vB3toUYUxIGd-5Q4Zlclt1s_p238zG/preview?usp=drivesdk></iframe></div>

- Target Group ID: The ID for the objects you want to change the scale of.
- Center Group ID: *Similar to the rotate trigger’s center group ID*, this is a one-object group. It’s a center that objects should scale from. If you leave this box empty, all objects will use their own Centers.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/15HW7rOqiyUGsHcXurIUbT063fjPEQtwp/preview?usp=drivesdk></iframe></div>

- ScaleX & Scale Y: Lets you squash and stretch the targeted objects by using the sliders or typing in the value.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1rJG1xCjXct9eXFszF2FNBGvaWFISqVd1/preview?usp=drivesdk></iframe></div>

- Div by Value X / Y: Divides the current scale by the values put in the ScaleX / ScaleY boxes.

Let’s say you have a block that’s scaled up 3 times. Normally, you can’t revert it perfectly back to normal, but with this option enabled, you just need to put the same values you scaled the object by and it will revert back to normal.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1sezV-RCL0HUmu_gDPGV9u3J1py34pZ7y/preview?usp=drivesdk></iframe></div>

- Only Move: Moves objects the way they would otherwise be scaled without actually scaling them. This option only works if you specify the Center Group ID.

<div><iframe src=https://drive.google.com/file/d/1NUioctF0Ts4s4afs70S68KBKuvfmglfp/preview?usp=drivesdk></iframe></div>

- Relative Rotation: By enabling this option, all assigned objects will remember where their X and Y axis were, but what does this mean exactly? Normally, when you scale an object, it stretches in the X or Y axis *(horizontally or vertically)*. However, that doesn’t take into account their rotation, which can give you different scaling results when you play. Enabling this option ensures that the end results scale consistently.

In the example below, I used 2 x scale on the X axis and rotated the blocks by 45 degrees.

None

- Relative Scale: This option uses the reference object / the center ID to calculate the scale. Normally, if you scale an object down, the object’s scale will change each time. When this option is enabled, the Scale Trigger will instead refer to the Center Group ID to determine what the new scale should be.

None

Similar to the move and rotate triggers, you can apply easings, and make it activate on touch-triggered / spawn-triggered.
## Pre 2.2 Scaling
Before 2.2, scaling was achieved by using plenty of groups and follow triggers, which was unoptimized. JamAttack made a video in which he discussed and explained this method.

{{< youtube FzVIs43rNUs >}}



## Return to the [Table of Contents](https://discord.com/channels/414295025883545600/1194068611409661983/1194068611409661983) here



## Credits
Created by @EYZ and @Selena
