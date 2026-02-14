---
title: Optimizing
weight: 519
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Tiny** (2-4 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- Optimizing refers to reducing the amount of objects used without affecting appearance, important for creating less lag when playing levels.
- Some important efficiency skills to include are overlapping objects, using scaling (scalehacks), and using certain object archetypes to achieve something in a conservative manner.
- Reducing objects can be done by creating a second copy of any group of objects that need to be optimize and using efficiency skills to reduce object count.

{{< /callout >}}

** **
**Object Efficiency**, or **Optimization**, refers to decreasing the object count while keeping the visuals the same. This is important because poor optimization can often make levels far more difficult to play, and much more laggy. In this guide, we'll go over how you can optimize your decoration.

**1: Efficiency Skills**

There are many techniques you can use to make your object use more efficient.

> **Overlapping** objects is usually the easiest way to optimize. You simply delete objects which are fully covered by others. This works best on decoration that utilizes many layers.

> **Scaling**  is another simple way to reduce object counts. By making one object take up more space, you can use far fewer objects to fill in a space. Note that this is much easier with scale hack.

*Warning: GD renders large objects differently depending on their hitboxes. Be careful with this because it can cause visual errors.*

> **Object Types** are the strongest way to efficiently optimize, although using them requires experience. Essentially, some objects can be sufficient to maintain similar quality with far lower object counts. These objects will depend on what you’re trying to do with the objects.
>
> For example, you can get away with using the wood objects in the 1st and 9th tabs instead making your own custom wood. In general, be aware that custom assets will always be more inefficient than using default objects, which include things like custom curves.

**2: Reducing Objects**

This is an algorithm which lets you reduce object counts without affecting the overall look of the deco. If applied properly, you can use half or even one-third of the prior objects, without impacting the visuals much at all.

> **1.** Make two copies of the deco you want to optimize. Unlink all of the objects if necessary.

> **2.** Using the “All” layer, remove all objects that don’t show up above others.

> **3.** Disable Preview Mode and go through each layer. Use scaling and object types to reduce object counts for filled-in shapes.

Note that this works significantly better if you use a lot of Editor layers. This will help you stay organized and makes the layering task less tedious

Here is an example of this process. This video shows all of the efficiency techniques, as well as the object reduction algorithm.

{{< youtube NMwzuKoi3Nk >}}



 **Research** and **Examples**

  @koma5

**Proofreading**

  @C4

