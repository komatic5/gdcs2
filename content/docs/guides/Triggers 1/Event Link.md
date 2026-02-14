---
title: Event Link
weight: 338
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Tiny** (1-3 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- The Event Link trigger is used to detect player inputs and activate a group based on what the player does.

{{< /callout >}}

** **
The Event Link trigger :EventLinkTrigger: spawns a group if certain conditions are met. It allows you to detect up to 6 player inputs for building a controller. Before 2.2, we had to rely on quirky setups that were 3 times less efficient, but now we can achieve much more using only a few groups and little to no effort.

*NOTE: Event Link ONLY works as a Spawn trigger, not a Toggle trigger.*

None

Its features are as follows:

- **Group ID:** This is the assigned group that will activate once a certain action takes place.
- **Extra ID:** Activates if the player interacts with a corresponding object that matches its Material ID. You can set an object's Material ID in :EditGroup: -> Extra2.
- **Extra ID2:** Useful If you want to use the 2 player mode in order to access all 6 different inputs.
 - 0 = Can be activated by both players
 - 1 = Activated by P1
 - 2 = Activated by P2
- Select Event Menu:

None

In the top right corner of the menu, there's a tablelist button that leads to another menu.

This menu lets you determine which action needs to occur in order for your GroupID to activate. Fortunately, each checkbox has an explanation next to them so feel free to explore.

Now that we know how the Event Link Trigger works, we can make some contraptions

Here is an example of what you can make with this trigger:

{{< youtube q_29LgSGSM4 >}}

In this particular level, the player always moves forward at a certain speed. By pressing a corresponding key we either turn left or right. Upon pressing W or ^ we dash forward. This trigger is also used at a start to choose between different set of controls: **A W D** or **< ^ >**.





## Credits
Created by @EYZ and @Selena
