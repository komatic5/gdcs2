---
title: Mechanics 2 (Gameplay Loops)
weight: 702
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Short** (5-7 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- Gameplay loops are essential for keeping players interested in your gameplay.
- A good gameplay loop should be easy to understand, expandable over time, and reward the player.
- Skill Chains are effective for implementing gameplay loops into your level.

{{< /callout >}}

** **
Ensuring player engagement throughout gameplay is crucial for any level. So, the question arises: "How do you keep a player interested in your gameplay?" The answer - Gameplay Loops. If you’re making a minigame, or considering how to use a custom mechanic as described in Making Mechanics, you should certainly read this guide.

# 1: What are Gameplay Loops?

Let's define what exactly a **Gameplay Loop** is: __the core actions the player repeats throughout the gameplay.__ They represent the “core” of your gameplay and keep the player driving toward the end goal. Additionally, gameplay loops tell the player something new about your level. 

Gameplay loops can occur at any stage of gameplay. Basic loops include controls, determining actions and their outcomes in the gameplay - like moving, jumping, and clicking orbs - which are small gameplay loops. 

For example, Geometry Dash involves a gameplay loop of playing a level, dying, and retrying, emphasizing trial and error. However, not all loops follow this pattern.

*Larger gameplay loops build upon the smaller ones to work.* You may use your abilities to move and jump from one platform to another, which represents a loop. Moreover, you can determine which platforms are best to jump towards to get a coin or beat a level, which is an overarching goal. 

*This is important to consider because a bad gameplay loop will immediately take the player out of your level*. If you’re making a custom mechanic but the controls are subpar, players will leave quickly. If you’re using existing mechanics in an unintuitive way, people will struggle and give up. If you don’t give the player a real reason to keep moving forward, they will stop and go to something more engaging.

Here are two examples of Geometry Dash levels that use custom mechanics for a gameplay loop. One of them does a good job at it, while the other doesn’t.

VEIL by neigefeu: 

- The gameplay loop here revolves around the orbs tracking the player’s position - a custom mechanic in the level. Think of learning the level as the following steps: “Look at the next section, determine where I’ll need to click on the orbs, move properly to position the orbs now, repeat”. The mechanic is intuitive and can be seen from the first few seconds of the gameplay.

{{< youtube 0mYIK9zp5eI >}}

DAYA by WerewolfGD: 

- The gameplay loop in this section revolves around controlling the player’s position using the 2-player mode. This is how you’d learn the section: “Look at the next section, determine where I need to move properly to avoid dying, repeat”. Unfortunately, this mechanic is introduced halfway through the level which gives the player less time to get used to it. Additionally, the mechanic suffered from bugs which made it harder to understand.

{{< youtube 0XdeZ9zlyg8 >}}

# 2: Good Gameplay Loops

It’s very easy to notice when a gameplay loop sucks, but intentionally designing a good loop is much more difficult as you may guess. Thankfully, there are some factors you can consider as you evaluate your gameplay.

A good gameplay loop must:

- Be easy to understand. Do not start your gameplay loop with a complex set of actions unless it is impossible to simplify things. Otherwise, it’ll be hard for people to start playing your level. 
- Be expandable. If you’re doing the same thing over and over without getting anything interesting from it, then players who understand the loop will get bored. Keep in mind the prior guides on the Flow state; over time you should introduce extra mechanics that can make the loop more interesting. 
- Be rewarding. If you finish a game loop but don’t get anything from it, you’ll feel cheated. When the player does what you want you, reward them as soon as possible, and vice versa. This helps players finish the loop and feel motivated to continue playing.

For example, let’s look at Rain World’s main gameplay loop: 

- The game’s loop can be summarized as “Get food, hibernate, repeat”. Hibernating lets you escape the rain which instantly kills you, and for that you must find food. 
- To get food you can either find plants to eat or kill animals. You’re near the bottom of the food chain, so being cautious not to run into enemies you can't fight is a must. 
- Hibernating enough times gives you Karma, which is required to pass into new regions and beat the game.

This loop is simple; I can describe it in two sentences. It’s expandable; because of food and Karma, the game’s platforming, map, and combat become accessible, which keep things fresh over time. It’s also rewarding; by playing cautiously and being prepared you can progress through the game. A good loop like this will give you plenty of ideas that you can implement in your level.

# 3: Implementing Loops

After creating a gameplay loop you’ll need to use it inside your level. *Since gameplay loops rely on mechanics, you must map out how each mechanic will tie into your loop.*

**Skill Chains** are a useful tool to improve your gameplay loops. As all gameplay loops should teach something to the player, you must start with a goal for that loop. In Rain World, the platforming gameplay loop aims to equip players to handle enemies and hazards, while providing the means to complete the game.

To this extent, ensure your gameplay loops align with your overarching theme. This can be something gameplay related, like trying to explore every possibility a mechanic can provide. Alternatively, it can be something related to a story, where a mechanic becomes an ability needed for the player to progress through the narrative.

In either case, there’s a few steps you can take to produce a set of gameplay loops for your level, which is outlined below. They will help you simplify the process of creating your gameplay loops.

- Define your main level idea, being as specific as possible.
- Quantify the skills you want the player to learn through your gameplay, and use those to define some core mechanics. 
- Create a *prototype* game loop that combines the main mechanics and can be expanded upon.
- Get playtesters to your gameplay and use their feedback to improve and refine your game loop.


## Sources
- [GameAnalytics: How to Perfect your Game's Core Loop](<https://gameanalytics.com/blog/how-to-perfect-your-games-core-loop/amp/>)
- [Daniel Cook: Loops and Arcs](<https://lostgarden.home.blog/2012/04/30/loops-and-arcs/>)



## Credits
Created by @etherail and @koma5
