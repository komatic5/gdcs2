---
title: Advanced Movements (2.1)
weight: 621
draft: true
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Short** (4-6 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- Many trigger setups let you use movements in unique and interesting ways.
- Target Tracking, Movement Tracing, and Vector Rotation are three such ways to use movements in more interesting ways than the normal Move trigger can provide.

{{< /callout >}}

** **
# 1: Movement Tracing

Movement tracing is useful to create complex or precise shapes, primarily for decoration. The best way to make these complex shapes is to plot out points which you can connect using various objects, and move triggers are the easiest method of accurately creating these shapes. 

However, it is difficult to precisely plot points along a move trigger’s path unless you have a method like Movement Tracing. This lets you automatically plot points on an object’s movement path, and is fairly easy to use.

The initial [setup](https://cdn.discordapp.com/attachments/921535634475212811/1126635016206696488/RPReplay_Final1688663399.mov) takes two groups, but the more points you wish to plot, the more groups it’ll take.

1. Place one object and have it move along your intended.
2. Use multiple Follow triggers to follow that object. You can either manually adjust the durations for each Follow trigger, or give them all the same duration and space them out horizontally.

# 2: Target Tracking

If you’ve ever used the Move trigger’s “Use Target” feature, you may be aware of a major limitation it has. Use Target will [not update](https://cdn.discordapp.com/attachments/921535634475212811/1126635842648166491/RPReplay_Final1688663475.mov) an object’s movement if you move the target during the movement.

Target Tracking allows you to roughly approximate a system which lets you continue to track that object through space. It costs 4 groups to [set up](https://cdn.discordapp.com/attachments/921535634475212811/1126635044887351377/RPReplay_Final1688663700.mov).

1. Create a fast loop, like a Spawn loop with low delay or a Collision loop. Make this loop target a Move trigger with Use Target enabled.
2. Place a Stop trigger which targets your Move trigger. Use another Spawn or Collision trigger to make it activate just before the Move trigger does – so if you use a Spawn loop with 0.04 delay, have it activate 0.03 seconds after the loop iterates.
3. When you wish for the tracking to finish, break your loop. You may use a final Use Target trigger to move your object to the precise location.

Target Tracking lets you create things like [Bezier curves](https://cdn.discordapp.com/attachments/921535634475212811/1126635071701532814/RPReplay_Final1688663965.mov) if applied properly. However, it may have minor delay depending on your device, and it isn’t best for a system that requires a constant speed. I suggest using the Exponential Out easing and making the duration of the Use Target trigger ~1.3 times longer than you actually wish for the final setup.

The [most accurate version](https://cdn.discordapp.com/attachments/1108884718440693850/1126654865259642940/Geometry_Dash_2023-07-06_19-23-19.mp4) of this uses a frame counter, a continuous move loop which slows down a bit over time, and a third group which follows your tracking object with twice the speed. Your final tracking object will track the object in this third group with the Ease In easing. I’ve created a copyable setup of this which you can access at the ID `94985965`. This setup uses 10 groups to work.

# 3: Vector Rotation

This last setup is a bit less useful than Movement Tracing and Target Tracking, but it is still somewhat interesting. To put it simply, it allows you to treat a movement as a vector, and rotate that vector by any angle.
## Use Target Method

This method costs two groups to [produce](https://cdn.discordapp.com/attachments/1108884718440693850/1126656428103434270/Geometry_Dash_2023-07-06_19-29-13.mp4), and works smoothly with all easings.

1. Make a setup to use a Move trigger with Use Target.
2. Rotate your Target Position object around the Target Group instantly, just before the Move trigger activates.

## Rotation Method

This method lets you rotate vectors by using Rotate triggers. It is not useful for conventional uses, but it does allow you to translate a player’s Y-axis movement into horizontal movement on the X axis. This only costs 5 groups and leads to some interesting gameplay gimmicks, like what I did here.

{{< youtube 3csPWAJ7cRM >}}

1. Set up your first movement. Then, set up a follow trigger that reflects this movement in the opposite direction – it should have X and Y mods of -1.
2. Use two rotate triggers to target the same object (see the Stacking guide to understand how this works). Make their rotation values 60 and -60 degrees respectively, and make their easings identical to your first Move trigger’s. Your object will now move perpendicular to your original movement.
3. If you want to get a movement that isn’t just perpendicular, you’ll need to use two Follow triggers. One will copy the X and Y mod values from your first movement, and another will copy them from your perpendicular movement. You’ll need to use the Unit Circle and some trigonometry to determine the best X and Y mod values for your new angle.

Here's a [video](https://cdn.discordapp.com/attachments/1108884718440693850/1126657505355903036/7_VectorRotate2.mp4) of this first setup.

4. To translate the player’s Y position into horizontal movement, make your first movement a Follow Player Y trigger. Make the second movement another Follow Player Y trigger, but with a very small delay (such as 0.02).
5. Then, do the same rotation trick from step 2. This time, use a much higher rotation value - I recommend using values so you get about 5 full rotations per second. To get the most accuracy, place another Follow trigger and have it target your perpendicular object; set the X mod to 2.40, and the Y mod to 0.

Here's a [video](https://cdn.discordapp.com/attachments/1108884718440693850/1126658528367628388/8_TranslatePlayerYtoX.mp4) of this being fully applied.





## Credits
Created by @koma5
