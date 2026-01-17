---
title: Admin Commands
description: 
published: true
date: 2025-10-01T02:03:35.431Z
tags: 
editor: markdown
dateCreated: 2023-12-25T19:33:59.122Z
---

# serverstatus
 - Usage: `+serverstatus`
 - Restricted to: `ADMIN`

Server status channel settings

# viewservers
 - Usage: `+viewservers`
 - Restricted to: `ADMIN`
 - Aliases: `ark`

Open the main menu for server management

# addcluster
 - Usage: `+addcluster <name>`
 - Restricted to: `ADMIN`

Create a cluster to add servers to

# delcluster
 - Usage: `+delcluster <cluster_name>`
 - Restricted to: `ADMIN`
 - Aliases: `remcluster`

Delete a cluster

# addserver
 - Usage: `+addserver <cluster_name>`
 - Restricted to: `ADMIN`

Add a server to a cluster

# delserver
 - Usage: `+delserver <cluster_name> <server_name>`
 - Restricted to: `ADMIN`
 - Aliases: `remserver`

Delete a server

# rshopset
 - Usage: `+rshopset`
 - Restricted to: `ADMIN`
 - Aliases: `rss`

Setup the RCON shop

# viewsysinfo
 - Usage: `+viewsysinfo`
 - Restricted to: `ADMIN`
 - Cooldown: `1 per 60.0 seconds`
 - Checks: `server_only`

View data about the system running your servers

# sortdinos
 - Usage: `+sortdinos <level> [dino_name]`
 - Restricted to: `ADMIN`
 - Checks: `server_only`

Find all dinos above or equal to the specified level

# arkset
 - Usage: `+arkset`
 - Restricted to: `ADMIN`
 - Aliases: `arktools`

ArkTools configuration

# xdm (Hybrid Command)
 - Usage: `+xdm <player> <message>`
 - Slash Usage: `/xdm <player> <message>`
 - Restricted to: `ADMIN`
 - Cooldown: `1 per 10.0 seconds`

DM a player on Xbox<br/><br/>The message sender will be the host Gamertag of the last server they were on.

# xsapi
 - Usage: `+xsapi`
 - Restricted to: `ADMIN`

Xbox crossplay tools/settings

# resetkit
 - Usage: `+resetkit <gameid>`
 - Restricted to: `ADMIN`
 - Checks: `server_only`

Reset a players claimed kit

