---
title: Perspective 3 (Using Planes)
weight: 822
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Medium** (11-13 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- Planes are needed to divide or multiply forms; they are 2D shapes that are located in a 3D space.
- Mirroring planes in perspective helps you with creating symmetry in your object’s forms.
- For mirroring curves, there are 4 techniques to comb over, most of which rely upon transfer points; depending on your vision, some techniques will be more valid than another.

{{< /callout >}}

** **
At this point, you should be comfortable with basic perspective uses. However, once you make something more complex than just basic shapes, it becomes crucial to know how to speed up your workflow. This is where perspective tools come into play. All of these tools are useful for a more advanced understanding of perspective, like the type used to make complex objects shown in this image from Scott Robertson. Even if you don’t wish to make 3D stuff in the future, you can still benefit from thinking of shapes in a more advanced way.

None

For all of these operations, please refer back to the [Creating Decoration guide](<https://discord.com/channels/414295025883545600/1245491810470465536/1245491810470465536>) and use multiple editor layers to organize yourself and keep track of what you’re doing. Otherwise, this can get very messy. Additionally, if you’re struggling with executing the later techniques here, go back and practice on the earlier techniques more. This is crucial because they all build on top of each other.

This guide will assume that you’re working with 2-point perspective, as it makes all of these operations much easier to learn.

# 1: Basic Plane Operations

A **plane** is a __flat, 2D rectangle positioned in a 3D space__. Planes are useful for making complex forms because you can create any shape inside a plane, position the plane in 3D space, then create that shape in perspective. It's an incredibly useful tactic which is used to draw all sorts of complex objects, from cars and airplanes to bridges and buildings. You’ll learn more about this process in the next few guides,  but for now let’s start with manipulating rectangular planes.

Cutting forms into pieces is an important operation that’ll save you a lot of time when making constructions. Similarly, multiplying the same plane multiple times in perspective is very useful. Both of these operations work by cutting planes apart.

## Dividing & Multiplying Planes
These are the most basic plane operations and are crucial for understanding the ones afterwards.

To divide a rectangle into two, do the following:

1. Make two lines which connect the diagonal corners of the rectangle. This will mark the center point of the rectangle.
2. Create a new line inside the plane which goes through the center point and divides the rectangle into two new ones, both in perspective. This line can be horizontal or vertical, depending on what you need.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1mzOdSmQuf38A4wqoOQccWmWSmLdKCC6y/preview?usp=drivesdk></iframe></div>

To multiply a rectangle, do the following:

1. Make two lines which connect the diagonal corners of the rectangle. This will mark the center point of the rectangle.
2. Extend the rectangle’s lines to the vanishing point. Similarly, make a line which extends from the center point to the vanishing point.
3. Make a line which extends from the corner of the rectangle, through where the edge of the rectangle intersects with the center line. Extend this line until it goes past the other rectangle line (where it’s extended to the VP). Repeat this with the other corner.
4. Make a line connecting the points formed by these new lines.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1ck5-MXn6LTa10_cVZXrvEEUTSGfbjIDz/preview?usp=drivesdk></iframe></div>

## Dividing Planes into Odd-Numbered Segments
Multiplying planes an odd number of times is pretty easy; you can just repeat the same multiplication technique multiple times. However, dividing a plane into odd-numbered segments can be much trickier. This technique helps with that process.

1. Make two lines which start at the VP opposite the one the plane points towards, and end on a horizontal line somewhere below the plane. Mark the points where these lines intersect.
2. Place down multiple points on the line — use Align X as necessary to space the points out equally.
3. Make lines which connect from the same VP through the points you just created.
4. Create points on the original plane which mark where the lines you just created intersect with it. Extend these points upwards to divide your plane into multiple parts.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1Rp9RaHDxBaHyfpr98WY07-YejJZ0nygT/preview?usp=drivesdk></iframe></div>

# 2: Mirroring Planes

Mirroring planes is an operation with a lot of uses. If you’re trying to make something symmetrical in perspective, it is crucial to use mirroring. Furthermore, the techniques for mirroring objects are very versatile, allowing you to mirror things in basically any way you can think of.

## Mirroring Planes across a Parallel Line in the Same Plane

1. Draw your rectangle, along with the mirror plane which you’ll be using. Follow step 1 of dividing a rectangle and create the diagonal lines.
2. Extend a line from the center of your rectangle to the midpoint plane.
3. Mirror the furthest lines from the mirror plane by using Step 3 of the rectangle multiplication technique. Here, the center line in question is simply where the center line intersects with the mirror plane.
4. Mirror the closest lines by using the multiplication technique. Connect all the lines accordingly.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1e2Wn8YDVbuLx_AGo-1B1ZxNCjxmiL0_k/preview?usp=drivesdk></iframe></div>

This works vertically as well, as you can expect. Think of that scenario in the same way as rotating the original constructions shown in the video.

## Mirroring Planes across an Offset Plane

Here, the plane you’re mirroring across is parallel to your rectangle, instead of being on the same height as it.

1. Set up your rectangle and place your mirror plane below it. Use steps 1-3 of the multiplication technique to mirror the first line in the front.
2. Use your perspective grid to copy the rest of the lines accordingly. You can copy a perspective grid from the ID `97223198` for now, as they’ll be covered in more detail in the next guide.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1IC5RA1V4oKa946A1y9Fs8jdNAofEAXcU/preview?usp=drivesdk></iframe></div>

## Mirroring Planes Tilted on One Axis

Here, the mirror plane is tilted on one axis. This makes the construction a bit trickier but it is still doable.

1. Create your tilted rectangle and your mirror plane. I recommend you to copy the perspective grid from the given ID to help position both planes in space accurately.
2. Extend the tilted rectangle’s line until it intersects with the mirror plane. Mark this point as Point A. Mark the furthest point from A on your rectangle as Point B.
3. Create a rectangle that shares a corner with B (with the help of your perspective grid), and use the multiplication technique to copy B across the mirror plane. We’ll call this new, mirrored point C.
4. Draw a new line from A to the new point C. This copies the angle of your tilted plane in perspective. Then, finish the drawing by using your perspective grid to determine where the other points will lie, and connect them accordingly.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1RBbsT3ZzT64-piNY_0jLOXMY_whA2xji/preview?usp=drivesdk></iframe></div>

## Mirroring Planes Tilted on Two Axes

Here your mirror plane is tilted at an angle, but your rectangle is also rotated on purpose as well. Using this you can create things which are physically impossible in real life. This is because a plane is defined by using three points in space, so the final point must also sit on that plane; otherwise, you can get weird shapes which are impossible in real life. (You’ll understand this best if you take a math course on 3D geometry, such as Calculus III).

1. Create your mirror plane, and two parallel tilted planes in perspective by using the same plane construction as in the prior section. Then, connect the points of those planes together to make a tilted, rotated plane. Notice how none of the points match in depth & width, and only two sets of them match height-wise.
2. Take the topmost point and use the rectangle multiplication technique to mirror it across your mirror plane. (This is why making both tilted planes beforehand is so useful.)
3. Extend the mirror plane and the front edge of your rectangle until they intersect. Then, connect this intersection point with the mirrored topmost corner. Use your perspective grid to determine exactly how long the front line will be, and draw it accordingly.
4. Extend your rectangle’s bottom line (where it touches the ground) until it intersects with the mirror plane. Then, connect this second intersection point with the mirrored bottom corner. Extend this line outwards until it’s long enough, once again using the perspective grid to help you.
5. Repeat Step 4 with the top line of your rectangle, mirroring it across to the other side. Then, connect the open edges and you should have mirrored your tilted, rotated rectangle.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1HqMYVjLKExteMG8v-J-KcbdOwzPJQtyN/preview?usp=drivesdk></iframe></div>

# 3: Mirroring Curves

The final discussion for this guide is how to mirror curves. This is the final major thing you’d need to understand, and is incredibly useful for making the most complex shapes. You may be able to get away with copy-pasting a curve and using the :Flip: and :2Point2: Warp options to make it in perspective (although you’d have to freehand the lines again so they keep the same thickness), but it’s important to understand WHAT makes a construction like this work as it’s the basis for more advanced perspective in the next guide.

## Basics of Mirroring Curves (Main Techniques)

There are four techniques you can use to mirror a curve in perspective. These techniques are used to transfer points from inside one plane to another. Assuming you’ve built your curve inside of that plane, you can then freehand the new curve using these points.

To start, define the plane for your 2D curve. Multiply this plane using the rectangle multiplication technique.

- **Technique 1:** Draw a V which starts at a common point where both planes touch, and ends in the corner of each plane. Mark where this V crosses your curve, and draw a horizontal line from that point to the other side of the V. This transfers a point accordingly.
- **Technique 2:** Use the center line that was created from the original rectangle multiplication. Make a V with your common point on both planes, and transfer the point where the V intersects with your curve.
- **Technique 3:** Choose a point on your curve to mirror. Place a diagonal line which goes through this point and through the bottom of your center line (where both planes touch). Extend this line so it touches the edge of your plane, and make a horizontal line across to the other plane.
- Then, draw a new line connecting the bottom of your center line to the other edge of your horizontal line. Draw another horizontal line which goes through the point you wish to mirror, until it intersects with this new diagonal line. You have transferred the point now.
- **Technique 4:** Choose which point you’re going to mirror. Draw a vertical line and a horizontal line through it to define a rectangle (so your point is now a corner of the rectangle). Then, duplicate this rectangle so you transfer the point accordingly.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1WOTU4L9bR7Y3ioq1DoffAmU5_n2gfNIl/preview?usp=drivesdk></iframe></div>

Any of these techniques can be mixed and matched to transfer points across planes. I recommend you choose the techniques which help you efficiently copy points without using too much effort for that scenario. You don’t need to use every technique here, but it’s useful to know all of them to use as necessary.

## Mirroring Curves Tilted on One Axis
This lets you mirror curves when they’re placed on tilted planes, just like the types of planes you should've learned to mirror earlier.

1. Define your tilted surface and draw a curve on it. The curves in the example connect to the corners, but that’s not necessary; what matters is that your curve fits snugly inside the plane.
2. Use the plane mirroring technique to mirror your tilted plane.
3. Draw a diagonal line through your original plane so it intersects with the curve. Repeat this on your mirrored plane, then draw a line from this intersection which is parallel to your perspective grid. This gives you three points to draw your curve with.
4. Draw a vertical line from the centerline of your tilted plane upwards to the curve. Transfer this to your mirrored plane. Then, repeat this with a horizontal line on your tilted plane.
5. You should now have enough points to freehand the mirrored curve fairly well.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1CLBRCIXlTktpdw_UkK-4Kqh56-9AoRks/preview?usp=drivesdk></iframe></div>

## Mirroring 3D Curves
A 3D curve/2-Curve is created by making a 2D curve with a horizontal plane, a second 2D curve with a vertical plane, and extending essential points of these curves outwards until they intersect. You can then create a new curve this way, which is useful for very complex forms like those you’ll see in [Perspective 5](<https://discord.com/channels/414295025883545600/1245810131267227769/1245810131267227769>).

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1GLYsIFB8NHrIh1gu9eoX2YpWrEGCOixa/preview?usp=drivesdk></iframe></div>

Once you’ve built a 3D curve, follow these instructions to mirror it across a plane.
1. Mirror the starting point of your curve by creating a rectangle between the start of your 3D curve, your horizontal curve, and your vertical curve. Duplicate this rectangle to mirror this point.
2. Repeat this process for the other points on the curve. I recommend mirroring more points when you start out, so you can be more confident in the construction.
3. Connect the points together and make your mirrored curve. Then, use the bottom corners of your mirrored rectangles to mirror the horizontal curve as well.

<div><iframe src=https://drive.google.com/file/d/1ZT2B9h_UPrCX9Z3aVy4BUDgIU-cuGLNc/preview?usp=drivesdk></iframe></div>


## Sources
- Scott Robertson: How to Draw, Chapters 3 & 5



## Credits
Created by @Selena and @koma5
