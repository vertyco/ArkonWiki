---
title: RCON Shop Setup — Automated In-Game Item Store for Ark Servers
description: Set up Arkon automated RCON shop for your Ark servers. Configure items, pricing, quality scaling, blueprints, role discounts, lootboxes, and daily deals.
published: true
date: 2026-01-17T18:53:48.988Z
tags: shop, rcon, economy, setup, guide
editor: markdown
dateCreated: 2023-12-17T22:12:43.240Z
---

# Setting up the RShop
The RShop (RCON Shop) uses the `giveitem` rcon command to send items directly to a players inventory when they purchase an item. The currency used for purchase can be obtained in various ways depending on how you configure the bot in your server (via `+payday` or other minigames)

## Step 1. Get your shop template
Run `+rshopset template` to get an excel file with most of the items available in the game already filled out for you.
<img src="/assets/shoptemplate.png" style="max-width: 50%;"/>
Download the file and open it up.
> If you don't have microsoft office you can upload it to Google sheets for free!
{.is-info}

## Step 2. Configure Item Prices
<img src="/assets/rshopexcel.png" style="max-width: 90%;"/>

- Item: The name of the item shown to the user.
- Price: How many credits per 1 item (This can be a decimal, like 0.1 for cheap resources, it will be rounded up). 
	- `Set price to 0 to disable it from the shop, or delete the whole row`
- Quality Select: If TRUE, the user can select what quality they want, otherwise if FALSE it is always 1.
- Blueprint Select: If TRUE, the user can select if they want it as a blueprint, otherwise if FALSE it is always just an item.
- Stack Size: The maximum stack size for that item on your server.
	- To handle this automatically, you can run `+rshopset readstacks` and upload your Game.ini file with the command.
- Category: An easy way to group items together, Items with the same category will be in the same menu.
- Description: This is optional, you can leave blank. Shows a description to the user.
- Class Name: The actual class of the item, this is required.
- Blueprint: The full blueprint path of the item, this is used in the RCON command to send it.
	- Example: `"Blueprint'/Game/PrimalEarth/CoreBlueprints/Items/Structures/Misc/PrimalItemStructure_Turret.PrimalItemStructure_Turret'"`
- Server Type: What type of servers can the item be purchased on.

#### Packs Tab
The rshop template has a second tab called `Packs`, here you can add multiple items to a single purchase as a "Pack".
Under the `Commands` column, you add the entire blueprint path along with the quantity/quality/bp specifier numbers. Separate each command with a comma.
![packstab.png](/assets/packstab.png)

> If you used Google sheets, you can download the prices back to an excel file.
> <img src="/assets/downloadexcel.png" style="max-width: 50%;"/>
{.is-info}


## Step 3. Upload Your Item Prices
Now that you've setup the prices you want, you can upload the file to discord with a command.
Run `+rshopset upload` and attach the excel file to the command.
<img src="/assets/uploadprices.png" style="max-width: 30%;"/>
You should get a message saying `Rshop has been updated!`

> Your prices have now been configured, you can now use the shop as-is, or continue to configure additional settings.
{.is-success}

## Step 4. Additional Settings
To view your shop settings, run `+rshopset view`
![shopsettings.png](/assets/shopsettings.png)
- Log Channel: All purchases are logged to this channel.
- Quality Exponent: Used for the exponential price multiplier when changing quality.
- Blueprint Multiplier: Used to multiply the price if blueprint is selected.
- Discount: % Discount globally (WIP)
- Categories: How many categories you have set.
- Shown Items: All items that have a price greater than 0.
- Unpriced Items: These items have no price and are not shown to users.

### Pricing Equation
When a user purhcases an item, the final price is applied like so:
`Final Price` = `Base Price` x `Quantity` x `Quality`^Quality-Multipler^
In the case of the image above it would be `final` = `base` x `quantity` x `quality`^1.0^
If blueprint is selected, the total price would then be multiplied by `4`

#### Commands
- Set the shop log channel: `+arkset shoplog #channel`
- Set the blueprint multiplier: `+rshopset bpmultiplier`
- Set the quality exponent: `+rshopset qualityexp`
- Set the maximum quality allowed to be purchased: `+rshopset maxquality`


