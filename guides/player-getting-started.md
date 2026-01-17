---
title: Getting Started (Players)
description: 
published: true
date: 2026-01-17T18:53:42.377Z
tags: 
editor: markdown
dateCreated: 2023-12-18T02:19:40.657Z
---

# Player Quickstart
To use some of Arkon's features, there are a few simple steps to get started.

## Linking your Discord
To use features like the Rshop and some in-game commands, you will first need to link your Discord account to your in-game account. The easiest way to do this is from in-game.

Type `+register <YourDiscord>` **IN-GAME** in global chat to link your Discord account.
For example my discord username is vertyco so I would type `+register vertyco` in-game.

> Congrats, your Discord should now be linked! Run `+playerstats` in the Discord to see your in-game player.
> You can now also use the `+rshop` command to purchase items.
{.is-success}

> `+register` also works in Discord, but only for ASE servers.
{.is-info}

### Xbox/PC Crossplay
If the server you play on is hosted via Microsoft store version and has a host Gamertag, you can make the host Gamertag add you as a friend so that you can easily join its session.
Simply run `+addme` and select a server, the host Gamertag for that map will add you as a friend, you can add it back and should then be able to go to its profile page and click `Join Game`

> The server owner needs to authenticate their host gamertags with the Xbox API for this to work
{.is-info}



## In-game commands
The following commands can be typed in-game in global chat. Some require you to register your Specimen # before you can use them with `+specimen <YourSpecimenNumber>`
- `+voteday`: Start a vote session to make it day, if enough people also run the command it will become day.
- `+votenight`: Start a vote session to make it night.
- `+votecleanup`: Start a vote session to clear beaver dams and spoiled eggs from the map.
- `+votedinowipe`: Start a vote session to wipe all wild dinos from the map.
- `+rename`: Rename your character.
- `+imstuck`: If enabled, running this gives you a small care package to unalive yourself if you get stuck 
	- `Requires specimen # to be registered`
- `+unregister`: Unlinks the Discord account associated with your in-game account if there is one.
- `+register`: This command can be used to both link your Discord account and set your specimen number.
- `+implant`: An alias for `+specimen` and `+register`
- `+players`: See how many players are on the server.
- `+payday`: If enabled by the admins, get a reward every X hours you run this.
	- `Requires specimen # to be registered`
- `+help`: View a list of these commands in-game for all to see.
- `+kit`: If enabled by admins, get a one-time starter kit of whatever items are configured.
	- `Requires specimen # to be registered`
  

## Playerstats
To view detailed info for every map you've been on, you can run the `+playerstats` command in Discord.
<img src="/assets/playerstats.png" style="max-width: 50%;"/>
This will track character names, playtimes, kills, deaths, dinos tamed ect..
