---
title: Making Duals
weight: 421
draft: true
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Medium** (10-12 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- The Dual gamemode lets you play as two icons at the same time.
- There are three types of duals: symmetrical, asymmetrical and 2-player duals.
- Duals allow for more interesting gameplay, as you have a lot of room for customization, experimentation and mix ups.
- You can use different gimmicks to spice up your dual gameplay.

{{< /callout >}}

** **
Dual is a unique gamemode that opens up a slew of new gameplay ideas and mechanics. In this guide we will go through each important mechanic, explain how it works, and how to set it up effectively.

# 2: How Duals Work

Duals function much the same as single gamemode play. The moment you enter the dual portal, _two icons will appear, and both icons will react when you click_. By default, each icon’s gravity is the inverse of the other; that is, one icon has normal gravity while the other one has inverted gravity. Also, when one icon changes its gravity, the other will automatically do as well. This gravity dependency can be changed, but that will be discussed in a later section. 

Now, the two icons don’t need to be on the same gamemode necessarily, *each one can be a different gamemode as well!* This is where the real fun starts when building duals. This also means that each icon can now have its own independent gravity. For example, you could have a ship and cube dual where both icons can have the same gravity, but you could also have two cubes in a dual where they have opposite gravity of each other. Do note however that only cube and wave still share their gravity because Robtop somehow coded it that way. All other gamemode combinations will have independent gravity.

# 3: Dual Types

## Symmetrical Duals

**Symmetrical duals** refers to _dual gameplay where both icons follow the same path and are the same gamemode_, meaning that the bottom icon and top icon mirror each other’s movements. An example of this can be seen at 28-43% in Verdant Landscape by Nisha. This is the easiest form of dual gameplay to build, as most of the time you only need to create gameplay for one icon and then copy paste this gameplay for the other one.

{{< youtube dSbox0NKuXs >}}

## Asymmetrical Duals

**Asymmetrical duals** refers to _dual gameplay where each icon follows its own path_. You can make this either where both icons are the same gamemode or different ones. It is easier and more common to use different gamemodes, because that way there is more versatility in what you can do. An example of this can be seen at 34-43% in Diligence by Davphla and more. You can see the icons are sometimes different gamemodes and sometimes the same, but follow different paths.

{{< youtube OyWM-uXuuqU >}}

## 2 Player Gameplay

**2-player mode** is a configuration you can enable in your level settings that _allows each dual icon to be controlled independently of each other_. Also, with this setting enabled, the icons will always have independent gravity, no matter the gamemode the icons are in.

The 2-player mode is mostly used for minigames that require multiple inputs, especially in 2.1. For instance, levels like Floating Outskirts by YoReid, Area Tracer by GDvesuvius, and Geo Kart by Incidius utilize this mechanic. 
You can also use 2 player controls in a more conventional way and make (a)symmetrical duals if you don't fancy yourself a trigger person. An example of a level like this is Codependence by TCTeam, where each icon is controlled individually.

{{< youtube lYswi_4FrcM >}}

{{< youtube GuDam2WUoNs >}}

{{< youtube kZzp_QeahS0 >}}

{{< youtube ti5G-c3wcM0 >}}

# 4: Building Dual Gameplay

Now that we have gone over the basics of the 3 main dual types, it is time we go over how to build dual gameplay. 

Building **symmetrical duals** is easy; you just have to mirror the bottom/top icon’s gameplay to the other side/icon, as discussed before.

When building **asymmetrical duals**, it is important to keep in mind that you don’t have to focus on building two gameplay paths; choose to build one for the main icon, and as you go along, build gameplay for the other icon but don't focus too much on it. If you do, you will find that your gameplay becomes difficult to sightread/play/build because you have to constantly switch your focus of what icon you need to look at. This is why it is best to build gameplay for one icon and let the other just float along. Still, remember to put in enough effort into the other icon’s gameplay so it feels like it serves a purpose and isn't there for the sake of being there.

Another way to make the second icon feel useful, is to switch focus between the icons. There are many ways of doing this, such as having player 1 move to the top or bottom of the screen while player 2 moves to the middle, where your focus usually lies. Transitioning between the two may be difficult at first but over time as you build more duals it will become second nature.

For **2 player duals**, you essentially can build 2 different levels in one. The only restriction is screen space, but this can be changed and will be discussed in the dual borders section.

In the example below you can see that if you only focus on the ufo, you will pass the part just fine, as the cube just has its own gameplay that virtually plays itself.

None

# 5: Dual Borders

By default, the dual gamemode is 9 blocks tall. This distance can vary depending on what gamemode the icons are, and if they are currently on the same gamemode or not. Ship, Wave, UFO and Swing change this height to 10 blocks and the rest stay as 9.

None

Now, having such little space can be restricting, which is why you can use the camera zoom trigger to expand these borders as much as you want. Portals also have this very cool feature called **Free Mode** found in the Edit Object menu. If you enable this option, *the dual borders get completely removed*, allowing you to build duals with no mind to any border restrictions you would have encountered.

Note that if you enabled Free Mode on a dual portal, *you also need to do this for every gamemode change within the dual as well*, otherwise the borders will come back again. Also note that when using Free Mode, the camera will always follow player 1. If you want the camera to follow player 2, you will need to use an Advanced Follow trigger to lock an object to player 2, and then use a static camera trigger set to follow that object.

# 6: Offset Duals

In update 2.1, if you wanted to separate the two icons in a dual across the x axis, you needed to use a bug.There were several ways to do it, all of them meticulous to set up; one method even required hundreds of slopes to separate the duals.

Now with the Teleport trigger, unlinked Teleport portals and the Teleport orb, you can create this setup very easily across any speed you want to anywhere in the level. You can also use a spawn loop, where you constantly teleport player 2 to an object using a Teleport trigger. By moving around this object, you are essentially controlling where player 2 goes as well. This is mainly used for visuals though, such as Angel GD’s part in Resonance hosted by Human.

{{< youtube gNeCvicI6CA >}}

## How to Build Offset Duals

The process of building offset duals is much the same as building asymmetrical duals. Focus primarily on one icon while the other one lingers around, occasionally shifting your attention between them. This is a bit harder to pull off correctly; since one icon will be either in front of or behind the other one, you need to make the switch not feel jarring or sudden. One way to do this is by creating a small auto part for both icons and doing the switch there, or by making the gameplay be slightly easier.

As you can see in the example below, the focus starts off on the bottom icon so the top icon can teleport without ever obstructing your playing experience or feeling overwhelming. Then, when both icons hit the spider orbs at the same time, there is a long wait so you have enough time to move your focus to the other icon being the ball, allowing you to time the clicks and the teleport orb correctly. After the icon teleports again, you can either keep your focus on the same icon or switch back to the first, as the part allows for that kind of mental gymnastics.

None

# 7: Advanced Dual Gimmicks

With the introduction of the Options trigger, Gravity trigger, Teleport trigger and Arrow trigger, you are able to do stuff with duals that weren’t previously possible. You can for instance:
- Give each icon independant gravity even if they are in the same gamemode.
- Disable one or both of the player’s controls.
- Make one player go in reverse.
- Change the fall gravity of an icon.

At first these gimmicks may not seem useful, but once you start experimenting you will see how helpful they are for creating advanced duals.

## Control Gimmicks 

Starting off with **Unlink Dual Gravity** on the second page of the Options trigger, this does exactly as it says. _Each icon has its own gravity irrespective of if they’re the same gamemode or not_. This is a small change but opens up the possibility for more gameplay using the same icon.

None

Next is **Disable Controls P1/P2** on the first page. These two options do as they say and _disable the controls for either icon_. When used wisely, this opens up enormous potential for gimmick duals. For example, you could disable the controls of one icon and use it only for sync purposes. You could also switch between two icons such that if one falls off the screen, the other enters; disabling the controls gives you precise control over transitions between the icons.

None

## Direction and Gravity Gimmicks

Duals really start to become interesting when you make one icon go in reverse or have different gravity to the other.

Let’s discuss **gravity** first. You can give player 1 and player 2 different gravity values using the Gravity trigger. Since the two icons can have independent gravity values, this opens up a lot of room for experimentation. You could for example have one icon fly along the screen with low gravity while the other one has regular gravity and is the focus of the gameplay, or you could make one icon mini but let it have lower gravity to bring it closer to the jump height of a regular sized icon.

*In the second video, start from 0:19.*

None

To make one icon go in **reverse** in respect to the other one, the icon needs to hit a Reverse pad or orb; *anything else will affect both players*. It is recommended to reverse player 2, as the camera is by default tied to player 1. If you reverse player 1 you will end up with pretty goofy camera behavior, unless that is your intention in the first place.

None

Finally, let’s talk about **Arrow trigger gimmicks**. Combining duals with the Arrow trigger is the most complicated gimmick here due to the setup and the fact that the icons are moving in different directions.

In order to have a dual where one icon moves vertically, you will need a vertical arrow trigger to be activated before the player enters a dual portal, that way the second icon remains on the original trajectory. You are able to do this with any gamemode, but wave is used a lot more for its consistency.

None

Working with this gimmick is quite complicated due to them going in different directions, so you will need to use Teleport triggers/portals if you want both icons to appear on the screen. What is wonderful about this gimmick is that you can use reverse pads or orbs without breaking the gameplay rotation on the icons, opening up a whole lot of different new ideas. This can be seen in the second example below, where the ship is completely unaffected by what the cube is doing.

Probably the most popular level that uses Arrow trigger duals is Out Of This World by Perox08. Another example but with different gamemodes is [Magic Touch](https://cdn.discordapp.com/attachments/1195352304136749087/1281069228962873416/youtube-KW7tPgRYz0M.mp4?ex=66dc5a71&is=66db08f1&hm=37759352e73db15d5b7fe9696955eba13905b6887f8e825496e2f4be8b01ab68&) by DawuU.

{{< youtube 9AuptH4fElM >}}





## Credits
Created by @ChuckOlate and @naem
