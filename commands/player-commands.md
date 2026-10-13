---
title: Player Commands - Arkon Commands for Ark Server Players
description: Commands every player can use on an Arkon-managed Ark server: registration, the shop, lootboxes, tribe log threads, map tools and leaderboards.
published: true
date: 2026-10-12T00:00:00.000Z
tags: commands, player, reference
editor: markdown
dateCreated: 2023-12-25T18:45:05.484Z
---

# Ark Player Commands (Arkon)

These are the Arkon commands any member can use: link your Discord account to your character, buy items in the shop, open lootboxes, manage your tribe log thread, hunt dinos and check the leaderboards. New player? Read the [Player Guide](/guides/player-getting-started) first.

**How to read this page**

- Type commands in any Discord channel Arkon can see. The default prefix is `+`.
- `<value>` means you must fill it in. `[value]` means it is optional.
- **Who can use it:** *Admin* and *Mod* are the roles you set when you [set up Arkon](/guides/getting-started). *Everyone* means any member. *Server owner* means the owner of the Discord server.
- 🔹 needs [ArkView](/guides/arkview). 🔸 is for Xbox / Microsoft Store ASE servers only.
- Each section links to the guide that explains the commands step by step.

Full details for every command are on the [All Commands](/commands/all-commands) page.

## Turn On RCON and Find Your RCON Details

Guide: [Turn On RCON and Find Your RCON Details](/guides/rcon-setup)

| Command | What it does | Who |
|---|---|---|
| `+rconhelp` | Get a guide for finding your ARK server's RCON port and admin password | Everyone |

## Live Server Status Channel and Player Count Graphs

Guide: [Live Server Status Channel and Player Count Graphs](/guides/status-channel)

| Command | What it does | Who |
|---|---|---|
| `+servergraph [timespan] [clusters_only] [include_total] [search_query] [start_time] [end_time]` | See how your player count changed over time. | Everyone |
| `+playercounts [local]` | View player counts either globally or locally | Everyone |

## Player Registration

Guide: [Player Registration: Link Discord Accounts to Ark Players](/guides/player-registration)

| Command | What it does | Who |
|---|---|---|
| `+register [username]` | Register your in-game account with the database. | Everyone |
| `+unregister` | Unregister yourself | Everyone |
| `+specimen <specimen_number>` | Set your specimen number to use the Rshop | Everyone |
| `+findsurvivor <survivor_name>` | Look up a survivor by character name. | Everyone |
| `+kickme` | Kick your character from the server. | Everyone |

## The RCON Shop (Rshop)

Guide: [The RCON Shop (Rshop): Sell In-Game Items](/guides/rshop)

| Command | What it does | Who |
|---|---|---|
| `+rshop [item]` | Open the in-game RCON shop. | Everyone |
| `/quickbuy <item> [quantity] [quality] [blueprint]` | Buy something from the shop without opening the menu. | Everyone |
| `+shopoverview` | Generate a visual summary of the guild's shop economy. | Everyone |
| `+shopsettings` | Show the current shop configuration for this guild.   Examples: - +shopsettings | Everyone |
| `+shopstats [user]` | Show purchase stats for you or another member. | Everyone |

## Lootboxes

Guide: [Lootboxes](/guides/lootboxes)

| Command | What it does | Who |
|---|---|---|
| `+lootbox` | Open a lootbox | Everyone |

## Tribe Logs in Discord and Private Tribe Threads

Guide: [Tribe Logs in Discord and Private Tribe Threads](/guides/tribe-logs)

| Command | What it does | Who |
|---|---|---|
| `+tribe [user]` | Open the tribe menu! | Everyone |
| `+threadadd <member>` | Add a member to your tribelog thread | Everyone |
| `+threadkick <member>` | Remove a member from your tribelog thread | Everyone |
| `+threadpurge <confirm>` | Remove ALL members from your tribelog thread except yourself | Everyone |
| `+threadmembers` | List all members in your tribelog thread | Everyone |
| `+threadtransfer <member>` | Transfer thread ownership to another member | Everyone |

## Map Tools

Guide: [Map Tools: Hunt Dinos, Find Tames and Map Structures](/guides/map-tools)

| Command | What it does | Who |
|---|---|---|
| `+hunt <dino>` 🔹 | Hunt for a dino! | Everyone |
| `+findtame <search_query>` 🔹 | Find tames by tame name, imprinter, tamer, or tribe name | Everyone |
| `+mytames` 🔹 | Check your tribe's tames on a map | Everyone |
| `+mystructures` 🔹 | Count structures near your last known location on a map | Everyone |
| `+mapstats` 🔹 | Get detailed stats for a map | Everyone |
| `+creaturepie [count]` 🔹 | Get a pie chart of wild dinos on a map | Everyone |
| `+structurepie [count]` 🔹 | Get pie chart of structures | Everyone |
| `+tamepie [count]` 🔹 | Get a pie chart of tamed dinos on a map | Everyone |
| `+playerheat` 🔹 | Get a heatmap of player locations | Everyone |
| `+arkviewer` 🔹 | Quickly view your servers' ArkView metrics | Everyone |

## Player Stats and Leaderboards

Guide: [Player Stats and Leaderboards](/guides/stats-and-leaderboards)

| Command | What it does | Who |
|---|---|---|
| `+playerstats [player]` | View info about a player | Everyone |
| `+players [timespan] [cluster]` | Show the playtime leaderboard. | Everyone |
| `+clusterlb [sort_by]` | Show the top players on a specific cluster. | Everyone |
| `+tribelb <sort_by> [cluster]` | See which tribes are leading the pack. | Everyone |
| `+dbstats [showglobal]` | Show ArkTools stats for this guild or globally. | Everyone |

## Xbox and Microsoft Store Features

Guide: [Xbox and Microsoft Store Features](/guides/xsapi)

| Command | What it does | Who |
|---|---|---|
| `+addme` 🔸 | (Xbox/Win10 CROSSPLAY ONLY)Add yourself as a friend | Everyone |
| `+inviteme` 🔸 | Get an Xbox game invite to one of our servers | Everyone |
