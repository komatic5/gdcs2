---
title: GP Options & Player Control
weight: 332
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Tiny** (2-4 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- The Options Trigger is essentially a toggle trigger for player related actions. To toggle them back on or off use another one with opposite settings.
- The Player Control trigger stops you from performing a certain action until you perform it again.

{{< /callout >}}

** **
The Options trigger lets you control the player's actions and controls, but the changes are permanent until you use another Options trigger to disable those options. Think of this as a complex toggle trigger.

- **Streak Additive:** Toggles blending of player trail and particles.
- **Hide Ground:** Hides the ground.
- **Hide MG:** Hides the Middle Ground.
- **Hide P1 or P2:** Hides the corresponding player *sort of like the hide player trigger* :HidePlayer:.
- **Disable P1 or P2 Controls:** Toggles a corresponding player's controls. *Useful during cutscenes or dialogues*.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1heqpeciu1Rf7bO_RA1raePDNNOfzBN8x/preview?usp=drivesdk></iframe></div>

- **Unlink dual gravity:** Allows dual players to switch gravity independently. Normally they both have different gravity, for the most part that is. This is explained [here](https://discord.com/channels/414295025883545600/1086726744725278840/1086726744725278840).
- **Hide attempts:** Hides attempts in a level.
- **Audio on death:** Continues to Play music and SFX after the player dies.
- **No death SFX:** Stops the Death Effect sound from playing, when player dies.
- **Edit respawn time:** Allows you to edit time that takes a player to respawn via the Respawn Time slider at the bottom of this page.
- **Boost Slide:** Increases sliding after a force is applied.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1u6ZjzFytpmd-wtInzlOcYLpBhSPh2sxg/preview?usp=drivesdk></iframe></div>

To have a better understanding of what this actually means, take a look at these 2 levels as well as the video below.
Chromaside by qalli
SpeedTek by G4lvatron

{{< youtube 096FwIbfIOE >}}

{{< youtube tEPKl-QUmNU >}}

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1k8UunbEVgUUalT8F4SGeUcCmarlgwTJM/preview?usp=drivesdk></iframe></div>

# 2: :PlayerControl: Player Control Trigger

This is another useful trigger that controls the player behavior. With it you can control whenever a player should stop performing a certain action until they hit a certain key again.

Do not confuse this with :GPOptionsTrigger:, as they are separate triggers.

- **P1 or P2:** Determines whenever a certain setting should apply to player 1, 2 or both.
- **Stop Jump:** Prevents the player from jumping again unless they hit the jump button again. *This option works similarly to the J block*
- **Stop Move:** Prevents the player from moving unless they hit the corresponding key again.
- **Stop Rot:** Stops player's rotation.
- **Stop Slide:** Can be used to stop the player from sliding after a force has been applied.

<div><iframe src=https://drive.google.com/file/d/1CgKcsngUdn6lONfz4Kv8VPNA78qgjKdF/preview?usp=drivesdk></iframe></div>

<div><iframe src=https://drive.google.com/file/d/1fkFKPvFYMwbQ_DHL91YJSUiYpj5Ubesc/preview?usp=drivesdk></iframe></div>





## Credits
Created by @EYZ and @koma5
