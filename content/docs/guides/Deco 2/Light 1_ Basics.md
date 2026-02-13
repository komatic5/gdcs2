---
title: Light 1 (Basics)
weight: 806
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Short** (4-6 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- Light and Shadow are an important way to make your deco more convincing. They’re two sides of the same coin; shadows are created in the absence of light.
- Hard Light occurs when light rays are parallel to each other, creating sharp shadows. Soft Light occurs when light rays scatter in many directions, making softer shadows.
- You can use properties like Occlusion, Reflected Light, and Light Falloff to make your rendering look more realistic.

{{< /callout >}}

** **
**1: Basics**

Light and shadows are something that you see everyday in your daily life. Light comes from things that emit light, such as the sun, candles, lamps, and your computer screen. Shadows are the result of light hitting an object.

To better understand this, take a look at any object that’s illuminated by light. You’ll see two different shadows: a **form shadow** – the dark areas of the object – and a **cast shadow** which shows up on the ground. Together, light and shadow create what’s known as **value**, how light or dark an object is. This is crucial for making objects look 3D.

When light rays hit an object, they’ll hit different sides in different ways. This creates a change in value; as such, different sides of an object will be brighter than others. The image below shows an example of this.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1LaZv5S39Izyf3YynsdwJ8iR_swR8_tQe/preview?usp=drivesdk></iframe></div>

Here, the light source is on the left side; as such, the sides facing the left are brighter. It may be hard to fully grasp this when you’re starting out, so I recommend using black & white images so you aren’t distracted by colors. I also recommend you gain an intuitive understanding of perspective, as it’ll help you gain intuition faster.

**2: Types of Light**

We can distinguish different types of light based on the types of shadows they cast on the ground. **Direct** or **Hard Light** means that light rays are strongly aligned with each other. This makes a harder cast shadow with a sharp edge, almost as if the shadow is mimicking the shape of the object itself. A good example of this is the light on a bright sunny day.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1QCcp2iJEsuIKduyVs_HjbByL9Any1p6_/preview?usp=drivesdk></iframe></div>

On the other hand, **Soft Light** occurs when the light rays come from many angles. This makes the cast shadow have a soft edge. Sunlight on a cloudy day is a good example of this.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1eU5me7ChIWFyDr5JFBvxXon6pe3uJqRz/preview?usp=drivesdk></iframe></div>

**Light Decay/Falloff** occurs because light gets less intense the further you are from it. Objects closer to light sources will be lit more strongly than ones further away. If you want to be fully scientific, you can use the Inverse Square Law, where light’s intensity decreases based on your distance squared.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1UhIfRE39HWg7lzYFecoN_cwuYcitymeL/preview?usp=drivesdk></iframe></div>

This is important when rendering, because the strength of the light will diminish with distance. As such, objects will be lit more ambiguously. Not only does light falloff help with realistic lighting, but it can also help you play with the environment’s mood.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1WTHDGA8BWAVyxb0UL74Dv9fPZGp-vjXE/preview?usp=drivesdk></iframe></div>

Sometimes you’ll want to use outlines when rendering, but just drawing a thick outline will look awkward. This is where **Edge** or **Rim Lighting** can be used. This lets you use light to outline an object, while it mostly stays dark otherwise.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1hY4LHPbkagZcpl8w-tatH_BiJGECKsRL/preview?usp=drivesdk></iframe></div>

This is especially true when the light source is coming from behind the object, creating shadows in the middle areas of the object but lighting up the edges.

**3: Light Properties**

Light can display interesting properties that aren’t always the most intuitive. Here, we’ll go over them in kind.

Multiple light sources occur when there is more than one light source coming from different directions. Having more than one light source will also create multiple cast shadows. These light sources can also be different from each other, so you must pay close attention to that when rendering. When the light sources change, so do the cast shadows.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1j3TvKbeEv3ZZiNsIEcA3GDnLpJ5RaRkn/preview?usp=drivesdk></iframe></div>

Multiple shadows can overlap, essentially making an even darker shadow where the two cast shadows cross paths, similar to a stacking or doubling effect. Note that the shadows will be lighter where they don’t intersect, as more light is reaching those areas.

**Occlusion** is a shadow effect of light being blocked by a surface next to it. This occurs where two surfaces meet to block the light, such as the corner of a wall.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1Q4O6foRtw8wFgSyqcwozy6LxCE2eCJbv/preview?usp=drivesdk></iframe></div>

Adding occlusion enhances the realism of what you are rendering. The image below shows the same image with and without occlusion. The image on the right seems much more 3d, and has a better sense of depth, as compared to the image on the left; this is primarily due to occlusion.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1H68njExaEMnSwKVLp-8ug7PmDT2GlrC7/preview?usp=drivesdk></iframe></div>

**Reflected/Bounce Light** is when light bounces off of one surface and illuminates another. This usually results in softer, less intense lighting. In the image below, Letter `A` is the light source, and letter `C` is illuminated due to light bouncing off of letter `B`.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1DpIfXgREBa_H8SoI3gOw2ZCl98DiknK3/preview?usp=drivesdk></iframe></div>

Another example is this sphere shown below.  The light bounces off of the ground which creates soft light on the underside of the sphere.

<div><iframe src=https://drive.google.com/file/d/1pfl5iVsOKiKedivoQS7Y2IvOHfDmaxto/preview?usp=drivesdk></iframe></div>


## Sources

- Scott Robertson: *How to Render*, Pages 17-26

Changed the channel name: Light 1: Basics



## Credits
Created by @koma5 and @print
