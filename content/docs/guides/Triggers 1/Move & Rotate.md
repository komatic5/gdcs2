---
title: Move & Rotate
weight: 308
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Short** (4-6 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- The Move Trigger changes the location of objects. You can enter specific coordinates (e.g. move 3 blocks to the right, then 5 up), or use Move To Target to move one object onto another.
- You can use the Lock to Player X/Y features to copy the player’s movements onto a group, and Lock to Camera X/Y to copy the camera’s movements.
- The Rotate Trigger rotates objects around a center point. You can use Degrees to determine how many degrees objects will rotate, or Times 360 to determine how many full revolutions they should make.
- Static objects (ones with hitboxes) will have their rotation locked no matter what.

{{< /callout >}}

** **
# 1: Move Trigger

The Move trigger moves objects using their X and Y coordinates. Positive X values move objects to the right, and positive Y values move them up. Negative values do the opposite.

This will move objects from their relative positions, so you can’t move an object to a specific location without doing a bit of math to figure out where that location is. However, note that a value of 10 will equal 1 block, so inputting “+10” into the X input will move your object 1 block to the right.

Enabling **Small Step** will make your input values three times smaller, so inputting “+30” into the X input will move your object 1 block to the right instead of 3.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1xhyGH7BO2PyFwz8a0gR_tu9MuoMoEkYS/preview?usp=drivesdk></iframe></div>

The “Lock to Player X” and “Lock to Player Y” checkboxes copy the player’s X and Y movements, while the “Lock to Camera X” and “Lock to Camera Y” checkboxes copy the camera’s X and Y movements. You can also add multipliers to these options, making objects move at half of the camera’s speed for example.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1ZTJ50v4AhTcneIj9cxz0h5A3tPM9sudN/preview?usp=drivesdk></iframe></div>

**Target Mode** lets you move an object to the location of another. You’ll need two groups; the Center Group ID is the object that moves to the TargetPos Group ID’s position. Both groups need to either have one object or a Parent Group in them to work, and you can copy this movement to your Target Group ID accordingly.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1tdFbSdKkOmrktdTQIGCv0AzjLLX8jqxI/preview?usp=drivesdk></iframe></div>

**Direction Mode** moves an object in the *direction* of another by a certain number of blocks. As with Target Mode, you’ll need two groups and the Center Group moves to the TargetPos Group ID’s position. The “Distance” modifier determines how many blocks to move the Target Group; as before, 10 units equals 1 block unless Small Step is enabled.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1ezTR5yTmITNbhcPtb13EqbPcjUI4FpR2/preview?usp=drivesdk></iframe></div>

Enabling **Dynamic Mode** on either Target or Direction Mode will constantly update the positions of your TargetPos Group ID. This [target tracking](<https://discord.com/channels/414295025883545600/1157751217456435260/1157751933340242022>) lets you automatically make changes in real time.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1B0smjmwGudlZ9908P-R3cPYkEtDA60fb/preview?usp=drivesdk></iframe></div>

**Easings** change how much your objects accelerate as they move. Some easings also have an **Easing Rate** option which changes how much they accelerate over time; an Easing Rate of 1 is linear, while a rate of 3 would be cubic. You can view a graph of all easings [here](https://www.desmos.com/calculator/xt4ddwuihh).

**Silent** changes how the player interacts with moving blocks in platformer mode. Normally, the player will move alongside blocks that move instantly; however, the Silent checkbox means the player can’t stick and will retain the same position as before.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1v0ni3Twm6O6ygsK4YgX3u_lC_LMqpg8S/preview?usp=drivesdk></iframe></div>

Move triggers will always stack, which lets you combine their easings in interesting ways. For example: The easing implementation for “Ease Out” is incorrect, and you can tell this by stacking a trigger with No easing and one with Ease In.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1dA2a5UAW-zzqsiYC3hatv9EArFDGtv_a/preview?usp=drivesdk></iframe></div>

# 2: Rotate Trigger

The Rotate trigger rotates objects around a center point. This center point must be a one-object group or a Parent object; without it, objects will rotate around themselves, or not at all.

**Degrees** describes how many degrees to rotate objects - positive values rotate objects clockwise, negative values rotate them counterclockwise. **Times 360** describes how many full revolutions the objects should make.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1Yldj4lPkVW-NSecpV_L3u0HRW4s0eqMj/preview?usp=drivesdk></iframe></div>

**Lock Object Rotation** lets the objects rotate around the center point without changing their actual rotation.

You’ll notice that some objects will always behave as though Lock Object Rotation is enabled. These are typically **Static** objects - ones with a hitbox the player can interact with, such as blocks. You can use the “Rotate Static Objects” option in Level Settings to make these objects appear to rotate properly, but their hitboxes will not update accordingly. If you want your static objects to actually rotate, make an invisible copy of them and then give the visible objects the "NoTouch" setting.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1vFPV93hmf0uuzkwiU7QeGrku0pKEY-8Z/preview?usp=drivesdk></iframe></div>

**Aim Mode** rotates your Target Group to face your “Rot Target ID” group. You can use the “Rot Offset” input to offset this rotation by a certain amount of degrees, and the “Dynamic Mode” option lets you update this rotation in real-time. Enabling Dynamic Mode will also let you set an infinite move time (duration -1), and also gives you access to an Easing slider that replaces the normal easings.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/16emFGT4gLUitXabj-0Tm1qVhn0opC0sd/preview?usp=drivesdk></iframe></div>

Aim Mode also gives you access to a new page with MinX, MaxX, MinY, and MaxY IDs. These will set a boundary for your rotation, so your objects won’t be able to move further left than your MinX ID or above your MaxY ID.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1svui17C_3UK-Ea4lAOofFRYrGY769sqF/preview?usp=drivesdk></iframe></div>

**Follow Mode** lets you copy the rotation of an object. The rest of the options here are similar to those in Aim Mode.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1SYPvYmM8u8jzFxZlsYkYeYHOO7Gf2TJm/preview?usp=drivesdk></iframe></div>

Rotate triggers will always stack in Update 2.2, but this used to not be the case. Beforehand, activating a new Rotate trigger with the same groups as an old one would override the first. This option can be configured with the “Allow Multi-Rotation” checkbox in level settings.

<div><iframe src=https://drive.google.com/file/d/1rlRJ5t_-tIM9qMsGAzo6-LaRMuw2NlBv/preview?usp=drivesdk></iframe></div>





## Credits
Created by @koma5
