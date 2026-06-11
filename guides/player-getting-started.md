---
title: Player Guide - Register Your Character and Use the Arkon Shop
description: Link your Xbox, Steam, or ASA account to Discord with Arkon. Learn how to register, check stats, use the in-game shop, and earn virtual currency.
published: true
date: 2026-06-11T00:00:00.000Z
tags: player, registration, guide, getting-started
editor: markdown
dateCreated: 2023-12-18T02:19:40.657Z
---

# Player Guide

Welcome! This guide will help you link your Discord account to your Ark character so you can use features like the shop, stat tracking, and more.

> **Having trouble?** Check the [FAQ](/guides/faq) for solutions to common issues, or see the [Glossary](/guides/glossary) for unfamiliar terms.
{.is-info}

---

## 🔗 Get Set Up in 2 Steps

**Step 1: Link your Discord account.** Type `+register <YourDiscord>` **IN-GAME** in global chat. For example, if your Discord username is `vertyco`, type `+register vertyco` in-game.

> Linked! Run `+playerstats` in Discord to see your in-game player.
{.is-success}

> `+register` also works from Discord, but only for ASE servers. On ASA, register in-game.
{.is-info}

**Step 2: Register your Specimen #.** Some commands (`+kit`, `+payday`, `+imstuck`) and the shop need to know which character you are. Your Specimen # is the number on your implant. Set it with:

> `+specimen <YourSpecimenNumber>` in-game.
> Tip: `+register` and `+implant` can also set your Specimen #.
{.is-success}

Once both are done, you can use `+rshop` to buy items and the in-game commands below.

## 💰 How Currency Works
The shop runs on a virtual currency your admins configure. You earn it by:
- `+payday` - claim a reward every X hours (if your admins enabled it).
- **Playtime** - admins can hand out currency for time spent on the server.
- **Admin rewards** - events, bonuses, or supporter perks set by the server.

You spend it in the shop with `+rshop` (browse) or `+quickbuy <item>` (buy directly). Check what you have and your history with `+shopstats`.

### Xbox/PC Crossplay
If the server you play on is hosted via Microsoft store version and has a host Gamertag, you can make the host Gamertag add you as a friend so that you can easily join its session.
Simply run `+addme` and select a server, the host Gamertag for that map will add you as a friend, you can add it back and should then be able to go to its profile page and click `Join Game`

> The server owner needs to authenticate their host gamertags with the Xbox API for this to work
{.is-info}



## In-game commands
Type these in-game in global chat. Commands marked 🔑 need your Specimen # registered first.

**Account**
- `+register`: Link your Discord account and/or set your Specimen #.
- `+specimen` / `+implant`: Set your Specimen #.
- `+unregister`: Unlink the Discord account tied to your in-game account.
- `+rename`: Rename your character.

**Rewards**
- `+payday` 🔑: Claim a reward every X hours (if enabled by admins).
- `+kit` 🔑: Claim a one-time starter kit of configured items (if enabled).
- `+imstuck` 🔑: Get a small care package to respawn if you are stuck (if enabled).

**Voting**
- `+voteday`: Start a vote to make it day. Enough votes and it happens.
- `+votenight`: Start a vote to make it night.
- `+votecleanup`: Start a vote to clear beaver dams and spoiled eggs.
- `+votedinowipe`: Start a vote to wipe all wild dinos.

**Info**
- `+players`: See how many players are on the server.
- `+help`: Show this command list in-game for everyone.
  

## 📊 Playerstats
To view detailed info for every map you've been on, you can run the `+playerstats` command in Discord.
<img src="/assets/playerstats.png" style="max-width: 50%;"/>
This will track character names, playtimes, kills, deaths, dinos tamed ect..

---

## 📚 More Resources

- [Quick Reference](/guides/quick-reference) - All player commands in one place
- [FAQ](/guides/faq) - Common questions and troubleshooting
- [Glossary](/guides/glossary) - Definitions of Arkon terms