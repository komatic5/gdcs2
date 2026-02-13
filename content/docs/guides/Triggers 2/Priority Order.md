---
title: Priority Order
weight: 603
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Short** (5-7 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- Ordering of triggers is important, as it prevents possible randomness in the way they fire.
-  Priority Order is a hidden system that determines which objects get processed first, such as collision blocks, stacked orbs, and triggers on the same X axis.
- There are plenty of ordering algorithms that the game puts into place, but you can change this yourself with the Trigger Order option found in the Edit Group menu.

{{< /callout >}}

** **
# 1: Priority Order

Geometry dash is separated into invisible sections 100 units (3.33 blocks) wide, and infinitely tall. They can’t be seen in the editor, but if you could see them they’d look like the orange lines in the image below. These sections help determine the priority or order that objects or triggers activate.

None

The rules for Priority Order are as follows:

- Each section has its own priority. Sections further left in the editor will have higher priority than ones to their right.
- Priority order is determined within a section. Think of it as a “list” detailing all the objects in a section and where they stand on the game’s priority.
- When an object is added to a section or moved in from a different one, it’ll have the lowest priority of that section.
- When an object is deleted or moved out of a section, the object with the lowest priority will take its place on the priority list. For example: If the list is `1, 2, 3, 4`, and object `2` is removed, then the new priority is `1, 4, 3`.
- In **Update 2.1,** priority order is saved between attempts. 

Remember that Priority Order doesn’t care about an object’s X position, as long as it’s within the same section.

Here’s an example of Priority Order at work. The yellow orb has a priority of `1`, as it’s the first object in this section.

None

The purple orb is placed within the same section as the yellow orb, so it gets the lowest priority of `2`.

None

The red orb is added to the section to the left of the other two orbs. It gets the highest priority since it’s in the leftmost section.

None

The red orb is moved into the section with the other two orbs, so it gets the lowest priority. The purple and yellow orb gain priority as a result.

None

The best way to check an object’s priority is through layering. If two objects share the same Z layers and Z order, the object in front will have lower priority than the object behind it. This will only update in the editor when you save & exit, then re-enter the level.

# 2: Applications

In this section, we’ll focus on some applications of Priority Order and how you can use it for yourself.
## Changing Priority Order

Changing the Priority Order of two objects in the same section is fairly easy. Take the object with the highest Priority Order, move it at least three and a half blocks to the *right* of its original place, and then move it back where it was before.

For example, the yellow orb in this image has a priority of `1` while the purple one has a priority of `2`.

None

Moving the yellow orb into the next section resets its priority.

None

Then, the yellow orb is moved back - resetting its priority and switching the locations of the orbs on the priority list.

None

This can be done inside a level with move triggers, and lets you change the priority of orbs, collision blocks, and object Z layers. However, it’s much more finnicky for triggers because they can’t be moved on the X axis using move triggers.

## (2.1 Only) Saving Between Attempts

One of Priority Order’s most useful features is that it saves in between attempts. Since you can change it using move triggers, it’ll be saved for the next attempt - letting you save information between attempts.

Most importantly, this info will only save when you’re inside the level. If you exit then the priority will reset and that data will be lost. This will be expanded upon in the Binary Save lessons.

Here is a basic example of using portals of saving data. In the video below, you enter the portal with the highest priority taking you to one place. The portal is then moved to the right and back, setting it to the lowest priority. On the next attempt, you enter through the other portal as it has a higher priority.

None

Be aware that *Priority Order does NOT save between attempts in 2.2, only in 2.1*. However, Update 2.2 also introduces the **Order** system which also impacts how triggers work.

In most cases, triggers aren’t commutative, meaning that the result can vary drastically depending on the order they activate at. Setting up when triggers activate ensures you get the wanted results.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1lm3i9O7tO8LkgIBDe2HcaC8CwuauGQFF/preview?usp=drivesdk></iframe></div>

# 3: Simultaneous Ordering in 2.2

In certain cases, the game will order what triggers activate first to prevent unwanted randomness. An example of this is 2 pickup triggers activating at the same time, where trigger A  adds 1 to itemID 1, and trigger B multiplies the itemID 1 by 10; what will the final ItemID value be? The result can either be 1 or 10 based on which trigger activates first.

In order to eliminate randomness, triggers activated on the same frame happen in a set order, much like how a calculator processes mathematical operations. The game uses 3 different ordering algorithms to achieve this.

## Left to Right Priority
If "spawn triggered" is enabled, triggers will be activated from left to right, meaning the leftmost triggers will activate first, cascading until the last trigger is activated.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1AIcDUWLsr-DMH_zoYzhk0-NCkkYOE33L/preview?usp=drivesdk></iframe></div>

## Order Value Priority:
**As of 2.206, this feature suffers from multiple bugs, and should be avoided when possible until it’s fixed.** This can trigger on portals, pads, and orbs but has no visible effects. This can also break triggers if they aren’t set up properly.

This feature is only used for regular or touch-enabled triggers. Their order values are compared in ascending order, meaning the triggers with the lowest value activate first. You can change a trigger’s order value in the bottom left of :EditGroup:, and a trigger’s value must be larger than all other triggers before it in order to prevent breaking.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1YA2-6TemcOYSchI5TcjdrLDRRvxbKRAR/preview?usp=drivesdk></iframe></div>

## Placement Priority:
In the case of 2 or more triggers having the same X position and the same order value, the most recently created trigger will activate first, with the oldest activating last. For example, copy + pasting a trigger means the copy will activate before the original.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1-rB2P-jHWF8MdOLk3OSquluQ0xbosQnR/preview?usp=drivesdk></iframe></div>

## Order Inheritance:
An important thing to note is that a trigger’s priority depends on the previous triggers’ priority, so the order of 2 triggers activated by different spawn triggers is based on the order of these spawn triggers.

<div><iframe src=https://drive.google.com/file/d/156OvgVeq67cOymS_k4FDVTaCTbZbwlkL/preview?usp=drivesdk></iframe></div>





## Credits
Created by @NotAModerator and @𝕋ypexleta
