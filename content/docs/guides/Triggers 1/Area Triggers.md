---
title: Area Triggers
weight: 318
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Short** (7-9 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- Area triggers activate based on the distance between a center object and other objects. Think of them like a collision trigger "over time".
- Every area trigger has a Length, Offset, Target Group, and Center Group option. There are also Area Animate triggers which can edit the existing values of Area Triggers.
- Each area trigger, like Area Move, has unique options which let you customize their behavior.

{{< /callout >}}

** **
# 1: Overview

First, let's go over the options that are found in every area trigger.

The first page of all area triggers will have these options:
- **Length**: The distance an object must be from the center object for it to be affected by the area trigger. 
- **Offset**: Will offset the center of the effect on the x axis, without moving the center object itself.

The two options below are not found in Area Fade and Area Tint:
- **Easing**: The easing the objects should have.
- **Ease Out:** The easing the objects should have when the center moves away from them.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1F7DJyUtT3PWwkRbtpIAxUujXeyf8nQVT/preview?usp=drivesdk></iframe></div>

The second page of all area triggers will have these options:
- **TargetGID**: The objects that will visually change when the center is near them. Can have multiple objects in this group.
- **CenterGID**: The center of the area effect. This object will not visually change and is also a one object group.
- **OffsetY**: This option works the same as Offset but on the y axis instead.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1S4F5ecu8f08S5jmg11OUe9mIuebwaOgr/preview?usp=drivesdk></iframe></div>

- **ModFront/ModBack**: Modifies the length value in front of and behind the center object. Values greater than 1 decrease the length, and values less than 1 increase it. Negative values are treated as 0. These options don't work for the first two proximity options (discussed below)

-# - For the 3rd to 6th options, ModFront is considered to be behind the center object, and ModBack in front of the center.
-# - For the 7th to 10th options, ModFront is considered below the center and ModBack is above it.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/14oJsWPCSA_beutJwyme0oAfuLl9uoWBo/preview?usp=drivesdk></iframe></div>

- **Deadzone**: Will divide the length by this number and change the way the transition is applied at the resulting value. For example if you have a length of 80 and a deadzone of 0.5, the area effect will be fully applied from your player to 40 units (4 blocks) away and will fade out to not applied starting from 40 units (4 blocks) from the center to 80 units (8 blocks) from the center. Note that a deadzone greater than 1 will invert the area effect.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1kb0n_lfULdKxk9jzutz_4QHB5ICjUOAM/preview?usp=drivesdk></iframe></div>

- **Ignore Linked**: When you link objects together and one of them has group/area parent, the linked objects will act as one. Enabling this option will make all the objects act on their own again as if they're not linked.
- **Ignore Gparent**: Whenever an object has group parent enabled, anything that happens to this object will also happen to all the objects linked to this object. Enabling this option will “disable” the group parent and the objects will act as if there's no group parent at all.
- **DEAP**: This stands for “Don't Edit Area Parent”. Normally when there is an area parent involved in an area effect, it will also be affected by that area trigger. Enabling this option won't apply any area effects to the area parent, but it will still be the area parent of the linked objects.
- **Priority**: If several Area Triggers of the same kind are active at once, the one with the higher priority will perform its action.
- **EffectID**: This is an ID that is used to reference a specific area trigger when using Area Animate triggers or Area Stop triggers.

## Proximity Options
These are the 10 buttons found below Deadzone. They control where the area effect gets applied in respect to the center. The arrows indicate what direction the area effect will fade to 0. The dot is the center object for the first two buttons, and the line is the x/y axis of the center object for the remaining buttons.
Here’s a short description of each button in the order left to right top to bottom:

1. The effect is fully applied at the center object and fades to 0 in a circle around the center.
2. The inverse of number 1.
3. The effect is fully applied on the entire y axis of the center object and fades to 0 on the left and right.
4. The inverse of number 3.
5. The effect is fully applied to the left of the center object and fades to 0 on the right.
6. The inverse of number 5.
7. The effect is fully applied on the entire x axis of the center object and fades to 0 above and below.
8. The inverse of number 7.
9. The effect is fully applied above the x axis of the center object and fades to 0 below.
10. The inverse of number 9.

## Special Center Options
These are all the buttons on the right of the second page. They let you choose a center for the area effect without having to place a center object.

- **P1**: Player 1
- **P2**: player 2

The rest of the options are relative to the camera:
- **C**: Center
- **BL**: Bottom Left
- **CL**: Center Left
- **TL**: Top Left
- **BC**: Bottom Center
- **TC**: Top Center
- **BR**: Bottom Right
- **CR**: Center Right
- **TR**: Top Right

# 2: Specific Trigger Settings

Now, we will discuss options specific to each area trigger.

## Area Move
- **MoveDist**: The distance the target objects will move.
- **MoveAngle**: The angle offset the objects should move. 0/360 is down, 90 is to the right, 180 is up and 270 is left. Positive values rotate anticlockwise and negative values rotate clockwise.
- **Relative**: This option will make the objects move the “MoveDist” from the object in all directions. This option ignores any MoveAngle you input.
- **RFade**: with relative the objects move away from the center. Enabling this option the target objects don’t stay away from the center but move over it as if they have a very small length value. The larger the number the smaller the gap.
- **X/Y Mode**: Allows you to input x and y values like in the normal Move trigger.

Note that you can't use Follow triggers to copy movement from area affected objects to another, but Advanced Follow does work.
Also note that for static objects, if the MoveDist is larger than the Length and the objects have 1.00 deadzone some objects will flicker constantly.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1rJ1wUkG08D8gG_dXScg8ttxfHmcmpuHT/preview?usp=drivesdk></iframe></div>

## Area Rotate
- **Rotation**: the angle the objects should rotate at.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1FQ_WuOQxXMVc7tSB1hDrti0TGQr1natj/preview?usp=drivesdk></iframe></div>

## Area Scale
- **ScaleX/Y:** The size the objects should scale to. This is different to the scale trigger as the values in the scale trigger are multipliers and in Area Scale they will *set *the scale of objects.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1qVL1iDI8wHPi_tpH0W-7EY-sH-awsKN_/preview?usp=drivesdk></iframe></div>

## Area Fade
- **From Opacity**: The opacity of the objects closest to the center.
- **To Opacity**: The opacity of the objects farthest from the center.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/10x70JZybtWuv7DdGM_XLih4QxXMfj215/preview?usp=drivesdk></iframe></div>

## Area Tint
- **Color Channel**: the color channel the objects to change to when the center get near them.
- **%**: How much of the color should be copied to the target objects. 0 being none and 1 being fully applied. This is a percentage value.
- **Main Only/Secondary Only**: Will only affect the main or detail color of objects that have a main and detail color.
- **HSV**: Allows you to change the hue, brightness and saturation of the target objects.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1ReSgw764-7_d1eM0pHZnCOdF7FCPWChl/preview?usp=drivesdk></iframe></div>

## Area Stop
The Area Stop trigger works exactly the same as the normal :Stop: trigger, but it's specific to area triggers and works off of Effect IDs.

## Area Animate
Area Animate triggers allow you to permanently change the values of one or more area triggers using either a Group ID or an Effect ID. They are found directly after the normal area triggers.

Note that NA means no change to that specific option. The trash can icon next to each slider will set that value to NA.

All the options in area animate triggers work exactly the same as in the regular area triggers.
- **Duration**: The time it takes to change all of the area triggers' values.
- **Easing**: The rate at which the values change.
- **Use EID(Use Effect ID)**: targets the Effect ID instead of the Group ID.

If multiple Area triggers of the same type have the same Effect ID, whichever Area trigger is applying its effects will be affected by the Area Animate. 

Additionally, note that any Area Animate trigger can affect any area trigger. For example, Area Scale animate can edit Area Move. However, this only applies to options both triggers share (discussed in the “General options” section of this guide). Anything that doesn't match gets ignored.

For example, Area Scale animate can edit an Area Move trigger’s length but not its scale, as no such option exists in Area Move.

<div><iframe src=https://drive.google.com/file/d/1DnHSKTgOMw_iHwaJfYWKfG8qmMeKdotv/preview?usp=drivesdk></iframe></div>





## Credits
Created by @koma5 and @naem
