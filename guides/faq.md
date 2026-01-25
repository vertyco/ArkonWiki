---
title: FAQ & Troubleshooting
description: Common questions and solutions for Arkon bot issues
published: true
date: 2026-01-17T00:00:00.000Z
tags: 
editor: markdown
dateCreated: 2026-01-17T00:00:00.000Z
---

# Frequently Asked Questions

## General Questions

### What is Arkon?
Arkon is a Discord bot designed to help manage Ark: Survival Evolved (ASE) and Ark: Survival Ascended (ASA) game servers. It provides features like cross-chat, player tracking, an in-game shop, and much more.

### Which platforms does Arkon support?
- ✅ Ark: Survival Ascended (ASA) - All platforms
- ✅ Ark: Survival Evolved (ASE) - Self-hosted and most providers
- ❌ ASE on Nitrado - **Not supported**

### Is Arkon free?
Yes! Arkon has a generous free tier that includes most features for 1 server. [Premium](/guides/premium) unlocks additional servers (up to 100) and advanced features like Xbox alt detection.

### What's the bot prefix?
The default prefix is `+`. You can change it with `+set serverprefix <newprefix>`

---

## Connection Issues

### "Connection failed" when adding a server
Check these common causes:

1. **RCON port not forwarded** - Ensure your router forwards the RCON port (usually game port + 1) to your server's local IP
2. **Firewall blocking connection** - Add a TCP inbound exception for the RCON port on Windows Firewall
3. **Wrong IP or port** - Double-check your public IP and RCON port number
4. **CGNAT** - Carrier-grade NAT won't work. Contact your ISP or use a VPN with port forwarding
5. **RCON not enabled** - Make sure RCON is enabled in your server's GameUserSettings.ini

> Arkon's IP address is `51.79.109.160` - whitelist this if your firewall requires it.
{.is-info}

### Bot not responding to commands
1. Check that the bot has permission to **Send Messages** and **Embed Links** in the channel
2. Verify you're using the correct prefix (default is `+`)
3. Make sure you have the required role (Admin/Mod) for restricted commands
4. Try the command in a different channel

### Server shows offline but it's running
- The bot checks server status every few minutes - wait a moment and refresh
- Verify RCON is still accessible (server restart may have changed the IP)
- Check if your ISP changed your public IP address

---

## Registration Issues

### "+register" not working in-game
1. Make sure you're typing in **global chat**, not tribe chat
2. Use your exact Discord username (not display name)
3. The server must have in-game commands enabled

### Can't use the shop after registering
1. Run `+playerstats` in Discord to verify your account is linked
2. Make sure you registered your **specimen number** with `+specimen <number>` or `+register`
3. Check that the shop is configured by the server admin

### "Player not found" errors
- Your Discord must be linked to your in-game character
- Try re-registering with `+register <YourDiscordUsername>` in-game

---

## Shop Issues

### Items not appearing in inventory
1. Make sure you're online and your inventory has space
2. Check if you're on the correct server (items go to the server you select)
3. Large purchases may take a moment to process

### "Insufficient funds" but I have enough
- Currency is per-server/cluster - check you're looking at the right balance
- Run `+bal` to see your current balance

---

## Xbox/Crossplay Issues

### +addme not working
1. Server owner must authenticate their host Gamertag first with `+xsapi authenticate`
2. You must be playing on the Microsoft Store version of Ark
3. The server must be hosted via Microsoft Store version

### Can't join via host Gamertag
1. Make sure the host Gamertag added you back as a friend
2. Check if the Gamertag's friends list is full (max 1000)
3. The server owner may need to run `+xsapi cleanfriends` to free up space

---

## Still Need Help?

Join the [Arkon Support Server](https://discord.gg/RaR3wR4MgY) for direct assistance!

**When asking for help, please include:**
- What command you ran
- The exact error message (screenshot if possible)
- Your server type (ASE/ASA, self-hosted/provider)
