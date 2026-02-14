---
title: Blending Masks
weight: 516
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Short** (5-7 minutes)

# 1: How Blending Works

Every color is composed of three primary colors:  red, green, and blue (RGB). The intensities of these colors depend on their number values, which range from 0 to 255. For example, pure red would have an RGB value of (255, 0, 0), or 255 red, 0 green, and 0 blue.

The process of **additive blending**, or simply **blending** (as it is referred to in Geometry Dash), __takes the RGB values from two colors and adds them together to produce a new color__ with a new set of RGB values. As an example, using additive blending to combine red (255, 0, 0) and blue (0, 0, 255) produces magenta (255, 0, 255).

Since RGB values cannot exceed 255, if a pure red block were to be added onto another red block, the end result would produce pure red.

Although starting with pure RGB values is an important part of blending, there is no default way to select pure blue or green in the editor’s color slider. A workaround is to start with red through the HSV slider, copy the red to another color channel, and change the hue of that color: `+120` for green, `–120` for blue. Additionally, `-60` produces magenta, `+60` produces yellow, and `±180` produces cyan.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1mCcqYu6FAj5Cai-wknJ44foGBFH1lHm9/preview?usp=drivesdk></iframe></div>

There are some very important facts for this guide which you should know:
- Since black has a zero value for red, green, and blue, a blending color will perfectly show up on black.
- Since white has full values for red, green, and blue, blending colors will look invisible on white.
- Adding one color to another when its primary color is maxed out will not add any more of that primary color.

# 2: General Blending Mask

This mask uses blending to produce different colors depending on which color is behind it.

## Setup
1. Start by making two of the same pattern with different colors. Make the color of the top layer blending, and then stack them.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/12fLglTECj634AxXvG_5t1pJhdYeJLXSN/preview?usp=drivesdk></iframe></div>

2. Put a block design in between these layers.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/12V554HDrPGmDgtpxeQ3W2rm9xnRkH_2v/preview?usp=drivesdk></iframe></div>

You should end up with this.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/13QMjY_-H-nOkKuTXs5s1xqlHiHftkAYe/preview?usp=drivesdk></iframe></div>

## Pros
- Wide range of colors
- Simple
## Cons:
- Patterns cannot contain overlapping

## Examples

- Curl Up by ilrell and Millepatte

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1Id3MeXEcGGoMVDKwlsTXUPXphFju2DJy/preview?usp=drivesdk></iframe></div>

# 3: White Mask

This mask takes advantage of white’s properties regarding blending colors. Since blending colors look invisible on white, they can help make some interesting block designs and trippy effects.

## Setup
1. Start by making the background white. This is the most integral aspect of this mask.
2. Make your block designs. Black and gray are usually preferred, but any color besides white works perfectly fine.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1Uz-hAa36TakUCHg-VWD8wcTAZaUyU3Im/preview?usp=drivesdk></iframe></div>

3. Now make a design using blending colors. Make sure these designs have a higher Z Layer than the block structures.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/15esDbmAPDacEsEXPVzad8D3nNx6hx8LY/preview?usp=drivesdk></iframe></div>

4. Combine your two designs in the same space to complete the mask.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1pdLuaucRQ0JlaEehlQaJdvIk9DRspaBr/preview?usp=drivesdk></iframe></div>

## Pros
- Easy to use
- Trippy and interesting visuals
- Large range of colors
## Cons
- Background color is limited to white without using a non-blending overlay on top of everything

## Examples

- b e p i s by Wulzy

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1sXVUpCrZG7IbEw8AZ0HNOEy36aWw3QBr/preview?usp=drivesdk></iframe></div>

- INFINITY by FerdeFunky

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1zy2Z-BH8ZoyOZg066tu0n4XNDyWZI4o7/preview?usp=drivesdk></iframe></div>

- Abscond by ilrell

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1getxqFFvOogzIDsbev4SYIuCL30WDkLK/preview?usp=drivesdk></iframe></div>

# 4: RGB Color Mask

This mask takes advantage of the properties of red, green, and blue.

If pure red was added to a color with a full value of red such as yellow, the red will look invisible as `(255, 0, 0)` plus `(255, 255, 0)` equals `(255, 255, 0)`. The same applies for green and blue as well.

## Setup
1. Create two layers, one of white, and one of black. Make sure the black is on top.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1EZ5hKgc1xUAC7_EZudjIPEf9xCglxWcK/preview?usp=drivesdk></iframe></div>

2. Create two designs, using the following guidelines.
 - The first one must be either blending red, blue, or green, and it must be on top.
 - The next design must be between the black and white layers, and its color must *not* use blending.

In this example, blending red was used so the hearts were made yellow `(255, 255, 0)`.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1VZSx_UxgKwECEKAwXwFHjpn5VGp2bSIn/preview?usp=drivesdk></iframe></div>

When applied to some block silhouettes, you get the following.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1lVfnJ0pReMPtg6SlxGxmPRubh3bY9xWb/preview?usp=drivesdk></iframe></div>

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1t4T6NTW5I0sn00VCjMHfB8GTFHMGJMgv/preview?usp=drivesdk></iframe></div>

The colors can be varied to improve the color scheme. Here, the background is changed to a yellowish orange, and the hearts to a pink.

Since they still have a full value of red, the red stars still look invisible on them. Likewise, the blocks are changed to a dark blue. The stars will still show on them as they do not have a full value of red.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1zQ4wvz-Ax7CIJ02SXrY7HZ_KpeUUQFse/preview?usp=drivesdk></iframe></div>

## Pros
- Masked designs can overlap with each other
- More versatility than other masks
- Large potential
## Cons
- Tricky to use
- Colors hard to perfect

## Examples

- Curl Up by ilrell and Millepatte

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1PbvGp5FMy6hLotuWRWY-UTmapud5Z74C/preview?usp=drivesdk></iframe></div>

- WerewolfGD's part in Teslawolf (block structures)

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1a3h3YtugCTBnJQcMinIjXnO4EEtEuVfq/preview?usp=drivesdk></iframe></div>

- Key by ilrell and Swirl

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/12ktoSheq3T7wyLzdGIw0fsoAMDekA272/preview?usp=drivesdk></iframe></div>

# 5: CMYK Color Mask

This mask is similar to the RGB Color mask, but it lets 3 different masks occur at once.

## Setup
1. Start by making blocks of cyan, yellow, and magenta. You can use [this link](<https://discord.com/channels/414295025883545600/1104661567502549113/1162538491138277437>) if you need help making these colors.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1sYqIXNJWfl675PUcyPWViDTDPU2MPOhU/preview?usp=drivesdk></iframe></div>

2. Make patterns of blending red, blending green, and blending blue. Make sure they are slightly transparent so they will not show up as white when added onto the blocks.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1y6XlK5xKRv6K4WPyBiBusZMnepe7hPAT/preview?usp=drivesdk></iframe></div>

Because cyan has an RGB value of `(0, 255, 255)`, all colors besides those with a red value will appear invisible on top of it. This is also the case for yellow `(255, 255, 0)` and magenta `(255, 0, 255)`.

It's important the blending colors are semi-transparent, because if they were fully opaque, the pattern would look fully white, as `(255, 255, 0)` + `(0, 0, 255)` would result in `(255, 255, 255)`, which is white.

<div><iframe src=https://drive.google.com/file/d/1nEMsSesAVYH-IB5P9esH4irxKgoYwTvH/preview?usp=drivesdk></iframe></div>

## Pros
- Three mask designs can be used concurrently
## Cons
- Tricky to use
- Color schemes are difficult to use (a low opacity color overlay on the blocks is recommended)

## Examples

- Concept Video by Spu7nix

{{< youtube EyctAc5fsqw >}}

## Summary

- The Blending feature in the editor allows you to combine the colors of objects by adding their RGB values together.
- Masking is one of the many applications of this feature.

## Return To The [Table of Contents](https://discord.com/channels/414295025883545600/1104661567502549113/1104661567502549113) Here

**Video:** https://youtu.be/P2r4Z5kbx7M?si=OXRptoIaYPXfi597&t=1274



## Credits
Created by @KDE and @Unknown
