---
title: Groups
weight: 304
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Short** (5-7 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- Group IDs (when placed on an object) can contain an array of features that can enable certain functions to take place.
- Parent IDs are available on many triggers, which allow further versatility when wanting to control a group of objects as their reference point.
- The editor’s pause menu includes four buttons (Re-Group, New GroupX, New GroupY and Build Helper) to assist you when attempting to re-assign an object’s group.

{{< /callout >}}

** **
# 1: The Basics

To add a Group ID to an object, you must select the object and click the “Edit Group'' button. Next, select an ID number to assign the object to (from 1-9999) in the box under the “Add Group ID” text, and finally click the “Add” button next to the input box. 

Clicking the “Next Free” button will automatically set the number in the input box to one that hasn’t been used by an object or referenced by a trigger.

Adding a group will show a button in the space below the input box with the corresponding Group ID number the object is assigned. To remove a Group ID, simply click on the numbered button of the ID you want to remove.

The button showing the ID will be colored differently based on certain conditions:
- **Light Gray:** All selected objects have that Group ID.
- **Navy:** Some selected objects have that Group ID.
- **Pink:** One of the selected objects has a Parent ID (will be discussed later in the guide).

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1O9BZ4WCvpwCEqjb0XNcULkQLNYoD6SEf/preview?usp=drivesdk></iframe></div>

You can copy the groups an object uses by clicking the “Copy” button in the top right corner of the “Edit Group” menu and then clicking the “Paste” button below while selecting your preferred object(s). 

Group IDs are also copied when you copy an object's values using the “Copy Values” button and then pasting the state onto other objects. This can be disabled by turning on the “Disable Paste State Group” setting in the settings menu on the pause screen.

*If you have the “Show Object Info” setting in the pause menu enabled, you can see what groups an object or group of objects have by selecting them.* The Group ID numbers will appear under the “G:” section, and like with the button colors in the “Edit Group” menu, different symbols mean different things about the group:

- **Just the number:** All selected objects have that Group ID.
- **Number in parenthesis:** Some selected objects have that Group ID.
- **Number with an asterisk:** One of the selected objects has a Parent ID.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1b6xuZqWuzrymS_31vkoYfopzd2nuniyy/preview?usp=drivesdk></iframe></div>

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1029e75lV4bK6p75PBA8lMsll1DV6deXJ/preview?usp=drivesdk></iframe></div>

# 2: Reassigning Groups

If you want to reassign an object’s group, there are four buttons in the editor’s pause menu that can help.

## Re-Group

Changes all Group IDs that are referenced in another object or trigger to the next free group.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1mp370ffCtAmKf6jwHB9U-AKGl6pzZs2_/preview?usp=drivesdk></iframe></div>

## New GroupX

Adds the next free group to an object or group of objects, with the order of objects getting the IDs going from left to right in x-position. If two or more objects are in the same x-position, the bottom-most object gets the highest Group ID, and IDs are then distributed from lowest to highest values with the order of objects going from bottom to top.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1mB1CrG36NFsFOAF0FdgbfwtQBoQVO0Oo/preview?usp=drivesdk></iframe></div>

## New GroupY

Adds the next free group to an object or group of objects, with the order of objects getting the IDs going from bottom to top in y-position. If two or more objects are in the same y-position, the left-most object gets the highest Group ID, and IDs are then distributed from lowest to highest values with the order of objects going from left to right.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1-1Er8NrNnSO2YgTF-FARj7lI7x3MdGbI/preview?usp=drivesdk></iframe></div>

## Build Helper

This takes paired groups from objects/triggers and then replaces them with the next free group available. *The object and a trigger need to be selected in order for this feature to work and the trigger must hold a group held by the object* (groups that are not present in both the trigger and the object(s) will not be affected).

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1_6N9t5S78iMuVG5CUwZ9WPSYddIZ6cEB/preview?usp=drivesdk></iframe></div>

# 3: Parent IDs

Parent IDs (also referred to as Group Parent IDs) are special IDs given to one object in a group that is able to link the objects in that group together, with the object of the Parent ID being the reference point.

*Only one object can have a Parent ID per group.* If you give an object a Parent ID while a different object has that Parent ID, it will reassign the Parent ID to the new object.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1MoAp-CFPQr0xDBy6Lj4Ymy-oW0LQMeRE/preview?usp=drivesdk></iframe></div>

# 4: Triggers That Use Parent IDs

## Move :Move: 

Utilizing the target or direction mode, using the same TargetPos Group ID as the Parent ID object will make the moving group target that object. Note that the Target Group ID (the object being targeted) and the TargetPos Group ID (the target of the moving object) must be different.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1wiKbKMrtZAV6LdgAaEJ1daWhJmxAKoVC/preview?usp=drivesdk></iframe></div>

## Rotate :Rotate: 

The Parent ID object can be used to set the center of a rotating group. Note that the object will rotate around itself. Using aim or follow mode will make the rotating object target the Parent ID object. *Note that the Target Group ID and the Rot Target Group ID must be different.*

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1WhQhBLsA_n4I2CHuitfznGhdnRSydLIn/preview?usp=drivesdk></iframe></div>

## Scale :ScaleTrigger: 

The Parent ID object will be the reference point of the scaling group, meaning objects will scale towards or away from that object. The Parent ID object itself will scale around itself.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/16tduL2OeLfMd2jWwRFO8__cUIOaOmp7X/preview?usp=drivesdk></iframe></div>

## Keyframe :KeyframeTrigger: 

The Parent ID object will be the center for any rotating or scaling.

## Setup Keyframe

The Parent ID object will be used as reference for the center of the Preview Art option. Parent ID is also used to mark the starting keyframe.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1Jpm0E300QlrAzMeqGP1HjsGitupVVIEj/preview?usp=drivesdk></iframe></div>

## Advanced Follow :AdvancedFollow: 

All objects will be linked to the Parent ID object, with that object being the target and reference for the trigger.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1iyi6lZYCn-RFM7vMYM_rKN8siwH_1ZGU/preview?usp=drivesdk></iframe></div>

## Area Triggers :AreaMove:

All objects in the group will be affected in exactly the same way as the Parent ID object. Basically, the group objects are linked to the Parent ID object instead of being affected individually.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1-FFdxjlo-us3ULjPTBQ3AznVDgrGFB8q/preview?usp=drivesdk></iframe></div>

## UI :UITrigger: 

The Parent ID object will be used for the UI Target for reference in the UI.

<div><iframe src=https://drive.google.com/file/d/1PQ5kUhZ7jxQVOZ2VhYJQ0I839RmV4h1v/preview?usp=drivesdk></iframe></div>

*Concerning the Spawn Particle, Static, Edge, Song/Edit Song/SFX/Edit SFX (proximity targets), End, Gradient, and shader triggers w/ target: The Parent ID object will be used as the target.*





## Credits
Created by @Madzz and @TDP9
