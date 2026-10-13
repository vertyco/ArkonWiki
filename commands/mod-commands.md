---
title: Mod Commands - Arkon Moderator Reference for Ark Servers
description: Arkon moderator commands for Ark servers: bans, player lookups, join logs, map investigation tools and RCON, with links to step-by-step guides.
published: true
date: 2026-10-12T00:00:00.000Z
tags: commands, moderator, reference
editor: markdown
dateCreated: 2023-12-25T19:30:10.837Z
---

# Ark Moderator Commands (Arkon)

These are the commands for people with your Mod role: banning and unbanning players, looking up who was online, finding players and structures on the map, and running RCON commands. Admins can use them too.

**How to read this page**

- Type commands in any Discord channel Arkon can see. The default prefix is `+`.
- `<value>` means you must fill it in. `[value]` means it is optional.
- **Who can use it:** *Admin* and *Mod* are the roles you set when you [set up Arkon](/guides/getting-started). *Everyone* means any member. *Server owner* means the owner of the Discord server.
- 🔹 needs [ArkView](/guides/arkview). 🔸 is for Xbox / Microsoft Store ASE servers only.
- Each section links to the guide that explains the commands step by step.

Full details for every command are on the [All Commands](/commands/all-commands) page.

## Server Settings

Guide: [Server Settings: Clusters, Servers and Bot Settings](/guides/server-settings)

| Command | What it does | Who |
|---|---|---|
| `+arkset view` | View ark settings | Mod |

## Player Registration

Guide: [Player Registration: Link Discord Accounts to Ark Players](/guides/player-registration)

| Command | What it does | Who |
|---|---|---|
| `+unregisterplayer <player>` | Unlink the discord account from a player | Mod |

## Game Chat in Discord, Kill Feed and Join Logs

Guide: [Game Chat in Discord, Kill Feed and Join Logs](/guides/chat-and-logs)

| Command | What it does | Who |
|---|---|---|
| `+joinlog <timespan> [end_time]` | Show the join/leave log for a server over a time period. | Mod |
| `+whowason <time>` | List everyone who was online at a specific moment. | Mod |
| `+timeline <search_query> <start_time> [end_time]` | Show a player's join and leave timeline. | Mod |
| `+lookback <search_query> <start_time> [end_time]` | Find where a player was online during a specific window. | Mod |

## Moderation

Guide: [Moderation: Bans, Temp Bans and Tribe Warnings](/guides/moderation)

| Command | What it does | Who |
|---|---|---|
| `+banplayer <game_id> <reason>` | Ban a player from all servers | Mod |
| `+tempbanplayer <game_id> [duration] [reason]` | Temporarily ban a player from all servers | Mod |
| `+unbanplayer <game_id> [reason]` | Unban a player from all servers | Mod |
| `+bans [query]` | Manage player bans | Mod |
| `+globalbans [query]` | View global player bans | Mod |
| `+banfromtext` | Ban players from a list of player IDs | Mod |
| `+unbanfromtext` | Unban players from a list of player IDs. | Mod |

## Server Control

Guide: [Server Control: RCON Commands, Schedules and Restarts](/guides/server-control)

| Command | What it does | Who |
|---|---|---|
| `+rcon <cluster> <server> <command>` | Run an RCON command | Mod |
| `+doexit <cluster> <server> [countdown]` | Shut a game server down completely. | Mod |
| `+dorestartlevel <cluster> <server> [countdown]` | Restart a server without a full shutdown. | Mod |
| `/bulksend <cluster> <server> <implant> <item> <amount> <runcount> [quality] [blueprint]` | Bulk send an item to a player | Members with the Kick Members permission |
| `+clearall <cluster> <server> [inventory] [hotbar] [equipped]` | Clear inventory of all players in the server. | Mod |
| `+equipall <cluster> <server>` | - | Mod |
| `+pollvotetime <message> [cluster] [use_maptime]` | Check how much playtime each poll voter has logged. | Mod |
| `+pollvotefilter <message> <cluster_name> [this_wipe]` | Filter poll votes from players who haven't played on a cluster. | Mod |
| `+unhex <text>` | Unhex a string | Mod |

## Security

Guide: [Security: RDP Dupes, Imposters and Name Blacklist](/guides/security)

| Command | What it does | Who |
|---|---|---|
| `+rdpdupe <subcommand>` | Configure RDP dupe protection | Mod |
| `+rdpdupe action <action>` | Set the enforcement action: `kick` or `ban` | Mod |
| `+rdpdupe channel [channel]` | Set (or clear) the channel where RDP dupe alerts are sent. | Mod |
| `+rdpdupe toggle` | Toggle RDP dupe detection on/off | Mod |
| `+rdpdupe view` | View current RDP dupe protection settings | Mod |
| `+rdpdupe whitelist <gameid>` | Add or remove a gameid from the RDP dupe whitelist | Mod |

## Map Tools

Guide: [Map Tools: Hunt Dinos, Find Tames and Map Structures](/guides/map-tools)

| Command | What it does | Who |
|---|---|---|
| `+tamesfor <player>` 🔹 | Check your tribe's tames on a map | Mod |
| `+findplayer <search_query>` 🔹 | Find the location and tribe of a player in-game | Mod |
| `+findtribe <search_query>` 🔹 | Find details of a tribe | Mod |
| `+finditem <item_blueprint> [tribe_id]` 🔹 | Search for a specific item on a map | Mod |
| `+structures <search_query>` 🔹 | Get a marker map of structures for a tribe | Mod |

## Anti-Cheat

Guide: [Anti-Cheat: Dupes, Mass Breeding and Foreign Tames](/guides/anti-cheat)

| Command | What it does | Who |
|---|---|---|
| `+findexpired <days>` 🔹 | Get a list of tribes that haven't been active for more than X days | Mod |

## Player Stats and Leaderboards

Guide: [Player Stats and Leaderboards](/guides/stats-and-leaderboards)

| Command | What it does | Who |
|---|---|---|
| `+totalplaytime <player_query> <start_date> <end_date>` | Calculate a player's total playtime between two dates. | Mod |

## Xbox and Microsoft Store Features

Guide: [Xbox and Microsoft Store Features](/guides/xsapi)

| Command | What it does | Who |
|---|---|---|
| `+susrating <player>` 🔸 | Get a rating for how likely an xbox account is to be an alt | Mod |
