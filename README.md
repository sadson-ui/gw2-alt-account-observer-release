# Alt Account Observer

Alt Account Observer is a Nexus addon for **Guild Wars 2**. It brings item search, account storage, currencies, Trading Post information and Wizard's Vault progress together in one in-game window. You can configure multiple API keys and give each account an optional custom display name

## Features

- **Search across storage:** Search an account's inventory, bank, material storage, shared inventory, character bags and equipped gear. The All Accounts view combines item results across configured API keys
- **Separate storage views:** Inspect account items, bank and material storage, wallet currencies, Trading Post data, Wizard's Vault information, or an individual character
- **Multiple accounts:** Add several API keys, view accounts in separate tabs, and optionally assign a custom name to each one
- **Wallet:** View currencies and Astral Acclaim for an individual account. Sort the currency table by name or amount
- **Trading Post:** View pickup items and coins, open buy orders, open sell orders, and market listings for relevant items. Market data is fetched on demand. In All Accounts, the pickup view is grouped by account
- **Wizard's Vault:** View daily, weekly and special objectives, progress, claim status and reward listings. The All Accounts view groups Vault data by account. Objective and reward tables can be sorted by clicking their column headings (Daily data only available after login)
- **Manual refresh controls:** Use the main refresh for the full account data. Wallet, Wizard's Vault and Trading Post also have dedicated refresh buttons, so those sections can be refreshed independently
- **Character views:** Browse characters in a compact selector and see profession and elite specialization icons
- **Item details:** Tooltips can show item rarity, level, stats, weapon strength, defense and relevant gear upgrades
- **German and English interface**, configurable text sizes, Nexus toolbar access and a configurable keybind

## Installation

1. Install the [Nexus addon loader](https://raidcore.gg/Nexus) for Guild Wars 2
2. Download `nexus_alt_account_observer.dll` from the project's Releases page
3. Place the DLL in your Guild Wars 2 `addons` folder
4. Launch the game. The addon appears in the Nexus Quick Access bar

## Setup

Create an API key in the [ArenaNet API Key Manager](https://account.arena.net/applications) and add it in the Alt Account Observer settings. You can add multiple keys and assign an optional custom name to each account

Required permissions for the main account search:

- `account`
- `inventories`
- `characters`

Optional permissions enable additional data:

- `builds` — detects the active elite specialization for characters
- `unlocks` — enables legendary armory data where available
- `wallet` — enables account wallet currencies and Astral Acclaim
- `progression` — enables Wizard's Vault objectives and rewards
- `tradingpost` — enables Trading Post pickup data and open transactions

The public Trading Post market listings endpoint does not require an API key. The addon requests listings only for relevant item IDs, rather than downloading the full listings catalogue

## Using refresh buttons

- The main **Refresh** action updates the selected account's main data. **Refresh all** updates the configured accounts
- The Wallet refresh updates only the selected account's wallet
- The Wizard's Vault refresh updates only the selected account's Vault data. In All Accounts, its refresh action updates Vault data for all configured accounts
- The Trading Post refresh updates pickup and transaction data. Its All Accounts refresh updates pickup data for each configured account
- Market listings are fetched when requested and are limited to items shown in Trading Post data

The `/v2/commerce/delivery` endpoint provides items and coins ready to collect from the Trading Post. It does **not** provide access to the regular in-game mailbox.

## Privacy and local data

API keys and cached data are stored locally by the addon. Do not share your settings file because it may contain API keys

## Credits

- Author: **[utz]**
- Built on the [Nexus](https://raidcore.gg/Nexus) addon framework by Raidcore
- Account and game data are provided by the official [Guild Wars 2 API](https://wiki.guildwars2.com/wiki/API:Main)

> Readme created by AI. Addon creator was too lazy for it.

> *Guild Wars 2 and all associated trademarks are property of ArenaNet / NCSoft. This is an unofficial, fan-made addon.*
