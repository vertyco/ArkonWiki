---
title: Player Commands
description: 
published: true
date: 2026-01-17T18:53:40.115Z
tags: 
editor: markdown
dateCreated: 2023-12-25T18:45:05.484Z
---

# register
 - Usage: `+register [username]`
 - Checks: `server_only`

Register your in-game account with the database.

# addme (Hybrid Command)
 - Usage: `+addme`
 - Slash Usage: `/addme`
 - Checks: `server_only`

(Xbox/Win10 CROSSPLAY ONLY)Add yourself as a friend<br/><br/>Make the host Gamertags add you as a friend<br/><br/>This command requires api keys to be set for the servers

# unregister
 - Usage: `+unregister`
 - Aliases: `unregisterme`
 - Checks: `server_only`

Unregister yourself<br/><br/>Removes you from any Gamertags you have registered to

# setcluster
 - Usage: `+setcluster`
 - Checks: `server_only`

Unregister yourself<br/><br/>Removes you from any Gamertags you have registered to

# dshop (Hybrid Command)
 - Usage: `+dshop [search_query]`
 - Slash Usage: `/dshop [search_query]`
 - Checks: `server_only`

Open the DATA shop<br/><br/>**Arguments**<br/>`search_query: `Search directly for an item

# rshop (Hybrid Command)
 - Usage: `+rshop [search_query]`
 - Slash Usage: `/rshop [search_query]`
 - Checks: `server_only`

Open the RCON shop<br/><br/>**Arguments**<br/>`search_query: `Search directly for an item

# tribe (Hybrid Command)
 - Usage: `+tribe`
 - Slash Usage: `/tribe`
 - Aliases: `mytribe`

Open the tribe menu to view and/or claim your tribes, toggle notifications, and see your tribe stats.

# kicktribemate (Hybrid Command)
 - Usage: `+kicktribemate <member>`
 - Slash Usage: `/kicktribemate <member>`
 - Aliases: `kickmate and kickfromtribelogs`

Kick a member from your tribelog thread

# goldenbullet
 - Usage: `+goldenbullet`
 - Aliases: `gbullet and bullet`
 - Cooldown: `1 per 120.0 seconds`
 - Checks: `server_only`

Get the location of the golden bullet!

# hunt (Hybrid Command)
 - Usage: `+hunt <dino>`
 - Slash Usage: `/hunt <dino>`
 - Cooldown: `1 per 15.0 seconds`
 - Checks: `server_only`

Hunt for a dino!<br/><br/>Use the slash version of this command to make it private!

# findtame (Hybrid Command)
 - Usage: `+findtame <search_query>`
 - Slash Usage: `/findtame <search_query>`
 - Cooldown: `1 per 30.0 seconds`
 - Checks: `server_only`

Find tames by tame name, imprinter, tamer, or tribe name<br/><br/>`search_query` can be one of the following.<br/>The dino's name.<br/>The name of the person who tamed the dino.<br/>The name of the person who imprinted on the tame.<br/>The name of the tribe that owns the dino.<br/>The ID of the tribe that tamed the dino.<br/><br/>*You can search for unclaimed dinos by specifying `unclaimed`*

# mapstats
 - Usage: `+mapstats`
 - Cooldown: `1 per 5.0 seconds`
 - Checks: `server_only`

Get detailed stats for a map

# creaturepie
 - Usage: `+creaturepie [count=10]`
 - Aliases: `wildpie`
 - Cooldown: `1 per 5.0 seconds`
 - Checks: `server_only`

Get a pie chart of wild dinos on a map

# structurepie
 - Usage: `+structurepie [count=10]`
 - Cooldown: `1 per 5.0 seconds`
 - Checks: `server_only`

Get pie chart of structures

# tamepie
 - Usage: `+tamepie [count=10]`
 - Cooldown: `1 per 5.0 seconds`
 - Checks: `server_only`

Get a pie chart of tamed dinos on a map

# players
 - Usage: `+players [cluster=None]`
 - Aliases: `arkleaderboard, arklb, and arktop`
 - Checks: `server_only`

View the playtime leaderboard

# tribelb
 - Usage: `+tribelb <sort_by> [cluster=None]`
 - Aliases: `tribetop`
 - Checks: `server_only`

View leaderboard for all tribes<br/>**Arguments**<br/>`sort_by` - Sort the leaderboard by kills, dinos tamed, or structures destroyed<br/><br/>**Examples**<br/>`+tribelb kills` - Tribe kill leaderboard<br/>`+tribelb tamed` - Tribe tame leaderboard<br/>`+tribelb destroyed` - Tribe destruction leaderboard<br/><br/>*Also accepted: `k`, `t`, or `d`*

# findsurvivor
 - Usage: `+findsurvivor <survivor_name>`
 - Aliases: `findcharname`
 - Checks: `server_only`

Find info about a particular survivor name

# dbstats
 - Usage: `+dbstats`

Stats about the ArkTools database

# servergraph (Hybrid Command)
 - Usage: `+servergraph [timespan=1h] [clusters_only=False] [include_total=False] [search_query]`
 - Slash Usage: `/servergraph [timespan=1h] [clusters_only=False] [include_total=False] [search_query]`
 - Cooldown: `3 per 30.0 seconds`
 - Checks: `server_only`

View a graph of player count over a set time<br/>**Arguments**<br/>`<timespan>` How long to look for, or `all` for all-time data. Defaults to 1 hour.<br/>Must be at least 1 hour.<br/><br/>**Optional Arguments**<br/>`clusters_only:` (True/False) Only show playercounts by cluster, default is False<br/>`include_total:` (True/False) Include another line representing the Total<br/>`search_query: ` Filter by a specific map, cluster, or both<br/><br/>Example: +servergraph 4h<br/>Example: +servergraph 12d<br/>Example: +servergraph 3w2d<br/>Example: +servergraph 7w

# playerstats (Hybrid Command)
 - Usage: `+playerstats [player]`
 - Slash Usage: `/playerstats [player]`
 - Aliases: `player`
 - Checks: `bot_has_server_permissions and server_only`

View info about a player<br/><br/>The optional **player** argument can be one of the following.<br/>- Gamertag or Username<br/>- XUID, Steam ID, PSN ID, or EOS ID<br/>- Discord ID or Username<br/>- @mention

