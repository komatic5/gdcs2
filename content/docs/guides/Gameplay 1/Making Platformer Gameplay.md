---
title: Making Platformer Gameplay
weight: 419
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Short** (8-10 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- Platformer mode is a new level type introduced in 2.2 that allows free horizontal movement of the player.
- Writing down ideas and brainstorming gameplay helps tremendously in making platformer levels, along with having a clear idea of what makes good quality gameplay.
- There are many genres of gameplay that a platformer level can take on, some notable ones being Standard, Room, and Needle gameplay.

{{< /callout >}}

** **
# 1: What is platformer mode?

Platformer mode was introduced in 2.2, which completely altered the main gameplay loop. Unlike classic mode, you have complete horizontal freedom of movement via the arrow and A and D keys or the mobile UI controls.

Another difference to note is that instead of respawning at the very start, you can add checkpoints to aid the player; dying after making contact with a checkpoint will place you at the checkpoint’s location. Platformer levels also reward moons instead of stars, which operate in the same manner. Physics are also altered between modes, making some actions not the same compared to Classic.

# 2: Making Platformer Gameplay

## Ideas

Brainstorming ideas for a platformer level helps tremendously with the creating process, as having a roadmap for what the gameplay should be like makes the process overall easier. In order to come up with these ideas, you should take inspiration from either existing platformer levels, or games you’ve played. Having little to no experience with either will lead to vague ideas, making it harder to gauge what good platformer gameplay is. Although, please don’t make a 1:1 recreation of Celeste; people will appreciate creativity more than recreations of existing work.

Platformer levels often have diverse gameplay loops from each other, which is something worth knowing, as the diversity that platformer levels have can help you with making ideas; diversity brings awareness to aspects that are important to gimmicks or just gameplay overall.

Making the gameplay itself is rather complex, but this will be further explained in the next set of sections.

## Triggers

Despite the fact triggers will still behave the same way they would if placed in Classic mode, they are used differently in practice. Trigger setups are more convenient to use when activated via spawn triggers or the touch triggered option. Using them without touch triggered enabled is still useful but only for scenarios such as syncing with the song.

## Mechanics

Adding mechanics in a platformer level helps make your level stand out, but can sometimes be hard to implement. Following a simple procedure to test your mechanics helps greatly.

To start, use a mostly empty area in order to start creating and testing your mechanic freely. This area should not include obstacles if the mechanic hasn’t been fully tested yet. Thought should be put into how your mechanic will work, which will give you a general idea of what triggers/objects to use for that mechanic. This process does take time due to unexpected bugs, sometimes at the hands of developer error, but these issues are solvable.

Say your mechanic is done and works well after some basic testing. Now you’ll want to add more obstacles to test its behavior. Methods of testing such as spamming or using the mechanic in unintended ways will open up possible bugs you may have been unaware of previously.

## Layout

During layout creation, you must take into account the key elements of the gameplay you've decided to make. For example, a level based on dash orbs and momentum based gameplay would utilize layout design that focuses on timings or other techniques that these types of levels may use.

# 3: Platformer Gameplay Quality

Given the freedom provided by being able to build platformer gameplay, it comes with responsibility; setting a good impression for the player with how the level plays is important since platformers are more casual compared to classic. Learning concepts beyond what you learn by making levels in classic mode, whether through teaching mechanics or making gameplay in a progressive manner will help with the gameplay creating process.

## Teaching Mechanics

If your level includes one or more mechanics that are integral to the gameplay, you may want to introduce the player to them to make the experience easier to understand. A good way to teach mechanics to the player is to give them a safe place where the player can interact with the mechanic to get an understanding on how it works. After that, you can create simple gameplay based on that mechanic so that the player adapts to it and can be prepared for more complex situations.

## Difficulty Progression

In platformer mode and games in general, instead of keeping a consistent difficulty in each part you can opt for harder sections the further you progress, making sure to add checkpoints along the way. While this is the case, do make sure that each section has proper balancing as to not have an unfair spike in difficulty. An example of a difficulty spike in this case would be a level whose first section is medium demon gameplay, but cuts to precise insane demon gameplay after the first checkpoint.

## Fair Gameplay
Artificial difficulty is an inefficient way to make a level hard, as it makes the experience unfair to the player and solidifies their belief that their deaths are caused by creator error. Many factors contribute to the artificial difficulty category, whether it's poor camera controls like the ones seen in blind sections of gameplay in DownWell, or the difficulty depends on bad RNG in Stella Infection. Making a platformer level with fair gameplay is important, since otherwise your level may hinder from these executive flaws.

## Gameplay Tips
One tip that can improve the overall experience of your gameplay is by not making gameplay that could otherwise be possible in classic mode. This is not engaging for the player and can bore them fairly quickly. Instead, opt for gameplay that involves a sizable amount of horizontal displacement.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1xGrUg6fOkDVPdv4lYAJukPJbivYQbmjo/preview?usp=drivesdk></iframe></div>

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1rTcwF_xdr8ZssAdfvE_Z8TP0P9KBVlu6/preview?usp=drivesdk></iframe></div>

## How is this achievable?
When making the level you’ll likely have the bias that nothing is wrong because you believe the gameplay you made is better than anyone else and you will have flaws that are less serious, but people will think differently, leading to varying opinions. Getting playtesters will help with this greatly.

# 4: Types of Platformer Gameplay

After understanding what principles make up basic platformer gameplay, we can cover different genres of gameplay.

## Standard 

This is usually the most common gameplay type for levels. It’s known for being straightforward and is something anyone can pick up. They usually don't include too many gimmicks and stick to the vanilla experience.

Levels such as The Sewers, Platmosphere and Over the City by Robtop, Gabbs, and PAHC respectively are clear examples of this level type. The images show the levels listed in order.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1_CpdW94UeAhxkspt50y5pyy4K79-YsuN/preview?usp=drivesdk></iframe></div>

## Rooms

This is also a common type of gameplay in GD. This usually involves each part being separated by the use of boxing off the gameplay in different rooms. Some examples are Gateway by vyp, Twenty Trials by morpe, and Die to Win by ReyRU.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1Jox6b6ihw0D2pOpCUke-rlsP4kE5CHiJ/preview?usp=drivesdk></iframe></div>

## Momentum Tech
This type of gameplay utilizes the player's momentum in unique ways. It often uses dash orbs to boost the player, but is not limited to just that. Slopes and platform movements are also used. Some examples are SpeedTek by G4lv4tron, Zip Lash by Colon, and SpiderTek by OWOSI. SpiderTek is an exceptional example of this gameplay type.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1FfEwZkJswkPk-5Rltzu0sG_9b-J6IUzt/preview?usp=drivesdk></iframe></div>

## Autoscroll Gameplay
This type consists of gameplay where the camera is locked to a center point and moves to the left or right until the end. This kind of gameplay can also be seen in games such as Super Mario Bros. 3 with its airship levels, along with many levels in Mario Maker. GD levels that use this type of gameplay are Maximum Security by Buziris, Crerro Kaizo I by Crerro, and The Lightning Road by KingEggplant987.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1Xa3F7yG4zv3Ozhm1v3UyYb9ewgQ2Ju7u/preview?usp=drivesdk></iframe></div>

## Speedrun Gameplay

This gameplay type limits the amount of time that the player can beat the level. Some examples are Decaying Silo by LunarLeo77, Loco Motive by Subwoofer, Fast N Accuracy by lplmal, and Calamitous Fortune by Xyraphella.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1ANhXkbTFDoz9DhwHJF-5lfZM3qys_tTo/preview?usp=drivesdk></iframe></div>

## Needle Gameplay

This type of gameplay is popular among insane/extreme demons in general. It usually takes inspiration from “I Wanna be the Guy” and is known for having tight and precise timings that abuse hitboxes. This gameplay includes but is not limited to the robot gamemode. Some examples are I wanna be the guy by Orelu & Aless50, The Abyss and Tower of infinity by zYuko, and Arachnid Tetris by spark.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1F1fvQnvdR6WWZN7Q67IZMF43zuBUws3S/preview?usp=drivesdk></iframe></div>

## Bossfight Gameplay

This type of gameplay involves battling a boss, usually in the format of a Terraria boss. Some examples of this type are Logodomy by TheMilkCat, Stella Infection by LopyLuna, and Flame Arena I by ilovefreddy123.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1HHVk_IWl_2p-YG5ogOzl8QvzYdOh4VnH/preview?usp=drivesdk></iframe></div>

## Other Gameplay Types
Many other gameplay types exist that weren’t listed previously, which are either branches of what was listed or new types completely.

- Quarion by Zejoant is a Metroidvania-style level, taking concepts from games such as Super Metroid and Celeste.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1qfLPRunkNYgEjWMpqJ1cFOipZHhU92od/preview?usp=drivesdk></iframe></div>

- Only Upwards by OWOSI is an example of a puzzle level, using gimmicks to have the player think critically to get to the solution.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1Yss0Lv_0zpyNMvEiXVixZ_Kcel5shqtA/preview?usp=drivesdk></iframe></div>

- Blink Block Blitz by Codex is an example of a Blinking Block level, which is a concept used by games such as Super Mario Galaxy in some stages and Super Mario Maker 2.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1hdftb4Ihz_39DjmuBx5RFjoq2cUvlj6K/preview?usp=drivesdk></iframe></div>

- Vacuum Tank by FakeHATETAG is a Slope Boost level, which by itself is a gimmick seen in SpeedTek, where you jump up a steep slope using the player’s momentum.

<div><iframe src=https://drive.google.com/file/d/1DglwQWnoLvo4nnaT2-1OXgNaBifuHiUa/preview?usp=drivesdk></iframe></div>

These are only a few examples of platformer gameplay you may see or use in your own levels, which should give you a better understanding of how you can structure your gameplay.





## Credits
Created by @NotAModerator and @those
