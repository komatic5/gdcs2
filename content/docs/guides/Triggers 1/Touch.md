---
title: Touch
weight: 336
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Tiny** (2-4 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- The Touch trigger activates when the player clicks; it doubles as a toggle and a spawn trigger
- You can simulate the Touch trigger using Toggle Orbs/Blocks.

{{< /callout >}}

** **
The **Touch trigger** :Touch: works as a Toggle trigger and a Spawn trigger; __it activates when the player clicks or touches the screen__.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1_eTmwMj75UfXvxED8iv7gpnSRn-f5KAs/preview?usp=drivesdk></iframe></div>

## Normal Behavior
Normally, the touch trigger toggles the group ID on and off when the player clicks. Similar to a light switch, If that group ID was previously toggled on, it’s toggled off, and vice versa. Additionally, any trigger set to spawn triggered will activate when toggled on.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1iK3rrwwavCh2tQq1y8HsFkoKnvmt44h6/preview?usp=drivesdk></iframe></div>

Unlike event triggers, touch triggers can still detect inputs when using the :GPOptionsTrigger: options trigger’s “Disable P1/P2 Controls”.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/116-Rp8FdGVnxHN0fC7CL2Oab2s7p560w/preview?usp=drivesdk></iframe></div>

The settings **Toggle on** and **Toggle off** __set the touch trigger to only toggle the group ID on or off rather than alternating__.

None

## Hold Mode
Rather than clicking, **hold mode** makes it so that __you activate the touch trigger by holding and releasing rather than clicking__:
- Normally, hold mode toggles off objects when holding, and toggles them on when releasing.
- With **Toggle on** enabled, hold mode toggle on objects when holding, and toggles them off when releasing.
- With **Toggle off** enabled, hold mode functions normally.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1WNCZlLxRMsuuqvyPW2PIXtORuO5x0F6d/preview?usp=drivesdk></iframe></div>

## P1 Only / P2 Only
The settings **P1 only** and **P2 only** can __limit the touch trigger to only detect Player 1’s controls or Player 2’s controls__. They are unrelated to [dual mode](<https://discord.com/channels/414295025883545600/1083169667906027551/1086495080300421180>) or 2-player mode:
- With **P1 only** enabled, the touch trigger will only activate when the player presses the W A D keys, space bar, or mouse left click for PC, or taps on the left side of the screen for mobile.
- With **P2 only** enabled, the touch trigger will only activate when the player presses the arrow keys for PC or taps on the right side of the screen for mobile.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/17d0VKv16YVwjsHrzPjNEHZExcS-Llv35/preview?usp=drivesdk></iframe></div>

## Dual Mode
Dual mode works similarly to P2 only from earlier, with the addition that it blocks P2’s controls from affecting either player, as well as stops P2’s movement (jumping in classic mode, jumping and moving in platformer). It is unrelated to 2-player mode.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1fjghVKPrEFn8qPp85bKfK9JCrwLM4cIl/preview?usp=drivesdk></iframe></div>

# 2: Toggle Orb and Toggle Block

None

**Toggle orbs** and **toggle blocks** have a __similar purpose to the touch trigger__. They work identically to each other except for the following differences:
- The toggle orb acts like a typical orb, :EditObject: is used to set its colors, while :EditSpecial:  is used to set it up.
- The toggle block is hidden like any other trigger; :EditSpecial:  is used to set it up.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1q9zP6Wm9iuSqC57Zl-ZuQ4dHAc4Bh2C_/preview?usp=drivesdk></iframe></div>

## Normal Behavior 
Normally, the toggle orb/block can only toggle off the group ID; checking Activate group will toggle on the group ID instead and spawn any triggers in that group ID.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1RqKCjZ6HVROd2atQsL5kI36RX4v-Hhrf/preview?usp=drivesdk></iframe></div>

## Spawn Only
The toggle orb/block now functions as a spawn trigger; it does not toggle on or off objects.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1P-kRlbc_cXBumvR47zgeUJAQuxgYSVKC/preview?usp=drivesdk></iframe></div>

## Claim Touch
Enabling this option cancels the jump button’s action; the player cannot jump while inside the toggle orb/block.

<div><iframe src=https://drive.google.com/file/d/1ByR4FkrEmHDcG5QqW0ZpEObIsktbOO1V/preview?usp=drivesdk></iframe></div>





## Credits
Created by @Selena and @eggyolk
