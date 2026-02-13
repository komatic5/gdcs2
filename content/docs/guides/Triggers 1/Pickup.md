---
title: Pickup
weight: 343
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Tiny** (2-4 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- The Pickup trigger lets you modify the value of an Item ID. Its checkboxes give you more control of how you modify it.
- The Counter object lets you display the value of an Item ID.

{{< /callout >}}

** **
# 1: Item IDs & Pickup Trigger

**Item IDs** __essentially store numbers__. If you want to change the value of an Item ID, set a pickup trigger to target it then change the value in the “Count” box.

The :BluePlus: button lets you select the next free Item ID.
There are three checkboxes within the interface of the pickup trigger that you need to know.
## Multiply
Enabling the checkbox “multiply” will cause the “count” to be t replaced by a slider, which will enable you to multiply the number that you’ve set on the slider (decimals won’t work).
## Divide
Enabling the “divide” checkbox will cause the “count” to get replaced by a slider, allowing you to divide by the number that you’ve set on the slider (decimals won’t work).
## Override
Enabling the “override” checkbox  will allow you to set that value to the “count” (e.g., if the value in item ID 1 is 10, an override pickup trigger with 2 on the counter, it will set to 2, if you place an override pickup trigger with 3, it will set it to 3).

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1S-DhD1lOKDCw_vjfYdps7bQDmkTrsLAQ/preview?usp=drivesdk></iframe></div>

# 2: Counter Object

This object appears as a "0" in the trigger section. When placed, clicking :EditSpecial: Edit Special will open a page with several buttons. All of them besides "Time Counter" and "Seconds" will be covered here.
## Maintime 
Maintime calculates the total time that you spent in a level (e.g., if you have spent a total of 60 seconds in a level, then it’ll display “60.00” etc).
## Points
This will count the total amount of points that you’ve obtained from collectibles. When you set collectibles to a certain amount of points, they add/subtract points (e.g., if you were to set a collectibles “point” value to 2, then it’ll add to the points of a “0” object).
## Attempts
This will allow you to count your in-game attempts and display them as a number -  useful for death counting.
## Left align”/”Right align 
This works by setting the center of the pickup trigger to the digit in that position. For example, if it’s in left align and the number is “123”, the center will be the number 1, which means that digit is stuck to that position and will never move, if “right align” is on and the number is 456, the center is the number 6, and it will be stuck to that position.

<div><iframe src=https://drive.google.com/file/d/120TwW6FX-qeBE8LQv7SOjoWkSuhNhxxe/preview?usp=drivesdk></iframe></div>





## Credits
Created by @Danail and @Madzz
