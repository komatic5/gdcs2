---
title: Player Snap Bug
weight: 412
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Short** (4-6 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- The snap bug is a mechanic created by RobTop to make staircases like the ones from Stereo Madness work indefinitely without the player falling off them.
- It works when the player interacts with two solid objects one after the another, comparing the positions of the player and the objects themselves.
- If the player lands further ahead than when they jumped relative to the block position, then the game moves them backwards.
- If the player lands further behind than when they jumped relative to the block position, then the game moves them forwards.

{{< /callout >}}

** **
# 1: Introduction

The **Snap bug** is an obscure mechanic that RobTop implemented for jumping staircases to function properly.

This mechanic __moves the player based on how they land on a platform after jumping or sliding off another one__, tweaking the position of the player by moving it 1 or 2 units forwards or backwards, allowing the player to climb staircases shown below without falling off from them.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1P5s0WTkfyun-2HB7ytsGegfw89fvWp03/preview?usp=drivesdk></iframe></div>

# 2: Conditions

The game watches for specific conditions to activate the snap mechanic. All of the conditions must be satisfied for a snap to happen and this condition happens every Subframe.

The main hitbox of the player must interact with two solid hitboxes consecutively at a specific distance from each other. This depends on the player's size – that is, if they’re mini or not – and speed.

The interaction may include standing on a block or hitting a ceiling. In the diagram below, an interaction is red to white.

This interaction must not be obstructed by touching another solid hitbox – note that clipping through a block is not considered a solid interaction. This will cause the player to displace by 1 or 2 units, depending on the player’s speed (labeled in the diagram below).

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1nQn12HJ5RSfLPmutMVGFGwnudmmhJFVk/preview?usp=drivesdk></iframe></div>

# 3: Type of Snaps

There are four common types of snaps: +1 snap, +2 snaps, -1 snap and -2 snaps. The game goes through a step-by-step process to determine what kind of snap to use in a given situation. This process happens every Subframe.

1. During the first interaction, before the player leaves the block, the game stores the difference between the current player's x position and the block's x position. Let's call this variable `old_diff` for short.

2. Then, when the player interacts with the next object, `old_diff` is unchanged (it will always change at the end of this process), and the player's x position is stored. Let's call this variable `old_x` since it will change.

3. The predicted position of the player's x position is also stored by adding `old_diff` to the current object's x position the player is colliding with. Let's call this variable `predicted_x` since the player's x position will be set to it in the future.

4. The game picks 1 snap if the player’s speed is 0.5x, 1x or 4x, or 2 snaps if the player’s speed is above 1x except 4x speed. Let’s store this value in the variable `x_shift`.

5. The game then checks if the previously calculated value of `x_shift` is less than the absolute value (aka positive value) of the difference between `predicted_x` and `old_x`. The difference indicates how far the player's current x position is to the player's old x position before leaving the object relative to the current object the player is touching.       
 - If that condition is false, the player's x position is set to `predicted_x`. 
 - Else, the game will check again if `predicted_x` is greater than `old_x`. If that's true, then `old_x` will be added to the `predicted_x`. Otherwise, `predicted_x` will become the difference between `old_x` and the previously calculated `x_shift` (no longer being a prediction of the player’s position). Finally, the player's x position is set to `predicted_x` and `old_diff` is updated to have the new player's x position and the new object's x position. 

The diagram below shows an example of a snap.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1vOOxSbLCNCfe5lvXToJCIYMRUMwMbGh0/preview?usp=drivesdk></iframe></div>

# 4: Setups

This is the simplest snap setup because if `old_x` is past the center of the block, then almost all snaps will be positive. This is what this setup uses to propel the player forwards; however, due to the calculations above, it is **only possible on 0.5 speed**. Also, the setup only works for the cube; however, you can switch the gamemode after the cube goes through the setup. To make one for your speed, read the steps below:

1. Place a 5x block. If you don’t have scale hack, you can save a 5x block from this level `86600819` in your custom objects tab.

2. Place a 1x block on the top right corner of the 5x block if the cube you want to move is in normal gravity, or on the bottom right corner if the cube’s gravity is upside-down. It should look like the image below.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1kG8rWYcpMMQ4cLQsUn09AohAmwClZ8Xq/preview?usp=drivesdk></iframe></div>

3. Now Copy+Paste this and move it right by one block. 
 - If the cube you want to move is in normal gravity, move the blocks down using the smallest arrow in the edit tab. 
 - If the cube is upside-down, move the blocks up using the smallest arrow in the edit tab. 

4. Repeat step 3 until you are satisfied. Your setup should look like what is shown below.

Normal gravity:

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1h5tGVYbrcc31IEAMWy7whiYHLpBGq7xi/preview?usp=drivesdk></iframe></div>

Upside down gravity:

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1q8lnflgI9nGDz491xYYI7rYAlHwOcC23/preview?usp=drivesdk></iframe></div>

**NOTE:** This setup above is highly FPS dependent, meaning the player will move forward on a larger distance on higher FPS than on lower FPS due to the fact that more FPS has more subframes. Tax Evasion by Skub uses a more stable but inconsistent setup that is not FPS dependent.

{{< youtube oeIzV2SgZFY >}}

The setup is shown below.

<div><iframe src=https://drive.google.com/file/d/1wJZGf03brHXm2Nx9yNxT73O7pf6Gch66/preview?usp=drivesdk></iframe></div>

## Additional Resources
If you don’t want to bother calculating everything by hand, MateussDev has created a [convenient calculator](https://www.geogebra.org/calculator/nzeyrb27) that calculates snaps like shown above, and has the ability to tweak values very fast.





## Credits
Created by @DangerChampion and @MateussDev
