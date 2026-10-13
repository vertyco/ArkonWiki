---
title: All Commands - Complete Arkon Bot Command Reference
description: "Every Arkon bot command for Ark: Survival Evolved and Ascended servers, with syntax, who can use it, and a link to the step-by-step guide."
published: true
date: 2026-10-12T00:00:00.000Z
tags: commands, reference, complete-list
editor: markdown
dateCreated: 2023-12-12T01:56:40.592Z
---

# All Arkon Commands

Every command the public Arkon bot offers (244 in total), grouped by topic. New to Arkon? Start with the [Getting Started guide](/guides/getting-started) instead, or use the [Quick Reference](/guides/quick-reference) for a one-page cheat sheet.

**How to read this page**

- Type commands in any Discord channel Arkon can see. The default prefix is `+`.
- `<value>` means you must fill it in. `[value]` means it is optional.
- **Who can use it:** *Admin* and *Mod* are the roles you set when you [set up Arkon](/guides/getting-started). *Everyone* means any member. *Server owner* means the owner of the Discord server.
- 🔹 needs [ArkView](/guides/arkview). 🔸 is for Xbox / Microsoft Store ASE servers only.
- Each section links to the guide that explains the commands step by step.

**Topics:** [Getting Started](/guides/getting-started) · [Turn On RCON and Find Your RCON Details](/guides/rcon-setup) · [Server Settings](/guides/server-settings) · [Playtime Tracking, Playtime Roles and Welcome Messages](/guides/playtime-and-roles) · [Live Server Status Channel and Player Count Graphs](/guides/status-channel) · [Player Registration](/guides/player-registration) · [In-Game Chat Commands](/guides/in-game-commands) · [The RCON Shop (Rshop)](/guides/rshop) · [Lootboxes](/guides/lootboxes) · [Tribe Logs in Discord and Private Tribe Threads](/guides/tribe-logs) · [Game Chat in Discord, Kill Feed and Join Logs](/guides/chat-and-logs) · [Moderation](/guides/moderation) · [Server Control](/guides/server-control) · [Security](/guides/security) · [Map Tools](/guides/map-tools) · [Anti-Cheat](/guides/anti-cheat) · [Player Stats and Leaderboards](/guides/stats-and-leaderboards) · [Xbox and Microsoft Store Features](/guides/xsapi)

## Getting Started

Step-by-step guide: [Getting Started: Connect Your First Ark Server](/guides/getting-started)

### /setup

Start the guided setup wizard.

- **Usage:** `/setup`
- **Who can use it:** Members with the Manage Server permission
- **Slash command only**

### +addcluster

Create a cluster to group your servers.

One cluster collects join, leave, and admin logs for a set of maps.  
Configure log channels later from the server management menu.

Arguments:  
`name` - Unique name for the cluster.

Examples:
- +addcluster mycluster

- **Usage:** `+addcluster <name>`
- **Who can use it:** Admin

### +addserver

Add a server to one of your clusters.

We'll guide you through setting IP, RCON, and other details once you start.  
Set the chat relay channel later from the server configuration menu.

Arguments:  
`cluster_name` - Name of the cluster this server belongs to.

Examples:
- +addserver mycluster

- **Usage:** `+addserver <cluster_name>`
- **Who can use it:** Admin

### +delcluster

Delete a cluster

- **Usage:** `+delcluster <cluster_name>`
- **Who can use it:** Admin
- **Also called:** `+remcluster`

### +delserver

Delete a server

- **Usage:** `+delserver <cluster_name> <server_name>`
- **Who can use it:** Admin
- **Also called:** `+remserver`

### +checklist

View a configuration checklist for all ArkTools features

- **Usage:** `+checklist`
- **Who can use it:** Admin

## Turn On RCON and Find Your RCON Details

Step-by-step guide: [Turn On RCON and Find Your RCON Details](/guides/rcon-setup)

### +rconhelp

Get a guide for finding your ARK server's RCON port and admin password

- **Usage:** `+rconhelp`
- **Who can use it:** Everyone

## Server Settings

Step-by-step guide: [Server Settings: Clusters, Servers and Bot Settings](/guides/server-settings)

### +viewservers

Open the main menu for server management

- **Usage:** `+viewservers`
- **Who can use it:** Admin

### +arkset

ArkTools configuration

- **Usage:** `+arkset <subcommand>`
- **Who can use it:** Admin
- **Also called:** `+arktools`

### +arkset view

View ark settings

- **Usage:** `+arkset view`
- **Who can use it:** Mod

### +arkset timezone

Set your server's timezone

- **Usage:** `+arkset timezone <timezone>`
- **Who can use it:** Admin

### +arkset clustertype

Set the type of ark servers you host

Valid arguments are `xbox, steam, both`

- **Usage:** `+arkset clustertype <cluster_type>`
- **Who can use it:** Admin

### +arkset alertchannel

Set a channel to receive alerts

The following alerts are sent here:
- Server goes down
- Unauthorized admin command in-game
- Tribe auto-banned for foreign tames

**These events will fall back to the event log if no alert channel is set**

- **Usage:** `+arkset alertchannel <channel>`
- **Who can use it:** Admin

### +arkset eventlog

Set the event log

The logs include the following events:
- New players that are added to the database
- Welcome messages sent to new players(if enabled)
- Old players that are unfriended for inactivity(if enabled)
- Players that are unfriended for leaving the Discord(if enabled)
- Players that are unfriended due to unfriending a host Gamertag

- **Usage:** `+arkset eventlog <channel>`
- **Who can use it:** Admin

### +arkset retention

Set the days worth of playercount data to keep

- **Usage:** `+arkset retention <days>`
- **Who can use it:** Admin

### +arkset usedisplaynames

Toggle whether discord->ark messages use display names

If Enabled, messages sent to Ark will use the user's nickname or username instead of their username

- **Usage:** `+arkset usedisplaynames`
- **Who can use it:** Admin

### +arkset regenkey

Generate a fresh ArkView API key.

This replaces the existing key immediately, so update any integrations that use it.

Examples:
- +arkset regenkey

- **Usage:** `+arkset regenkey`
- **Who can use it:** Server owner

### +arkset tempbandefault

Set the default tempban duration

Example: 1h30m

- **Usage:** `+arkset tempbandefault <duration>`
- **Who can use it:** Server owner

### +arkset uncryolimit

Set how many uncryoed tames a tribe can have.

Put 0 to disable the limit entirely.

Arguments:  
`limit` - Maximum number of active tames allowed.  
`cluster_name` - Cluster to apply the rule to.

Examples:
- +arkset uncryolimit 200 main
- +arkset uncryolimit 0 pve

- **Usage:** `+arkset uncryolimit <limit> <cluster_name>`
- **Who can use it:** Admin

### +arkset exportregisteredplayers

Export all registered players to a CSV file

**Arguments**  
`specimen_set` - Set to True to only export players that also have a specimen number set

- **Usage:** `+arkset exportregisteredplayers <specimen_set>`
- **Who can use it:** Admin

### +arkset recentlycreated

List players created after a specific date.

Use the ISO format `YYYY-MM-DDTHH:MM:SS` so we know where to start.

Arguments:  
`created_after` - ISO timestamp marking the oldest creation time to include.

Examples:
- +arkset recentlycreated 2024-04-03T20:00:00

- **Usage:** `+arkset recentlycreated <created_after>`
- **Who can use it:** Admin
- **Also called:** `+arkset rc`

### +arkset wipeclusterimplants

Reset all player's set specimen numbers for a cluster

- **Usage:** `+arkset wipeclusterimplants <cluster_name>`
- **Who can use it:** Admin

### +arkset wipeclusterstats

Reset all player stats like kills/tames/deaths for a cluster

- **Usage:** `+arkset wipeclusterstats <cluster_name>`
- **Who can use it:** Admin

### +arkset wipeclustertribes

Reset all player tribes for a cluster

- **Usage:** `+arkset wipeclustertribes <cluster_name>`
- **Who can use it:** Admin

## Playtime Tracking, Playtime Roles and Welcome Messages

Step-by-step guide: [Playtime Tracking, Playtime Roles and Welcome Messages](/guides/playtime-and-roles)

### +arkset linkrole

Add a playtime role

- **Usage:** `+arkset linkrole <hours> <role>`
- **Who can use it:** Admin

### +arkset unlinkrole

Remove a playtime role

- **Usage:** `+arkset unlinkrole <hours>`
- **Who can use it:** Admin

### +arkset autoremoverole

Toggle auto-removal of previous playtime role

- **Usage:** `+arkset autoremoverole`
- **Who can use it:** Admin

### +arkset viewranks

View playtime roles

- **Usage:** `+arkset viewranks`
- **Who can use it:** Admin

### +arkset initroles

Initialize playtime roles

- **Usage:** `+arkset initroles`
- **Who can use it:** Admin

### +arkset registerrole

Set the role required to register

- **Usage:** `+arkset registerrole [role]`
- **Who can use it:** Admin

### +arkset autowelcome

Toggle auto welcoming of new players discovered in-game

This is just a broadcast in the server, not a DM

- **Usage:** `+arkset autowelcome`
- **Who can use it:** Admin

### +arkset autowelcomemessage

Set the welcome message sent when a new player is found

Placeholders
- `{username}` - Player's username
- `{gameid}` - Player's game ID

- **Usage:** `+arkset autowelcomemessage [message]`
- **Who can use it:** Admin
- **Also called:** `+arkset welcomemsg`

### +arkset autoinvite

Toggle posting a Discord invite in-game when a player mentions 'discord' in chat

On by default. Turn it off if the bot runs from a Discord you don't want players joining.

**Example**
- `+arkset autoinvite off`

- **Usage:** `+arkset autoinvite <enabled>`
- **Who can use it:** Admin

### +arkset invitelink

Set the Discord address given to players in-game when they mention 'discord' in chat

Leave it blank to go back to picking an invite automatically.  
Discord invite links are checked before saving.  
Anything else, like a website that redirects to your Discord, is saved as typed.

**Examples**
- `+arkset invitelink discord.gg/yourserver`
- `+arkset invitelink` (back to automatic)

- **Usage:** `+arkset invitelink [address]`
- **Who can use it:** Admin
- **Also called:** `+arkset discordlink`

### +arkset resetplaytime

Reset player playtime (useful for monthly playtime contests)

Lowering playtime can also lower a player's playtime rank roles.

- **Usage:** `+arkset resetplaytime <subcommand>`
- **Who can use it:** Admin

### +arkset resetplaytime all

Reset ALL playtime for every player on every server

- **Usage:** `+arkset resetplaytime all`
- **Who can use it:** Admin

### +arkset resetplaytime cluster

Reset playtime for all players on every server in a cluster

The time played on that cluster is also removed from each player's total playtime.

Examples:
- +arkset resetplaytime cluster pvp

- **Usage:** `+arkset resetplaytime cluster <cluster>`
- **Who can use it:** Admin

### +arkset resetplaytime server

Reset playtime for all players on a server

Leave out the server (or use `all`) to reset every server in the cluster.  
The time played there is also removed from each player's total playtime.

Examples:
- +arkset resetplaytime server pvp island
- +arkset resetplaytime server pvp all

- **Usage:** `+arkset resetplaytime server <cluster> [server]`
- **Who can use it:** Admin

### +arkset resetplaytime player

Reset a single player's playtime

With no cluster, their overall playtime is reset on every server.  
With a cluster (and optionally a server), only the time played there is reset and  
removed from their total playtime.

Arguments:  
`player` - The player's XUID, SteamID, EOSID, Discord ID, Specimen #, ect.  
`cluster` - Optional cluster to limit the reset to.  
`server` - Optional server in that cluster to limit the reset to.

Examples:
- +arkset resetplaytime player 2535412345678901
- +arkset resetplaytime player 2535412345678901 pvp
- +arkset resetplaytime player 2535412345678901 pvp island

- **Usage:** `+arkset resetplaytime player <player> [cluster] [server]`
- **Who can use it:** Admin

### +setplayertime

Set the tracked playtime for a player.

Use common time shorthand like 1d, 6h, or 45m. Combine them for longer spans, such as 3d12h.

Arguments:  
`time` - How much playtime to assign.  
`player_query` - Name, ID, or partial match for the player.

Examples:
- +setplayertime 2d6h SurvivorSam
- +setplayertime 45m "Player Name"

- **Usage:** `+setplayertime <time> <player_query>`
- **Who can use it:** Admin

## Live Server Status Channel and Player Count Graphs

Step-by-step guide: [Live Server Status Channel and Player Count Graphs](/guides/status-channel)

### +serverstatus

Server status channel settings

- **Usage:** `+serverstatus <subcommand>`
- **Who can use it:** Admin

### +serverstatus channel

Set the status channel for your Ark servers

- **Usage:** `+serverstatus channel <channel>`
- **Who can use it:** Admin

### +serverstatus init

Initialize the status message

- **Usage:** `+serverstatus init`
- **Who can use it:** Admin

### +serverstatus time

Set the status graph timedelta

- **Usage:** `+serverstatus time <seconds>`
- **Who can use it:** Admin

### +serverstatus view

View the status channel for your Ark servers

- **Usage:** `+serverstatus view`
- **Who can use it:** Admin

### +servergraph

See how your player count changed over time.

Arguments:  
`timespan` - How far back to check. Use values like 4h, 12d, 3w2d, or all. Defaults to 1 hour.  
`clusters_only` - true to merge maps by cluster instead of showing every map.  
`include_total` - true to add a line that shows the combined player count.  
`search_query` - Filter to specific clusters or maps.  
`start_time` - Override the start time, e.g. April 10 2032 5:00pm.  
`end_time` - Optional end time that pairs with start_time.

Examples:  
+servergraph 4h  
+servergraph 12d  
+servergraph 3w2d  
+servergraph 7w

- **Usage:** `+servergraph [timespan] [clusters_only] [include_total] [search_query] [start_time] [end_time]`
- **Who can use it:** Everyone
- **Slash command:** also works as `/servergraph`
  - `timespan`: How far back you want to view
  - `clusters_only`: (T/F) Group the maps by cluster
  - `include_total`: (T/F) Include a 'total' line in the graph
  - `search_query`: Search for a specific set of clusters or maps
  - `start_time`: Start time for the graph (e.g. April 10, 2032 5:00pm)
  - `end_time`: End time for the graph (e.g. April 11, 2032 5:00pm)

### +playercounts

View player counts either globally or locally

- **Usage:** `+playercounts [local]`
- **Who can use it:** Everyone

## Player Registration

Step-by-step guide: [Player Registration: Link Discord Accounts to Ark Players](/guides/player-registration)

### +register

Register your in-game account with the database.

- **Usage:** `+register [username]`
- **Who can use it:** Everyone
- **Slash command:** also works as `/register`

### +unregister

Unregister yourself

Removes you from any Gamertags you have registered to

- **Usage:** `+unregister`
- **Who can use it:** Everyone
- **Also called:** `+unregisterme`

### +registerplayer

Register another user to the database.

- **Usage:** `+registerplayer <member> <gameid> [overwrite]`
- **Who can use it:** Admin
- **Slash command:** also works as `/registerplayer`

### +unregisterplayer

Unlink the discord account from a player

The optional **player** argument can be one of the following.
- Gamertag or Steam Username
- XUID or Steam ID
- Discord ID or Username
- @mention

- **Usage:** `+unregisterplayer <player>`
- **Who can use it:** Mod

### +specimen

Set your specimen number to use the Rshop

Your specimen number (aka Implant ID) can be found in the top left of your player inventory.

- **Usage:** `+specimen <specimen_number>`
- **Who can use it:** Everyone
- **Also called:** `+implant`, `+speciment`, `+implantid`, `+specimen#`

### +setplayerimplant

Set the implant number for a player.

- **Usage:** `+setplayerimplant <gameid> <implant>`
- **Who can use it:** Admin
- **Slash command:** also works as `/setplayerimplant`

### +findsurvivor

Look up a survivor by character name.

Returns their servers, tribes, and recent activity if we have it logged.

Arguments:  
`survivor_name` - Anything we can use to match the character name.

Examples:
- +findsurvivor SurvivorSam
- +findsurvivor "Super Survivor"

- **Usage:** `+findsurvivor <survivor_name>`
- **Who can use it:** Everyone
- **Also called:** `+findcharname`

### +kickme

Kick your character from the server.

Use this when you're stuck in a loading screen or need a fresh join.

Examples:
- +kickme

- **Usage:** `+kickme`
- **Who can use it:** Everyone

## In-Game Chat Commands

Step-by-step guide: [In-Game Chat Commands: Kits, Payday and Unstuck](/guides/in-game-commands)

### +arkset ingame

Configure in-game settings

- **Usage:** `+arkset ingame <subcommand>`
- **Who can use it:** Admin

### +arkset ingame kit

Toggle new player kit claiming for a cluster

- **Usage:** `+arkset ingame kit <cluster_name>`
- **Who can use it:** Admin

### +arkset ingame getkitpaths

Get the current kit paths for a cluster

- **Usage:** `+arkset ingame getkitpaths <cluster_name>`
- **Who can use it:** Admin

### +arkset ingame setkitpaths

Upload kit blueprint paths for a cluster.

Attach a `.txt` file with one entry per line in the format `path quantity quality blueprint`.

Arguments:  
`cluster_name` - Cluster whose kit paths you're updating.

Examples:
- +arkset ingame setkitpaths main (with kit_paths.txt attached)

- **Usage:** `+arkset ingame setkitpaths <cluster_name>`
- **Who can use it:** Admin

### +arkset ingame autokit

Toggle automatic starter kit delivery on a player's first-ever join to a cluster

Delivers the cluster's kit paths as soon as the new player has a character,  
then sends the auto-kit welcome message in-game. Uses the same claim list as  
the in-game kit command, so players can never receive the kit twice.

- **Usage:** `+arkset ingame autokit <cluster_name>`
- **Who can use it:** Admin

### +arkset ingame autokitplaytime

Set the lifetime playtime cap for auto-kit eligibility

Players whose total guild-wide playtime exceeds this many hours will not  
receive an auto-kit. Lifetime playtime survives season wipes.

Arguments:  
`hours` - Max lifetime playtime in hours (default 10).  
`cluster_name` - Cluster to apply the cap to.

- **Usage:** `+arkset ingame autokitplaytime <hours> <cluster_name>`
- **Who can use it:** Admin

### +arkset ingame autokitwindow

Set the seeding recency window for auto-kit

When auto-kit is enabled on a cluster, only players seen within this many  
days are queued for a backfilled kit. Joins after enabling are unaffected.

Arguments:  
`days` - Seeding window in days (default 30).  
`cluster_name` - Cluster to apply the window to.

- **Usage:** `+arkset ingame autokitwindow <days> <cluster_name>`
- **Who can use it:** Admin

### +arkset ingame autokitwelcome

Set the in-game welcome message sent after an auto-kit delivery

Placeholder: `{username}`.  
Quote the cluster name if it contains spaces. Run with no template to reset to the default.

Examples:
- +arkset ingame autokitwelcome main Welcome {username}! Type register to link your Discord!

- **Usage:** `+arkset ingame autokitwelcome <cluster_name> [template]`
- **Who can use it:** Admin

### +arkset ingame payday

Toggle payday rewards for a cluster

- **Usage:** `+arkset ingame payday <cluster_name>`
- **Who can use it:** Admin

### +arkset ingame paydaycooldown

Set cooldown seconds for paydays

- **Usage:** `+arkset ingame paydaycooldown <seconds> <cluster_name>`
- **Who can use it:** Admin

### +arkset ingame paydayrandom

Toggle randomization of payday rewards

- **Usage:** `+arkset ingame paydayrandom <cluster_name>`
- **Who can use it:** Admin
- **Also called:** `+arkset ingame randompayday`

### +arkset ingame getpaydaypaths

Get the current payday paths for a cluster

- **Usage:** `+arkset ingame getpaydaypaths <cluster_name>`
- **Who can use it:** Admin

### +arkset ingame setpaydaypaths

Upload the blueprint paths used for payday rewards.

Attach a `.txt` file with one line per path using `path quantity quality blueprint` format.

Arguments:  
`cluster_name` - Cluster whose payday rewards you're updating.

Examples:
- +arkset ingame setpaydaypaths main (with payday_paths.txt attached)

- **Usage:** `+arkset ingame setpaydaypaths <cluster_name>`
- **Who can use it:** Admin

### +arkset ingame imstuck

Enable or disable the /imstuck rescue command for a cluster.

Arguments:  
`cluster_name` - Cluster to toggle.

Examples:
- +arkset ingame imstuck main

- **Usage:** `+arkset ingame imstuck <cluster_name>`
- **Who can use it:** Admin

### +arkset ingame imstuckcooldown

Change the cooldown for the /imstuck rescue command.

Arguments:  
`seconds` - How many seconds users must wait between uses.  
`cluster_name` - Cluster to apply the cooldown to.

Examples:
- +arkset ingame imstuckcooldown 900 main

- **Usage:** `+arkset ingame imstuckcooldown <seconds> <cluster_name>`
- **Who can use it:** Admin

### +arkset ingame getimstuckpaths

Get the current imstuck paths for a cluster

- **Usage:** `+arkset ingame getimstuckpaths <cluster_name>`
- **Who can use it:** Admin

### +arkset ingame setimstuckpaths

Upload the teleport paths used for /imstuck.

Attach a `.txt` file with one line per path using `path quantity quality blueprint` format.

Arguments:  
`cluster_name` - Cluster whose teleport paths you're updating.

Examples:
- +arkset ingame setimstuckpaths main (with imstuck_paths.txt attached)

- **Usage:** `+arkset ingame setimstuckpaths <cluster_name>`
- **Who can use it:** Admin

### +resetkit

Reset a players claimed kit

Accepts an XUID, EOS ID, or Steam ID.

If per-server kits are enabled, this will reset the kit for all servers in the cluster.

- **Usage:** `+resetkit <gameid>`
- **Who can use it:** Admin

### +resetclusterkits

Reset all player kits for a cluster

If per-server kits are enabled, this will reset all kits for all servers in the cluster.

- **Usage:** `+resetclusterkits <cluster_name>`
- **Who can use it:** Admin

## The RCON Shop (Rshop)

Step-by-step guide: [The RCON Shop (Rshop): Sell In-Game Items](/guides/rshop)

### +rshop

Open the in-game RCON shop.

Start typing to filter items, or browse the full catalog.

Arguments:  
`item` - Optional search term to jump straight to an item.

Examples:
- +rshop
- +rshop shotgun

- **Usage:** `+rshop [item]`
- **Who can use it:** Everyone
- **Slash command:** also works as `/rshop`
  - `item`: Search for an item (armor/weapons/tools/ect..)

### /quickbuy

Buy something from the shop without opening the menu.

Pick the item and optionally adjust the quantity, quality, or blueprint flag.

Arguments:  
`item` - The item name to purchase.  
`quantity` - How many copies to buy.  
`quality` - Desired quality value.  
`blueprint` - Toggle to request the blueprint version.

Examples:
- /quickbuy item:"Pump-Action Shotgun" quantity:2 quality:120 blueprint:true
- /quickbuy item:"Element" quantity:50

- **Usage:** `/quickbuy <item> [quantity] [quality] [blueprint]`
- **Who can use it:** Everyone
- **Slash command only**
  - `item`: The item you want to buy
  - `quantity`: The quantity of the item you want to buy
  - `quality`: The quality of the item you want to buy
  - `blueprint`: Whether or not the item is a blueprint

### +rshopset

Admin setup commands for the RCON shop.

Run with a subcommand to manage pricing, discounts, and exports.  
Examples:
- +rshopset view
- +rshopset discount 0.15

- **Usage:** `+rshopset <subcommand>`
- **Who can use it:** Admin
- **Also called:** `+rss`

### +rshopset autorefund

Toggle automatic refunds when purchases fail.

When enabled, players get their currency back if a command errors out. One-command purchases always refund.  
Examples:
- +rshopset autorefund

- **Usage:** `+rshopset autorefund`
- **Who can use it:** Admin
- **Also called:** `+rshopset refunds`, `+rshopset refund`

### +rshopset bpmultiplier

Adjust the blueprint pricing multiplier.

Helps offset extra work when players request blueprints instead of items. Use 0 to disable.

Arguments:  
`blueprint_multiplier` - Multiplier value, zero or higher.  
`cluster` - Optional cluster name for a local rule.

Examples:
- +rshopset bpmultiplier 1.5
- +rshopset bpmultiplier 0 fjordur

- **Usage:** `+rshopset bpmultiplier <blueprint_multiplier> [cluster]`
- **Who can use it:** Admin

### +rshopset delimiter

Set the delimiter used inside pack rows.

Choose how multiple blueprint paths or commands are separated in the packs sheet.

Arguments:  
`delimiter` - The separator character or string to use.

Examples:
- +rshopset delimiter |
- +rshopset delimiter ;

- **Usage:** `+rshopset delimiter <delimiter>`
- **Who can use it:** Admin

### +rshopset discount

Set a flat discount for the shop.

Provide 0 to disable. Target a cluster or leave blank for all of them.

Arguments:  
`discount` - Percent as a decimal, between 0 and 0.99.  
`cluster` - Optional cluster name to scope the discount.

Examples:
- +rshopset discount 0.2
- +rshopset discount 0 extinction

- **Usage:** `+rshopset discount <discount> [cluster]`
- **Who can use it:** Admin

### +rshopset discountdays

Set a specific day's discount rotation.

Use numbers 0-6 for Monday through Sunday. Put 0 to clear that day's promo.

Arguments:  
`day` - Day index (0 = Monday ... 6 = Sunday).  
`discount` - Percent as a decimal, between 0 and 0.99.

Examples:
- +rshopset discountdays 5 0.15
- +rshopset discountdays 2 0

- **Usage:** `+rshopset discountdays <day> <discount>`
- **Who can use it:** Admin
- **Also called:** `+rshopset discountday`, `+rshopset dd`

### +rshopset discountrole

Give a role a permanent shop discount.

Set the value to 0 to remove the role from the list.

Arguments:  
`role` - Discord role to adjust.  
`discount` - Percent as a decimal, between 0 and 0.99.

Examples:
- +rshopset discountrole @VIP 0.1
- +rshopset discountrole @Member 0

- **Usage:** `+rshopset discountrole <role> <discount>`
- **Who can use it:** Admin

### +rshopset download

Export the current shop to Excel.

Useful for backups or editing in bulk before re-uploading.

Examples:
- +rshopset download

- **Usage:** `+rshopset download`
- **Who can use it:** Admin

### +rshopset maxbpquality

Limit the highest blueprint quality a user can request.

Use 0 to lift the limit.

Arguments:  
`max_bp_quality` - Highest blueprint quality to allow.  
`cluster` - Optional cluster name for an override.

Examples:
- +rshopset maxbpquality 120
- +rshopset maxbpquality 0 aberration

- **Usage:** `+rshopset maxbpquality <max_bp_quality> [cluster]`
- **Who can use it:** Admin

### +rshopset maxquality

Limit the highest item quality a user can request.

Set it to 0 to remove the cap entirely.

Arguments:  
`max_quality` - Highest quality value the command should allow.  
`cluster` - Optional cluster name for a targeted override.

Examples:
- +rshopset maxquality 100
- +rshopset maxquality 0 valguero

- **Usage:** `+rshopset maxquality <max_quality> [cluster]`
- **Who can use it:** Admin

### +rshopset qualityexp

Tweak the quality exponent multiplier.

Lower values make high-quality requests pricier. Use 0 to turn the modifier off.

Arguments:  
`exponent` - Multiplier value, zero or higher.  
`cluster` - Optional cluster name to scope the change.

Examples:
- +rshopset qualityexp 0.6
- +rshopset qualityexp 0 crystal

- **Usage:** `+rshopset qualityexp <exponent> [cluster]`
- **Who can use it:** Admin

### +rshopset readstacks

Read stack sizes from a Game.ini file.

Attach your `Game.ini` and we'll sync custom stack amounts for matching items.

Examples:
- +rshopset readstacks (with Game.ini attached)

- **Usage:** `+rshopset readstacks`
- **Who can use it:** Admin

### +rshopset template

Download the Excel template for building your shop.

Use this file as the base when creating or updating item listings.

Examples:
- +rshopset template

- **Usage:** `+rshopset template`
- **Who can use it:** Admin

### +rshopset upload

Upload an Excel sheet to refresh the shop.

Attach the exported template with your changes and the bot will replace the current listings.

Examples:
- +rshopset upload (with your sheet attached)

- **Usage:** `+rshopset upload`
- **Who can use it:** Admin

### +rshopset view

Show the current shop configuration for this guild.  
Examples:
- +rshopset view

- **Usage:** `+rshopset view`
- **Who can use it:** Admin

### +shopoverview

Generate a visual summary of the guild's shop economy.

Builds charts and totals for spending, popular items, and top buyers.

Examples:
- +shopoverview

- **Usage:** `+shopoverview`
- **Who can use it:** Everyone
- **Slash command:** also works as `/shopoverview`

### +shopsettings

Show the current shop configuration for this guild.  
Examples:
- +shopsettings

- **Usage:** `+shopsettings`
- **Who can use it:** Everyone

### +shopstats

Show purchase stats for you or another member.

Defaults to your own stats unless you mention someone else.

Arguments:  
`user` - Optional member to inspect.

Examples:
- +shopstats
- +shopstats @Vert

- **Usage:** `+shopstats [user]`
- **Who can use it:** Everyone
- **Slash command:** also works as `/shopstats`

### +arkset toggleshop

Toggle the shop on/off

- **Usage:** `+arkset toggleshop`
- **Who can use it:** Admin

### +arkset toggleshopcluster

Disable the shop for a specific cluster

- **Usage:** `+arkset toggleshopcluster <cluster_name>`
- **Who can use it:** Admin

### +arkset shoplog

Set the shop log channel

All purchases will be logged here

- **Usage:** `+arkset shoplog <channel>`
- **Who can use it:** Admin

### +arkset refundclusterdelta

Refund shop purchases for a cluster within a time window.

Provide the start and end timestamps using `YYYY-MM-DDTHH:MM:SS`.

Arguments:  
`start_time` - Oldest timestamp to refund from.  
`end_time` - Newest timestamp to refund through.  
`cluster_name` - Cluster whose purchases you want to reverse.

Examples:
- +arkset refundclusterdelta 2024-04-03T20:00:00 2024-05-05T18:00:00 pvp

- **Usage:** `+arkset refundclusterdelta <start_time> <end_time> <cluster_name>`
- **Who can use it:** Admin

### +arkset refundserverdelta

Refund purchases for a specific server within a time window.

Use `YYYY-MM-DDTHH:MM:SS` for both timestamps.

Arguments:  
`start_time` - Oldest timestamp to refund from.  
`end_time` - Newest timestamp to refund through.  
`server_name` - Server name within the cluster.  
`cluster_name` - Cluster the server belongs to.

Examples:
- +arkset refundserverdelta 2024-04-03T20:00:00 2024-05-05T18:00:00 volcanic pvp

- **Usage:** `+arkset refundserverdelta <start_time> <end_time> <server_name> <cluster_name>`
- **Who can use it:** Admin

### +arkset refundplaytimedelta

Award players credits based on playtime over a time window.

Arguments:  
`credits_per_hour` - How many credits to award per hour of playtime.  
`start_date` - Start of the time range (e.g. Aug 12, 2025 or 2024-12-01).  
`end_date` - End of the time range (e.g. Dec 15, 2025 or 2024-12-15).  
`dry_run` - If true, show what would be awarded without actually awarding.

Examples:
- +arkset refundplaytimedelta 100 "Aug 1, 2025" "Aug 15, 2025"
- +arkset refundplaytimedelta 50 2024-12-01 2024-12-15 true

- **Usage:** `+arkset refundplaytimedelta <credits_per_hour> <start_date> <end_date> [dry_run]`
- **Who can use it:** Admin

## Lootboxes

Step-by-step guide: [Lootboxes](/guides/lootboxes)

### +lootbox

Open a lootbox

- **Usage:** `+lootbox`
- **Who can use it:** Everyone
- **Also called:** `+lootcrate`

### +lootboxset

Setup the lootbox system

- **Usage:** `+lootboxset <subcommand>`
- **Who can use it:** Admin
- **Also called:** `+lbs`

### +lootboxset add

Quickly add an item to the lootbox system

- **Usage:** `+lootboxset add <chance> <quality> <quantity> <blueprint> <stacksize> <path> <name> [cluster_blacklist]`
- **Who can use it:** Admin

### +lootboxset cooldown

Set the lootbox cooldown

- **Usage:** `+lootboxset cooldown <cooldown>`
- **Who can use it:** Admin

### +lootboxset download

Get the current lootboxes as an Excel file

- **Usage:** `+lootboxset download`
- **Who can use it:** Admin

### +lootboxset logchannel

Set the lootbox log channel

- **Usage:** `+lootboxset logchannel <channel>`
- **Who can use it:** Admin

### +lootboxset price

Set the price of a lootbox

0 Will make the loot box free

- **Usage:** `+lootboxset price <price>`
- **Who can use it:** Admin

### +lootboxset simulate

Simulate opening a lootbox X times and generate a summary of selections.

- **Usage:** `+lootboxset simulate [times]`
- **Who can use it:** Admin
- **Also called:** `+lootboxset sim`

### +lootboxset template

Get an example Excel file for the lootbox system

- **Usage:** `+lootboxset template`
- **Who can use it:** Admin

### +lootboxset toggle

Toggle lootboxes for a specific cluster

- **Usage:** `+lootboxset toggle <cluster_name>`
- **Who can use it:** Admin

### +lootboxset upload

Set the lootbox items

- **Usage:** `+lootboxset upload`
- **Who can use it:** Admin

### +lootboxset view

View general lootbox settings

- **Usage:** `+lootboxset view`
- **Who can use it:** Admin

## Tribe Logs in Discord and Private Tribe Threads

Step-by-step guide: [Tribe Logs in Discord and Private Tribe Threads](/guides/tribe-logs)

### +tribe

Open the tribe menu!

- **Usage:** `+tribe [user]`
- **Who can use it:** Everyone
- **Slash command:** also works as `/tribe`
- **Also called:** `+mytribe`

### +tribeset

Configure tribe settings

- **Usage:** `+tribeset <subcommand>`
- **Who can use it:** Admin

### +tribeset view

View tribe settings

- **Usage:** `+tribeset view`
- **Who can use it:** Admin

### +tribeset logchannel

Set master tribelogs for a cluster

- **Usage:** `+tribeset logchannel <clustername> <channel>`
- **Who can use it:** Admin

### +tribeset claimrole

Add/Remove roles that can claim their tribes

- **Usage:** `+tribeset claimrole <role>`
- **Who can use it:** Admin

### +tribeset claimchannel

Set the channel that private tribelogs threads will be created from

- **Usage:** `+tribeset claimchannel <channel>`
- **Who can use it:** Admin

### +tribeset resetclaims

Wipe the threads from the claimlog channel and reset all claimed tribes

- **Usage:** `+tribeset resetclaims <confirm>`
- **Who can use it:** Admin

### +tribeset unclaim

Force-unclaim a specific member's tribe thread without deleting it

Resets the owner so another player can claim the tribe.  
The thread itself is preserved.

- **Usage:** `+tribeset unclaim <member>`
- **Who can use it:** Admin

### +threadadd

Add a member to your tribelog thread

- **Usage:** `+threadadd <member>`
- **Who can use it:** Everyone
- **Slash command:** also works as `/threadadd`
- **Also called:** `+addmember`, `+tribeaddmate`

### +threadkick

Remove a member from your tribelog thread

- **Usage:** `+threadkick <member>`
- **Who can use it:** Everyone
- **Slash command:** also works as `/threadkick`
- **Also called:** `+kicktribemate`, `+kickmate`

### +threadpurge

Remove ALL members from your tribelog thread except yourself

Use this if unwanted users have been added to your thread and you need to start fresh.  
You will need to re-add your tribemates afterwards.

**Usage:** `+threadpurge true`

- **Usage:** `+threadpurge <confirm>`
- **Who can use it:** Everyone
- **Slash command:** also works as `/threadpurge`
- **Also called:** `+kickall`, `+threadclear`

### +threadmembers

List all members in your tribelog thread

- **Usage:** `+threadmembers`
- **Who can use it:** Everyone
- **Slash command:** also works as `/threadmembers`
- **Also called:** `+threadwho`, `+threadlist`

### +threadtransfer

Transfer thread ownership to another member

The new owner will be able to add/remove members and manage the thread.

- **Usage:** `+threadtransfer <member>`
- **Who can use it:** Everyone
- **Slash command:** also works as `/threadtransfer`
- **Also called:** `+tribetransfer`, `+threadowner`

### +cleantribelogs

Delete tribelog threads that arent associated with a tribe

- **Usage:** `+cleantribelogs`
- **Who can use it:** Admin

## Game Chat in Discord, Kill Feed and Join Logs

Step-by-step guide: [Game Chat in Discord, Kill Feed and Join Logs](/guides/chat-and-logs)

### +arkset killfeed

Toggle the killfeed

The killfeed shows player kills in the map chats in a silly way, it will also shame bob killers publicly

- **Usage:** `+arkset killfeed`
- **Who can use it:** Admin

### +joinlog

Show the join/leave log for a server over a time period.

Arguments:  
`timespan` - How far back to check, e.g. 7d, 12h, 3w.  
`end_time` - Optional end time, e.g. April 10 2032 5:00pm. Defaults to now.

- **Usage:** `+joinlog <timespan> [end_time]`
- **Who can use it:** Mod

### +whowason

List everyone who was online at a specific moment.

Arguments:  
`time` - When to check. Accepts ISO times like 2024-10-15T12:00:00 or natural times such as 4:20pm April 10 2024.

- **Usage:** `+whowason <time>`
- **Who can use it:** Mod

### +timeline

Show a player's join and leave timeline.

Arguments:  
`search_query` - Player name, game ID, or Discord member to inspect.  
`start_time` - When to start the timeline, e.g. April 10 2032 5:00pm.  
`end_time` - Optional time to stop the timeline.

- **Usage:** `+timeline <search_query> <start_time> [end_time]`
- **Who can use it:** Mod

### +lookback

Find where a player was online during a specific window.

Arguments:  
`search_query` - Player name, game ID, or Discord member to look up.  
`start_time` - When to start looking, e.g. April 10 2032 5:00pm.  
`end_time` - Optional time to stop looking, e.g. April 11 2032 5:00pm.

- **Usage:** `+lookback <search_query> <start_time> [end_time]`
- **Who can use it:** Mod

## Moderation

Step-by-step guide: [Moderation: Bans, Temp Bans and Tribe Warnings](/guides/moderation)

### +banplayer

Ban a player from all servers

- **Usage:** `+banplayer <game_id> <reason>`
- **Who can use it:** Mod
- **Slash command:** also works as `/banplayer`

### +tempbanplayer

Temporarily ban a player from all servers

`duration` is the amount of time the player should be banned for.  
`days` is the amount of days of messages to cleanup on tempban.

Examples:
- `+tempbanplayer 2535437775463072 Because I say so`  
This will ban the player with ID 2535437775463072 for the default amount of time set by an administrator.
- `+tempbanplayer 2535437775463072 15m You need a timeout`  
This will ban the player with ID 2535437775463072 for 15 minutes.

- **Usage:** `+tempbanplayer <game_id> [duration] [reason]`
- **Who can use it:** Mod
- **Slash command:** also works as `/tempbanplayer`
- **Also called:** `+tbp`

### +unbanplayer

Unban a player from all servers

- **Usage:** `+unbanplayer <game_id> [reason]`
- **Who can use it:** Mod
- **Slash command:** also works as `/unbanplayer`

### +bans

Manage player bans

- **Usage:** `+bans [query]`
- **Who can use it:** Mod

### +globalbans

View global player bans

- **Usage:** `+globalbans [query]`
- **Who can use it:** Mod
- **Also called:** `+allbans`

### +banfromtext

Ban players from a list of player IDs

The text should be a list of player IDs separated by commas or new lines.

**NOTE**: This will not block players on Xbox, you will need to do that manually.

- **Usage:** `+banfromtext`
- **Who can use it:** Mod

### +unbanfromtext

Unban players from a list of player IDs.

The text should be a list of player IDs separated by spaces or new lines.

XUIDs in the list are also unblocked on every host gamertag (Xbox Live  
block removal) using each server's stored XSAPI tokens.

- **Usage:** `+unbanfromtext`
- **Who can use it:** Mod

### +bantribe

Ban all members of a tribe at once

- **Usage:** `+bantribe <tribe_id> <reason>`
- **Who can use it:** Admin

### +tempbantribe

Temporarily ban all members of a tribe at once.

Arguments:  
`tribe_id` - The tribe ID to ban.  
`duration` - How long to ban for (e.g. 1d, 6h, 30m). Uses the default tempban duration if omitted.  
`reason` - The reason for the ban.

Examples:
- +tempbantribe 12345 1d Meshing
- +tempbantribe 12345 6h Griefing outside raid hours

- **Usage:** `+tempbantribe <tribe_id> [duration] [reason]`
- **Who can use it:** Admin
- **Also called:** `+tbt`

### +warntribe

Warn all members of a tribe at once

- **Usage:** `+warntribe <tribe_id> <warning>`
- **Who can use it:** Admin

### +tribenote

Add a note to all members of a tribe at once

- **Usage:** `+tribenote <tribe_id> <note>`
- **Who can use it:** Admin

### +suswatch

Add/Remove players from the watchlist.

Admins will be alerted when players on the watchlist join or leave a server

`gameid` is their XUID, SteamID, or EOS ID (NOT their username)

- **Usage:** `+suswatch [gameid]`
- **Who can use it:** Admin

### +syncbans

Sync the banlists for all servers

- **Usage:** `+syncbans <subcommand>`
- **Who can use it:** Admin

### +syncbans all

Sync every ban across every server.

Explanation:  
Runs as a dry run by default and shows what would change. Confirm true re-bans missing entries, removes stray bans, and cleans invalid IDs.

Arguments:  
`confirm` - true to apply the changes instead of previewing them.

- **Usage:** `+syncbans all [confirm]`
- **Who can use it:** Admin

### +syncbans betweenservers

Mirror bans between every server.

Explanation:  
Keeps ASA maps in sync with each other, keeps ASE maps in sync, updates the database, and removes invalid IDs. Dry run first, then confirm to commit.

Arguments:  
`confirm` - true to apply the changes instead of previewing them.

- **Usage:** `+syncbans betweenservers [confirm]`
- **Who can use it:** Admin

### +syncbans fromdb

Sync bans using the database as the source of truth.

Explanation:  
Re-bans players missing on servers, removes bans that only exist on servers, and can run as a dry run before confirming.

Arguments:  
`confirm` - true to make the changes. Leave false for a dry run.

- **Usage:** `+syncbans fromdb [confirm]`
- **Who can use it:** Admin

### +syncbans fromserver

Copy bans from the servers into the database.

Explanation:  
Treats each server as the source of truth, cleans invalid IDs, and adds missing database entries. Run without confirm to preview.

Arguments:  
`confirm` - true to make the changes instead of running a dry run.

- **Usage:** `+syncbans fromserver [confirm]`
- **Who can use it:** Admin

## Server Control

Step-by-step guide: [Server Control: RCON Commands, Schedules and Restarts](/guides/server-control)

### +rcon

Run an RCON command

Note that `+doexit`, `+dorestartlevel`, `+banplayer` and `+unbanplayer`  
are standalone commands, running these commands with pure rcon will not execute  
the extra steps associated with these commands like countdowns,  
saving, or player blocking.

- **Usage:** `+rcon <cluster> <server> <command>`
- **Who can use it:** Mod
- **Slash command:** also works as `/rcon`
- **Also called:** `+run`

### +scheduledrcon

Schedule an RCON command to run at a later time.

- **Usage:** `+scheduledrcon [query]`
- **Who can use it:** Admin

### +doexit

Shut a game server down completely.

Sends a countdown broadcast first so players can get safe before it closes.

Arguments:  
`cluster` - Which cluster to target, or all for every cluster.  
`server` - Which map to stop, or all for every map.  
`countdown` - Optional delay like 30s, 1m, or 1m30s before the shutdown.

Examples:
- +doexit main ragnarok 5m
- +doexit all all

- **Usage:** `+doexit <cluster> <server> [countdown]`
- **Who can use it:** Mod
- **Slash command:** also works as `/doexit`

### +dorestartlevel

Restart a server without a full shutdown.

Great for rolling fresh map updates while letting players prep during the countdown.

Arguments:  
`cluster` - Which cluster to restart, or all for every cluster.  
`server` - Which map to restart, or all for every map.  
`countdown` - Optional delay like 30s, 1m, or 1m30s before the restart.

Examples:
- +dorestartlevel main fjordur 2m
- +dorestartlevel all all

- **Usage:** `+dorestartlevel <cluster> <server> [countdown]`
- **Who can use it:** Mod
- **Slash command:** also works as `/dorestartlevel`

### +arkset countdown

Set the `doexit` and `dorestartlevel` countdowns

- **Usage:** `+arkset countdown <seconds>`
- **Who can use it:** Admin

### +arkset modcommands

Mod command allow list

- **Usage:** `+arkset modcommands <command>`
- **Who can use it:** Admin
- **Also called:** `+arkset modcmd`

### +arkset commandblacklist

Set forbidden commands

- **Usage:** `+arkset commandblacklist <command>`
- **Who can use it:** Admin

### +arkset ansicolors

Toggle ANSI color codes in RCON output.

- **Usage:** `+arkset ansicolors`
- **Who can use it:** Admin
- **Also called:** `+arkset ansi`

### +bulksend

Run GiveItem commands multiple times in a row.

Handy when you need to load someone with stacks that craft commands can't handle in one go. Your blueprint string must already include amount, quality, and blueprint flags.

Arguments:  
`cluster` - Cluster the player is on.  
`server` - Server name within that cluster.  
`implant` - Specimen number to send items to.  
`count` - How many times to run the command.  
`blueprint_string` - Full GiveItem blueprint string including numbers.

Examples:
- +bulksend main rag 12345 50 "Blueprint'/Game/...Polymer' 100 1 0"

- **Usage:** `+bulksend <cluster> <server> <implant> <count> <blueprint_string>`
- **Who can use it:** Admin

### /bulksend

Bulk send an item to a player

- **Usage:** `/bulksend <cluster> <server> <implant> <item> <amount> <runcount> [quality] [blueprint]`
- **Who can use it:** Members with the Kick Members permission
- **Slash command only**
  - `cluster`: The cluster to send the item to
  - `server`: The server to send the item to
  - `implant`: The specimen # to send the item to
  - `item`: The item to send
  - `amount`: How many items to send in each run
  - `runcount`: How many times to run the command
  - `quality`: The quality of the item to send
  - `blueprint`: Whether the item is a blueprint

### +excelsend

Send yourself in-game commands from an Excel sheet.

Your excel file must have two columns, `command` and `amount`.
- `command` is the command you want to send to yourself.
- `amount` is the amount of times you want to send the command.

Command Column Example:  
```  
"Blueprint'/Game/PrimalEarth/CoreBlueprints/Resources/PrimalItemResource_Element.PrimalItemResource_Element'" 5 0 0  
```  
Amount Column Example:  
```  
5  
```  
This would send the command 5 times.  
Each command gives you 5 element.  
This would give you a total of 25 element.

- **Usage:** `+excelsend`
- **Who can use it:** Admin
- **Also called:** `+xlsend`

### +clearall

Clear inventory of all players in the server.

- **Usage:** `+clearall <cluster> <server> [inventory] [hotbar] [equipped]`
- **Who can use it:** Mod
- **Slash command:** also works as `/clearall`
  - `cluster`: The cluster to send the item to
  - `server`: The server to send the item to
  - `inventory`: Clear inventory items
  - `hotbar`: Clear hotbar items
  - `equipped`: Clear equipped items

### +equipall

- **Usage:** `+equipall <cluster> <server>`
- **Who can use it:** Mod
- **Slash command:** also works as `/equipall`
  - `cluster`: The cluster to send the item to
  - `server`: The server to send the item to

### +dummywall

Build a list of spawn commands for a loadout dummy wall.

Handy when you want quick cover, cave fillers, or to plug rat holes.

Arguments:  
`width` - How many dummies wide the wall should be.  
`height` - How many dummies tall the wall should be.

Examples:
- +dummywall 2 2
- +dummywall 4 3

- **Usage:** `+dummywall <width> <height>`
- **Who can use it:** Admin

### +dummyfloor

Build a list of spawn commands for a loadout dummy floor.

Perfect for quick foundations or filling cave floors.

Arguments:  
`width` - How many dummies wide the floor should be.  
`depth` - How many rows of dummies to spawn.

Examples:
- +dummyfloor 3 3
- +dummyfloor 5 2

- **Usage:** `+dummyfloor <width> <depth>`
- **Who can use it:** Admin

### +pollvotetime

Check how much playtime each poll voter has logged.

Pulls totals from either overall playtime or just this wipe's map data.

Arguments:  
`message` - The Discord message containing the poll.  
`cluster` - Optional cluster name to filter hours.  
`use_maptime` - True to only count playtime from the current wipe.

Examples:
- +pollvotetime 123456789012345678
- +pollvotetime 123456789012345678 valguero true

- **Usage:** `+pollvotetime <message> [cluster] [use_maptime]`
- **Who can use it:** Mod

### +pollvotefilter

Filter poll votes from players who haven't played on a cluster.

Optionally limit it to hours logged this wipe to keep polls fair.

Arguments:  
`message` - The Discord message containing the poll.  
`cluster_name` - Name of the cluster the poll is about.  
`this_wipe` - True to only count players active this season.

Examples:
- +pollvotefilter 123456789012345678 valguero
- +pollvotefilter 123456789012345678 extinction true

- **Usage:** `+pollvotefilter <message> <cluster_name> [this_wipe]`
- **Who can use it:** Mod

### +remreacts

Remove reactions from a message based on the following.
- `min_playtime`: Minimum playtime required in hours
- `min_joined`: Minimum time in discord in hours
- `min_age`: Minimum age of discord account in hours

- **Usage:** `+remreacts <message> [min_playtime] [min_joined] [min_age]`
- **Who can use it:** Admin

### +unhex

Unhex a string

- **Usage:** `+unhex <text>`
- **Who can use it:** Mod

## Security

Step-by-step guide: [Security: RDP Dupes, Imposters and Name Blacklist](/guides/security)

### +getips 🔹

Get a list of player IPs from the database

- **Usage:** `+getips`
- **Who can use it:** Admin

### +rdpdupe

Configure RDP dupe protection

Detects when the same gameid is online on two maps in the same cluster  
at the same time (the RDP / multi-session obelisk dupe exploit) and  
kicks or bans the player. An alert is posted to the configured RDP-dupe  
log channel (falls back to the alert channel) when detection fires.

- **Usage:** `+rdpdupe <subcommand>`
- **Who can use it:** Mod
- **Also called:** `+rdp`

### +rdpdupe action

Set the enforcement action: `kick` or `ban`

- **Usage:** `+rdpdupe action <action>`
- **Who can use it:** Mod

### +rdpdupe channel

Set (or clear) the channel where RDP dupe alerts are sent.

Leave `channel` blank to clear and fall back to the guild alert channel.

- **Usage:** `+rdpdupe channel [channel]`
- **Who can use it:** Mod

### +rdpdupe toggle

Toggle RDP dupe detection on/off

- **Usage:** `+rdpdupe toggle`
- **Who can use it:** Mod

### +rdpdupe view

View current RDP dupe protection settings

- **Usage:** `+rdpdupe view`
- **Who can use it:** Mod

### +rdpdupe whitelist

Add or remove a gameid from the RDP dupe whitelist

- **Usage:** `+rdpdupe whitelist <gameid>`
- **Who can use it:** Mod

### +arkset banimposters

Protect your server if anyone discovers your admin password

- **Usage:** `+arkset banimposters`
- **Who can use it:** Admin

### +arkset imposterwhitelist

Whitelist certain game IDs from triggering imposter bans

- **Usage:** `+arkset imposterwhitelist <player_id>`
- **Who can use it:** Admin

### +arkset characternameblacklist

Character name blacklist

- **Usage:** `+arkset characternameblacklist <name>`
- **Who can use it:** Admin
- **Also called:** `+arkset charnameblacklist`, `+arkset charbl`, `+arkset badname`

## Map Tools

Step-by-step guide: [Map Tools: Hunt Dinos, Find Tames and Map Structures](/guides/map-tools)

### +hunt 🔹

Hunt for a dino!

Use the slash version of this command to make it private!

- **Usage:** `+hunt <dino>`
- **Who can use it:** Everyone
- **Slash command:** also works as `/hunt`
  - `dino`: The name of the dino you want to search for

### +findtame 🔹

Find tames by tame name, imprinter, tamer, or tribe name

`search_query` can be one of the following.  
The dino's name.  
The name of the person who tamed the dino.  
The name of the person who imprinted on the tame.  
The name of the tribe that owns the dino.  
The ID of the tribe that tamed the dino.

*You can search for unclaimed dinos by specifying `unclaimed`*

- **Usage:** `+findtame <search_query>`
- **Who can use it:** Everyone
- **Slash command:** also works as `/findtame`
  - `search_query`: Dino Name, Tamer, Imprinter, TribeName, or TribeID

### +mytames 🔹

Check your tribe's tames on a map

- **Usage:** `+mytames`
- **Who can use it:** Everyone

### +tamesfor 🔹

Check your tribe's tames on a map

- **Usage:** `+tamesfor <player>`
- **Who can use it:** Mod

### +mystructures 🔹

Count structures near your last known location on a map

- **Usage:** `+mystructures`
- **Who can use it:** Everyone

### +mapstats 🔹

Get detailed stats for a map

- **Usage:** `+mapstats`
- **Who can use it:** Everyone

### +creaturepie 🔹

Get a pie chart of wild dinos on a map

- **Usage:** `+creaturepie [count]`
- **Who can use it:** Everyone

### +structurepie 🔹

Get pie chart of structures

- **Usage:** `+structurepie [count]`
- **Who can use it:** Everyone

### +tamepie 🔹

Get a pie chart of tamed dinos on a map

- **Usage:** `+tamepie [count]`
- **Who can use it:** Everyone

### +playerheat 🔹

Get a heatmap of player locations

- **Usage:** `+playerheat`
- **Who can use it:** Everyone

### +arkviewer 🔹

Quickly view your servers' ArkView metrics

- **Usage:** `+arkviewer`
- **Who can use it:** Everyone
- **Also called:** `+arkview`, `+lastsynced`

### +findplayer 🔹

Find the location and tribe of a player in-game

Mods can use this on clusters where an admin allowed it; admins can use it anywhere.

`search_query` can be one of the following.  
Player's in-game name  
Gamertag or Username  
Specimen number (exact matches only)  
XUID or SteamID (exact matches only)  
Tribe ID (exact matches only)

- **Usage:** `+findplayer <search_query>`
- **Who can use it:** Mod
- **Slash command:** also works as `/findplayer`

### +findtribe 🔹

Find details of a tribe

Mods can use this on clusters where an admin allowed it; admins can use it anywhere.

`search_query` can be one of the following.
- Tribe name
- Tribe ID (exact matches only)
- Player's in-game name
- Gamertag or Username
- Specimen number (exact matches only)
- XUID or SteamID (exact matches only)

If any tribes have the player info found in them, they will be shown

- **Usage:** `+findtribe <search_query>`
- **Who can use it:** Mod

### +finditem 🔹

Search for a specific item on a map

- **Usage:** `+finditem <item_blueprint> [tribe_id]`
- **Who can use it:** Mod

### +structures 🔹

Get a marker map of structures for a tribe

Mods can use this on clusters where an admin allowed it; admins can use it anywhere.

`search_query` can be one of the following.
- Tribe name
- Tribe ID (exact matches only)

- **Usage:** `+structures <search_query>`
- **Who can use it:** Mod
- **Slash command:** also works as `/structures`

### +findstructure 🔹

Get a marker map of specific structures for a tribe or the whole map

`structure_class` is the class name of the structure you want to search for.
- e.g. "CookingPot_C" or "StructureTurretTek_C

`search_query` can be one of the following.
- Tribe name
- Tribe ID (exact matches only)

- **Usage:** `+findstructure <structure_class> [search_query]`
- **Who can use it:** Admin
- **Slash command:** also works as `/findstructure`

### +territory 🔹

Visualize controlled areas of a server by tribe.

- **Usage:** `+territory [include_other] [top]`
- **Who can use it:** Admin

### +structuregraph 🔹

Visualize controlled areas of a server by tribe.

- **Usage:** `+structuregraph`
- **Who can use it:** Admin

### +tribesize 🔹

Visualize a tribe's controlled territory along with their types of structures and area they take up.

- **Usage:** `+tribesize <search_query>`
- **Who can use it:** Admin

### +sortdinos 🔹

Find all dinos above or equal to the specified level

- **Usage:** `+sortdinos <level> [dino_name]`
- **Who can use it:** Admin

### +setcustomdinos 🔹

Register custom dinos for features like hunt and findtame.

Paste entries directly or attach a `.txt` file. Each line should be `FriendlyName|ClassName`.

Arguments:  
`custom_dinos` - Optional pasted list of entries. Attach a file instead if you leave this blank.

Examples:
- +setcustomdinos Royal Griffin|RoyalOwlGriffin_MM_Character_BP_C  
Gecko|Gecko_Character_BP_C
- +setcustomdinos (with custom_dinos.txt attached)

- **Usage:** `+setcustomdinos [custom_dinos]`
- **Who can use it:** Admin

### +showcustomdinos 🔹

Show the list of custom dinos for this guild

- **Usage:** `+showcustomdinos`
- **Who can use it:** Admin
- **Also called:** `+listcustomdinos`, `+getcustomdinos`

### +clearcustomdinos 🔹

Clear all custom dinos for this guild

- **Usage:** `+clearcustomdinos`
- **Who can use it:** Admin

### +servermetrics 🔹

View current server memory usage

- **Usage:** `+servermetrics <metric>`
- **Who can use it:** Admin

### +viewsysinfo 🔹

View data about the system running your servers

- **Usage:** `+viewsysinfo`
- **Who can use it:** Admin

### +avsync 🔹

Sync tribes, players and characters with with the database

- **Usage:** `+avsync`
- **Who can use it:** Admin

## Anti-Cheat

Step-by-step guide: [Anti-Cheat: Dupes, Mass Breeding and Foreign Tames](/guides/anti-cheat)

### +tamedupes 🔹

Find duplicated tames if a tribe has more than X of the same dino ID

- **Usage:** `+tamedupes <cluster_name> <server_name> <threshold>`
- **Who can use it:** Admin

### +checkmassbreed 🔹

Find clusters of dinos left breeding.

Explanation:  
Spots dense groups of dinos with mating enabled so you can deal with mass breeders before they lag the map.

Arguments:  
`threshold` - Maximum distance (lat/lon) between dinos in a cluster. Default 0.5.  
`min_dinos` - Minimum mating dinos in the area before it flags the cluster. Default 6.

- **Usage:** `+checkmassbreed [threshold] [min_dinos]`
- **Who can use it:** Admin
- **Also called:** `+massbreed`

### +scanforeigntames 🔹

Scan all servers for tames that are from a server not in the valid server list

- **Usage:** `+scanforeigntames`
- **Who can use it:** Admin

### +setvalidservers 🔹

Comma separated list of valid server names for this guild, any servers not in this list will be flagged when a tame is transferred to them

- **Usage:** `+setvalidservers <valid_names>`
- **Who can use it:** Admin

### +showvalidservers 🔹

Show the list of valid server names for this guild

- **Usage:** `+showvalidservers`
- **Who can use it:** Admin

### +tamestatcheck 🔹

Find tames that hit a stat goal.

Arguments:  
`stat` - Which stat to check: hp, stam, melee, weight, speed, food, or oxy.  
`points` - Minimum number of points the tame needs in that stat.  
`stat_type` - Choose tamed or wild points. Defaults to tamed.

- **Usage:** `+tamestatcheck <stat> <points> [stat_type]`
- **Who can use it:** Admin

### +uncryocheck 🔹

Get a list of tribes who's uncryo'd tame count is above the specified amount

- **Usage:** `+uncryocheck <amount>`
- **Who can use it:** Admin
- **Also called:** `+cryocheck`

### +findexpired 🔹

Get a list of tribes that haven't been active for more than X days

Example: +findexpired 60  
this will show tribes inactive for 60 days or more that have at least 1 structure or tame

- **Usage:** `+findexpired <days>`
- **Who can use it:** Mod
- **Also called:** `+expired`

### +finddbtribe 🔹

Find details of a tribe from the database

`search_query` can be one of the following.
- Tribe name
- Tribe ID (exact matches only)
- Player's in-game name
- Gamertag or Username
- XUID or SteamID (exact matches only)

Shows tribe data stored in the database.

- **Usage:** `+finddbtribe <search_query>`
- **Who can use it:** Admin

### +wipetribes 🔹

Wipe all tribes that haven't been active for X days or more

This will delete all their tames, structures, and players

- **Usage:** `+wipetribes <days>`
- **Who can use it:** Admin

## Player Stats and Leaderboards

Step-by-step guide: [Player Stats and Leaderboards](/guides/stats-and-leaderboards)

### +playerstats

View info about a player

The optional **player** argument can be one of the following.
- Gamertag or Username
- XUID, Steam ID, PSN ID, or EOS ID
- Discord ID or Username
- @mention

- **Usage:** `+playerstats [player]`
- **Who can use it:** Everyone
- **Slash command:** also works as `/playerstats`

### +players

Show the playtime leaderboard.

Pick a time window to see who played the most recently, or `all` for all-time playtime.  
Filter to a cluster if you just want local rankings.

Arguments:  
`timespan` - How far back to look (e.g. 7d, 2w, 30d), or `all`. Defaults to all.  
`cluster` - Optional cluster name to limit the results.

Examples:
- +players
- +players 7d
- +players 30d scorchedearth
- +players all scorchedearth

- **Usage:** `+players [timespan] [cluster]`
- **Who can use it:** Everyone
- **Also called:** `+arkleaderboard`, `+arklb`, `+arktop`

### +clusterlb

Show the top players on a specific cluster.

Pick which stat to sort by: playtime, tamed, kills, or tamekills.

Arguments:  
`sort_by` - Stat to highlight. Defaults to kills.

Examples:
- +clusterlb playtime
- +clusterlb tamekills

- **Usage:** `+clusterlb [sort_by]`
- **Who can use it:** Everyone

### +tribelb

See which tribes are leading the pack.

Sort by kills, dinos tamed, or structures destroyed. Short forms k, t, and d work too.

Arguments:  
`sort_by` - What stat to rank by.  
`cluster` - Optional cluster name for a local board.

Examples:
- +tribelb kills
- +tribelb d fjordur

- **Usage:** `+tribelb <sort_by> [cluster]`
- **Who can use it:** Everyone
- **Also called:** `+tribetop`

### +totalplaytime

Calculate a player's total playtime between two dates.

Arguments:  
`player_query` - The player's XUID, SteamID, EOSID, Discord ID, Character Implant, ect.  
`start_date` - Start of the time range (e.g. Aug 12, 2025 or 2024-12-01).  
`end_date` - End of the time range (e.g. Dec 15, 2025 or 2024-12-15T23:59:59).

Examples:
- +totalplaytime 2535412345678901 "Aug 1, 2025" "Aug 15, 2025"
- +totalplaytime 76561198012345678 2024-12-01 2024-12-15

- **Usage:** `+totalplaytime <player_query> <start_date> <end_date>`
- **Who can use it:** Mod

### +dbstats

Show ArkTools stats for this guild or globally.

Toggle global mode to compare against all ArkTools servers.

Arguments:  
`showglobal` - True to show global totals instead of this guild.

Examples:
- +dbstats
- +dbstats true

- **Usage:** `+dbstats [showglobal]`
- **Who can use it:** Everyone

## Xbox and Microsoft Store Features

Step-by-step guide: [Xbox and Microsoft Store Features](/guides/xsapi)

### +xsapi 🔸

Xbox crossplay tools/settings

- **Usage:** `+xsapi <subcommand>`
- **Who can use it:** Admin

### +xsapi altdetection 🔸

Alt detection for newly discovered players in-game

Get alerts in the event log when a suspicious account joins a server,  
and optionally Auto-ban them or send a warning message based on customizable settings

[botname] Premium is required to use this system

- **Usage:** `+xsapi altdetection <subcommand>`
- **Who can use it:** Admin
- **Also called:** `+xsapi alt`

### +xsapi altdetection autoban 🔸

Toggle alt detection autoban on/off

**NOTE**  
Auto-ban only applies to Silver accounts. Xbox Gold accounts will be logged but not auto-banned.

- **Usage:** `+xsapi altdetection autoban`
- **Who can use it:** Admin

### +xsapi altdetection channel 🔸

Set the channel for alt detection alerts

- **Usage:** `+xsapi altdetection channel <channel>`
- **Who can use it:** Admin

### +xsapi altdetection threshold 🔸

Set the threshold for alt detection

- **Usage:** `+xsapi altdetection threshold <threshold>`
- **Who can use it:** Admin

### +xsapi altdetection toggle 🔸

Toggle alt detection system on/off

[botname] Premium is required to use this system

- **Usage:** `+xsapi altdetection toggle`
- **Who can use it:** Admin

### +xsapi altdetection whitelist 🔸

Whitelist a cluster for auto-ban

- **Usage:** `+xsapi altdetection whitelist <cluster_name>`
- **Who can use it:** Admin

### +xsapi authenticate 🔸

Authenticate a host gamertag (MS Crossplay Only)

- **Usage:** `+xsapi authenticate`
- **Who can use it:** Admin
- **Also called:** `+xsapi auth`

### +xsapi autofriend 🔸

Auto host gamertag friend/unfriend system

- **Usage:** `+xsapi autofriend <subcommand>`
- **Who can use it:** Admin
- **Also called:** `+xsapi smartmanage`

### +xsapi autofriend toggle 🔸

Toggle the auto-friend system

This will enable automatically adding new players as a friend by the host Gamertag  
and automatically unfriending them after the set number of days of inactivity (Default is 30).  
The Gamertags will also unfriend anyone that isn't following them back  
or leaves the discord after registering.

You must have [botname] Premium to use this!

- **Usage:** `+xsapi autofriend toggle`
- **Who can use it:** Admin

### +xsapi autofriend unfriendtime 🔸

Set days of inactivity to auto-unfriend

This is the number of days of inactivity for the host Gamertags to unfriend a player.

This keeps the xbox host Gamertag friends lists clean since the max you can have is 1000.

- **Usage:** `+xsapi autofriend unfriendtime <days>`
- **Who can use it:** Admin

### +xsapi cleanfriends 🔸

Trim old friends from a host gamertag.

Removes players who haven't been on the specified map within the given timeframe.

Arguments:  
`cluster` - Cluster name to check.  
`server` - Server name within that cluster.  
`days` - How many days of inactivity before removing a friend.

Examples:
- +xsapi cleanfriends valguero pve 30
- +xsapi cleanfriends fjordur main 14

- **Usage:** `+xsapi cleanfriends <cluster> <server> [days]`
- **Who can use it:** Admin

### +xsapi dumpfriends 🔸

Dump a player's friends list and check which ones are in the database.

This will show which other players in your database are friends with this player.

- **Usage:** `+xsapi dumpfriends <xuid>`
- **Who can use it:** Admin

### +xsapi friendinvites 🔸

Get a list of pending friend invites for the host gamertag

- **Usage:** `+xsapi friendinvites <cluster> <server>`
- **Who can use it:** Admin

### +xsapi friendrequests 🔸

Get a list of friend requests for the host gamertag

- **Usage:** `+xsapi friendrequests <cluster> <server>`
- **Who can use it:** Admin

### +xsapi gettokens 🔸

Get a payload dump of your server tokens (Careful not to do in public channel)

- **Usage:** `+xsapi gettokens <cluster> <server>`
- **Who can use it:** Admin

### +xsapi inviteauth 🔸

Authorize a host gamertag to send game invites (needed for `inviteme`)

The host must already be authorized with `xsapi authenticate`.  
Sign in with the host Gamertag email that corresponds with the server you select.

- **Usage:** `+xsapi inviteauth`
- **Who can use it:** Admin

### +xsapi view 🔸

View settings related to the xbox api

- **Usage:** `+xsapi view`
- **Who can use it:** Admin

### +xsapi viewhosts 🔸

View XSAPI info of your servers

- **Usage:** `+xsapi viewhosts`
- **Who can use it:** Admin

### +xdm 🔸

DM a player on Xbox

The message sender will be the host Gamertag of the last server they were on.

- **Usage:** `+xdm <player> <message>`
- **Who can use it:** Admin
- **Slash command:** also works as `/xdm`

### +susrating 🔸

Get a rating for how likely an xbox account is to be an alt

- **Usage:** `+susrating <player>`
- **Who can use it:** Mod

### +addme 🔸

(Xbox/Win10 CROSSPLAY ONLY)Add yourself as a friend

Make the host Gamertags add you as a friend

This command requires api keys to be set for the servers

- **Usage:** `+addme`
- **Who can use it:** Everyone

### +addplayer 🔸

(Xbox/Win10 CROSSPLAY ONLY) Add a player to a host Gamertag's friends list

This command requires api keys to be set for the servers

- **Usage:** `+addplayer <player>`
- **Who can use it:** Admin

### +removeplayer 🔸

Unfriend a player from the host Gamertag

- **Usage:** `+removeplayer <xuid>`
- **Who can use it:** Admin

### +inviteme 🔸

Get an Xbox game invite to one of our servers

The server's host gamertag sends the invite straight to your Xbox.  
You must be registered with an Xbox account first.

- **Usage:** `+inviteme`
- **Who can use it:** Everyone
