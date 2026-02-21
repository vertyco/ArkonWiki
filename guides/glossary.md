---
title: Glossary — Ark Server Hosting and Arkon Bot Terminology
description: Definitions of terms used in Arkon and Ark server hosting. Covers clusters, RCON, crossplay, ArkViewer, tribes, cross-chat, and more.
published: true
date: 2026-01-17T00:00:00.000Z
tags: glossary, definitions, terminology
editor: markdown
dateCreated: 2026-01-17T00:00:00.000Z
---

# Glossary

Quick reference for terms used throughout the Arkon wiki.

---

## A

### Admin Role
A Discord role configured with `+set roles addadminrole @role`. Users with this role can use all Arkon commands including server management and RCON access. This is a [Red-DiscordBot](#red-discordbot) feature.

### ArkViewer
A free, open-source plugin that enables advanced map features like `+hunt`, `+findtame`, and detailed tribelogs. [Get ArkViewer](https://github.com/vertyco/arkview)

### ASA (Ark: Survival Ascended)
The 2023 remake of Ark on Unreal Engine 5. Fully supported by Arkon.

### ASE (Ark: Survival Evolved)
The original 2017 Ark game. Supported by Arkon except for Nitrado-hosted servers.

---

## C

### Cluster
In Arkon, a **cluster** is a group of related game servers you manage together. This is different from Ark's transfer cluster - it's simply how Arkon organizes your servers.

> Even if you only have 1 server, you still need to create a cluster first.
{.is-info}

### Cross-Chat / Interchat
A feature that syncs in-game chat to Discord, and optionally between all servers in a cluster.

---

## D

### Discord Leveling
A system that tracks user activity (messages and voice time) and awards experience points. Users level up as they participate, unlocking roles and perks. See `+levelset` for configuration.

---

## E

### Extended Economy
Advanced economy features including command costs, transfer taxes, auto-paydays, and bank event logging. Builds on Red-DiscordBot's built-in economy.

---

## G

### Gamertag (Host GT)
The Xbox/Microsoft account that hosts a crossplay server. Players add this as a friend to easily join the server.

---

## I

### Implant / Specimen Number
Your character's unique ID in Ark, found on your implant (the diamond in your inventory). Used to link your in-game character to Discord for features like the shop.

---

## K

### Kill Feed
A feature that announces player kills in map chat with a fun format. Also "shames" players who kill low-level characters (bobs). Toggle with `+arkset killfeed`.

---

## L

### Lookback
An investigation tool that shows where a player was online during a specific time window. Useful for investigating incidents. See `+lookback`.

### Lootbox
A randomized reward system where players can open crates for a chance at various items. Admins configure item pools and drop rates.

---

## M

### Mod Role
A Discord role configured with `+set roles addmodrole @role`. Users with this role have limited staff permissions - they can use moderation commands but not full admin features. This is a [Red-DiscordBot](#red-discordbot) feature.

---

## P

### Payday
A reward system where players can claim currency or items at set intervals by typing `+payday` in-game or Discord.

### Power Rating
🔹 A score calculated from a tribe's defensive structures (turrets, generators, tek). Used for the `+power` leaderboard. Higher power = more competitive tribe.

### Prefix
The character(s) typed before a command to trigger the bot. Arkon's default prefix is `+`. Change it with `+set serverprefix <newprefix>`.

### Premium
Arkon's paid tier ($10/month) that unlocks up to 100 servers, longer data retention, and exclusive features. See [Premium Features](/guides/premium).

### Prestige (Discord)
In the Discord leveling system, players who reach the max level can "prestige" to reset their level while earning a special prestige rank and perks.

### Profile Card
A customizable image showing a user's Discord stats (level, XP, messages, voice time, stars). Viewable with `+profile`.

---

## R

### RCON (Remote Console)
A protocol that lets Arkon send commands to your game server. Requires port forwarding and proper configuration.

### Red-DiscordBot
The open-source Discord bot framework that Arkon is built on. Red provides the core command system, permissions, and role management. [Learn more](https://github.com/Cog-Creators/Red-DiscordBot)

### RShop (RCON Shop)
The item shop system that uses RCON to deliver purchased items directly to players' inventories.

---

## S

### Scheduled RCON
Automate RCON commands to run at specific times. Useful for automatic restarts, broadcasts, or maintenance tasks.

### Specimen Number
See [Implant](#implant--specimen-number).

### Stars
A recognition system where community members can give "stars" to thank helpful users. View with `+stars` and see leaderboard with `+startop`.

### Suggestion System
A feature for collecting community ideas. Players submit suggestions with `+idea`, others vote with reactions, and admins can approve/reject them.

### Sus Rating
🔸 A score indicating how likely an Xbox account is to be an alternate account (alt). Based on account age, gamerscore, and other factors.

---

## T

### Timeline
An investigation feature showing a player's join and leave events over a time period. See `+timeline`.

---

## U

### Uncryo Limit
🔹 A configurable limit on how many uncryoed (active) tames a tribe can have at once. Helps prevent server lag from too many active dinos.

---

## V

### Valid Servers
🔹 A whitelist of server names that tames are allowed to transfer from. Used with `+scanforeigntames` to detect cheated-in tames from unauthorized sources.

---

## W

### Watchlist
A list of suspicious players that admins want to monitor. When a watched player joins or leaves, admins receive an alert.

### Weekly Leaderboard
A Discord leveling feature that tracks and announces top contributors each week. Configure with `+weeklyset`.

---

## X

### XSAPI (Xbox Services API)
Xbox integration features for crossplay servers, including automatic friend management, Xbox DMs, and alt detection.

### XUID
A player's unique Xbox identifier. Used internally by Arkon for tracking crossplay players.

---

## Symbols in Documentation

| Symbol | Meaning |
|--------|---------|
| ⚡ | Premium feature - requires [Arkon Premium](/guides/premium) |
| 🔸 | Xbox/Crossplay feature - requires Microsoft Store version |
| 🔹 | Self-hosting feature - requires [ArkViewer](https://github.com/vertyco/arkview) plugin |