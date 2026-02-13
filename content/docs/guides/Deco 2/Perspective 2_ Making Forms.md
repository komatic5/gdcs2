---
title: Perspective 2 (Making Forms)
weight: 821
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Short** (5-7 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- We learned how to create stencils for our 3D shapes, and the ways you can easily create ellipses.
- From those stencils, we can make basic forms.
- We can merge basic forms together to form more complex shapes and decorate them as needed.

{{< /callout >}}

** **

# 1: Recap on Lines

Remember that straight lines, C curves, and S curves are used to make shapes. This is important when making ***forms*** because __forms are just shapes put into a 3D space__.

However, you’ll need more precise ways to make planes when working in 3D. As such, here are some ways to make precise lines and curves.
## Lines

If you want a line with a specific length regardless of the angle, you can use a GD feature called **Group Parent** to easily rotate lines. When you enable Group Parent on one object and then select multiple objects, that object becomes the center point for rotation and scaling.

1. Place two small objects to act as the start and end points for the line. Select **one** of them and enable “Group Parent” in the Edit Group interface.
 - I’ll refer to the point with Group Parent enabled as the **Pivot Point** (PP), and the other point as the **Non-Pivot Point** (NPP).
2. Duplicate the Non-Pivot Point, and select the Pivot Point. Rotate both around the Pivot until they’re perfectly horizontal.
3. Use line objects to make a line between both points.
4. Rotate the line around the Pivot until its other end touches the NPP at the right angle.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1uY3TReLDC9V8tnIKAY-iTHr9WcYFzcwF/preview?usp=drivesdk></iframe></div>

Alternative method: (convenient for Steam users)

1. Follow the same instructions as Step 1 of the prior method.
2. Make your line first. Attach one end of the line to the Pivot Point and rotate it until the other end crosses the NPP.
3. Delete the parts of the line which extend past the NPP.
4. Use the Free Move tool to extend the line until its length is precise. You can zoom the camera in for better accuracy.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1C7v6Co9U1OexSYl9SHylcEfzsyE-3h2e/preview?usp=drivesdk></iframe></div>

## Ellipses

Ellipses are a mess in-game, no matter which update you’re playing on. Even in Geometry Dash 2.2, where you can create a circle and transform the objects to be wider, you won’t get an ellipse with consistent line thickness without doing more work.

The simplest way to make an optimized ellipse is by using an ellipse helper. There are two types you can make; one which uses Follow and Rotate triggers, along with movement tracing, and another which uses the circular saw objects. Both ellipse helpers are available using the ID ‘96013135’. 

There is also a special tool catered to this very process called the ‘Circle Tool’, which can change the angle, amount of compression, and the amount of units each object steps. [Circle Tool](https://matcool.github.io/mods)

Once you create your ellipse guidelines using one of these methods, you can simply freehand the ellipse using objects, then remove the ellipse helper. You’ll have to use scaling and rotation extensively for this to work.

Since ellipses have major and minor axes, you should also get used to constructing ellipses by defining their major and minor axes *first*.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1_aBIXuRv00xaG15RRYbt-hSr-6yHbzJO/preview?usp=drivesdk></iframe></div>

# 2: Basic Forms

With your guide/stencil set in place, we can move on to making basic forms. These are ones you’ll use extensively when working in perspective.

## Rectangular Prisms

To make a rectangular prism, start by deciding how many planes are visible from the viewing angle of the camera. If one plane is visible, build a rectangle/parallelogram.

If two or more planes are visible, make a line for the edge closest to the viewer. Then, construct two points somewhere else in your workspace which will serve as vanishing points. Construct lines which extend from the points on your prism’s edge to the vanishing points, then create more lines which define the other corners of the prism. Finally, connect everything together.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1HJ2bPCaftfn6I5WCJJVzrsC3r4-rv8me/preview?usp=drivesdk></iframe></div>

Rectangular prisms are also commonly made using ***Orthographic Perspective***. This is __where depth exists, but parallel lines don’t converge to vanishing points__. The game’s default 3DL objects are an example of orthographic perspective.

Simply create a prism, then make a copy and offset it a bit. Then, connect the closest corners together using lines that have the same angle.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1q7R0-QOILwvAgG7ujdv8SJmO0ccqx784/preview?usp=drivesdk></iframe></div>

## Spheres

Spheres are one of the simpler forms you can make. Simply construct a circle, then construct two ellipses. One ellipse will divide the sphere into a top hemisphere and a bottom hemisphere, like the Equator. The other will divide it into a right and left hemisphere.

To ensure that your construction is correct, place a point at the center of the circle. Then, draw lines extending outwards and upwards to define the major and minor axes of both ellipses. This is largely to get used to making accurate ellipses, as it’s important for some other constructions later.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/16Mt_7vnnGard9ISBcK4kLuayUkjNxwra/preview?usp=drivesdk></iframe></div>

## Cylinders

Cylinders combine the practices from rectangular prisms and spheres. Start by drawing two lines – in perspective, of course – to determine the top and bottom of the cylinder. 

Next, construct ellipses at the front and back of the cylinder. Remember that ellipses are circles being viewed in perspective, so their width will change depending on the camera’s viewpoint. 
This is something that requires practice to gain intuition for where exactly each ellipse will be placed.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1vmR8i-39jWtvE8wWqu0I2Z-fJJEEHt-w/preview?usp=drivesdk></iframe></div>

## Cones

Cones are fairly simple. Create an ellipse in perspective by marking the major and minor axes. Then construct a line starting at the ellipse’s center which extends upwards to whatever height you desire. Connect the edges of the ellipse to the top of this line and you have a cone.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1fsKa0_sC84DdzKG6fXZ-2jZApnoVuNUM/preview?usp=drivesdk></iframe></div>

# 3: Combining Forms

These basic forms are used to make more complex forms by connecting them together and deleting any hidden edges from the final draft. Adding forms together is as easy as making two simple forms, then putting one of their planes next to the other form’s plane and erasing the lines between them.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/12ueVLUjbPazLHXeVU_RkYeAoZQCxPP2k/preview?usp=drivesdk></iframe></div>

Subtracting forms from each other requires you to make the larger form, then make the smaller form *inside it* and erase the lines where they intersect. In some cases this is known as negation.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1fQdeY_7TNoL1qYRUsN1qi0OEo8mNps1V/preview?usp=drivesdk></iframe></div>

As you can imagine from the prior Decoration guides, the same process applies when working with forms as it does with 2D shapes and objects. Choose the forms which will most efficiently achieve your decoration ideas. And when studying forms, be sure to dissect them into their most basic versions.

Here are some examples from Chunlv1 which demonstrate this process.

<div><iframe src=https://drive.google.com/file/d/1YI2Ui_-5M-nXWX8e9m2ZX_If6ahBYhLW/preview?usp=drivesdk></iframe></div>


## Sources

- [Proko: Structure Basics](<https://youtu.be/3uEtdDvK6Xo>)

Changed the channel name: Perspective 2: Making Forms



## Credits
Created by @NotAModerator and @koma5
