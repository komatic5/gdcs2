---
title: Color 4 (Color Grading)
weight: 804
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Short** (8-10 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- There are numerous ideas regarding color grading, like gradual transitions between colors when there are changes of scenes. However, that is up to the creator to ideate themselves, and seeing what they can come up with.
- The next time you want to set an atmosphere for your level, always ask yourself if the colors are playing their role.

{{< /callout >}}

** **
Picture your favorite film in nothing but black and white, devoid of any greens of a forest, the reds of a sunset, or the blues of a moonlit night. How different would the impact be? In this guide, we will look at what **color grading** is, and how you can use it to bump up your levels.

## Crucial Techniques You Should Note before Digging into Color Grading
- **Color Balance** __focuses more on adjusting the intensity of colors__ to achieve a desired effect, or ensure that colors in the image appear natural and realistic. This is done by manually adjusting the Red, Green and Blue values, or by using Histograms and Curves. Histograms let you directly modify the tonal distribution of an image by adjusting sliders for highlights, midtones and shadows, while Curves let you adjust the alpha and lightness channel, often as a post-process filter to heighten the mood by adjusting the overall color, by moving parts of the curve.
- **Color Correction** __focuses on adjusting colors__ in order for the final product to look as accurate and visually pleasing as possible. This is done by adjusting the exposure, saturation, contrast and hue.
- **Color Curves** are a powerful tool to aid in the above methods, __allowing more precise control over tonal ranges and color channels__. This is done by shifting parts of the curve to change the brightness (by moving it up or down), or contrast (with an S-shaped curve).
- **White Balance** also assists in balance and correction, __adjusting the colors for objects that appear white in person to also appear white in the photo__, for a natural appearance. This is usually done by altering the intensities of RGB channels to neutralize the color cast.
- **Saturation Control** __involves adjusting the intensity or purity of colors in an image__. Just like how the Saturation slider in Geometry Dash’s HSV color menu works, more saturation means more vividness, while less saturation means more muted.

Some useful triggers for this include Edit Color (for saturation, brightness and tints), pulses with HSV settings (to control each aspect more finely than Edit Color), and the Grayscale shader (with a value below 1.00). The Edit Color trigger will be covered again later in this guide.

## What is Color Grading?
**Color grading** __is about creating a color tone for your level, to create a mood with the chosen color palette__. Instead of simply making the level appear more “realistic,” color grading conveys visual tone.

*But how do you incorporate this into your levels?*

# 1: Setting the Atmosphere

A level’s **“atmosphere”** can be defined as __how the player feels when playing the level__. Do you want your player to be intimidated or adventurous? Should they be energized or relaxed? There are many aspects to creating an atmosphere, and color palettes are no exception.

## Choosing Your Theme
By choosing your theme, you are easily able to choose what feelings you want to express through colors. For instance, a **horror** level may use a __dark, desaturated__ color palette for an ominous atmosphere, while a more **energetic** level will use __bright and vibrant__ colors.

Here are common colors and the feelings often associated with them:
- Red - Death, Anger, Power, Warning (Stop Sign)
- Orange - Freedom, Warmth, Joy, Playful, Caution (Traffic Cones)
- Yellow - Fun, Happy, Energy (the Sun)
- Green - Fresh, Love, Nature, Peace OR Toxic (Acid)
- Blue - Cold OR Burning (Blue flames from a stove), Sadness, Calm, Lonely
- Purple - Quiet, Reflective, Imagination, Royalty (in ancient times e.g. Bible)
- Pink - Luxury, Power, Mystery, Royalty, Romance (Valentine’s Day)
- Brown - Rusty, Old, Resilient, Well-worn (i.e. muddy)
- White - Purity, Mourning (in many Eastern cultures)
- Black - Mourning (in Western cultures), Formality (think Black-tie events)
- Grey - Metallic, Neutral, Conforming, Balance

While most color symbolism depends on things like culture (as evidenced by Black and White for mourning), the context of the colors also depends on things like the objects being coloured and their value.

APEIROPHOBIA by Ph4lip focuses on a very ominous and threatening mood, using dark and dull colors to increase the level’s immersion.

{{< youtube p-BUROO_-z0 >}}

## Finding Your Color Palette
The most effective way to do this is by creating the decoration using its normal colors, then altering them later to match the mood you want to convey, through trial and error. You can also browse reference images based on your theme, and examine the color palettes that they use, utilizing them when making your level.

The first part in Postbluane, created by Deovise, invokes a very calm, yet adventurous mood by utilizing blue tints and contrasting green colors.

Anarchy Road by Komatic5 enhances the destruction of the city by using red tints to invoke a more violent feel.

{{< youtube QHe2vLYCvSQ >}}

{{< youtube kY_iLItMdWw >}}

One way to learn how different colors work together is by altering the color palette of an existing artwork. In the following example, I will use mine.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1oW8Z7ideTpePacI3WN3MLp7fxCP77_9w/preview?usp=drivesdk></iframe></div>

I have made 5 other versions, each with a different color scheme.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1UuodsuVmJ5peI3CLkHvqxxxF4yBGZRJ3/preview?usp=drivesdk></iframe></div>

Although every version depict the same set of clouds and scenery, each artwork invokes a different mood (e.g. Time of day, Temperature), due to the change in color palettes. This activity allows you to understand how specific color combinations can lead you to specific atmospheres.

Now that you’ve gotten your color palette, how can you make it work from a design perspective?

# 2. Creating Visual Harmony

## Proportional Color Usage
You should use colors in proportion to maintain visual balance. **Dominant colors** should take up __most__ of the visual space, while **accent colors** should be used __sparingly__ to highlight important areas, or add visual interest.

## Pulses
Pulses are generally used to show intensity. However, when sticking to a theme, it’s best not to make them stand out too much, as it will eventually ruin the mood of the level. This includes aspects like brightness and hue.

**Hue:** __This is defined as a color or shade.__ For a level intended to feel hot, you would stick to a warm color scheme (Red - Yellow), hence avoiding pulses with cool colors (Green - Purple). Keep your pulses within the range of warm colors.

**Brightness:** __This is defined as the amount of luminance a color of shade has.__ For a dark level, your pulses would need to be fairly dark as well, but light enough such that they are visible to the naked eye.

An example of mine shows strong pulses that don’t necessarily disrupt the mood of the level. To stick to a cold atmosphere, I stuck with pulses around the blue range, to allow the cold mood to maintain itself throughout the level.

{{< youtube Njg8nLXN4-M >}}

## Tools of the Trade: Edit Color Trigger
When you open the **Edit Color** shader trigger, you will be greeted with this menu.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1NPELig6bZgiHzCXV7zm3pJrvX1Y_i9eE/preview?usp=drivesdk></iframe></div>

The top row (CR, CG, CB) affects the tints of each corresponding color (Red, Green, Blue). A value of 1.00 implies no tint. A value **greater than 1.00** __strengthens__ the tint of the color, while a value **lower than 1.00** __uses up the colour__ more instead.

The bottom row (BR, BG, BB) act as brightness sliders, similar to the one in the HSV menu. A value of 0.00 adds no brightness. A value **greater than 0.00** __brightens__ the color, while a value **lower than 0.00** __darkens__ it, removing the color.

Here’s an example on using the Edit Color trigger to alter color schemes, using my level And Ever as the subject.

Here is what the original looks like:

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1xaYLHxINWGZ6BzYH7y5CQYwMI6hS0Tea/preview?usp=drivesdk></iframe></div>

Here is an example where I was trying to get a cooler, blue mood, but the colors needed to be corrected:

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1tehI42JAsomZG1rKfoAdKXFOK4CMKibO/preview?usp=drivesdk></iframe></div>

Although a blue tint helps with a cooler mood, too much of it may just make it look more “blue” than “cool”. We can take a look at several images of cooler nature, and try to take inspiration.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1vvoXwmfDWC8zDjYOx4LNE6c5CQXVNCk9/preview?usp=drivesdk></iframe></div>

We can see that most of the green colors are visible, and that the blue is slightly grayed out. On our Edit Color trigger, we can try to reduce the blue colors, and keep most of the green present like how the image depicts it. We can also resort to altering the colors themselves if we can’t get our desired color scheme with just the Edit Color Trigger alone.

<div><iframe src=https://drive.google.com/file/d/1YVhchkq_Cnb94GMrVqu2v_zP-IgImIiM/preview?usp=drivesdk></iframe></div>

Though still not the best, this definitely looks a lot more reasonable than the earlier example.

While this trigger focuses more on color correction, it is still effective as it allows you to alter the colors to the atmosphere in a more concise way, instead of having to manually edit every color channel. You can also stack 2 of these triggers (one with a new setting, and another with the original setting that’s offset to the right) to create a pulse effect.



## Sources
- [Adobe: What is color grading and how do I use it?](<https://www.adobe.com/creativecloud/photography/hub/guides/what-is-color-grading-in-photography.html>)
- [Film Supply: Understanding the Basics of Cinematic Color Grading](<https://www.filmsupply.com/articles/cinematic-color-grading/>)
- [London Image Institute: Color Psychology: How Do Colors Affect Mood & Emotions?](<https://londonimageinstitute.com/how-to-empower-yourself-with-color-psychology/>)

**Video:** https://youtu.be/P2r4Z5kbx7M?si=do9Of4Aj0y9cZkz1&t=1116



## Credits
Created by @DangerChampion and @galofuf
