---
title: UI & Link Visible
weight: 347
draft: true
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Tiny** (2-4 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- The UI Trigger lets you create a UI that stays on screen at all times.
- The Link Visible Trigger lets you force objects in a group to always render.

{{< /callout >}}

** **
# 1: UI Trigger

The UI Trigger allows you to keep objects on screen at all times. This also means that any objects in the UI will not have a hitbox, so they cannot be used as center objects for triggers like :Rotate: and :GradientTrigger:. The camera guide is a good object to center your UI around as it tells you what is visible on the screen when playing.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1IpF-Y98S5wLBUKExt4zLr8XP4IJ6Uo9D/preview?usp=drivesdk></iframe></div>

The green box represents the size of your UI; anything outside of this box will not be visible.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1bUaFigGKahBvrm1DjwVxAIXzzQLM9R5e/preview?usp=drivesdk></iframe></div>

## Relative
The UI used in the video does not consider devices with different aspect ratios. The inner box represents the typical 4:3 aspect ratio while the outer box represents the aspect ratio of your device. To accommodate for this issue there is an option to select “relative” in the UI trigger.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1QFWf0T_crbqN6LVzf9XC_3La49D7iOjb/preview?usp=drivesdk></iframe></div>

In the video above, you can see that using the relative option on multiple objects in a group spaces it out. To fix it you need to add a single-object parent group ID in the center of the objects, the parent ID must match the ID of the objects. You can create a parent ID by selecting the P icon after entering the group ID.

## Extra Options
If you ever want the objects in your UI to be oriented in a certain way automatically, you can select that option under the XRef and YRef as shown in the video.

For XRef, if “Center” is selected it will orientate the object in the center of the UI relative to the x-axis, the same rule applies for selecting “Left” and “Right”. 

YRef works similarly to XRef but only orientates objects on the y-axis and has slightly different options, that being “Bottom” and “Top”. 

For Auto, the object is orientated based on the camera’s edge of the “UI Target Object.”

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1THK5h2Ez3fodjbmGsl2ZKP0zMihXbeoo/preview?usp=drivesdk></iframe></div>

Here is a practical example of how a UI could look.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1ql1-7A_7Yf1RdQ-h8_z8riLN0sWGw9_e/preview?usp=drivesdk></iframe></div>

# 2: Link Visible

The Link Visible Trigger is useful if you need to render an object regardless of its location.

For this to work you must have an object that can be rendered at all times acting as a reference such as a basic block, and the object you are trying to render. In my example, I used a scaled-up basic block. As long as one object in the group is rendered, all of them will be.

> **Note:** All of the objects must be under the same group ID.

<div><iframe src=https://drive.google.com/file/d/1h1uzq50hxcVEZnXXbn767UvAd-H7s-Ls/preview?usp=drivesdk></iframe></div>

The scaled-up object will remain rendered until the reference block goes off the screen. You can add more reference blocks to continue rendering the scaled object. __Once the trigger is activated it cannot be stopped. __





## Credits
Created by @Dimstack and @koma5
