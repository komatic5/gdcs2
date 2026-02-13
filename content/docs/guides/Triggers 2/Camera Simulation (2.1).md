---
title: Camera Simulation (2.1)
weight: 619
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Short** (8-10 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- The rectangular field that you can see on screen is the camera.
- There are 2 modules to simulate this camera: with borders and without borders.
- The camera simulation with borders cost at least three groups.
- For the robot/cube, the camera simulation will cost seven groups, if you don’t plan to change the gravity.
- With gravity changes, at least two groups will be needed for spawns.
- When starting out, choose one of these modules; it will save you the headache.

{{< /callout >}}

** **
# 1: Camera

Before we go to the meaty part of this guide, let’s take a look at the **camera**. Simply put, __it captures the screen of the device; the rectangular field that constantly follows the player__. Regardless of your device, your screen’s height will remain exactly `10 ⅔` blocks tall. However, your screen’s length depends on your device’s aspect ratio: Standard Aspect Ratio (`22` blocks) vs. Widescreen (`24` blocks). But there are other lengths beyond these two ratios.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/143OLGl-IVvywoqZpSMG44NJStYzA1PF0/preview?usp=drivesdk></iframe></div>

If you manage to simulate this camera, you can upgrade the parallax in your levels, similar to the mini cube part in `So` by `Neigefeu` , and `YoReid`’s part in `Planet X` . Both horizontal and vertical parallax are considered for this setup. Additionally, if you want to create effects that stick to your screen such as song lyrics or raindrops, this will be useful.

In addition, you’ll notice that most gamemodes have fixed borders at the top and bottom, even the duals. However, only the robot and cube gamemodes are borderless. This will change in 2.2 once Free Fly Mode is introduced for all gamemodes. As of 2.1, there are two ways to set up the camera: with borders and without borders. We need this distinction because the camera’s modules will differ greatly.

{{< youtube 8G_8F2tXYpw >}}

{{< youtube fPXLGli6XGw >}}

# 2: Camera Simulation with Borders

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1-p29Rjw-yf8K3hhSwzdi6qRRvkFktAGx/preview?usp=drivesdk></iframe></div>

Search for this level with the ID: `90903111` in order to check the camera simulation with borders.

Gamemode portals with fixed borders can move the camera depending on their Y-position. While locking the visuals in the X-position is simple, the Y-position is where things get tricky.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1VQ3DroGjgLfe679BfHCdt2oFAEHUNlIS/preview?usp=drivesdk></iframe></div>

You can simulate this movement into your objects with the help of a move trigger. From trial and error, the move trigger’s setup needs to have these units so that your objects can match with the camera’s movements, regardless of the Y units you add. Though as a safeguard, keep your Y units below `50` units.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1JckmsuysCNpa0w15u957iQZ8ZIWLtok9/preview?usp=drivesdk></iframe></div>

However, where should you place this move trigger? Do you snap it in the same grid with the portal? For simple camera locking, yes. This is because the portal’s hitbox and the move trigger’s hitbox would align perfectly.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1zIbh-SLUk0Hu_JhFusYB-BKaF7-6UFAN/preview?usp=drivesdk></iframe></div>

However, refresh rates complicate things. Depending on your game’s refresh rate, it detects the timing of your camera differently. This is not really an issue when it comes to simple camera visuals, but with more complexity in parallax, this needs to be taken into account. This will be more taxing for the borderless camera setup later.

## Hitbox Issues

Different gamemodes can shrink or expand the player’s hitbox, causing inaccuracies in the camera’s movement. For example, going from ship to wave, the hitbox will shrink; additional corrections need to be made for your setup. With modding apps such as Megahack, you can align these triggers with the respective hitboxes.
    
## Overlaps in Camera Duration

Sometimes, you may place your gamemode portals too closely, that the previous camera movement gets interrupted by the next. How would the setup simulate that? The issue is they won’t run at the same time, because they are exclusive. 

Starting a camera movement will automatically negate all camera movements before it. This is an issue because previously, you can merely type your Y-units and the camera will move accordingly. In the case of overlaps, your move triggers need Use Target while also stopping the previous triggers using a stop trigger.

## Overlap Setup

1. The first move trigger instantly moves a one-object group up and down depending on the portal’s trend. Place this to the left of each portal.

None

2. The second move trigger has Use Target where another one-object group moves to the previous group’s target position in step 1. Set the easing to “Ease In Out” with 1.4 easing rate and 0.4s move time. This will be spawn-triggered and multi-triggered to 2 more groups.

None

3. A touch-triggered spawn trigger is exactly aligned with the portal to activate the object in Step 2. Meanwhile, a stop trigger is placed slightly to the left of the spawn trigger to interrupt the camera movement. Set both of these to a Follow Player Y trigger to ensure they will be touched.

None

4. Group your visuals to a follow trigger with the follow ID from Step 2. Locking visuals will have `0` in the X-Mod and `1.00` in the Y-Mod. If you need vertical parallax, add another follow trigger and change the Y-mod to your liking.

None

5. Playtest. Slightly move the triggers in Step 1 if the camera fails to move the whole way. The bordered setup is complete!

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/139Zq-uvq24NhxyFw3n-xweIOXhdM1XjO/preview?usp=drivesdk></iframe></div>

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1X32WKG2c8v_9HzHrK12Hud8fb2sWBPAb/preview?usp=drivesdk></iframe></div>

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1bBp4cVypgzpXzYdcKjngJ6H-azHekODF/preview?usp=drivesdk></iframe></div>

However, this is not the only camera setup that you can make.

# 3: Borderless Camera Simulation

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1HRzjNHj7d42qaI6HGqaialY8o2WwY2qJ/preview?usp=drivesdk></iframe></div>

Search for this level with the ID: `92313313` in order to check the camera simulation without borders.

However, notice that for the robot and cube gamemode, the camera only moves if the player goes near the screen’s edges, so how would you simulate the camera with that condition? Referring to the trigger workflow, let’s specify the function, module, and truth conditions:

> **Function**: Make the camera visuals lock to a borderless camera in the Y-axis. If the camera goes up by 10 units, the visuals go up by 10 units at the same speed. Because this is borderless, we need to take into account both the top edges and bottom edges of the screen.

None

> **Module**: You’ll need two sets of collision blocks to build an **adjustment area** to the camera visuals; they are located at the top and bottom of the screen. For normal gravity, the upper adjustment area has 3 blocks, while the lower has 4 blocks. These blocks need to be grouped to a follow trigger where its X-mod needs to be `0` to avoid the blocks from moving horizontally.

None

> **Truth Condition**: Following Pin - A square with a Follow group ID which will move the camera visuals and adjustment area when activated. You’ll want to set the speed of the follow player Y to `0.1`. In this case, there are two truth conditions for the top and bottom areas of the screen. If the player passes either areas, the module will activate.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1FBoPg6nlkzj0M6uB8ws-UgOpjn2vlC3u/preview?usp=drivesdk></iframe></div>

As a result, the setup looks like this, where the screen’s height is roughly `10.7` blocks.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1k1mYRoFKFVz9_73yKsVwUgBI3Kjr-i_Z/preview?usp=drivesdk></iframe></div>

Its trigger work will look like this.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1fsZN_rQm1clu6zt59d2rAELP80iL_KyO/preview?usp=drivesdk></iframe></div>

Referencing the image above, seven groups were used for the Y-lock:

- Group `2` makes the camera module and visuals follow the following pin when activated.
 * For vertical parallax, you add two extra follow triggers for each adjustment area targeting a new group, then tweak the Y-Mod numbers to not equal `1.000`.
- Groups ‘3’ and ‘4’ are the following pins when the player touches either adjustment areas. They also follow each other when this happens.
- Collision triggers that target groups `5` and `8` will activate the camera module and move the visuals. The difference is the adjustment area that it affects. Group `5` targets the top adjustment area while group `8` targets the bottom.
- Collision triggers which target groups `6` and `9` use “Trigger on Exit”: when the player leaves the adjustment area, the camera stops following the pin.
- With unique group IDs, two separate Follow Player Y triggers are placed depending on the adjustment area.

Most importantly, set the spawn-triggered triggers as “Multi-trigger”.

## Borderless Setup

1. Let’s start with making some cube gameplay.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1V4mZVCScPMn7MhTup7USnVwJRy-68L9A/preview?usp=drivesdk></iframe></div>

2. Identify the initial/starting camera position. As the previous part is a dual, it’ll be easy to pinpoint the exact camera position, and build the module upon.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1_soEHhOqIuBJ-rk1573qUH6K2AglJU9R/preview?usp=drivesdk></iframe></div>

3. Roughly measure the initial position to the closest you can get.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1Vap6wI_sE4wc-f1kDZshCsxz5G8DoKK1/preview?usp=drivesdk></iframe></div>

4. Build the player’s collision hitbox and mark this as a dynamic block. Additionally, set the Follow Player Y’s Speed to `5.000` so that the collision block can follow the player more responsively.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1Jr9YHaZ0u1tWT_cm6_4qERbk3PIt4__l/preview?usp=drivesdk></iframe></div>

- If you have scale hack, you can even reduce the collision box’s size to `0.01` for extra accuracy. This is provided in the uploaded level.

None

5. Build the adjustment area and the necessary triggers.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1BhZno2o4bH-0so5JRTfL78g8YJdPbUEu/preview?usp=drivesdk></iframe></div>

6. Playtest.

<div><iframe src=https://drive.google.com/file/d/1UQ-1tyktyGsc147Y_ODBvoydoj7FP4WK/preview?usp=drivesdk></iframe></div>

Now that the main part is finished, it should be able to work without gravity changes. If you want gravity changes, however, there are extra steps to go through.

## Adding Gravity Changes

Recall how the bottom adjustment area has one extra collision block than the top? This needs to change when the player goes upside down. Putting the numbers, we need to shift this module downwards by `10` units, then return to its original setup in normal gravity. Referring back to the trigger workflow, switching gravity complicates the module and truth conditions.

None

Adding this setup costs two extra groups for the touch-triggered spawn triggers which act as truth conditions for the gravity changes. However, feel free to replace it with other spawns; for example, when it comes to blue orbs, toggle orbs are much more effective than spawn triggers as they activate alongside touching the blue orbs.

Triggers on the right side are activated when the player goes upside-down. For the move triggers, they shift the collision blocks and following pins downwards by `10` units; they move instantly by `0` seconds. They move back up by ‘10’ units to their original position when the player is right side up.

Triggers at the centre activate by either spawn triggers. Think of it as an OR gate. The stop trigger is activated so that the Follow Player Y trigger doesn’t interrupt the move triggers. 

The toggle triggers at the bottom acts as a calibration sequence for the camera module. You know how when your laptop suddenly has problems, you turn the laptop off and then on again? That’s what the toggle triggers are doing for the gravity change.

None

Ultimately, the borderless camera setup with gravity changes is complete.

None

None

As a precaution, stick to building either the bordered or borderless setup separately.



> **Research and Examples:** @Chunlv1 @Unknown @Selena 🦄 @koma5

