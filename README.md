# Alt Account Observer

A [Nexus](https://raidcore.gg/Nexus) addon for **Guild Wars 2** that lets you search for items across your **entire account** — bank, material storage, shared inventory, every character's bags and equipped gear, and the legendary armory — all from a single in-game window.

## Features

- **Account-wide search** — type part of an item name and instantly see everywhere you own it, with stack counts.
- **All storage locations in one place:**
  - Account bank (grouped by bank tab)
  - Material storage
  - Shared inventory slots
  - Every character's bags
  - Equipped gear
- **Per-character tabs** with class/elite-spec icons and signature profession colours. Tabs are grouped by base profession, then elite specialization, so characters never appear in a random order.
- **Rich tooltips** — rarity, level, stat prefix with computed attribute values, defense/weapon strength, food/utility effects, and nested runes, sigils and infusions slotted into gear.
- **Quick access** via the Nexus toolbar icon or a configurable keybind.
- **German & English** localization (selectable in the options).
- **Local caching** of item metadata to keep things fast and reduce API calls.

## Installation

1. Install the [Nexus](https://raidcore.gg/Nexus) addon loader for Guild Wars 2.
2. Download the latest `nexus_alt_account_observer.dll` from the [Releases](../../releases) page.
3. Drop it into your `addons` folder (e.g. `…/Guild Wars 2/addons/`).
4. Launch the game — *Alt Account Observer* loads automatically and appears in the Nexus Quick Access bar.

## Setup

The addon needs a Guild Wars 2 API key to read your account.

1. Create a key at the [official ArenaNet API Key Manager](https://account.arena.net/applications).
2. Grant at least these permissions:
   - `account`
   - `inventories`
   - `characters`
   - `builds` *(optional — enables detection of the active elite specialization per character; without it characters fall back to their core profession)*
   - `unlocks` *(optional — enables searching the legendary armory; without it everything else still works, the armory is simply omitted)*
  - `tradingpost` *(optional — enables Trading Post pickup, open buy/sell orders and item-specific market listings)*
3. Open the *Alt Account Observer* options in Nexus and paste your API key.
4. Pick your language (German / English) if needed.

Your key and settings are stored locally in `addons/AltAccountObserver/settings.json`. Item metadata is cached in `addons/AltAccountObserver/items_cache.json`.

## Usage

- Click the toolbar icon or press your bound key to toggle the search window.
- Use the **Account** tab to search everything at once, the **Bank** tab for bank/material storage, a **character** tab to inspect a single character, or **Trading Post** for pickup, open orders and relevant market prices. Trading Post account data is loaded only when you manually refresh that account; market listings are fetched on demand for the item IDs present in pickup and open orders.
- Start typing to filter results live by item name.

The `/v2/commerce/delivery` endpoint reports items and coins ready for collection from the Trading Post. It does **not** provide access to the normal in-game mailbox.

## Credits

- Author: **[utz]**
- Built on the [Nexus](https://raidcore.gg/Nexus) addon framework by Raidcore.
- Item, character and account data provided by the official [Guild Wars 2 API](https://wiki.guildwars2.com/wiki/API:Main).

> Readme created by AI. Addon creator was too lazy for it.

> *Guild Wars 2 and all associated trademarks are property of ArenaNet / NCSoft. This is an unofficial, fan-made addon.*


