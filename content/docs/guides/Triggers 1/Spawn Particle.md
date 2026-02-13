---
title: Spawn Particle
weight: 321
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Tiny** (1-3 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- The Spawn Particle trigger lets you spawn particle objects at a group of your choosing.

{{< /callout >}}

** **
# 1: Spawn Particle

- **Particle Group:** The group of the particle object. This group can have multiple particle objects in it.
- **Position Group:** The position where you want the particle to be spawned at. Leaving this as 0 will spawn the particle at the position of the particle trigger itself. If this group has more than 1 object in it the particles will spawn at a random object with this group.
- **Offset X/Y:** Will offset the position of where the particles will spawn. 30 units = 1 block.
- **OffVar X/Y:** Creates a box around the “Position Group” in which the particle can spawn, the same as the “PosVar X/Y” options in the particle editor. 30 units = 1 block.

- **Rotation:** Changes the rotation of the particles that get spawned.
- **Scale:** The size of the particles that get spawned. This value is a multiplier, so particles with size 10 will appear as size 20 if you input "2" here.
- **Match Rot:** Will rotate the particles that get spawned with the object set at the “Position group”. So if the “Position group” was rotated 90 degrees clockwise, the particles that get spawned will also be rotated 90 degrees clockwise.

The +/- sliders next to “Scale” and “Rotation” is variance and will randomize their respective options’ values each attempt.

<div><iframe src=https://drive.google.com/file/d/1cLuyN1tQCa28qLF2SiodeL8LP5qRYMDx/preview?usp=drivesdk></iframe></div>





## Credits
Created by @koma5 and @naem
