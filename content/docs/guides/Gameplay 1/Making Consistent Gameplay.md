---
title: Making Consistent Gameplay
weight: 415
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Medium** (10-12 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- Consistency is an integral part of creating a good and fair player experience in a level
- Playtesting and study can help you identify common inconsistencies in your level
- Using gameplay objects, game physics, and the options trigger are great ways to fix bugs

{{< /callout >}}

** **
# 1: What is consistent gameplay?

**Consistent gameplay** is __having a level play similarly every time you play through it__. Gameplay where you randomly die because you clicked a little off or randomly pass a part when you were supposed to die is considered inconsistent. Having very similar clicks and  very different results in the gameplay is where inconsistency can hurt the quality of a level. When designing gameplay, inconsistencies in the player’s inputs should be taken into account; they should not cause significant changes in the player’s experience.
## Why is it important to have consistent gameplay?
When a player dies in a level, they should understand why they died and how they can avoid dying next time. When the gameplay in a level is inconsistent, players don’t feel like the deaths are their fault, meaning they don’t feel like they can improve and learn from each death. Having consistent gameplay is important to avoid making the player feel punished for doing something that isn't their fault. Levels that have inconsistent gameplay are often heavily criticized, with players saying that the level is bad, the level did not get playtested, and they would rather not beat the level. This negatively affects the perception of the level in one of the worst ways possible, making consistent gameplay one of the most important features in a high-quality level.

# 2: Identifying Gameplay Errors

In order to make consistent gameplay, we must identify gameplay errors. **Gameplay errors** are __moments when a player’s path is altered greatly from a slight mistake__. Often this causes the player to die to something that isn’t necessarily their fault. There are many different types of gameplay errors, all of which can ruin a level.

## Unjustified Deaths
An **unjustified death**, often known as a bug, is __an area in a level where slight changes in click delay cause a death__. Jumping a little earlier than what is intended, clicking on an orb slightly early or late, or not landing on a gravity portal correctly can lead you to a different path which will kill you before being able to make the next input.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/19RW0mp9XgmuJFrm6kPLjteqSerPcuBY7/preview?usp=drivesdk></iframe></div>

## Unfair Transitions
Momentum and icon position are very important when transitioning into another gamemode. It is important to consider the player’s movement speed since this will change where the player is going to land. For example, clicking with a cube right before entering a ball portal can have different results if there is a slight timing difference. Entering with a wave into a ship portal will have different results when holding and when releasing before entering the portal. Touching a portal a bit late or a bit early can also have a huge difference in result even if the difference in position is small.
## Slopes
Slopes can be very inconsistent when landing and jumping on them. Jumping at different points on a slope will give different results in height. The higher the speed, the bigger the difference will be. This image shows the difference in launch height from a slope in different landing positions.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/11EaLUxK8B85G1rGLB2OV8_HJSHoeRNA1/preview?usp=drivesdk></iframe></div>

## Consecutive Orb Inputs
Using several consecutive orb inputs, also known as orb chains, is one of the most inconsistent types of gameplay. Clicking an orb too early could lead to not reaching the next orb or barely reaching it, causing you to land in an unintended place. In these situations, a slight timing difference can give you very different results.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1cfCqUfoDM__AUeVd4gcNR2fbXIJM_Bo9/preview?usp=drivesdk></iframe></div>

# 3: Bug Fixing

There are several ways to fix gameplay errors. Implementing gameplay objects to fix icon position, moving around structures, portals, and orbs, and removing inconsistent pieces of gameplay are all great ways to fix errors.

## Adding Other Gameplay Objects.

There are many different types of gameplay objects such as slopes, pads, portals, and certain triggers that can be used to correct the player's path. 
- **Slopes** can be used to fix the player's path by leaving a gridblock space to reset the player’s Y position during transitions.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1hErNpe-EnsSHcOos6QjWkLgwLCRkrmW-/preview?usp=drivesdk></iframe></div>

- **Pads** can be used to keep transitions from one gamemode to another consistent. Wave is the only exception since pads don't affect the wave’s trajectory.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1TBzdiqu63vAHpeWWoaf_4NhNklnOmRPl/preview?usp=drivesdk></iframe></div>

- **Teleport Portals** and the **Teleport Trigger** are used to instantly move the player to a specific position. The force sliders in these objects can be used to keep gameplay consistent no matter how the player enters the objects.
- **Special Blocks** are some of the most useful objects in the game. H and J blocks are especially useful for making consistent gameplay in certain scenarios. Sometimes orbs will launch you higher than you want. A H block on top of another block can act as a “roof” to realign the player. When using black or blue orbs close to a structure you're supposed to land on, the player may hold too long and jump accidentally, causing the player to die. Placing a J block will avoid this by making you not jump automatically every time, having the same outcome in every attempt.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1hU-XdErJTRpKRwmuEg7rpoJF374PzUVs/preview?usp=drivesdk></iframe></div>

## Drawbacks
Using this method could make the rest of the gameplay different than originally planned since you are resetting the player's momentum. Using other gameplay objects could increase the risk of encountering new bugs right after the fixed part. You need to consider which objects to use based on the gameplay that follows afterwards. The gameplay might feel unnatural due to sudden changes in the gameplay. These changes may be visually unpleasant and can make the gameplay feel forced. The player might not expect the sudden changes which might cause confusion, making the gameplay feel unfair. With any method you use to fix the player's trajectory you might need to move around a few structures to keep the gameplay consistent throughout.

## Using game physics
By carefully crafting your gameplay, you can use the game physics to force the player to go through unavoidable pathways. This method gives the best outcomes, but it is the hardest to pull off. You must be knowledgeable of how the game modes behave when interacting with other gameplay objects. 

Platforms and structures are essential. When jumping or falling off platforms, there is almost no possibility for inconsistencies. Keeping this in mind, it is important to add structures and not depend on orbs in your gameplay too much. Structures act as a reset to your momentum and behave exactly the same every time.

Orbs and Pads will launch the player at the same speed and height in every attempt, as long as the player enters or clicks the object at roughly the same spot every time. Using several orbs consecutively is not ideal since the player's position will be altered depending on when you click the orb. As explained in the previous point, using orbs can be consistent if you use them when jumping or falling off a platform.

** **

Flying Game Modes (Ship, UFO, Wave, Swing) are more likely to cause issues with consistency, especially during transitions. Using orbs with ship and swing, wave spam sections, gravity changes and slopes with UFO, and clicking right before entering any portal can cause potential inconsistencies, causing players to die unfairly due to the variation in potential outcomes. To avoid this, you need to consider how the game modes behave, keeping things like acceleration and position in mind. You can also place portals before orbs as it will make the gameplay more understandable and consistent. The images below show how inconsistent orb clicks into portals can be. These inconsistencies can be fixed by simply moving the portal slightly in front of the orb.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1cuQNnSS2i9_Nmz4DxOWfC0ySZ-5_rsLz/preview?usp=drivesdk></iframe></div>

There are some cases where you can use orbs in order to fix issues and make the gameplay feel more natural. For example, if you have a yellow orb click onto a block and it feels inconsistent, you could add a black orb so it always hits the block you are supposed to land on.

<div><iframe src=https://drive.google.com/file/d/1TP5D79mHyfi-_BAuigKiZKJwAcOItk_q/preview?usp=drivesdk></iframe></div>

## Drawbacks
As stated before, using this method might require you to rework a whole section to make it consistent. In order to fix inconsistent sections you need to consider what the player is doing before getting to that specific part. You might need to rework gameplay after the part as well to account for any bugs your changes may have caused. Playtesting a level requires checking every click and part in a level for bugs or inconsistencies. This can be a difficult process for inexperienced creators, but it is absolutely necessary. 

## Using Options Trigger.
The options trigger can be very beneficial to fix different types of gameplay. Whether you are fixing transitions, dual gameplay, or fast/sudden player movements, you can modify how the player behaves by using the options trigger.

**During transitions**, you can disable the controls for a short period of time in case the player accidentally clicks or holds. Disabling the player controls during a transition will make the player have the same outcome in every attempt, as well as keep the player from dying randomly to invisible objects. You may see this as a viable option especially in fast paced gameplay.

**Dual Gameplay** can sometimes be difficult to make consistent. Holding for a bit longer could make you jump with the other player if the structures are very close together. With the options trigger, you can disable either player 1 or player 2 controls depending on which player isn't meant to have an input. Unlinking duals can also make gameplay more consistent. When you have the gravity linked, when you change gravity with one player, the other will change as well. This can cause inconsistencies depending on how the player was previously moving. Unlinking the gravity can prevent this, but you will have to make the gravity change manually if needed.

** **

**Fast and sudden changes** can be confusing for the player, and they won't have enough time to react. You can enable and disable player controls accordingly so the player can hold and continue the gameplay. The gamemodes you will find this more useful in are wave, ship, and cube. 

Landing after a blue or black orb can make you jump immediately after, and though **J** blocks are used to fix this, they aren’t perfect. You can guarantee the player doesn’t jump afterwards by disabling their controls for a short amount of time.

## Drawbacks
Many players are more used to seeing the icon's movement rather than focusing on where or when exactly to click, meaning that if you disable player controls, players can get confused because their icon won't have any reaction after clicking. The players will feel that they don't have any control over their inputs since the icon will not react when they click or will have a delay if they hold for a bit, making it more difficult for them to know when it's actually going to react. This method could be inconsistent during practice mode because the player respawns at different points, making the triggers not activate. This will affect their practice experience and the way they learn the level. When using the options trigger extra care should be taken to ensure the player’s experience is as consistent and fair as possible.

# 4: Conclusion

Consistency is a key aspect of the enjoyment and quality of a level. The techniques described above are great ways to keep your gameplay consistent and fix bugs. However, the best strategy will always be to playtest your levels. Study parts in other levels you’ve played that feel inconsistent or consistent and apply those principles to your own gameplay. Finally, getting playtesters for your levels is a great way to get outside opinions on the consistency and fairness of your gameplay.





## Credits
Created by @Eclypse and @kyouki
