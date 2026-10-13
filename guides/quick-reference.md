---
title: Quick Reference - Arkon Ark Discord Bot
description: One-page cheat sheet of every Arkon command for your Ark Discord server, grouped by Players, Mods and Admins, with a link to the guide for each task.
published: true
date: 2026-10-12T00:00:00.000Z
tags: commands, reference, quick-start, cheat-sheet
editor: markdown
dateCreated: 2026-01-17T00:00:00.000Z
---

# Quick Reference

This page lists every Arkon command in one place, grouped by who uses it. Find the command, read the one-line summary, then follow the link to the guide if you need the steps.

The default prefix is `+`. Type `<value>` for a value you must give and `[value]` for one you may skip. Do not type the brackets.

> Each command works only for the people listed in its group, and some are open to everyone. Admin and Mod are roles you pick in Discord. See [Getting Started](/guides/getting-started) to set them.
{.is-info}

**Markers on this page:**

- 🔹 needs ArkView (the free helper program that reads your Ark save file). Set it up in [ArkView setup](/guides/arkview).
- 🔸 works only for Xbox / Microsoft Store ASE servers. See [Xbox features](/guides/xsapi).

Commands marked "also works as /command" are not listed twice: any command that has a slash version also runs with `/`.

---

## Players

Players need to link their Discord to their in-game character first. The steps are in [Player Getting Started](/guides/player-getting-started).

### Register and set up your account

| Command | What it does | Guide |
|---|---|---|
| `+register` | Links your Discord account to your in-game character | [Registration](/guides/player-registration) |
| `+unregister` | Removes your own link | [Registration](/guides/player-registration) |
| `+specimen <number>` | Saves your specimen (implant) number, needed for the shop | [Registration](/guides/player-registration) |
| `+kickme` | Kicks your own character so you can rejoin | [Registration](/guides/player-registration) |
| `+findsurvivor <name>` | Finds players by their in-game character name | [Registration](/guides/player-registration) |
| `+addme` 🔸 | Asks the host Gamertag to add you as a friend | [Xbox features](/guides/xsapi) |
| `+inviteme` 🔸 | Sends you an Xbox game invite to a server | [Xbox features](/guides/xsapi) |

### Shop, paydays and lootboxes

| Command | What it does | Guide |
|---|---|---|
| `+rshop` | Opens the RCON shop (buy items that arrive in your game) | [RCON shop](/guides/rshop) |
| `+quickbuy` | Buys a shop item without opening the menu | [RCON shop](/guides/rshop) |
| `+shopsettings` | Shows how the shop is set up on this Discord | [RCON shop](/guides/rshop) |
| `+shopstats [member]` | Shows purchase stats for you or another member | [RCON shop](/guides/rshop) |
| `+shopoverview` | Makes a picture summary of the shop economy | [RCON shop](/guides/rshop) |
| `+lootbox` | Opens a lootbox | [Lootboxes](/guides/lootboxes) |

### In-game chat commands

Type these inside the game chat. They start with `/`, `!` or `+`. An admin must switch on kit, payday, imstuck, the votes and rename first. The rest are always on.

| Command | What it does | Guide |
|---|---|---|
| `kit` (short: `k`) | Gives your one-time starter kit | [In-game commands](/guides/in-game-commands) |
| `payday` (short: `pd`) | Gives a reward you can claim again after a wait | [In-game commands](/guides/in-game-commands) |
| `imstuck` (short: `is`) | Gives a care package of basic items | [In-game commands](/guides/in-game-commands) |
| `voteday` (`vd`), `votenight` (`vn`) | Players vote to make it day or night | [In-game commands](/guides/in-game-commands) |
| `votedinowipe` (`vdw`) | Players vote to wipe all wild dinos | [In-game commands](/guides/in-game-commands) |
| `votecleanup` (`cleanup`) | Players vote to remove beaver dams and spoiled eggs | [In-game commands](/guides/in-game-commands) |
| `rename <new name>` (`rn`) | Changes your character name | [In-game commands](/guides/in-game-commands) |
| `players` (`online`) | Says how many people are on this server | [In-game commands](/guides/in-game-commands) |
| `mytames` (`tames`) 🔹 | Counts your tribe's tames on this map | [In-game commands](/guides/in-game-commands) |
| `register <Discord name or ID>` (`reg`) | Links your Discord to your character | [Registration](/guides/player-registration) |
| `unregister` (`unreg`) | Unlinks your Discord | [Registration](/guides/player-registration) |
| `specimen <number>` (`spec`) | Saves your specimen number | [Registration](/guides/player-registration) |
| `testreg` | Shows which character Arkon matched you to | [In-game commands](/guides/in-game-commands) |
| `help` (short: `commands`) | Lists the in-game commands that are switched on | [In-game commands](/guides/in-game-commands) |

### Tribe logs

| Command | What it does | Guide |
|---|---|---|
| `+tribe` | Opens the tribe menu (claim your tribe log thread) | [Tribe logs](/guides/tribe-logs) |
| `+threadadd` | Adds a member to your tribe log thread | [Tribe logs](/guides/tribe-logs) |
| `+threadkick` | Removes a member from your thread | [Tribe logs](/guides/tribe-logs) |
| `+threadmembers` | Lists who is in your thread | [Tribe logs](/guides/tribe-logs) |
| `+threadpurge` | Removes everyone from your thread except you | [Tribe logs](/guides/tribe-logs) |
| `+threadtransfer` | Gives your thread to another member | [Tribe logs](/guides/tribe-logs) |

### Stats and leaderboards

| Command | What it does | Guide |
|---|---|---|
| `+playerstats` | Shows a stats card for a player | [Stats and leaderboards](/guides/stats-and-leaderboards) |
| `+players` | Shows the playtime leaderboard | [Stats and leaderboards](/guides/stats-and-leaderboards) |
| `+clusterlb` | Shows the top players on one cluster | [Stats and leaderboards](/guides/stats-and-leaderboards) |
| `+tribelb <sort>` | Ranks tribes (for example by kills) | [Stats and leaderboards](/guides/stats-and-leaderboards) |
| `+dbstats` | Shows Arkon's stats for this Discord | [Stats and leaderboards](/guides/stats-and-leaderboards) |
| `+playercounts [local]` | Lists live player counts as text | [Status channel](/guides/status-channel) |
| `+servergraph [timespan]` | Draws a graph of player counts over time | [Status channel](/guides/status-channel) |

### Map tools 🔹

An admin must have set up [ArkView](/guides/arkview) first.

| Command | What it does | Guide |
|---|---|---|
| `+hunt` | Finds wild dinos on the map | [Map tools](/guides/map-tools) |
| `+findtame` | Finds tames by name, imprinter, tamer or tribe | [Map tools](/guides/map-tools) |
| `+mytames` | Shows your tribe's tames on a map | [Map tools](/guides/map-tools) |
| `+mystructures` | Counts structures near your last known spot | [Map tools](/guides/map-tools) |
| `+mapstats` | Shows detailed stats for a map | [Map tools](/guides/map-tools) |
| `+playerheat` | Draws a heatmap of where players are | [Map tools](/guides/map-tools) |
| `+creaturepie` | Pie chart of wild dinos | [Map tools](/guides/map-tools) |
| `+tamepie` | Pie chart of tamed dinos | [Map tools](/guides/map-tools) |
| `+structurepie` | Pie chart of structures | [Map tools](/guides/map-tools) |
| `+arkviewer` | Shows when each map's ArkView data was last updated | [Map tools](/guides/map-tools) |

### Setup help

| Command | What it does | Guide |
|---|---|---|
| `+rconhelp` | Shows how to find your server's RCON port and admin password | [RCON setup](/guides/rcon-setup) |

---

## Mods

Mods can run everything in the Players section too.

### Player lookups and history

| Command | What it does | Guide |
|---|---|---|
| `+lookback <player> <start> [end]` | Finds where a player was online in a time window | [Chat and logs](/guides/chat-and-logs) |
| `+whowason <time>` | Lists everyone online at one moment | [Chat and logs](/guides/chat-and-logs) |
| `+timeline <player>` | Shows a player's join and leave timeline | [Chat and logs](/guides/chat-and-logs) |
| `+joinlog` | Shows the join and leave log for a server | [Chat and logs](/guides/chat-and-logs) |
| `+totalplaytime` | Adds up a player's playtime between two dates | [Stats and leaderboards](/guides/stats-and-leaderboards) |
| `+arkset view` | Shows your current Arkon settings card | [Server settings](/guides/server-settings) |
| `+unregisterplayer` | Removes the link between a Discord account and a player | [Registration](/guides/player-registration) |
| `+susrating <player>` 🔸 | Rates how likely an Xbox account is to be an alt | [Xbox features](/guides/xsapi) |
| `+tamesfor` 🔹 | Shows another tribe's tames on a map | [Map tools](/guides/map-tools) |

### Bans

| Command | What it does | Guide |
|---|---|---|
| `+banplayer` | Bans a player from all servers | [Moderation](/guides/moderation) |
| `+tempbanplayer` | Bans a player for a set time | [Moderation](/guides/moderation) |
| `+unbanplayer` | Lifts a ban | [Moderation](/guides/moderation) |
| `+banfromtext` | Bans a list of player IDs | [Moderation](/guides/moderation) |
| `+unbanfromtext` | Unbans a list of player IDs | [Moderation](/guides/moderation) |
| `+bans` | Shows and manages bans | [Moderation](/guides/moderation) |
| `+globalbans` | Shows bans across all servers | [Moderation](/guides/moderation) |

### Map lookups 🔹

| Command | What it does | Guide |
|---|---|---|
| `+findplayer` | Finds a player's location and tribe in the game | [Map tools](/guides/map-tools) |
| `+findtribe` | Finds a tribe's details | [Map tools](/guides/map-tools) |
| `+structures` | Draws a map of a tribe's structures | [Map tools](/guides/map-tools) |
| `+finditem` | Searches the map for a specific item | [Map tools](/guides/map-tools) |
| `+findexpired` | Lists tribes that have been inactive for X days | [Anti-cheat](/guides/anti-cheat) |

### Server control

| Command | What it does | Guide |
|---|---|---|
| `+rcon` | Runs an RCON command on a server | [Server control](/guides/server-control) |
| `+doexit` | Shuts a server down with a countdown | [Server control](/guides/server-control) |
| `+dorestartlevel` | Restarts a server without a full shutdown | [Server control](/guides/server-control) |
| `+clearall` | Clears the inventory of every player on a server | [Server control](/guides/server-control) |
| `+equipall` | Gives every player a set of items (event helper) | [Server control](/guides/server-control) |
| `+unhex` | Turns a hex string back into readable text | [Server control](/guides/server-control) |
| `+pollvotetime` | Checks how much playtime each poll voter has | [Server control](/guides/server-control) |
| `+pollvotefilter` | Filters poll votes from players who have not played on a cluster | [Server control](/guides/server-control) |

### Security

| Command | What it does | Guide |
|---|---|---|
| `+rdpdupe` (view, toggle, action, channel, whitelist) | Sets up RDP dupe protection | [Security](/guides/security) |

---

## Admins

Admins can run everything in the Players and Mods sections too. Two commands need the Discord server owner: `+arkset tempbandefault` and `+arkset regenkey`.

### First-time setup

| Command | What it does | Guide |
|---|---|---|
| `/setup` (slash command only) | Starts the guided setup wizard | [Getting Started](/guides/getting-started) |
| `+set roles addadminrole <role>` | Chooses which role counts as Admin | [Getting Started](/guides/getting-started) |
| `+set roles addmodrole <role>` | Chooses which role counts as Mod | [Getting Started](/guides/getting-started) |
| `+checklist` | Shows what is and is not set up yet | [Getting Started](/guides/getting-started) |
| `+viewservers` | Opens the server and cluster menu | [Server settings](/guides/server-settings) |
| `+addcluster` / `+delcluster` | Adds or deletes a cluster (a group of linked servers) | [Server settings](/guides/server-settings) |
| `+addserver` / `+delserver` | Adds or deletes a server | [Server settings](/guides/server-settings) |

### General settings (`+arkset`)

| Command | What it does | Guide |
|---|---|---|
| `+arkset timezone` | Sets your time zone | [Server settings](/guides/server-settings) |
| `+arkset clustertype` | Sets whether your servers are Xbox, Steam or both | [Server settings](/guides/server-settings) |
| `+arkset eventlog` | Sets the event log channel | [Server settings](/guides/server-settings) |
| `+arkset alertchannel` | Sets the channel for alerts | [Server settings](/guides/server-settings) |
| `+arkset retention` | Sets how many days of player count history to keep | [Server settings](/guides/server-settings) |
| `+arkset usedisplaynames` | Switches Discord names to display names in game chat | [Server settings](/guides/server-settings) |
| `+arkset recentlycreated` | Lists players created after a date | [Server settings](/guides/server-settings) |
| `+arkset exportregisteredplayers` | Exports registered players to a CSV file | [Server settings](/guides/server-settings) |
| `+arkset wipeclusterstats` | Resets player stats for a cluster | [Server settings](/guides/server-settings) |
| `+arkset wipeclusterimplants` | Resets specimen numbers for a cluster | [Server settings](/guides/server-settings) |
| `+arkset wipeclustertribes` | Resets player tribes for a cluster | [Server settings](/guides/server-settings) |
| `+arkset tempbandefault` | Sets the default temp ban length (server owner) | [Server settings](/guides/server-settings) |
| `+arkset regenkey` | Makes a new ArkView API key (server owner) | [ArkView setup](/guides/arkview) |

### Status channel

| Command | What it does | Guide |
|---|---|---|
| `+serverstatus` (view, channel, time, init) | Sets up the live server status message | [Status channel](/guides/status-channel) |

### Playtime, roles and welcomes

| Command | What it does | Guide |
|---|---|---|
| `+arkset linkrole` / `unlinkrole` | Adds or removes a playtime role | [Playtime and roles](/guides/playtime-and-roles) |
| `+arkset viewranks` | Lists your playtime roles | [Playtime and roles](/guides/playtime-and-roles) |
| `+arkset initroles` | Gives players the roles they have earned | [Playtime and roles](/guides/playtime-and-roles) |
| `+arkset autoremoverole` | Removes the previous playtime role when a new one is earned | [Playtime and roles](/guides/playtime-and-roles) |
| `+arkset autowelcome` / `autowelcomemessage` | Welcomes new players and sets the message | [Playtime and roles](/guides/playtime-and-roles) |
| `+arkset autoinvite` / `invitelink` | Posts your Discord invite in game when players mention discord | [Playtime and roles](/guides/playtime-and-roles) |
| `+arkset registerrole` | Sets the role needed to register | [Registration](/guides/player-registration) |
| `+arkset resetplaytime` (all, cluster, server, player) | Resets playtime | [Playtime and roles](/guides/playtime-and-roles) |
| `+setplayertime` | Sets one player's tracked playtime | [Playtime and roles](/guides/playtime-and-roles) |

### Registration tools

| Command | What it does | Guide |
|---|---|---|
| `+registerplayer` | Registers another user for them | [Registration](/guides/player-registration) |
| `+setplayerimplant` | Sets the specimen number for a player | [Registration](/guides/player-registration) |

### In-game commands setup

| Command | What it does | Guide |
|---|---|---|
| `+arkset ingame` (kit, payday, imstuck, autokit and their path and cooldown settings) | Turns the in-game commands on and sets their items | [In-game commands](/guides/in-game-commands) |
| `+resetkit <gameid>` | Lets one player claim the kit again | [In-game commands](/guides/in-game-commands) |
| `+resetclusterkits <cluster>` | Lets everyone claim the kit again | [In-game commands](/guides/in-game-commands) |

### Shop setup

| Command | What it does | Guide |
|---|---|---|
| `+rshopset template` / `download` / `upload` | Gets the shop spreadsheet, exports it, and uploads your prices | [RCON shop](/guides/rshop) |
| `+rshopset view` | Shows the current shop settings | [RCON shop](/guides/rshop) |
| `+rshopset discount` / `discountrole` / `discountdays` | Sets flat, role and weekday discounts | [RCON shop](/guides/rshop) |
| `+rshopset autorefund` | Turns automatic refunds for failed purchases on or off | [RCON shop](/guides/rshop) |
| `+rshopset qualityexp` / `maxquality` / `maxbpquality` / `bpmultiplier` | Controls quality limits and blueprint pricing | [RCON shop](/guides/rshop) |
| `+rshopset delimiter` / `readstacks` | Pack separator and stack sizes from Game.ini | [RCON shop](/guides/rshop) |
| `+arkset toggleshop` / `toggleshopcluster` | Turns the shop on or off | [RCON shop](/guides/rshop) |
| `+arkset shoplog` | Sets the shop log channel | [RCON shop](/guides/rshop) |
| `+arkset refundclusterdelta` / `refundserverdelta` / `refundplaytimedelta` | Refunds purchases or credits playtime within a time window | [RCON shop](/guides/rshop) |

### Lootbox setup

| Command | What it does | Guide |
|---|---|---|
| `+lootboxset` (view, price, cooldown, logchannel, toggle) | Sets how lootboxes work | [Lootboxes](/guides/lootboxes) |
| `+lootboxset template` / `download` / `upload` / `add` | Builds the lootbox item list | [Lootboxes](/guides/lootboxes) |
| `+lootboxset simulate` | Tests a lootbox many times and shows the results | [Lootboxes](/guides/lootboxes) |

### Tribe log setup

| Command | What it does | Guide |
|---|---|---|
| `+tribeset` (view, logchannel, claimrole, claimchannel, resetclaims, unclaim) | Sets up tribe logs and private threads | [Tribe logs](/guides/tribe-logs) |
| `+cleantribelogs` | Deletes threads not tied to any tribe | [Tribe logs](/guides/tribe-logs) |

### Chat and game messages

| Command | What it does | Guide |
|---|---|---|
| `+arkset killfeed` | Turns the kill feed on or off | [Chat and logs](/guides/chat-and-logs) |

### Moderation tools

| Command | What it does | Guide |
|---|---|---|
| `+warntribe` | Warns every member of a tribe | [Moderation](/guides/moderation) |
| `+tribenote` | Adds a note to every member of a tribe | [Moderation](/guides/moderation) |
| `+bantribe` / `+tempbantribe` | Bans every member of a tribe | [Moderation](/guides/moderation) |
| `+syncbans` (all, fromdb, fromserver, betweenservers) | Syncs bans between servers and Arkon | [Moderation](/guides/moderation) |
| `+suswatch` | Adds or removes players on the watchlist | [Moderation](/guides/moderation) |

### Server control

| Command | What it does | Guide |
|---|---|---|
| `+scheduledrcon` | Schedules an RCON command to run later | [Server control](/guides/server-control) |
| `+bulksend` (also works as /bulksend) | Sends the same item to a player many times | [Server control](/guides/server-control) |
| `+excelsend` | Sends in-game commands from a spreadsheet | [Server control](/guides/server-control) |
| `+dummywall` / `+dummyfloor` | Builds spawn commands for a loadout dummy wall or floor | [Server control](/guides/server-control) |
| `+remreacts` | Removes reactions from a message | [Server control](/guides/server-control) |
| `+arkset countdown` | Sets the shutdown and restart countdowns | [Server control](/guides/server-control) |
| `+arkset commandblacklist` | Lists in-game admin commands that get a player banned when they use them | [Security](/guides/security) |
| `+arkset modcommands` | Chooses which commands plain mods may use | [Server control](/guides/server-control) |
| `+arkset ansicolors` | Turns colors in RCON output on or off | [Server control](/guides/server-control) |

### Security

| Command | What it does | Guide |
|---|---|---|
| `+arkset banimposters` | Turns imposter protection on or off | [Security](/guides/security) |
| `+arkset imposterwhitelist` | Adds a game ID to the imposter safe list | [Security](/guides/security) |
| `+arkset characternameblacklist` | Blocks character names | [Security](/guides/security) |
| `+getips` 🔹 | Gets a list of player IPs | [Security](/guides/security) |

### ArkView map setup and checks 🔹

| Command | What it does | Guide |
|---|---|---|
| `+avsync` | Syncs tribes, players and characters with the database | [Map tools](/guides/map-tools) |
| `+servermetrics` / `+viewsysinfo` | Shows server memory use and the machine your servers run on | [Map tools](/guides/map-tools) |
| `+setcustomdinos` / `showcustomdinos` / `clearcustomdinos` | Manages custom dinos for hunt and findtame | [Map tools](/guides/map-tools) |
| `+findstructure` | Maps specific structures for a tribe or the whole map | [Map tools](/guides/map-tools) |
| `+structuregraph` / `+territory` / `+tribesize` | Shows which areas tribes control | [Map tools](/guides/map-tools) |
| `+sortdinos` | Lists dinos at or above a level | [Map tools](/guides/map-tools) |
| `+finddbtribe` | Finds a tribe in Arkon's own records (works without ArkView) | [Anti-cheat](/guides/anti-cheat) |

### Anti-cheat 🔹

| Command | What it does | Guide |
|---|---|---|
| `+setvalidservers` / `+showvalidservers` | Sets or shows the servers tames may come from | [Anti-cheat](/guides/anti-cheat) |
| `+scanforeigntames` | Finds tames from servers not on your list | [Anti-cheat](/guides/anti-cheat) |
| `+tamedupes` | Finds the same tame copied many times | [Anti-cheat](/guides/anti-cheat) |
| `+checkmassbreed` | Finds areas where dinos were left breeding | [Anti-cheat](/guides/anti-cheat) |
| `+tamestatcheck` | Finds tames that hit a stat goal | [Anti-cheat](/guides/anti-cheat) |
| `+uncryocheck` | Lists tribes over the uncryo limit | [Anti-cheat](/guides/anti-cheat) |
| `+arkset uncryolimit` | Sets how many uncryoed tames a tribe may have | [Anti-cheat](/guides/anti-cheat) |
| `+wipetribes` | Wipes tribes inactive for X days | [Anti-cheat](/guides/anti-cheat) |

### Xbox features 🔸

| Command | What it does | Guide |
|---|---|---|
| `+xsapi authenticate` | Signs in a host Gamertag | [Xbox features](/guides/xsapi) |
| `+xsapi inviteauth` | Allows the host Gamertag to send game invites | [Xbox features](/guides/xsapi) |
| `+xsapi view` / `viewhosts` | Shows Xbox settings and hosts | [Xbox features](/guides/xsapi) |
| `+xsapi autofriend` (toggle, unfriendtime) | Controls the auto-friend system | [Xbox features](/guides/xsapi) |
| `+xsapi altdetection` (toggle, autoban, channel, threshold, whitelist) | Controls alt detection | [Xbox features](/guides/xsapi) |
| `+xsapi friendrequests` / `friendinvites` / `cleanfriends` / `dumpfriends` | Looks at and trims host friend lists | [Xbox features](/guides/xsapi) |
| `+xsapi gettokens` | Posts a host's login tokens as a file. Use only in a private admin channel | [Xbox features](/guides/xsapi) |
| `+addplayer` / `+removeplayer` | Adds or removes a player on the host's friend list | [Xbox features](/guides/xsapi) |
| `+xdm <player> <message>` | Sends a player an Xbox message | [Xbox features](/guides/xsapi) |

---

## More help

- [Full command lists](/commands/all-commands): [Admin](/commands/admin-commands), [Mod](/commands/mod-commands), [Player](/commands/player-commands)
- [Ark RCON console commands](/guides/ark-rcon-commands): raw game commands for `+rcon`
- [Free vs Premium](/guides/premium): which features have limits
- [FAQ and troubleshooting](/guides/faq) and [Glossary](/guides/glossary)
- [Discord Support](https://discord.gg/RaR3wR4MgY)
