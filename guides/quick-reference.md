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

### In-Game Commands
| Command | Description |
|---------|-------------|
| `+kit` | Claim starter kit (one-time) |
| `+imstuck` | Get unstuck items |
| `+voteday` | Vote to change time to day |
| `+votenight` | Vote to change time to night |
| `+players` | See online player count |

### Map Tools 🔹
| Command | Description |
|---------|-------------|
| `+hunt <dino>` | Find wild dinos on the map |
| `+findtame <query>` | Find your tamed dinos |
| `+mapstats` | View map statistics |

---

## 🛡️ Moderator Commands

| Command | Description |
|---------|-------------|
| `+findplayer <query>` | Locate a player in-game |
| `+structures <tribe>` | View tribe's structure locations |
| `+territory` | Visualize tribe territories |
| `+findexpired <days>` | Find inactive tribes |
| `+checkmassbreed` | Detect mass breeding areas |
| `+rcon <cluster> <server> <cmd>` | Run RCON command |
| `+banplayer <id> [reason]` | Ban player from all servers |
| `+unbanplayer <id>` | Unban a player |
| `+doexit <cluster> <server>` | Shut down a server |
| `+dorestartlevel <cluster> <server>` | Restart a server |

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

### Xbox/Crossplay 🔸
| Command | Description |
|---------|-------------|
| `+xsapi authenticate` | Link host Gamertag |
| `+xsapi view` | View XSAPI settings |
| `+xsapi cleanfriends <cluster> <server> [days]` | Remove inactive friends |
| `+xsapi autofriend toggle` | ⚡ Toggle auto-friend system |
| `+xsapi altdetection toggle` | ⚡ Toggle alt detection |

---

## 📋 Useful Links

- [Full Admin Commands](/commands/admin-commands)
- [Full Mod Commands](/commands/mod-commands)
- [Full Player Commands](/commands/player-commands)
- [FAQ & Troubleshooting](/guides/faq)
- [Glossary](/guides/glossary)
- [Discord Support](https://discord.gg/RaR3wR4MgY)
