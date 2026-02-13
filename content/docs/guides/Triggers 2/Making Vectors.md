---
title: Making Vectors
weight: 612
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Short** (9-11 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- Using vectors and mathematics, we can move points in more ways than what the game typically provides.
- Follow Triggers can be used to represent the values of vectors, but you can also use Item IDs if you need vectors for other uses.

{{< /callout >}}

** **
# 1: Vectors

In mathematics, a **vector** is defined by __a length and a direction__, but can be seen as an offset of position. A vector can also be expressed using X and Y as coordinates, where X is the horizontal offset and Y the vertical one. This is because a point is similar to a vector. If you take the origin point which has the coordinates (0, 0), you can think of any point as a translation or offset to that point from the origin.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1T-PU-6CZwtPHR-NAxG9KBnAFt3N7R-YP/preview?usp=drivesdk></iframe></div>

Vectors are also useful as they are the foundation of physics and graphic engines. Knowing how to do vector calculus In Geometry Dash will help if you plan on making one or both of these engines, and more. When it comes to graphics engines, making shapes just requires a [gradient](<https://discord.com/channels/414295025883545600/1194067331836551278/1194067331836551278>) trigger and 3-4 points.

You can represent points in Geometry Dash with a single object. For simplicity, we will label points with a single letter. As an example, we will use A for the output point.

Since points can move over time, the position of a point, also called its **position vector**, is __the vector that goes from the original position of the object to where it is currently__. For point A, we will denote a position vector A. Vectors can also go from a point to another point. If we want to make a vector that goes from a point A to a point B, we will write it AB. And we can add an arrow on the top as well in the formulas. Position vectors cover four branches of operations: sum, product, rotation and derivatives.

# 2: Vector Sums and Products

Adding and multiplying vectors in Geometry Dash is best done with the Follow trigger.The formulas for these describe the position of a certain point, which will be the output vector, depending on a set of other points. This means that your point will dynamically move with the others, no matter what kind of movement they are doing.

## Following Position Vectors

In order to follow the position of point A, you can use a follow trigger with A’s group as the follow group. In addition, you can multiply that vector A by the X and Y Mod values to change the vector’s values.

None

## Following Several Vectors

Now that you can follow a vector A, stacking follow triggers lets you follow all points at once, which adds the vectors together. In the example, point C follows the vector A + B, with two follow triggers corresponding to A and B’s groups. As stated earlier, you can change the values in a follow trigger to change the coefficient or how much A or B is multiplied by.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1D5y-NvJ2jNOBsXnDD-gPL4gKU1JE2cLN/preview?usp=drivesdk></iframe></div>

## Following Midpoints of Segments

Adding multiple vectors also lets you place a point at the midpoint of two other points, by getting the average value of their positions. 

1. We can refer to the midpoint as point I, placing an object in the middle of A and B.
- Place a follow trigger that makes point I follow point A with X and Y mods of 0.5.
- Repeat step 2 with point B.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1xReaBW09jin6QreiXji_lj1IBzSjI_-b/preview?usp=drivesdk></iframe></div>

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1UUC1NAsg9onxV2iH1JdEJwuBAXiqKYjE/preview?usp=drivesdk></iframe></div>

If you’re struggling to determine the midpoint, you can place I, A and B on the same spot before the triggers activate, since I will still be equidistant from both points.
## Following the Center of Mass
Averaging points like this doesn’t just work with two points. You can average out any number of points to get the center of mass. The formula for this is provided below, where pn is the weight of the point Pn and k is the sum of all weights.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1wvjYdNkmiQXaK6HidmaVmZOlSk1vLMnk/preview?usp=drivesdk></iframe></div>

As an example, let point A follow the center of 5 points where one of them is weighted twice as much as the others. This leaves us with k = 1 + 1 + 1 + 1 + 2 = 6.

To represent this in GD, we have 5 objects with follow triggers corresponding to each of their groups. These follow triggers will have 0.17 as their X and Y mods, with one of the follow triggers being twice that, or 0.33. These decimals translate to our example with point A, in the form of fractions. 0.17 is approximately ⅙, and 0.33 is ⅓.

In theory, the numbers ⅙ + ⅙ + ⅙ + ⅙ + ⅓ equal 1, which is the exact value we need for a weighted average like this. However, GD rounds numbers to the nearest hundredth which adds a slight bit of error in-game. . To fix this, we must subtract .01 from one of the follow triggers’ X and Y mods. This will keep A from drifting when all other points move.

None

## Following Vector AB

As of now, we have only been able to follow a position vector, but not vectors defined by two points. To know the coordinates of vector AB, we can subtract the coordinates of A from B. Subtracting these coordinates makes a new vector that starts at point A and ends at point B.

None

If we want to follow a vector AB in Geometry Dash, we can follow points A and B with X and Y mods of -1. We can also put a coefficient in front of our output vector, with the formula kAB = kB - kA.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1GuV3ljjRNAcpPnm1Yu13NCOAo0Z0MA0l/preview?usp=drivesdk></iframe></div>

When both A and B move the same way, the point following the vector AB doesn’t move. If you want a point to follow the points even when both move, you can add vector A to the formula from earlier.

None

In the follow trigger corresponding to vector B, we will use k as our mod, and point A will use 1 - k. Here is an example with k = 0.2, and 1 - k = 0.8.

None

## Dynamic Frames

With vectors and points, we can create what’s called a **frame**. In mathematics, a frame is defined as an origin C, and two basis vectors starting from the origin named CI and CJ respectively.

None

We can plot points with coordinates in that frame, and when moving the points C, I and J, the points plotted in the frame will move according to those coordinates. A property of their movement is that if the points form a quadrilateral, they will keep that shape regardless of the frame. This shape can change position, orientation, scale and can skew. This is useful when making 3D shapes, such as with the Gradient trigger.

Let's say we want to plot points using the coordinates X and Y. We will start from origin C, move X times the vector CI and Y times the vector CJ. The formula decomposed is the origin multiplied by the difference of 1, X, and Y, summed with xI and yJ.

None

To implement this in-game, we will use 3 follow triggers, one of which following point C with 1 - x - y as the mod, and the rest follow I and J with x and y as their coefficient respectively. The result should be point A with coordinates (6, -3) in the frame.

1. Place a follow trigger for point A that follows I. Enter 6 as the X and Y mods.
2. Place another follow trigger that follows J. Enter -3 as the X and Y mods.
3. In our formula, point C should be represented by 1 - x - y. This should give us -2. Place a follow trigger that follows point C. Enter -2 for the mods.
4. To get the system to work, place all points in the same spot. From here, you can freely move C, I and J and A will follow.

This process can be repeated as many times as necessary to make points for your frame. If you need further help, here is a desmos animation demonstrating what happens above. [Desmos Animation](<https://www.desmos.com/calculator/5du2xh0xi4>)

None

## Tips
### Teleport Points to One Spot
You may notice that these setups require all points to be in the same spot to function, but having many points in one spot isn't convenient to work with. We can teleport all points during playtesting to fix this.

1. Give a group to all points. Place another point that all objects will be teleported to.
2. Put an advanced follow trigger at the start of your level. Put group A in the Target group and group B in the target group. Stop the trigger after it activates.
3. Activate your follow triggers after the stop trigger has activated and move your points as you want.

None

### Keep Follow Triggers from picking up Movement
    
You’ll also notice that when you don’t want the setup to operate for a set time, the points within the frame will move regardless. If you activate the Silent option inside a move trigger, other triggers won't see that movement. This is useful if you want to instantly move certain points without worrying about follow triggers.

<div><iframe src=https://drive.google.com/file/d/1jbKyVtyqFiz118HS-0tjNRXHhkVuOxPB/preview?usp=drivesdk></iframe></div>

# 3: Derivatives

Vectors evolve over time, meaning they are a function of time. With any function, we can approximate its derivative. The **derivative** of a vector is __another vector that represents how much the original vector changes at a given time__. As an example, moving right creates a position vector that faces right. This means the derivative, or in this case velocity, is a vector pointing right. To calculate this we can use a formula involving a vector A at a certain instant t and moment Δt before t, all divided by Δt. Approximating this is more accurate the smaller Δt is.

None

To construct a derivative in-game, we need to have a point follow A with some delay, and have another point follow with 1 / Δt as the coefficient.

1. Place point B over point A. Use an advanced follow trigger to have B follow A. Put a delay of Δt in the trigger, with smaller numbers being best.
2. Place a point C that represents the derivative vector.
3. Place follow triggers that have C follow points B and A. Their coefficient should be 1 / Δt. Any number will work, but it’s up to you which is best. This is covered further in section [link] of this guide.

None

Having 2 derivatives, for example deriving the derivative of C, you will get a derivative of A, representing that points’ acceleration.

## Other Calculus

If you need vectors to perform something outside geometry, such as calculus, then there are methods much better than moving objects. You can use item IDs to represent vectors and actually use values coming from a derivative, since a vector is characterized with 2 coordinates. With Item Edit triggers, you can use its many calculation options to get the results you want.





## Credits
Created by @NotAModerator and @tanhR
