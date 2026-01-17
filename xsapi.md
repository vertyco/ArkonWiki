---
title: ASE Crossplay Xbox Tools
description: 
published: true
date: 2023-12-18T01:40:20.657Z
tags: 
editor: markdown
dateCreated: 2023-12-18T01:40:19.645Z
---

# Microsoft Store ASE Exclusive features!
If you are self-hosting ASE with the Microsoft store version of Ark, you can use these features to manage the friends list on your host Gamertags.

## Features

###### Auto Friend Management
You can have the host Gamertag for each of your servers do the following automatically.
- Add new players as a friend when they first join your server.
- Follow players back that follow them.
- Automatically unfriend players after X days of inactivity.

###### Alt-Detection
Detect (*and optionally ban*) new players that join the server who may be alt accounts based on the following.
- `Detect silver accounts`: If a player joins with a silver account this will be flagged.
- `Minimum Gamerscore`: If a player joins with less than the minimum.
- `Minimum Folowers`: If a player joins with less followers than this theyll be flagged.
- `Minimum Following`: If a player joins and they are following less players than this theyll be flagged.

##### Send DMs to Players on behalf of your Host Gamertags
If your server host Gamertags are authenticated, when viewing `+playerstats` for someone there will be a `DM` button.
You can then send the player a DM on xbox via the host Gamertag of the last map they were on.

## Authenticating Your Server
Run `+xsapi authenticate` and a menu will appear.
<img src="/authenticate.png" style="max-width: 50%;"/>
Select your server and you will be instructed to sign into the xbox account associated with the server host Gamertag.
<img src="/authenticatestep2.png" style="max-width: 50%;"/>
Click `Sign In` and enter your credentials.
> Your user info is not stored, you're just authorizing the Arkon app to manage your host Gamertag friends list and send messages.
{.is-info}

> After signing in, you will be greeted with a LOCALHOST error, this is normal!
{.is-warning}

Copy the ENTIRE contents of the address bar after you authorize and then click `Enter Code`, a modal will pop up prompting you to enter the url, paste it there and click submit.

> Thats it, your server should now be linked to the host Gamertag account!
{.is-success}

### Using XSAPI Commands
To view all Xbox API commands for Arkon, run the base command `+xsapi`
This will display a list of subcommands you can use.
Run any subcommand with `+xsapi <subcommand>`
Example: `+xsapi autofriend` will display the available autofriend commands.
