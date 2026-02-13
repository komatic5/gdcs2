---
title: Detail Objects
weight: 503
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Short** (3-5 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- Detail Objects are those that the player cannot interact with, and are usually used to enhance decoration.
- There are many detail objects which we can categorize based on their shape, texture and glow.
- Any object can be used as a detail; this includes text, animated objects, or just the base or detail color of an object.

{{< /callout >}}

** **
None

# 1: Types of Detail Objects

We can classify detail objects based on their characteristics, namely their shapes, blurriness, glow, and sharpness.

Shapes can be regular or irregular, and geometric or organic.
Glow is a type of smooth gradient which is often used with blending, with the express intent of making an object shine. Blurry textures just happen to have antialiased edges, making them look blurry when they're scaled to large sizes.

Here are a few examples of objects that meet each one of these characteristics:

## Shapes

Regular vs Irregular

None

Geometric vs Organic

None

## Texture Blurriness

Sharp vs (slightly) Blurry

None

## Glow

None

# 2: Potential Uses

Having a large variety of objects means you can use objects in a variety of ways. Let's make a broken stone pillar for an example. I don't suggest copying this at all; this is just an example of some ways that you can use different objects.

First, I'll start with a simple base.

None

Then, I make the shape more complex by adding some more specific details.

None

And finally I use some additional objects to make the pillar look more interesting.

None

Now you may wonder "That's cool, but how do I actually know what objects to choose and how to place them appropriately?", so I'll also explain my thought process in more depth.

I chose a **stone pillar** as the thing i wanted to do make in the editor. I wanted to start my base with an object that would be effective for a pillar and is one block wide. The object I chose satisfies this well as the line appears to separate the pillar into two halves, which is the effect I want.

Next, I decided to start with major details – ones that directly affect the pillar's shape, letting you know that it's broken and hazardous on the top – and then moved on to minor ones that strengthen the "ruined" vibe I was going for. I made the pillar's edge more irregular using these objects in particular. As always, my main consideration for these objects was their shape; if their shape worked with my goal, I could use them.

None

I also colored these objects in a way that indicated how the pillar was being lit. There is some yellow light on the left side and some reflected purple light on the right, so I outlined the pillar in those colors accordingly.

Finally, I added more cracks inside the pillar to strengthen the ruined vibe I wanted, and some glow for depth - specifically ambient occlusion, which made it look as realistic as I wished.

# 3: Uncommon Object Uses

There are many ways to use objects in the editor; however, many of these techniques aren't the most intuitive without some prior guidance. Here are some examples of them.

- By setting an object's Base or Detail Color to an invisible color channel (opacity 0 or black with blending enabled), you can **partially mask** it and use the resulting shape in new ways.

None

- Text objects (found in the :YellowOrb: Gameplay Objects tab) are also interesting as they let you get a near-limitless amount of new shapes. You'll see these fairly often in works from people like Bli and Galofuf.

None

Here is an example from Galofuf's part in Carcass, where you can see various characters used to make shapes.

None

[Animated Objects](<https://discord.com/channels/414295025883545600/1189378539875741726/1189378539875741726>) also work well as details. Since you can pause each individual frame of them, you can effectively get multiple shapes out of one specific object.

None

Objects in the Particle and Animated Object tabs can also be used in interesting ways. However, be aware that they are always __one Z layer below other objects with the same Z layer__. As with Blending objects, you need to put them one Z layer above everything else.

*Same Z Layer and higher Z Order:*

None

*Higher Z Layer and same Z Order:*

None





## Credits
Created by @Aquarware and @koma5
