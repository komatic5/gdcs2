---
title: Making Sync
weight: 414
draft: false
---
{{< img src="images/GDEmotes/Icons/Clock.png" class="emote">}} **Short** (5-7 minutes)

{{< callout context="note" title="TLDR - What this guide covers" icon="outline/info-circle" >}}
- Implementing sync into your level helps keep the level engaging for the player, and gives them a “foundation” for their clicks.
- There are plenty of tools in the editor that allow you to create accurate sync, and can all be used to effectively build different types of sync.
- Outside factors such as audio delay, polling rate, and speed portals can affect the result of how your gameplay syncs. Employing thorough playtesting can help combat these issues.

{{< /callout >}}

** **
# 1: Why does sync matter?

Sync is an essential component for classic gameplay, since it keeps the level engaging for the player. It’s also useful for giving the player a “foundation” for their clicks.

There are many ways you can convey sync — and in turn energy — in your gameplay through syncing by clicks or syncing with the player's movement. The energy of a song can be conveyed this way if actions match the song’s rhythm, but you need to be selective on what you want to sync with. This can include the melody, bass, or with percussion. Patterns will form from this and are what players enjoy since they match with the song. This can be taken further by having extra clicks sync with extra notes, although this is usually done with slower songs as it’s much clearer to the player.

# 2: Ways to Make Sync

## Music Line :MusicPlaytest:

The music line follows the X-position of the cube unless an arrow trigger is used, which switches between vertical or horizontal movement. Using the music line can be useful in this case since otherwise, it would be difficult to discern where to place synced elements or build transitions this way. It helps to use the playback option to start the music line from the arrow trigger for more accuracy. This option can also be enabled for speed portals.

While this feature is useful, it can be inconsistent. Arrow triggers, along with speed portals and X-axis teleportals are likely to conflict with this feature as of 2.207. It’s also limiting when building click-sync, since some clicks may not have an impact to go along with them.

[Video](https://cdn.discordapp.com/attachments/1226717493041565778/1321250159774007316/Screen_Recording_20241224_165315_Geometry_Dash.mp4?ex=676c8d99&is=676b3c19&hm=4d681c4935fdf6230b7df25480c7f65462792f4526e4207ff0c8b79be6b090d6&)

## Editor Playtest

Editor playtesting lets you test click behaviour thoroughly while playing, which is good for syncing with the player's movement. This includes different types of synchronization such as air-time or being idle.

Editor physics can differ from in-game physics, so do keep in mind that what you’re playtesting may not feel the same to the player; test sections of gameplay in-game occasionally to remedy this.

[Video](https://cdn.discordapp.com/attachments/1226717493041565778/1321253624554459208/Screen_Recording_20241224_165232_Geometry_Dash.mp4?ex=676c90d3&is=676b3f53&hm=3eeed733857ae7e776e779910c916cd3c27b5f89d4cc393a0a7ed0e345abfe21&)

## Music Guidelines

Music guidelines help you sync clicks without needing to reuse Music Line as often. To create them, go to level settings and click “new” in the song selection, which should show a button called “create lines” in the bottom left corner. Clicking “record” will start the song and other clicks will register as lines in the editor. If these lines are aligned to the rhythm of the song, they can be used as a foundation for sync. These can be removed by clicking the “clear” button.

Since this feature doesn’t allow for differently colored or different opacities of line, it can cause clutter quickly. This can also be affected by input/audio delay, offsetting the lines by that delay.

https://cdn.discordapp.com/attachments/1248071898999427123/1321256029387755591/Screen_Recording_20241224_171752_Geometry_Dash.mp4?ex=676c9311&is=676b4191&hm=2b42330d95f3ddfc90d892eee7782363f1a8890beb521ee6065eee9da69e7ea9&

## BPM Trigger :BPMTrigger:

The [BPM trigger](https://discord.com/channels/414295025883545600/1194072364124749824) works similarly to guidelines, but is strictly aligned to the BPM set. You can also place beats between the bars with the **BPB** (Beats Per Bar) slider. This is helpful for adding extra clicks in the gameplay, which allows for engaging click patterns.

This feature doesn’t work with vertical gameplay, limiting sync with things such as  percussive instruments to the X-axis. It also suffers the same cons as music guidelines, and should be used in moderation to avoid clutter.

## Speed Hack

Speed Hack can be useful for increasing precision with sync. This is mostly used for more difficult levels as they have less error for timings and would help the player to have a base for their click. Speed Hack should not be set to a drastically slow number, but enough to have a better idea on the position of the click; 0.5 - 0.75x usually works best. Doing this may cause the clicks to feel or appear different once the game speed is set back to 1x.

# 3: Tips To Consider

## Speed Portal Positions

When making accurate sync, speed portal position should be taken into account. The Music Line ignores its perpendicular axis, which affects objects like speed portals; The speed will always change at a predetermined point. While playtesting, the spot in which the player collides with a speed portal changes the speed.

Fixing this behaviour is simple: By using a Follow Player Y :FollowPlayerY: trigger, you can have a secondary portal that prevents the player from being able to jump over the original portal, mitigating desync.

https://cdn.discordapp.com/attachments/1248071898999427123/1321335191825944606/Screen_Recording_20241224_192851_Geometry_Dash.mp4?ex=676cdcca&is=676b8b4a&hm=8c80daa0af021104ad3280ea07b38827cef419e592283d22f8a3f3b207077311&

## Device Audio Delay

### Bluetooth Devices

Bluetooth Audio Devices are likely to introduce delay to your level, since it takes longer for information to reach the speaker than by wire. You should avoid using these for level building when possible, since they may create up to 2 or more blocks of delay.

### Device Click Delay

This problem is common for mobile devices due to bad polling rate from the device or inconsistent frames from the game. You may have small delays when playing, which may make it unnoticeable for you, but others who don't experience delay will notice it quickly. Music Line comes in handy to combat this; matching movements (jumps and holds) to the music line rather than physical clicks can help while creating sync.

## Thorough Playtesting

Using only one method of playtesting is generally not a good idea since many factors can affect the sync in noticeable ways. Using multiple methods to check for consistency helps greatly. Speed portals are one of the most important cases to use this, since the point where the player collides can drastically change the sync of the song.





## Credits
Created by @Eclypse and @NotAModerator
