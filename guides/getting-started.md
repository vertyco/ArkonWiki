---
title: Getting Started With Arkon — Setup Guide for Ark Server Owners
description: Add Arkon to your Discord and connect your Ark servers in about 10 minutes. Step-by-step setup guide with screenshots for ASE and ASA server owners.
published: true
date: 2026-01-17T18:53:31.630Z
tags: setup, getting-started, guide, server-owner
editor: markdown
dateCreated: 2023-12-10T05:14:02.435Z
---

# Server Owner Setup Guide

Get Arkon running on your Ark server in about 10 minutes.

> **New to Arkon?** Check out the [Glossary](/guides/glossary) if you encounter unfamiliar terms, or the [FAQ](/guides/faq) if you run into issues.
{.is-info}

---

## ✅ Prerequisites Checklist

Before you begin, make sure you have:

- [ ] An Ark server (ASE or ASA) that you can manage - *this guide won't teach server hosting*
- [ ] RCON enabled on your server with a known port and password
- [ ] A static (or semi-static) public IP address - *CGNAT will not work*
- [ ] Port forwarding configured for your RCON port
- [ ] Basic Discord knowledge (roles, permissions, channels)

> **Already have the bot?** Skip to [Step 1](#step-1-configure-the-admin-and-mod-roles).
{.is-info}

**[👉 Invite Arkon to your Discord](https://discord.com/api/oauth2/authorize?client_id=857070505294430218&permissions=1495118769367&scope=applications.commands%20bot)**

Make sure the bot has permission to **Send Messages** and **Embed Links** in your channels!

---

# QuickStart
Setting up Arkon on your server can feel a little overwhelming at first, but this guide will try to get you off to a good start.

> When giving command examples below, you do **not** include the `<>` or `[]` in the command - those are just placeholders. `<required>` means you must provide a value, `[optional]` means it's optional.
{.is-info}

## About the Prefix
The default prefix for Arkon is `+`. You can change it at any time:

> `+set serverprefix <newprefix>`
> Example: `+set serverprefix !` changes the prefix to `!`
{.is-success}

---

## Step 1. Configure the Admin and Mod roles

Arkon uses Red-DiscordBot's role system to control who can use which commands. You'll need to tell the bot which Discord roles should have elevated permissions.

### Admin Role
Users with an **Admin role** get full access to Arkon's configuration commands, including server management, RCON access, and all bot settings.

> `+set roles addadminrole <role>` Adds an admin role
> `+set roles removeadminrole <role>` Removes an admin role
>
> Example: `+set roles addadminrole @ArkAdmin`
{.is-success}

### Mod Role
Users with a **Mod role** get limited staff permissions - they can use moderation commands like `+banplayer`, `+rcon`, and `+findplayer`, but cannot change bot configuration.

> `+set roles addmodrole <role>` Adds a moderator role
> `+set roles removemodrole <role>` Removes a mod role
>
> Example: `+set roles addmodrole @ArkMod`
{.is-success}

> **Tip:** You can assign multiple admin and mod roles if needed. Run the command multiple times with different roles.
{.is-info}

---

## Step 2. Create a cluster for your server
Even if you only have 1 server you will still need to create a cluster. This is separate from the Ark version of "cluster" in the sense that it is how the bot groups related Ark servers together.

> Command
> `+addcluster <cluster_name>`
> Example
> `+addcluster MyArkCluster`
{.is-success}

## Step 3. Add a server to the cluster.
> **Before adding your server, ensure the following are checked!**
> -- You must have a static or at least semi-static IP address. Carrier-grade NAT (CGNAT) will not work!
> -- The PC hosting your server has a private ip that is static (assigned by your router).
> -- The RCON port for the server youre trying to connect is forwarded in your router to that private IP.
> -- If Windows, ensure a firewall exception is made as TCP inbound for the RCON port.
> -- If applicable, ensure your router/firewall has the bot ip address `51.79.109.160` whitelisted.
{.is-warning}

> Command
> `+addserver <cluster_name>`
> Example
> `+addserver MyArkCluster`
{.is-success}

A menu will pop up with the following format:
![addserver.png](/assets/addserver.png)
Click the `Set Connection Info` button
![addservermodal.png](/assets/addservermodal.png)
Enter the connection information to your server and click `Submit`
![addserverconnect.png](/assets/addserverconnect.png)
You should see the info you entered in the modal, you can now click `Test & Save!` to test the connection and save the server.
> The server will only be saved if the connection is successful, you can make changes on your end and then click test again until you get it working.
{.is-info}

![addserverconnected.png](/assets/addserverconnected.png)
> Your server has now been added! The configured channels should start streaming in logs from your server.
{.is-success}

## Step 4. Set the status channel
This channel will display a live-updated embed showing all of your servers along with a historical player count graph.
> `+serverstatus channel #status-channel`
{.is-success}

To set the lookback time for the graph you can run the following
> `+serverstatus time <seconds>`
> Example: `+serverstatus time 3600` will display the last hour of player counts.
{.is-success}

<img src="/assets/statusgraph.png" style="max-width: 40%;"/>

## Step 5. Set the type of servers you plan on having
You can change the registration behavior for Arkon based on the type of servers you have.
The available types are `xbox`, `steam`, `both`
For ASA you will want to set `both`
> `+arkset clustertype <type>`
{.is-success}

## Step 6. Set Your Timezone
Type `+arkset timezone <YourTimezone>` to have the status graph be in your timezone.
Example: `+arkset timezone US/Eastern`

## Step 7. Tweaking Your Servers
You can view the server menu by typing `+viewservers`
Your main menu will look something like this.
<img src="/assets/viewservers.png" style="max-width: 40%;"/>
- `Interchat`: if Enabled, not only will each map sync chat to discord, but will also sync chat to every other map in that cluster.
- `Kit`: Shows how many items are included and how many users claimed their kit.
- `Imstuck`: Same as kit, but shows the cooldown (*If paths arent set it will use a default of organic poly, climbing picks, foundation, and GPS*)
- `Payday`: If Randomize is True, instead of giving every item in the path list to the player, a path is randomly selected each payday.
> Configuring the item paths for `Kit`, `Imstuck`, and `Payday` commands can be done by using the base command `+arkset ingame`
> <img src="/assets/arksetingame.png" style="max-width: 40%;"/>
{.is-info}



- `MapView Prices`: These are the prices for their respective commands.
>  The ArkView plugin is required to use the MapView commands
{.is-info}

Clicking on `Servers` will bring you to the servers within that cluster.
<img src="/assets/serverview.png" style="max-width: 40%;"/>

#### ArkView Settings
Host: Optional, if running the plugin on a server other than the one the map is on, you can specify an alternate ip.
Port: If set, the bot will try to enable the use of ArkView features such as `hunt`, `find`, `findtame` ect...
Below that shows whether each command is enabled.
[Click Her To Get ArkViewer](https://github.com/vertyco/arkview)

###### ArkView Features
- Extremely detailed tribelogs in discord
- Ability to view visual data about your maps
	- `+structures` will display an image of the map and have a red dot for each structure.
  - `+tamepie` and `+structurepie` shows a pie chart of how many structures each tribe has.
  - `+tribesize` can show the square footage a tribe's structures take up, and identify bases versus traps or spam
  - `+findtribe` shows details about a tribe along with each player in it.
  - `+findplayer` shows details about an in-game character.
  - `+checkmassbreed` can detect large clusters of dinos with breeding left enabled.
  - `+findexpired` get a list of tribes that havent been active in X days.
  - `+wipetribes` get a copy/past command list to wipe those tribes in-game.
  - `+mapstats` get an overview of all items/dinos/structures/tribes/players on the map.
- Ability for players to use special commands.
	- `+hunt` to hunt for wild dinos.
  - `+findtame` for finding lost tames.
  - `+playerheat` for viewing a heatmap of player locations.
  - `+find` to find locations of different eggs and beaver dams. (WIP)
  
#### Mapvote Settings
This section shows the configuration of the in-game voting commands, you can toggle them on and off per-map along with their cooldowns.

#### Xbox Info
If you are self-hosting via the Microsoft Store version of Ark, you can authenticate the host Gamertag to take advantage of the Xbox API to automatically manage your server Gamertag's friends list.

---

## 🎉 What's Next?

Now that your server is connected, explore these features:

- [Shop Setup](/guides/rshop) - Set up an automated item shop for players
- [Xbox/Crossplay Features](/guides/xsapi) - Authenticate host Gamertags for friend management
- [Quick Reference](/guides/quick-reference) - All essential commands in one place
- [FAQ & Troubleshooting](/guides/faq) - Solutions to common issues

**Need help?** Join the [Discord Support Server](https://discord.gg/RaR3wR4MgY)!
