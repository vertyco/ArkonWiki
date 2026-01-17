---
title: Getting Started With Arkon
description: 
published: true
date: 2025-10-01T01:15:41.924Z
tags: 
editor: markdown
dateCreated: 2023-12-10T05:14:02.435Z
---

## Prerequisites!
- Understand how to host and manage an Ark server, whether ASE or ASE, self-hosted or through a host provider. This tutorial will not teach you how to host an Ark server.


- Understand how to assign static ip addresses to your servers and port forward on your router so the bot can communicate with your servers.

- Understand the basics of Discord, bot commands and how to assign permissions in your server.

- If you haven't already done so, you will want to **[Invite the Bot!](https://discord.com/api/oauth2/authorize?client_id=857070505294430218&permissions=1495118769367&scope=applications.commands%20bot)**


- Make sure the bot has permission to send messages and embed links in the channels you are using!



# QuickStart
Setting up Arkon on your server can feel a little overwhelming at first, but this guide will try to get you off to a good start.

> when giving command examples below, you do **not** include the `<>` in the command, those are just placeholders.
{.is-info}

The prefix for arkon is `+`, but you can change it by typing `+set serverprefix !` or whatever other symbol or letter you want.


## Step 1. Configure the Admin and Mod roles.
- Admin: Users with this role will be considered administrative staff with permissions to use admin commands in-game.
> 	`+set roles addadminrole @role` Adds an admin role for the server.
> 	`+set roles removeadminrole @role` Removes an admin role for the server.
>
> Example: `+set addadminrole @ArkAdmin`
{.is-success}

- Mod: Users with this role will be considered minimal privelaged Discord-specific staff with minimal access to RCON command use through the bot.
>   `+set roles addmodrole @role` Adds a moderator role for the server.
>   `+set roles removemodrole @role` Removes a mod role for the server.
>
> Example: `+set addmodrole @ArkMod`
{.is-success}

  
## Step 2. Create a cluster for your server.
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
> -- If applicable, ensure your router/firewall has the bot ip address `51.81.94.254` whitelisted.
{.is-warning}

> Command
> `+addserver <cluster_name>`
> Example
> `+addserver MyArkCluster`
{.is-success}

A menu will pop up with the following format:
![addserver.png](/addserver.png)
Click the `Set Connection Info` button
![addservermodal.png](/addservermodal.png)
Enter the connection information to your server and click `Submit`
![addserverconnect.png](/addserverconnect.png)
You should see the info you entered in the modal, you can now click `Test & Save!` to test the connection and save the server.
> The server will only be saved if the connection is successful, you can make changes on your end and then click test again until you get it working.
{.is-info}

![addserverconnected.png](/addserverconnected.png)
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

<img src="/statusgraph.png" style="max-width: 40%;"/>

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
<img src="/viewservers.png" style="max-width: 40%;"/>
- `Interchat`: if Enabled, not only will each map sync chat to discord, but will also sync chat to every other map in that cluster.
- `Kit`: Shows how many items are included and how many users claimed their kit.
- `Imstuck`: Same as kit, but shows the cooldown (*If paths arent set it will use a default of organic poly, climbing picks, foundation, and GPS*)
- `Payday`: If Randomize is True, instead of giving every item in the path list to the player, a path is randomly selected each payday.
> Configuring the item paths for `Kit`, `Imstuck`, and `Payday` commands can be done by using the base command `+arkset ingame`
> <img src="/arksetingame.png" style="max-width: 40%;"/>
{.is-info}



- `MapView Prices`: These are the prices for their respective commands.
>  The ArkView plugin is required to use the MapView commands
{.is-info}

Clicking on `Servers` will bring you to the servers within that cluster.
<img src="/serverview.png" style="max-width: 40%;"/>

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










