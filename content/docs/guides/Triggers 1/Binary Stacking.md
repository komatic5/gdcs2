---
title: Binary Stacking
weight: 347
draft: true
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Short** (5-7 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- You can use Binary Counting to your advantage to optimize groups in the form of Binary Stacking.
- Count in binary and use it in Move Logic to stack X/Y Mod multiples This can allow you to do things like make dozens of parallax layers with only a few groups.
- Use Toggle Logic to optimize frame-by-frame animations or anything that requires separate states.
- Binary stacking can be further expanded for other types such as ternary stacking, although these require a bit more math and are further limited by groups.

{{< /callout >}}

** **
# 0: What is Binary?

Binary is a numeral system that is __composed of just 1s and 0s__, unlike the more commonly used decimal system which is __based on powers of 10__. Counting in **decimal** looks like this: 1, 2, 3, 4, 5, 6, 7, 8, 9, and 10. Counting in **binary** looks like this: 0, 1, 10, 11, 101, and so on. 

## Numbers in Binary
The 1s and 0s in binary are called binary digits, also known as **bits**. Each bit represents a power of 2, starting with 2⁰, and can increase in value indefinitely.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1Y4XItPD-xoV_Qfw2NvAZIJ5HGfQnPBco/preview?usp=drivesdk></iframe></div>

## Converting from Binary to Decimal
To convert from *binary to decimal*, we add the value of every active bit (1) multiplied by its placement in base-2 to get a decimal sum.

For example, the binary number 0010110 converts into 22.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1DIIfbRcyacIvVK0QBPPKla-J7P0fSUkH/preview?usp=drivesdk></iframe></div>

## Converting from Decimal to Binary

To convert from *decimal into binary*, start at the largest power of 2 that can fit into the number you are converting. If the number you are converting is larger than the selected power of 2, put a 1 in that column, and subtract that power of 2 from your number. If the number you are converting is smaller, put a 0 in that column and don’t subtract anything. Move on to the next highest column of 2 with your new number and repeat this for each of the following columns.

For example, take 22 again, but this time convert it back into a binary number.
1. The highest power 22 can fit into is 16, so put a 1 in the 16 column and subtract 16 from 22 to get 6. 
2. 6 cannot fit into 8, so put a 0 in the 8 column. 
3. 6 can fit into 4, so put a 1 in the 4 column and subtract 4 from 6 to get 2.
4. 2 can fit into 2, so put a 1 in the 2 column and subtract 2 from 2 to get 0.
5. 0 cannot fit into 1, so put a 0 in the 1 column and you're done.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1QJGhpapr9Y2r2-RnSa_CAjoBp_IGrtCf/preview?usp=drivesdk></iframe></div>

This is only a brief explanation. If you are still confused about how to convert from decimal to binary, https://discord.com/channels/414295025883545600/1085291975663689809 explains this in more detail. **This video may help too**. (You will only need to know how to use the subtraction method for this lesson.)
https://www.youtube.com/watch?v=rsxT4FfRBaM

# 1: Move Logic

This stacking method works on Move, Follow, Rotate, and HSV Pulse triggers (triggers that can **transform objects**). When these triggers stack, __their effects combine to make one singular effect__. What this means is that you can get *significantly* more efficient stacks without using nearly as many groups.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/15cp0Z2SjfPR9oCo_uAAlI2lhshpAH7ea/preview?usp=drivesdk></iframe></div>

**Parallax** is a good example of where Move Logic can be used. Instead of making a new follow trigger for each layer, you can use follow triggers for 0.5x and 0.25x the camera speed – as well as any other set of X/Y Mods you wish – __at the same time__.

For example, using 0.5x, 0.25x, and 0.12x gives you **7 possible combinations** (0.12, 0.25, 0.37, 0.5, 0.62, 0.75, and 0.87), which are almost perfectly spaced out. You can do this with any set of numbers as long as they are in multiples of base-2. (e.g. the first layer moves .25x, on the 4th bit, you multiply 8 * .25 to get 2.)

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1k7FjetNBAX4C8-NcbespVNkCtnaAOkYl/preview?usp=drivesdk></iframe></div>

Using this method of stacking will give you **2*ⁿ* - 1** possible combinations, where *n* is the *number of groups* you’ve stacked.

# 2: Toggle Logic

Toggle logic is significantly more powerful than Move Logic since it works with any trigger that can **toggle objects**.

To recap the __Logic Gates__ guide, Toggle triggers essentially work like **AND gates**. If an object is linked to multiple groups, it will only be toggled on if ALL of those groups are toggled on.

Going back to __Binary Counting__, you can see how Toggle triggers function in the same way as **bits** do. With a single bit, you get **two** possible states, 2 bits get you **four** possible states, 3 bits get you **eight**, etc.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1HX3DMEiAo4xBha_dSCjpTaMpskp4ph_r/preview?usp=drivesdk></iframe></div>

Much like Move Logic, for every *n* toggle group, you’ll have a maximum of 2*ⁿ* - 1 possible states. This is especially useful for things that require a lot of unique states, such as frame-by-frame animation.

## Setup
To set this up, you need to have a base set of Toggle triggers - one that toggles a first group on, and another to toggle a second group off. I’ll refer to this Toggle setup as a “switch” from now on; this first switch will be for the Ones Digit.

Next, you need to place down your Ones Digit switches so they alternate which groups get toggled on and toggled off every time they run. Use as many as you need here.

After this, place your Twos Digit switches – use two new groups to make these switches, and place them down every other Ones switch. Repeat with Fours, Eights, Sixteens, and so on, just like you would when counting in binary.

<div><iframe src=https://drive.google.com/file/d/1olKmLB0YPBk6dsOaYJrLt8syULBUcSYY/preview?usp=drivesdk></iframe></div>

Overall this will give you 2⁽*ⁿ*/²⁾ -1 possible states, where *n* is the number of groups you’ve used on the switches.

# 3: Further Topics

There are further examples of this kind of stacking, such as Ternary Stacking in Base 3, but their applications follow a similar set of principles to Binary Stacking. You should be able to deduce their rules in a similar fashion.

If the math behind this stacking interests you then I would suggest you look into the closed-form summations behind trigger stacking – this’ll help you to optimize your group setups as much as possible. For example, if your stacking uses a base A then with n unique switches, you’ll be able to have A^(n/A) -1 possible states.

                                            ~~

> **Research:**  @koma5

> **Examples:** @koma5 @NotAModerator

> **Proofreading:** @nau. @NotAModerator

