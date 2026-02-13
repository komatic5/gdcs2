---
title: Stop
weight: 341
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Tiny** (1-3 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- The Stop trigger ends the action of an active trigger.
- The Pause option puts the target trigger “on hold” and allows it to be resumed by the Resume option.

{{< /callout >}}

** **
**1: Stop Trigger**

The Stop trigger is the 4th trigger found in the trigger section in the editor. The Stop trigger halts any active triggers it targets. Any triggers with a finite duration, like Pulse, Color, or Move, can be stopped using it.

To use the trigger, simply assign a Group ID to the trigger you want to stop. Then, enter that Group ID into the Stop trigger. Once it activates, that trigger will stop working.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1SapMrFYhRatY7UZlbpu8OZz2R5gvJ0nV/preview?usp=drivesdk></iframe></div>

As shown, the block stops following the player once the stop trigger is activated. The Stop trigger will always "stop" actions of the triggers it targets.

Note that Stop triggers can crash the game if used in certain ways. If a Stop trigger is activated by a Spawn trigger, which itself stops the Spawn trigger, the game won’t know what to do, and will just decide that the best course of action is to close the game.

**2: Pause and Resume Options**

Pause and Resume are two new options in the Stop trigger. The Pause option acts similarly to the stop trigger, however, triggers can resume their functions when targeted by a Resume option. The Resume option takes the remaining trigger data and uses it to finish what  was originally paused. 

To use these options, place down a Stop trigger, go to :EditObject: Edit Object, and click on "Pause" or "Resume".

<div><iframe src=https://drive.google.com/file/d/1OX2Cu1LMZ4FiB97qG_yvA-rVfF7F40sG/preview?usp=drivesdk></iframe></div>

The Resume option does not have to target the same group as the original Pause option. As long as a trigger has been affected by a Pause, a Resume trigger can resume its actions.

These triggers also interact with each other in unique ways. For example, you can’t use a Pause or Stop trigger on another Pause/Resume trigger. If you want to stop/pause a Resume trigger, you have to stop or pause the original group. Similarly, you can’t pause or resume a trigger which has been stopped *until it’s activated again*.



**Credits:**

> **Research & Examples**

  @TDP9

> **Proofreading**

  @Half-Cooked Ramen

Changed the channel name: Stop

