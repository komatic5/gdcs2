---
title: Fixing Bugs
weight: 347
draft: true
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Short** (6-8 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- Bugs are errors that don’t match what you intended.
- You can find the cause of a bug by checking the groups and the triggers.
- How you fix a bug depends on the type of bug and its complexity.

{{< /callout >}}

** **
# 1: What is a Bug?

A **bug** is when __something happens in-game you didn’t intend for__. The first step to fixing any bug in your level is to identify _what_ the problem is. While working with triggers, you should playtest often in order to spot a bug before the trigger work gets complex, and harder to bugfix. Before starting, you should have a _clear vision of the process and the result_. This can be made simpler by adding text objects as labels to organize your work. When playtesting, keep your eye out for anything that doesn't match your said vision. Once you have identified any bug, move on to the next step.

# 2: Why are These Bugs Occurring?

Now that we know a bug exists, our next step is to examine _why_ these bugs happen. This is the most complex step, as there’s no clear cause of why they occur. Many creators get stuck on this step. Fortunately, there are different ways to check the reasoning behind a bug:

1. Analyze what happens: See what goes wrong and what could potentially be related. Use logic to pinpoint what might have happened. This helps narrow down the process a lot, however it’s still okay if you haven’t figured out why the bug or bugs happen.
2. Check the groups: You should always check the groups of the object that you’re trying to fix. You always need to make sure that you don’t have any miscellaneous groups overlapping, to prevent unintended movements, rotations, pulses, etc.
3. Check the triggers: If all of the groups on the object are correct, you should check if the triggers are incorrectly set. To do this, go through every trigger that interacts with the set groups, and make sure the values are correct. Mistakes can happen, so don’t stress if you notice many inconsistencies.
4. Check special IDs: Triggers could have the wrong group ID, block ID, or item ID, so if the previous two strategies don’t work, you can look for triggers that have a miscellaneous ID. This process might be tedious, but it’s easy to spot a false ID in repeating patterns, such as spawn loops or pulse columns.
5. Use logic: If the problem is related to move triggers but isn’t because of a wrong move trigger, then the problem must be from the activation of the move trigger, or another trigger changing the output of the move trigger.

In complex trigger setups, finding bugs tends to be more difficult. But there are still ways you can narrow down the reason a bug occurs. When spawning groups, you can add a temporary color/pulse trigger to the group to find out if the correct group is being spawned. Doing this gives you a signal when a group is being spawned. In the case that color/pulse triggers aren't being spawned, it means the bug must be somewhere earlier in the trigger setup, rather than after.

# 3: Debugging

Now you know why a bug occurs, all you have left is to fix the bug. Debugging completely differs depending on the bug you’re trying to fix. However, make sure that your fix _works and doesn’t introduce new problems_. If you know the cause of a bug, but you don’t know how to fix it, you can try again with a different trigger setup. To make the process easier, you can make a post in #bug-help to get bug fixing help.

# 4: Common Mistakes

To make it easier to find mistakes, here’s a list of common mistakes that almost all creators tend to make:

- A move trigger could have the wrong X/Y value, leading your object to be misdirected.
- When duplicating move triggers, you could unknowingly paste a move trigger with Lock to Player X/Y, and forget to deactivate it.
- There’s a chance that you forgot to change an alpha trigger’s opacity value to a different number, making it so your object's opacity won’t change.
- When toggling on/off objects, make sure to correctly activate Toggle On/Toggle Off. These mistakes are easier to identify because toggle triggers turn red or green depending on their state.
- Rotate triggers almost always require a center group ID. When building, make sure that your objects have 1 center. If your objects rotate awkwardly, the problem is most likely that you have the center group set wrong or you have more than one center binded to the same group.
- When playtesting in the editor, rotate triggers tend to break whatever is rotating over time. Keep this in mind as it could ruin rotations. 
- Pulse triggers that overlap tend to cancel eachother, so check that all pulse triggers are spaced apart correctly.
Mixing up Count and Instant Count triggers is possible, but they have some distinct differences that can make a difference in your trigger-work. Instant Count triggers have 3 options: Equal, Larger, and Smaller, while Count triggers do not. Check if the correct one is selected.
- Touch, Collision, On Death, Count, and Instant Count all have the option to select Activate Group. Make sure that you have this option correctly selected/unselected.

- Collision Triggers have an option to Trigger On Exit. On setups that require this, it's possible that you missed selecting it.
- When you make a setup with collision triggers, every moving collision block needs to have Dynamic Block enabled.
- Stop triggers only work when they are stopping any triggers that are in the middle of working. You are not able to stop triggers later in the level unless the stop trigger is spawned after the trigger you want to stop.
- Activate Multi-Triggered when necessary. This is a common mistake people make when making spawn loops.

# 5: Example: Double Click

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1E4fGRtGM3_M00ZH9k0mapIHfMkXDE5JT/preview?usp=drivesdk></iframe></div>

In the image above, we have a double click detector. When making a trigger setup, we need a vision for it. Our vision in this double click detector is that when you click, collision block 1 moves onto collision block 2 in a 0.25 second move time, which when triggered moves Block 1 to the left by 2 blocks and stops the trigger that moves Block 1 to the left by 1 block. In our vision, it should look like Block 1 is shifting back and forth, but never leaving to the left or right of either collision block.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1K6pLGgUxUw25_xtHHnXTExKeNCPOGMjp/preview?usp=drivesdk></iframe></div>

In this video, we see Block 1 moving too far to the left, which _goes against our vision_. We have now _identified_ the bug, which goes to the next step, which is to _examine_ the bug. 

To start, we analyze what happened; Block 1 moved too far to the left. However, looking closer shows that as soon as Block 1 moved onto Block 2, the collision trigger moved Block 1 to its starting position, and then soon after, Block 1 shifted left by 2 grid spaces with a small delay in between. With logical thinking, we can infer that the problem came from the stop trigger and the move trigger that shifts Block 1 to the left by 1 grid space.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1Az0djF0Ol8P2WgkuwuZkG78lAtxPdT-u/preview?usp=drivesdk></iframe></div>

In this video, we’re looking through the groups and triggers to find anything odd. First, we start off with the collision block to see if there are any miscellaneous IDs. Then, we look at all the move triggers with wrong values, as well as the stop trigger. When looking through the spawn trigger, it seems it wasn’t given group 6, the group that the stop trigger stops. This is a common mistake when working with stop triggers.

<div><iframe src=https://drive.google.com/file/d/1JVGQU35qnNENoxMrdprd2Rt5vgiz_qBr/preview?usp=drivesdk></iframe></div>

Now that we know the bug’s origin, we just have to fix it. This fix is as simple as adding a group to a spawn trigger, but most other setups would require an extra module in order to patch a bug. Now that we’ve implemented a fix, we need to playtest and make sure no further problems arise. On a double click detector, spamming is easy enough to make sure.





## Credits
Created by @NotAModerator and @ontos
