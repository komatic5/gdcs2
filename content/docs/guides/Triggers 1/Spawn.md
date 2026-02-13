---
title: Spawn
weight: 334
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Short** (4-6 minutes)

# 1: Activating Triggers

To understand why the Spawn trigger is important, we have to first discuss how triggers get activated. Normally, triggers activate when the player passes by them. This is the default activation that you should be used to.

You may have also noticed that every trigger has a “Touch Triggered” checkbox somewhere in their setup menu. This makes triggers only activate when the player directly touches them.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1KpFA4CHlKMCqYGWVHQcMJYRhKFfpMPOe/preview?usp=drivesdk></iframe></div>

To work with a spawn trigger, a trigger should first be marked as “Spawn Triggered”. It must also be added to a group so the Spawn knows which triggers to activate, and it must obviously be toggled on.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1MnXpPeVbi-GjOLuesS2zl-WLHSki4s3E/preview?usp=drivesdk></iframe></div>

You can also make a trigger activate multiple times with the Multi Activate checkbox. This is what makes spawn triggers so useful.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1FETy9leB_W--grL7r2sT5sQw4goG5M7Y/preview?usp=drivesdk></iframe></div>

# 2: Spawn Trigger

Spawn triggers have a few features that make them unique from other condition triggers. The most important of these is **Delay**, which __delays the triggers from activating for some time__. Instead of activating immediately, the Spawn trigger will wait however long you tell it to before activating the triggers.

In 2.2, the Delay option lets you have 4 decimals after it for timings in the milliseconds, making it more precise. Variance was also added to the delay option; the +- slider adds or subtracts a random value between 0 and your delay variance, so having a delay of 3 with a slider of 2 means you can have 1-5 seconds of delay.

None

Additionally, the **Editor Disable** checkbox __disables spawn triggers when you’re not playtesting__ your level. They’ll still work if you playtest in the editor or in-game.

None

Spawn triggers activate triggers instantly from left to right. This is a feature known as Spawn Order, and it’ll be discussed more in a [later guide](<https://discord.com/channels/414295025883545600/1085288651103150150/1085288651103150150>). Do not confuse this with “Spawn Ordered”.

None

The **Spawn Ordered** checkbox __lets you spawn triggers in order from left to right, with the same timing that they’d have if you passed them in classic mode at 1x speed__. This means triggers won’t activate instantly and the distance between them matters.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1gAV3puv0eTeZxtheen4NFp_6klB9UZdH/preview?usp=drivesdk></iframe></div>

# 3: Spawn Remapping

Spawn remapping is a new 2.2 feature which is incredibly useful; it lets you copy spawn trigger setups from one group to another. 

In 2.1 you would have to copy over the entire trigger setup and regroup everything, and now you can do this all with one spawn trigger.

This may sound complex, so let me provide an example.

## Setup

First you need to define which group will be remapped to another one.

1. Create a trigger setup you want to use for multiple objects, like projectiles for a boss or platforms that move down when you stand on them. In my case this is a block that moves down then up again.
2. Identify the group for the block with the original spawn setup; in my case that’s Group 1. This is the group you input in the “Origin Group ID” box. Always refer to this group when you want to remap another object to copy this spawn setup.
3. Identify the group of the new block you want to remap your setup to; in my case that is Group 3. This is the group you will input in the “New Group ID” box.

Next you need to configure the spawn trigger setup.

4. Place a spawn trigger and set it to spawn the group of the *original trigger setup*. In my case that’s Group 2. 
5. Head to the second page. In the “Origin Group ID” box, input the group you identified in Step 2. In “New Group ID”, input your group from Step 3. For me, these are Groups 1 and 3.
6. Once you're done click the green + button to add the remap. And that’s it!

<div><iframe src=https://drive.google.com/file/d/1xtQMX3hE-agDLrKI_V_keTJjGvq0lgaV/preview?usp=drivesdk></iframe></div>

Spawn remapping may seem a bit complicated to understand, but once you can identify which groups should be remapped to others it becomes incredibly easy to use it properly.

## Remapping Multiple Groups

You can remap up to 20 groups per spawn trigger. To remap another group, simply follow the steps above. Find what group is the original group and what group you want to remap to.

If you want to remap the same group twice you can do that, but the group it remaps to must be different or you won't be able to add it.

## Summary

- The Spawn Trigger lets you activate triggers which are marked as “Spawn Triggered” and added to a group. This lets you create trigger setups that you can reuse as necessary.
- Delay lets you delay the triggers’ activation by a time range, while Spawn Ordered lets you activate triggers based on their placement in the editor.
- Spawn Remapping lets you copy a spawn setup from one group to another.



## Credits
Created by @koma5
