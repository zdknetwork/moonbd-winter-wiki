# MoonBD Wiki - Agent Instructions

This document outlines the core coding, style, and content standard guidelines for agentic AI workflows collaborating on the MoonBD Wiki repository. All modifications to the wiki must adhere strictly to these principles.

---

## 1. Core Philosophy

* **Concise & Informative:** Keep all wiki pages short, focused, and high-density. Avoid writing long paragraphs of descriptive text or basic game mechanics.
* **No Bloat:** Do not duplicate information that is dynamically updated or natively available in-game or on the database.
* **Strict Categorization:** Maintain a clear and clean directory structure. Use minimal subdirectory `README.md` files (index pages), as GitBook handles subpage navigation automatically.

---

## 2. Rule on Recipes, Drops & NPC Shop Data

> [!IMPORTANT]
> **Never list recipes, box contents, NPC shop inventories, exchange lists, or drop tables manually on the wiki.**
>
> All recipes, drops, and NPC shop data are dynamically managed and available on the official database. Instead of listing them on the wiki, remove the tables/lists entirely and replace them with direct **MoonBD Codex** database links.

---

## 3. Codex & Page Linking Protocols

* **GitBook Pages:** Use absolute URLs for all external links, and standard GitBook page paths for internal wiki links. Do not use raw relative paths.
* **Specific Items:** Bold the item name and link using the double-slash syntax:
  `[**Item Name**](https://moonbd.online/codex/item//ITEMKEY)` (e.g. `[**Caphras Stone**](https://moonbd.online/codex/item//721003)`)
* **Specific NPCs:** Bold the NPC name and link using the single-slash NPC details syntax:
  `[**NPC Name**](https://moonbd.online/codex/npc/NPCID)` (e.g. `[**Nemos**](https://moonbd.online/codex/npc/900995)`)
* **Search Queries (Unknown IDs):** If the exact ID is unknown, link to the search query instead:
  * Items: `[**Item Name**](https://moonbd.online/codex/?q=Item+Name&lim=25)`
  * NPCs: `[**NPC Name**](https://moonbd.online/codex/?q=NPC+Name&lim=50&t=npcs)`

---

## 4. Tone, Style & Grammar

* **Voice:** Third-person objective only. Do not use first-person ("I", "We") or second-person ("You").
* **Imperatives:** Banned. Do not write instructions in the imperative mood (e.g., replace "Go to Moon Master and buy the token" with "Players can purchase the token from the Moon Master NPC shop").
* **Tense:** Present tense.
* **Formatting:** Bold all item names, NPC names, and critical terms. Use inline backticks for hotkeys or console commands.
* **Banned Characters:** Em-dashes (`—`) are strictly banned. Use standard hyphens (`-`) instead.

---

## 5. Official Website Domains & Route Map

When linking to official services or UI routes, agents must use the absolute domain mappings below.

### Service Domains
* **Main Website:** `https://moonbd.online`
* **API Service:** `https://api.moonbd.online`
* **CDN Assets:** `https://cdn.moonbd.online`
* **Launcher Storage:** `https://launcher-bucket.moonbd.online`
* **Official Discord:** `https://discord.gg/3xK6p7rhD4`

### Absolute Page Route Mappings
* **Home Page:** `https://moonbd.online/`
* **Rules & Policies:** `https://moonbd.online/rules`
* **Terms of Service:** `https://moonbd.online/terms`
* **Privacy Policy:** `https://moonbd.online/privacy`
* **Voting Page:** `https://moonbd.online/vote`
* **Redeem Coupon Page:** `https://moonbd.online/redeem` (or `/redeem-codes`)
* **Account Transfer Page:** `https://moonbd.online/transfer`
* **Server Status:** `https://moonbd.online/status`
* **Donations Page:** `https://moonbd.online/donations`
* **Boss Spawn Calendar:** `https://moonbd.online/boss-calendar`
* **Live World Timers:** `https://moonbd.online/timers`
* **Common Issues / FAQ:** `https://moonbd.online/common-issues`
* **Game Installation Guide:** `https://moonbd.online/installation`
* **Web Central Market:** `https://moonbd.online/market`
* **Player / Guild Rankings:** `https://moonbd.online/ranking`
* **Announcements / News:** `https://moonbd.online/announcements`
* **Patch Notes:** `https://moonbd.online/patch-notes`
* **Codex Database Search:** `https://moonbd.online/codex`
* **Feedback Submission:** `https://moonbd.online/feedback`
* **Grind Sessions Tracker:** `https://moonbd.online/grind-sessions`

### Authenticated Account Portal Mappings
* **User Profile:** `https://moonbd.online/account/profile`
* **Account Settings:** `https://moonbd.online/account/settings`
* **Shop Inventory / Purchases:** `https://moonbd.online/account/shop`
* **Character Directory:** `https://moonbd.online/account/characters`
* **Mysterious Shop:** `https://moonbd.online/account/mysterious-shop`
* **Account Transaction History:** `https://moonbd.online/account/history`
