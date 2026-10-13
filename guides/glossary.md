---
title: Glossary - Arkon Ark Discord Bot
description: Plain-words meanings of Ark and Arkon terms like RCON, cluster, ArkView, specimen number, host Gamertag and tribe log thread, with links to the guides.
published: true
date: 2026-10-12T00:00:00.000Z
tags: glossary, definitions, terminology, rcon, cluster, arkview
editor: markdown
dateCreated: 2026-01-17T00:00:00.000Z
---

# Glossary

Not sure what a word means? Look it up here. Each entry says what the thing is in one plain sentence, then links to the guide where it matters.

Markers used across this wiki: 🔹 = needs [ArkView](/guides/arkview). 🔸 = Xbox / Microsoft Store ASE only.

**Jump to:** [A](#a) | [B](#b) | [C](#c) | [E](#e) | [F](#f) | [G](#g) | [H](#h) | [I](#i) | [K](#k) | [L](#l) | [M](#m) | [N](#n) | [P](#p) | [R](#r) | [S](#s) | [T](#t) | [U](#u) | [V](#v) | [W](#w) | [X](#x)

---

## A

### Admin
One of Arkon's two staff levels: people you trust with all settings, such as the server owner, anyone with the Arkon Admin role, or anyone with the Discord Manage Server permission. See [Getting Started](/guides/getting-started).

### Alert channel
The Discord channel where Arkon posts warnings, such as a schedule or reward that stopped working. Set it with `+arkset alertchannel`. If you set none, Arkon uses the event log instead. See [Server settings](/guides/server-settings) and [Server control](/guides/server-control).

### Alt detection 🔸
A Premium check that gives each brand new Xbox player a score from 0 to 100 for how likely they are to be a fake extra account. See [Xbox features](/guides/xsapi).

### Anti-cheat
The set of ArkView checks that find duped tames, mass breeding pens, foreign tames, too many uncryo'd tames and inactive tribes. See [Anti-cheat](/guides/anti-cheat).

### ArkView (also ArkViewer) 🔹
A free program that reads your Ark save file and hands the results to Arkon, which unlocks the map commands and anti-cheat checks. See [ArkView setup](/guides/arkview), or [ArkView for Nitrado](/guides/arkview-nitrado) if your ASA server is on Nitrado.

### ASA (Ark: Survival Ascended)
The newer version of Ark. Arkon works with it, including Nitrado-hosted ASA servers. See [Getting Started](/guides/getting-started).

### ASE (Ark: Survival Evolved)
The original version of Ark. Arkon works with it, except on Nitrado, which does not allow RCON for ASE. See [Getting Started](/guides/getting-started).

### Auto-friend 🔸
A Premium feature where the host Gamertag adds new players as Xbox friends for you. See [Xbox features](/guides/xsapi).

---

## B

### Ban sync
The `+syncbans` commands, which compare each server's ban list with Arkon's own ban list and fix the differences. They only show what would change (a dry run) unless you add `true`. See [Moderation](/guides/moderation).

### Bulk send
The `+bulksend` command, which sends the same item to a player several times, handy for events. See [Server control](/guides/server-control).

---

## C

### Cluster
A named group of servers that you manage together in Arkon, like a folder that holds your maps. You must make one before you can add a server, even if you have only one. See [Server settings](/guides/server-settings).

### Command blacklist
A list of admin commands that nobody may run in game, even a player who is allowed to use admin commands. Set it with `+arkset commandblacklist`. See [Security](/guides/security).

### Crosschat
The switch that sends game chat lines and in-game command replies to your map chat channel in Discord. Turning it off stops only that direction. See [Chat and logs](/guides/chat-and-logs).

### Cryopod
An in-game item that stores a tame so it is not out in the world. Arkon's uncryo limit counts the tames a tribe has taken out. See [Anti-cheat](/guides/anti-cheat).

---

## E

### EOS ID
The long mix of letters and numbers that identifies a player on ASA. Arkon uses it to ban and register players. See [Player registration](/guides/player-registration).

### Event log
A Discord channel where Arkon posts notices about what it did, such as a New Player Detected card or a Tame Limit Warning. It is also where alerts go when no alert channel is set. See [Server settings](/guides/server-settings).

---

## F

### Foreign tame 🔹
A tame that was brought in from a server that is not one of yours, often a sign of cheating. Arkon finds them with `+scanforeigntames`. See [Anti-cheat](/guides/anti-cheat).

---

## G

### Game ID
The number that identifies a player in the game: a Steam ID, an Xbox XUID or an Epic EOS ID. You give it to Arkon to ban someone. See [Moderation](/guides/moderation).

### Gamertag
Your Xbox name. See [Player registration](/guides/player-registration).

---

## H

### Hosting company
The company that runs your game server, such as Nitrado, G-Portal, Shockbyte, Host Havoc, or Self-Hosted. The setup wizard and `+rconhelp` ask for it so they can show the right steps. See [Getting Started](/guides/getting-started) and [RCON setup](/guides/rcon-setup).

### Host Gamertag 🔸
The Xbox account that hosts your ASE server on the Microsoft Store version. Players add it as a friend to join, and Arkon can sign in as it to add friends and send messages. See [Xbox features](/guides/xsapi).

---

## I

### Imposter protection
A security feature that bans players who run admin commands without being allowed to. It is off until you turn it on. See [Security](/guides/security).

### Imstuck
An in-game chat command that gives a player a care package of basic items. See [In-game commands](/guides/in-game-commands).

### Implant ID
Another name for the [specimen number](#specimen-number-implant-id).

### Interchat
Chat that is passed between the maps of a cluster. In game it shows as `ServerChat <Map> -> <line>`. See [Chat and logs](/guides/chat-and-logs).

### In-game commands
Short commands players type in Ark chat, such as `kit`, `payday` and `imstuck`, which Arkon answers by handing out items. See [In-game commands](/guides/in-game-commands).

---

## K

### Kill feed
A line posted in your map chat channel whenever a player kills another player. It reads kills from tribe logs. Turn it on with `+arkset killfeed`. See [Chat and logs](/guides/chat-and-logs).

### Kit
A starter pack of items that a player claims by typing `kit` in game. See [In-game commands](/guides/in-game-commands).

---

## L

### Leaderboard
A ranked list of top players or tribes, shown in Discord. See [Stats and leaderboards](/guides/stats-and-leaderboards).

### Lookback
The `+lookback` command, which draws a chart of where one player was online during a time window. See [Chat and logs](/guides/chat-and-logs).

### Lootbox
A paid mystery prize: a player pays a price and Arkon sends one random item into their game. See [Lootboxes](/guides/lootboxes).

---

## M

### Master tribe log channel
The Discord channel that shows every tribe's events on a cluster, for staff to read. See [Tribe logs](/guides/tribe-logs).

### Mod
Arkon's second staff level: helpers with day-to-day tools such as banning. See [Getting Started](/guides/getting-started).

---

## N

### Name blacklist
A list of banned character names. Arkon renames players who use one. See [Security](/guides/security).

---

## P

### Payday
An in-game reward that a player can claim again after a wait. See [In-game commands](/guides/in-game-commands).

### Player registration
Linking one Discord account to one in-game character with `+register`, so Arkon knows who is who. See [Player registration](/guides/player-registration).

### Prefix
The character you type before a command. Arkon's default is `+`. See [Getting Started](/guides/getting-started).

### Playtime role
A Discord role Arkon gives a player after they reach a set amount of play time. See [Playtime and roles](/guides/playtime-and-roles).

### Premium
Arkon's paid plan that raises limits and unlocks extra tools. It is tied to the owner of your Discord server. See [Premium](/guides/premium).

---

## R

### RCON
The remote-control connection Arkon uses to send commands to your game server and read who is online. It needs an IP, a port and a password. See [RCON setup](/guides/rcon-setup), and [Ark RCON commands](/guides/ark-rcon-commands) for the commands themselves.

### Rename (in game)
An in-game chat command (`!rename` or `!rn`) that lets a player change their character name. It is off until an admin turns it on. See [In-game commands](/guides/in-game-commands).

### RDP dupe
A trick where one player is logged in on two maps of the same cluster at once to copy items. Arkon can kick or ban for it. See [Security](/guides/security).

### Rshop
The RCON shop, where players spend currency in Discord and get real items in their Ark inventory. See [RCON shop](/guides/rshop).

---

## S

### Scheduled command
An RCON command that Arkon runs on a timer, such as a broadcast or a restart. See [Server control](/guides/server-control).

### Server
One Ark map, like "The Island". See [Server settings](/guides/server-settings).

### Slash command
A command you start by typing `/` in Discord and picking it from the list. Some Arkon commands work both ways, for example `+findtame` and `/findtame`, while `/setup` works only as a slash command. See [Getting Started](/guides/getting-started).

### Specimen number (Implant ID)
The number in the top left of your in-game inventory. Arkon uses it to send items to your character. See [Player registration](/guides/player-registration).

### Status channel
A Discord channel with one message that Arkon keeps updated with how many players are on each server, plus player count graphs. See [Status channel](/guides/status-channel).

### Steam ID
A 17 to 19 digit number that identifies a Steam player. See [Player registration](/guides/player-registration).

### Sus score 🔸
The 0 to 100 number from alt detection. Higher means more suspicious. See [Xbox features](/guides/xsapi).

---

## T

### Tame
A creature a player has tamed in game. Map commands such as `+findtame` look tames up. See [Map tools](/guides/map-tools).

### Tame limit warning
A warning sent to a tribe when it nears the tame cap, by Discord DM and in game chat, and logged in the event log. See [Anti-cheat](/guides/anti-cheat).

### Temp ban
A ban that ends by itself after a set time, made with `+tempbanplayer`. See [Moderation](/guides/moderation).

### Timeline
The `+timeline` command, which shows one player's joins and leaves across all maps. See [Chat and logs](/guides/chat-and-logs).

### Tribe
A group of players in Ark who share bases and tames. Arkon shows each tribe's events in Discord. See [Tribe logs](/guides/tribe-logs).

### Tribe log
The record of what happens to a tribe in game: kills, deaths, tames, destroyed structures and more. Arkon copies these into Discord. See [Tribe logs](/guides/tribe-logs).

### Tribe log thread
A private Discord thread that only one tribe can see, with pings for the events they choose. Players get it by pressing Claim in the `+tribe` menu. See [Tribe logs](/guides/tribe-logs).

### Tribe warning
A message sent to every member of a tribe with `+warntribe`. See [Moderation](/guides/moderation).

---

## U

### Uncryo limit 🔹
A cap on how many tames a tribe can have out in the world instead of stored in cryopods. See [Anti-cheat](/guides/anti-cheat).

---

## V

### Valid server names 🔹
The list of server names that tames are allowed to come from. Anything else counts as a foreign tame. See [Anti-cheat](/guides/anti-cheat).

### Vote (in game)
A chat vote players start to change the day or night, wipe wild dinos or clean up. See [In-game commands](/guides/in-game-commands).

---

## W

### Watchlist
A list of suspicious players, managed with `+suswatch`. See [Moderation](/guides/moderation).

### Welcome message
A message Arkon posts the first time it sees a new player. The free plan adds a Powered by Arkon footer. See [Playtime and roles](/guides/playtime-and-roles) and [Premium](/guides/premium).

---

## X

### XUID
The long 16-digit number behind an Xbox Gamertag. See [Player registration](/guides/player-registration).

### Xbox features 🔸
Tools for Microsoft Store ASE servers: host Gamertag friends, auto-friend, alt detection and Xbox messages. See [Xbox features](/guides/xsapi).

---

## Related pages

- [Getting Started](/guides/getting-started)
- [FAQ](/guides/faq)
- [Quick reference](/guides/quick-reference)
- [All commands](/commands/all-commands)
