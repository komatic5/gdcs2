---
title: Making Optimized Setups
weight: 615
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Medium** (13-15 minutes)

During the creating process, you will be met with various issues regarding the performance and effectiveness of your trigger setups. This guide seeks to help you better optimize and organize your triggers.
## Why Optimize and Organize?
**Optimizing** __is the practice of enhancing a system to run faster, be more accurate, or have little to no bugs__. On the other hand, **Organization** __is the practice of reordering the various elements of a system to enhance their readability__. These two practices are crucial to ensure a pleasant experience for both the creators and players.

# 1: Optimization

## Lag 
One of the main reasons you’d want to optimize your systems is to minimize lag, which causes frame drops and, in the worst case, can crash the game. The following reasons are the main contributors to lag issues within a trigger system:
- **Overloading:** Too many triggers running at the same time, especially the more complicated or demanding ones, consume a great amount of resources.
- **Creator bugs:** These bugs are caused by an incorrect use of triggers or a faulty implementation of your system.
- **Game bugs:** These bugs cannot be fixed, due to them being caused by the game code. If you encounter a bug, make sure to report it to RobTop or an elder mod.
There are other causes for lag that aren’t related to trigger usage but are worth checking out, for that read the [Deco 1 optimization guide](https://discord.com/channels/414295025883545600/1086730328271491114). Note that, while there are various factors that affect the general performance of your level, it hugely depends on the device you’re playing in; a powerful computer would suffer less lag than an old mobile phone.

## Correct choice of triggers:
Each trigger performs differently due to the way it’s coded, so it's important to determine a trigger’s strength and when to use it over another. For example, a move trigger is very performant, but its follow feature is very unreliable compared to Advanced follow. The graph below shows how much different triggers affect the game’s performance. The metric used is frames per second (FPS) as it’s the most affected. Since triggers are mostly based on the CPU, objects have been toggled off in order to prevent decreasing the FPS due to the graphical rendering.

**CPU used:** AMD Ryzen 5 7600 X.
**Game version:** 2.207.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1C7AUKTtfy-ygNMFLJhHxv3oLrRfI1-Xx/preview?usp=drivesdk></iframe></div>

Level ID: `115004379`.

## Practices to Reduce Lag

Given the information of the previous sections, a lot of optimization comes from choosing the most fitting triggers for your situation and keeping the amount of running triggers at a minimum. However, there are a lot more practices that you can use to improve the performances of your systems even further. 

**Halt unneeded processes**
Remember to stop or pause any triggers or loops that aren’t being used.

**Minimize dynamic and extended collisions** 
Avoid using too many dynamic collision blocks. Check which block ID has the lesser blocks and assign Dynamic to those blocks. Enabling extended collision can cause lag as well, so lower as much as possible the amount of objects that have that feature.   

**Playtesting**
Playtest your level on lower end devices. Ask your playtesters where and how they encountered any performance drops. Additionally, if you are on PC, you can increase your FPS to a really big number and identify in which areas it drops more.

**Planning**
Write down an algorithm for your system before building it, this can help you figure out what and how many triggers and IDs you’ll need, and also help you spot errors faster.

**Fast, Cheap, Good**
In multiple cases, you will be met with a choice between 3 features: fast, cheap and good. You can almost always only choose 2 out of the 3: 
- Good and cheap, but not fast.
- Good and fast, but not cheap.
- Cheap and fast, but not good.

For example, imagine we need a random number generator. One way to achieve this is by using the Advanced Random trigger, where each value is represented by a pickup trigger with its own group ID. The more values we need, the more costly it is for this solution to be implemented and modified due to the increasing number of pickup triggers. Another approach is to use a timer ID, which can be stopped using a spawn trigger with varying delay that activates a stop trigger. This provides a larger range for random values, but is slower by design compared to the first solution.

**Loops**
Loops are one example of accurate setups; they can repeat indefinitely, and be stopped whenever a condition is met. They also save on some IDs compared to a “no loop” approach. However, their downside is that they are not instant; a trigger can only activate once at the same frame, therefore each loop iteration takes a minimum of 1/240th of a second, or 4.2 ms.

Here’s an example on how you’d use the practices above. Say we want to implement the exponential function exp(x). The exponential of a real number x is the constant number e = 2.71828... to the power of x, it can also be represented as an infinite sum:

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1NkiL-SRInPnW1EWUrd7oBRJAIU3iRUvG/preview?usp=drivesdk></iframe></div>

We can build this using the following algorithm: 
```
Objects:
    X: Real variable // already set
    Exp, U: Float variables set to 1
    PrevExp: Float variable set to 0 // used to stop the **Do** while loop
    k: Integer variable set to 1
    Tolerance: constant set to 0.01 // used to stop the **Do** while loop
Start:
    Do {    
        PrevExp = Exp    # PrevExp will keep track of the current value of Exp
        U = (U * X)/k         # calculates the value of x^k/k!
        Exp = Exp + U      # update the value of Exp
        k = k + 1              # increase the index
    } While ( Abs(Exp - PrevExp) >= Tolerance ) # repeat until the difference is as small as we want
End
```

The algorithm can be translated to GD as such:
- X = Item ID 1.
- Exp = Item ID 2 set as timer.
- k = Item ID 3.
- U = Item ID 4 set as timer.
- PrevExp = Item ID 5 set as timer.
- Item ID 6 is used to store Exp - PrevExp.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/141B8bkKGjNMfKSZQ4j9sjskmI9WMm1HJ/preview?usp=drivesdk></iframe></div>

Spawn trigger: has GID 2, spawns all other triggers (GID 3).

This setup can calculate the value you need with all the precision you want, but it can take a while to compute, especially for large values of X. However, we can do it another way. Instead of having an infinite number of iterations, you can copy paste each iteration multiple times to get a satisfying enough value depending on your needs. This option gives you an instant answer as there isn’t any spawn delay downtime.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/13S1rKLW7hSpvG-XmNEszHA8il83dDRqw/preview?usp=drivesdk></iframe></div>

You can notice the difference between both setups in the video below: the first solution gives the most accurate value, while the second gives the fastest answer.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1RNIk3EbTbDQgGWcT-saVkNTmJO3y1X8N/preview?usp=drivesdk></iframe></div>

Level ID: `115004354`.

## ID Simplification and Spawn Remapping
The simpler a trigger setup is, the less prone it is to bugs and lag, and the easier it is to understand. Avoid adding unnecessary complexity to your system like extra triggers or IDs. 2.2 brought new ID types which can reduce the complexity of your setups:
- Group ID parent removes the need for an extra Center ID, and can even fix bugs, like moving objects that rotate around a center.
- Group parent allows the use of one Advanced Follow trigger for multiple complex shapes, as all linked objects follow the movement of their group parent.
- Area parent is similar to group parent in that all linked objects follow their parent, removing the need for any extra follow triggers.
- Control ID, while mainly used for spawn remapping, can save on some group IDs for more important use.

Reuse IDs when possible; objects that have the same movement can use the same group ID. Using functions, or spawn remapping in general, greatly decreases your ID usage as well. For example, if a trigger setup uses 5 IDs that will be remapped, then you’ll save 5 IDs every time you use spawn remapping. Making changes to setups is also faster, since you’ll only need to change the original trigger setup, instead of having to check every copy.

# 2: Organization

This section discusses practices that help in the readability of your trigger setups. To make your systems more comprehensible, make sure to:
- Leave space between trigger setups to improve clarity and reserve some space for extra modifications.
- Keep your triggers next to the objects or space they act on to improve navigation.
- Each trigger must be visible. Avoid placing triggers on top of each other.

How you **sort** and **label** trigger setups is important as well, as doing that helps to convey much easier what the setups actually do. We’ll cover each of these in more detail.

## Trigger Sorting:
**Trigger sorting** __describes how you can place your triggers in relation to others to improve the readability of your systems__. These sorting methods are not exclusive, and can be modified or mixed together depending on your needs.

**Box sorting**
You can highlight trigger setups by surrounding them in a frame. This method groups triggers that work for a specific task, and help the reader easily identify trigger setups and differentiate between them.
Use line objects (outline solid blocks with NoTouch enabled, deco line objects…) to create a box around your triggers, generally in a rectangular shape. You can also divide this box into sub-sections, for example grouping pulse triggers together.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/14baAXWXFsKDw2yQz752hFGiJFZ2NvCHk/preview?usp=drivesdk></iframe></div>

**Branch sorting**
You can link triggers together with the relations they have with each other. Generally, a spawning trigger is linked with the triggers it spawns. This method highlights the chain of activation between triggers; a reader can easily find what caused a specific trigger to activate.
Use arrow objects or line objects to draw a link between 2 triggers; you can link one trigger with more than 1 trigger. The final shape will have the structure of a graph. Here are some examples of how you can branch your triggers:

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1C4e0qCoUmiIgr2HaHdDhlxg8yLetK4Lo/preview?usp=drivesdk></iframe></div>

You can also use symbols instead of lines to indicate the direction or if the condition was true or false (see example 2). Branching is especially useful to represent loops (see example 3).
Notice how you can build your system both horizontally or vertically. If a part of your system depends on the order in which triggers are activated, it is recommended to sort them left to right, in order in which they must spawn. This will let the reader know the trigger’s order without ambiguity (see the exponential function example). For more information, check the [Priority Order guide](https://discord.com/channels/414295025883545600/1230618156565921894). 

**Pillar sorting**
You can place all triggers that happen at the same time in a vertical pillar, similarly to how non spawn and touch activated triggers are sorted in classic mode. This method orders triggers chronologically; a reader can easily figure out when a trigger might activate.
This method has been improved by @TheMilkCat, below are some of the guidelines they created:

- **Unicity of Spawn trigger:** A pillar should contain only one Spawning trigger (Spawn, Collision, Count…) , which activates this pillar, in the case of multiple spawn triggers, divide the pillar into smaller ones, where each has its parent spawning trigger and the triggers it activates.
- **Sorting triggers by type:** In a pillar, the Spawning trigger should be on the top of the pillar, followed by Toggle On triggers then Toggle Off triggers. The remaining triggers should be sorted by the order they appear in the triggers tab.
- **Sorting triggers by ID:** In a pillar, triggers of the same type should be sorted by the ID they affect, in ascending or descending order.
- **Pillar Alignment:** In a chain of pillars, all parent Spawning triggers should be on the same Y level, pillars with no spawning trigger are one block lower.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1oUwMI-IRJ5ntX5ZamlYfxXAQw5-JAzrG/preview?usp=drivesdk></iframe></div>

## Labeling
Labeling trigger setups helps with their readability and makes it easier for the reader to figure out the function of your systems. There are multiple ways to label setups:

**Naming Functions**
They are short descriptions, usually 1-3 words, that explain the general purpose of this function or trigger setup. 
Use the text object in 0.5-1.0 size on top of the trigger setup, don’t over exceed the width of your triggers. You can also use symbols, for example using the skull deco object to label a function that does a death animation.

**Commenting**
For complex setups, it’s good practice to write a small description about what the triggers do. Keep it short and direct, there is no need to describe every small step.
Use the text object with 50%-75% opacity and 0.5-1.0 in size, keep the length short and avoid making the comment larger than the trigger setup itself.

**Color Coding**
This is mostly useful for identifying important triggers without the need to dedicate text space inside a trigger setup. For example, you can assign the color red to a function, and color any spawn trigger that calls it red.

To color a trigger, select a colorable object with the desired color channel (and HSV), click copy values, then select your trigger and click copy color. Note that the final color will depend on the original color of the trigger. Alternatively, you can place a full square block behind your trigger with the desired color.

**Editor Layers**
In large trigger clumps, you can give related triggers the same editor layer to isolate them while modifying. Additionally, you can give each editor layer a title as a text object, and dedicate one editor layer for all titles (using editor L2) for easier navigation. Below is an example of various labeling methods being used.

<div><iframe src=https://drive.google.com/file/d/17NXyfxT_bR7dYOoOK7Y3akC8n1a0A1Vs/preview?usp=drivesdk></iframe></div>

- Function 1’s name is colored red, while Function 2 is colored yellow, this is also used for the spawn triggers that activate them.
- The comment on top explains what both functions do without describing each one individually, as they can be understood from the triggers used.

## Balance
While these methods can greatly improve the readability of your trigger setups, remember that overusing them will eventually make your triggers hard to navigate. For instance:
- Box sorting is useful for medium to large sized trigger structures, using it for every small trigger setup defeats its purpose.
- Comments are to be kept simple and short, they describe the general idea of a system, not the details.
- Color coding too many triggers can make your setup very distracting.
Choose the labeling method(s) that make you comfortable, while keeping things understandable for readers.

## ID management
It’s good practice to dedicate a range of IDs for a specific system. For example, when making an enemy, I can use group IDs 100-110 for deco objects, item IDs 111-115 for health and/or damage…, block IDs 116-119 for collisions, etc.
This makes tasks like spawn remapping much easier, as the next enemy will use IDs 120-139 and so on.
However, managing IDs can be challenging to pull off correctly, as it can raise various issues:
- **Case 1:** a tight range of IDs prevents further additions to a trigger setup. For the previous example, adding a second attack for the enemy would require me to use a couple of IDs above 120, which are already used by the second enemy.
- **Case 2:** a loose range of IDs creates wasted IDs. In the same enemy example, if I used IDs 100-139 (accounting for the first case), then 20 IDs would go to waste if kept unused.

To mitigate this, you can use multiple types of ID within a single remap. In the example above, IDs 100-110 can host the group IDs for deco, the item IDs for health, *and* the block IDs for collisions, while saving the rest for additional features. Although, if you do this you’d need more comprehensive ID tracking. You can check the [Using IDs guide](https://discord.com/channels/414295025883545600/1189381677978484877) for more information.

In any case, this step should be used close to finalizing the trigger system or in advanced trigger setups where ID management is mandatory.

## Summary
- Optimizing your levels is important to provide a smooth and bug free experience to a larger range of devices.
- Organizing your levels speeds up the creating process and makes your setup more readable for others (in the case of collabs for example).

## Sources
- Trigger Building Guidelines by @TheMilkCat

None



## Credits
Created by @ChuckOlate, @TheMilkCat and @eggyolk
