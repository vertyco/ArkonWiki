---
title: Crafter - Arkon Ark Discord Bot
description: Look up Ark crafting recipes in Discord with /craft. See ingredients, stack size, weight, where an item is crafted and its blueprint path. No setup needed.
published: true
date: 2026-10-14T00:00:00.000Z
tags: crafter, craft, ark, recipes, ingredients, blueprint
editor: markdown
dateCreated: 2026-10-14T00:00:00.000Z
---

# Crafter

Crafter tells you what an Ark item is made of. Type `/craft` and an item name. Arkon replies with the full recipe, down to the raw resources.

It works right away. There is nothing to set up, and it does not need a connected game server.

**You need:**

- Arkon in your server. That is all.

## How it works

```mermaid
graph LR
A["Player types /craft Gunpowder"] --> B["Arkon finds the closest item name"]
B --> C["Recipe built from Arkon's item list"]
C --> D["Reply only the player can see"]
```

Arkon has its own built-in list of about 1,500 items from Ark: Survival Evolved. It does not ask your game server anything.

## Look up an item

### Step 1: Type the command

Where: any channel where Arkon can read and reply.

Type `/craft` and pick the `item` box. As you type, Discord shows up to 25 matching item names. Pick one and press Enter.

You can also use the prefix version: `+craft Gunpowder`. The prefix version has no list of suggestions, so type the name yourself.

### Step 2: Read the reply

You will see: a card with the item name at the top and these lines.

| Line | What it means |
|---|---|
| Stack Size | How many fit in one slot |
| Weight | Weight of one item |
| Category | The kind of item, like Resource or Structure |
| Class Name | The internal game name. It links to the item's page on the Ark wiki |
| Crafted In | Where you can make it, like a Mortar and Pestle. Shows `?` if unknown |
| Yields | How many items one craft gives |

If the item has a recipe, an **Ingredients** box shows it as a tree. Ingredients that are themselves crafted are broken down too, so you see every raw resource. A **Blueprint Path** box at the bottom holds the item's game path.

<img src="/assets/guide-crafter-result.png" alt="The /craft reply for Gunpowder" style="width: 600px; max-width: 100%;"/>

### Step 3: Check it worked

Look at the numbers next to each ingredient. They are already multiplied through the whole tree. In the example, Gunpowder needs 1 Sparkpowder, and that Sparkpowder needs 2 Flint and 1 Stone.

> With `/craft`, only the player who typed it can see the reply. Nobody else in the channel sees it. With `+craft`, the reply is a normal message.
{.is-info}

## Use the blueprint path

The Blueprint Path is the text you need for admin commands and for [Lootboxes](/guides/lootboxes) or the [RCON shop](/guides/rshop). Copy it from the box. See [Ark RCON commands](/guides/ark-rcon-commands) for where paths are used.

## Commands

| Command | Who | What it does | Example |
|---|---|---|---|
| `/craft <item>` (also `+craft`) | Everyone | Shows the recipe, ingredients and blueprint path for an item | `/craft item:Gunpowder` |

There are no settings and no admin commands.

## Common problems

| Problem | Why it happens | Fix |
|---|---|---|
| The reply shows a different item than I typed | Arkon never says "not found". It picks the closest name in its list | Check the name at the top of the card. Retry with the full name from the suggestion list |
| No suggestion list shows up | Suggestions only work with the slash command | Use `/craft`, not `+craft` |
| No Ingredients box | The item has no recipe, for example a raw resource | Nothing to fix |
| Crafted In shows `?` | The item list has no crafting station for it | Look it up on the Ark wiki through the Class Name link |
| The recipe does not match my ASA server | The list is built from Ark: Survival Evolved | Use the recipe as a guide only and check in game |
| The reply disappeared | `/craft` replies can be seen only by the person who typed it, and Discord hides them over time | Run it again |

## Related pages

- [Lootboxes](/guides/lootboxes)
- [RCON shop](/guides/rshop)
- [Ark RCON commands](/guides/ark-rcon-commands)
- [Player getting started](/guides/player-getting-started)
- [FAQ](/guides/faq)
