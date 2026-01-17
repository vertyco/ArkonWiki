---
title: Quick Reference
description: Essential Arkon commands at a glance
published: true
date: 2026-01-17T00:00:00.000Z
tags: 
editor: markdown
dateCreated: 2026-01-17T00:00:00.000Z
---

# Quick Reference

Essential commands organized by user type. Default prefix is `+`.

> Remember: `<required>` and `[optional]` are placeholders - don't type the brackets!
{.is-info}

---

## 👤 Player Commands

### Getting Started
| Command | Description |
|---------|-------------|
| `+register <discord_username>` | Link Discord to your character (run in-game) |
| `+specimen <number>` | Set your specimen/implant number |
| `+playerstats` | View your stats across all servers |
| `+addme` | 🔸 Have host Gamertag add you as friend |

### Shop & Economy
| Command | Description |
|---------|-------------|
| `+rshop` | Open the RCON shop |
| `+dshop` | Open the data shop |
| `+bal` | Check your balance |
| `+payday` | Claim periodic rewards |
| `+lootbox` | Open a lootbox (if configured) |
| `+shopstats` | View your purchase history |

### In-Game Commands
| Command | Description |
|---------|-------------|
| `+kit` | Claim starter kit (one-time) |
| `+imstuck` | Get unstuck items |
| `+kickme` | Kick yourself if stuck loading |
| `+voteday` | Vote to change time to day |
| `+votenight` | Vote to change time to night |
| `+players` | See online player count |

### Map Tools 🔹
| Command | Description |
|---------|-------------|
| `+hunt <dino>` | Find wild dinos on the map |
| `+findtame <query>` | Find your tamed dinos |
| `+mytames` | View your tribe's tames |
| `+mapstats` | View map statistics |
| `+playerheat` | View heatmap of player locations |

### Leaderboards
| Command | Description |
|---------|-------------|
| `+players` | Playtime leaderboard |
| `+tribelb <sort>` | Tribe leaderboard (kills/tamed/destroyed) |
| `+clusterlb [sort]` | Cluster leaderboard |
| `+alpha` | 🔹 Alpha tribe leaderboard |
| `+power` | 🔹 Power rating leaderboard |

---

## 🛡️ Moderator Commands

### Player Management
| Command | Description |
|---------|-------------|
| `+findplayer <query>` | Locate a player in-game |
| `+findtribe <query>` | Find tribe details |
| `+findsurvivor <name>` | Search by character name |
| `+banplayer <id> <reason>` | Ban player from all servers |
| `+unbanplayer <id>` | Unban a player |
| `+tempbanplayer <id> [duration] [reason]` | Temporary ban |
| `+bans` | View/manage bans |

### Investigation Tools
| Command | Description |
|---------|-------------|
| `+lookback <player> <start> [end]` | Find where player was during timeframe |
| `+whowason <time>` | List everyone online at a moment |
| `+timeline <player> <start> [end]` | Player join/leave timeline |
| `+susrating <player>` | 🔸 Check if Xbox account is likely an alt |

### Map Analysis 🔹
| Command | Description |
|---------|-------------|
| `+structures <tribe>` | View tribe's structure locations |
| `+territory` | Visualize tribe territories |
| `+findexpired <days>` | Find inactive tribes |
| `+checkmassbreed` | Detect mass breeding areas |
| `+finditem <blueprint> [tribe]` | Search for specific items |

### Server Control
| Command | Description |
|---------|-------------|
| `+rcon <cluster> <server> <cmd>` | Run RCON command |
| `+doexit <cluster> <server> [countdown]` | Shut down a server |
| `+dorestartlevel <cluster> <server> [countdown]` | Restart a server |

---

## ⚙️ Admin Commands

### Initial Setup
| Command | Description |
|---------|-------------|
| `+set roles addadminrole @role` | Set admin role |
| `+set roles addmodrole @role` | Set moderator role |
| `+addcluster <name>` | Create a server cluster |
| `+addserver <cluster>` | Add server to cluster |
| `+viewservers` | Open server management menu |

### Configuration
| Command | Description |
|---------|-------------|
| `+set serverprefix <prefix>` | Change bot prefix |
| `+arkset timezone <zone>` | Set timezone (e.g., US/Eastern) |
| `+arkset clustertype <type>` | Set platform: xbox/steam/both |
| `+serverstatus channel #channel` | Set status display channel |
| `+arkset ingame` | Configure kit/payday items |

### Shop Setup
| Command | Description |
|---------|-------------|
| `+rshopset template` | Download shop template |
| `+rshopset upload` | Upload configured prices |
| `+rshopset view` | View shop settings |
| `+rshopset discount <percent> [cluster]` | Set flat discount |
| `+rshopset discountrole @role <percent>` | Role-based discount |
| `+rshopset discountdays <day> <percent>` | Daily discount rotation |

### Lootbox Setup
| Command | Description |
|---------|-------------|
| `+lootboxset template` | Download lootbox template |
| `+lootboxset upload` | Upload lootbox config |
| `+lootboxset price <price>` | Set lootbox price |
| `+lootboxset cooldown <seconds>` | Set cooldown between opens |

### Anti-Cheat & Security 🔹
| Command | Description |
|---------|-------------|
| `+setvalidservers <names>` | Set allowed transfer servers |
| `+scanforeigntames` | Find tames from invalid servers |
| `+tamestatcheck <stat> <points>` | Find tames hitting stat thresholds |
| `+uncryocheck <amount>` | Find tribes over uncryo limit |
| `+arkset uncryolimit <limit> <cluster>` | Set max uncryoed tames |
| `+suswatch [gameid]` | Manage player watchlist |
| `+arkset banimposters` | Toggle imposter protection |

### Advanced Analytics
| Command | Description |
|---------|-------------|
| `+servergraph [timespan]` | Player count graph over time |
| `+dbstats` | View ArkTools database stats |
| `+shopoverview` | Shop economy summary |
| `+pollvotetime <message>` | Check playtime of poll voters |
| `+pollvotefilter <message> <cluster>` | Filter invalid poll votes |

### Ban Management
| Command | Description |
|---------|-------------|
| `+syncbans all [confirm]` | Sync all bans everywhere |
| `+syncbans fromdb [confirm]` | Push DB bans to servers |
| `+syncbans fromserver [confirm]` | Pull server bans to DB |
| `+globalbans` | View all global bans |

### Xbox/Crossplay 🔸
| Command | Description |
|---------|-------------|
| `+xsapi authenticate` | Link host Gamertag |
| `+xsapi view` | View XSAPI settings |
| `+xsapi cleanfriends <cluster> <server> [days]` | Remove inactive friends |
| `+xsapi autofriend toggle` | ⚡ Toggle auto-friend system |
| `+xsapi altdetection toggle` | ⚡ Toggle alt detection |
| `+xdm <player> <message>` | DM player via Xbox |

---

## 🌟 Discord Leveling Commands

### Player Commands
| Command | Description |
|---------|-------------|
| `+profile [user]` | View your or another user's profile card |
| `+setprofile` | Customize your profile background, colors, fonts |
| `+leveltop [stat]` | View the server leaderboard (xp/level/voice/messages) |
| `+stars [user]` | Give a star to thank a helpful member |
| `+startop` | View the star leaderboard |
| `+prestige` | Reset your level for prestige perks (if at max) |
| `+lastweekly` | View previous week's top contributors |

### Admin Commands
| Command | Description |
|---------|-------------|
| `+levelset toggle` | Enable/disable the leveling system |
| `+levelset view` | View all leveling settings |
| `+levelset addxp <user> <amount>` | Award XP to a user or role |
| `+levelset setlevel <user> <level>` | Set a user's level |
| `+levelset roles add <level> <role>` | Award role at level |
| `+levelset algorithm <part> <value>` | Customize XP curve |
| `+levelset messages xp <min> <max>` | Set XP per message range |
| `+levelset voice xp <xp>` | Set XP per minute in voice |
| `+weeklyset toggle` | Toggle weekly stat tracking |
| `+weeklyset channel <channel>` | Set weekly announcement channel |

---

## 💡 Suggestion System Commands

### Player Commands
| Command | Description |
|---------|-------------|
| `+idea <suggestion>` | Submit a new suggestion |

### Admin Commands
| Command | Description |
|---------|-------------|
| `+ideaset` | View all suggestion settings |
| `+ideaset channel <channel>` | Set the suggestion channel |
| `+ideaset anonymous <true/false>` | Toggle anonymous suggestions |
| `+ideaset upvoteemoji <emoji>` | Set upvote reaction |
| `+ideaset downvoteemoji <emoji>` | Set downvote reaction |
| `+ideaset minlevel <level>` | Require LevelUp level to suggest |
| `+ideaset minplaytime <hours>` | Require playtime to suggest |
| `+approve <id> [reason]` | Approve a suggestion |
| `+reject <id> [reason]` | Reject a suggestion |
| `+implemented <id>` | Mark suggestion as implemented |

---

## 💵 Extended Economy Commands

### Admin Commands
| Command | Description |
|---------|-------------|
| `+extendedeconomy view` | View economy settings |
| `+addcost <command> <cost>` | Add a cost to run a command |
| `+extendedeconomy transfertax <rate>` | Set transfer tax (0.05 = 5%) |
| `+extendedeconomy autopayday` | Toggle automatic paydays |
| `+extendedeconomy rolebonus <role> <rate>` | Payday bonus for role (0.1 = 10%) |
| `+extendedeconomy eventlog <event> [channel]` | Log bank events |
| `+banksetrole <role> <amount>` | Set balance for all with role |
| `+backpay <duration> [confirm]` | Award missed paydays |
| `+bankpie [top_count]` | View bank balance pie chart |

---

## 📋 Useful Links

- [Full Admin Commands](/commands/admin-commands)
- [Full Mod Commands](/commands/mod-commands)
- [Full Player Commands](/commands/player-commands)
- [FAQ & Troubleshooting](/guides/faq)
- [Glossary](/guides/glossary)
- [Discord Support](https://discord.gg/RaR3wR4MgY)
