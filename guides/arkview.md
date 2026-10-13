---
title: ArkView Setup Guide - Map Tools for the Arkon Ark Discord Bot
description: Install ArkView, the free companion plugin that lets Arkon read your Ark save and unlock map commands like +hunt, +findtame, +structures, and private tribelogs. Windows, Linux, and Docker setup for ASE and ASA.
published: true
date: 2026-10-12T00:00:00.000Z
tags: arkview, arkviewer, setup, guide, server-owner, map-tools
editor: markdown
dateCreated: 2026-10-12T00:00:00.000Z
---

# ArkView Setup Guide

ArkView is a free program that reads your Ark save file and hands the results to Arkon. Without it, Arkon can only talk to your server through RCON, so it can't see what is on the map. With it, map commands like `+hunt`, `+findtame`, and `+structures` start working.

> **New to Arkon?** Connect your server first with the [Getting Started guide](/guides/getting-started). ArkView is an add-on for a server that already works with Arkon.
{.is-info}

---

## What ArkView Unlocks

Everything marked 🔹 on the wiki needs ArkView. The main ones:

| Area | Commands and features |
|------|-----------------------|
| **Map tools** | `+hunt`, `+findtame`, `+mytames`, `+mapstats`, `+playerheat` |
| **Map analysis** | `+structures`, `+territory`, `+findexpired`, `+checkmassbreed`, `+finditem` |
| **Anti-cheat** | `+scanforeigntames`, `+tamestatcheck`, `+uncryocheck` |
| **Tribes** | Private tribelogs, tribelog alerts |

See the [Quick Reference](/guides/quick-reference) for what each command does.

---

## How It Works

ArkView runs next to your Ark server. Every time the server saves, ArkView reads the save and gets the data ready. When someone runs a map command, Arkon asks ArkView for that data over the internet.

```
Ark server  --writes save-->  ArkView  <--asks for data--  Arkon (Discord)
                              (your PC or server, one open port)
```

A few things follow from this:

- **ArkView must be able to read your save files.** If you host the server yourself, that's easy. If you rent from a game host, see [Using a Game Host](#using-a-game-host).
- **Arkon must be able to reach ArkView.** Like RCON, that means one open TCP port.
- **One ArkView per map.** Running three maps means three copies of ArkView, each on its own port.

---

## ✅ What You Need

- [ ] An Ark server (ASE or ASA) already connected to Arkon
- [ ] Access to the server's save folder
- [ ] A free TCP port for each map (for example `8000`, `8001`, `8002`). **Not** your RCON or game port.
- [ ] The ability to port forward that port, the same way you did for RCON
- [ ] About 2 GB of free RAM per map while it reads a save. Small maps use far less. Big, busy maps can need more.

---

## Step 1. Find Your Save File

ArkView needs the full path to your map's `.ark` file.

| Game | Where the save lives |
|------|----------------------|
| **ASE** | `ShooterGame/Saved/SavedArks/TheIsland.ark` |
| **ASA** | `ShooterGame/Saved/SavedArks/TheIsland_WP/TheIsland_WP.ark` |

Swap `TheIsland` for your map's name.

> **Player and tribe files must sit next to the save.** ArkView reads the `.arkprofile` (players) and `.arktribe` (tribes) files from the same folder as the `.ark` file. Your server already puts them there. If you copy saves somewhere else, copy those files too, or tribes, players, and tribelogs will come up empty.
{.is-warning}

> **No spaces in the path.** ArkView refuses a save path that contains a space. If your server sits under a folder like `Program Files`, see the fix in [Troubleshooting](#troubleshooting).
{.is-warning}

---

## Step 2. Install ArkView

Pick the one that matches your server.

### Option A: Windows

1. Download the latest `ArkViewer.exe` from [GitHub Releases](https://github.com/vertyco/arkview/releases).
2. Put it in its own folder, for example `C:\ArkView\TheIsland\`, and run it once. It creates a `config.ini` file next to itself, then you can close it.
3. Fill in `config.ini` (see [Step 3](#step-3-fill-in-configini)), then run `ArkViewer.exe` again and leave it open.

For more than one map, make one folder per map, each with its own copy of `ArkViewer.exe` and its own `config.ini`.

> **Start it with Windows:** press `Win + R`, type `shell:startup`, and put a shortcut to `ArkViewer.exe` in the folder that opens.
{.is-info}

### Option B: Linux (systemd)

These commands are for Ubuntu or Debian with Python 3.10 or newer. They install ArkView once, then run one copy per map. Swap `theisland` for your map's name.

1. Install ArkView under its own user:

```bash
sudo apt update && sudo apt install -y git python3-venv
sudo useradd -r -s /usr/sbin/nologin arkviewer
sudo mkdir -p /opt/arkviewer && sudo chown arkviewer:arkviewer /opt/arkviewer
sudo -u arkviewer git clone https://github.com/vertyco/arkview /opt/arkviewer
cd /opt/arkviewer
sudo -u arkviewer python3 -m venv .venv
sudo -u arkviewer .venv/bin/pip install --no-cache-dir -r requirements.txt
```

2. Make a folder and config for your map:

```bash
sudo -u arkviewer mkdir -p /opt/arkviewer/maps/theisland
sudo -u arkviewer cp /opt/arkviewer/default_config.ini /opt/arkviewer/maps/theisland/config.ini
sudo nano /opt/arkviewer/maps/theisland/config.ini
```

Fill it in using [Step 3](#step-3-fill-in-configini), then save with `Ctrl + O`, `Enter`, `Ctrl + X`.

3. Install the service:

```bash
sudo cp /opt/arkviewer/deploy/arkview@.service /etc/systemd/system/
sudo sed -i 's|main.py$|main.py 0.0.0.0|' /etc/systemd/system/arkview@.service
sudo systemctl daemon-reload
sudo systemctl enable --now arkview@theisland
```

The `sed` line makes ArkView listen for outside connections. Without it, ArkView only answers requests from the same machine, so Arkon can't reach it.

4. Watch the log to confirm it started:

```bash
journalctl -u arkview@theisland -f
```

For another map, repeat step 2 with a new folder name and a different `Port`, then run `sudo systemctl enable --now arkview@<newname>`.

> **Save files under `/home`?** The service blocks access to `/home` by default. Run `sudo sed -i 's|^ProtectHome=true|ProtectHome=read-only|' /etc/systemd/system/arkview@.service`, then `sudo systemctl daemon-reload` and restart the service. The `arkviewer` user also needs permission to read the save folder.
{.is-warning}

### Option C: Docker

Docker runs one container per map. Build the image from the ArkView repo:

```bash
git clone https://github.com/vertyco/arkview
cd arkview
cp docker-compose.example.yml docker-compose.yml
docker build -t arkviewer:latest .
```

Edit `docker-compose.yml`. For each map, set:

- the save folder mount (the `TheIsland_WP` folder for ASA, or the `SavedArks` folder for ASE) to `/saves`
- a `configs/<map>.ini` file mounted to `/app/config.ini`
- a unique host port, mapped to `8000` inside the container

Inside the container the paths change, so in each `.ini` use `MapFilePath = /saves/TheIsland_WP.ark` (ASA) or `MapFilePath = /saves/TheIsland.ark` (ASE), and keep `Port = 8000`. Then start it:

```bash
docker compose up -d
```

The example file has comments for every line. If your save files aren't owned by user ID 1000, build with `--build-arg UID=<uid> --build-arg GID=<gid>`.

---

## Step 3. Fill In config.ini

Most settings can stay as they are. These are the ones that matter:

| Setting | What to put |
|---------|-------------|
| `Port` | The TCP port Arkon will connect to, for example `8000`. Each map needs its own. |
| `MapFilePath` | Full path to the `.ark` file from [Step 1](#step-1-find-your-save-file). |
| `ClusterFolderPath` | *(Optional)* Your cluster transfer folder, so tames uploaded to the cluster show up too. Leave blank if you don't run a cluster. |
| `BanListFile` | *(Optional)* Path to your server's `BanList.txt`. |
| `Threads` | How many CPU cores ArkView may use while reading a save. `2` is fine for most servers. |
| `APIKey` | Your Arkon ArkView key (see below). Strongly recommended. |
| `Debug` | Leave this `False`. `True` blocks all outside connections. |

Example for an ASA server on Windows:

```ini
[Settings]
Port = 8000
MapFilePath = C:\ArkServer\ShooterGame\Saved\SavedArks\TheIsland_WP\TheIsland_WP.ark
ClusterFolderPath =
BanListFile =
Priority = LOW
Threads = 2
ReprocessOnArkDataUpdate = False
Debug = False
DSN =
APIKey = paste-your-key-here
```

### Set the API key

The API key stops strangers from reading your map data. Without it, anyone who finds your ArkView port can see where every tribe has built.

1. In Discord, run `+arkset view`. Copy the value next to **ArkView API Key**.
2. Paste it after `APIKey =` in every `config.ini` you run.
3. Restart ArkView.

Arkon sends this key every time it asks ArkView for data, and ArkView turns away any request without it. One key covers every ArkView in your Discord server. If the key ever leaks, the Discord server owner can run `+arkset regenkey` to make a new one. Arkon DMs it to you, and then you update every `config.ini` and restart each ArkView.

---

## Step 4. Open the Port

Arkon connects to ArkView the same way it connects to RCON, so the port must be reachable from the internet.

1. **Router:** forward the ArkView port (TCP) to the machine running ArkView. [Router guides](https://portforward.com/router.htm).
2. **Firewall on that machine:**
   - Windows (PowerShell as administrator): `New-NetFirewallRule -DisplayName "ArkView 8000" -Direction Inbound -Protocol TCP -LocalPort 8000 -Action Allow`
   - Linux with ufw: `sudo ufw allow 8000/tcp`
3. *(Optional)* To only let Arkon in, allow just Arkon's IP `51.79.109.160`. On Linux: `sudo ufw allow from 51.79.109.160 to any port 8000 proto tcp`.

> **Behind CGNAT?** Port forwarding doesn't work if your internet provider shares one public IP between customers. The [Nitrado guide](/guides/arkview-nitrado) shows how to use a cheap VPS as a relay, and the same relay works for a home server.
{.is-info}

---

## Step 5. Connect ArkView to Arkon

1. Run `+viewservers` in Discord.
2. Select your cluster, then click **Servers** and pick the server.
3. Click **ArkView**.
4. Fill in the form:
   - **Host IP:** leave it blank to use the same address as your RCON connection. Only fill it in if ArkView runs on a different machine. The box only fits 15 characters, so use an IP address.
   - **Port:** the `Port` from that map's `config.ini`. Not your RCON port.
5. Click **Submit**.

Repeat for each map. The **ArkView Toggles** button next to it has **Hunt**, **Find**, **FindTame**, and **Playerheat** switches. Set one to `False` to turn that player command off for that server.

---

## Step 6. Check That It Works

1. Wait for the first read. ArkView reads the save as soon as it starts. That takes about a minute on a typical map and up to several minutes on a big, busy one. Map commands return nothing until it finishes.
2. Run `+arkviewer` to see each server's ArkView status and when it last synced.
3. Try a real command, like `+structures <tribe name>` or `+hunt rex`.

If results come back, you're done. ArkView re-reads the save every time your server saves, so the data stays current on its own.

To turn on private tribelogs, set a tribelog channel for the cluster with `+tribeset logchannel <cluster> #channel`.

---

## Using a Game Host

ArkView has to run somewhere it can read your save files. Most rented game servers don't let you run your own programs, so you can't install ArkView on the host itself.

If your host gives you **FTP access** to the save folder, you can copy the save to a machine you control every few minutes and run ArkView there. The [ArkView on Nitrado (ASA)](/guides/arkview-nitrado) guide walks through this step by step. The same approach should work with other hosts that offer FTP, but Nitrado is the only one it has been tested on.

> **ASE on Nitrado** has no RCON, so Arkon can't connect to it at all. ArkView doesn't change that.
{.is-warning}

---

## Troubleshooting

| Problem | Likely cause | Fix |
|---------|--------------|-----|
| Map commands time out | Arkon can't reach ArkView | Check the port forward, the firewall rule, and the Port in `+viewservers`. Test from outside your network: on a phone with Wi-Fi off, open `http://<your-public-ip>:<port>/`. Any response means the port is open. |
| Works on the same PC but not from outside (Linux) | ArkView is only listening locally | Make sure the service's `ExecStart` line ends in `main.py 0.0.0.0` (the `sed` line in [Option B](#option-b-linux-systemd)), then restart the service. |
| "Invalid API key" or "No API key provided" | The key in `config.ini` doesn't match Arkon's | Copy the key again from `+arkset view`, paste it into `APIKey`, and restart ArkView. |
| Commands return nothing right after starting | The first read hasn't finished yet | Wait a few minutes on a big map, then check `+arkviewer`. |
| Map data works but tribes, players, or tribelogs are empty | The `.arkprofile` and `.arktribe` files aren't next to the `.ark` file | Point `MapFilePath` at the save in its real folder, or copy those files along with the save. |
| ArkView says the map path has invalid characters | The path has a space in it | Link a folder without spaces to it. On Windows (Command Prompt as administrator): `mklink /J C:\ArkSaves "C:\Program Files\ArkServer\ShooterGame\Saved\SavedArks"`, then use `C:\ArkSaves\...` in `MapFilePath`. |
| The Linux service restarts in the middle of reading | It ran out of its memory limit | Raise `MemoryMax=4G` in `/etc/systemd/system/arkview@.service`, then run `sudo systemctl daemon-reload` and restart the service. |

**Still stuck?** Ask in the [Discord Support Server](https://discord.gg/RaR3wR4MgY) and include what `+arkviewer` shows.
