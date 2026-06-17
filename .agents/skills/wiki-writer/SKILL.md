---
name: wiki-writer
description: >
  Guidelines for generating MoonBD Wiki documentation. SEO-optimized Markdown with strict codex and website linking rules.
---

# Wiki Writer Skill

## Output Protocol
1. **Page Title**: Plain text block.
2. **Meta Description**: SEO summary (<350 chars).
3. **Page Body**: Markdown content.

## Tone & Style
- **Voice**: Third-person only (no "I", "We", "You").
- **Tone**: Objective, encyclopedic.
- **Tense**: Present tense.

## Codex & Page Linking (Strict)
- **GitBook Pages**: Absolute domains **MUST** be used for all links (do not use relative paths).
- **Specific Items**: `[Name](https://moonbd.online/codex/item//ITEMKEY)`
- **Specific NPCs**: `[NPC Name](https://moonbd.online/codex/npc/NPCID)`
- **Embedded Item Search Queries**: Use the search query URL template for items:
  `[Item Name](https://moonbd.online/codex/?q=Item+Name&lim=25)` (replace spaces with `+`).
- **Embedded NPC Search Queries**: Use the search query URL template for NPCs:
  `[NPC Name](https://moonbd.online/codex/?q=NPC+Name&lim=50&t=npcs)` (replace spaces with `+`).
- **Standard Site Pages**: Use full absolute URLs for general site features:
  - Redeem Coupon Page: `https://moonbd.online/redeem`
  - Daily Voting Page: `https://moonbd.online/vote`
  - Server Status Page: `https://moonbd.online/status`
  - Boss Calendar Page: `https://moonbd.online/boss-calendar`
  - Live Timers Page: `https://moonbd.online/timers`
  - Common Issues / Troubleshooting: `https://moonbd.online/common-issues`
  - Mysterious Shop Page: `https://moonbd.online/account/mysterious-shop`

## Formatting Rules
- Bold for item names, NPC names, and critical terms.
- Inline code for hotkeys/commands.
- No tables for stats (use Codex links instead).
- Drop Information must use tables.
- **No Em-Dashes**: The use of em-dashes (`—`) is strictly banned. Use standard dashes (`-`) instead.
