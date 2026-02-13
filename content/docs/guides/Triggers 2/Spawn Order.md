---
title: Spawn Order
weight: 602
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Short** (3-5 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- Triggers activate from left to right when spawned by a Spawn trigger, in a process called Spawn Order.
- You can activate multiple spawn triggers with one trigger, known as Branching. The branch with the higher Spawn Order will activate in full before the game processes the next branch.
- You can merge branches together by activating the same group on the same frame with multiple branches.

{{< /callout >}}

** **
If you activate two triggers on the same frame, how does Geometry Dash know which to activate first? The answer is Activation Order. There are two systems in-game for this, the first of which is Spawn Order. This guide will discuss what it is and how it works.

# 1: Spawn Order

Spawn triggers will activate triggers from left to right on the X-axis. This seems like a small detail, but it’s important when using them. I recommend you order your triggers from left to right when they’re spawned by the same group to avoid conflicts.

In the example below, both color triggers are activated by the same spawn trigger. In the first attempt the green color trigger activates first and is then overridden by the red one. In the second attempt, the opposite occurs.

None

Spawn order in the editor depends on the order you place down the triggers. Once you save and exit the level, it’ll follow the normal Spawn Order rules.

Also, note that this behavior has changed across game updates:
- In Update 2.1, this ONLY applies when a trigger is activated by a Spawn trigger. All other condition triggers, like On Death and Touch, use Priority Order to activate their triggers.
- In Update 2.2, this applies to ALL condition triggers, and Priority Order is not used by condition triggers anymore.

# 2: Branching

**Branching** is __when one spawn family trigger activates other spawn family triggers__. These triggers make new “branches” that can activate more triggers. Branches will activate according to normal Spawn Order from left to right if they are activated by a spawn trigger. When using a non-spawn trigger, they’ll use Priority Order instead; you’ll learn more about that in the next lesson.

When a branch is activated, GD will only move onto the next branch once everything in that branch has finished activating. If the branch encounters a spawn delay, it’ll move to the next branch and return to the first after the delay finishes. Branches can also have sub-branches of their own, which will function in the same way.

While branching is not too useful using just spawn triggers, it lets you make far more complex programs when used with instant count or toggle triggers.

The image below shows an example of spawn branching. The number above each trigger shows the order it’ll activate in, while the number below is the group it’s assigned to. The first spawn trigger makes two branches and the upper one activates first, as it’s further left than the bottom one. Once both color triggers activate, the lower branch is activated.

None

# 3: Merging

**Merging** is __the opposite of branching, where you merge two branches into one__. This works because one group can’t be activated multiple times on the same frame, with some exceptions. If you spawn the same group on the same frame with different branches, they’ll merge into one.

Note that as of Update 2.2, triggers *can* be updated multiple times per frame, but ONLY if they don't activate other triggers. This means that merged branches need to activate a Condition trigger before activating others, or you may risk duplicating the same actions on accident.

None

This is most useful when making OR gates, which you’ll learn more about in a later guide.


## Return to the Table of Contents [here](https://discord.com/channels/414295025883545600/1230610140940730479/1230610140940730479)



## Credits
Created by @koma5 and @𝕋ypexleta
