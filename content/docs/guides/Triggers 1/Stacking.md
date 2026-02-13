---
title: Stacking
weight: 347
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Tiny** (2-4 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- Trigger stacking is how different triggers with overlapping durations combine their effects together.
- Different types of triggers will combine their effects with each other differently.

{{< /callout >}}

** **
**1: No Stacking**

The following triggers cannot be stacked.

> • Condition Triggers (Spawn, On Death, etc)
> • Stop, Pause, Resume
> • Fade Triggers
> • Animate Trigger (2.1)

Basically, any trigger that has an instantaneous effect cannot be stacked.

**2: Overrides**

Certain types of triggers can override the effects of other active triggers.

> • **Color Triggers**

 If a color trigger is activated while another is also active, the trigger that is activated last will override the previous one.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1wgjh5YM8w1dMJ9LLsXDJGYZGjqk-fuo7/preview?usp=drivesdk></iframe></div>

> • **Pulse Triggers**

Similar to color triggers, if a pulse trigger is activated while another is also active, the trigger that is activated last will override the previous one. If the overriding trigger’s duration finishes before the overridden trigger, the overriding trigger will take effect again afterwards. Note that this will occur regardless of if the pulse triggers are exclusive or not.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/103t9aVHE4E7DulP_YD_AYvSERXsMuXo4/preview?usp=drivesdk></iframe></div>

> • **Toggle Triggers**

These can “stack” across groups. If an object is part of multiple groups, it will be toggled off if any one of those groups gets toggled off. This is also used for And gates, which are covered in another lesson.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/12OCyeovd6NKT9DkaDQL-5_BXRrt8_7JQ/preview?usp=drivesdk></iframe></div>

**3: Combined Effects**

Some trigger effects can get combined depending on the types of triggers.

> • **Move Triggers / Follow Player Y Triggers**

When multiple of these triggers are active simultaneously, their effects get added together. Stacking two move triggers with opposite easings (ease out and ease in, for example) can make things like smooth curves or smooth movements.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1_MdhgHCM8FgzSZKuDvn0Ct8iJGDwPDKJ/preview?usp=drivesdk></iframe></div>

> • **Rotate Triggers**

When multiple of these triggers are active simultaneously, their effects combine additively. However, if the triggers have the same target and center groups, the second will override the first. You must give the rotating objects unique target and center groups for the rotation to work properly.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1SaTDl9STVioO1tEMkSK0SLXnjCzZ3eVo/preview?usp=drivesdk></iframe></div>

Additionally, stacking two rotate triggers with opposite directions (e.g. 60 degrees for one, -60 degrees for the other) makes an object move in a straight line. This can be used to make objects move and rotate at the same time, as shown here: https://youtu.be/glsG87Ipg0Q

> • **Follow Triggers**

Stacking follow triggers is complex and heavily dependent on the way you do it.

> • Many groups CAN follow one group. One group CAN follow many groups.
> • One object can be added to multiple follow groups, and their move effects will be additively combined.
> • If two follow triggers have the same target & center groups, the later trigger activation will override the first.
> • If one follow trigger’s center group is another’s target group, and vice versa, then the results will vary depending on activation order.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1VLGVrJqCobMwgscvSnSvyVliPTPHZWz3/preview?usp=drivesdk></iframe></div>

> • **Alpha Triggers**

This depends on the opacity and layering of the two objects. If the objects have a different colors, you'll get different results depending on how they're layered.

The exact formula is as follows: When the top object’s opacity is `o₁`, and the bottom’s is `o₂`, the mixed opacity will be `o₁`+`o₂`-(`o₁`*`o₂`). Some common values of that are as follows:

> • Stacking two colors with 0.5 opacity gives you 0.75 opacity.
> • Stacking two colors with 0.25 opacity gives you 0.44 opacity.
> • Stacking three colors with 0.5 opacity gives you 0.88 opacity.

<div><iframe src=https://drive.google.com/file/d/1ArfUCp9eq9G-Ty41ctoJ9spZFGjsILoQ/preview?usp=drivesdk></iframe></div>



**Research** and **Examples**
﻿
  @koma5
﻿
**Proofreading**
﻿
  @KDE

