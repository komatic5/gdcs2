---
title: Mechanics 3 (Feedback)
weight: 703
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Short** (8-10 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- Feedback in games or levels encompasses how information is conveyed to the player.
- Feedback can come from visuals, sound, and responsiveness; as long as it is tangible.
- Feedback teaches the player the rules of your game/level.
- The information that feedback gives to the player and how the player responds creates a feedback loop.
- Different games and mechanics accommodate different types of feedback, so be mindful with those details.

{{< /callout >}}

** **
By this point, you would have a mechanic and its gameplay loop for the player to repeat. However, these elements alone are not enough for a game if they are not clearly taught to the player. This is why *feedback* is important in game design. What is feedback? How can a creator design feedback that reflects the intended feeling of a mechanic? This guide will explore these questions.

# 1: What is Feedback?

Let’s start off by defining feedback. At a glance, you can say that feedback tells the player that they’ve used a mechanic, usually through visuals. However, there’s more to this as the key point here is *information*. **Feedback** shows *how the game/level conveys any information to the player*. Any tangible thing that the player can see, hear, or interact is a form of feedback, acting as a teacher for your mechanics. Take this video for example and compare these two dashes: notice how the second dash’s visuals conveyed the mechanic more clearly.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1zlUyfRrdjo69DV8iXLyqSob2U8oWK6X2/preview?usp=drivesdk></iframe></div>

As the player needs to click to activate this dashing mechanic, responsiveness becomes a factor; they help with the way players perceive the mechanic. You can influence the player’s experience if you can help them understand and sense your game’s mechanics.

On a surface level, players will have a subconscious opinion of how a mechanic feels at the very start:

- “This attack feels powerful.”
- “This movement feels janky.”
- “These controls feel natural.”

Players think about these mechanics even if they don’t say it out loud. This is why feedback matters: it directly controls the feeling of a mechanic, which changes how the game feels as a whole.

# 2: Using Feedback

Before you start crafting the feeling of your mechanic, let’s settle some baseline information:

Whether your mechanics are simple or complex, players should CLEARLY know that they’ve interacted with your mechanic. Design your feedback the same way you would teach someone: would you mislead them? Would you make them have zero clue on what they’re doing?

Gameplay is rarely fun if the mechanics are obscure or inconsistent, so you should make sure players know what they’re doing. There can be exceptions to this depending on the level’s idea. 

Let’s take a look at the earlier example. Because players can freely rotate the dash, a moving arrow is placed to show its direction, followed by a small trail to emphasize the player’s path. The player can use the dash to break fragile walls in the actual level; the “shield” in front of the icon further conveys the dash’s strength. All of these little details teach the player about what the mechanic does visually.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1s32wu189FfSYJtMI9EHMYn_v6uBLmTyM/preview?usp=drivesdk></iframe></div>

Generally, the more visual effects and sound effects you put on a mechanic, the more important it feels. While there's a balance to this, you can use visuals to convey the hierarchy of a mechanic; some mechanics will be more powerful than others after all. While this extends into animation territory, it’s still good to know that you can use visuals to show importance.

In the video below, you can see a big explosion when the player dives into the ground and bounces. This doesn’t actually explain the dive’s functionality, but it does show the dive’s strength.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1MqAxh4zJxdOJZC7uRtLNdHlTamM6ZCsp/preview?usp=drivesdk></iframe></div>

Aside from visuals, you can also influence what the player hears to convey your mechanics. Listen to how all these mechanics below have different sounds, giving them each a unique identity. However, this guide won’t be talking as much about how to make SFX themselves as that’s for the Sound Design guides.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1KdVv0L00pGjA1UXk9CxxC7NmqDkfab0X/preview?usp=drivesdk></iframe></div>

Another form of feedback is how soon an action is performed after a player input - the responsiveness of an action. For a rhythm-based game such as Geometry Dash, players expect an immediate response after an input, especially for extreme demon levels; it’s why you can see many extreme demon players discuss about input delay.

With that said, the responsiveness of a mechanic shows a lot about how it should be used. Mechanics that are highly responsive show that they are reliable and available to use often whenever they want, whereas mechanics that respond slowly show that it requires timing and is important to get right.

Obviously, not every fast or slow mechanic follows these, but it’s still a first impression that matters which can be manipulated.

# 3: Advanced Applications

Feedback conveys information, and you can manipulate this information to guide the player. Visual feedback tells what a mechanic does, but you can bend how the mechanic works with other mechanics to reward and punish the player. For example, imagine an enemy swinging a giant hammer. Getting hit by the hammer will deal heavy damage to you, telling you to *watch out and dodge* the swing next time. If the enemy misses the swing, they topple over and need to recover, giving you time to attack the enemy, which once again reinforces you to *dodge the attack and punish*. If the hammer didn’t do enough damage or didn’t give the player enough time to attack, the intended purpose of the hammer swing wouldn’t work. Having an obvious “right” or “wrong” at the very beginning of a level will help reinforce the general approach to an obstacle for the rest of the game too; in our example above, players will know what to do and how to dodge for the rest of the game.

Of course, a lack of information may be useful at times too. Not giving a clear “right” or “wrong” outcome will leave the player to do what they want and *figure out what to do themselves*. This creates puzzles and strategy; you need to think about how you’re going to approach an obstacle on your own. Strategy will be further covered in [Mechanics 5](<https://discord.com/channels/414295025883545600/1099913209319796748/1099913209319796748>). For example, Minecraft has a unique system called redstone, which you use to make various contraptions in the game such as farms, doors, computers, flying machines, etc. When a piece of redstone dust - the most basic component - activates, it lights up, which acts as basic visual feedback.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1HCAAfjOY30R6H7OSxx8T_wiY_NEIQGkA/preview?usp=drivesdk></iframe></div>

Running dust into the side of a repeater, a different type of redstone component, will do nothing, teaching that repeaters work from the front and back.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1Y8jCwgxcEgvGl5hd377ypAqYMWFJ9MdN/preview?usp=drivesdk></iframe></div>

Minecraft uses feedback to teach basic things like that, but it’s different on larger scale contraptions like a redstone door. When something goes wrong, the player has no idea where and has to go through their contraption to find the error, making them rethink their logic and promoting more strategy (apart from the logic to make the contraption in the first place). 

While on the subject of Minecraft, let’s cover a sneaky feedback mistake that you have to look out for. I mentioned how redstone dust can’t go into the sides of repeaters, reinforcing the idea that they only work from the front and back, but this isn’t always true. Running the front of a repeater into the side of another repeater can lock the second one, which is a unique mechanic that is really niche due to it contradicting the “assumptions” of redstone dust. When using feedback to teach a mechanic, make sure it aligns rather than contradicts with other mechanics.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1qWm3On7LNkjT_koQKI_x1ccus_lvq8Sq/preview?usp=drivesdk></iframe></div>

## Feedback Loops

The next application that we'll cover is feedback loops. A feedback loop is when your game/level provides information to the player, which will hook the player and make them respond, which will provide more information and the loop continues. This loop is designed to create engagement. You can see this everywhere:

You message your friend → Your friend responds with their message → You respond to your friend’s message → Repeat 

As you hear the message notification or popup, this will make you want to text back as you wouldn’t want to leave your friend hanging (hopefully), and then your friend messages you back and the cycle continues.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1cTJW4yY1Twq76Ii7xDoDQ4I2kBML78kr/preview?usp=drivesdk></iframe></div>

When designing feedback loops, you need to decide on an action that the player will take and its results. The result should further engage the player and incentivize them to repeat said action. Upgrades are another example, because you get a small boost regularly that makes it easier to continue getting boosts and continuing the cycle. Feedback loops are fundamentally similar to gameplay loops and progression but are simply smaller in scale. Breath of the Wild and Tears of the Kingdom involve exploring big regions to defeat their local divine beast/temple, but there are also shrines all over the world which fulfill the same purpose on a smaller scale; explore a small area, complete the local shrine, continue on. It’s a small dopamine rush that’s easy to continue, while slowly building up the bigger gameplay loop.

<div><iframe src=https://drive.google.com/file/d/14FqslFZVBLHbgChP3pPLfliFlZRtCwnj/preview?usp=drivesdk></iframe></div>

## Know Your Game First

Finally, keep in mind that different games require different types of feedback. Calmer adventure games such as Hollow Knight wouldn’t require a detailed UI that tells the player everything they need to know because it’s a streamlined single player experience. First person shooter games such as Fortnite on the other hand have much more information in their UI: health, ammunition, inventory, number of remaining players, location. Players need to know a lot more than their health to play optimally while having fun. In fighting games such as Super Smash Brothers Ultimate or Xenoblade Chronicles 2 where the players’ reflexes are tested, the exact speed of the character animations are crucial, making sure that the mechanic’s feedback is finely tuned to the gameplay. 

Another point to mention here is cutscenes. Single player games such as Ori would use them while removing player controls since the player isn’t supposed to die in these sequences, but implementing this exact system to competitive multiplayer games such as Fortnite? Taking away player controls becomes incredibly frustrating, creating this “animation lock”.

Know your game mechanics first and the feedback will follow suit.





## Credits
Created by @Selena and @ontos
