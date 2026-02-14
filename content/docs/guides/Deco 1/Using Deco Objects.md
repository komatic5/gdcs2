---
title: Using Deco Objects
weight: 501
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Short** (9-11 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- All decoration is made with shapes, and all shapes are made from objects. You can use a variety of methods to create your own custom shapes and curves, which usually comes down to choosing objects and dissecting them to make shapes.
- Shapes are also colored, which can be done by setting new color channels for your objects. You can also use Blending and Opacity to use colors in more interesting ways.

{{< /callout >}}

** **
# 1: Choosing Objects By Shape

As a new decorator, you might wonder how to choose objects. Should you look at an object’s texture? Its size? Color? While those are good to consider, they’re largely unimportant.

> The most important aspect of any object is its **shape**.

If you can get a shape to look accurate, you can make an object people recognize. If you mess up an object’s shape, nobody will know what it is.

If color or texture were the primary factor, then the Apple logo wouldn’t be recognizable as an apple. If detail or complexity were key, then you wouldn’t be able to see forests, but a bunch of trees. And if shapes didn’t communicate an object’s function, all of the objects you use daily would be completely unintuitive to use.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1sysEc9YJymgVARicANf842KfAE4A43pX/preview?usp=drivesdk></iframe></div>

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1i2aomyMdr7FLMgwhSs0DtxBt3P365ly2/preview?usp=drivesdk></iframe></div>

Shapes help us recognize objects as useful, harmful, or dangerous; you can tell that a button is meant to be poked, while a knife is not. You can tell that a cube should go in a square hole because their shapes match, and you can recognize a cube instantly because it’s one of the simplest shapes out there. All objects are made of simple shapes, so if you can recognize the shapes that make up an object, you can create anything in general.

So to answer the question of “How do I choose proper objects?”: you choose objects by their shape. If you imagine objects as strictly their shapes, decoration becomes a puzzle where you put the right shapes together to create something. Not only that, but your hundreds of puzzle pieces can be rotated, warped, and recolored to fit your vision of the final piece. There are also tons of ways to fill in the puzzle, so you can experiment and mess around as much as you wish. This is the most fundamental part of decoration, and it’s the core of what you’ll be doing from here on.

## Choosing Basic Shapes

As you should recall from the Detail Objects guide, objects come in many different forms. There are Geometric shapes which are angular and rigid, and Organic shapes that are fluid and curvy. In time you’ll learn to use these shapes wherever you want in your deco, but for now ignore that and focus on just learning how to use them.

Start with the most basic shape an object can take on, and choose an object which makes that shape. An apple’s most basic shape is a kind of circle; a sign should come from a rectangle; and a spike from a triangle. These basic shapes can be found everywhere in the editor, so you should have an easy time finding them.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1TjSFBUnZ-Cck5-OnRADshcFa47jtw_dO/preview?usp=drivesdk></iframe></div>

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1FzcJ_lWe1BxKcaRIkzhtpkVevp19yK9s/preview?usp=drivesdk></iframe></div>

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/19UU1-jmQGf1U4NyscTJPz1dgSkYYxZbO/preview?usp=drivesdk></iframe></div>

Some objects will have more complex shapes that require some more fiddling to create. An apple isn’t just a circle; it has two “ovals” on the top, and usually becomes more of a triangle or trapezoid at the bottom. You can use the transformations in the Edit tab - especially scaling and warping - to make these more complex shapes. For a trapezoid you could use 3D lines, and for ovals you could stretch out circles.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1MM-S9NYQTaSmdoBcUrgMf3p-1VsWLSfb/preview?usp=drivesdk></iframe></div>

While it is difficult to do at first, you should practice trying to simplify objects to their most basic shapes. Details are easy to focus on (especially in this community where people ALWAYS focus on them), but you can’t make complex details before you know how to make simple shapes. Once you're comfortable finding the basic shapes of an object, then combining and modifying them to make something similar to it, you’re ready for the next topic in this guide.

# 2: Making Custom Shapes

As you can probably tell from trying to practice the last section, many objects aren’t as simple as “finding a basic shape” because their basic shape simply doesn’t exist in the editor as an easily usable form. This is where you have to make your own custom shapes to get by.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1kqKsf3D8sulpB8jeYugxFFJgQeg_E8Vi/preview?usp=drivesdk></iframe></div>

Recall that shapes can usually be classified as geometric or organic. Geometric shapes are usually some combination of polygons; triangles, squares, octagons, and so on. Organic shapes usually require custom curves to be created and filled in. Here you will learn how to create both.

## Making Custom Polygons

There are many ways to create polygons, which all come from how you can view them. You could view every polygon as a combination of triangles or rectangles (as they are the simplest geometric shapes), or as a collection of corners which are connected by lines.

To this extent, if a polygon isn’t already in the editor, you could make it using triangles, rectangles, and other simpler polygons:

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1pyBPSdJtA33WasKXbuUlhv1H6paIyfIY/preview?usp=drivesdk></iframe></div>

Alternatively, you could place down a set of points and connect them using lines or glow, which is better for outlining shapes:

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1oIHl5QZD5ofi3tQvzWg378GxpAEprvyP/preview?usp=drivesdk></iframe></div>

In either case, you’ll be able to make your complex polygons very quickly with a bit of practice.

> Pro tip: Try to remove any visual bugs you encounter. For example, fill in the corners of your shapes so they don’t look amateurish. You can find these corner pieces in the second tab, along with the other outline objects. (Image of the corner objects on some block outlines)

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/15FEzm-XP_aOahu6cTp3MEEcLW-NL8VAy/preview?usp=drivesdk></iframe></div>

## Making Custom Curves

Custom curves are really just a collection of lines or rectangles stacked next to each other. Many techniques for making them require you to use a lot of these objects.

For example, you could make a circle by rotating lines around a center point. Be aware of where each object’s rotation center is, as it’ll make certain objects harder to make custom circles with:

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1d8jINGALTCRvf9SacJ8vROzYzq0jiKRs/preview?usp=drivesdk></iframe></div>

Or, you could make a parabolic curve by combining a bunch of straight lines:

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/15RnUY0UBEKMd2TB-WDCfh8oxQlOOFfRu/preview?usp=drivesdk></iframe></div>

Using 2.2’s new warping features, you can stretch out the pre-made curves to make larger circles more efficiently:

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1cYv3788ydSa1ds3zAuywGHPhOg-5z9_a/preview?usp=drivesdk></iframe></div>

And finally, you could freehand your curves if you’re patient and want a lot of control:

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1Og7HkPUDKp-nu1mNZww2AJ0HfEve15sd/preview?usp=drivesdk></iframe></div>

Once again, practice makes perfect here. This is especially true of the last two methods, as they can be quite time-consuming.

As a final thing, you can also combine curves to create custom ones with more complexity. Feel free to mix and match different parts of curves as you wish, or to scale, warp, and transform them as necessary:

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1T1HE_O680fU_84sEYnAjhvSQnR0VDR6t/preview?usp=drivesdk></iframe></div>

## Combining Geometric & Organic Shapes

You don’t need your shapes to be entirely geometric or entirely organic. Combining the two together can make your decoration far more interesting. You’ll learn a lot more about how this works in future guides, but for now take these examples as inspiration - try to dissect them and see how their shapes work for yourself.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/15iGJBZPw5tto6tCyp1gkCZuE8n2hROfF/preview?usp=drivesdk></iframe></div>

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1FrC3MOJA40QHaTfkwqUzqeGZ71Kwa10W/preview?usp=drivesdk></iframe></div>

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1BAxvjxnn7Boo5fjMgEx7UZ_tBC-gNuW3/preview?usp=drivesdk></iframe></div>

# 3: Setting Object Colors

While shapes are crucial to recognizing objects, colors are also very important as well. I’m sure you can recognize something like the **golden** arches of McDonalds, the **blue** tint of the sky, or the **green** of grass. While you can recognize things with different colors (because of their shapes!) you can tell that something is off; for example, green fire and red water indicate that something has been tampered with to produce that color.

In Geometry Dash, object colors are the same. As you can expect, you start by dissecting the simplest aspects of a shape’s color: how bright it is, the strength of the color, and its hue. You can then emulate these colors in GD by setting a color channel to have that color, then assigning it to your shape. Repeat this process with every shape in your decoration and you will have yourself a good set of colors.

I recommend you learn to choose colors by hand instead of strictly using hex codes or HSV numbers; specific numerical colors will not help you learn as much as eyeballing things and getting a good feel for what works.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1vZWkmHGgrZkQ98CqxJ3qgpGJ7s-Dvg2g/preview?usp=drivesdk></iframe></div>

# 4: Layering Objects & Texturing

This is the most complex section of the guide for a reason. Once you add Z layers and the ability to stack objects, decoration becomes far more convoluted to learn, and I do not recommend practicing this without a solid grasp on the prior skills.

That aside, stacking objects on each other is most useful when you want to add a texture to an object. Texture is the least useful element of any object; you don’t look for the texture of fur to determine if a tiger is charging toward you. (As you should know by now, you’d see the shape and probably run away).

The process for making a texture should be familiar by now; identify the material of the object, then stack objects to emulate that texture. However, this is only the most basic explanation and texture requires a lot of lighting knowledge to fully understand it. You will learn that eventually; for now, just be patient and focus on how you use objects.

There are two main ways to stack objects; using blending and using opacity. Objects generally will not show underneath other objects without one of these being present.

## Stacking with Blending

Blending (or Additive Blending) combines colors together when they’re placed on top of each other. On a technical level it adds the colors together, so blending on black is invisible and blending objects don’t show up on white.

Stacking blending objects usually limits you to basic shapes or ones you can create without overlapping objects. Otherwise you risk your objects looking very messy, as blending creates new shapes that are much harder to control.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1k1cITEoQi-7PRj1B1CPmND6CawCMhqT2/preview?usp=drivesdk></iframe></div>

However, blending also lets you experiment with colors more. You can use Hue Shifting to create gradients that change hue as they get brighter, which looks more dynamic than keeping everything the same color.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/16KOoBdkDs3uneptCfIfDRMQB6mKaO17e/preview?usp=drivesdk></iframe></div>

Similarly you can squeeze more hues out of objects with less effort; instead of using every single hue between red and purple, for example, you can create a simple gradient and let that do the work for you.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1NCpeBACJ4NdD5SOBTpYaoY6AWCqVSOIf/preview?usp=drivesdk></iframe></div>

When using blending objects on top of non-blending objects, make sure the non-blending objects are much brighter. Failure to do so will make your decoration foggy which can be an undesirable effect.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1uIYX3mpoQNzDHi02hqdV3E1JuyWZGkU8/preview?usp=drivesdk></iframe></div>

## Stacking with Opacity

Opacity makes objects transparent or see-through. This is useful when you want to lower the visibility of an object, such as a gradient or something with blending colors. It is also useful with objects that have complex shapes, like animated objects and some objects from the particle tab.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1guo7zHxbA25uaT4eUk-in6jmZ4SAgDUS/preview?usp=drivesdk></iframe></div>

Opacity lets you layer an object over another to make textures without the brightening effect of blending. When used with Partial Masks (where you make an object’s base/detail color invisible), you can create all sorts of interesting shapes.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1yeP3fcyGnpS2noCXXYmqyQw9x4_lUAmF/preview?usp=drivesdk></iframe></div>

As with blending, make sure your stacked objects don’t overpower your normal ones. This will make your deco messy and incomprehensible.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1Ke2rrlOb4fDNxMxJVvWOTqZP94lUqhUD/preview?usp=drivesdk></iframe></div>

You can also combine opacity with blending, of course. This makes your blending objects even less visible, just like if you darken them.

Finally, note that you can use low opacity copies of objects to create blurred shapes, which is quite time-efficient.

<div><iframe src=https://drive.google.com/file/d/1Q2kOwjN0RCfjhbjJkz8X1DqDpXek78Ih/preview?usp=drivesdk></iframe></div>


## Return To The [Table of Contents](https://discord.com/channels/414295025883545600/1233650406089949254/1233650406089949254) here

**Video:** https://youtu.be/3ofZI82lKQ8?si=a5bXL1ilq24c9C_N



## Credits
Created by @koma5
