---
title: ArkTools Command Dump
description: 
published: true
date: 2026-01-17T18:53:29.321Z
tags: 
editor: markdown
dateCreated: 2023-12-12T01:56:40.592Z
---

AIO server manager for Ark: Survival Evolved!

# /quickbuy (Slash Command)
Quickly buy an item from the Rshop!<br/>
 - Usage: `/quickbuy <item> [quantity] [quality] [blueprint]`
 - `item:` (Required) The item you want to buy
 - `quantity:` (Optional) The quantity of the item you want to buy
 - `quality:` (Optional) The quality of the item you want to buy
 - `blueprint:` (Optional) Whether or not the item is a blueprint

 - Checks: `Server Only`
# /bulksend (Slash Command)
Bulk send an item to a player<br/>
 - Usage: `/bulksend <cluster> <server> <implant> <item> <amount> <runcount> [quality] [blueprint]`
 - `cluster:` (Required) The cluster to send the item to
 - `server:` (Required) The server to send the item to
 - `implant:` (Required) The specimen # to send the item to
 - `item:` (Required) The item to send
 - `amount:` (Required) How many items to send in each run
 - `runcount:` (Required) How many times to run the command
 - `quality:` (Optional) The quality of the item to send
 - `blueprint:` (Optional) Whether the item is a blueprint

 - Checks: `Server Only`
# +susrating
Get a rating for how likely an xbox account is to be an alt<br/>
 - Usage: `+susrating <player>`
 - Restricted to: `MOD`
# +xdm (Hybrid Command)
DM a player on Xbox<br/>

The message sender will be the host Gamertag of the last server they were on.<br/>
 - Usage: `+xdm <player> <message>`
 - Slash Usage: `/xdm <player> <message>`
 - Restricted to: `MOD`
 - Cooldown: `1 per 10.0 seconds`
 - Checks: `server_only`
# +xsapi
Xbox crossplay tools/settings<br/>
 - Usage: `+xsapi`
 - Restricted to: `ADMIN`
## +xsapi viewhosts
View XSAPI info of your servers<br/>
 - Usage: `+xsapi viewhosts`
## +xsapi cleanfriends
Trim old friends from a host gamertag.<br/>

    Removes players who haven't been on the specified map within the given timeframe.<br/>

Arguments:<br/>
`cluster` - Cluster name to check.<br/>
`server` - Server name within that cluster.<br/>
`days` - How many days of inactivity before removing a friend.<br/>

    Examples:<br/>
    - +xsapi cleanfriends valguero pve 30<br/>
    - +xsapi cleanfriends fjordur main 14<br/>
 - Usage: `+xsapi cleanfriends <cluster> <server> [days=30]`
## +xsapi view
View settings related to the xbox api<br/>
 - Usage: `+xsapi view`
## +xsapi friendinvites
Get a list of pending friend invites for the host gamertag<br/>
 - Usage: `+xsapi friendinvites <cluster> <server>`
## +xsapi autofriend
Auto host gamertag friend/unfriend system<br/>
 - Usage: `+xsapi autofriend`
 - Aliases: `smartmanage`
### +xsapi autofriend unfriendtime
Set days of inactivity to auto-unfriend<br/>

This is the number of days of inactivity for the host Gamertags to unfriend a player.<br/>

This keeps the xbox host Gamertag friends lists clean since the max you can have is 1000.<br/>
 - Usage: `+xsapi autofriend unfriendtime <days>`
### +xsapi autofriend toggle
Toggle the auto-friend system<br/>

This will enable automatically adding new players as a friend by the host Gamertag<br/>
and automatically unfriending them after the set number of days of inactivity (Default is 30).<br/>
The Gamertags will also unfriend anyone that isn't following them back<br/>
or leaves the discord after registering.<br/>

You must have Arkon Premium to use this!<br/>
 - Usage: `+xsapi autofriend toggle`
## +xsapi altdetection
Alt detection for newly discovered players in-game<br/>

Get alerts in the event log when a suspicious account joins a server,<br/>
and optionally Auto-ban them or send a warning message based on customizable settings<br/>

Arkon Premium is required to use this system<br/>
 - Usage: `+xsapi altdetection`
 - Aliases: `alt`
### +xsapi altdetection threshold
Set the threshold for alt detection<br/>
 - Usage: `+xsapi altdetection threshold <threshold>`
### +xsapi altdetection channel
Set the channel for alt detection alerts<br/>
 - Usage: `+xsapi altdetection channel <channel>`
### +xsapi altdetection whitelist
Whitelist a cluster for auto-ban<br/>
 - Usage: `+xsapi altdetection whitelist <cluster_name>`
### +xsapi altdetection toggle
Toggle alt detection system on/off<br/>

Arkon Premium is required to use this system<br/>
 - Usage: `+xsapi altdetection toggle`
### +xsapi altdetection autoban
Toggle alt detection autoban on/off<br/>

**NOTE**<br/>
Auto-ban only applies to Silver accounts. Xbox Gold accounts will be logged but not auto-banned.<br/>
 - Usage: `+xsapi altdetection autoban`
## +xsapi dumpfriends
Dump a player's friends list and check which ones are in the database.<br/>

This will show which other players in your database are friends with this player.<br/>
 - Usage: `+xsapi dumpfriends <xuid>`
 - Restricted to: `MOD`
## +xsapi friendrequests
Get a list of friend requests for the host gamertag<br/>
 - Usage: `+xsapi friendrequests <cluster> <server>`
## +xsapi authenticate
Authenticate a host gamertag (MS Crossplay Only)<br/>
 - Usage: `+xsapi authenticate`
 - Aliases: `auth`
## +xsapi gettokens
Get a payload dump of your server tokens (Careful not to do in public channel)<br/>
 - Usage: `+xsapi gettokens <cluster> <server>`
# +tribe (Hybrid Command)
Open the tribe menu!<br/>
 - Usage: `+tribe [user]`
 - Slash Usage: `/tribe [user]`
 - Aliases: `mytribe`
# +kicktribemate (Hybrid Command)
Kick a member from your tribelog thread<br/>
 - Usage: `+kicktribemate <member>`
 - Slash Usage: `/kicktribemate <member>`
 - Aliases: `kickmate and kickfromtribelogs`
# +tribeset
Configure tribe settings<br/>
 - Usage: `+tribeset`
 - Restricted to: `ADMIN`
 - Checks: `server_only`
## +tribeset resetclaims
Wipe the threads from the claimlog channel and reset all claimed tribes<br/>
 - Usage: `+tribeset resetclaims <confirm>`
## +tribeset logchannel
Set master tribelogs for a cluster<br/>
 - Usage: `+tribeset logchannel <clustername> <channel>`
## +tribeset view
View tribe settings<br/>
 - Usage: `+tribeset view`
## +tribeset claimrole
Add/Remove roles that can claim their tribes<br/>
 - Usage: `+tribeset claimrole <role>`
## +tribeset claimchannel
Set the channel that private tribelogs threads will be created from<br/>
 - Usage: `+tribeset claimchannel <channel>`
# +serverstatus
Server status channel settings<br/>
 - Usage: `+serverstatus`
 - Restricted to: `ADMIN`
## +serverstatus channel
Set the status channel for your Ark servers<br/>
 - Usage: `+serverstatus channel <channel>`
## +serverstatus init
Initialize the status message<br/>
 - Usage: `+serverstatus init`
## +serverstatus time
Set the status graph timedelta<br/>
 - Usage: `+serverstatus time <seconds>`
# +tribeitemsmanual
Get a list of all tribes that have a specific item along with the quantity<br/>
 - Usage: `+tribeitemsmanual <item_path> <cluster_name> <server_name>`
 - Restricted to: `ADMIN`
 - Aliases: `tribeitemsm`
 - Checks: `server_only`
# +tribeitems
Get a list of all tribes that have a specific item along with the quantity<br/>
 - Usage: `+tribeitems <item_path>`
 - Restricted to: `ADMIN`
 - Checks: `server_only`
# +tamedupes
Find duplicated tames if a tribe has more than X of the same dino ID<br/>
 - Usage: `+tamedupes <cluster_name> <server_name> <threshold>`
 - Restricted to: `ADMIN`
 - Checks: `server_only`
# +viewservers
Open the main menu for server management<br/>
 - Usage: `+viewservers`
 - Restricted to: `ADMIN`
 - Checks: `ensure_db_connection`
# +addcluster
Create a cluster to group your servers.<br/>

    One cluster collects join, leave, and admin logs for a set of maps.<br/>
    Configure log channels later from the server management menu.<br/>

Arguments:<br/>
`name` - Unique name for the cluster.<br/>

    Examples:<br/>
    - +addcluster mycluster<br/>
 - Usage: `+addcluster <name>`
 - Restricted to: `ADMIN`
 - Checks: `ensure_db_connection`
# +delcluster
Delete a cluster<br/>
 - Usage: `+delcluster <cluster_name>`
 - Restricted to: `ADMIN`
 - Aliases: `remcluster`
 - Checks: `ensure_db_connection`
# +addserver
Add a server to one of your clusters.<br/>

    We'll guide you through setting IP, RCON, and other details once you start.<br/>
    Set the chat relay channel later from the server configuration menu.<br/>

Arguments:<br/>
`cluster_name` - Name of the cluster this server belongs to.<br/>

    Examples:<br/>
    - +addserver mycluster<br/>
 - Usage: `+addserver <cluster_name>`
 - Restricted to: `ADMIN`
 - Checks: `ensure_db_connection`
# +delserver
Delete a server<br/>
 - Usage: `+delserver <cluster_name> <server_name>`
 - Restricted to: `ADMIN`
 - Aliases: `remserver`
 - Checks: `ensure_db_connection`
# +scheduledrcon
Schedule an RCON command to run at a later time.<br/>
 - Usage: `+scheduledrcon [query]`
 - Restricted to: `ADMIN`
 - Checks: `server_only`
# +rshopset
Admin setup commands for the RCON shop.<br/>

Run with a subcommand to manage pricing, discounts, and exports.<br/>
Examples:<br/>
- +rshopset view<br/>
- +rshopset discount 0.15<br/>
 - Usage: `+rshopset`
 - Restricted to: `ADMIN`
 - Aliases: `rss`
 - Checks: `server_only`
## +rshopset reprice
Recalculate shop prices from a base price sheet.<br/>

The Excel file needs a `base_prices` sheet with two columns: resource and price. Include every base ingredient you can't break down further.<br/>

    Examples:<br/>
    - +rshopset reprice (with base_prices.xlsx attached)<br/>
 - Usage: `+rshopset reprice`
## +rshopset delimiter
Set the delimiter used inside pack rows.<br/>

    Choose how multiple blueprint paths or commands are separated in the packs sheet.<br/>

Arguments:<br/>
`delimiter` - The separator character or string to use.<br/>

    Examples:<br/>
    - +rshopset delimiter |<br/>
    - +rshopset delimiter ;<br/>
 - Usage: `+rshopset delimiter <delimiter>`
## +rshopset readstacks
Read stack sizes from a Game.ini file.<br/>

Attach your `Game.ini` and we'll sync custom stack amounts for matching items.<br/>

    Examples:<br/>
    - +rshopset readstacks (with Game.ini attached)<br/>
 - Usage: `+rshopset readstacks`
## +rshopset discount
Set a flat discount for the shop.<br/>

    Provide 0 to disable. Target a cluster or leave blank for all of them.<br/>

Arguments:<br/>
`discount` - Percent as a decimal, between 0 and 0.99.<br/>
`cluster` - Optional cluster name to scope the discount.<br/>

    Examples:<br/>
    - +rshopset discount 0.2<br/>
    - +rshopset discount 0 extinction<br/>
 - Usage: `+rshopset discount <discount> [cluster]`
## +rshopset view
Show the current shop configuration for this server.<br/>
Examples:<br/>
- +rshopset view<br/>
 - Usage: `+rshopset view`
## +rshopset qualityexp
Tweak the quality exponent multiplier.<br/>

    Lower values make high-quality requests pricier. Use 0 to turn the modifier off.<br/>

Arguments:<br/>
`exponent` - Multiplier value, zero or higher.<br/>
`cluster` - Optional cluster name to scope the change.<br/>

    Examples:<br/>
    - +rshopset qualityexp 0.6<br/>
    - +rshopset qualityexp 0 crystal<br/>
 - Usage: `+rshopset qualityexp <exponent> [cluster]`
## +rshopset template
Download the Excel template for building your shop.<br/>

Use this file as the base when creating or updating item listings.<br/>

Examples:<br/>
- +rshopset template<br/>
 - Usage: `+rshopset template`
## +rshopset maxbpquality
Limit the highest blueprint quality a user can request.<br/>

Use 0 to lift the limit.<br/>

Arguments:<br/>
`max_bp_quality` - Highest blueprint quality to allow.<br/>
`cluster` - Optional cluster name for an override.<br/>

Examples:<br/>
- +rshopset maxbpquality 120<br/>
- +rshopset maxbpquality 0 aberration<br/>
 - Usage: `+rshopset maxbpquality <max_bp_quality> [cluster]`
## +rshopset download
Export the current shop to Excel.<br/>

Useful for backups or editing in bulk before re-uploading.<br/>

Examples:<br/>
- +rshopset download<br/>
 - Usage: `+rshopset download`
## +rshopset upload
Upload an Excel sheet to refresh the shop.<br/>

Attach the exported template with your changes and the bot will replace the current listings.<br/>

    Examples:<br/>
    - +rshopset upload (with your sheet attached)<br/>
 - Usage: `+rshopset upload`
## +rshopset discountdays
Set a specific day's discount rotation.<br/>

    Use numbers 0-6 for Monday through Sunday. Put 0 to clear that day's promo.<br/>

Arguments:<br/>
`day` - Day index (0 = Monday ... 6 = Sunday).<br/>
`discount` - Percent as a decimal, between 0 and 0.99.<br/>

    Examples:<br/>
    - +rshopset discountdays 5 0.15<br/>
    - +rshopset discountdays 2 0<br/>
 - Usage: `+rshopset discountdays <day> <discount>`
 - Aliases: `discountday and dd`
## +rshopset maxquality
Limit the highest item quality a user can request.<br/>

    Set it to 0 to remove the cap entirely.<br/>

Arguments:<br/>
`max_quality` - Highest quality value the command should allow.<br/>
`cluster` - Optional cluster name for a targeted override.<br/>

    Examples:<br/>
    - +rshopset maxquality 100<br/>
    - +rshopset maxquality 0 valguero<br/>
 - Usage: `+rshopset maxquality <max_quality> [cluster]`
## +rshopset bpmultiplier
Adjust the blueprint pricing multiplier.<br/>

    Helps offset extra work when players request blueprints instead of items. Use 0 to disable.<br/>

Arguments:<br/>
`blueprint_multiplier` - Multiplier value, zero or higher.<br/>
`cluster` - Optional cluster name for a local rule.<br/>

    Examples:<br/>
    - +rshopset bpmultiplier 1.5<br/>
    - +rshopset bpmultiplier 0 fjordur<br/>
 - Usage: `+rshopset bpmultiplier <blueprint_multiplier> [cluster]`
## +rshopset discountrole
Give a role a permanent shop discount.<br/>

    Set the value to 0 to remove the role from the list.<br/>

Arguments:<br/>
`role` - Discord role to adjust.<br/>
`discount` - Percent as a decimal, between 0 and 0.99.<br/>

    Examples:<br/>
    - +rshopset discountrole @VIP 0.1<br/>
    - +rshopset discountrole @Member 0<br/>
 - Usage: `+rshopset discountrole <role> <discount>`
## +rshopset autorefund
Toggle automatic refunds when purchases fail.<br/>

When enabled, players get their currency back if a command errors out. One-command purchases always refund.<br/>
Examples:<br/>
- +rshopset autorefund<br/>
 - Usage: `+rshopset autorefund`
 - Aliases: `refunds and refund`
# +shopsettings
Show the current shop configuration for this server.<br/>
Examples:<br/>
- +shopsettings<br/>
 - Usage: `+shopsettings`
 - Checks: `server_only`
# +rshop (Hybrid Command)
Open the in-game RCON shop.<br/>

    Start typing to filter items, or browse the full catalog.<br/>

Arguments:<br/>
`item` - Optional search term to jump straight to an item.<br/>

    Examples:<br/>
    - +rshop<br/>
    - +rshop shotgun<br/>
 - Usage: `+rshop [item]`
 - Slash Usage: `/rshop [item]`
 - Checks: `server_only`
# +shopstats (Hybrid Command)
Show purchase stats for you or another member.<br/>

    Defaults to your own stats unless you mention someone else.<br/>

Arguments:<br/>
`user` - Optional member to inspect.<br/>

    Examples:<br/>
    - +shopstats<br/>
    - +shopstats @Vert<br/>
 - Usage: `+shopstats [user=None]`
 - Slash Usage: `/shopstats [user=None]`
 - Checks: `server_only`
# +shopoverview (Hybrid Command)
Generate a visual summary of the server's shop economy.<br/>

Builds charts and totals for spending, popular items, and top buyers.<br/>

Examples:<br/>
- +shopoverview<br/>
 - Usage: `+shopoverview`
 - Slash Usage: `/shopoverview`
 - Checks: `server_only`
# +registerplayer (Hybrid Command)
Register another user to the database.<br/>
 - Usage: `+registerplayer <member> <gameid> [overwrite=False]`
 - Slash Usage: `/registerplayer <member> <gameid> [overwrite=False]`
 - Restricted to: `ADMIN`
 - Checks: `server_only`
# +setplayerimplant (Hybrid Command)
Set the implant number for a player.<br/>
 - Usage: `+setplayerimplant <gameid> <implant>`
 - Slash Usage: `/setplayerimplant <gameid> <implant>`
 - Restricted to: `ADMIN`
 - Checks: `server_only`
# +register (Hybrid Command)
Register your in-game account with the database.<br/>
 - Usage: `+register [username]`
 - Slash Usage: `/register [username]`
 - Checks: `server_only`
# +addme
(Xbox/Win10 CROSSPLAY ONLY)Add yourself as a friend<br/>

Make the host Gamertags add you as a friend<br/>

This command requires api keys to be set for the servers<br/>
 - Usage: `+addme`
 - Checks: `server_only`
# +addplayer
(Xbox/Win10 CROSSPLAY ONLY) Add a player to a host Gamertag's friends list<br/>

This command requires api keys to be set for the servers<br/>
 - Usage: `+addplayer <player>`
 - Restricted to: `ADMIN`
 - Checks: `server_only`
# +removeplayer
Unfriend a player from the host Gamertag<br/>
 - Usage: `+removeplayer <xuid>`
 - Restricted to: `ADMIN`
 - Checks: `server_only`
# +unregisterplayer
Unlink the discord account from a player<br/>

The optional **player** argument can be one of the following.<br/>
- Gamertag or Steam Username<br/>
- XUID or Steam ID<br/>
- Discord ID or Username<br/>
- @mention<br/>
 - Usage: `+unregisterplayer <player>`
 - Restricted to: `MOD`
 - Checks: `server_only`
# +unregister
Unregister yourself<br/>

Removes you from any Gamertags you have registered to<br/>
 - Usage: `+unregister`
 - Aliases: `unregisterme`
 - Checks: `server_only`
# +specimen
Set your specimen number to use the Rshop<br/>

Your specimen number (aka Implant ID) can be found in the top left of your player inventory.<br/>
 - Usage: `+specimen <specimen_number>`
 - Aliases: `implant, speciment, implantid, and specimen#`
 - Checks: `server_only`
# +resetclusterpoints
Reset alpha points for all tribes of a specific cluster<br/>
 - Usage: `+resetclusterpoints <cluster>`
 - Restricted to: `ADMIN`
 - Checks: `server_only`
# +resetpoints
Reset alpha points for a specific tribe<br/>
 - Usage: `+resetpoints <cluster> <server> <tribe_id>`
 - Restricted to: `ADMIN`
 - Checks: `server_only`
# +power
View the power leaderboard for your server<br/>

Power rating is calculated based on the following structure points:<br/>
- Generator: 1<br/>
- Plant Z: 2<br/>
- Plant X: 5<br/>
- Tek Generator: 8<br/>
- Ballista Turret: 9<br/>
- Catapult Turret: 9<br/>
- Auto Turret: 20<br/>
- Heavy Turret: 35<br/>
- Tek Turret: 55<br/>
- Tek Forcefield: 100<br/>

**Note**: Powered structures MUST be powered on to count towards power rating.<br/>
 - Usage: `+power`
 - Aliases: `powerlb and powertop`
 - Cooldown: `1 per 3.0 seconds`
 - Checks: `server_only`
# +alpha
View the cluster alpha leaderboard for your server<br/>

**How does this work?**<br/>
Gaining points is kind of like King of the Hill with multiple hills controlled increasing points per hour.<br/>
The more powerful your tribe is, the more points you will gain per hour.<br/>
Every hour, the bot will calculate each tribe's "Power" rating.<br/>
Points added each hour == Natrual log of the tribe's power rating rounded to the nearest whole number.<br/>
Example:<br/>
- 100 power = 5 points added per hour<br/>
- 5000 power = 9 points added per hour<br/>

Power rating is calculated based on the following structure points:<br/>
- Generator: 1<br/>
- Plant Z: 2<br/>
- Plant X: 5<br/>
- Tek Generator: 8<br/>
- Ballista Turret: 9<br/>
- Catapult Turret: 9<br/>
- Auto Turret: 20<br/>
- Heavy Turret: 35<br/>
- Tek Turret: 55<br/>
- Tek Forcefield: 100<br/>
 - Usage: `+alpha`
 - Aliases: `alphaboard and alphalb`
 - Cooldown: `1 per 3.0 seconds`
 - Checks: `server_only`
# +playerstats (Hybrid Command)
View info about a player<br/>

The optional **player** argument can be one of the following.<br/>
- Gamertag or Username<br/>
- XUID, Steam ID, PSN ID, or EOS ID<br/>
- Discord ID or Username<br/>
- @mention<br/>
 - Usage: `+playerstats [player]`
 - Slash Usage: `/playerstats [player]`
 - Checks: `server_only`
# +clusterlb
Show the top players on a specific cluster.<br/>

    Pick which stat to sort by: playtime, tamed, kills, or tamekills.<br/>

Arguments:<br/>
`sort_by` - Stat to highlight. Defaults to kills.<br/>

    Examples:<br/>
    - +clusterlb playtime<br/>
    - +clusterlb tamekills<br/>
 - Usage: `+clusterlb [sort_by=kills]`
 - Checks: `server_only`
# +players
Show the overall playtime leaderboard.<br/>

    Filter to a cluster if you just want local rankings.<br/>

Arguments:<br/>
`cluster` - Optional cluster name to limit the results.<br/>

    Examples:<br/>
    - +players<br/>
    - +players scorchedearth<br/>
 - Usage: `+players [cluster=None]`
 - Aliases: `arkleaderboard, arklb, and arktop`
 - Checks: `server_only`
# +tribelb
See which tribes are leading the pack.<br/>

    Sort by kills, dinos tamed, or structures destroyed. Short forms k, t, and d work too.<br/>

Arguments:<br/>
`sort_by` - What stat to rank by.<br/>
`cluster` - Optional cluster name for a local board.<br/>

    Examples:<br/>
    - +tribelb kills<br/>
    - +tribelb d fjordur<br/>
 - Usage: `+tribelb <sort_by> [cluster=None]`
 - Aliases: `tribetop`
 - Checks: `server_only`
# +findsurvivor
Look up a survivor by character name.<br/>

    Returns their servers, tribes, and recent activity if we have it logged.<br/>

Arguments:<br/>
`survivor_name` - Anything we can use to match the character name.<br/>

    Examples:<br/>
    - +findsurvivor Vertyco<br/>
    - +findsurvivor "Super Survivor"<br/>
 - Usage: `+findsurvivor <survivor_name>`
 - Aliases: `findcharname`
 - Checks: `server_only`
# +dbstats
Show ArkTools stats for this server or globally.<br/>

    Toggle global mode to compare against all ArkTools servers.<br/>

Arguments:<br/>
`showglobal` - True to show global totals instead of this server.<br/>

    Examples:<br/>
    - +dbstats<br/>
    - +dbstats true<br/>
 - Usage: `+dbstats [showglobal=False]`
 - Checks: `server_only`
# +kickme
Kick your character from the server.<br/>

Use this when you're stuck in a loading screen or need a fresh join.<br/>

Examples:<br/>
- +kickme<br/>
 - Usage: `+kickme`
 - Cooldown: `1 per 60.0 seconds`
 - Checks: `server_only`
# +playercounts
View player counts either globally or locally<br/>
 - Usage: `+playercounts [local=False]`
 - Cooldown: `1 per 10.0 seconds`
# +excelsend
Send yourself in-game commands from an Excel sheet.<br/>

Your excel file must have two columns, `command` and `amount`.<br/>
- `command` is the command you want to send to yourself.<br/>
- `amount` is the amount of times you want to send the command.<br/>

Command Column Example:<br/>
```
"Blueprint'/Game/PrimalEarth/CoreBlueprints/Resources/PrimalItemResource_Element.PrimalItemResource_Element'" 5 0 0
```
Amount Column Example:<br/>
```
5
```
This would send the command 5 times.<br/>
Each command gives you 5 element.<br/>
This would give you a total of 25 element.<br/>
 - Usage: `+excelsend`
 - Restricted to: `ADMIN`
 - Aliases: `xlsend`
 - Checks: `server_only`
# +dummywall
Build a list of spawn commands for a loadout dummy wall.<br/>

    Handy when you want quick cover, cave fillers, or to plug rat holes.<br/>

Arguments:<br/>
`width` - How many dummies wide the wall should be.<br/>
`height` - How many dummies tall the wall should be.<br/>

    Examples:<br/>
    - +dummywall 2 2<br/>
    - +dummywall 4 3<br/>
 - Usage: `+dummywall <width> <height>`
 - Restricted to: `ADMIN`
# +dummyfloor
Build a list of spawn commands for a loadout dummy floor.<br/>

    Perfect for quick foundations or filling cave floors.<br/>

Arguments:<br/>
`width` - How many dummies wide the floor should be.<br/>
`depth` - How many rows of dummies to spawn.<br/>

    Examples:<br/>
    - +dummyfloor 3 3<br/>
    - +dummyfloor 5 2<br/>
 - Usage: `+dummyfloor <width> <depth>`
 - Restricted to: `ADMIN`
# +rcon (Hybrid Command)
Run an RCON command<br/>

Note that `+doexit`, `+dorestartlevel`, `+banplayer` and `+unbanplayer`<br/>
are standalone commands, running these commands with pure rcon will not execute<br/>
the extra steps associated with these commands like countdowns,<br/>
saving, or player blocking.<br/>
 - Usage: `+rcon <cluster> <server> <command>`
 - Slash Usage: `/rcon <cluster> <server> <command>`
 - Restricted to: `MOD`
 - Aliases: `run`
 - Checks: `ensure_db_connection and server_only`
# +bulksend
Run GiveItem commands multiple times in a row.<br/>

    Handy when you need to load someone with stacks that craft commands can't handle in one go. Your blueprint string must already include amount, quality, and blueprint flags.<br/>

Arguments:<br/>
`cluster` - Cluster the player is on.<br/>
`server` - Server name within that cluster.<br/>
`implant` - Specimen number to send items to.<br/>
`count` - How many times to run the command.<br/>
`blueprint_string` - Full GiveItem blueprint string including numbers.<br/>

    Examples:<br/>
    - +bulksend main rag 12345 50 "Blueprint'/Game/...Polymer' 100 1 0"<br/>
 - Usage: `+bulksend <cluster> <server> <implant> <count> <blueprint_string>`
 - Restricted to: `ADMIN`
 - Checks: `ensure_db_connection and server_only`
# +banplayer (Hybrid Command)
Ban a player from all servers<br/>
 - Usage: `+banplayer <game_id> <reason>`
 - Slash Usage: `/banplayer <game_id> <reason>`
 - Restricted to: `MOD`
 - Checks: `server_only and ensure_db_connection`
# +unbanplayer (Hybrid Command)
Unban a player from all servers<br/>
 - Usage: `+unbanplayer <game_id> [reason]`
 - Slash Usage: `/unbanplayer <game_id> [reason]`
 - Restricted to: `MOD`
 - Checks: `server_only and ensure_db_connection`
# +tempbanplayer (Hybrid Command)
Temporarily ban a player from all servers<br/>

`duration` is the amount of time the player should be banned for.<br/>
`days` is the amount of days of messages to cleanup on tempban.<br/>

Examples:<br/>
- `+tempbanplayer 2535437775463072 Because I say so`<br/>
    This will ban the player with ID 2535437775463072 for the default amount of time set by an administrator.<br/>
- `+tempbanplayer 2535437775463072 15m You need a timeout`<br/>
    This will ban the player with ID 2535437775463072 for 15 minutes.<br/>
 - Usage: `+tempbanplayer <game_id> [duration=None] [reason]`
 - Slash Usage: `/tempbanplayer <game_id> [duration=None] [reason]`
 - Restricted to: `MOD`
 - Aliases: `tbp`
 - Checks: `server_only and ensure_db_connection`
# +setplayertime
Set the tracked playtime for a player.<br/>

    Use common time shorthand like 1d, 6h, or 45m. Combine them for longer spans, such as 3d12h.<br/>

Arguments:<br/>
`time` - How much playtime to assign.<br/>
`player_query` - Name, ID, or partial match for the player.<br/>

    Examples:<br/>
    - +setplayertime 2d6h Vertyco<br/>
    - +setplayertime 45m "Player Name"<br/>
 - Usage: `+setplayertime <time> <player_query>`
 - Restricted to: `ADMIN`
 - Checks: `server_only and ensure_db_connection`
# +unbanfromtext
Unban players from a list of player IDs<br/>

The text should be a list of player IDs separated by spaces or new lines.<br/>

**NOTE**: This will not unblock players on Xbox, you will need to do that manually.<br/>
 - Usage: `+unbanfromtext`
 - Restricted to: `MOD`
 - Checks: `server_only and ensure_db_connection`
# +banfromtext
Ban players from a list of player IDs<br/>

The text should be a list of player IDs separated by commas or new lines.<br/>

**NOTE**: This will not block players on Xbox, you will need to do that manually.<br/>
 - Usage: `+banfromtext`
 - Restricted to: `MOD`
 - Checks: `ensure_db_connection and server_only`
# +doexit (Hybrid Command)
Shut a game server down completely.<br/>

    Sends a countdown broadcast first so players can get safe before it closes.<br/>

Arguments:<br/>
`cluster` - Which cluster to target, or all for every cluster.<br/>
`server` - Which map to stop, or all for every map.<br/>
`countdown` - Optional delay like 30s, 1m, or 1m30s before the shutdown.<br/>

    Examples:<br/>
    - +doexit main ragnarok 5m<br/>
    - +doexit all all<br/>
 - Usage: `+doexit <cluster> <server> [countdown=None]`
 - Slash Usage: `/doexit <cluster> <server> [countdown=None]`
 - Restricted to: `MOD`
 - Checks: `server_only and ensure_db_connection`
# +dorestartlevel (Hybrid Command)
Restart a server without a full shutdown.<br/>

    Great for rolling fresh map updates while letting players prep during the countdown.<br/>

Arguments:<br/>
`cluster` - Which cluster to restart, or all for every cluster.<br/>
`server` - Which map to restart, or all for every map.<br/>
`countdown` - Optional delay like 30s, 1m, or 1m30s before the restart.<br/>

    Examples:<br/>
    - +dorestartlevel main fjordur 2m<br/>
    - +dorestartlevel all all<br/>
 - Usage: `+dorestartlevel <cluster> <server> [countdown=None]`
 - Slash Usage: `/dorestartlevel <cluster> <server> [countdown=None]`
 - Restricted to: `MOD`
 - Checks: `server_only and ensure_db_connection`
# +resetkit
Reset a players claimed kit<br/>

If per-server kits are enabled, this will reset the kit for all servers in the cluster.<br/>
 - Usage: `+resetkit <gameid>`
 - Restricted to: `ADMIN`
 - Checks: `ensure_db_connection and server_only`
# +cleantribelogs
Delete tribelog threads that arent associated with a tribe<br/>
 - Usage: `+cleantribelogs`
 - Restricted to: `ADMIN`
 - Checks: `ensure_db_connection and server_only`
# +resetclusterkits
Reset all player kits for a cluster<br/>

If per-server kits are enabled, this will reset all kits for all servers in the cluster.<br/>
 - Usage: `+resetclusterkits <cluster_name>`
 - Restricted to: `ADMIN`
 - Checks: `ensure_db_connection and server_only`
# +remreacts
Remove reactions from a message based on the following.<br/>
- `min_playtime`: Minimum playtime required in hours<br/>
- `min_joined`: Minimum time in discord in hours<br/>
- `min_age`: Minimum age of discord account in hours<br/>
 - Usage: `+remreacts <message> [min_playtime=0] [min_joined=0] [min_age=0]`
 - Restricted to: `ADMIN`
 - Checks: `ensure_db_connection and server_only`
# +bans
Manage player bans<br/>
 - Usage: `+bans [query]`
 - Restricted to: `MOD`
 - Checks: `ensure_db_connection and server_only`
# +globalbans
View global player bans<br/>
 - Usage: `+globalbans [query]`
 - Restricted to: `MOD`
 - Aliases: `allbans`
 - Checks: `ensure_db_connection and server_only`
# +pollvotetime
Check how much playtime each poll voter has logged.<br/>

    Pulls totals from either overall playtime or just this wipe's map data.<br/>

Arguments:<br/>
`message` - The Discord message containing the poll.<br/>
`cluster` - Optional cluster name to filter hours.<br/>
`use_maptime` - True to only count playtime from the current wipe.<br/>

    Examples:<br/>
    - +pollvotetime 123456789012345678<br/>
    - +pollvotetime 123456789012345678 valguero true<br/>
 - Usage: `+pollvotetime <message> [cluster=None] [use_maptime=False]`
 - Restricted to: `MOD`
 - Checks: `ensure_db_connection and server_only`
# +pollvotefilter
Filter poll votes from players who haven't played on a cluster.<br/>

    Optionally limit it to hours logged this wipe to keep polls fair.<br/>

Arguments:<br/>
`message` - The Discord message containing the poll.<br/>
`cluster_name` - Name of the cluster the poll is about.<br/>
`this_wipe` - True to only count players active this season.<br/>

    Examples:<br/>
    - +pollvotefilter 123456789012345678 valguero<br/>
    - +pollvotefilter 123456789012345678 extinction true<br/>
 - Usage: `+pollvotefilter <message> <cluster_name> [this_wipe=False]`
 - Restricted to: `MOD`
 - Checks: `ensure_db_connection and server_only`
# +suswatch
Add/Remove players from the watchlist.<br/>

Admins will be alerted when players on the watchlist join or leave a server<br/>

`gameid` is their XUID, SteamID, or EOS ID (NOT their username)<br/>
 - Usage: `+suswatch [gameid=None]`
 - Restricted to: `ADMIN`
 - Checks: `ensure_db_connection and server_only`
# +unhex
Unhex a string<br/>
 - Usage: `+unhex <text>`
 - Restricted to: `MOD`
 - Checks: `server_only and ensure_db_connection`
# +arkset
ArkTools configuration<br/>
 - Usage: `+arkset`
 - Restricted to: `ADMIN`
 - Aliases: `arktools`
## +arkset initroles
Initialize playtime roles<br/>
 - Usage: `+arkset initroles`
 - Cooldown: `1 per 900.0 seconds`
## +arkset viewranks
View playtime roles<br/>
 - Usage: `+arkset viewranks`
## +arkset countdown
Set the `doexit` and `dorestartlevel` countdowns<br/>
 - Usage: `+arkset countdown <seconds>`
## +arkset autowelcomemessage
Set the welcome message sent when a new player is found<br/>

Placeholders<br/>
- `{username}` - Player's username<br/>
- `{gameid}` - Player's game ID<br/>
 - Usage: `+arkset autowelcomemessage [message]`
 - Aliases: `welcomemsg`
## +arkset uncryolimit
Set how many uncryoed tames a tribe can have.<br/>

    Put 0 to disable the limit entirely.<br/>

Arguments:<br/>
`limit` - Maximum number of active tames allowed.<br/>
`cluster_name` - Cluster to apply the rule to.<br/>

    Examples:<br/>
    - +arkset uncryolimit 200 main<br/>
    - +arkset uncryolimit 0 pve<br/>
 - Usage: `+arkset uncryolimit <limit> <cluster_name>`
## +arkset characternameblacklist
Character name blacklist<br/>
 - Usage: `+arkset characternameblacklist <name>`
 - Aliases: `charnameblacklist, charbl, and badname`
## +arkset tempbandefault
Set the default tempban duration<br/>

Example: 1h30m<br/>
 - Usage: `+arkset tempbandefault <duration>`
 - Restricted to: `GUILD_OWNER`
## +arkset wipeclustertribes
Reset all player tribes for a cluster<br/>
 - Usage: `+arkset wipeclustertribes <cluster_name>`
## +arkset linkrole
Add a playtime role<br/>
 - Usage: `+arkset linkrole <hours> <role>`
## +arkset registerrole
Set the role required to register<br/>
 - Usage: `+arkset registerrole [role]`
## +arkset regenkey
Generate a fresh ArkView API key.<br/>

This replaces the existing key immediately, so update any integrations that use it.<br/>

Examples:<br/>
- +arkset regenkey<br/>
 - Usage: `+arkset regenkey`
 - Restricted to: `GUILD_OWNER`
## +arkset refundserverdelta
Refund purchases for a specific server within a time window.<br/>

    Use `YYYY-MM-DDTHH:MM:SS` for both timestamps.<br/>

Arguments:<br/>
`start_time` - Oldest timestamp to refund from.<br/>
`end_time` - Newest timestamp to refund through.<br/>
`server_name` - Server name within the cluster.<br/>
`cluster_name` - Cluster the server belongs to.<br/>

    Examples:<br/>
    - +arkset refundserverdelta 2024-04-03T20:00:00 2024-05-05T18:00:00 volcanic pvp<br/>
 - Usage: `+arkset refundserverdelta <start_time> <end_time> <server_name> <cluster_name>`
## +arkset ingame
Configure in-game settings<br/>
 - Usage: `+arkset ingame`
### +arkset ingame paydaycooldown
Set cooldown seconds for paydays<br/>
 - Usage: `+arkset ingame paydaycooldown <seconds> <cluster_name>`
### +arkset ingame payday
Toggle payday rewards for a cluster<br/>
 - Usage: `+arkset ingame payday <cluster_name>`
### +arkset ingame paydayrandom
Toggle randomization of payday rewards<br/>
 - Usage: `+arkset ingame paydayrandom <cluster_name>`
 - Aliases: `randompayday`
### +arkset ingame setpaydaypaths
Upload the blueprint paths used for payday rewards.<br/>

Attach a `.txt` file with one line per path using `path quantity quality blueprint` format.<br/>

Arguments:<br/>
`cluster_name` - Cluster whose payday rewards you're updating.<br/>

Examples:<br/>
- +ingame setpaydaypaths main (with payday_paths.txt attached)<br/>
 - Usage: `+arkset ingame setpaydaypaths <cluster_name>`
 - Restricted to: `ADMIN`
### +arkset ingame kit
Toggle new player kit claiming for a cluster<br/>
 - Usage: `+arkset ingame kit <cluster_name>`
### +arkset ingame getkitpaths
Get the current kit paths for a cluster<br/>
 - Usage: `+arkset ingame getkitpaths <cluster_name>`
 - Restricted to: `ADMIN`
### +arkset ingame setkitpaths
Upload kit blueprint paths for a cluster.<br/>

Attach a `.txt` file with one entry per line in the format `path quantity quality blueprint`.<br/>

Arguments:<br/>
`cluster_name` - Cluster whose kit paths you're updating.<br/>

Examples:<br/>
- +ingame setkitpaths main (with kit_paths.txt attached)<br/>
 - Usage: `+arkset ingame setkitpaths <cluster_name>`
 - Restricted to: `ADMIN`
### +arkset ingame imstuck
Enable or disable the /imstuck rescue command for a cluster.<br/>

Arguments:<br/>
`cluster_name` - Cluster to toggle.<br/>

Examples:<br/>
- +ingame imstuck main<br/>
 - Usage: `+arkset ingame imstuck <cluster_name>`
### +arkset ingame setimstuckpaths
Upload the teleport paths used for /imstuck.<br/>

Attach a `.txt` file with one line per path using `path quantity quality blueprint` format.<br/>

Arguments:<br/>
`cluster_name` - Cluster whose teleport paths you're updating.<br/>

Examples:<br/>
- +ingame setimstuckpaths main (with imstuck_paths.txt attached)<br/>
 - Usage: `+arkset ingame setimstuckpaths <cluster_name>`
 - Restricted to: `ADMIN`
### +arkset ingame getimstuckpaths
Get the current imstuck paths for a cluster<br/>
 - Usage: `+arkset ingame getimstuckpaths <cluster_name>`
 - Restricted to: `ADMIN`
### +arkset ingame getpaydaypaths
Get the current payday paths for a cluster<br/>
 - Usage: `+arkset ingame getpaydaypaths <cluster_name>`
 - Restricted to: `ADMIN`
### +arkset ingame imstuckcooldown
Change the cooldown for the /imstuck rescue command.<br/>

Arguments:<br/>
`seconds` - How many seconds users must wait between uses.<br/>
`cluster_name` - Cluster to apply the cooldown to.<br/>

Examples:<br/>
- +ingame imstuckcooldown 900 main<br/>
 - Usage: `+arkset ingame imstuckcooldown <seconds> <cluster_name>`
## +arkset wipeclusterstats
Reset all player stats like kills/tames/deaths for a cluster<br/>
 - Usage: `+arkset wipeclusterstats <cluster_name>`
## +arkset timezone
Set your server's timezone<br/>
 - Usage: `+arkset timezone <timezone>`
## +arkset recentlycreated
List players created after a specific date.<br/>

    Use the ISO format `YYYY-MM-DDTHH:MM:SS` so we know where to start.<br/>

Arguments:<br/>
`created_after` - ISO timestamp marking the oldest creation time to include.<br/>

    Examples:<br/>
    - +arkset recentlycreated 2024-04-03T20:00:00<br/>
 - Usage: `+arkset recentlycreated <created_after>`
 - Aliases: `rc`
## +arkset toggleshopcluster
Disable the shop for a specific cluster<br/>
 - Usage: `+arkset toggleshopcluster <cluster_name>`
## +arkset modcommands
Mod command allow list<br/>
 - Usage: `+arkset modcommands <command>`
 - Aliases: `modcmd`
## +arkset autoremoverole
Toggle auto-removal of previous playtime role<br/>
 - Usage: `+arkset autoremoverole`
## +arkset toggleshop
Toggle the shop on/off<br/>
 - Usage: `+arkset toggleshop`
## +arkset shoplog
Set the shop log channel<br/>

All purchases will be logged here<br/>
 - Usage: `+arkset shoplog <channel>`
## +arkset banimposters
Protect your server if anyone discovers your admin password<br/>
 - Usage: `+arkset banimposters`
## +arkset alertchannel
Set a channel to receive alerts<br/>

The following alerts are sent here:<br/>
- Server goes down<br/>
- Unauthorized admin command in-game<br/>
- Tribe auto-banned for foreign tames<br/>

**These events will fall back to the event log if no alert channel is set**<br/>
 - Usage: `+arkset alertchannel <channel>`
## +arkset commandblacklist
Set forbidden commands<br/>
 - Usage: `+arkset commandblacklist <command>`
## +arkset usedisplaynames
Toggle whether discord->ark messages use display names<br/>

If Enabled, messages sent to Ark will use the user's nickname or username instead of their username<br/>
 - Usage: `+arkset usedisplaynames`
## +arkset refundclusterdelta
Refund shop purchases for a cluster within a time window.<br/>

    Provide the start and end timestamps using `YYYY-MM-DDTHH:MM:SS`.<br/>

Arguments:<br/>
`start_time` - Oldest timestamp to refund from.<br/>
`end_time` - Newest timestamp to refund through.<br/>
`cluster_name` - Cluster whose purchases you want to reverse.<br/>

    Examples:<br/>
    - +arkset refundclusterdelta 2024-04-03T20:00:00 2024-05-05T18:00:00 pvp<br/>
 - Usage: `+arkset refundclusterdelta <start_time> <end_time> <cluster_name>`
## +arkset view
View ark settings<br/>
 - Usage: `+arkset view`
 - Restricted to: `MOD`
## +arkset eventlog
Set the event log<br/>

The logs include the following events:<br/>
- New players that are added to the database<br/>
- Welcome messages sent to new players(if enabled)<br/>
- Old players that are unfriended for inactivity(if enabled)<br/>
- Players that are unfriended for leaving the Discord(if enabled)<br/>
- Players that are unfriended due to unfriending a host Gamertag<br/>
 - Usage: `+arkset eventlog <channel>`
## +arkset wipeclusterimplants
Reset all player's set specimen numbers for a cluster<br/>
 - Usage: `+arkset wipeclusterimplants <cluster_name>`
## +arkset ucstats
View Upgrade.Chat purchases by cluster<br/>
 - Usage: `+arkset ucstats`
 - Restricted to: `GUILD_OWNER`
## +arkset retention
Set the days worth of playercount data to keep<br/>
 - Usage: `+arkset retention <days>`
## +arkset clustertype
Set the type of ark servers you host<br/>

Valid arguments are `xbox, steam, both`<br/>
 - Usage: `+arkset clustertype <cluster_type>`
## +arkset autowelcome
Toggle auto welcoming of new players discovered in-game<br/>

This is just a broadcast in the server, not a DM<br/>
 - Usage: `+arkset autowelcome`
## +arkset imposterwhitelist
Whitelist certain game IDs from triggering imposter bans<br/>
 - Usage: `+arkset imposterwhitelist <player_id>`
## +arkset unlinkrole
Remove a playtime role<br/>
 - Usage: `+arkset unlinkrole <hours>`
## +arkset killfeed
Toggle the killfeed<br/>

The killfeed shows player kills in the map chats in a silly way, it will also shame bob killers publicly<br/>
 - Usage: `+arkset killfeed`
# +lootbox
Open a lootbox<br/>
 - Usage: `+lootbox`
 - Aliases: `lootcrate`
 - Checks: `server_only`
# +lootboxset
Setup the lootbox system<br/>
 - Usage: `+lootboxset`
 - Restricted to: `ADMIN`
 - Aliases: `lbs`
## +lootboxset simulate
Simulate opening a lootbox X times and generate a summary of selections.<br/>
 - Usage: `+lootboxset simulate [times=100]`
 - Aliases: `sim`
## +lootboxset logchannel
Set the lootbox log channel<br/>
 - Usage: `+lootboxset logchannel <channel>`
## +lootboxset price
Set the price of a lootbox<br/>

0 Will make the loot box free<br/>
 - Usage: `+lootboxset price <price>`
## +lootboxset upload
Set the lootbox items<br/>
 - Usage: `+lootboxset upload`
## +lootboxset add
Quickly add an item to the lootbox system<br/>
 - Usage: `+lootboxset add <chance> <quality> <quantity> <blueprint> <stacksize> <path> <name> [cluster_blacklist]`
## +lootboxset cooldown
Set the lootbox cooldown<br/>
 - Usage: `+lootboxset cooldown <cooldown>`
## +lootboxset download
Get the current lootboxes as an Excel file<br/>
 - Usage: `+lootboxset download`
## +lootboxset view
View general lootbox settings<br/>
 - Usage: `+lootboxset view`
## +lootboxset template
Get an example Excel file for the lootbox system<br/>
 - Usage: `+lootboxset template`
# +arkviewer
Quickly view your servers' ArkView metrics<br/>
 - Usage: `+arkviewer`
 - Aliases: `arkview and lastsynced`
 - Cooldown: `1 per 10.0 seconds`
 - Checks: `server_only`
# +playerheat
Get a heatmap of player locations<br/>
 - Usage: `+playerheat`
 - Cooldown: `1 per 5.0 seconds`
 - Checks: `server_only`
# +hunt (Hybrid Command)
Hunt for a dino!<br/>

Use the slash version of this command to make it private!<br/>
 - Usage: `+hunt <dino>`
 - Slash Usage: `/hunt <dino>`
 - Cooldown: `1 per 3.0 seconds`
 - Checks: `server_only`
# +mytames
Check your tribe's tames on a map<br/>
 - Usage: `+mytames`
 - Cooldown: `1 per 20.0 seconds`
 - Checks: `server_only`
# +tamesfor
Check your tribe's tames on a map<br/>
 - Usage: `+tamesfor <player>`
 - Restricted to: `MOD`
 - Cooldown: `1 per 20.0 seconds`
 - Checks: `server_only`
# +findtame (Hybrid Command)
Find tames by tame name, imprinter, tamer, or tribe name<br/>

`search_query` can be one of the following.<br/>
The dino's name.<br/>
The name of the person who tamed the dino.<br/>
The name of the person who imprinted on the tame.<br/>
The name of the tribe that owns the dino.<br/>
The ID of the tribe that tamed the dino.<br/>

*You can search for unclaimed dinos by specifying `unclaimed`*<br/>
 - Usage: `+findtame <search_query>`
 - Slash Usage: `/findtame <search_query>`
 - Cooldown: `1 per 5.0 seconds`
 - Checks: `server_only`
# +mapstats
Get detailed stats for a map<br/>
 - Usage: `+mapstats`
 - Cooldown: `1 per 5.0 seconds`
 - Checks: `server_only`
# +creaturepie
Get a pie chart of wild dinos on a map<br/>
 - Usage: `+creaturepie [count=10]`
 - Cooldown: `1 per 5.0 seconds`
 - Checks: `server_only`
# +structurepie
Get pie chart of structures<br/>
 - Usage: `+structurepie [count=10]`
 - Cooldown: `1 per 5.0 seconds`
 - Checks: `server_only`
# +tamepie
Get a pie chart of tamed dinos on a map<br/>
 - Usage: `+tamepie [count=10]`
 - Cooldown: `1 per 5.0 seconds`
 - Checks: `server_only`
# +avsync
Sync tribes, players and characters with with the database<br/>
 - Usage: `+avsync`
 - Restricted to: `ADMIN`
 - Cooldown: `1 per 600.0 seconds`
 - Checks: `server_only`
# +servermetrics
View current server memory usage<br/>
 - Usage: `+servermetrics <metric>`
 - Restricted to: `ADMIN`
 - Cooldown: `1 per 3.0 seconds`
 - Checks: `server_only`
# +getips
Get a list of player IPs from the database<br/>
 - Usage: `+getips`
 - Restricted to: `ADMIN`
 - Cooldown: `1 per 3.0 seconds`
 - Checks: `server_only`
# +viewsysinfo
View data about the system running your servers<br/>
 - Usage: `+viewsysinfo`
 - Restricted to: `ADMIN`
 - Cooldown: `1 per 60.0 seconds`
 - Checks: `server_only`
# +datadump
Get a json dump of the specified data type from ArkView<br/>
 - Usage: `+datadump <datatype>`
 - Restricted to: `ADMIN`
 - Checks: `server_only`
# +clearcustomdinos
Clear all custom dinos for this server<br/>
 - Usage: `+clearcustomdinos`
 - Restricted to: `ADMIN`
 - Checks: `server_only`
# +setcustomdinos
Register custom dinos for features like hunt and findtame.<br/>

            Paste entries directly or attach a `.txt` file. Each line should be `FriendlyName|ClassName`.<br/>

        Arguments:<br/>
        `custom_dinos` - Optional pasted list of entries. Attach a file instead if you leave this blank.<br/>

            Examples:<br/>
            - +setcustomdinos Royal Griffin|RoyalOwlGriffin_MM_Character_BP_C<br/>
Gecko|Gecko_Character_BP_C<br/>
            - +setcustomdinos (with custom_dinos.txt attached)<br/>
        <br/>
 - Usage: `+setcustomdinos [custom_dinos]`
 - Restricted to: `ADMIN`
 - Checks: `server_only`
# +showcustomdinos
Show the list of custom dinos for this server<br/>
 - Usage: `+showcustomdinos`
 - Restricted to: `ADMIN`
 - Aliases: `listcustomdinos and getcustomdinos`
 - Checks: `server_only`
# +setvalidservers
Comma separated list of valid server names for this server, any servers not in this list will be flagged when a tame is transferred to them<br/>
 - Usage: `+setvalidservers <valid_names>`
 - Restricted to: `ADMIN`
 - Checks: `server_only`
# +showvalidservers
Show the list of valid server names for this server<br/>
 - Usage: `+showvalidservers`
 - Restricted to: `ADMIN`
 - Checks: `server_only`
# +scanforeigntames
Scan all servers for tames that are from a server not in the valid server list<br/>
 - Usage: `+scanforeigntames`
 - Restricted to: `ADMIN`
 - Checks: `server_only`
# +checkmassbreed
Find clusters of dinos left breeding.<br/>

    Explanation:<br/>
    Spots dense groups of dinos with mating enabled so you can deal with mass breeders before they lag the map.<br/>

Arguments:<br/>
`threshold` - Maximum distance (lat/lon) between dinos in a cluster. Default 0.5.<br/>
`min_dinos` - Minimum mating dinos in the area before it flags the cluster. Default 6.<br/>
 - Usage: `+checkmassbreed [threshold=0.5] [min_dinos=6]`
 - Restricted to: `ADMIN`
 - Aliases: `massbreed`
 - Checks: `server_only`
# +findplayer (Hybrid Command)
Find the location and tribe of a player in-game<br/>

`search_query` can be one of the following.<br/>
Player's in-game name<br/>
Gamertag or Username<br/>
Specimen number (exact matches only)<br/>
XUID or SteamID (exact matches only)<br/>
Tribe ID (exact matches only)<br/>
 - Usage: `+findplayer <search_query>`
 - Slash Usage: `/findplayer <search_query>`
 - Restricted to: `ADMIN`
 - Checks: `server_only`
# +findtribe
Find details of a tribe<br/>

`search_query` can be one of the following.<br/>
- Tribe name<br/>
- Tribe ID (exact matches only)<br/>
- Player's in-game name<br/>
- Gamertag or Username<br/>
- Specimen number (exact matches only)<br/>
- XUID or SteamID (exact matches only)<br/>

If any tribes have the player info found in them, they will be shown<br/>
 - Usage: `+findtribe <search_query>`
 - Restricted to: `MOD`
 - Checks: `server_only`
# +warntribe
Warn all members of a tribe at once<br/>
 - Usage: `+warntribe <tribe_id> <warning>`
 - Restricted to: `ADMIN`
 - Checks: `server_only`
# +structures (Hybrid Command)
Get a marker map of structures for a tribe<br/>

`search_query` can be one of the following.<br/>
- Tribe name<br/>
- Tribe ID (exact matches only)<br/>
 - Usage: `+structures <search_query>`
 - Slash Usage: `/structures <search_query>`
 - Restricted to: `ADMIN`
 - Checks: `server_only`
# +findstructure (Hybrid Command)
Get a marker map of specific structures for a tribe or the whole map<br/>

`structure_class` is the class name of the structure you want to search for.<br/>
- e.g. "CookingPot_C" or "StructureTurretTek_C<br/>

`search_query` can be one of the following.<br/>
- Tribe name<br/>
- Tribe ID (exact matches only)<br/>
 - Usage: `+findstructure <structure_class> [search_query=None]`
 - Slash Usage: `/findstructure <structure_class> [search_query=None]`
 - Restricted to: `ADMIN`
 - Checks: `server_only`
# +structuregraph
Visualize controlled areas of a server by tribe.<br/>
 - Usage: `+structuregraph`
 - Restricted to: `ADMIN`
 - Cooldown: `1 per 45.0 seconds`
 - Checks: `server_only`
# +territory
Visualize controlled areas of a server by tribe.<br/>
 - Usage: `+territory [include_other=False] [top=10]`
 - Restricted to: `ADMIN`
 - Cooldown: `1 per 5.0 seconds`
 - Checks: `server_only`
# +findexpired
Get a list of tribes that haven't been active for more than X days<br/>

Example: +findexpired 60<br/>
this will show tribes inactive for 60 days or more that have at least 1 structure or tame<br/>
 - Usage: `+findexpired <days>`
 - Restricted to: `MOD`
 - Aliases: `expired`
 - Checks: `server_only`
# +wipetribes
Wipe all tribes that haven't been active for X days or more<br/>

This will delete all their tames, structures, and players<br/>
 - Usage: `+wipetribes <days>`
 - Restricted to: `ADMIN`
 - Checks: `server_only`
# +sortdinos
Find all dinos above or equal to the specified level<br/>
 - Usage: `+sortdinos <level> [dino_name]`
 - Restricted to: `ADMIN`
 - Checks: `server_only`
# +tribesize
Visualize a tribe's controlled territory along with their types of structures and area they take up.<br/>
 - Usage: `+tribesize <search_query>`
 - Restricted to: `ADMIN`
 - Checks: `server_only`
# +finditem
Search for a specific item on a map<br/>
 - Usage: `+finditem <item_blueprint> [tribe_id=None]`
 - Restricted to: `MOD`
 - Checks: `server_only`
# +itemsearch
Find information about an item across all maps<br/>
 - Usage: `+itemsearch <item_blueprint> [tribe_id=None] [clustername=all] [servername=all]`
 - Restricted to: `ADMIN`
 - Checks: `server_only`
# +tamestatcheck
Find tames that hit a stat goal.<br/>

Arguments:<br/>
`stat` - Which stat to check: hp, stam, melee, weight, speed, food, or oxy.<br/>
`points` - Minimum number of points the tame needs in that stat.<br/>
`stat_type` - Choose tamed or wild points. Defaults to tamed.<br/>
 - Usage: `+tamestatcheck <stat> <points> [stat_type=tamed]`
 - Restricted to: `ADMIN`
 - Checks: `server_only`
# +uncryocheck
Get a list of tribes who's uncryo'd tame count is above the specified amount<br/>
 - Usage: `+uncryocheck <amount>`
 - Restricted to: `ADMIN`
 - Aliases: `cryocheck`
 - Checks: `server_only`
# +syncbans
Sync the banlists for all servers<br/>
 - Usage: `+syncbans`
 - Restricted to: `ADMIN`
 - Checks: `server_only`
## +syncbans all
Sync every ban across every server.<br/>

    Explanation:<br/>
    Runs as a dry run by default and shows what would change. Confirm true re-bans missing entries, removes stray bans, and cleans invalid IDs.<br/>

Arguments:<br/>
`confirm` - true to apply the changes instead of previewing them.<br/>
 - Usage: `+syncbans all [confirm=False]`
 - Cooldown: `1 per 600.0 seconds`
 - Checks: `bot_has_server_permissions`
## +syncbans betweenservers
Mirror bans between every server.<br/>

    Explanation:<br/>
    Keeps ASA maps in sync with each other, keeps ASE maps in sync, updates the database, and removes invalid IDs. Dry run first, then confirm to commit.<br/>

Arguments:<br/>
`confirm` - true to apply the changes instead of previewing them.<br/>
 - Usage: `+syncbans betweenservers [confirm=False]`
 - Cooldown: `1 per 300.0 seconds`
## +syncbans fromdb
Push bans from the database to every server.<br/>

    Explanation:<br/>
    Re-bans players missing on servers, removes bans that only exist on servers, and can run as a dry run before confirming.<br/>

Arguments:<br/>
`confirm` - true to make the changes. Leave false for a dry run.<br/>
 - Usage: `+syncbans fromdb [confirm=False]`
 - Cooldown: `1 per 300.0 seconds`
## +syncbans fromserver
Copy bans from the servers into the database.<br/>

    Explanation:<br/>
    Treats each server as the source of truth, cleans invalid IDs, and adds missing database entries. Run without confirm to preview.<br/>

Arguments:<br/>
`confirm` - true to make the changes instead of running a dry run.<br/>
 - Usage: `+syncbans fromserver [confirm=False]`
 - Cooldown: `1 per 300.0 seconds`
# +servergraph (Hybrid Command)
See how your player count changed over time.<br/>

Arguments:<br/>
`timespan` - How far back to check. Use values like 4h, 12d, 3w2d, or all. Defaults to 1 hour.<br/>
`clusters_only` - true to merge maps by cluster instead of showing every map.<br/>
`include_total` - true to add a line that shows the combined player count.<br/>
`search_query` - Filter to specific clusters or maps.<br/>
`start_time` - Override the start time, e.g. April 10 2032 5:00pm.<br/>
`end_time` - Optional end time that pairs with start_time.<br/>

    Examples:<br/>
    +servergraph 4h<br/>
    +servergraph 12d<br/>
    +servergraph 3w2d<br/>
    +servergraph 7w<br/>
 - Usage: `+servergraph [timespan=None] [clusters_only=False] [include_total=False] [search_query=] [start_time=None] [end_time=None]`
 - Slash Usage: `/servergraph [timespan=None] [clusters_only=False] [include_total=False] [search_query=] [start_time=None] [end_time=None]`
 - Cooldown: `3 per 30.0 seconds`
 - Checks: `server_only`
# +lookback
Find where a player was online during a specific window.<br/>

Arguments:<br/>
`search_query` - Player name, game ID, or Discord member to look up.<br/>
`start_time` - When to start looking, e.g. April 10 2032 5:00pm.<br/>
`end_time` - Optional time to stop looking, e.g. April 11 2032 5:00pm.<br/>
 - Usage: `+lookback <search_query> <start_time> [end_time=None]`
 - Restricted to: `MOD`
 - Cooldown: `5 per 30.0 seconds`
 - Checks: `server_only`
# +whowason
List everyone who was online at a specific moment.<br/>

Arguments:<br/>
`time` - When to check. Accepts ISO times like 2024-10-15T12:00:00 or natural times such as 4:20pm April 10 2024.<br/>
 - Usage: `+whowason <time>`
 - Restricted to: `MOD`
 - Checks: `server_only`
# +timeline
Show a player's join and leave timeline.<br/>

Arguments:<br/>
`search_query` - Player name, game ID, or Discord member to inspect.<br/>
`start_time` - When to start the timeline, e.g. April 10 2032 5:00pm.<br/>
`end_time` - Optional time to stop the timeline.<br/>
 - Usage: `+timeline <search_query> <start_time> [end_time=None]`
 - Restricted to: `MOD`
 - Checks: `server_only`
