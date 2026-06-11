---
title: Getting Started With Arkon - Setup Guide for Ark Server Owners
description: Add Arkon to your Discord and connect your Ark servers in about 10 minutes. Step-by-step setup guide with screenshots for ASE and ASA server owners.
published: true
date: 2026-06-11T00:00:00.000Z
tags: setup, getting-started, guide, server-owner
editor: markdown
dateCreated: 2023-12-10T05:14:02.435Z
---

# Server Owner Setup Guide

Get Arkon running on your Ark server in about 10 minutes. The fastest way is the **`/setup` wizard**, which connects and tests your first server for you. Prefer to do it by hand? A manual path is below too.

> **New to Arkon?** Check out the [Glossary](/guides/glossary) if you encounter unfamiliar terms, or the [FAQ](/guides/faq) if you run into issues.
{.is-info}

---

## ✅ Prerequisites Checklist

Before you begin, make sure you have:

- [ ] An Ark server (ASE or ASA) that you can manage - *this guide won't teach server hosting*
- [ ] **RCON enabled** on your server with a known port and password
- [ ] A **public IP address** that does not change (or a Dynamic DNS hostname)
- [ ] **Port forwarding** set up for your RCON port
- [ ] Basic Discord knowledge (roles, permissions, channels)

**Not sure what some of these mean? Here is the plain-language version:**

| Term | What it means |
|------|---------------|
| **RCON** | A remote console that lets Arkon send commands to your server. Enable it in `GameUserSettings.ini` with `RCONEnabled=True` and `RCONPort=27020` (27020 is the default for both ASE and ASA). Your RCON password is the `ServerAdminPassword` from that same file. See [RCON in the glossary](/guides/glossary). |
| **Public vs local IP** | Arkon connects to your **public** IP (the one at [whatismyip.com](https://whatismyip.com)), not a local `192.168.x.x` or `10.x.x.x` address. |
| **Port forwarding** | If you self-host, your router must forward the RCON port (TCP) to the PC running the server. [Router guides](https://portforward.com/router.htm). |
| **CGNAT** | If your ISP puts you behind Carrier-Grade NAT you cannot port forward. Ask your ISP for a public IP, or use a server host that gives you one. |
| **Dynamic IP** | If your IP changes on its own, use a free Dynamic DNS service ([No-IP](https://noip.com), [DuckDNS](https://duckdns.org)) and give Arkon the hostname instead. |

> **Using a game host?** Most providers support RCON and show the port and password in their control panel. **Nitrado (ASE only) does NOT support RCON, so Arkon cannot work with ASE on Nitrado.**
{.is-warning}

> If your router or firewall filters by address, whitelist Arkon's IP `51.79.109.160` and allow TCP inbound on your RCON port.
{.is-info}

**[👉 Invite Arkon to your Discord](https://discord.com/api/oauth2/authorize?client_id=857070505294430218&permissions=1495118769367&scope=applications.commands%20bot)**

Make sure the bot has permission to **Send Messages** and **Embed Links** in your channels!

---

# Path A: The `/setup` Wizard (Recommended)

The quickest way to connect your first server. Run the slash command in your server:

> `/setup`
{.is-success}

The wizard walks you through everything with buttons and pop-up forms. Have your server's **IP address**, **RCON port**, and **admin password** ready. It will:

1. **Pick your game** - ARK: Survival Evolved (ASE) or ARK: Survival Ascended (ASA).
2. **Check prerequisites** - a built-in checklist with an **I Need Help** button covering public IP, dynamic DNS, port forwarding, firewall, and hosting providers.
3. **Name your cluster** - a group for your servers. Use something simple like `pvp`, `pve`, or `main` (letters and numbers only). Even with one server you need a cluster.
4. **Enter server details** - server name, IP address (without the port), RCON port (default `27020`), and admin password.
5. **Test the connection** - Arkon live-tests RCON before saving. If something is wrong, it tells you exactly what (wrong password, timed out, connection refused) and how to fix it, then lets you edit and retry.
6. **Set chat channels** - pick a **server chat channel** (recommended, shows this server's chat plus command feedback) and optionally a **cluster chat channel** (combined chat from all servers in the cluster). You can skip and do this later.
7. **Crossplay (ASE only)** - if your server is Xbox/Win10 crossplay, the wizard points you to [autofriend.arkonbot.com](https://autofriend.arkonbot.com) and the `+addme` / `+gamertag` / `+xsapi` commands.

When it finishes, your cluster and server are saved and connected. Jump to **[After Setup](#after-setup)** to finish configuring.

> Already ran `/setup` before? Running it again shows a summary of your current clusters and servers with quick links instead of starting over.
{.is-info}

---

# Path B: Manual Setup

Prefer to set things up by hand, or adding more servers later? Use these commands.

> When giving command examples below, you do **not** include the `<>` or `[]` - those are just placeholders. `<required>` means you must provide a value, `[optional]` means it's optional. The default prefix is `+`; change it any time with `+set serverprefix <newprefix>`.
{.is-info}

## Step 1. Create a cluster

Even with one server you need a cluster. This is separate from Ark's own "cluster" concept; it is how Arkon groups related servers.

> `+addcluster <cluster_name>`
> Example: `+addcluster MyArkCluster`
{.is-success}

## Step 2. Add a server to the cluster

> **Before adding your server, confirm:**
> -- You have a static or semi-static public IP (CGNAT will not work).
> -- The PC hosting your server has a static private IP (assigned by your router).
> -- The RCON port is forwarded in your router to that private IP.
> -- If Windows, a firewall exception exists for TCP inbound on the RCON port.
> -- If applicable, your router/firewall has the bot IP `51.79.109.160` whitelisted.
{.is-warning}

> `+addserver <cluster_name>`
> Example: `+addserver MyArkCluster`
{.is-success}

A menu pops up:
![addserver.png](/assets/addserver.png)
Click `Set Connection Info`:
![addservermodal.png](/assets/addservermodal.png)
Enter your server's connection info and click `Submit`:
![addserverconnect.png](/assets/addserverconnect.png)
Review the details, then click `Test & Save!` to test the connection and save.
> The server is only saved if the connection succeeds. Fix things on your end and click test again until it works.
{.is-info}

![addserverconnected.png](/assets/addserverconnected.png)
> Your server is added! The configured channels should start streaming logs from your server.
{.is-success}

---

# After Setup

Both paths connect your server, but a few settings are still worth doing. (The wizard recommends these on its success screen.)

## 1. Set your Admin and Mod roles
Arkon uses Red-DiscordBot's role system. **Admin** roles get full configuration access; **Mod** roles get moderation commands like `+banplayer`, `+rcon`, and `+findplayer` but cannot change settings.

> `+set roles addadminrole <role>` Example: `+set roles addadminrole @ArkAdmin`
> `+set roles addmodrole <role>` Example: `+set roles addmodrole @ArkMod`
{.is-success}

> **Tip:** Run these multiple times to assign more than one admin or mod role.
{.is-info}

## 2. Set the status channel
A live-updating embed showing all your servers with a player-count graph.

> `+serverstatus channel #status-channel`
> `+serverstatus time <seconds>` Example: `+serverstatus time 3600` shows the last hour.
{.is-success}

<img src="/assets/statusgraph.png" style="max-width: 40%;"/>

## 3. Set your timezone
So the status graph uses your local time.

> `+arkset timezone <YourTimezone>` Example: `+arkset timezone US/Eastern`
{.is-success}

## 4. Set the cluster type
Controls registration behavior. Options: `xbox`, `steam`, `both`. For ASA, use `both`.

> `+arkset clustertype <type>`
{.is-success}

---

## ✅ Verify It Works

Confirm your setup actually took:

- `+checklist` - shows which features are configured and what is still missing.
- `+viewservers` - opens the server menu; your server should be listed.
- `+players` - shows who is currently online across your servers.

If your server appears and `+players` responds, you are connected.

---

## ⚙️ Optional Power Features

Once the basics work, you can layer these on. None are required to run a server.

- **In-game systems** (`+viewservers` to configure): `Interchat` syncs chat across every map in a cluster; `Kit` gives new players a one-time starter kit; `Imstuck` hands stuck players a respawn care package; `Payday` rewards players on a timer. Set the item paths with `+arkset ingame`.
  <img src="/assets/arksetingame.png" style="max-width: 40%;"/>
- **ArkView plugin** - unlocks map and investigation commands like `+hunt`, `+findtame`, `+structures`, `+mapstats`, plus detailed tribelogs. [Get ArkView](https://github.com/vertyco/arkview), then set the Host/Port under a server in `+viewservers`.
- **Mapvote** - toggle in-game voting commands per map with cooldowns.
- **[Shop Setup](/guides/rshop)** - an automated RCON item shop for players.
- **[Xbox/Crossplay Tools](/guides/xsapi)** - authenticate a host Gamertag for auto-friend and alt detection (ASE Microsoft Store).

---

## 🎉 What's Next?

- [Quick Reference](/guides/quick-reference) - All essential commands in one place
- [FAQ & Troubleshooting](/guides/faq) - Solutions to common issues
- [Premium](/guides/premium) - Compare Free vs Premium features

**Need help?** Join the [Discord Support Server](https://discord.gg/RaR3wR4MgY)!
