---
title: Screen Filters
weight: 322
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Medium** (14-16 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- Shader Triggers alter the player’s and level’s qualities and colors.
- Shader Triggers are divided into two categories: Screen effects and Color filters.
- Screen effects distort the screen and the player, while Color filters change the colors of the player and the level.

{{< /callout >}}

** **
# 1: Screen Effects

## Shader
__Sets a range of Z layers that other shader triggers will affect.__
- The cyan buttons are the minimum and maximum layers.
- The green buttons are layers affected by the other shader triggers.
- The gray buttons are layers unaffected by the other shader triggers.
- **Disable All**: __Disables any active shaders__.
- **Disable player particles**: __Prevents any shaders from affecting the particles that come from the player during gameplay__. This option is here since the rendering of some shaders on these particles can look a bit weird.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1zWChW-p3LqHCxN4BxaavnkIIe_tKMS84/preview?usp=drivesdk></iframe></div>

## Shock Wave
__Creates a shock wave that moves to or from a center point.__
- **Speed**: __How fast the wave will move__. Higher values mean higher speed.
- **Strength**: __The amount of distortion of the wave__. The higher the value, the more distorted objects will be in the wave.
- **Thickness**: __How “long” the wave is__. The higher the value, the longer the wave of the effect will last. Generally, if the thickness is higher than the wave width, multiple waves will spawn to fill the gap of time, however the ratio is not 1:1 and more like 1.5:1 (in thickness’ favor).
- **WaveW**: Stands for “Wave Width”. __Sets the width of each wave__. The higher the value, the wider the wave.
- **FadeIn**: __How smooth the wave will fade into distortion__. In other words, this affects the outer part of the *first* wave in a wave sequence.
- **FadeOut**: __How smooth the wave will fade out from distortion__. In other words, this affects the inner part of the *last* wave in a wave sequence.
- **TimeOff**: __The amount of seconds the effect will be offset by__. Negative values will delay the start of the waves, positive values will start the waves at an earlier point of the effect (This does not start the effect before the trigger is activated, think of it as the song offset but for an effect).
- **MaxSize**: __The maximum distance the waves can travel__. 0 is the default and leaves no limit.

- **ScreenOffX**: __The X offset of where the waves spawn__. Negative values go left, positive values go right.
- **ScreenOffY**: __The Y offset of where the waves spawn__. Negative values go down, positive values go up.
- **Invert**: __Inverts the movement of the wave__ so that it spawns waves that go from the edge of the screen to the center.
 - **Inner**: __How big the radius of distortion is from the center of the screen__. Basically creates a circle you set the size of that distorts the area it is in as waves get to it.
 - **Outer**: __How far the waves spawn away from the center of the screen__. The waves will travel the same distance as before, so higher values may not be seen without any offset.
- **Target**: __Sets the center of the effect to a player or a single object using a group ID__. The default position of this option is around 3 blocks under the player’s spawn point.
 - **Follow**: __If enabled, the center of the effect will follow the Target if it is moving__. If not enabled, the center of the effect will stay at the place the Target was at when the shader was originally activated.
- **Animate**: __Allows you to change the settings of an active shock wave effect__. Pressing the trash button next to a setting will have that setting ignored.
 - **FadeTime**: __How long the effect lasts__. To the right are some easing options for the transition.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1CycJU3rf-ykl5pTSKXRZP-woTpFW3dHX/preview?usp=drivesdk></iframe></div>

## Shock Line
__Creates a shock wave effect that moves across the screen.__
- **Speed**: How fast the wave will move. Higher values mean higher speed.
- **Strength**: The amount of distortion of the effect. The higher the value, the more distorted the effect will make objects.
- **Thickness**: How “long” the wave is. The higher the value, the longer the wave of the effect will last. Generally, if Thickness is higher than the Wave Width, multiple waves will spawn to fill the gap of time, however the ratio is not 1:1 and more like 1.5:1 (in thickness’ favor)
- **WaveW**: Stands for “Wave Width”. Sets the width of each wave. The higher the value, the wider the wave.
- **FadeIn**: How smooth the wave will fade into distortion. Basically effects the outer part of the *first* wave in a wave sequence.
- **FadeOut**: How smooth the wave will fade out from distortion. Basically effects the inner part of the *last* wave in a wave sequence.
- **TimeOff**: The amount of seconds the effect will be offset by. Negative values will delay the start of the waves, positive values will start the waves at an earlier point of the effect (This does not start the effect before the trigger is activated, think of it as the song offset but for an effect).
- **MaxSize**: The maximum distance the waves can show up from in the center of the screen. 0 is the default and leaves no limit.

- **Invert**: __Inverts the amplitude of the wave__. Basically it turns the high parts of the wave to low parts and vice versa.
- **Flip**: __Reflects the effect so that it moves from the opposite side of the screen__.
- **Rotate**: __Rotates the effect so it moves along the y-axis instead of the x-axis__.
- **Dual**: __Spawns two waves that spawn at the center of the target that move away from each other__.
- **Target**: Sets the center of the effect to a player or a single object using a group ID. The default position of this option is around 5 blocks to the right of the player’s spawn point.
 - **Follow**: If enabled, the center of the effect will follow the Target if it is moving. If not enabled, the effect will stay at the place the Target was at during the original activation of the shader.
- **Animate**: Allows you to change the settings of an active shock line effect. Pressing the trash button next to a setting will have that setting ignored.
 - **FadeTime**: How long the new changes will take effect. To the right are some easing options for the transition.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1nIeIXO1Z2JQCoHLH-5SkTx_gxtEYHsse/preview?usp=drivesdk></iframe></div>

## Glitch
__Creates a glitch effect.__
- **FadeTime**: __How long, in seconds, it takes to transition into the effect__.
- **Strength**: __How strong the distortion is__. It is a multiplier for the other adjustable settings.
- **Speed**: __How fast each glitch will occur__. Higher values mean more glitches happening per second.
- **SliceHeight**: Slices are horizontal strips that offset the visuals within them. __This setting sets the *max* height these slices can be__.
- **MaxSliceXOff**: __How much each slice can distort objects from its original x-axis__.
- **MaxColXOff**: __How far the RGB values can be offset from its original x-axis__.
- **MaxColYOff**: __How far the RGB values can be offset from its original y-axis__.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1gOG17AQngKDum5CUt2BISxrDJlSoVt4T/preview?usp=drivesdk></iframe></div>

## Chromatic
__Splits up RGB values and offsets them from each other.__
- **TargetX**: __How far the colors move on the x-axis__. Must have “Use X” enabled for this to apply.
- **TargetY**: __How far the colors move on the y-axis__. Must have “Use Y” enabled for this to apply.
- FadeTime: How long, in seconds, it takes to transition into the effect. Easing gives options on what easing the transition will use.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1eFRGCveuV86Fgb4CmiZmzxToFdfpYDw0/preview?usp=drivesdk></iframe></div>

## Chromatic Glitch
__Creates a different glitch effect, with slightly more emphasis on chromatic effects.__
- **Speed**: __How fast the distortion effect moves__.
- **RGBOff**: __How far from the x-axis the color split is offset__. Negative values can be entered to offset it to the right.
- **Strength**: The amount of distortion of the effect. Higher values mean more distortion.
- **FadeTime**: How long in seconds it takes to transition the effect. Easing options at the bottom give easing for the transition.
- **LineThickness**: How wide the horizontal lines on screen are.
- **SegmentH**: __How high each segment is (how far apart they are)__. Each segment is marked by the lines on screen.
- **LineStrength**: __The opacity of the lines__. Lower values make the lines more transparent.
- **Disable**: __Disables the effect__.
- **Relative Pos**: __Locks the segments to the grid instead of them following the camera__.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1PV3YjFJCR9OslqfsEbeTkqMs9Rmc9mo1/preview?usp=drivesdk></iframe></div>

## Pixelate
__Pixelates the screen__.
- **TargetX**: __How much the screen is pixelated on the x-axis__. “Use X” must be enabled for this to work.
- **TargetY**: __How much the screen is pixelated on the y-axis__. “Use Y” must be enabled for this to work.
- **FadeTime**: How long, in seconds, it takes to transition into the effect. Easing gives options on what easing the transition will use.
- **Snap Grid**: __Enabling this makes the pixels follow the grid instead of the camera__.
- **Hard Edges**: __Sharpens the pixelation effect so it looks less blurred__.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1E94nWqkZHQMxL8409JU0eTfRSOMXgXRG/preview?usp=drivesdk></iframe></div>

## Lens Circle
__Creates a lens circle around a center point__
- **Size**: __The radius of the effect__. Higher values means a larger circle.
- **Fade**: __The size of the gradient of the circle__. The fade is dependent on the size. Any values higher than the current size of the circle will be ignored as the max size is the max fade of the circle.
- **FadeTime**: How long, in seconds, it takes to transition into the effect. Easing gives options on what easing the transition will use.
- **Strength**: __The opacity of the effect__. Lower values make it more transparent.
- **ScreenOffX**: The x-axis offset from the center of the effect.
- **ScreenOffY**: The y-axis offset from the center of the effect.
- **CenterID**: __The ID of the object the effect centers on__. You can have player 1 or 2 set as this ID. By default, the center of the effect is the center of the screen.
- **Tint Channel**: __The color channel that the effect takes the color of__. By default, the effect is black. The opacity of the color channel is ignored.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1QV3RpgTISm219NR3O0PKDnteIEKhCflD/preview?usp=drivesdk></iframe></div>

## Radial Blur
__Blurs the screen from a center point__.
- **Size**: __How far each layer of “blur” is from the origin__.
- **FadeTime**: How long, in seconds, it takes to transition into the effect. Easing gives options on what easing the transition will use.
- **Intensity**: __**Doesn’t seem to work as of now**__. __Is supposed to change the opacity of the blur__.
- **Ref Channel**: __Sets the color channel the blur will use as reference to fade objects to__. By default, the blur will go into the color of the background.
- **ScreenOffX**: Offsets the center of the blur from its original x-value.
- **ScreenOffY**: Offsets the center of the blur from its original y-value.
- **Fade**: __How blurred the blur effect is__. Higher values mean less blur. Negative values don't do anything.
- **Target**: Sets the center of the effect to a player or a single object (using a group ID). The default position used if this is enabled is around the spawn point.
- **EmptyOnly**: __**Doesn’t work as of now**__. __Is supposed to only blur pixels with no objects in them__.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1GtemFTaORFoIwLLmEjvYF8Zbs3GtL9DN/preview?usp=drivesdk></iframe></div>

## Motion Blur
__Blurs the screen based on the movement of the camera, player, or selected object__.
- **TargetX**: How much the screen is blurred on the x-axis. Positive numbers offset it to the left, negative numbers to the right. “Use X” must be enabled for this to work.
- **TargetY**: How much the screen is blurred on the y-axis. Positive numbers offset it down, negative numbers up. “Use Y” must be enabled for this to work.
- **Ref Channel**: Sets the color channel the blur will use as reference to fade objects to. By default, the blur will go into the color of the background.
- **FadeTime**: How long, in seconds, it takes to transition into the effect. Easing gives options on what easing the transition will use.
- **Fade**: How blurred the blur effect is. Higher values mean less blur.
- **Follow Ease**: __How smoothly the blur reacts to movement__. Higher values means better easing.
- **Intensity**: __**Doesn’t seem to work as of now**__. Is supposed to change the opacity of the blur.
- **DualDir**: __Blurs objects in two directions instead of one__.
- **EmptyOnly**: __**Doesn’t seem to work as of now**__. Is supposed to only blur pixels with no objects in them.
- **TargetID**: __Sets the center of the effect to a player, the camera, or a single object using a group ID__. The default uses the default position as viewed in the editor, and the blur will not move.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1obNTxQfjjH8l4MxabKyzOqvHl4CWlzyo/preview?usp=drivesdk></iframe></div>

## Bulge
__Bulges the screen__.
- **Bulge**: __How intense the bulge effect is__.
- **Radius**: __The size of the radius of where the bulge is contained__.
- **ScreenOffX**: Offsets the center of the blur from its original x-value.
- **ScreenOffY**: Offsets the center of the blur from its original y-value.
- **FadeTime**: How long, in seconds, it takes to transition into the effect. Easing gives options on what easing the transition will use.
- **Target**: Sets the center of the effect to a player or a single object using a group ID. If no reference is put in, the bulge will act the same as if Target was not enabled.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1rDnreoZcI2BrKiXU03Gdmz0BUkjjZ4Zy/preview?usp=drivesdk></iframe></div>

## Pinch
__Distorts the screen by “pinching” it__. The opposite of the bulge effect.
- **TargetX**: How much the x-axis gets distorted. Higher values mean higher distortion. “Use X” must be enabled for this to work.
- **TargetY**: How much the y-axis gets distorted. Higher values mean higher distortion. “Use Y” must be enabled for this to work.
- **ScreenOffX**: Offsets the center of the effect from its original x-value.
- **ScreenOffY**: Offsets the center of the effect from its original y-value.
- **Radius**: The radius in which the pinch effect is contained.
- **Modifier**: __Modifies the distortion values used__. A lower value means less distortion.
- **FadeTime**: How long, in seconds, it takes to transition into the effect. Easing gives options on what easing the transition will use.
- **Target**: Sets the center of the effect to a player or a single object using a group ID. The default position used is around 3 blocks under the spawn.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1iQbWjP-E0K2389gVkpNucO9xJ2gNYzy2/preview?usp=drivesdk></iframe></div>

# 2: Color Filters

## Grayscale
__Filters the screen to a grayscale color__.
- **Target**: __How much the filter is applied__. Lower values mean less grayscale.
- **FadeTime**: How long, in seconds, it takes to transition into the effect. Easing gives options on what easing the transition will use.
- **Tint Channel**: Uses a color channel to tint the screen by instead of gray. The box next to the input must be checked in order to work.
- **UseLum**: __Uses a different color conversion method for the grayscale filter__. Instead of simply desaturating the end image, it applies a “value” filter which is more accurate for [color theory](https://discord.com/channels/414295025883545600/1104656557574213742/1185375023276503090).

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1Hqd1CVvEHWs-9OgqkccDVyL5xKAyya9K/preview?usp=drivesdk></iframe></div>

## Sepia
__Filters the screen with a sepia effect__.
- **Target**: How much the filter is applied. Lower values mean less sepia coloring.
- **FadeTime**: How long, in seconds, it takes to transition into the effect. Easing gives options on what easing the transition will use.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1sXUjLEG_NEq9h9kwHEFRVn5fhH-ob-BP/preview?usp=drivesdk></iframe></div>

## Invert Color
__Inverts the color of the screen__.
**Target**: How much the filter is applied. Lower values mean less inversion.
FadeTime: How long, in seconds, it takes to transition into the effect. Easing gives options on what easing the transition will use.
**R G B Sliders**: __Determines the percentage of the RGB values that will be affected by the options below__.
**EditRGB**: __Edits the final inversion filter__. The RGB sliders determine how much each color is affected by the inversion. Lower percentages mean less inversion. Values higher than 1 will transition into inversion faster, but will tint the final image.
**TweenRGB**: __Transitions new values for an invert color trigger smoothly instead of instantly__. Needs “EditRGB” to work and only works after an active invert color effect.
**ClampRGB**: __Limits the final max values for each color to 1/1/1__. Any values over 1 in the RGB sliders will be ignored.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1bgspn4aFN7iyNAXmAD4Wi3CTxzLw9g06/preview?usp=drivesdk></iframe></div>

## Hue Shift
__Shifts the hue of the colors on screen__.
**Degree**: __How many degrees the colors shift by__.
**FadeTime**: How long, in seconds, it takes to transition into the effect. Easing gives options on what easing the transition will use.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1Ca4cbeWeQWQKIkaeLB2WQG2mdsdOItPt/preview?usp=drivesdk></iframe></div>

## Edit Color
__Edits the RGB values of the colors on screen__.
**FadeTime**: How long, in seconds, it takes to transition into the effect. Easing gives options on what easing the transition will use.
**CR CG CB sliders**: C stands for color. __These sliders edit how much red, green, and blue colors are displayed__. Higher values mean more color and smaller values mean less color.
**BR BG BB sliders**: B stands for brightness. __These sliders edit the brightness of the red, green, blue values__. Higher values mean more brightness and lower values mean less brightness.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1e0h6B5rxP0-Sf68cffpw0NIT4Rif8Xgr/preview?usp=drivesdk></iframe></div>

## Split Screen
__Splits the screen into multiple screens__.
- **TargetX**: __How many screens the trigger adds to the x-axis__. Higher values mean more screens. Negative values invert the x-axis. “Use X” must be enabled for this to work.
- **TargetY**: __How many screens the trigger adds to the y-axis__. Higher values mean more screens. Negative values invert the y-axis. “Use Y” must be enabled for this to work.

<div><iframe src=https://drive.google.com/file/d/1qhbFhjKQoXIKHWoSNWGj9JU8xUcoLDTJ/preview?usp=drivesdk></iframe></div>





## Credits
Created by @DangerChampion and @TDP9
