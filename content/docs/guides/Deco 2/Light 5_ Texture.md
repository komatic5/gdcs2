---
title: Light 5 (Texture)
weight: 810
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Medium** (14-16 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- Texture is a type of detail that communicates how an object might feel to touch.
- Although it’s very tempting to make textures by spamming objects, being smart about how you place your objects will save you time and make your textures more effective.
- Many materials like metal, wood, and glass have distinct properties which you can leverage when making textures. It’s a good idea to employ photo reference and do some basic research on materials not covered here.
- Textures can also leverage lighting effects, such as subsurface scattering and the Fresnel Effect.

{{< /callout >}}

** **
Textures are details that let us imagine how an object would feel to touch. People typically use these for more “realistic” decoration to communicate what materials an object is made of.

However, textures are useful for more than just realism. This art was made by [NAKA](<https://naka.bio/>) as part of an abstract art prompt, and even though it’s not depicting any real-life objects, the texture and form still help you imagine what it might feel like to touch it.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1SKdRx3_Jqf8ivTtjIgHu0QqpM2NTQPqv/preview?usp=drivesdk></iframe></div>

This guide will explain how to render certain materials and use textures in more interesting ways, such as the art above.

# 1: Using Textures

Before we get into specifics of how to create textures, it’s important to lay down a few principles about how they work. Many creators end up with messy, spammed textures in their work because they don’t think about the *how* of using textures when building.
## Implied Texture
**Implied texture** is crucial for making efficient textures. This is when viewers use visual context clues to “fill in” details in your decoration, even when those details don’t actually exist. This will help you save time and objects when making textures, since you don’t *actually* need to lay down every single line and shape in a complex texture.

For instance, take this digital painting by [Philipp Urlich](<https://urlich.art/projects>). The grass is very detailed up front, but it quickly gets simplified into flat swathes of color with some basic hue variation. This also occurs with the trees; the trees closer to the viewer have far more texture than the more distant trees, which only have one or two colors on them.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1KwYFa37UYP4fFeGGcjBjuw6_NfgFhWaj/preview?usp=drivesdk></iframe></div>

## Texture Density
Implied texture also relates to **texture density**, or __how intricate a texture is__. People don’t just simplify textures to save time, but because that effort could be completely wasted. If you try to make extremely small and dense textures, they’ll often just turn an object into a noisy, indistinguishable mess rather than adding to it in a positive way. 

Texture is one of those things where it's a good idea to build up from a point of simplicity and not to go overboard with it. You can start by trying to find large shapes with major value changes and then start to get more detailed as you develop the textures further.

## Focus
But which objects should you give more texture than others? Well besides objects that are closer to the camera, you should give texture to objects that you want to emphasize more. Textures are another way to create contrast, just like shapes and colors, so a more textured object will stand out more than a less textured one assuming everything else about those objects are the same.

Generally the more detailed a texture is, the wider the value range and the more attention that object will demand. This links back to [Depth of Field](https://discord.com/channels/414295025883545600/1104656677678104650/1351282666166685726) and [Atmospheric Perspective](https://discord.com/channels/414295025883545600/1104656677678104650/1351282705790275784), since they’re both ways to control the viewer’s focus and make certain details less prominent.

# 2: Rendering Specific Materials

## Metals
There are many types of metals you can render, as well as different conditions and properties that change how you render them. You will need a different approach if you're rendering something like polished chrome compared to rusted copper.

**Reflective Metals**
Contrast and colors are crucial for reflective & polished metals, like silver and chrome. More reflective objects will have edges that look sharper against their environments.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1VgxUrDunO5nw9FADrjE0AlGBCVB7rOn2/preview?usp=drivesdk></iframe></div>

Obviously, curved surfaces like spheres will distort the reflections more, as you should recall from the last guide. The closer a reflection is to the edge of the curve, the more distorted it will get.

**Semi-Reflective Metals**
These aren’t as reflective as things like chrome, but will still have a decent amount of reflection to them. Often, objects will be less reflective due to wear & tear, provided they’re not regularly cleaned or polished. You can use the same principles for semi-reflective metals as you do with fully polished ones, just with less defined edges and less overall detail.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1aJNGfeKuIpC6LdAeAU6xtqFtdCNtdp7a/preview?usp=drivesdk></iframe></div>

**Rust**
Rust is an interesting part of metal texture because it’s very different from regular metal. It’s typically a coppery-brown color, but this can change depending on the metal. For instance, copper turns green as it oxidizes, instead of brown.

Rust occurs in areas that are exposed to water and moisture in the air. As a result, if you’re making a very dry area like a desert, there won’t be much rust from natural causes like the weather.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1Xew4jQG9zQv3JJ-T_t-3w-JZvLql4AEV/preview?usp=drivesdk></iframe></div>

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1Cf1h1yc1bj5FXdyAN5gXKFnTJcDSpmc-/preview?usp=drivesdk></iframe></div>

Looking at these two references, the main parts of rendering rust are the main patches, and the additional bleeding that occurs outside the main patches. There are smaller, darker patches of orange inside the rust, and smaller patches of rust outside the main ones as well.

With that in mind, I made a 10 minute drawing to simulate both of these parts of rust. This shows that you don’t even need much texture to give off a rusty look. If you want to develop your textures more, just look at the specifics of your references.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1sZpIY2ctspBBk3_4XL-CxvzS57hx7Ay8/preview?usp=drivesdk></iframe></div>

## Water
Water is another very reflective texture, like the reflective metals mentioned earlier. There are three water scenarios we’ll cover here, being flat water, slightly rippled water and wind/rain on water.

**Flat Water**
This is the easiest kind of water to render. It’s really similar to a flat piece of metal, so we can just use a similar approach to rendering a flat piece of metal. Even though it may not technically be flat water, water very far away can also be rendered with this approach.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1ptmjs5u7dZ0nBvZlSFaFlaLUmzXsssXY/preview?usp=drivesdk></iframe></div>

It's always important to know where the sun is, since it’ll impact how many details you can see under the water. This is thanks to the Fresnel Effect, as you should recall from the last guide.

**Rippled Water**
While rippled water is similar to flat water, there are more distortions which makes it slightly harder to render. The distortions warp the reflections with their shape, and they also make the edges of objects fuzzier the further away those objects are from the viewer. The more ripples there are, the less reflective the water will be.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1emHcV16rMh0s7y9baUwSs8_p5JJAekXN/preview?usp=drivesdk></iframe></div>

In this photo, you can see that the reflections are still similar to flat water, just with some distortion. The distortion that water causes for reflections is much easier to render than the distortion caused by a curved metal surface, for example. This is because of how the water moves on the surface. As seen below, the waves make lots of triangular and trapezoidal shapes. If you know this then figuring out how the distortions should look becomes much easier.

Often in stormy weather or places where ocean waves are really violent, the water will not be reflective at all. The more disturbed the surface is, the less it reflects, and violent waves disturb the water a lot which results in basically no reflection at all.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/177NbNfebA0Q_Yyj1SVKTyXE4yVsiSeHx/preview?usp=drivesdk></iframe></div>

The basic shape of waves are triangles with some added flow in their shape. More violent waves will have more white caps on them due to the waves breaking up. These white caps will be seen on the crests of waves, and form triangles and trapezoids in the troughs as seen here.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1ItwOPcDELc0b80Z5OGEZqChjla0NB_Oz/preview?usp=drivesdk></iframe></div>

## Glass
Glass can be interesting to render just because there's so much you can do with it. If it is a clear glass like a cup or window, then there's very little you need to render. If you’re making a window, then aside from the panes you can make it reflect the outside world. For any clear glass, you can define the shapes with just some highlights to the edges which is where the light can make it shine. This can be used for rendering objects like a drinking glass, such as this painting by [John Stone](<https://www.artstation.com/johnstone>).

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1h-NFsgDTUgFsPTOhybiBcCssFxllOD7X/preview?usp=drivesdk></iframe></div>

If the glass has a liquid like water inside, then it's important to know that objects behind it will distort. As always, it’s important to get references for the distortions. The glass will also have a shadow if there are liquids inside, most noticeably along the edges where light would be tangent to it - mostly due to the Fresnel effect again.

Anywhere that light passes through the glass close to a perpendicular angle will let light through, leading to a brighter spot in the shadow. This is the same way light passes through objects like magnifying glasses, and just like with those lenses, the light direction may change and focus into specific parts.

## Wood & Bark

**Tree Bark**
A common misconception about tree bark is its color. Most people will pick a color that's way too brown when making trees. If you go outside and try to take notice of the color of a tree trunk or a branch, you'll notice that bark is usually a very greyish green or orange.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1gTsgabOy1qZOO-6_QFb8gjERWpVycDro/preview?usp=drivesdk></iframe></div>

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1SRyEM29jVbCVelyKxBzMbEFgxZV11295/preview?usp=drivesdk></iframe></div>

Of course, there's more to bark than just the color. There are many types of trees, and different trees will have different ways that the bark goes around the trunk. A birch tree, for example, has a horizontal pattern instead of the regular vertical pattern.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1LdUcBverD94qcT-EfW6nVgewb5NMq9sD/preview?usp=drivesdk></iframe></div>

Bigger and older trees will have a less cylindrical shape than smaller and younger trees. This is very much useful in conveying the age and even the importance of a tree.

Take the White Tree of Gondor from the *Lord of the Rings* films. You can see how gnarled the tree looks. This gives a sense of how ancient it is and due to the context of its surroundings, you can infer that it has some kind of significance even if you haven’t been told what it symbolises.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1kGUfK9kHQTSnPA3C1MDdKZfO0UZhjGXD/preview?usp=drivesdk></iframe></div>

**Unvarnished Wood**
Once trees are cut into planks and boards, you’ll need a different texture for the wood on the inside. Unlike varnished wood, unvarnished wood isn’t reflective and usually has a paler, rougher look.

These four photos show the different ways that the wood grain can appear. Wood grain can be put into two different categories; open grain and tight grain. Open grain will have more value contrast, whereas tight grain looks much softer and has less overall contrast like the 1st image. You can also categorize wood grain by how much “straightness” there is; it’ll usually have straight lines with some “rings” scattered, or it’ll have far more swirls and rings in it, depending on how the wood was cut out.

-# *Straight, tight grain*

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1EiX6Ta4SaffMhYrIf6vuYJj4F3wuAN-h/preview?usp=drivesdk></iframe></div>

-# *Straight, open grain*

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1HFrpo3917BnREjdNHnx86LrdO78NTeTk/preview?usp=drivesdk></iframe></div>

-# *Circular, open grain*

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/11eaJmfnhVEbYaZuBWUYIdVctxXMq06mH/preview?usp=drivesdk></iframe></div>

-# *Circular, tight grain*

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1aMWoKnr8TSMFOTsUFATB-joGa4I_Ci42/preview?usp=drivesdk></iframe></div>

**Varnished Wood**
Varnished wood is very similar to unvarnished wood with just a few changes. The wood will look much more saturated and rich in color, and it will also be much more reflective. The increase in reflectivity means that it will pick up more colors from its surroundings and can even cast reflections of objects.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1DghcxwkWpmSlCCBaioWW3dqvd7q9PASb/preview?usp=drivesdk></iframe></div>

This was a quick study I did of an egg in the past. You can tell that the wood is reflective because the wood is both more saturated than the rest of the browns in comparison and also you can see that the egg has a reflection on the wood. Because it’s reflective, it is again important to use the Fresnel effect as that will change how any reflections look, as you can see in this next photo.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1jMKOwCPjiPSbInghsdSH11NT0uDxmaEC/preview?usp=drivesdk></iframe></div>

# 3: Rendering Texture Effects

There are many visual effects you can create with textures. This section will go over many of them.
## Subsurface Scattering
Subsurface scattering is the effect where light hits a translucent object, resulting in the rays of light bouncing all around the inside of the object. This effectively makes the object glow.

You can take the actual name of this effect to understand how it works. Subsurface means beneath the surface, so you can infer that the light scatters beneath the surface of an object. Subsurface scattering can normally be seen in bits of the skin such as ears, nose and fingers.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1exbyd1qr-PTYNTE14BaXMupETU6KetGd/preview?usp=drivesdk></iframe></div>

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1VAuuKgMfqQ-taDDkvr7Y0owHNGYz_sR9/preview?usp=drivesdk></iframe></div>

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/17V_DTDLwvmZRPNheQyhJzI73QUkpWqu5/preview?usp=drivesdk></iframe></div>

As you can see from the references, SSA that occurs in flesh bits are usually more saturated and have an orange glow that diffuses into a reddish color. This is mainly because of the blood we have in our flesh.

However, it is good to know that SSA can occur in other places like in plants or even water and clouds. These will have different colors which you can understand better with references.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1Miy2-5fnBtLFoTDtULsU6SDuya0nc9FV/preview?usp=drivesdk></iframe></div>

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1rbNvdvPZnNoxnpJM7bEJOAK6TeaxoKn2/preview?usp=drivesdk></iframe></div>

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1fhZtLPh6V_N-MSL4tHhokB6UUUfqV3_7/preview?usp=drivesdk></iframe></div>

## Depth of Field
Many cameras have an automatic or manual focusing feature, where they __focus on a specific area or object and blur the rest of the scene__. This is actually how our eyes work and the effect that happens is called **depth of field**. It is a hard thing to try and actively notice with your eyes as whenever you try to focus on the blurred part, it instantly becomes unblurred.

Depth of field is a useful thing to try and implement as it can help to control the viewers area of focus and to distinguish between what is important and what isn’t. Keep in mind that you don’t need your depth of field to only focus on one object or range; you can lower its strength and only use it on objects very close or far away from the viewer.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1wx4Omcbqmetvc6uSuKdNg3JvnvFqGsHd/preview?usp=drivesdk></iframe></div>

## Atmospheric Perspective
**Atmospheric Perspective**, sometimes referred to as Aerial perspective, is the __softening of details and contrast levels the further away objects are__ (normally in an open area with a sky). As objects recede away from the viewer or viewing point, they will become closer to the color of the sky, blending in a bit more and appearing less detailed. It helps to think of it as seeing objects through tons and tons of layers of air or fog.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1jWe_pNMolYPVxe_Hpbaq-TeJx95avVLH/preview?usp=drivesdk></iframe></div>

Take this screenshot from the game *Little Nightmares II*. You can clearly see that the buildings get less detailed, and beyond a certain point, the houses all seem to merge into a foggy haze that starts taking up the color of the farthest point.

Of course depending on the scenario, atmospheric perspective can and often will be much less intense, but it all depends on context. A strong atmospheric perspective with lots of haze can make it a whole lot gloomier but it also gives you an opportunity to focus on making sure everything else looks good. The viewer won’t care much about a point that doesn't convey lots of visual information and that isn’t where they should be focusing on.

## Fresnel Effect
The **Fresnel effect** is an effect in optics __relating the angle of incidence to the intensity of the reflection__. Fully understanding why this happens requires some physics, but not too much so do not worry.

The *2nd Law of Reflection* states that the angle of incidence is the same as the angle of reflection, which we measure with respect to the normal of the surface. The normal is an imaginary line that is perpendicular to its surface, and the incident ray is the ray of light that falls onto the surface. Therefore, the reflected ray is the same as the ray of light that is reflected from the surface.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/13Au7QLl6MTrnx69QOAzNPP69s8qtuGlm/preview?usp=drivesdk></iframe></div>

You can see here that the reflections on the water are much clearer near the edge of the pond. The water becomes more transparent the closer it is to the viewer, or where the angle of reflection increases until you can see the sand rocks beneath the water.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1BSdLEbGSz5sXKT04dQrKViTXt3fdyEy3/preview?usp=drivesdk></iframe></div>

It's good to know that almost everything follows the Fresnel effect, and not just reflective materials. Although most materials like leaves don't reflect very clearly, light still bounces off of it and therefore, when viewed at the right angle, some surrounding color might reflect onto them. This is how bounce light works if you recall the earlier guides.

<div><iframe src=https://drive.google.com/file/d/1j4XLRvNDn3fZcGzVo_dyZvaby6UPj7kj/preview?usp=drivesdk></iframe></div>

These three photos are of the same leaf, with just a change to the angle they were taken. You can see that the greens start getting bluer and reflecting the color of the sky.


## Sources

- Scott Robertson: How to Render, Chapter 10



## Credits
Created by @koma5 and @sku
