---
title: Mod Commands — Arkon Moderator Reference for Ark Servers
description: Arkon moderator commands for Ark server management. Player investigation, ArkViewer map tools, watchlist, foreign tame detection, and enforcement tools.
published: true
date: 2026-01-17T18:53:37.851Z
tags: commands, moderator, reference
editor: markdown
dateCreated: 2023-12-25T19:30:10.837Z
---

# checkmassbreed
 - Usage: `+checkmassbreed [threshold=0.5] [min_dinos=6]`
 - Restricted to: `MOD`
 - Aliases: `massbreed`
 - Checks: `server_only`

Detect if and where mass breeding is taking place<br/><br/>This command will detect dense clusters of dinos with mating enabled in order to<br/>detect if players have left a bunch of dinos with breeding enabled<br/><br/>A list of "dino clusters" will be returned with coordinates for each cluster and a map of the locations<br/><br/>**Arguments**<br/>- **threshold**: the max latitude/longitude between any two dinos<br/>- **min_dinos**: the minimum amount of mating enabled dinos within the area to be considered "mass breeding"

# findplayer (Hybrid Command)
 - Usage: `+findplayer <search_query>`
 - Slash Usage: `/findplayer <search_query>`
 - Restricted to: `MOD`
 - Checks: `server_only`

Find the location and tribe of a player in-game<br/><br/>`search_query` can be one of the following.<br/>Player's in-game name<br/>Gamertag or Username<br/>Specimen number (exact matches only)<br/>XUID or SteamID (exact matches only)<br/>Tribe ID (exact matches only)

# structures (Hybrid Command)
 - Usage: `+structures <search_query>`
 - Slash Usage: `/structures <search_query>`
 - Restricted to: `MOD`
 - Checks: `server_only`

Get a marker map of structures for a tribe<br/><br/>`search_query` can be one of the following.<br/>- Tribe name<br/>- Tribe ID (exact matches only)

# territory (Hybrid Command)
 - Usage: `+territory [include_other=False] [dotsize=15]`
 - Slash Usage: `/territory [include_other=False] [dotsize=15]`
 - Restricted to: `MOD`
 - Cooldown: `1 per 45.0 seconds`
 - Checks: `server_only`

Visualize controlled areas of a server by tribe.

# findexpired
 - Usage: `+findexpired <days>`
 - Restricted to: `MOD`
 - Aliases: `expired`
 - Checks: `server_only`

Get a list of tribes that haven't been active for more than X days<br/><br/>Example: +findexpired 60<br/>this will show tribes inactive for 60 days or more that have at least 1 structure or tame

# rcon (Hybrid Command)
 - Usage: `+rcon <cluster> <server> <command>`
 - Slash Usage: `/rcon <cluster> <server> <command>`
 - Restricted to: `MOD`
 - Aliases: `run`
 - Checks: `server_only`

Run an RCON command<br/><br/>Note that `+doexit`, `+dorestartlevel`, `+banplayer` and `+unbanplayer`<br/>are standalone commands, running these commands with pure rcon will not use execute<br/>the extra steps associated with these commands like countdowns,<br/>saving, or player blocking.

# banplayer (Hybrid Command)
 - Usage: `+banplayer <player_id> [reason]`
 - Slash Usage: `/banplayer <player_id> [reason]`
 - Restricted to: `MOD`
 - Checks: `server_only`

Ban a player from all servers

# unbanplayer (Hybrid Command)
 - Usage: `+unbanplayer <player_id>`
 - Slash Usage: `/unbanplayer <player_id>`
 - Restricted to: `MOD`
 - Checks: `server_only`

Unban a player from all servers

# doexit (Hybrid Command)
 - Usage: `+doexit <cluster> <server>`
 - Slash Usage: `/doexit <cluster> <server>`
 - Restricted to: `MOD`
 - Checks: `server_only`

Fully shut down a server

# dorestartlevel (Hybrid Command)
 - Usage: `+dorestartlevel <cluster> <server>`
 - Slash Usage: `/dorestartlevel <cluster> <server>`
 - Restricted to: `MOD`
 - Checks: `server_only`

Restart a server

