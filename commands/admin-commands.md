---
title: Admin Commands - Arkon Server Owner and Admin Reference
description: "Every Arkon admin command for Ark server management: server setup, settings, the RCON shop, tribe logs, security and Xbox tools, with links to step-by-step guides."
published: true
date: 2026-10-12T00:00:00.000Z
tags: commands, admin, reference
editor: markdown
dateCreated: 2023-12-25T19:33:59.122Z
---

# Ark Admin Commands (Arkon)

Arkon is an Ark admin manager that runs from Discord. These are the commands for people with your Admin role (and a few that only the Discord server owner can run): connecting servers, changing settings, setting up the RCON shop and tribe logs, security tools and more. Run `+viewservers` to open the admin menu. Looking for raw game console commands instead? See the [Ark RCON Commands](/guides/ark-rcon-commands) reference.

**How to read this page**

- Type commands in any Discord channel Arkon can see. The default prefix is `+`.
- `<value>` means you must fill it in. `[value]` means it is optional.
- **Who can use it:** *Admin* and *Mod* are the roles you set when you [set up Arkon](/guides/getting-started). *Everyone* means any member. *Server owner* means the owner of the Discord server.
- 🔹 needs [ArkView](/guides/arkview). 🔸 is for Xbox / Microsoft Store ASE servers only.
- Each section links to the guide that explains the commands step by step.

Full details for every command are on the [All Commands](/commands/all-commands) page.

## Getting Started

Guide: [Getting Started: Connect Your First Ark Server](/guides/getting-started)

| Command | What it does | Who |
|---|---|---|
| `/setup` | Start the guided setup wizard. | Members with the Manage Server permission |
| `+addcluster <name>` | Create a cluster to group your servers. | Admin |
| `+addserver <cluster_name>` | Add a server to one of your clusters. | Admin |
| `+delcluster <cluster_name>` | Delete a cluster | Admin |
| `+delserver <cluster_name> <server_name>` | Delete a server | Admin |
| `+checklist` | View a configuration checklist for all ArkTools features | Admin |

## Server Settings

Guide: [Server Settings: Clusters, Servers and Bot Settings](/guides/server-settings)

| Command | What it does | Who |
|---|---|---|
| `+viewservers` | Open the main menu for server management | Admin |
| `+arkset <subcommand>` | ArkTools configuration | Admin |
| `+arkset timezone <timezone>` | Set your server's timezone | Admin |
| `+arkset clustertype <cluster_type>` | Set the type of ark servers you host | Admin |
| `+arkset alertchannel <channel>` | Set a channel to receive alerts | Admin |
| `+arkset eventlog <channel>` | Set the event log | Admin |
| `+arkset retention <days>` | Set the days worth of playercount data to keep | Admin |
| `+arkset usedisplaynames` | Toggle whether discord->ark messages use display names | Admin |
| `+arkset regenkey` | Generate a fresh ArkView API key. | Server owner |
| `+arkset tempbandefault <duration>` | Set the default tempban duration | Server owner |
| `+arkset uncryolimit <limit> <cluster_name>` | Set how many uncryoed tames a tribe can have. | Admin |
| `+arkset exportregisteredplayers <specimen_set>` | Export all registered players to a CSV file | Admin |
| `+arkset recentlycreated <created_after>` | List players created after a specific date. | Admin |
| `+arkset wipeclusterimplants <cluster_name>` | Reset all player's set specimen numbers for a cluster | Admin |
| `+arkset wipeclusterstats <cluster_name>` | Reset all player stats like kills/tames/deaths for a cluster | Admin |
| `+arkset wipeclustertribes <cluster_name>` | Reset all player tribes for a cluster | Admin |

## Playtime Tracking, Playtime Roles and Welcome Messages

Guide: [Playtime Tracking, Playtime Roles and Welcome Messages](/guides/playtime-and-roles)

| Command | What it does | Who |
|---|---|---|
| `+arkset linkrole <hours> <role>` | Add a playtime role | Admin |
| `+arkset unlinkrole <hours>` | Remove a playtime role | Admin |
| `+arkset autoremoverole` | Toggle auto-removal of previous playtime role | Admin |
| `+arkset viewranks` | View playtime roles | Admin |
| `+arkset initroles` | Initialize playtime roles | Admin |
| `+arkset registerrole [role]` | Set the role required to register | Admin |
| `+arkset autowelcome` | Toggle auto welcoming of new players discovered in-game | Admin |
| `+arkset autowelcomemessage [message]` | Set the welcome message sent when a new player is found | Admin |
| `+arkset autoinvite <enabled>` | Toggle posting a Discord invite in-game when a player mentions 'discord' in chat | Admin |
| `+arkset invitelink [address]` | Set the Discord address given to players in-game when they mention 'discord' in chat | Admin |
| `+arkset resetplaytime <subcommand>` | Reset player playtime (useful for monthly playtime contests) | Admin |
| `+arkset resetplaytime all` | Reset ALL playtime for every player on every server | Admin |
| `+arkset resetplaytime cluster <cluster>` | Reset playtime for all players on every server in a cluster | Admin |
| `+arkset resetplaytime server <cluster> [server]` | Reset playtime for all players on a server | Admin |
| `+arkset resetplaytime player <player> [cluster] [server]` | Reset a single player's playtime | Admin |
| `+setplayertime <time> <player_query>` | Set the tracked playtime for a player. | Admin |

## Live Server Status Channel and Player Count Graphs

Guide: [Live Server Status Channel and Player Count Graphs](/guides/status-channel)

| Command | What it does | Who |
|---|---|---|
| `+serverstatus <subcommand>` | Server status channel settings | Admin |
| `+serverstatus channel <channel>` | Set the status channel for your Ark servers | Admin |
| `+serverstatus init` | Initialize the status message | Admin |
| `+serverstatus time <seconds>` | Set the status graph timedelta | Admin |
| `+serverstatus view` | View the status channel for your Ark servers | Admin |

## Player Registration

Guide: [Player Registration: Link Discord Accounts to Ark Players](/guides/player-registration)

| Command | What it does | Who |
|---|---|---|
| `+registerplayer <member> <gameid> [overwrite]` | Register another user to the database. | Admin |
| `+setplayerimplant <gameid> <implant>` | Set the implant number for a player. | Admin |

## In-Game Chat Commands

Guide: [In-Game Chat Commands: Kits, Payday and Unstuck](/guides/in-game-commands)

| Command | What it does | Who |
|---|---|---|
| `+arkset ingame <subcommand>` | Configure in-game settings | Admin |
| `+arkset ingame kit <cluster_name>` | Toggle new player kit claiming for a cluster | Admin |
| `+arkset ingame getkitpaths <cluster_name>` | Get the current kit paths for a cluster | Admin |
| `+arkset ingame setkitpaths <cluster_name>` | Upload kit blueprint paths for a cluster. | Admin |
| `+arkset ingame autokit <cluster_name>` | Toggle automatic starter kit delivery on a player's first-ever join to a cluster | Admin |
| `+arkset ingame autokitplaytime <hours> <cluster_name>` | Set the lifetime playtime cap for auto-kit eligibility | Admin |
| `+arkset ingame autokitwindow <days> <cluster_name>` | Set the seeding recency window for auto-kit | Admin |
| `+arkset ingame autokitwelcome <cluster_name> [template]` | Set the in-game welcome message sent after an auto-kit delivery | Admin |
| `+arkset ingame payday <cluster_name>` | Toggle payday rewards for a cluster | Admin |
| `+arkset ingame paydaycooldown <seconds> <cluster_name>` | Set cooldown seconds for paydays | Admin |
| `+arkset ingame paydayrandom <cluster_name>` | Toggle randomization of payday rewards | Admin |
| `+arkset ingame getpaydaypaths <cluster_name>` | Get the current payday paths for a cluster | Admin |
| `+arkset ingame setpaydaypaths <cluster_name>` | Upload the blueprint paths used for payday rewards. | Admin |
| `+arkset ingame imstuck <cluster_name>` | Enable or disable the /imstuck rescue command for a cluster. | Admin |
| `+arkset ingame imstuckcooldown <seconds> <cluster_name>` | Change the cooldown for the /imstuck rescue command. | Admin |
| `+arkset ingame getimstuckpaths <cluster_name>` | Get the current imstuck paths for a cluster | Admin |
| `+arkset ingame setimstuckpaths <cluster_name>` | Upload the teleport paths used for /imstuck. | Admin |
| `+resetkit <gameid>` | Reset a players claimed kit | Admin |
| `+resetclusterkits <cluster_name>` | Reset all player kits for a cluster | Admin |

## The RCON Shop (Rshop)

Guide: [The RCON Shop (Rshop): Sell In-Game Items](/guides/rshop)

| Command | What it does | Who |
|---|---|---|
| `+rshopset <subcommand>` | Admin setup commands for the RCON shop. | Admin |
| `+rshopset autorefund` | Toggle automatic refunds when purchases fail. | Admin |
| `+rshopset bpmultiplier <blueprint_multiplier> [cluster]` | Adjust the blueprint pricing multiplier. | Admin |
| `+rshopset delimiter <delimiter>` | Set the delimiter used inside pack rows. | Admin |
| `+rshopset discount <discount> [cluster]` | Set a flat discount for the shop. | Admin |
| `+rshopset discountdays <day> <discount>` | Set a specific day's discount rotation. | Admin |
| `+rshopset discountrole <role> <discount>` | Give a role a permanent shop discount. | Admin |
| `+rshopset download` | Export the current shop to Excel. | Admin |
| `+rshopset maxbpquality <max_bp_quality> [cluster]` | Limit the highest blueprint quality a user can request. | Admin |
| `+rshopset maxquality <max_quality> [cluster]` | Limit the highest item quality a user can request. | Admin |
| `+rshopset qualityexp <exponent> [cluster]` | Tweak the quality exponent multiplier. | Admin |
| `+rshopset readstacks` | Read stack sizes from a Game.ini file. | Admin |
| `+rshopset template` | Download the Excel template for building your shop. | Admin |
| `+rshopset upload` | Upload an Excel sheet to refresh the shop. | Admin |
| `+rshopset view` | Show the current shop configuration for this guild.   Examples: - +rshopset view | Admin |
| `+arkset toggleshop` | Toggle the shop on/off | Admin |
| `+arkset toggleshopcluster <cluster_name>` | Disable the shop for a specific cluster | Admin |
| `+arkset shoplog <channel>` | Set the shop log channel | Admin |
| `+arkset refundclusterdelta <start_time> <end_time> <cluster_name>` | Refund shop purchases for a cluster within a time window. | Admin |
| `+arkset refundserverdelta <start_time> <end_time> <server_name> <cluster_name>` | Refund purchases for a specific server within a time window. | Admin |
| `+arkset refundplaytimedelta <credits_per_hour> <start_date> <end_date> [dry_run]` | Award players credits based on playtime over a time window. | Admin |

## Lootboxes

Guide: [Lootboxes](/guides/lootboxes)

| Command | What it does | Who |
|---|---|---|
| `+lootboxset <subcommand>` | Setup the lootbox system | Admin |
| `+lootboxset add <chance> <quality> <quantity> <blueprint> <stacksize> <path> <name> [cluster_blacklist]` | Quickly add an item to the lootbox system | Admin |
| `+lootboxset cooldown <cooldown>` | Set the lootbox cooldown | Admin |
| `+lootboxset download` | Get the current lootboxes as an Excel file | Admin |
| `+lootboxset logchannel <channel>` | Set the lootbox log channel | Admin |
| `+lootboxset price <price>` | Set the price of a lootbox | Admin |
| `+lootboxset simulate [times]` | Simulate opening a lootbox X times and generate a summary of selections. | Admin |
| `+lootboxset template` | Get an example Excel file for the lootbox system | Admin |
| `+lootboxset toggle <cluster_name>` | Toggle lootboxes for a specific cluster | Admin |
| `+lootboxset upload` | Set the lootbox items | Admin |
| `+lootboxset view` | View general lootbox settings | Admin |

## Tribe Logs in Discord and Private Tribe Threads

Guide: [Tribe Logs in Discord and Private Tribe Threads](/guides/tribe-logs)

| Command | What it does | Who |
|---|---|---|
| `+tribeset <subcommand>` | Configure tribe settings | Admin |
| `+tribeset view` | View tribe settings | Admin |
| `+tribeset logchannel <clustername> <channel>` | Set master tribelogs for a cluster | Admin |
| `+tribeset claimrole <role>` | Add/Remove roles that can claim their tribes | Admin |
| `+tribeset claimchannel <channel>` | Set the channel that private tribelogs threads will be created from | Admin |
| `+tribeset resetclaims <confirm>` | Wipe the threads from the claimlog channel and reset all claimed tribes | Admin |
| `+tribeset unclaim <member>` | Force-unclaim a specific member's tribe thread without deleting it | Admin |
| `+cleantribelogs` | Delete tribelog threads that arent associated with a tribe | Admin |

## Game Chat in Discord, Kill Feed and Join Logs

Guide: [Game Chat in Discord, Kill Feed and Join Logs](/guides/chat-and-logs)

| Command | What it does | Who |
|---|---|---|
| `+arkset killfeed` | Toggle the killfeed | Admin |

## Moderation

Guide: [Moderation: Bans, Temp Bans and Tribe Warnings](/guides/moderation)

| Command | What it does | Who |
|---|---|---|
| `+bantribe <tribe_id> <reason>` | Ban all members of a tribe at once | Admin |
| `+tempbantribe <tribe_id> [duration] [reason]` | Temporarily ban all members of a tribe at once. | Admin |
| `+warntribe <tribe_id> <warning>` | Warn all members of a tribe at once | Admin |
| `+tribenote <tribe_id> <note>` | Add a note to all members of a tribe at once | Admin |
| `+suswatch [gameid]` | Add/Remove players from the watchlist. | Admin |
| `+syncbans <subcommand>` | Sync the banlists for all servers | Admin |
| `+syncbans all [confirm]` | Sync every ban across every server. | Admin |
| `+syncbans betweenservers [confirm]` | Mirror bans between every server. | Admin |
| `+syncbans fromdb [confirm]` | Sync bans using the database as the source of truth. | Admin |
| `+syncbans fromserver [confirm]` | Copy bans from the servers into the database. | Admin |

## Server Control

Guide: [Server Control: RCON Commands, Schedules and Restarts](/guides/server-control)

| Command | What it does | Who |
|---|---|---|
| `+scheduledrcon [query]` | Schedule an RCON command to run at a later time. | Admin |
| `+arkset countdown <seconds>` | Set the `doexit` and `dorestartlevel` countdowns | Admin |
| `+arkset modcommands <command>` | Mod command allow list | Admin |
| `+arkset commandblacklist <command>` | Set forbidden commands | Admin |
| `+arkset ansicolors` | Toggle ANSI color codes in RCON output. | Admin |
| `+bulksend <cluster> <server> <implant> <count> <blueprint_string>` | Run GiveItem commands multiple times in a row. | Admin |
| `+excelsend` | Send yourself in-game commands from an Excel sheet. | Admin |
| `+dummywall <width> <height>` | Build a list of spawn commands for a loadout dummy wall. | Admin |
| `+dummyfloor <width> <depth>` | Build a list of spawn commands for a loadout dummy floor. | Admin |
| `+remreacts <message> [min_playtime] [min_joined] [min_age]` | Remove reactions from a message based on the following. - `min_playtime`: Minimum playtime required in hours - `min_joined`: Minimum time in discord in hours - `min_age`: Minimum age of discord account in hours | Admin |

## Security

Guide: [Security: RDP Dupes, Imposters and Name Blacklist](/guides/security)

| Command | What it does | Who |
|---|---|---|
| `+getips` 🔹 | Get a list of player IPs from the database | Admin |
| `+arkset banimposters` | Protect your server if anyone discovers your admin password | Admin |
| `+arkset imposterwhitelist <player_id>` | Whitelist certain game IDs from triggering imposter bans | Admin |
| `+arkset characternameblacklist <name>` | Character name blacklist | Admin |

## Map Tools

Guide: [Map Tools: Hunt Dinos, Find Tames and Map Structures](/guides/map-tools)

| Command | What it does | Who |
|---|---|---|
| `+findstructure <structure_class> [search_query]` 🔹 | Get a marker map of specific structures for a tribe or the whole map | Admin |
| `+territory [include_other] [top]` 🔹 | Visualize controlled areas of a server by tribe. | Admin |
| `+structuregraph` 🔹 | Visualize controlled areas of a server by tribe. | Admin |
| `+tribesize <search_query>` 🔹 | Visualize a tribe's controlled territory along with their types of structures and area they take up. | Admin |
| `+sortdinos <level> [dino_name]` 🔹 | Find all dinos above or equal to the specified level | Admin |
| `+setcustomdinos [custom_dinos]` 🔹 | Register custom dinos for features like hunt and findtame. | Admin |
| `+showcustomdinos` 🔹 | Show the list of custom dinos for this guild | Admin |
| `+clearcustomdinos` 🔹 | Clear all custom dinos for this guild | Admin |
| `+servermetrics <metric>` 🔹 | View current server memory usage | Admin |
| `+viewsysinfo` 🔹 | View data about the system running your servers | Admin |
| `+avsync` 🔹 | Sync tribes, players and characters with with the database | Admin |

## Anti-Cheat

Guide: [Anti-Cheat: Dupes, Mass Breeding and Foreign Tames](/guides/anti-cheat)

| Command | What it does | Who |
|---|---|---|
| `+tamedupes <cluster_name> <server_name> <threshold>` 🔹 | Find duplicated tames if a tribe has more than X of the same dino ID | Admin |
| `+checkmassbreed [threshold] [min_dinos]` 🔹 | Find clusters of dinos left breeding. | Admin |
| `+scanforeigntames` 🔹 | Scan all servers for tames that are from a server not in the valid server list | Admin |
| `+setvalidservers <valid_names>` 🔹 | Comma separated list of valid server names for this guild, any servers not in this list will be flagged when a tame is transferred to them | Admin |
| `+showvalidservers` 🔹 | Show the list of valid server names for this guild | Admin |
| `+tamestatcheck <stat> <points> [stat_type]` 🔹 | Find tames that hit a stat goal. | Admin |
| `+uncryocheck <amount>` 🔹 | Get a list of tribes who's uncryo'd tame count is above the specified amount | Admin |
| `+finddbtribe <search_query>` 🔹 | Find details of a tribe from the database | Admin |
| `+wipetribes <days>` 🔹 | Wipe all tribes that haven't been active for X days or more | Admin |

## Xbox and Microsoft Store Features

Guide: [Xbox and Microsoft Store Features](/guides/xsapi)

| Command | What it does | Who |
|---|---|---|
| `+xsapi <subcommand>` 🔸 | Xbox crossplay tools/settings | Admin |
| `+xsapi altdetection <subcommand>` 🔸 | Alt detection for newly discovered players in-game | Admin |
| `+xsapi altdetection autoban` 🔸 | Toggle alt detection autoban on/off | Admin |
| `+xsapi altdetection channel <channel>` 🔸 | Set the channel for alt detection alerts | Admin |
| `+xsapi altdetection threshold <threshold>` 🔸 | Set the threshold for alt detection | Admin |
| `+xsapi altdetection toggle` 🔸 | Toggle alt detection system on/off | Admin |
| `+xsapi altdetection whitelist <cluster_name>` 🔸 | Whitelist a cluster for auto-ban | Admin |
| `+xsapi authenticate` 🔸 | Authenticate a host gamertag (MS Crossplay Only) | Admin |
| `+xsapi autofriend <subcommand>` 🔸 | Auto host gamertag friend/unfriend system | Admin |
| `+xsapi autofriend toggle` 🔸 | Toggle the auto-friend system | Admin |
| `+xsapi autofriend unfriendtime <days>` 🔸 | Set days of inactivity to auto-unfriend | Admin |
| `+xsapi cleanfriends <cluster> <server> [days]` 🔸 | Trim old friends from a host gamertag. | Admin |
| `+xsapi dumpfriends <xuid>` 🔸 | Dump a player's friends list and check which ones are in the database. | Admin |
| `+xsapi friendinvites <cluster> <server>` 🔸 | Get a list of pending friend invites for the host gamertag | Admin |
| `+xsapi friendrequests <cluster> <server>` 🔸 | Get a list of friend requests for the host gamertag | Admin |
| `+xsapi gettokens <cluster> <server>` 🔸 | Get a payload dump of your server tokens (Careful not to do in public channel) | Admin |
| `+xsapi inviteauth` 🔸 | Authorize a host gamertag to send game invites (needed for `inviteme`) | Admin |
| `+xsapi view` 🔸 | View settings related to the xbox api | Admin |
| `+xsapi viewhosts` 🔸 | View XSAPI info of your servers | Admin |
| `+xdm <player> <message>` 🔸 | DM a player on Xbox | Admin |
| `+addplayer <player>` 🔸 | (Xbox/Win10 CROSSPLAY ONLY) Add a player to a host Gamertag's friends list | Admin |
| `+removeplayer <xuid>` 🔸 | Unfriend a player from the host Gamertag | Admin |
