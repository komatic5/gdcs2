---
title: Low Detail Mode
weight: 519
draft: true
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Short** (9-11 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- Levels tend to lag due to high object densities and complex object properties, especially with trigger usage.
- Tick “High Detail” to an object to toggle it off when Low Detail Mode is on or use toggle triggers if you need more customization.
- Optimization refers to reducing the amount of objects used without affecting its appearance, which is important for creating less lag when playing levels.
- Some important efficiency skills to include are overlapping objects, using scaling (scalehack and/or warping), and using certain object archetypes to achieve something in a sustainable manner.
- Reducing objects can be done by creating a second copy of any group of objects that need to be optimized and using efficiency skills to reduce object count.

{{< /callout >}}

** **
# 1: How Levels are Rendered

Generally speaking, the game does calculations for every object in a level. By that logic, the more frequent and complex the calculations are, the laggier the level.
For the scope of this guide, 2 factors come to mind: **active object counts** and **object properties**.

 ## Active Objects
[Show Info Label](<https://discord.com/channels/414295025883545600/1083170592573902868/1216773432025550949>) has a description that measures the amount of active objects that are visible on  screen at any given moment.

Every detail created, every orb that was placed, and every trigger that was set up contributes to your level’s object count. Those corner pieces and low-opacity blocks that you might have used for parallax or texturing will also add up in the object count. With high active object counts, the risk of lag and input delays increase, which can affect the level’s experience as a whole.

The rule of thumb for active object counts is similar to Super Smash Bros’ health mechanic: the higher the active object count, the higher the risk of lag.

https://tenor.com/view/smash-bros-melee-super-smash-bros-melee-bat-homerun-homerun-bat-gif-26180968

If you are using merely the default static and detail objects, the most lag risk that you face will come from object density - where many objects and little details cover up the entirety of the screen.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1tTkM-n06v2-0OojxCJn0YZ7Ek-yyLL16/preview?usp=drivesdk></iframe></div>

## Object Properties

While blending and opacity eat up a level’s performance, it wasn't a problem back in Update 1.9, especially with the restrictions the editor had and the lower object limit standard they had compared to the 40k objects we are used to.

Historically, lag started to become an issue once Update 2.0 came out with groups, animated objects, and more triggers such as the Move and Spawn Trigger. Minigame levels are the best example, as triggers go beyond editing colors, the risk of lag increases.

These features snowballed to Updates 2.1 and 2.2 where players grew more concerned about lag, level performance, and optimizing details for effects and trigger setups to effectively create the vision they wanted. Additionally, with some mods allowing creators to bypass the object count limit, levels reached as high as [1 million objects](<https://youtu.be/Htg4aIoRcYw?si=hacIGUodFEURDHNe>).

# 2: Low Detail Mode

**Low Detail Mode** (LDM) __gives the player an option to limit the amount of visuals in a level to improve its performance and playability__. This is especially useful for lower-end devices. As of 2.2, there are 2 methods of doing LDM: Ticking High Detail and using Toggle Triggers.

## 1a) High Detail

You can tick High Detail in the Edit Group’s Extra tab in order to make an object disappear in low detail mode.

With that said, you can make objects only appear in Low Detail Mode if you set a toggle trigger to High Detail.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1Sql4eDH7lWR5jxmzZSsUyn_xllBBIg1q/preview?usp=drivesdk></iframe></div>

## 1b) Toggles

If High Detail is too unintuitive to use, you can create your own custom LDM with toggle triggers. 

Following that idea, sometimes you might want to give the players more customization in which details could be set to LDM. You can even use collectible objects or toggle orbs to activate said LDM. For example, in Sedulous by Samifying, there are 4 different detail modes:
1. Full Detail Mode
2. Normal Mode
3. Normal with LDM ticked
4. Min Mode with LDM ticked

{{< youtube j_Hgp-k2twk >}}

With 2.2’s upgrades in Item IDs, the amount of LDM customization has expanded.

> Would Alpha triggers work too?

Absolutely not. Changing the objects’ opacity doesn't reduce the active object count, nor does ticking the “Hide” option in the Extras menu.

With that said, if you end up using an alpha trigger for hiding your layout blocks, that also adds up to the active object count when it’s on screen.

## Which Details Need LDM?

Every level has their own vision, plan, idea, and details in mind when created. So how would someone know which details need to be included in the LDM? Going back to the [Creating Details](<https://discord.com/channels/414295025883545600/1233710767895740456/1240438278096949289>) guide and the different types of details, LDM mostly applies to aesthetic details, which narrows down what objects can be set to LDM:

- Subtle atmosphere for immersion such as background or air decoration
- Visual-heavy effects
- Intricate background art
- Details using scale trigger with a centre
- Area-trigger related setups
- Trigger-heavy setups for details

The point of LDM is to create an accessible playing experience for lower-end devices, so functional details cannot be removed. Could you imagine if ISpyWithMyLittleEye by Voxicat removes the black screen obscuring the player’s vision in LDM? Or if Skeletal Shenanigan’s bossfight removes its attack indicators?

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1hiuN2dybuPc_f_wPTXOR_95wywdb__o7/preview?usp=drivesdk></iframe></div>

If you feel that setting up an LDM is too tedious for you, the other option is to be efficient with the way you use your objects for details. This means you need to understand your detail’s properties, shape, function, and match them to the existing objects and features in the editor with as few objects as possible.

# 3: Detail Intricacy vs Object Count

If the details you created are more intricate, the higher the active object count. These shapes can be categorized into two types: primitive and complex.

## Primitive Shapes

**Primitive shapes** are __objects that can be found in the editor without doing anything besides scaling__, these can include squares, spike triangles, hexagons, stars and circles. When designing a base for your decoration, these will be very helpful as they only add 1 object.

## Complex Shapes

**Complex shapes** are __created once you start combining or skewing shapes to create new ones__. For example, pentagons don't exist in the editor as one object, so you need to make 1 yourself.

While there are curved objects available in the editor, sometimes they might not match your level’s vision. To that effect, you may want to make your own curves as explained in the [Using Deco Objects](<https://discord.com/channels/414295025883545600/1233650406089949254/1234246152925221014>) guide. However, these creations consume more objects that increase the risk of lag, especially when locked into triggers for effects.

# 4: Methods of Optimization

**Optimizing** within the context of decoration is described as __reducing the object count of a level’s visuals while maintaining its detail and quality__. Like a puzzle game, the aim is to get the same visual quality with less objects. There are certain methods on how to achieve this:

## Common Methods

## 1a) Overlapping

**Overlapping** objects is usually the easiest way to optimize. You simply delete objects which are fully covered by others. This works best on decoration that uses many layers.

## 1b) Scaling/Warping

**Scaling**  is another simple way to reduce object counts. By making one object take up more space, you can use far fewer objects to fill in the needed space. Note that this is much easier with warping.

> *Warning*: GD renders large objects differently depending on their hitboxes but this can be remedied by ticking NoTouch to remove the hitbox. Be careful with this because it can cause visual errors.

<div><iframe src=https://drive.google.com/file/d/1SbmTH_Sp1LEu1efhi6I1uW9EfAYzmwd5/preview?usp=drivesdk></iframe></div>

## 1c) Object Types

**Object Types** is the strongest way to efficiently optimize, although using this requires more experience. Essentially, some objects can be sufficient to maintain similar quality with far lower object counts. These optimized objects will depend on what you’re trying to do with the unoptimized objects as shown in[Creating Details](<https://discord.com/channels/414295025883545600/1233710767895740456/1233710767895740456>).  For example, you can get away with using the wood objects in the 1st and 9th tabs in the editor instead of making your own custom wood. In general, be aware that custom assets will always be more inefficient than using default objects, which includes things like creating custom curves instead of default curves.

With other object types that have both base and detail color channels, you can also make use of partial masking to make them part of a detail.

## 1d) Toggles

As much as creators can use toggles for LDM, toggles can also be used for optimizing by removing unnecessary objects that are offscreen. Castlemania does this with its branching paths where any path the player avoids gets toggled off. As shown here, removing those toggles makes the level difficult to render in the editor and in-game.

{{< youtube dhsYDtOrvw0 >}}

## Miscellaneous Methods

## Glow-related Optimization

In the context of glow objects, gradient trigger overlays are usually less laggy than scaled up glow. The reason for this is that the gradient barely adds glow to empty space rather than adding an active object count.

## Trigger-related Optimization

In the case of trigger usage for visual effects, there are 3 points worth noting for the current update: misusing shaders, particle objects, and link visible trigger.

## 1. Shaders 

Due to how shaders are rendered, they can create severe lag when activated. For example, Rage Quit’s split screen transition creates an unfortunate lag for lower-end devices. In contrast, Change of Scene had little to none of those issues. The real kicker here is that Rage Quit has half the object count of Change of Scene, which makes this lag all the more fascinating.

## 2. Particle Objects

Particle objects are also a recent 2.2 addition that is well known to cause lag, especially if you have attempted to create a black hole before. Oddly, increasing the particle amount doesn’t increase the active object count. However, it does create the same object density issue that increases the risk of lag.

## 3. Link Visible Trigger

While it’s true that camera culling can happen to extremely large objects after a certain scale, this trigger remedies that issue by forcing it to stay as an active object, even when it’s off-screen. However, remember how high active objects increases the risk of lag? You want to make sure that the Link Visible Trigger only targets those few important objects.

## Reducing Objects

This is a method which lets you reduce object counts without affecting the overall look of the deco. If applied properly, you can use half or even one-third of the prior objects, without impacting the visuals much at all.

1. Make two copies of the deco you want to optimize. Unlink all of the objects if necessary.

2. Using the “All” layer, remove all objects that don’t show up above others.

3. Disable Preview Mode and go through each layer. Use scaling and object types to reduce object counts for filled-in shapes.

Note that this works significantly better if you use a lot of Editor layers. This will help you stay organized and make the layering task less tedious.

Here is an example of this process.

{{< youtube NMwzuKoi3Nk >}}

                   ~~



## Credits
Created by @Selena and @Unknown
