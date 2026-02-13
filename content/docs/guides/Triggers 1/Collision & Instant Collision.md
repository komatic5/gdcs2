---
title: Collision & Instant Collision
weight: 337
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Short** (4-6 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- Collision Triggers activate when two Collision Blocks touch. This makes them simulate hitboxes well.
- You have to use at least one Dynamic Block so collision triggers can detect the blocks.
- Instant Collision Triggers detect whether two Collision Blocks are touching at a certain moment.
- State Blocks detect players entering or exiting a certain area and can activate different groups accordingly.

{{< /callout >}}

** **
# 1: Collision Trigger

If you know how hitboxes work in games, you’ll know that things only occur when one item’s hitbox touches another’s. You’ll only die in a level when your icon’s hitbox touches the hitbox of a spike, for example.

The collision trigger replicates this feature. To make hitboxes, you use “Collision Blocks” which are found next to the trigger in the Triggers tab. You can then use any transformation triggers - Move, Rotate, Follow, Scale, etc - to move the hitboxes until they touch each other. Do note that as of 2.1, rotate triggers tend to break collision blocks as they are Static blocks with 'hitboxes'.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1yrYdJS-f2TXnuE_0MSq-BWcHbeuiksBI/preview?usp=drivesdk></iframe></div>

Collision Blocks have Block IDs, which is how the Collision Trigger knows which blocks to look for. If you enter Block IDs `1` and `2`, you’ll need the Collision Trigger to detect BlockA and BlockB IDs `1` and `2`.

Detecting hitboxes is a very intensive process, so the game doesn’t do it for every block. You’ll need mark at least one collision block as a **Dynamic Block** – __the collision trigger will watch that block and wait for it to touch one with the right Block ID__. Try to minimize how many dynamic blocks you have toggled on at any time because they can be very laggy.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1J4mMFcRU0VKZGP44WCGE6ZF8KyaejTet/preview?usp=drivesdk></iframe></div>

While the trigger normally activates when two blocks start touching, you can use the “Trigger on Exit” checkbox to activate it when the blocks stop touching. Please note that the collision trigger will wait until NO blocks with either ID are touching.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/15tJkyCOkVe4K_pq-l04nZNZepKahjhcS/preview?usp=drivesdk></iframe></div>

:2Point2: In 2.2, the Collision trigger also gains three new checkboxes:

> • P1 makes the BlockA ID use Player 1’s hitbox, so the trigger will activate when Player 1 touches a collision block.
> • P2 makes the BlockA ID use Player 2’s hitbox.
> • PP makes the BlockA and BlockB IDs use Player 1 and 2’s hitboxes, so the trigger will activate when both icons touch each other.

<div><iframe src=https://drive.google.com/file/d/1MVntF_yxNlTJuob6crqh3iXneGrbbufp/preview?usp=drivesdk></iframe></div>

# 2: Instant Collision

The **instant collision trigger** will __test whether or not two collision blocks are touching at a single instance__, hence the name.

To better understand the difference between a normal collision trigger and an instant collision trigger, think about it this way:
A collision trigger detects *when* two block IDs touch or exit each other.
An instant collision trigger detects *if* two block IDs are touching at that moment.

If you’re familiar with programming, it might make sense to view the instant collision trigger as an “if-else” statement to more easily create logic with it:

> If: Block ID A is touching Block ID B
> Then: activate True ID group 
> Else: activate False ID group

**Options:**
- Block ID A & B - The IDs of the collision blocks to test, same as the collision trigger.
- True ID - The ID of the group that will activate if Block A is touching Block B.
- False ID - The ID of the group that will activate if Block A is *not* touching Block B.
- P1 - Replaces Block ID A with P1 and will test whether player 1 is interacting with Block ID B.
- P2 - Replaces Block ID A with P2 and will test whether player 2 is interacting with Block ID B.
- PP - Replaces both Block ID A & B with P1 and P2, will test whether both icons are touching.

None

# 3: State Block

A **state block** __activates a group when the player enters or leaves it__. This can still be done with collision blocks and collision triggers, but it is quicker and easier with a state block.

**Options:**
- State On - The group ID to activate upon the player entering the block.
- State Off - The group ID to activate upon the player leaving the block.

In the example below, a state block is used as a button to rotate platforms. This is done by setting one group as State On, which activates a rotate trigger, and another group as State Off, which activates a stop trigger that stops the rotate trigger.

None

**Further Details:**
- Each state block will act independently of one another even if there is another state block with the same values, unlike collision blocks with the same ID which act as one big collision block.
- If both players enter or leave the state block on the same frame, it registers as one input.
- If both players are in the same state block at the same time, it will register *both* enters, but only *one* exit.



Changed the channel name: Collision & Instant Collision



## Credits
Created by @koma5
