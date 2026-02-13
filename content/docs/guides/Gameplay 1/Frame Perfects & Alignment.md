---
title: Frame Perfects & Alignment
weight: 410
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Short** (6-8 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- We described the different types of frame-perfects and how to construct them.
- Discovered the internal mechanics of how frame-perfects work.
- Understood the purpose and fundamentals of frame alignment.

{{< /callout >}}

** **
# 1: What are Frame-perfects?

**Frame-perfects** are __timings that have a window of one frame to click.__ These are usually difficult due to the little to no error needed to pass, but there are variations of a frame-perfect.

- **Hard Timing**

Hard timings are almost frame perfect, having a window of 2-5 frames at N FPS.

- **Common Frame-perfect**

A common frame perfect is a timing with a window of 1 frame at N fps. Due to changes in the game’s physics, most of these are broken without the use of a physics bypass, as 240fps makes the room for error larger than normal.

- **Frame Gate**

A step up from the common frame perfect, being possible on only N FPS. These usually include jump height differing with FPS, subframes, or the Rotation hitbox. They’re much harder to build and force the player to play the level at any FPS the creator desires.

- **Swift Click Timing**

Usually isn’t a frame perfect, but rather a clicking type, requiring the player to click and release within 1 frame. This becomes exponentially harder the higher the FPS. These are commonly used in most modern impossible levels due to the effects caused by the players’ gravity when using a pink dash orb.

- **Alignment Frame-perfect**

One of the hardest timings, relying on the change of the position of the player and how many units the player moves in a frame. Most of the time these are made accidentally, and technically any frame-perfect is an alignment frame perfect.

Frame-perfects can be made on any FPS or gamemode. Usually ones involving a snapping gravity like the spider or wave tend to be easier than the rest, while modes based on a curve in gravity like the ship are harder due to the floatiness and unpredictability.

# 2: How to Create Frame-perfects

## Copy an existing Frame-perfect

People have made many hard levels, meaning there are structures for the common 60, 144 and 240 FPS values. 360+ frame-perfects are rarer due to hardware limitations.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1jtyOjjWAMvQj6rxnxt24p5NQeEHyo54J/preview?usp=drivesdk></iframe></div>

## The Macrobuff Method

This is a more complex method which can be used with macro recording software to build a frame-perfect. The steps to construct one with macrobuffing are shown below.

1. First, create any timing that is close to frame-perfect. A triple-spike will usually do the job nicely. Also make sure to decide which FPS the jump should work on.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1go5minGusmaU0iLlWUWk5jAr9IDWnmTI/preview?usp=drivesdk></iframe></div>

2. Record a macro of that frame-perfect. To save time you can place a start position, but if you don’t want to risk accidentally making an alignment frame perfect then bot from 0% and make sure to hit anything that misaligns you *(Speed portals, mirror portals, platforms [only for y align], etc.)*. If you don’t have a macro bot, then you can play in the editor with hitbox trail on and continue from there.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1k1aB_V6LQQdR2SUv9cVZEWxMFLusI663/preview?usp=drivesdk></iframe></div>

3. After botting, you simply buff the timing to barely touch the hitboxes. Hitbox trail is required here. Take note the ways the game handles collisions to create a unique frame perfect and avoid obvious issues with physical possibility of this timing.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1qUV6qOsxtcMJ6gTBoI4Wq7LK96CGL4Le/preview?usp=drivesdk></iframe></div>

4. Test the frame-perfect. Make sure it’s physically possible by playing the macro you recorded. If it is, place a start position and test the frame-perfect yourself. *(For MHv7, the trajectory tool does not accurately show whether a timing is physically possible, especially at higher[>360] and lower[<144] FPS values)*. Use the frame stepper to accurately test it.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1X8ex5udEEG6X4aGStp8eVrzQp0GEnzC2/preview?usp=drivesdk></iframe></div>

# 3: Extra Details

*Everything described here is nerdy stuff about how frame perfects work and some ways to troubleshoot them.*

- Despite its many references and its wide use in the GD community, pixel-perfects don’t exist in GD due to how the game calculates positions using units instead of pixels, as well as the size of 1 pixel in units being inconsistent with different monitors and resolutions in windowed mode. The closest thing to a Pixel perfect is a Hitbox perfect, where the hitboxes of the player are mathematically as close as possible to the player.

- While you can make a frame perfect with any gamemode, each mode has a different difficulty of frame perfects. The easiest are usually wave frame-perfects, since it’s easy to predict trajectory. After that comes spider frame-perfects, which are slightly harder to predict due to how tight the hitboxes are. Ball frame-perfects are next, which are slightly easier than the Cube and UFO. The hardest ones are with the robot and ship modes due to them requiring a release at a frame-perfect interval.

- Any frame perfect timing on N FPS will be physically possible on double N fps and above, however these timings can be possible on higher or lower FPS with the help of alignment.

- Decimal-based frame-perfects can exist as well, which can be used to force the player to play at a very specific FPS to complete the jump. For example, you can set it up to make it possible on only 59.69 FPS.

# 4: Alignment

Sometimes you’ll notice your frame-perfect you copied is physically impossible in your level, even though it's possible in the level you copied it from. This is usually **Alignment** to blame. 

**Alignment** is the __value in the player’s position, rotation or location of subframes that is smaller than the distance in units the player takes in one step, causing it to persist until another event happens that causes it to change.__

Let’s imagine the player is running the game at 60 frames per second, and the X position is changed by 1 unit every frame.

The player’s location will change like this:
1.0 → 2.0 → 3.0 → 4.0 → 5.0 → 6.0 → 7.0 → 8.0 → 9.0 …

Now imagine that a mirror portal offset the player by 0.1 units. 0.1 is smaller than the player’s speed, so it will persist. 

Now our X position will look like this:
1.0 → 2.0 → 3.0 → 4.1 *(entered mirror portal)* → 5.1 → 6.1 → 7.1 → 8.1 → 9.1 …

0.1 is alignment of each movement after colliding with the mirror portal.

This slight discrepancy can create an **Alignment frame-perfect**, since with a different alignment the checks for collision with hitboxes will be changed, possibly making the timing physically impossible. You can have an insanely small change in alignment due to the **Snap bug** which usually doesn’t affect anything unless your timings are very tight.

## How to Avoid/Force Alignment?

- **X Pos Alignment**: Happens with rotated speed portals, mirror portals and Snaps.

- **Y Pos Alignment**: Happens depending on how the player enters a wave portal, size portal, the ufo click pattern, as well as velocity of the ship. Hitting the ground or a platform will reset this alignment to where the platform was placed vertically.

- **Rotation Alignment**: Depends on the orb patterns, ball gameplay and ship velocity.

- **Subframe Alignment**: A difficult alignment that is usually not used in many cases. X and Y positions of the player can affect how subframes can change, due to how the game processes them.

## Alignment on Different FPS

Alignment is also a term that describes the difference in positions of FPS.

Each colored line represents a frame within the game, and the position represents the player at each frame. 120 FPS has twice the frames as 60 FPS, so the distance the player travels in a frame is half.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1tv1vN6B1wg5qbfYUfGyrp0BRiQ0G9NzL/preview?usp=drivesdk></iframe></div>

Since 120 is a multiple of 60 the positions at certain frames match, you can mathematically assume every frame-perfect on 60 FPS is possible on 60*N or 360+ FPS.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/16nKf7XL1EtmdWicG2MwgkHtMcyQ3-3AJ/preview?usp=drivesdk></iframe></div>

However FPS values that are not multiples have a different outcome: They won’t match, only having certain frames that match the given FPS. This explains why levels are possible on FPS values that are not a multiple of N FPS (eg: VSC is possible both on 60FPS and likely on 144FPS)

<div><iframe src=https://drive.google.com/file/d/1iDNq7WqgACRmhtrCTWJjUp4iOX-g8ixg/preview?usp=drivesdk></iframe></div>





## Credits
Created by @MateussDev and @NotAModerator
