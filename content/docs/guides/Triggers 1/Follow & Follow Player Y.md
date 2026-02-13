---
title: Follow & Follow Player Y
weight: 309
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Tiny** (1-3 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- The Follow Trigger copies one object’s movements to a group. You can use X/Y mod to multiply the X and Y movements accordingly.
- The Follow Player Y trigger sets objects’ Y positions to the player’s. You can change the speed of the objects, or how much delay they have when copying the player’s movements.

{{< /callout >}}

** **
# 1: Follow Trigger

The Follow trigger copies one object’s movements to another set of objects. The Center group must be a One-Object group or a Parent Group, as usual.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1cSxeIEAtD_40-2HC7utJkrQ0DokKYoCs/preview?usp=drivesdk></iframe></div>

X/Y mod multiplies the size of the movements.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1JFdK2xcbjlxHJMvm_URcGq6CJ4Hi5N8i/preview?usp=drivesdk></iframe></div>

Stacking follow triggers is complex and heavily dependent on the way you do it.

- Many groups CAN follow one group. One group CAN follow many groups.
- One object can be added to multiple follow groups, and their move effects will be additively combined.
- If two follow triggers have the same target & center groups, the second trigger activation will override the first.
- If one follow trigger’s center group is another’s target group, and vice versa, then the results will vary depending on activation order.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1qugIBnvnK4r7bsoW5BfNXgHQFXwImp5h/preview?usp=drivesdk></iframe></div>

# 2: Follow Player Y Trigger

The Follow Player Y trigger sets object’s positions to the player’s Y position, as opposed to just copying the player’s movements. This lets it work even when the player teleports.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1YJc3OYi0dUETutU7IPh86FcAy44t_kOC/preview?usp=drivesdk></iframe></div>

Speed determines how fast the objects move to the player’s Y position, in terms of the player’s speed. Max Speed is the maximum speed of the trigger’s movement, in blocks per second.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1VO-jBoTK1eEHB2zieQ2hnpFLev6-e4FQ/preview?usp=drivesdk></iframe></div>

Delay adjusts how delayed the Follow Player Y’s movements are from the player’s.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1BOGUv58V5dqmnBveeH8neC-shOXdA2Hk/preview?usp=drivesdk></iframe></div>

Offset adjusts how far above/below the player the objects are.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1dmIzsnA-3Cjf-X_T_0C7S89SYu3r4A7P/preview?usp=drivesdk></iframe></div>

You’ll notice that when multiple objects are involved in the trigger, they’ll all collapse on a single point. To counteract this, either use a Follow trigger and a One-Object group, or set a Parent Group object for the trigger.

<div><iframe src=https://drive.google.com/file/d/1_Vu03TfWwYTV6_d9rsW2DUfrU3zx9Zgx/preview?usp=drivesdk></iframe></div>

Follow Player Y triggers stack normally, just like Move triggers do. You don't need to do anything additional to get them to stack.





## Credits
Created by @koma5
