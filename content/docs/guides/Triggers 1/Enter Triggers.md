---
title: Enter Triggers
weight: 325
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Short** (4-6 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- Enter Effect triggers add transitions to objects entering or exiting the screen.
- In 2.2, several new enter effect triggers were added, allowing you to create custom effects.

{{< /callout >}}

** **
# 1: Pre-made Enter Effects

**Target Enter Channel** makes the trigger target object present in a set Enter Channel. 
*Enter channel is a new type of group introduced in 2.2. It works just like the Block ID in collision blocks, the gradient ID or The EffectID in the area triggers.*

To assign an Enter Channel ID to an object, head to its Edit Group tab and click on Extra 2. You should see a small plus sign, which assigns the object to a new ID. 

- **Enter / Exit Only** lets you toggle the effect when the object enters the screen, or exits it. 

- By default Objects fade in and out. *This is how objects normally appear and disappear.*

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1_MYSlgD0GV__tswSDKPVr74JCIV7xE-l/preview?usp=drivesdk></iframe></div>

- :Fade2: Objects fade in by moving down and fade out by moving up.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1XQmCb1CM17z2GXUUL-BQ0MoOlwRqDcvm/preview?usp=drivesdk></iframe></div>

- :Fade3: does the opposite of the previous trigger.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/17RSpYK3Hy4HB7oZee6Cv5VP0gh13uv_J/preview?usp=drivesdk></iframe></div>

- :Fade4: Objects appear from behind the blocks near the screen's edge and then disconnect and move towards the left.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1XVJ00MMtSJXCkEc0PAvxFAztsw4YG-Wx/preview?usp=drivesdk></iframe></div>

- :Fade5: Objects fade in by connecting to the rest from the right and fade out, by disappearing from behind the blocks near the screen's edge.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1ga4fDkatnu-ikUYMZIfMP__uN5FEr1wF/preview?usp=drivesdk></iframe></div>

- :Fade6: Objects fade in by scaling up and fade out by scaling down.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1dShqqCYPSL76z64xZqeEdzc56J2eYvkB/preview?usp=drivesdk></iframe></div>

- :Fade7: does the opposite of the previous trigger.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1g1KFPPEIUdCzFMRiqRmedJGMtN9mS178/preview?usp=drivesdk></iframe></div>

- :EnterTrigger12: Objects enter and exit the screen with random movements, fading in and out. *This was a secret trigger in 2.1, and has now been added officially in 2.2.*

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1wv-RSmUxkW4d6Ygn9Xql4eQTgng4g19v/preview?usp=drivesdk></iframe></div>

- :Fade8: The top half of the objects fading in move downwards, while connecting to the rest from the right. The bottom half moves upwards and dissapears from behind the blocks near the screen'sedge. Objects fading out do the opposite of this.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1NvVZuNCFVHkdYXijofaIpaynmumcvKKn/preview?usp=drivesdk></iframe></div>

- :Fade9: does the opposite of the previous trigger.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1Vx4AHPK9Icbtbmx_L9tdFDmU-XRMR0oO/preview?usp=drivesdk></iframe></div>

- :Fade10: Similar to the previous two triggers, the top half moves downwards and the bottom half moves upward, while objects fading out do the opposite.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1Lncgndpkm_OKe5EXywizx0OB-QDMCQ7C/preview?usp=drivesdk></iframe></div>

- :Fade11: does the opposite of the previous trigger.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1w_yC7hFFVrobuuixVPz_NVsxjwcERdh8/preview?usp=drivesdk></iframe></div>

- :EnterTrigger1: This trigger cancels any ongoing effects. It effectively enables the “Don't Fade” and “Don't Enter” options.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1AM5gz5leRUKGE1MFkZ0_J8V4SvjEP04u/preview?usp=drivesdk></iframe></div>

# 2: Area Enter Effects

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1ZDUWJ7RuqMMW-7CMGgXau29K7AXSpY0Q/preview?usp=drivesdk></iframe></div>

Update 2.2 introduced several new triggers which allow you to create your own enter effects. This section will go over how they work. 
## Enter Effect GUI

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1H31DjTCEh-300JIAf1qXWVRjWb4PTVpc/preview?usp=drivesdk></iframe></div>

All custom enter effect triggers have a common GUI. This should be familiar if you’ve used Area Triggers before.

- **Length**: Determines the length from the screen borders the effect is applied. 

- **Offset**: Offsets the screen borders. Positive values offset the screen to the right, and negative values offset it to the left. *The sliders on the right side let you add variety, so that the parameters are random each time.*

- **Effect ID**: A new type of Group IDs. This one is used for individual effects, to later disable them. 

- **Enter / Exit Only**: Determines if the effect is applied only when objects enter/exit the screen. Leave this blank to apply the effect to both sides. 

- **Easing**: Modifies the way objects start and end their transitions, similar to the easings in a Move trigger. 

Now that we know what every custom enter effect has in common, let's talk about their individual functions and applications.
## Move Enter Effect

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1ie9Zk8wEXK7rTDh6di1BCC9eO76vGtyF/preview?usp=drivesdk></iframe></div>

Moves objects when they enter/exit the screen. 

- **MoveDist**: Specifies the distance the objects will move, with 10 being an equivalent to 1 block.

- **Move Angle**: The angle at which the objects move, with 0° being straight upwards, 90° being right, 180° downwards, and 270° left. 

- **XY Mode**: Allows you to input X and Y values instead of choosing a direction for the objects’ movement. 
## Rotate Enter Effect

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1Uq8hknt9AYMCRq1Z0S3Zg0XZ3iP9Pzrd/preview?usp=drivesdk></iframe></div>

Rotates objects when they enter/exit the screen. 

- **Rotation**: Determines the degree of rotation for the objects. 
## Scale Enter Effect

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1mdxbT7Illk1vQqTS11ArmaAcg4z66-X_/preview?usp=drivesdk></iframe></div>

Changes object size when they enter/exit the screen. 

- **ScaleX / Y**: Lets you scale objects the same way as a Scale trigger. 
## Fade Enter Effect

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/17yzoluFWY-s_HenJ4yG1gSlptb0VHn4M/preview?usp=drivesdk></iframe></div>

Changes object opacity when they enter/exit the screen. 

- **Opacity**: The opacity the objects will have when near the screen's edge. 0.00 means completely invisible, and 1.00 means fully opaque. 
## Tint Enter Effect

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1Z3Oz2pUulUWvgWgoeibVtQnWzf1kS-fp/preview?usp=drivesdk></iframe></div>

Changes object color when they enter/exit the screen. 

- **Color Channel**: Targets a specific color channel. 

- **Tint**: Changes a set color, similar to choosing a color on the color wheel. 
 - Inputting 0.00 doesn't change the color, while 1.00 yields the exact opposite of it. 
 - For example, inputting 1.00 on a white object turns it black. 0.5 would turn it gray in this case. 

- **Main / Sec Only**: Specifies whether to target the base or secondary color of the object. If the object only has a base color, this will do nothing to it. 
 - Replacing the Color Channel and Tint sliders with an HSV button leads to the set HSV menu.
## Stop Enter Effect

<div><iframe src=https://drive.google.com/file/d/1_oHrHylhZpTg0Dr72j4a3xyRSZeO7DDy/preview?usp=drivesdk></iframe></div>

This trigger is used to disable an ongoing custom enter effect, similar to :EnterTrigger1:





## Credits
Created by @EYZ and @etherail
