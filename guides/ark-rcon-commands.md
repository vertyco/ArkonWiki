---
title: Ark RCON Commands - Full Server Admin Reference (ASE & ASA)
description: Complete list of Ark RCON commands for server admins. Save, broadcast, kick, ban, destroy wild dinos, set time, and more. Run them from Discord with Arkon.
published: true
date: 2026-06-13T00:00:00.000Z
tags: rcon, ark, commands, server-admin, ase, asa, reference
editor: markdown
dateCreated: 2026-06-13T00:00:00.000Z
---

# Ark RCON Commands

RCON (Remote Console) lets you send admin commands to a running Ark dedicated server without being in-game. It works on both Ark: Survival Evolved (ASE) and Ark: Survival Ascended (ASA), as long as you have enabled RCON in your server settings and know the admin password.

This page is a reference for the most useful Ark RCON commands. With [Arkon](/), you run every command below straight from Discord, schedule them to fire automatically, and sync the results across an entire cluster, no need to keep a console window open.

## Enabling RCON on your Ark server

Add these to your `GameUserSettings.ini` under `[ServerSettings]`:

```ini
RCONEnabled=True
RCONPort=27020
ServerAdminPassword=YourStrongPasswordHere
```

Restart the server. Any RCON client (or Arkon) can now connect on `RCONPort` using `ServerAdminPassword`.

> Keep `ServerAdminPassword` secret. Anyone with it has full control of your server. Arkon's Imposter Protection auto-bans anyone who discovers and abuses it.
{.is-warning}

## Server management commands

| Command | What it does |
|---|---|
| `SaveWorld` | Force an immediate world save. Run before restarts and backups. |
| `DoExit` | Shut the server down cleanly. |
| `DoRestartLevel` | Restart the current map without a full process restart. |
| `GetGameLog` | Pull recent server log lines. |
| `GetChat` | Read recent in-game chat. |
| `Broadcast <message>` | Send a screen-wide message to every player. |
| `ServerChat <message>` | Post a message in global chat. |
| `ServerChatTo "<EOSID>" <message>` | Private message one player by ID. |
| `SetMessageOfTheDay <message>` | Set the message shown when players join. |

## Player management commands

| Command | What it does |
|---|---|
| `ListPlayers` | List every connected player with their ID and EOS/Steam ID. |
| `KickPlayer <ID>` | Disconnect a player. |
| `BanPlayer <ID>` | Ban a player from the server. |
| `UnbanPlayer <ID>` | Lift a ban. |
| `RenamePlayer "<old>" <new>` | Rename a survivor. |
| `RenameTribe "<old>" <new>` | Rename a tribe. |
| `AllowPlayerToJoinNoCheck <ID>` | Add a player to the server whitelist. |
| `DisallowPlayerToJoinNoCheck <ID>` | Remove a player from the whitelist. |

## World and creature commands

| Command | What it does |
|---|---|
| `SetTimeOfDay <hh:mm:ss>` | Change the in-game time of day. |
| `DestroyWildDinos` | Wipe and respawn all wild creatures. Common after a settings change. |
| `DestroyAll <ClassName>` | Destroy every instance of a class (use with care). |
| `Slomo <multiplier>` | Change game speed (1 is normal). |

## Run Ark RCON commands from Discord with Arkon

Typing RCON commands by hand into a console is slow and easy to fumble across a cluster of servers. Arkon turns the whole list above into Discord commands and automation:

- **One-click execution:** run any RCON command on one server or a whole cluster from Discord.
- **[Scheduled Commands](/commands/admin-commands):** auto-run `SaveWorld`, `DestroyWildDinos`, broadcasts, and restarts on a timer.
- **Cross-chat and broadcasts:** `Broadcast` and `ServerChat` wired into your Discord channels.
- **Ban Sync:** a single `BanPlayer` propagates across every server automatically.

Ready to stop using a raw console? [Set up Arkon in about 10 minutes](/guides/getting-started) or [invite the bot](/) to your Discord.

## Related guides

- [Getting Started](/guides/getting-started) - connect your first server
- [Admin Commands](/commands/admin-commands) - Arkon's full admin command set
- [All Commands](/commands/all-commands) - every Arkon command
- [FAQ & Troubleshooting](/guides/faq) - common questions
