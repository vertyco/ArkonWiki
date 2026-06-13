---
title: Admin Commands - Arkon Server Owner and Admin Reference
description: Full list of Arkon admin commands for Ark server management. RCON execution, ban sync, player management, scheduled commands, and server configuration.
published: true
date: 2026-06-13T00:00:00.000Z
tags: commands, admin, reference
editor: markdown
dateCreated: 2023-12-25T19:33:59.122Z
---

# Ark Admin Commands (Arkon)

Arkon's admin commands give Ark: Survival Evolved (ASE) and Ark: Survival Ascended (ASA) server owners full control from Discord: RCON execution, cluster and server setup, ban sync, scheduled commands, the RCON shop, and Xbox crossplay tools. Every command below is restricted to the ADMIN role. Looking for raw game console commands instead? See the [Ark RCON Commands](/guides/ark-rcon-commands) reference.


## serverstatus
 - Usage: `+serverstatus`
 - Restricted to: `ADMIN`

Server status channel settings

## viewservers
 - Usage: `+viewservers`
 - Restricted to: `ADMIN`
 - Aliases: `ark`

Open the main menu for server management

## addcluster
 - Usage: `+addcluster <name>`
 - Restricted to: `ADMIN`

Create a cluster to add servers to

## delcluster
 - Usage: `+delcluster <cluster_name>`
 - Restricted to: `ADMIN`
 - Aliases: `remcluster`

Delete a cluster

## addserver
 - Usage: `+addserver <cluster_name>`
 - Restricted to: `ADMIN`

Add a server to a cluster

## delserver
 - Usage: `+delserver <cluster_name> <server_name>`
 - Restricted to: `ADMIN`
 - Aliases: `remserver`

Delete a server

## rshopset
 - Usage: `+rshopset`
 - Restricted to: `ADMIN`
 - Aliases: `rss`

Setup the RCON shop

## viewsysinfo
 - Usage: `+viewsysinfo`
 - Restricted to: `ADMIN`
 - Cooldown: `1 per 60.0 seconds`
 - Checks: `server_only`

View data about the system running your servers

## sortdinos
 - Usage: `+sortdinos <level> [dino_name]`
 - Restricted to: `ADMIN`
 - Checks: `server_only`

Find all dinos above or equal to the specified level

## arkset
 - Usage: `+arkset`
 - Restricted to: `ADMIN`
 - Aliases: `arktools`

ArkTools configuration

## xdm (Hybrid Command)
 - Usage: `+xdm <player> <message>`
 - Slash Usage: `/xdm <player> <message>`
 - Restricted to: `ADMIN`
 - Cooldown: `1 per 10.0 seconds`

DM a player on Xbox<br/><br/>The message sender will be the host Gamertag of the last server they were on.

## xsapi
 - Usage: `+xsapi`
 - Restricted to: `ADMIN`

Xbox crossplay tools/settings

## resetkit
 - Usage: `+resetkit <gameid>`
 - Restricted to: `ADMIN`
 - Checks: `server_only`

Reset a players claimed kit

## Related references
- [All Commands](/commands/all-commands) - complete command list
- [Admin Commands](/commands/admin-commands) - server owner / admin
- [Mod Commands](/commands/mod-commands) - moderator tools
- [Player Commands](/commands/player-commands) - player commands
- [Ark RCON Commands](/guides/ark-rcon-commands) - raw game console reference
- [Getting Started](/guides/getting-started) - connect your first server
