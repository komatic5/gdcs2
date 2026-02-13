---
title: SFX & Edit SFX
weight: 315
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Short** (9-11 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- The SFX trigger allows you to choose a variety of sound effects to use. You can give these sound effects unique IDs; change when they start and end; and change their speed, pitch, and proximity.
- The Edit SFX trigger changes a sound effect’s properties and proximity, assuming that the sound effect in question has an ID.

{{< /callout >}}

** **
Sometimes, a GD level with a Newgrounds song just isn't enough to make your levels complete. You want to add in SFX to add details to your level. Imagine playing a Super Mario game, but without the iconic jump sound. It just doesn't hit the same. The new :SFXTrigger: SFX trigger completely changes that now, and here's how to utilize it to your advantage. 

First place down the SFX trigger.When selected, click on the :EditObject: Edit Object button. The first page of the SFX Trigger is shown below:

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1NuHdJN5htewog6oaTLTLXvpaSzweX6JL/preview?usp=drivesdk></iframe></div>

You can select the sound effect you want by clicking on the tablelist button in the top right corner of the UI.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1CyDDv-Q4V7xVll8hFkHEAQujvx4nBjvJ/preview?usp=drivesdk></iframe></div>

From here, you are able to select a wide variety of sounds, ranging a total of *13,590 sound effects* for anyone to choose. The magnifying glass allows you to search for any track, and even has a checkbox for specific folders.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1Ska9vbP79cL3FJP8rh72HmYqcvj0s-6b/preview?usp=drivesdk></iframe></div>

Exiting out of “Find SFX'', you can click on the arrow button to sort these sound effects in alphabetical order (Name+/Name-), length (Len+/Len-), or SFX ID (ID+, ID-).

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1eULzqlJC8kt0AudTUc8oePPYvwpuKYDr/preview?usp=drivesdk></iframe></div>

Once you select an audio, you are able to replay it and use the sliders and checkboxes to adjust the sound effect to your liking.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1kwssgJ6xOwcjxfGGMoTsf_vbAVYYIbSg/preview?usp=drivesdk></iframe></div>

Speaking of which, let's talk about the SFX options on the first page:

- As mentioned in the [Song Trigger](<https://discord.com/channels/414295025883545600/1193403796466970756/1193579459912151140>), the **Speed slider** __changes the velocity of the song__ that is played in the channel. 
- **Pitch**: __Transposes the sound per semitone__. In music theory, there are 12 semitones in one octave, ranging from keys C to B.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1HTo4Tp6QfbySbXbYOFBVOdbqfj-dED8p/preview?usp=drivesdk></iframe></div>

- In this piano chart above, we can move between semitones by playing the next note. Next semitone of C in this case would be C#, then D, then D#, and so on. If I were to play C, then move myself 12 semitones higher or lower, I will end up back to C, but a different frequency will be played.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1twXUNTqqiGxaYFwrQfjJmqiv3_qRNAGZ/preview?usp=drivesdk></iframe></div>

- This is a sine wave being played at C2

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1DIqIZqLkc97H_Geg-vT0ezal6lILPwiK/preview?usp=drivesdk></iframe></div>

- and this is a sine wave played at C3.
 - What's actually happening is that the wavelength gets multiplied if you play the same note every 12th semitone. These are referred to as Octaves. 
- Going back to GD, we have a range of 2 octaves, one being lower and one being higher. (If C4 is the note, then it ranges from C3 at -12 pitch to C5 at 12 pitch)
- Volume: Adjusts the gain volume of the sound being played. 

Over on the bottom right, you can see 4 checkboxes:
- **Reverb**:__ Causes the sound to be repeated and bounced around numerous times in an echo__. These could be used to insinuate a sense of space in an enclosed area in real life through sound. Tighter reverb details a small room (like a bathroom), while a big, open reverb details a big room (like a church). 
 - Clicking on the + Button on reverb presents you with a bunch of presets made for reverberation.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1MPS3UqPMbbw3Z_LYPw_JkDvLD-OsSRyj/preview?usp=drivesdk></iframe></div>

- Note that there is a limitation to using reverbs. As of right now, there is only ONE global reverb channel. This means that you cannot use multiple sounds in different reverb settings played simultaneously. 
- **FFT**: Stands for “Fast Fourier Transformation”. It calculates the DFT (Discrete Fourier Transform), or its inverse at a much faster rate. In music production, signal processing, and audio engineering, __FFT is used to signal speeds and pitches in the form of frequencies in a given domain and also gives information about its signal__. 
 - In audio engineering and software development, this is used for many applications, such as vocoding, multi-band compression, EQing, and simply for frequency analysis. 
 - Below is an example of using FFT to visually demonstrate a frequency spectrum of a song.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1--6u2BjlIaqpEICez-Ku9Wuj-w3_lzNs/preview?usp=drivesdk></iframe></div>

- If you would like to learn more about how FFT works, here is a link to a website that explains the general basics about [Fast-Fourier Transform](<https://www.nti-audio.com/en/support/know-how/fast-fourier-transform-fft>).
 - In Geometry Dash, we do not need to worry about how to apply all of the complicated post-processing effects to our sound. In this case, FFT is used as a different stretching algorithm for sorting speeds and pitches. 
 - In comparison to FL Studio, this is equivalent to using resample vs stretch mode when stretching audio.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/106oF2E9m3glzOCXknZs6W-INMWgnutkO/preview?usp=drivesdk></iframe></div>

- **Loop**: __Repeats the audio__ back to the beginning of the song when it reaches the end of the track.
- **PreLoad**: As covered in the Song trigger, __it reads the audio before the trigger is being spawned__. Useful for optimization if there is multiple audio being loaded at once. 

Let's head to the next page of the SFX Trigger by clicking on the left arrow.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1zu86A0mLdEAoZzytx-_mg-8VDphBZb7z/preview?usp=drivesdk></iframe></div>

This is the second page of the SFX Trigger.

- The **Start slider** allows you to __start from any timestamp in the song__, and vice versa for the End slider.
 - Note that the values are actually multiplied by 1000, so 1 second is actually 1000 in value, 2 seconds = 2000, and so on. 
- The **FadeIn slider** gives values of __how much the song goes from no volume to its actual volume gain__ (Volume Slider), and vice versa for the FadeOut slider.

Click on the right arrow to go to the next page.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1SGixR4zb5imNAPsLPTlSBLLeyTBcsS9I/preview?usp=drivesdk></iframe></div>

This is the third page for the SFX Trigger.

In the left, there are two counters and a slider:
- **Unique ID**: __A new ID dedicated to SFX__. The sounds get linked into these Unique IDs instead of relying on Group IDs. 
- **SFXGroup**: __A new ID dedicated to sorting SFX IDs into groups__. 
- **MinInterval**: __The minimal interval that occurs before playing the sound effect__. Behaves like a cooldown. 
 - Use UniqueID and SFXGroup to organize your sound library and to know which Unique ID and SFXGroup are correlated. 

On the right you have 3 checkboxes:
- **IsUnique**: A constant Unique ID in the SFXGroup __that makes it so that no other SFX are able to replace or substitute itself__. 
- **Override**: Unlike IsUnique, __this gives the ability for SFX to be able to replace or substitute any Unique IDs and SFXGroup__.
- **Ignore Volume Test**: __Ignores volume being adjusted by proximity__ (i.e. If the proximity makes the Volume go to 0, enabling this will ignore it.).

Click on the right arrow to head to the last page in the SFX Trigger.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/15w45AlrWBbbVaE7G8YNaCOsj_QAxpH6k/preview?usp=drivesdk></iframe></div>

This is the 4th and final page of the SFX Trigger.

This entire page deals with proximity based on the player, camera, or object. As stated previously, proximity in music is adjusting volume gain based off of the distance relative to an object or player. The farther away the target is to the object, the less of an effect it'll create. The closer it is, the more effect it'll create. 

- Group ID 1 is the target object that will be used when calculating the proximity. 
- Group ID 2 (when applying proximity with Group ID 1) is the object that will be applied to the object. 

In the left set of sliders, you can adjust the volume for whatever distance you set it to:
- **VolNear**: __Volume in a near distance__. This creates a red area when selecting the SFX trigger.
- **VolMed**: __Volume in a range of distances between Near and Far__. This creates a green area when selecting the SFX trigger.
- **VolFar**: __Volume in a far distance__. This creates a blue area when selecting the SFX trigger.

In the right set of sliders, you can adjust the distance of VolNear, VolMed, and VolFar in their own respective sliders labeled MinDist, Dist2, and Dist3. Adjusting these sliders will also move the colored areas accordingly. 

Note that these colored lines represent a visualization of proximity. 

On the bottom left, you can select either P1, P2, and/or Camera to be the replacement for Group ID 2.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1dl3sAZ_hRVImgnHx6qJYe57ch4qeSjlI/preview?usp=drivesdk></iframe></div>

On the bottom right, you can select different modes for proximity. Each button shows arrows facing which way will the proximity take effect, while the line represents the object that is being targeted. (Group ID 1).

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1VJXZOwq21g9SEtatvtJYQmDv7MNmqqcp/preview?usp=drivesdk></iframe></div>

# 2: Edit SFX Trigger

Place down the Edit SFX Trigger. It is shown below.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1IcipJhlyHR33sO-H7OecFHT_upEtpkzO/preview?usp=drivesdk></iframe></div>

When selected, click on the :EditObject: Edit Object button. Below is the first page of the Edit SFX trigger.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/10nOjkprPboqYbDX4w9NCumLdKryyY7UJ/preview?usp=drivesdk></iframe></div>

You can assign target Group IDs for the SFX trigger that is played, however you can alternatively choose the SFXGroup and the Unique ID for the SFX trigger. 

- The Duration slider is the time it takes to edit the property of the sound effect (Volume or Speed). Think of this as the “Move Time” in a Move trigger or the “Fade time” in the alpha trigger. Alongside the duration slider, you got two checkboxes:
 - Stop: Abruptly stops the sound effect in the channel.
 - Stop Loop: Ends the loop of the sound effect played in the channel, assuming that Loop is enabled in the SFX trigger. 
- The Speed slider changes the velocity of the sound effect that is played in the channel. Next to the slider is the Change Speed checkbox. This needs to be enabled in order for the speed change to take effect. Note that: 12 Speed = 150% Speed, -12 Speed = 50% Speed.
 - Below is the formula for the velocity of the speed:
  - s = 2^(t/12)
   - t = the speed set to the slider
 - Below is the formula for the time it takes when applying its speed slider:
  - n+(2^t/12)(x-n)
   - n = start offset
   - x = end offset
- The Volume slider adjusts the gain volume of the channel that is being played. Next to the slider is the Change Volume button. This needs to be enabled in order for the volume to take effect. 

Click on either arrows to go to the next page of the SFX Trigger.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1oVHsJelojsBMmwbngm4VqvOzBL_vGF8S/preview?usp=drivesdk></iframe></div>

This is the second page of the SFX Trigger, and it deals with proximity relative to the player, object, or camera.

This page is already covered in the fourth page of the SFX trigger, so this is going to be brief, but this modifies the volume based on the distance of the targeted object, whether it would be the Group ID, Player 1, Player 2, or Camera on multi-colored lines visually demonstrated in the editor when selecting the trigger.

<div style="width: fit-content; height: fit-content"><iframe src=https://drive.google.com/file/d/1eSRwQx_g7RcAc7pWslA6CTrXItu3T7-N/preview?usp=drivesdk></iframe></div>

The video below demonstrates the usages of SFX and Edit SFX triggers:

<div><iframe src=https://drive.google.com/file/d/1FbXa2GOVXoAYdyGai7vkdhwKPEL14C8Q/preview?usp=drivesdk></iframe></div>





## Credits
Created by @DangerChampion and @Electrify
