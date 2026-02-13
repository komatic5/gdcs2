---
title: Advanced Follow
weight: 312
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Short** (9-11 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- The Adv. Follow trigger allows you to create more complex movements for objects that regular Follow triggers can't do.
- The trigger is split into 3 separate triggers which allow for more freedom.
- It contains three follow modes which change the behavior of the objects.
- The trigger is stackable, which means multiple triggers can affect the same objects.

{{< /callout >}}

** **
# 1: Basics

Advanced Follow is split into three triggers:  **Advanced Follow**, **Edit Adv Follow**, and **Re-Target Adv Follow**. *Note that the last two triggers require an active advanced follow in the level to function.*

Active Advanced Follow triggers persist even when toggled off. To stop them, you need to use a Stop or Pause trigger. This also applies to Edit Advanced Follow and Re-target Advanced Follow triggers targeting an active Advanced Follow trigger.

The +- sliders adjust variance, adding or subtracting a random value between 0 and the input number for each attempt, including respawning at a checkpoint in platformer mode.

As with Area triggers, you can use "Group Parent" on an object and link it to others to apply the effects of one Advanced Follow trigger to many sets of objects in that group. This can give more control than using a Parent ID object.

# 2: Advanced Follow

This trigger is the one you use to set up the initial movement and other settings to your liking. 
## First Page - Basic Setup

- **Target GID**: The target group which follows another specified group. It can have as many objects as you like. 
- **Follow GID**: The group which the Target GID follows. This is a one-object group. In a sense, it's the “center” of the trigger. 
P1, P2, and C are special centers which are respectively assigned to Player 1, Player 2, and the bottom left corner of the camera. 
- **Priority:** Sets the order in which movements are applied if an object is targeted by more than one advanced follow trigger. 
- **Exclusive:** Turns the trigger into the only one that can affect the target object(s). This cannot be changed by other advanced follow triggers. 

The video below demonstrates how Exclusive works. To start off, you can see that the first advanced follow trigger has exclusive turned off. When I touch the second trigger, the spike moves faster due to MaxSpeed stacking. However, when Exclusive is enabled, activating the second trigger doesn't stack the movements.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1JtUGcV8ir84QhkXEbY3AYyiUYz8utseQ/preview?usp=drivesdk></iframe></div>

- **X Only/Y Only**: The objects will only consider the X or Y position of the Follow GID. 
- **Rotation Offset:** Offsets the object rotation in degrees. Positive values rotate to the right and negative to the left. Zero is upwards. 
- **Ignore Disabled:** The movement is disabled if the target objects are toggled off. 
- **Rotate Dir**: Makes the objects rotate to face the target. Once they reach the Follow GID, they turn upright.
- **Rotate Easing**: This applies easing to the object rotation, making it rotate towards the target slower. 
- **Rotate DeadZ**: Adds a dead zone for the rotation of the objects.

**Init**, **Set**, and **Add** only work with follow types 2 and 3 and only affect **Startspeed** and **StartDir**.

- **Init:** With this option, the values are used only when the object has no speed (i.e. acceleration is 0). This will make the target objects move in the direction set in “StartDir”.
- **Set:** Overrides any current object velocity. 
- **Add:** Adds the velocity to the object's current velocity.

The **Pre** button allows you to choose ready-made presets. There are only two currently, but more may be added in the future.

## Second Page - Follow Modes

You can see what mode you're currently on and change the modes by selecting the 1/2/3 buttons in the top right corner. 
## Mode 1: Standard Follow

- **Delay**: The time in seconds an object waits before following the target. 
- **MaxSpeed**: The fastest speed the objects can move towards the Follow GID. 
- **MaxRange**: the maximum distance the Follow GID has to be from the Target GID for it to move toward the. One block is 30 units with 0 being at the object’s or structure’s center. 
- **Easing**: Adds easing to the start and end of the movement. Uses the “Ease in out” easing type. 

The box next to the max range is the **Range Center ID**. Normally, when you set a MaxRange the target GID(s) will use their own center or the structure’s center. Entering a group into this box will set the group as the range center. *This is also a one-object group.*

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/10jjGhg6Q-5uL_UZhG7V_OYD7WBEPT3_3/preview?usp=drivesdk></iframe></div>

## Mode 2: Accelerated Follow

In this mode, you can edit how objects move based on their distance from the Follow GID. 
- **Startspeed:** The speed the objects have when they start moving.
The box next to this option is its multiplier. For example, inputting `2` will double the current speed of the target objects. 
- **StartDir**: The direction in degrees the objects face when RotateDir is enabled and move toward when they start moving. Positive values shift to the right, negative to the left, and 0 is straight up.
The box beside this option allows you to input a singular object's group. The target objects will then rotate towards it. 
- **Acceleration:** Sets the objects’ acceleration. They will continue to accelerate until the max speed is reached. 
- **Friction**: The friction applied to the objects as they move. 
- **NearDist:** Sets the distance for which objects are considered near the target. *Note that one block is equal to 30 units.*
- **NearFriction**: The object’s friction when it  near the target. What counts as near is configured by the NearDist value.
- **NearAccel**: The object’s acceleration when it moves near the target. What counts as near is configured by the NearDist value.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1d79gq2b0mIICYiEVB0QxMLXQYix2ddFC/preview?usp=drivesdk></iframe></div>

## Mode 3: Complex follow

Unlike the previous modes, this follow mode has 2 pages of settings and is much more configurable. 
- **Steerforce**: The force applied when the objects steer (turn) toward the target. 
- **SpeedRangeLow:** sets the Target GID’s speed range to be considered low.
- **SteerForceLow:** Sets the Target GID’s steer force when it’s below the speed range set in SpeedRangeLow.
- **SpeedRangeHigh**: Sets the Target GID’s speed range to be considered high.
- **SteerForceHigh:** Sets the Target GID’s steer force when it’s above the speed range set in SpeedRangeHigh.

- **SlowDist:** The distance from the Follow GID that is considered slow, which applies the SlowAccel setting. One block is equal to 30 units. 
- **SlowAccel**: The object acceleration when inside the SlowDist distance from the Follow GID.
- **BreakForce**: The force at which the objects brake when the Target GID moves in a different direction.
- **BreakAngle**: The angle at which the objects will brake. 0 is the direction of the movement and goes clockwise until you reach 180,which is the opposite direction of the current movement. 
- **BreakSteerForce**: The force at which the objects steer while braking.
- **BreakSteerSpeedLimit**: The max speed at which the objects can steer while braking. 
- **TargetDir**: This is a checkbox on the 3rd page. This makes the target object choose a random direction to steer toward instead of always steering towards one direction when passing the Follow GID. Also influences the object’s rotation when RotateDir is enabled. 

The upper checkbox on page 3 is to enable the SteerForceLow and SpeedRangeLow sliders, while the one on the bottom is to enable SteerForceHigh and SpeedRange High. If you don't enable these checkboxes, their respective options won't apply their settings.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/14iZh9KyaphdC9rlHBm5tB2YLGQpr_68B/preview?usp=drivesdk></iframe></div>

# 3: Edit Advanced Follow

This trigger lets you edit certain properties of an active advanced follow trigger temporarily. This only works when follow type 2 or 3 is selected. However, you can’t customize the duration of this trigger's effect. 

- **Target GID**: The Group ID of the objects that you want to edit the movement of. This group is the same as the one specified in the Target GID box in the normal advanced follow trigger. 
- **X Only/Y Only**: Makes this trigger affect only the X and Y movements. 
- **Mod X/Mod Y**: Modifies the speed on the X and Y axes by multiplying with the value you input. 
- **Speed**: Modifies the speed of the object’s Y movement. The object will move up when the trigger is activated. This direction can be edited by the Dir setting. If it’s 0 it gets ignored. 
- **Dir**: Modifies the movement direction in degrees. 0 is straight up, positive values rotate to the right, and negative to the left. 
- **Target Control ID**: Allows you to target a specific group ID when using remapping. For example, if you remap a Spawn trigger to use group IDs 1, 2, and 3, and you need to target 3, you can enter a Control ID after enabling the option in the trigger, and input the control id in the upper box. You can find the Control ID option in Extra 2 after clicking Edit Group with the trigger selected.
*Note that Control ID may not appear in Extra 2 due to a possible bug, but this may be fixed in the future.*
- **Redirect Dir**: Redirects the direction towards a reference object, whose group you input in an input box towards the bottom right.

In this video, there are 3 edit advanced follow triggers. The first one accelerates  the spike toward the top of the screen. This can be changed by setting an angle in “Dir”.

The second trigger does the same as the first, but now a small triangle is set as the reference object. You can see the spike move towards it instead of the top of the screen. You can still offset this by using “Dir”.

The third trigger modifies the XY movement of the spike by flipping its direction using the X and Y mods.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1P1yn-GC7M4PUpqcWdzmLaHJoI_f3a1yi/preview?usp=drivesdk></iframe></div>

# 4: Re-Target Advanced Follow

The third and final trigger allows you to change the Target GID of an active advanced follow trigger. 

- **Target GID**: The group id of the trigger you want to re-target.
- **Follow GID**: The Group ID of the new target. You can choose from the buttons below for special centers P1, P2, and C which are player 1, player 2, and the bottom left corner of your screen respectively. 
- **Target Control ID** in this trigger is the same as the option in Edit Advanced Follow. 

In this video, you can see the particle trails collide with the player, re-target themselves, and move toward a stationary particle object near the beginning of the level. Upon colliding with that particle they get re-targeted again and move toward the player.

<div><iframe src=https://drive.google.com/file/d/1VEMzaoCHrMbmk-gZ1kTYTAXxg3OseF0G/preview?usp=drivesdk></iframe></div>

# 5: Stacking

Advanced follow triggers are stackable. Activating two at the same time, or one after the other adds the values together and the object will receive a stacked movement. *Note that triggers with different follow types cannot be stacked.* It's simply ignored.





## Credits
Created by @etherail and @naem
