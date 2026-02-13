---
title: Gravity, Teleport, & Timewarp
weight: 347
draft: true
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Tiny** (2-4 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- The Gravity Trigger can control the amount of gravity applied to the player or players whether the player is in a dual.
- The Teleport Trigger teleports the player to a specified Group ID. There are also many options to customize the behavior of the trigger.
- The Timewarp trigger sets the speed of the game based on a single value. This is incomplete as of 2.206.

{{< /callout >}}

** **
The Gravity Trigger changes the amount of gravity inflicted onto the player. Lower values mean a lower gravity and higher ones have higher gravity. This value can be set to a maximum of 1 billion.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/13bCnkBEQzecISrrbwdkv4vfjpC5yC-mJ/preview?usp=drivesdk></iframe></div>

This trigger has 3 options: P1, P2, and PT. P1 targets Player 1, P2 targets Player 2 if the current gamemode is a dual, and PT targets the player that comes in contact if Touch Triggered is enabled. If all options are disabled, both players will be affected.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1hFmfaypHVuwaU3nl5xOi6DS5CY_0Ykzc/preview?usp=drivesdk></iframe></div>

# 2: Teleport Trigger

The Teleport Trigger teleports the player to the position of an object with a target Group ID. If multiple objects have the Group ID, a random one will be chosen to be teleported to. The blue unlinked teleport portal in the orb tab has the same options as this trigger.

**Teleport Triggers only work on Player 1, as of the time of writing.** If you wish to teleport the second player (e.g. for a dual), you need to use the normal teleport portal.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1FQTUD7GJoO69769ZhyGdxW5XBKQv0vIY/preview?usp=drivesdk></iframe></div>

- **Gravity:** Allows you to determine if the player's gravity is normal, upside-down, or switched between the two on teleport.

- **Rotate Force:** Sets the force applied to the player when teleported. This force is done at the angle the target object’s rotation is at. Rotating the trigger itself can have an effect on this force as well.

- **Static Force: **Sets the player's exit force to a set value. Enabling “Additive” will add the specified force to the player’s current force instead.

- **Redirect Force: **Multiplies the player’s force by the mod value. You can set the minimum and maximum force output using the respective sliders; keeping it at 0 will have it ignored.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1lnTk2SkZ_j_8GqJ3qyQ5aa7WqU5U6Bny/preview?usp=drivesdk></iframe></div>

- **Smooth Ease:** Eases the camera to the new teleport position. This operates much like the Smooth Ease option on teleport portals in 2.113.

- **Save Offset: **Offsets the teleport position to the target object based on where the player hits the teleport trigger instead of teleporting them to the center of the target object.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/15WKSqUOULFOrCiDnN857VdGmTtpFd0Oi/preview?usp=drivesdk></iframe></div>

- **Ignore X/Ignore Y:** Teleports you to only the X or Y position of the target object respectively. 

- **Instant Camera: **Snaps the camera to the teleported position instantly.

- **Snap Ground: **Useless as of 2.206.

- **Redirect Dash:** Redirects a dash orb into the angle of the target object’s rotation.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1QYH7dNgtyUaKV6N2vhF7Oi_EuBovuYuL/preview?usp=drivesdk></iframe></div>

# 3: Timewarp Trigger

This trigger speeds up or slows down game speed to a specified value in the 0.10 to 2.00 range. This can affect many things in a level, such as triggers (namely time-related triggers), game physics, etc. This trigger is incomplete as of 2.206, suggested by the triggers UI help button.

**Easings are not possible by default with the trigger; **if you want anything of the sort, you need to place multiple triggers down with different values inside them.

<div><iframe src=https://drive.google.com/file/d/196ve6eD_LyfZv2vHK5u-49Gm-FgNCyAw/preview?usp=drivesdk></iframe></div>





## Credits
Created by @NotAModerator and @TDP9
