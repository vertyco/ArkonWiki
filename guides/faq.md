---
title: FAQ & Troubleshooting - Arkon Ark Discord Bot
description: Fix common Arkon problems for your Ark Discord server: RCON connection errors, registration, shop, tribe logs, status channel, ArkView, Xbox and permissions.
published: true
date: 2026-10-12T00:00:00.000Z
tags: faq, troubleshooting, help, support
editor: markdown
dateCreated: 2026-01-17T00:00:00.000Z
---

# FAQ and Troubleshooting

Something not working? Find your problem below, read the cause, and do the fix. Each answer links to the full guide if you need more detail.

Quick tip: the exact message Arkon showed you is the best clue. Search this page (Ctrl+F) for a piece of it.

## Jump to a topic

- [General questions](#general-questions)
- [Connection (RCON)](#connection-rcon)
- [Setup and servers](#setup-and-servers)
- [Permissions](#permissions)
- [Registration](#registration)
- [Shop and lootboxes](#shop-and-lootboxes)
- [In-game commands](#in-game-commands)
- [Tribe logs](#tribe-logs)
- [Chat and logs](#chat-and-logs)
- [Status channel](#status-channel)
- [Playtime roles](#playtime-roles)
- [Moderation and security](#moderation-and-security)
- [Server control](#server-control)
- [ArkView and map tools](#arkview-and-map-tools)
- [Xbox](#xbox)
- [Premium and limits](#premium-and-limits)
- [Still need help](#still-need-help)

## General questions

### What is Arkon?

Arkon is a Discord bot that helps you run Ark: Survival Evolved (ASE) and Ark: Survival Ascended (ASA) servers. It connects your game server to Discord. See the [home page](/) for the full feature list.

### Which games and hosts work?

- ASA works on all platforms.
- ASE works on self-hosted servers and most hosts.
- ASE on Nitrado does not work, because Nitrado blocks RCON (the remote-control connection Arkon uses) on ASE. Nitrado ASA works. See [RCON Setup](/guides/rcon-setup).

### Is Arkon free?

Yes. Free covers the basics for a small number of servers. [Premium](/guides/premium) removes limits and unlocks a few extra tools.

### What is the prefix?

The default prefix is `+`, so a command looks like `+viewservers`. Many commands also work as slash commands, for example `/setup`.

### Where do I start?

Follow [Getting Started](/guides/getting-started). Players should read [Player Getting Started](/guides/player-getting-started).

## Connection (RCON)

RCON is the remote-control connection Arkon uses to talk to your game server. Most "it will not connect" problems are here. The full walkthrough is in [RCON Setup](/guides/rcon-setup).

### "Wrong password!"

The admin password does not match. It is case-sensitive.
**Fix:** copy `ServerAdminPassword` again with no extra spaces. Do not use the join password. If you just changed it, save and restart the server first (G-Portal especially).

### "Connection timed out" or "No response!"

Arkon cannot reach your RCON port. The cause is a wrong IP or port, a port that is not forwarded, a firewall, a server that is off, or RCON turned off.
**Fix:** check each item in [RCON Setup](/guides/rcon-setup). Test the port at [canyouseeme.org](https://canyouseeme.org). Use the RCON port, not the game or query port.

### "Connection refused"

Wrong port, RCON disabled, or the server is still loading.
**Fix:** wait for the server to finish starting. Check `RCONEnabled=True`. Read `RCONPort=` in your config or panel instead of guessing from the game port.

### "No response from server"

The server gave an empty reply. It is still starting, or the port is not an RCON port.
**Fix:** wait a minute and retry. Use the RCON port.

### It works inside my home but not from Arkon

You used a `192.168.x.x` or `10.x.x.x` address. Those only work inside your home network.
**Fix:** use your public IP from [whatismyip.com](https://whatismyip.com).

### It worked yesterday, now it times out

Your home IP probably changed.
**Fix:** enter the new IP, or use a DDNS name (a free name that follows your changing IP, such as DuckDNS). See [RCON Setup](/guides/rcon-setup).

### I cannot forward ports at all

Your provider may use CGNAT (they share one public IP between many customers).
**Fix:** ask your provider for a public IP.

### Server shows Offline but it is running

Arkon cannot reach it over RCON.
**Fix:** fix RCON using [RCON Setup](/guides/rcon-setup). Also check that your public IP did not change.

### The +rconhelp dropdown does nothing

It expires after 10 minutes.
**Fix:** type `+rconhelp` again. The dropdown lists Nitrado, G-Portal, Shockbyte, Host Havoc, Self-Hosted and Other. The same dropdown also appears under the "Failed to connect" message. See [Getting Started](/guides/getting-started).

## Setup and servers

### "A cluster with the name `MyCluster` doesn't exist!"

Cluster names are saved in lowercase.
**Fix:** type it lowercase, for example `+addserver mycluster`. See [Server Settings](/guides/server-settings).

### "Cluster names can only contain letters and numbers!"

The name has a dash, underscore or symbol.
**Fix:** use only letters and numbers.

### "You must create a cluster before you can add servers to it."

You have no clusters yet.
**Fix:** run `+addcluster mycluster`.

### "That's an address inside your home network..."

You typed a private address in the setup wizard.
**Fix:** use your public IP. See [Getting Started](/guides/getting-started).

### "Invalid host address. Please enter a valid IPv4 address or hostname."

You typed the port together with the IP, like `203.0.113.25:27020`.
**Fix:** put the IP in Host IP and the port in RCON Port.

### "Port must be a number between 1 and 65535."

**Fix:** enter digits only, for example `27020`.

### "Duplicate Server Detected"

That server is already added.
**Fix:** press **Edit Details** to change what you typed, or **Cancel Setup**. Use `+viewservers` to see what you already have. See [RCON Setup](/guides/rcon-setup).

### "Setup Timed Out"

The setup wizard waits 10 minutes for you.
**Fix:** run the setup again.

### The connection failed and the wizard shows buttons

**Fix:** press **Edit & Retry** to fix your details, **Troubleshooting Guide** for the five-step check, or **Get Help**. See [RCON Setup](/guides/rcon-setup).

### "That chat channel is already in use by another server!"

Each map needs its own chat channel.
**Fix:** pick a different channel.

### "This isn't your menu!" or "This setup wizard isn't for you!"

Only the person who ran the command can press its buttons.
**Fix:** run the command yourself.

### "Database connection is not active", "Database is currently migrating" or "Initializing database, One moment..."

Arkon's database is starting or updating.
**Fix:** wait a minute and try again.

### A server turned itself off

It was offline for 30 days, had a bad host or port, or you went over the free limit.
**Fix:** fix the cause, then press **Disabled** on its server page in `+viewservers` to enable it. See [Server Settings](/guides/server-settings).

### `/setup` is not in the command list

You lack Manage Server, or slash commands are not showing yet.
**Fix:** ask someone with Manage Server, or use the manual path in [Getting Started](/guides/getting-started).

## Permissions

### Arkon does not answer commands

1. Arkon needs **Send Messages** and **Embed Links** in that channel. Fix the channel permissions.
2. Check you are using the right prefix (default `+`).
3. Check you have the Admin or Mod role the command needs. See [Getting Started](/guides/getting-started).
4. Try another channel.

### No message from a lookup command

Arkon lacks **Embed Links**. Give it that permission.

### "That role is higher than my highest role, so I cannot assign it!"

Arkon's role sits below the role it should give.
**Fix:** in Server Settings, then Roles, drag Arkon's role higher.

### "I do not have permissions to manage roles!"

**Fix:** give Arkon the **Manage Roles** permission.

### Arkon cannot send a .txt or file

**Fix:** give Arkon **Attach Files** in that channel.

### "You must have one of the following roles to claim private tribelogs!"

**Fix:** ask an admin for the role, or add it with `+tribeset claimrole`. See [Tribe Logs](/guides/tribe-logs).

### Discord says I lack permission for `+arkset regenkey` or `+arkset tempbandefault`

These need the Server owner.
**Fix:** ask the owner of the Discord server to run them.

## Registration

Registration links a player's Discord account to their in-game character. Full guide: [Player Registration](/guides/player-registration).

### `+register` does nothing in game

Type it in Ark **global chat**, followed by your Discord name, for example `+register SurvivorSam`. Make sure in-game commands are set up. See [In-Game Commands](/guides/in-game-commands).

### "You are already registered as ..."

**Fix:** type `+unregisterme`, then `+register` again.

### "When registering from Discord, you must use your Username, Not your ID!"

**Fix:** type your name, not numbers.

### "This server does not have any clusters configured yet." or "...any active Ark servers configured yet."

**Fix (admin):** add a cluster and enable a server. See [Server Settings](/guides/server-settings).

### "... has already claimed this Gamertag"

Another Discord member still in your server holds that name.
**Fix:** that member, or a Mod using `+unregisterplayer`, unlinks it first.

### "I could not find that Gamertag!"

**Fix:** check spelling and leave out the `#`.

### "No player found with that EOS ID."

Arkon has not seen you on an ASA server yet.
**Fix:** join an ASA server once, then try again. An EOS ID has letters and numbers, like `0002c7cde9d24e1994d9cf87096e32f8`.

### "Specimen number must be 5 to 9 digits long!"

**Fix:** copy it from the top left of your in-game inventory.

### "You have not played on ... with this account!" or "I don't have you saved in the database for this server!"

Arkon has no record of you on that map.
**Fix:** play on that map, then run `+register`.

### Registration roles do not appear

Arkon's role is below the role it should give.
**Fix:** move Arkon's role above the register and playtime roles.

## Shop and lootboxes

Guides: [RCON Shop](/guides/rshop) and [Lootboxes](/guides/lootboxes).

### "There is nothing in the shop yet!"

No item has a price above 0, or none match the player's game version or cluster.
**Fix:** set prices and upload again. Check Server Type and the blacklist.

### "The shop is not enabled in this server!"

**Fix:** run `+arkset toggleshop`.

### "The shop is currently **disabled** for the cluster you're on!"

**Fix:** run `+arkset toggleshopcluster <cluster>` again.

### "You have not registered your profile yet!"

**Fix:** the player runs `+register`.

### "I could not find you on any of the servers..." or "I can't find you on any of the servers!"

The player is not online right now.
**Fix:** join the game, wait a minute or two, and retry.

### "You have not set your specimen number for {map} yet!!!" or "You do not have an implant set..."

**Fix:** the player runs `+specimen`.

### "You don't have enough ..." (followed by your shop currency name)

The player's balance is lower than the cart total.
**Fix:** earn more currency, or lower the price.

### "The server password is incorrect! Staff have been notified."

The RCON password saved in Arkon is wrong.
**Fix:** correct it in [Server Settings](/guides/server-settings). This failure does not refund automatically.

### "The server is not responding, staff have been notified."

The server is offline or RCON is blocked.
**Fix:** see [RCON Setup](/guides/rcon-setup). The player is refunded when refunds apply.

### "You are trying to purchase too many items at once!"

The purchase needs more than 100 stacks.
**Fix:** buy less, or fix stack sizes with `+rshopset readstacks`.

### "There were errors while parsing your file"

**Fix:** open `errors.txt` and fix those rows.

### "You must attach your excel file to this command!"

**Fix:** attach the `.xlsx` to the same message.

### "Could not find an item with that name!"

**Fix:** use the menu, or type the exact name.

### Lootbox: "No lootboxes have been set up!"

The prize list is empty. Do the setup steps in [Lootboxes](/guides/lootboxes).

### Lootbox: "Lootboxes are disabled for the **My Cluster** cluster."

**Fix:** `+lootboxset toggle My Cluster`.

### Lootbox: "The lootbox sheet must have 8 or 9 columns!"

**Fix:** start again from `+lootboxset download`.

### Lootbox: "There are no servers available!"

No enabled server could be found for the player.
**Fix:** enable a server and make sure the player is online. See [Lootboxes](/guides/lootboxes).

### Lootbox: "Failed to select a lootbox!"

**Fix:** try again. If it keeps happening, check the prize list in [Lootboxes](/guides/lootboxes).

### Lootbox: "No valid lootboxes found in the file!" or "Invalid blueprint path format (column 3)"

**Fix:** start again from `+lootboxset download` and fix the blueprint path column.

### Lootbox: "Failed to parse lootbox file"

**Fix:** rename the sheet to `lootboxes` and save as `.xlsx`.

### Lootbox: "Something went wrong while trying to send your lootbox items!"

RCON failed. Nothing was charged.
**Fix:** check [RCON Setup](/guides/rcon-setup).

## In-game commands

Guide: [In-Game Commands](/guides/in-game-commands).

### "First set your specimen number! (Ex: /specimen 12345678)"

**Fix:** the player types `/specimen` and their own 5 to 9 digit number in chat.

### "This command is disabled!"

**Fix:** turn it on with the `kit`, `payday` or `imstuck` admin command.

### "Starter kit has not been configured on this cluster yet!" or "Payday loot table has not been configured..."

The list is empty.
**Fix:** upload items with `setkitpaths` or `setpaydaypaths`.

### "I couldn't find your Game ID, please try again"

**Fix:** make sure the player has joined and your chat relay works.

### "Upload must be a `.txt` file!" or "You must attach a text file containing the paths!"

**Fix:** save as plain `.txt` and attach it to the same message as the command.

### Nothing happens and no error

Arkon could not reach the server through RCON. See [RCON Setup](/guides/rcon-setup).

### A vote command says it is disabled, or a vote never passes

Votes (day, night, dino wipe, cleanup) can be switched off with the **MapVotes** button, and they have their own cooldown (**MapVote Cooldowns**). A vote needs about half the players online to agree, within 8 minutes. See [In-Game Commands](/guides/in-game-commands).

### The rename command says it is disabled

**Fix:** turn on the second **Rename** button in `+viewservers`. See [In-Game Commands](/guides/in-game-commands).

### Cooldowns start over

Cooldowns are kept in memory and reset when the bot restarts. Nothing to fix.

## Tribe logs

Guide: [Tribe Logs](/guides/tribe-logs).

### "Private tribelogs have not been configured yet!"

The claim channel or claim role is missing. Do the claim channel and claim role steps in the guide.

### "You are not in any tribes yet!"

Arkon has not seen you online in a tribe.
**Fix:** join the server, wait a minute, try again.

### "I need the Manage Threads permission..." or "...Create Private Threads permission in the claim channel!"

**Fix:** give Arkon both permissions in that channel.

### "This tribe has already been claimed by ..."

**Fix:** ask them to run `+threadtransfer`, or an admin can run `+tribeset unclaim`.

### "This command must be run inside a tribelog thread!"

**Fix:** open the thread and run it there.

### "This channel is already set as the tribe log for another cluster!"

**Fix:** pick a different channel.

### `+threadpurge` does nothing

**Fix:** run `+threadpurge true`.

### Nothing posts in the master channel

RCON may be down, or the channel is shared with another log.
**Fix:** check [RCON Setup](/guides/rcon-setup) and give the log its own channel.

## Chat and logs

Guide: [Chat and Logs](/guides/chat-and-logs).

### Game chat never shows in Discord

No Crosschat Channel is set for that map, or the Crosschat button is grey.
**Fix:** set the channel and make the Crosschat button green. Note that turning Crosschat off only stops game chat and command replies going to Discord. Interchat and the kill feed keep working.

### Discord messages do not appear in game

The message was a command, from a bot, in a thread, or only had links or emoji.
**Fix:** send plain text in the map's chat channel.

### Nothing is polled at all

The server is off in Arkon, or it was not online in the last 30 minutes.
**Fix:** turn the server on in `+viewservers` and start it.

### "That chatlog channel is already in use by another log in this cluster!"

**Fix:** pick a different channel.

### "There are no servers to select!"

**Fix:** add and enable a server. See [Getting Started](/guides/getting-started).

### `+whowason` errors

- "Invalid timestamp format!" Use `2026-04-10T16:20:00` or `4:20pm April 10 2026`.
- "No players were online at that time." Try a different time.
- "No players found!" or "Multiple players found, please be more specific!" Use a Discord mention or a game ID.
- "No data found for the specified time range." Widen the window.

### Kill feed line never appears

Kill feed needs three things: it must be on, the map needs a Crosschat Channel, and tribe log lines must be arriving over RCON. It does not need a Tribelog Channel.
**Fix:** run `+arkset killfeed`, set the Crosschat Channel, and check [RCON Setup](/guides/rcon-setup).

### "Invalid Timezone"

**Fix:** use a real timezone name with `+arkset timezone`. See [Chat and Logs](/guides/chat-and-logs).

## Status channel

Guide: [Status Channel](/guides/status-channel).

### Nothing was posted after `+serverstatus channel`

That command only saves the channel.
**Fix:** run `+serverstatus init`, or wait about 2 minutes.

### "I am missing the following permissions for that channel!"

**Fix:** give Arkon View Channel, Send Messages, Embed Links and Attach Files.

### "No status channel has been set!"

**Fix:** run `+serverstatus channel #your-channel`, then `+serverstatus init`.

### "I could not find the channel you set!"

The channel was deleted.
**Fix:** set a new one with `+serverstatus channel`.

### `+serverstatus time 1h` gives an error

It needs seconds.
**Fix:** type `+serverstatus time 3600`.

### "Sorry, the maximum time the free version of Arkon allows is 1 hour"

**Fix:** use `3600` or less, or get [Premium](/guides/premium).

### "The histogram can display a maximum of 12 hours"

**Fix:** use 43200 or less.

### The graph did not change

The graph picture is redrawn about every 15 minutes. Wait.

### The link to the status message stopped working

Arkon posts a fresh message about every 7 days. Link to the channel instead.

## Playtime roles

Guide: [Playtime and Roles](/guides/playtime-and-roles).

### A player has hours but no role

They have not registered, or Arkon's role is below the role.
**Fix:** have them use `+register`, then run `+arkset initroles`.

### "The playtime role X is higher or equal to my top role! I can not assign it to users!"

**Fix:** move Arkon's role above that playtime role. See [Playtime and Roles](/guides/playtime-and-roles).

### "That amount of time isnt linked to a role!"

**Fix:** check with `+arkset viewranks`.

### "Invalid welcome message!"

You used braces other than `{username}` or `{gameid}`. Remove other brace text.

### "That invite doesn't exist or has expired."

**Fix:** make a new never-expiring invite.

### "Invalid time format!"

**Fix:** use `45m`, `6h` or `2d6h`.

## Moderation and security

Guides: [Moderation](/guides/moderation) and [Security](/guides/security).

### Ban: "Xbox IDs are 16 digits, Steam IDs are between 17 and 19 digits, and EOS IDs are 32 characters long"

**Fix:** copy the ID again and check for extra spaces.

### Ban: "No servers found"

You have no enabled server of the right game for that ID.
**Fix:** Steam and Xbox IDs need an ASE server. EOS IDs need an ASA server. Check `+viewservers`.

### Ban: "Failed to execute command"

No server answered, so Arkon saved nothing.
**Fix:** check [RCON Setup](/guides/rcon-setup) and try again.

### "I cannot ban them from the Discord, please do it manually."

**Fix:** move Arkon's role above theirs and give it Ban Members.

### No record in the modlog

**Fix:** type `+modlogset modlog #mod-log`.

### `+syncbans` says to wait

**Fix:** wait 5 minutes (10 for `all`).

### A banned player is back on a server

The server's ban list lost them. Arkon re-bans them when they join.
**Fix:** run `+syncbans fromdb`.

### Admins keep getting banned as imposters

Their game account is not linked, they left the Discord server, or they have no Admin role.
**Fix:** link their account and give them the Admin role, or add their ID to `+arkset imposterwhitelist`. Then unban them.

### Nothing is detected for RDP dupes

Detection is off, or the cluster has only one enabled server.
**Fix:** run `+rdpdupe view`. Turn it on and enable 2 or more servers in the cluster.

### A whitelist ID stopped working

The whitelist commands are toggles, so a second run removed it. Add it again.

## Server control

Guide: [Server Control](/guides/server-control).

### "You do not have permission to run that command!"

You are a Mod and the first word of the command is not on the allow list.
**Fix:** an Admin runs `+arkset modcommands <first word>`.

### "No servers found with those criteria"

**Fix:** check cluster and server names with `+viewservers`, and that the server is turned on.

### "No Response!"

The server did not answer in 60 seconds.
**Fix:** check [RCON Setup](/guides/rcon-setup).

### "You cannot use `all` for cluster or server!"

`/bulksend`, `clearall` and `equipall` need a real cluster and server. Type the names.

### A schedule will not turn on

It runs more often than every 5 minutes. Make the interval 5 minutes or more.

### "You don't need to include `cheat` when using Rcon commands!"

**Fix:** remove `cheat` from the front.

## ArkView and map tools

🔹 These need ArkView (a small helper program that reads your save files). Setup: [ArkView Setup](/guides/arkview). Map command guide: [Map Tools](/guides/map-tools). Checks guide: [Anti-Cheat](/guides/anti-cheat).

### "There are no servers with an ArkView port set!" or "There are no servers to select!"

No enabled server has an ArkView port, or the command is switched off for you.
**Fix:** fill in the **Port** under **ArkView** in `+viewservers`.

### "There is no data ready for this server yet, come back later."

ArkView has not read the save yet.
**Fix:** wait a few minutes, then run `+arkviewer`.

### An "ArkView Error" message

Arkon cannot reach ArkView, or the key is wrong.
**Fix:** check ArkView is running and the port is open. See [ArkView Setup](/guides/arkview).

### An ArkView Error with status 401 or 403 (wrong API key)

The key in ArkView's `config.ini` does not match Arkon's.
**Fix:** copy the key again from `+arkset view`, paste it into `APIKey`, and restart ArkView. This also happens after `+arkset regenkey`.

### Map commands time out

Arkon cannot reach ArkView.
**Fix:** check the port forward, firewall rule and the Port in `+viewservers`. Details in [ArkView Setup](/guides/arkview).

### Map data works but tribes and players are empty

The `.arkprofile` and `.arktribe` files are not next to the `.ark` file.
**Fix:** point `MapFilePath` at the save in its real folder, or copy those files along with it.

### "Hunting is not enabled for {map}" or "You can use `hunt` again ..."

Hunt is switched off for that server, or the cooldown has not finished.
**Fix:** an Admin can use **ArkView Toggles**. Otherwise wait for the time shown.

### Hunt cannot find a modded dino

**Fix:** add it with `+setcustomdinos`.

### `finditem` finds nothing

It matches the technical item name, not the in-game name.
**Fix:** use the blueprint name in one word.

### Anti-cheat: "There are no valid server names set!"

**Fix:** run `+setvalidservers Island, Ragnarok`.

### Anti-cheat: tame warnings or automatic alerts never come

The tame check only covers ASE, needs ArkView, needs a limit above 0, and runs every 10 minutes at 95% of the limit. It is not Premium only. The duplicate tame check is [Premium](/guides/premium) only.
**Fix:** set `+arkset uncryolimit` and make sure ArkView is connected. See [Anti-Cheat](/guides/anti-cheat).

## Xbox

🔸 These are for Xbox and Microsoft Store ASE only. Guide: [Xbox Features](/guides/xsapi).

### "Server has not been authorized by the xbox API!" or "This server hasn't been authenticated with Microsoft XSAPI!"

The host Gamertag was never signed in.
**Fix:** run `+xsapi authenticate` for it.

### "Authorization failed. The code may have expired or already been used."

**Fix:** start again and paste the code right away.

### "Authorization timeout."

You waited over 10 minutes. Run the command again.

### "Failed to refresh tokens for ..."

The host sign-in expired or was revoked.
**Fix:** sign in again with `+xsapi authenticate`.

### "Xbox IDs are 16 digits long!"

**Fix:** use the 16 digit Xbox ID.

### "This player's ID apears to be for steam or ASA..."

These tools are ASE Xbox and Microsoft Store only.

### "Failed to authenticate through Xbox API" when registering

**Fix (admin):** see [Xbox Features](/guides/xsapi). Players can use manual mode or register in game.

### "This feature requires your server owner to have an Arkon Premium subscription!"

**Fix:** see [Premium](/guides/premium).

### `+addme` does not work

The host Gamertag must be signed in first (`+xsapi authenticate`), and the player must be on Xbox or the Microsoft Store version. See [Xbox Features](/guides/xsapi).

## Premium and limits

Guide: [Premium](/guides/premium).

### "You cannot have more than N server(s) using the free version of Arkon"

You hit the free server limit. Switched-off servers still count.
**Fix:** subscribe, or remove a server.

### "You have reached the maximum number of schedules for the free tier." or "You have reached the maximum number of schedules."

**Fix:** delete one or subscribe. The second message is the Premium cap.

### A schedule or server was switched off by itself

Free servers that stay offline for 30 days are switched off, and schedules can be disabled when Premium lapses. Arkon posts a message in the alert channel set with `+arkset alertchannel`, or in the event log if none is set. See [Premium](/guides/premium) and [Server Control](/guides/server-control).

### "The total amount of servers I can manage is 100..."

That is the cap, even on Premium. Remove a server you no longer use.

### Arkon left a new Discord server

You already own as many Discord servers with Arkon as your plan allows (1 Free, 5 Premium).
**Fix:** subscribe, or use Arkon in fewer servers.

## Still need help

Join the [Arkon Support Server](https://discord.gg/RaR3wR4MgY) for direct help.

When you ask, please include:

- The command you ran
- The exact error message (a screenshot is best)
- Your server type (ASE or ASA, self-hosted or hosted)

## Related pages

- [Home](/)
- [Getting Started](/guides/getting-started)
- [RCON Setup](/guides/rcon-setup)
- [Server Settings](/guides/server-settings)
- [Player Getting Started](/guides/player-getting-started)
- [Quick Reference](/guides/quick-reference)
- [Glossary](/guides/glossary)
- [Premium](/guides/premium)
