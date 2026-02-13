---
title: Making Loops
weight: 607
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Medium** (15-17 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- Using loops is a great way to accurately and repeatedly use a set of triggers.
- The most common type of loop is a spawn loop, with many different variations of this loop.
- Every loop is best suited for a different application, and each has pros and cons.

{{< /callout >}}

** **
# 1: Spawn Loop

A spawn loop is the most well-known and common loop. It uses a sequence of spawn triggers that activate other spawn triggers. 

The setup consists of three main parts: the activator, the steppers, and the looper. The **activator** is the __spawn trigger that initially activates the loop__. The **steppers** are the __spawn triggers that activate the next “steps” or sets of triggers in the loop__. The **looper** __reactivates the first set in the loop so that the loop can repeat__. If the loop only contains one set of triggers that activates itself, that set acts as both the stepper and the looper.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1tE4WH1JBi8gy1HdeXRUOEzr7zpM1sNNp/preview?usp=drivesdk></iframe></div>

Each spawn trigger within the loop has a delay, which is the time it takes to activate the next step in the loop. You can add or remove steps by putting the necessary number of steppers needed for the loop.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/14-EiHzIWbwQ8Vth39YeLZaSmJMYwn6lO/preview?usp=drivesdk></iframe></div>

## Setup
1. Place down a spawn trigger (or any other condition trigger) and have it target a new group. This is the activator.
2. Place down the triggers you want to spawn and a spawn trigger and have them all be spawn-triggered and multi-triggered. The spawn trigger is the stepper. Assign them the group the activator targets.
3. Set the spawn trigger in the stepper to have a chosen delay and target a new group if needed.
4. Repeat steps 2 and 3 as many times as necessary with the new group.
5. When you have your final stepper, have the spawn trigger target the group of the first stepper in the loop. This is the looper.

Video: https://cdn.discordapp.com/attachments/827766936762056705/1267656176234139789/2024-07-29_18-30-09.mp4?ex=66a99450&is=66a842d0&hm=2135cf89b9c9229e677624a7f4d16e8397a193b1eac1e571699d64a0dfbea042&

## Create Loop Button
The Create Loop function is a button that can be found in the pause menu of the editor. When selecting your desired triggers to be part of the loop, pressing this button will automatically create a spawn loop for you.

If some selected triggers have the same x-position, they will be combined as part of a single stepper. This function determines the delay between each step based on the time it takes for the editor line when playing music to reach each stepper. This means the delay can be affected by speed portals. The best way to see this is by enabling the “Duration Lines” option.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/19yffJNR1QgBc7cg0Bf3X0qjRLXCAZy8M/preview?usp=drivesdk></iframe></div>

Because of this, if you were to try to create a loop with only a single stepper, the function would get confused and have no delay as there isn’t another stepper to use as a reference. In this case, you would have to manually set a delay for the setup to work.

Video: https://cdn.discordapp.com/attachments/827766936762056705/1267664078495547423/2024-07-29_19-02-15.mp4?ex=66a99bac&is=66a84a2c&hm=df61ee8efb301ab2c292beb8edea9a7756f72685b36b88fb4b8d894ee2ffc3ac&

## Breaking the Loop
To stop a spawn loop, simply add a group to the spawn triggers in the loop and stop it with a stop trigger. To restart it, spawn the loop as normal.

Video: https://cdn.discordapp.com/attachments/827766936762056705/1288008642930544640/2024-09-23_22-25-05.mp4?ex=66f39f06&is=66f24d86&hm=5da63dc82fa03986dd21d2003e6647bbdd21b6dc79cd5abc03a7b1eb851e745a&

## Pros and Cons
+ Can have as many steps in the loop as you want
+ Easy to have precise timings between steps
+ In-game button so the loop is easier to make

\- Can break from lag
\- Create Loop can be finicky to use, especially if your setup uses multiple types of IDs.

# 2: Spawn Ordered Loop
This loop is similar to the regular spawn loop, except it makes use of the “Spawn Ordered” setting. Since spawn ordered spawns the triggers based on their editor position, extra spawn triggers aren’t needed for the steppers.

This saves both groups and time, with a drawback being accuracy. The looper also needs to have spawn ordered enabled to keep the loop going, which means the delay timer won’t work. This also means the loop *must* be activated with a spawn trigger.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/17SrVANy69xlq-klK2dIh1ee7ObXb4sri/preview?usp=drivesdk></iframe></div>

## Setup
1. Place down a spawn trigger and have it target the next free group. Make sure the “Spawn Ordered” option is enabled. 
2. Place down your triggers in a line as if they activate normally through the editor.
3. Place down a spawn trigger with Spawn Ordered at the end of your trigger line, reactivating the group.
4. Select all triggers in the line and make them spawn-triggered and multi-triggered. Give them the group activated for the loop.

Video: https://cdn.discordapp.com/attachments/827766936762056705/1269473402138394634/2024-08-03_18-52-19.mp4?ex=66b030bc&is=66aedf3c&hm=45c10d1b1976921ef7ae0a2d7f85812e5e15323838bfca348fb16490c2dc7751&

## Breaking the Loop
To stop the loop, toggle off the group of the loop using a toggle trigger. To re-enable it, first toggle the loop back on, then spawn it using spawn ordered again.

Video: https://cdn.discordapp.com/attachments/827766936762056705/1288012404734693396/2024-09-23_22-40-15.mp4?ex=66f3a287&is=66f25107&hm=66d43cc230b8c3caf8444740cd4963498f147de8711d385a473a8b8558431ef5&

## Pros and Cons
+ Easy to set up
+ Uses fewer groups

\- Hard to have precise timings
\- Can only be started with a spawn trigger

# 3: Spawn Remap Loop

This loop uses the spawn remap feature to remap the groups within the steppers. This gives you all the benefits of using spawn remap while also maintaining a loop.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1T0F-JEGbVdj6Id4mHS-1rPjI4yoAtFCG/preview?usp=drivesdk></iframe></div>

The above example uses spawn ordered to activate the loop, but any other looping method can work as long as the looper uses a spawn trigger with spawn remap. Keep this in mind throughout the explanation.

The loop works by having the looper triggers remap two kinds of values:
1. The groups the steppers are activating.
2. The groups that activate the next looper.

The first step is to add a buffer trigger, which will be a spawn trigger. It will be the first trigger to be activated in the loop.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1FssVPQezFswVyAWXc01gn_m4EbhMZJTj/preview?usp=drivesdk></iframe></div>

This will target the steppers in the loop. This allows the loop to be remapped to a different group that will target a different looper on each iteration. Within the spawn trigger, there will be a remap that will change the values in the steppers. **This remap is crucial, as without it the loop will crash.**

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1x1ZgZu7kNm-vjL_8GC4PJ7xBjFSBRo5w/preview?usp=drivesdk></iframe></div>

The OriginalID is a placeholder value that will not be used, so make sure to keep an unused group to place there. This is the value that needs to be put in your stepper triggers and will be remapped. The NewID is the ID that will be remapped every loop; the one shown here will be the group activated on the first iteration.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1OH8vWiFm35_7xowjp_lGUDdU-EB4zrSV/preview?usp=drivesdk></iframe></div>

The looper will spawn the buffer trigger again, this time remapping the values within that spawn trigger. **The loopers must have “Reset Remap” enabled so previous remaps do not carry over, otherwise the game will crash.**

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1IJJlWUqk9z0VIen2kYUUN00Qo_u5ST1b/preview?usp=drivesdk></iframe></div>

The first pair of remaps will change which group the final stepper spawns (or if you use spawn ordered, it remaps which group the buffer trigger spawns). This will change which looper is activated next iteration. This also means that **the steppers activated by the OriginalID must have the NewID as well.**

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1lBnvb0UdwQx3MfgP4-nmUOmZzw-D_Yp_/preview?usp=drivesdk></iframe></div>

From then on, keep adding as many loopers as necessary for your setup, creating unique remaps for each of them and assigning the appropriate groups. The final looper will have no remaps on it, allowing the loop to go back to the first looper.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1veuEo198qkCb4oSTde6AhZ3_7wxtTchv/preview?usp=drivesdk></iframe></div>

## Setup
1. Place down your activator to start the loop. Have it target a new GroupID. 
2. Place down a spawn trigger that gets activated by this GroupID. This is the buffer trigger. Make sure it is spawn-triggered and multi-triggered and have it activate a new GroupID. This buffer trigger will have the group remap.
3. Set up the rest of your steppers in the loop, activating them with the GroupID in the buffer trigger.
4. Identify which value in the steppers you want to remap. In the buffer trigger, add a remap with the OriginalID being an unused group and the NewID being the value to be remapped.
5. Add your looper. Have it target the buffer trigger. The loopers should have reset remap enabled.
6. Add the first remap to the looper. It should remap the GroupID spawning the looper to a new GroupID. If applicable, any other triggers with this GroupID that aren’t this spawn trigger should have the remapped GroupID as well.
7. Add the second remap to the looper. This is the value you want to remap from the steppers (aka the value in the original buffer trigger). 
8. Repeat steps 5-7 as necessary.
9. For the final looper, do not add any remap values so that the loop can go back to the original looper.

Video: https://cdn.discordapp.com/attachments/827766936762056705/1302188115146051614/2024-11-02_01-23-141.mp4?ex=672734b0&is=6725e330&hm=87f93734caa6da3b0c1a0f27d391ffe49c9af97a59ce7bb7ccef96bd1f23e719&

## Breaking the Loop
Use the method for breaking and resetting the loop for whichever loop you used for the spawn remap loop (i.e. using stop triggers for a regular spawn loop, toggle triggers for a spawn ordered loop).

## Pros and Cons
+ Can be useful in remap setups

\- Extremely complicated loop

# 4: Collision Loop

A collision loop is made up of collision blocks. A main collision block moves through a line of other collision blocks via a move trigger (the activator), each one acting as a stepper that activates a group of triggers. The final collision block in the line acts as the looper as it will activate a move trigger that moves the main block back, resetting the loop.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1mFXtX0SrLqzYNfehMWXG0NLCbg3mpgcC/preview?usp=drivesdk></iframe></div>

## Setup
1. Place down your main block with a unique Collision ID and have it set as a Dynamic Block. Give it a new group.
2. Have a move trigger move the main block to the right for a large amount of time (alternatively you can spawn another move trigger to move it again when the block hits the looper, make sure to stop the previous movement before you do so).
3. Place down a collision block to the right of the previous block(s) and give it a new Collision ID. This will be your stepper.
4. Set up the triggers you want to be activated and have them be spawn and multi-triggered. Give the triggers a new group.
5. Place down a collision trigger before the loop would have been activated and have it spawn the group of your desired triggers when the ID of the main block and the stepper collide. 
6. Repeat steps 3-5 as much as necessary.
7. Once the final stepper is placed, include a move trigger in the activated triggers to move the main block back to its original position (this can be done by manually putting an amount to push it back or using target mode to move it to the position of a different object.)

Video: https://cdn.discordapp.com/attachments/827766936762056705/1271703803015598131/2024-08-09_22-33-29.mp4?ex=66b84df5&is=66b6fc75&hm=f0b52d0142fb657bb9e5c5aacad6c42c69c3a41465b7cf8456f7aa8a57022c27&

## Loop Flexibility
Due to the collision loop relying on the collision of actual objects, this means that steppers can be moved, removed from, or added into the loop as it’s running. If you plan on moving the looper block, it is a good idea to use a target mode move trigger to push the main block back so that timings will be consistent.

Video: https://cdn.discordapp.com/attachments/827766936762056705/1271723252074676335/2024-08-09_23-52-53.mp4?ex=66b86012&is=66b70e92&hm=9371788ff1d7c119129d9210235c416d119bd03cce2800e7b673e7f0fe0e1663&

## Breaking the Loop
There are multiple ways to break a collision loop. One way to have it break and be easily resetable is to stop the movement of the moving block and put it back in its original position using the move trigger’s target mode. From there, you would move the block again to start the loop.

Video: https://cdn.discordapp.com/attachments/827766936762056705/1288015601180344381/2024-09-23_22-52-23.mp4?ex=66f3a581&is=66f25401&hm=a4a34b1ced4ba9ae2ee56a35d46ef0138356638225252f58b6c50bc2a46dd0f0&

## Pros and Cons
+ Extremely flexible loop

\- Uses a lot of Group and Collision IDs
\- Can be difficult to get the timing correct

# 5: TPS Loop

2.2 changed how a lot of physics calculations have been done. Instead of relying on FPS to update things, it now uses a Ticks Per Second (TPS) system to run these checks. The game runs on 240 TPS, meaning things like physics and collisions are checked 240 times per second. These checks also include collisions between collision blocks, so we can use this to make a loop every time a collision is registered in the game. 

For this loop, we take two touching collision blocks and one of them toggle off once a collision is detected. Then a separate collision trigger will toggle it back on the next tick once it notices the two *aren’t* touching. This will create a loop that will trigger every 1/240th of a second.
## Setup
1. Place 2 collision blocks, one of them being dynamic and having a group.
2. Set up a collision trigger to spawn a toggle trigger that toggles off the collision block when the two blocks collide.
3. Set up another collision trigger to spawn a toggle trigger that toggles on the collision block when the blocks are no longer colliding (Enable “Trigger On Exit”).
4. Add your triggers to be spawned in the loop and give them the same groups as the toggle triggers.
5. Move the two collision blocks onto each other to activate the loop.

Video: https://cdn.discordapp.com/attachments/827766936762056705/1272055257442156574/2024-08-10_21-49-54.mp4?ex=66b99547&is=66b843c7&hm=3fa0345ede069c70911f771c56c39731b522d20bbddcbb8c5d96f5e4797e9f40&

## Breaking the Loop
To break the loop, move either collision block away so the two blocks don’t collide. To restart it, move them back together again.

Video: https://cdn.discordapp.com/attachments/827766936762056705/1288018089559986251/2024-09-23_23-02-54.mp4?ex=66f3a7d2&is=66f25652&hm=ec7670c89c84b5ec2a14b74d960550ebe0612732f96e8653e5842957b6772f24&

## Pros and Cons
+ Quick and consistent loop

\- Not easy to set any other delays

# 6: Time Event Loop

The time event loop makes use of the time and time event triggers. Time triggers will act as the activator (starting the timer) and the looper (resetting the timer), while the time event triggers will activate steppers when the timer hits your desired time.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1Zy50nY61xprmHg4i1GZSjF72YlebhgAD/preview?usp=drivesdk></iframe></div>

## Setup
1. Place down a time trigger to start the timer. Assign it to a unique Item ID. This is the activator. 
2. Place a time event trigger at or before the same x-position as the activator. Have the Item ID be the same as the timer, set your desired target time you want your action to activate on, and have it be multi-activate. This is your stepper.
3. Place down the triggers you want to be activated by the stepper. Have them be spawn and multi-triggered, give them a group, and have the time event trigger target that group.
4. Repeat steps 2 and 3 as necessary for your loop.
5. For your final stepper, include a time trigger in your activated triggers to reset the timer back to 0.00 seconds.

Video: https://cdn.discordapp.com/attachments/827766936762056705/1283574819409100860/2024-09-11_16-44-32.mp4?ex=66e37db4&is=66e22c34&hm=77a896dfcf7def447369c2882541ef01954f03ceba6015ff91540f64bba861b4&

## Using “Stop Time”
If only one stepper is needed in the loop, the time trigger’s “Stop Time” feature can be used.

<div><iframe src=https://drive.google.com/file/d/1BJQ10Fp9WAEjkiMZWQqnsqGZSPnBqxuw/preview?usp=drivesdk></iframe></div>

1. Have your desired activator spawn a new Group ID.
2. Place down a time trigger and give it the Group ID. Make sure it’s spawn and multi-triggered.
3. Set the Item ID to the one you want the timer to run on. Enable “stop time” and set it to the duration between each loop. Have the Target ID activate a new group.
4. Add the triggers you want to be activated on the loop and give it the Target ID group. 
5. Add a spawn trigger to the other triggers to activate the time trigger again.

Video: https://cdn.discordapp.com/attachments/827766936762056705/1283582061247987722/2024-09-11_17-15-07.mp4?ex=66e38473&is=66e232f3&hm=e52d46261a88076e0d83591f36d2aceb9a87f8421592eaabab9c7537b1cc375d&

## Breaking the Loop
To stop the loop, use the time control trigger to stop the timer. To restart it, activate a time trigger for the timer. 

Video: https://cdn.discordapp.com/attachments/827766936762056705/1288020969830486117/2024-09-23_23-14-11.mp4?ex=66f3aa81&is=66f25901&hm=cc320b27702d8a4f902ca40ef061aeed789911f60d910488124a2a8911ac5a14&

## Pros and Cons
+ Visible timer to visualize timings
+ Can modify the time speed
+ Can have the loop unaffected by timewarps

- Minor loss of timing accuracy
- Steppers have to be placed a certain way

# 7: While Loop

A while loop runs a loop *while* a condition is being met. The condition can be related to Item ID values, collision states, or any other trackable value. When the condition is not met, the loop stops. The condition is checked by using a trigger that can check the state of a value (i.e. instant count, instant collision, item comp, etc.)

None

## Setup
1. Place down your trigger that checks for a condition and have it be spawn and multi-triggered. Give it a group and have it activate another group when the condition is still true.
2. Configure the loop that you want to run, having the first stepper in the sequence be activated by the condition trigger.
3. Have the looper target the condition trigger to activate the while loop again.
4. Activate the condition trigger with the appropriate trigger to start the loop.

Video: https://cdn.discordapp.com/attachments/827766936762056705/1273883990314582088/2024-08-15_22-58-05.mp4?ex=66c03c6a&is=66beeaea&hm=fa82a8a52ef861713c801b9cacb0154e497f27890d01922c7332eba025a62807&

## Breaking the Loop
Use the method for breaking and resetting the loop for whichever condition or loop you used for the while loop.

## Pros and Cons
+ Built-in way to break the loop
+ Can use different types of loops

\- Can be a little complicated to set up

# 8: For Loop

The for loop will repeat a loop *for* a specified amount of times. A for loop is similar to the while loop in that it checks for a condition as it loops, the difference being that this condition is acted on by the loop itself. Typically, an item counter is used to count down from a number input to zero. The loop will automatically subtract from this counter each time it executes.

Video: https://cdn.discordapp.com/attachments/827766936762056705/1281372093732360232/2024-09-05_14-54-00.mp4?ex=66db7a41&is=66da28c1&hm=74074efab6684c8fc577f375ce82704b775e28f77ebbfcf8cb5a14c8473fe701&

## Setup
1. Place down an instant count trigger and make it spawn and multi-triggered. Give it a group and have it activate another group when your desired Item ID is larger than 0. 
2. Configure the loop that you want to run, having the first stepper in the sequence activated by the instant count trigger. Include a pickup trigger in the first stepper that decrements the tracked Item ID by one.
3. Have the looper target the instant count trigger to activate the for loop again.
4. Give the tracked Item ID a value larger than 0, then spawn the instant count trigger to begin the loop.

Video: https://cdn.discordapp.com/attachments/827766936762056705/1281375356640825536/2024-09-05_15-06-15.mp4?ex=66db7d4b&is=66da2bcb&hm=344a7c310961e8d39f95ab96e743a5f56699fcd25a53f4705ed09e33b2812ba5&

## Breaking the Loop
Use the method for breaking and resetting the loop for whichever condition or loop you used for the for loop.

## Pros and Cons
+ Built-in way to break the loop
+ Can use different kinds of loops
+ Easy to loop for a specific number of times

- Slightly complicated setup
- Have to specify the loop amount before activation





## Credits
Created by @TDP9 and @kyouki
