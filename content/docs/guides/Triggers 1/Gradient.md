---
title: Gradient
weight: 320
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Tiny** (2-4 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- The gradient trigger lets you create gradients in a certain range. It also has four different blending modes.
- The layer which the gradient is rendered on can be changed via the 'disable' option and the gradient color, you have to change the color channels that the gradient is using.
- Vertex mode enables a mesh to occur between four exact points of the editor, which can generate a variety of effects.
- Vertex mode uses center group id's, which can be used to implement 2D meshes (as while the points move, it causes the gradient shape to change).

{{< /callout >}}

** **
# 1: Basic Mode

The Gradient trigger has two major settings: Edit Object and Special Edit.

The U (up), D (down), L (left), and R (right) boxes are used to limit where the gradient will be applied. The effect is applied on group centers, although this feature is made redundant by Vertex mode.

ID is for the ID of the gradient effect. There cannot be two gradient effects with the same id and you can also modify gradients within the same id.

Blending changes the way the gradient blends. *There are 4 blending modes: Normal, Additive, Multiply and Invert.*

You can change which layer the gradient is rendered - the gradient is always rendered above everything in the chosen layer.
'Disable' disables the gradient effect. You can rotate the gradient effect by rotating the trigger; this works with a rotate trigger too.

To change the gradient color, you have to change the color of the color channels that the gradient trigger uses. HSV and pulse don't work on gradient triggers.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1s-IDJuWTFygLRulgQwFMF_P5FlsjDDAN/preview?usp=drivesdk></iframe></div>

# 2: Vertex Mode

Vertex mode allows you to draw a mesh between 4 points in the editor. *Enabling it will change the U, D, L and R parameters to BL (bottom left), BR (bottom right), TL (top left) and, and TR (top right).*

These parameters use one-object groups, just like the center group on a Rotate trigger. This allows you to make 2D meshes, as moving the points changes the gradient's shape. If you want to make a triangle instead of a square, you can use the same group for two parameters, like TL and TR.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1V9RqjXyiZ6haSa0YUh-KnJH5NHLMRwDY/preview?usp=drivesdk></iframe></div>

Let's take an effect and see how it uses the gradient trigger.

<div><iframe src=https://drive.google.com/file/d/1Q05DFn9ybIrLeq-BOQZsmye9ExSwPRY-/preview?usp=drivesdk></iframe></div>

This effect is created by using a lot of vertex triggers to make trapezoids. Moving the individual points also moves the mesh. Furthermore, the mesh will stay connected because some of the gradients share the same groups.

The curves here are created by using the Area Move trigger to smoothly move the objects around.


## Return to the [Table of Contents](https://discord.com/channels/414295025883545600/1194067331836551278/1194067331836551278) Here

**Video:** https://youtu.be/jhP4Tt_OpA0?si=VUeBGlPy1806EiqA



## Credits
Created by @Madzz and @TheMilkCat
