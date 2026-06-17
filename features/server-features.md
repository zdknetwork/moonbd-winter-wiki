---
description: >-
  A summary of unique quality-of-life mechanics and custom systems on MoonBD.
  Covers inventory shortcuts, the Moon Master NPC, mail merging, and the Moon
  Coin currency.
---

# 🪁 Server Features

### Overview

MoonBD includes several custom features designed to streamline gameplay, improve inventory management, and centralize essential services.

### Interface & Utility

#### Item Delete Hotkey

Manage inventory space quickly using a custom shortcut.

1. The player opens the inventory.
2. The player presses `Delete` + `Left-click` on the target item.
3. The action is confirmed with `Enter` or `Space`.

#### Alchemy Tab Skip

The Alchemy UI includes a **Skip Button** for **Recharge**, **Polish**, and **Growth** actions. This removes the animation delay during alchemy progression.

### Centralized Services

#### [**Moon Master**](https://moonbd.online/codex/npc/900994) (All-in-One NPC)

The [**Moon Master**](https://moonbd.online/codex/npc/900994) in **Velia** provides multiple services in a single location:

* **Storage** and **Currency Exchange**
* **Central Market** access
* **Skill Addons**

#### Moon Coin System

**Moon Coins** serve as a specialized currency for **Cash Shop** items.

* Players can purchase the [**Moon Coin Box (1000)**](https://moonbd.online/codex/?q=Moon+Coin+Box&lim=25) in the website Cash Shop under the Custom section.
* Players can exchange these coins at [**Lux**](https://moonbd.online/codex/npc/900991) in **Velia** for **Central Market** cash items.
* **Moon Coins** are non-tradable.

### Item & Mail Mechanics

#### Merge Mails & Reward Migration

The server consolidates identical mail entries and migrates rewards to reduce clutter.

* **Black Spirit Safe:** Most mail rewards move automatically to the **Black Spirit Safe** for easier collection.
* **Merging:** Identical mails remaining in the inbox combine into a single stack. This triggers when clicking the **Play** button in the Launcher.
* **Exceptions:** Mails containing **Hammers**, **Enchanted Items**, or individual user messages remain in the standard mailbox.

#### Stackable Crystals

Select crystals now stack within a single inventory slot.

* **Technical Note:** To equip a stackable crystal, only one may remain in the inventory. Players must store extras in **City Storage** or **Market Storage** before equipping to avoid system errors.

#### Farming & Crio Shop Updates

* All farming seeds and **Crio Shop** items now appear as boxes.
* Players can process **Blue Seed Boxes** into **Mysterious Seeds**.
* Players can use a [**Processing Stone**](https://moonbd.online/codex/?q=Processing+Stone&lim=25) to enable **Mass Processing** for these recipes.

### Client Security & Protection

#### Custom Anticheat System

MoonBD implements a custom client-side anticheat system to ensure a fair play environment. The anticheat software runs automatically alongside the game client, preventing unauthorized modifications, memory editing, and third-party automation tools.

### Discord Bot Integration

The server features a dedicated Discord bot client integrated with the game servers to provide real-time updates, player tools, and notifications.

#### 1. Slash Commands (`/` Commands)

Regular server members can use the following commands directly in chat:

* `/help`: Displays a guide listing all bot commands, website links, and troubleshooting references.
* `/timers`: Lists active server events (loot drop events, battlefield bonuses, cash shop discounts, and donation bonuses) including multiplier values, countdowns, and the current online player count.
* `/status`: Displays the real-time status of sub-servers (Online, Offline, or Maintenance).
* `/boss`: Displays upcoming World Boss schedules and dynamic relative countdowns.
* `/link <page>`: Returns a direct link to specific pages on the website, featuring auto-complete choice matching.
* `/wiki <query>`: Searches the GitBook wiki database for quick gameplay guides or troubleshooting instructions.
* `/codex <query>`: Looks up any item in the Codex database to show its description, stats, gear progression stats (AP/DP), and its item icon.
* `/market <query>`: Queries live Central Market prices, listed trade stock, and total volume traded for items across different enhancement levels (PRI-PEN).
* `/shop <query>`: Searches items inside the Web Cash Shop, listing their prices, categories, and direct purchase links.
* `/mysterious-shop`: Shows the active rewards rotation, item prices, item grades (with grade-specific icons), and a relative countdown to the next rotation reset (UTC 00:00), providing a direct hyperlink to the web shop.
* `/profile`: (Private response) Displays a secure summary of the player's linked web account details, including Family Name, ACoin/Pearls/Loyalty/Silver balances, playtime, and leaderboard standings.
* `/characters`: (Private response) Displays a list of the user's linked game characters, including their classes and levels.
* `/rankings <type>`: Displays live top-5 leaderboards (Wealth, Playtime, Level, Monster Kills, Life Skills, Guilds, and Red Battlefield).

#### 2. Persistent Live Timers Channel

A message in a dedicated channel is updated automatically every minute, showing:

* **Server Status:** Active status of all sub-servers and maintenance state.
* **Active Players:** Real-time count of active players online.
* **Next World Boss:** Dynamic countdown to the upcoming boss spawn.
* **Day/Night Cycle:** Dynamic countdown to the next day/night shift and the current in-game time.
* **Loot Events:** Current trash loot multiplier events active on specific sub-servers with relative end countdowns.
* **RBF Bonuses:** Active Red Battlefield reward multipliers (Silver and Pearls).
* **Cash Shop Discounts:** Active Pearl Shop category discounts.
* **Donation Cash Bonuses:** Active web shop donation promotions.

#### 3. Dynamic Auto-Responder (FAQ Helper)

The bot monitors chat channels and matches user questions using customizable regex patterns. When matched, it responds with a localized embed message in English, Russian, or Turkish:

* **Filters:** Configuration rules can ignore or allow specific channels, users, and roles.
* **Cooldowns:** Category-based cooldowns prevent spam.
* **Dynamic Variables:** Embed messages dynamically fetch live data using placeholders (e.g. `{Status.State}`, `{Status.OnlinePlayers}`, and `{Status.SubServers}`).

#### 4. Automated Server Broadcasts & Alerts

The bot listens to system event streams and automatically posts structured updates to specific Discord channels:

* **World Boss Spawn Alerts:** Custom embeds containing the boss name, drop information links, thumbnail icons, and customizable role pings minutes before the boss spawns.
* **Maintenance & Server Status Alerts:** Real-time alerts when the server goes under maintenance or sub-servers change status.
* **Announcements & Patch Notes:** Automatically posts new website announcements or patch notes with details and links.
* **New Redeem Codes:** Broadcasts new coupon/redeem codes to `@everyone`.
* **Event Changes:** Announces when loot events, cash shop promotions, custom events, or weekend boosts change.
* **Launcher Updates:** Automatically broadcasts when a new client launcher version is released.

#### 5. Launcher & Update Integrations

* **Launcher Gateway Integration:** The Discord bot client is integrated with the game launcher update gateway to broadcast launcher version changes.
* **Patch Broadcasting:** Structured patch updates are posted to the configured updates channel, pinging a subscription role when a new patch is published.
* **Urgency-Based Embed Colors:** The color of the embed reflects the update urgency:
  * *Emergency:* Red
  * *Maintenance:* Orange
  * *Warning:* Yellow
  * *Info/Standard:* Blue, Green, or Standard
* **Admin Controls & Shutdown Notices:** Administrators can configure ignore settings. The bot broadcasts game shutdown notices during server maintenance windows.

### Codex Special Features

The official database (Codex) includes several custom features to assist players:

* **NPC & Pearl Shop Loading:** Displays NPC locations and Pearl Shop details directly on item pages.
* **Value Estimations:** Provides estimated values for boxes, recipes, exchanges, drops, and quest rewards.
* **Localization:** Supports website translations in Chinese and Portuguese.
* **Patreon & Boosty Integration:** Allows players to link Patreon or Boosty accounts to their profile for automatic account crediting.

### Client UI & Custom Settings

The game client features unique UI elements and customizable options:

* **Character Customization:** Players can customize characters post-creation using the in-game interface.
* **Hidden Permanent Buffs:** Permanent login buffs are active and hidden until the year 2059.
* **FPS Slider:** An in-game slider allows players to adjust and lock their frame rates.
* **Loot Acquired Widget:** A filter system allows players to customize which items appear in the loot acquisition feed.
* **Custom Interaction Hotkeys:**
  * `Delete` + `Left-click`: Instantly deletes the selected item from the inventory.
  * `Middle-click`: Displays the database item key.
  * `Shift` + `Left-click`: Opens the selected item page directly in the in-game Codex database browser.
