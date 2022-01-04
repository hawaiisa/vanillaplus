# vanilla+

This is a brief guide to help out new players starting on the server.

Contents of this guide:
- [How to play on the server](#how-to-play-on-the-server)
  - [Using the launcher](#using-the-launcher)
  - [Not using the launcher](#not-using-the-launcher)
- [Technical issues](#technical-issues)
  - [Loading takes forever](#loading-takes-forever)
  - [My monitor's resolution is in the settings](#my-monitors-resolution-is-in-the-settings)
  - [My screen turned to black](#my-screen-turned-to-black)
  - [My addons don't work properly](#my-addons-dont-work-properly)
  - [My talent tree doesn't work properly or is still the same as original vanilla](#my-talent-tree-doesnt-work-properly-or-is-still-the-same-as-original-vanilla)
  - [Getting disconnected from the server as you log in](#getting-disconnected-from-the-server-as-you-log-in)
  - [RNG issues](#rng-issues)
- [Things to know about when starting on the server](#things-to-know-about-when-starting-on-the-server)
  - [Where can I see the list of the changes?](#where-can-i-see-the-list-of-the-changes)
  - [XP rates](#xp-rates)
  - [Changing account password](#changing-account-password)
  - [Server population and uptime](#server-population-and-uptime)
  - [Currently available raid content](#currently-available-raid-content)
  - [Talent calculator](#talent-calculator)
  - [Talent reset](#talent-reset)
  - [The Ironman challenge](#ironman-challenge)
  - [Rares, elites, and mobs in general](#rares-elites-and-mobs-in-general)
  - [The PVP scene](#the-pvp-scene)
  - [Multiboxing](#multiboxing)
  - [Other oddities](#other-oddities)
  - [Making suggestions](#making-suggestions)
  - [Helping the server](#helping-the-server)
- [Addons](#addons)
- [Other modifications](#other-modifications)
- [About](#about)

## How to play on the server

### Using the launcher

*This section is yet to be written.*

### Not using the launcher

- Register an account on the [website](https://vanillaplus.org/)
- Install any non-modified 1.12.1 wow client
- Download the [patch](https://vanillaplus.org/uploads/patch-3.mpq) from the website and place it in the `<wow folder>/Data` folder
  - If you are a Mac user, make sure the file extension is capitalised, ending up with `<wow folder>/Data/patch-3.MPQ`
  - If you are a Windows user, make sure you don't install the game in a system folder such as `Program Files` or you will need to run the `WoW.exe` as an administrator.
- Change the content of your `<wow folder>/realmlist.wtf` to be ```set realmlist logon.vanillaplus.org```
- Remove any previously downloaded cache by deleting the contents of your `<wow folder>/WDB` folder, if it exists
  - This step must also be repeated if you plan to connect back to another wow server with the same client later
- Log in and enjoy the game
  - You may also want to consider joining the [discord server](https://discord.com/invite/CfC8PGmg?utm_source=https://github.com/KrekoG/vanillaplus&utm_medium=Connect)
  - Starting the game will create your `<wow folder>\Interface\AddOns` folder in case you didn't have one before

## Technical issues

These are the issues we seen keep popping up in discord time and time again. Check the list if you run into one of these. If your issue is not listed, ask for help in the appropriate channel, providing as much information as you can, so others don't have to interrogate you to be able to help.

### Loading takes forever

Due to the custom modifications the loading time can be much longer than usual, however this is normal.

### My monitor's resolution is in the settings

You can't find your monitors resolution in the video settings of the game

#### Solution:

- Same steps as for [My screen turned to black](#my-screen-turned-to-black) below

### My screen turned to black

You set the game to windowed mode and it turned to black

#### Solution:

- Make sure your client is not running
- Add the following lines to the end of your `<wow folder>/WTF/Config.wtf` file:

```
SET gxWindow "1"
SET gxMaximize "1"
SET gxResolution "1440x900"
SET gxRefresh "60"
```

- Set `gxResolution` to what you wish it to be.
- Set `gxRefresh` to a **multiple** of `30`

Credit to: Admarel, Chuck, [Thirinena](https://github.com/hawaiisa), and so many more people...

### My addons don't work properly

Read all the points, if none of them applies, ask for help in the support or addons channel

#### Solutions:

- The version of the addon has to be compatible with the game. *Classic* is not *Vanilla*. If the addons are for `Classic`, they will NOT work. The client's version is `1.12.1`. If the addon was made for previous versions, you will need to tick `Load out of date AddOns` on the character selection screens bottom left `AddOns` menu.
- Some addons need to work with large amount of data to work properly. You may allow for this by changing the `Script Memory (MB)` option to `0` for unlimited memory access on the character selection screens bottom left `AddOns` menu.

### My talent tree doesn't work properly or is still the same as original vanilla

The game does not allow you to put 5 points on a talent that should allow 5 points? The talent trees you see are not like on the [talent calculator](https://hawaiisa.github.io/vanillaplus-talent-calculator)?

#### Solution:

- Download the server's custom patch and make sure it is at the correct path (`<wow folder>/Data/patch-3.MPQ`).
  - If you are a Mac user, make sure the file extension is capitalised, ending up with `<wow folder>/Data/patch-3.MPQ`
- Make sure you have no other custom patches that overwrites the content of `patch-3.MPQ`. The load order is alphabetical.
- Delete the game's cache by deleting the content of `<wow folder>/WDB` folder.

### Getting disconnected from the server as you log in

Sometimes when logging in, as the game finishes loading, you get a "Disconnected from server" message.

#### A potential solution that sometimes work

- Login in with a character that is located somewhere else
  - If you don't have one, just create a throwaway one, that has a different spawn point if you are still level 1
- Log in with your original character

### RNG issues

You seem to get dodged after missing, after getting parried just to be dodged again? You have seen people alluding that the RNG engine of the server is not working correctly?

#### Solutions:

- Run your own [experiment](https://github.com/KrekoG/HitAndMissCounter).
  - We have proven again and again that the complaints are not valid. Feel free to ignore said complaints until actual evidence is provided.

## Things to know about when starting on the server

To see the common chat, type `/join world`

### Where can I see the list of the changes?

There are no comprehensive list of changes, partially due to the spirit of the server. Having such a list would remove the sense of discovery and experimentation that was not seen in ages in the vanilla community.

It's also a lot of work... Just ask the others in the discord if you are curious of something, or try it out yourself.

### XP rates

- Kills: x2
- Quests: x3
- Elite & Dungeon Quests: x10
- Rested XP bonus gaining speed: x5

If you find these rates too high for your taste, you may lower them using `.xp <number between 1 and 0>` to reduce it. For example `.xp 0.5` would half your xp gain.

### Changing account password

To change your password, log in, and type in the chat
`.account password <old password> <new password> <new password>`
On success the server will respond with a `The password was changed` message

It is recommended to whisper something to yourself before typing it in to make sure your won't accidentally say your password out loud even if you make a mistake. (`/w <your character's name> .`)

### Server population and uptime

Type `.server info` in game. The response will let you know the current active player count, the maximum player count since the last restart, the number of queued people and the server's current uptime.

### Currently available raid content

- Lower Blackrock Spire
- Upper Blackrock Spire
- Onyxia's Lair
- Molten Core
- Dire Maul
- Azuregos
- Lord Kazzak
- Kurinnaxx

### Talent calculator

The talent calculator linked in the launcher is currently NOT accurate. Use the [talent calculator](https://hawaiisa.github.io/vanillaplus-talent-calculator/) created and maintained by [Thirinena](https://github.com/hawaiisa) instead.

### Talent reset

The talent reset cost has been capped to 5G maximum.

### Ironman challenge

There is an ironman challenge for those who want to take part in it. When creating a character you get a buff that gives you marginal bonuses while you are leveling. Upon your first death, you lose this buff and an announcement is made to the server of the circumstances of your demise. There are no other consequences of failing the challenge currently.

If you do not wish to take part, even though there aren't really any downsides, just remove the buff on lvl 1 by right clicking it.

The badassery of reaching lvl 60 with the buff still intact are rewarded with four things:
- A cosmetic item proving the deed
- A one time, 15 minute invulnerability buff
- An announcement made honouring your glory
- The sweet release from the eternal fear of in-game death, as the original buff is finally gone.

Also worth mentioning that the challenge cannot be lost due to fall damage or being killed in PvP.

### Rares, elites, and mobs in general

You may have seen that your character is a bit stronger than the vanilla equivalent would be. To compensate for this, the mobs have also been working out. Taking on a rare mob is often the cause of one's first death, as they rarely skip leg day and are always ready for some ass kicking, so adventurer beware!

### The PVP scene

Released battlegrounds:

- Warsong Gulch
- Arathi Basin

To incentivise PVP, you get one mark per hour for queueing. Furthermore you may buy flasks with your marks. When there aren't enough players for the battleground to continue, it closes down, rewarding one of the teams randomly with 3 marks, regardless of the state of the match.

You may join the queue from anywhere, by typing `.wsg` or `.ab`. This summons an invisible npc to talk to you. Beware though, once your battleground is finished, you will get teleported back to place where you joined the queue.

### Multiboxing

Having two logged in clients run on the same computer counts as multiboxing, even if you are manually switching between them to control the characters. Multiboxing in general is **NOT** allowed, however logging in with different accounts for trading purposes inside cities is allowed.

### Other oddities

#### I can talk to the other faction?!

Due to the low population, cross-faction cooperation was temporarily enabled so we can have fun together regardless of race. The developers promised that this will be removed once a satisfactory stable population is reached, so do not rely on this, friends will become foes again soon.

#### Summoning doesn't always work?!

Summoning spells have been level limited to avoid people abusing them. Now to summon someone of a higher level, the summoner needs to be at most 10 levels lower than the person being summoned. A level 30 player will be able to summon a level 40, but not a level 41 player.

Also when a warlock does the summoning one helper is enough to complete the spell.

#### Meeting stones

Meeting Stones, also known as Summoning Stones now require 4 players to be present to be able to summon someone. The first player's level is used for the level restriction calculation, the level of the helpers don't matter.

#### Dangerous heights

There is an increased fall damage on the server.

There is also a phenomena, where suddenly out of nowhere you suffer a massive fall damage, which sometimes kills you. This is a bug and there is not much you can do to avoid it, other than avoiding the places where this happened. Think of it like your character just fall. This is one of the reasons, why you can't loose the Ironman Challenge to fall damage.

#### Free market

All of the action houses are connected. Horde, Alliance, Neutral, all of them.

#### Cheap rides

Your first riding lessons at level 40 are free of charge

#### Public transport

Some zeppelins and boats change their destinations. Talk to the NPC before boarding to make sure you don't end up somewhere you don't want to!

### Making suggestions

There are some technical limitations that the developers are unwilling to take on, and for a good reason. If your suggestion requires the WoW.exe to be modified, it is an automatic no-no, for it has the potential to make massive unforeseen issues. This is non-negotiable and no amount of pleading will make this change.

#### Suggestions to reset the server

Don't. Just don't.

### Helping the server

The server is free to play but the necessary upkeep is not. Donations are welcome and appreciated, but they are just that, donations. Find more information about this on the [website](https://vanillaplus.org/), under the `Support Project` and `Rewards` menu points.

Bringing positive attention to the server is also a great way to help the project. A good example of this would be raising the attention of like minded individuals, such as creating content on twitch or youtube (see [Hamsterwheel](https://www.youtube.com/channel/UCQkKf5qwYKyJlyhZPbdAVmw)). A bad example would be spamming forums and competitors with links to the server. Committing acts of terror to coerce people to play on the server is also shunned. Please do **NOT** engage in war crimes to make the server more popular.

## Addons

There are some community developed addons that are made specificly for the server, but any addon made for `1.12.1` will work. Some have dependencies that you will need to install so always read the readme file.
You may also want to check the pinned messages of the #addons channel and may ask for help on [Discord](https://discord.com/invite/CfC8PGmg?utm_source=https://github.com/KrekoG/vanillaplus&utm_medium=Connect). If you can't find your addon folder at `<wow folder>\Interface\AddOns`, starting the game successfully will create it for you.

### Server specific addons:
- [AtlasLoot Enhanced for Vanilla+](https://github.com/hawaiisa/Atlas)
- [BloodlustHelper](https://github.com/KrekoG/BloodlustHelper)
- [pfUI Vanilla Plus](https://github.com/heroclastus09/pfui-vanillaplus)

### Addons maintained by the community:
- [SkelaCustomNameplates](https://github.com/KrekoG/SkelaCustomNameplates)
- [SpecialTalentUI](https://github.com/KrekoG/SpecialTalentUI)
- [ag_UnitFrames](https://github.com/KrekoG/ag_UnitFrames)

### Lists of other resources:
- [decaedent.github.io](https://decaedent.github.io/wow/vadp.html)

## Other modifications

These are patches that changes the way the game looks. Use them with care, some may not remain always compatible, as they are not maintained by the sever, or the community. To make sure the load order does not break, ensure that the name of the file is later in the alphabetical order than `patch-3.MPQ`. (For example `patch-A.MPQ`)

- [Very Dark Night Mod 1.12.1](https://discord.com/channels/530653671193706496/730518138831241297/893600417064321074) - credit: Wizdom
- [Leeviathan's WoD Character Models](https://model-changing.net/gc/11-leeviathans-wod-character-models/) - credit: Thirinena


## About

This document is currently maintained by [KrekoG](https://github.com/KrekoG/).

If you find any inaccuracies, grammatical errors or would like to suggest (or even write) additions, please contact me on github or discord.