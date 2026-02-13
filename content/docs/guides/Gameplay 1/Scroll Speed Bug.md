---
title: Scroll Speed Bug
weight: 411
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Short** (6-8 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- The Scroll Speed Bug (SSB) is a bug in the game that is unfixable.
- It is related to floating point numbers (floats) being inaccurate, especially at very high values.
- SSB can cause certain effects like:
- The player speeding up or slowing down.
- The wave pointing straight.
- The blocks and visuals displaying incorrectly.
- The X-pos limit, where the value you are adding to the player is so slow that the player just stops moving. It is not because the player reaches the 32-bit integer limit.

{{< /callout >}}

** **

# 1: Basic Info

If you have ever worked with a calculator, you may notice that doing arithmetic on numbers with many decimal places is inaccurate. For example, on Desmos, 2.222222222222 + 3.333333333333 will give you 5.55555555556, no matter how long you make the numbers. This is due to a little thing called floating point precision loss.

Floating point numbers are a subset of real numbers, allowing you to represent values with decimal places. On x86 (the version Robtop made GD in), floats are 4 bytes (or 32 bits), being in the IEEE 754-1985 binary32 format. This means you have 1 bit for the sign, 8 bits for the exponent (the floating part of the floating point), and 23 bits for the base value, also known as the mantissa (read more about this [here](<https://en.wikipedia.org/wiki/IEEE_754-1985>)).

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1_Z1cfHyU9vdRAVYXCpESbzi9hAQ4KrqM/preview?usp=drivesdk></iframe></div>

If this doesn't make complete sense to you, that's fine. The important thing to understand is that data is finite. You can only put the decimal in one place, which means you can run into rounding issues.

# 2: Floats Are Weird

Another problem with floats is that we use a different number system than the one computers use. Our numbers are encoded in base 10 (decimal), while computers use base 2 (binary). To see why this might be an issue, check out this site: <https://www.h-schmidt.net/FloatConverter/IEEE754.html>. If you enter a number that isn't directly representable, such as 0.7, you will get a value like 0.699999988079071044921875, which is a bit off!

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1HCHuAhIp2OE-eAzmVZWgYM8esCM14CbQ/preview?usp=drivesdk></iframe></div>

This is caused by the fact floats are represented in the form `mantissa * 2 ^ exponent`, where the mantissa is `1.NNNN....` For example, the number `6.0` is represented as `1.5 * 2^2`, an exact value. But the number `0.7` does not fit into base 2 perfectly, being represented as `1.399999976158142 * 2^-1`.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1hTzENqsSmgF4ayCqTpdMIftU3lZYHS8L/preview?usp=drivesdk></iframe></div>

# 3: How is this related to GD?

There are a few ways to represent a player's position relative to the world that avoid precision errors. One option is to recenter the world origin as the player moves around (which works best for single-player games). Another is to break up the world into multiple maps, not allowing the player to reach a position that would cause these inaccuracies in the first place. Geometry Dash does none of these.

Robtop could not have expected the way people would play the game, with players and creators bypassing the fixed length limit and playing at impossibly high framerates.

The player is moved forward by this pseudocode: `position = last_position + ((base_units * speed_constant) / FPS)`. Most of the time, this isn't an issue. `base_units` is ~`468.001038`, meaning when playing at the intended 60fps at 1x speed, you will move forward at ~`7.8 units/tick`.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1kzVw4Txc416FERWDcxQqQbftuanvH3Gn/preview?usp=drivesdk></iframe></div>

You only run into issues when using large FPS or X-pos values. To show why, let's look at 2 examples:

First, we want to do `3.0 + 1.5`. This is very easy to represent, as their exponents and values are very similar. You get the expected value of `4.5`, with exact representation.

Our second example is tough, being `10000.0 + 0.00001`. Here, the values are very different. This is internally represented as `(1.22 * 2^13) + (1.31 * 2^-17)` (mantissas rounded). When adding these, instead of getting `10000.00001` as you would expect, we get `10000`. The latter is the reason you stop moving at a certain point. The smaller value is just too low to be represented alongside the larger one and is discarded. This means no matter how many times you add it, nothing will change.

But what happens in between? Let's say you were at the x position 10,000 at 1x speed, using 1440fps. This would be the equation `10000 + 0.334286456`. Again, the value is not what we would expect, being `10000.333984375`, but instead of the added value being completely ignored, it is just rounded incorrectly, with an error of about `0.000302081`.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1lhcEgHahhlcqza6HkxDHDFs40tHWv2r7/preview?usp=drivesdk></iframe></div>

This is the cause of the Scroll Speed Bug: a combination of floats only being able to correctly represent powers of two, having a finite size, and being biased against their fractional part.

# 4: Can I Avoid the Scroll Speed Bug?

The only way you can avoid the Scroll Speed Bug is to never encounter it in the first place. There isn’t really another way to avoid it. You can slow it down by using more data, - such as double precision floats, which are 64-bit - but you will have the same problems as 32-bit floats. You can also use arbitrary precision floats, but this means you move the math out of hardware and into software, which is orders of magnitude slower (read more about this [here](<https://en.wikipedia.org/wiki/Floating-point_error_mitigation>)).

Even if there was a technique which completely removed this effect, it would be modding the game, effectively cutting out most of the players that might play your levels.

Instead, just make sure your 25957.9 FPS level doesn't go past 131072 units. This can be verified using this website: <https://godbolt.org/z/eMe1Yf8ee>.

# 5: The Consequences Of The Scroll Speed Bug

From Yang’s text above, we now know that the **Scroll Speed Bug (SSB)** is just __floating numbers being weird and imprecise__, causing the player or nearby objects to move at different speeds, seemingly changing randomly to be slower or faster than usual, display differently and collide differently.

A very extreme example of this is Unknown Processing by MagicTabLordGD, where the player is placed at the X-pos limit of 60fps and via a move trigger, the entirety of Blast Processing moves towards the player. In Unknown Processing, we see how crazy the game behaves at such large distances. The quads which render the textures of the game are no longer quads due to their position being calculated incorrectly because of floating point imprecision. The wave is also moving only up and down since the x position of the player doesn’t change, locking it in place.

<iframe width="560" height="315" src="https://www.youtube.com/embed/nlFyXTnNy24" frameborder="0" allowfullscreen></iframe>

A more practical example is this showcase of Blast Processing at 75000 FPS: https://youtu.be/rw5l_NNI-Ic?si=2CTlELZb19qt7sTL

Here, you can see the effects you will most likely encounter:
- Increase in speed: SSB can sometimes increase the speed of the player, allowing them to jump farther than expected. Here’s an example: <https://youtu.be/2NFb2StSFN4>
- Slowing down: Same as the above, but you instead slow down on the speed that you are on, causing you to jump in awkward trajectories
- Wave wonkiness: This is just 2 effects on the wave, which is shown below.

Blast processing but on 75000 fps (Recording by Aligned)

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1V_ahufaa72tVryEw5M0ks8beec0RwEMK/preview?usp=drivesdk></iframe></div>

Thanks level by FancyEX but on 80000 fps (Recording by PhiPan)

<div><iframe src=https://drive.google.com/file/d/1ouTeYbSvYmoiU-eO8dFn38kq5rdD9nij/preview?usp=drivesdk></iframe></div>





## Credits
Created by @DangerChampion and @Unknown
