---
title: Reverse & Arrow
weight: 328
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Short** (3-5 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- The Reverse Trigger makes go backwards, but it has the least utility if you need more complex sideways gameplay.
- The Reverse option in the Extras menu lets you change direction by using most orbs and pads.
- The arrow trigger allows you to go in any direction, but you need to be mindful with setting up the channels and order.

{{< /callout >}}

** **
<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1ckqDhwTumt2IHfk_9efgvfXlxElffrf7/preview?usp=drivesdk></iframe></div>

:ReverseTrigger: This is probably one of the simplest triggers in the game. Just place it down and the player goes backwards. However, it might be too simple that it also borders on useless. For example, placing two reverse triggers like below won’t work properly if you want the rightmost trigger to activate first:

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1LZSQMhF_gTwSB8JmeVJg3vc2noc-tC9R/preview?usp=drivesdk></iframe></div>

This is because the reverse trigger placed on the left activates first. While you can use the **Touch Triggered** option to make your gameplay, this will mess up the music playtest line unless you change the target channel using an arrow trigger, which will be explained in a later section.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1JMIa1kJAATksX-cCSvUuDM-4gWQ4-9An/preview?usp=drivesdk></iframe></div>

# 2: Reverse Option

Another way to change directions is enabling the **Reverse** option in the Edit Group tab’s extras menu. It makes jump pads & orbs [switch the direction](<https://www.youtube.com/watch?v=LhLE9MqU_SQ&t=24s>) you're going in with the only exceptions being Dash and Toggle orbs.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1408NOQrNn0eCfnkc01mnL4J_IDOuqn69/preview?usp=drivesdk></iframe></div>

*Keep in mind that both the Reverse trigger and option are useless in platformer mode because you can freely move left and right as you please.*

# 3: Arrow Trigger

The arrow trigger :ArrowTrigger: allows you to go in any direction, not just in reverse. By changing its rotation you'll change the player’s direction.

*If there are multiple arrow triggers without setting their target channels, the ones with the smaller X or Y value get activated first. This changes based on the rotation of the arrow trigger.*

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1MkrmEwBHsSegAE9jQD88SqgrLUe8mnKx/preview?usp=drivesdk></iframe></div>

The features include the following:
- Edit Velocity: Lets you edit the velocity when switching rotation.
- VelModX / VelModY: Multiplies the amount of force applied in X and Y axis after changing directions.
- Override Velocity: Sets the velocity instead of multiplying it.
- Change Channel: Changes the Channel to the number entered in the **Target Channel** box below. 
 - To revert back to normal, place another trigger, go to Edit Group and set the channel in the bottom right corner to the one you have entered in the first trigger. Once you do that, click the Edit Object button and set the Target Channel to 0 as a reset.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1Gdc6CFPChfEENMWQhO3j5rCOfrVdSy04/preview?usp=drivesdk></iframe></div>

- Channel Only: Only changes the Channel and keeps the same direction.
- Instant Offset: The camera updates instantly after changing directions.
- Don’t Slide: Stops the sliding effect when you rotate gameplay in platformer mode.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1BHNYLUWBi6c3AqONHH44-wIjxNGMP0LZ/preview?usp=drivesdk></iframe></div>

Additionally, you can replace a gravity portal with this trigger. However, it is less intuitive because it's invisible.

<div><iframe src=https://drive.google.com/file/d/1IWtT9Qci1hRIBLtsikB4OLb-cKs9ZnuS/preview?usp=drivesdk></iframe></div>

# 4: Cool Gameplay Applications

## Offsetting Players in Dual Mode
By placing two purple jump pads next to each other, you can offset one of the icons making the dual the more engaging and challenging. This exact things was done multiple times in [Badland Full Version](<https://www.youtube.com/watch?v=p4iYbmeWn9E&t=62s>) by MusicSounds.

You can also go crazy with this gimmick just like in a [later part of the same level](<https://www.youtube.com/watch?v=p4iYbmeWn9E&t=136s>). 

In Update 2.1, we could also use this trick, however we had to rely on bugs that made this possible. For those interested, this topic is explained in detail [here](<https://discord.com/channels/414295025883545600/1179853643348967475/1179853643348967475>).
## Going UP
By making the player go back and forth while guiding a camera to slowly go up, you can create some interesting gameplay. This was used twice in Toxic Surge by GiaMmix.

{{< youtube LhLE9MqU_SQ >}}



## Return to the [Table of Contents](<https://discord.com/channels/414295025883545600/1197970940882067466/1197970940882067466>) here



## Credits
Created by @EYZ and @Selena
