---
title: Count & Instant Count
weight: 344
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Tiny** (1-3 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- The Count trigger waits until an Item ID reaches a target count before activating, while the Instant Count trigger checks if the target count is reached at the instant it activates.
- Both triggers double as Toggle and Spawn triggers.

{{< /callout >}}

** **
The Count trigger :Count: will take an Item ID, *wait UNTIL that ID passes a specific Target Count*, and then activate or deactivate a Target Group ID. It can work as both a Toggle and a Spawn Trigger.

None

**Multi Activate** (*don’t confuse this with Multi Triggered!*) will __activate the trigger every time the Item ID reaches the Target Count.__

None

*Note that a Count trigger will still activate if the target count is passed.* If the Target Count is 2 and the Item ID’s value goes from 1 to 3, it’ll still activate.

If the target count is passed before the Count trigger’s activates, then it won’t work.

# 2: Instant Count Trigger

The Instant Count trigger :InstantCount: will take an Item ID, *check IF the target count’s been reached*, and then activate a Target Group ID. It can work as both a Toggle and Spawn trigger.

- With the Equals option, it’ll activate if the Item ID’s value is equal to the target count.
- With the Larger option it’ll activate if the value is larger.
- The Smaller option will make it activate if the value is smaller.

None

The target count must be reached *before* the Instant Count trigger activates, or it won’t work.





## Credits
Created by @Madzz and @koma5
