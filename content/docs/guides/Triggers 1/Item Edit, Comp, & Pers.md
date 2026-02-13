---
title: Item Edit, Comp, & Pers
weight: 347
draft: true
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Short** (4-6 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- Item Edit lets you form simple or complex equations using two Item ID values and store the result.
- Item Comp compares two Item ID values and activates groups based on the result.
- Item Pers gives Item IDs the ability to remain after the player has died.

{{< /callout >}}

** **
# 1: Item Edit

The Item Edit trigger lets you make simple equations using the values stored in Item IDs.

To start, you need at least one existing Item ID. Ideally, these IDs should already be modified by a Pickup trigger so its value is not zero.

None

ItemID1 & ItemID2 are the IDs containing the values you want to use in your equation. The Target ItemID is the ID that stores the result of the equation.

The checkboxes correspond to each Item ID’s type:
- Item - A normal item counter like that used in the Pickup trigger.
- Timer - A timer item counter. Place a Counter object, set its Item ID, and enable the “Time Counter” checkbox. You can then use this with the Time triggers.
- Points - A point item counter. In the Counter object, use the “Points” checkbox; this works with the Points mechanic in Platformer Mode.
- Time - The amount of time you’ve taken on your current attempt. Use the “MainTime” checkbox in the Counter object.
- Attempts (Att) - The amount of attempts you’ve taken so far. Use the “Attempts” checkbox in the Counter object.

Once your IDs are set up, you’ll get an equation in the box.

None

Use the first three green buttons to manipulate the equation. The first button modifies how the new values affect the Target ID, the second modifies the operation between ID1 and ID2, and the third chooses to either multiply or divide by the value in the “Mod” slider.

The 4th and 5th options choose between absolute value or negative value.

None

- Equals (=) - Equals sign; there can be only one in the equation.
- Addition (+) - Adds the two Item IDs.
- Subtraction (-) - Subtracts the first Item ID by the second Item ID.
- Multiplication (•) - Multiplies the two Item IDs.
- Division (/) - Divides the first Item ID by the second.
- Absolute value (A) - Makes the equation result always positive.
- Negative value (N) - Makes the equation result always negative.

> Note: Pay attention to the order of operations by looking at the parenthesis in your equation. Some operations listed above will always occur before or after other operations.

You can set the Target ID to be an Item ID, Timer value, or points.

None

The “NA” options allow for rounding:
- Round (RND) - Rounds numbers to the nearest integer. `0.4` rounds to `0`, while `0.5` goes to `1`.
- Floor (FLR) - Rounds numbers to the nearest *lesser* integer. `0.9` rounds to `0`.
- Ceiling (CEI) - Rounds numbers to the nearest *greater* integer. `0.1` rounds to `1`.

> Note: Be careful when taking the floor or ceiling of negative numbers, as they may not do what you would expect. For example, the floor of `2.5` is `2`, but the floor of `-2.5` is `-3` because `-3` is less than `-2.5`.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1cr-E24ITXEyuTeZ15pJ5wzc1QO9klHyR/preview?usp=drivesdk></iframe></div>

Item Edit also allows you to do complex algorithms like the Fibonacci Sequence and Recursion.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1KAPYPFq3-iCQp262z3OZK6SuC4UUvog-/preview?usp=drivesdk></iframe></div>

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1UFkPqKdwt-OYbQb9oLDMrGORxz20PpRL/preview?usp=drivesdk></iframe></div>

# 2: Item Compare (Item Comp)

The Item Comp trigger compares the values of two Item IDs and activates group IDs depending on the outcome.

*NOTE: Item Comp ONLY works as a Spawn trigger, not a Toggle trigger.*

The options in this trigger are very similar to Item Edit; the values from two Item IDs are used in an equation and the outcome is saved in another Item ID.
- TrueID - the ID that activates if the comparison is true.
- FalseID - the ID that activates if the comparison is false.
- Tol - the allowed margin of error for the True and False ID conditions.

None

The modification options and ID types are the same as well, but the differences come in the operations it lets you perform. These operations are **relational** and __compare values instead of manipulating them__:
- Equals (==) - I1 must equal I2 in value.
- Less than (<) - I1 must be less than I2.
- Less than or equal to (<=) - I1 must be less than or equal to I2.
- Greater than (>) - I1 must be greater than I2.
- Greater than or equal to (>=) - I1 must be greater than or equal to I2.
- Not equals (!=) - I1 must not equal I2.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1FKS5-D9AIZh3eB5AhJahbYtXEJXXtZUT/preview?usp=drivesdk></iframe></div>

# 3: Persistent Item (Item Pers)

The Item Pers trigger lets Item ID values remain the same after the player dies. This basically acts as a replacement for the Attempt-Based Data guides from 2.1.

None

The checkboxes provide options for the Item ID:
- Timer - select if the Item ID is a timer item counter.
- Persistent - sets the Item ID as “persistent” to work after the player dies.
- Target All - targets every persistent item at once.
- Reset - reset the Item ID’s value.

<div><iframe src=https://drive.google.com/file/d/1jvv4hqmjd0Y5A-_lx7aCAVgnU364kFyL/preview?usp=drivesdk></iframe></div>



**Video: **https://youtu.be/BT8PyW4iG0s?si=-qyr8apR7O4HARIP



## Credits
Created by @Vexilo and @koma5
