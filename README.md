# 📦 VCompressor

<div align="center">

[![Minecraft Version](https://img.shields.io/badge/Minecraft-1.20%20%2F%201.21-blue.svg)](https://papermc.io/)
[![Plugin Version](https://img.shields.io/badge/Version-1.0.0-green.svg)]()
[![Platform](https://img.shields.io/badge/Platform-Paper%20%2F%20Spigot%20%2F%20Purpur-orange.svg)]()
[![Java](https://img.shields.io/badge/Java-17%2B-red.svg)]()
[![PlaceholderAPI](https://img.shields.io/badge/Supports-PlaceholderAPI-yellow.svg)]()

**A high-performance, fully GUI-driven item compression plugin for modern Minecraft networks.**

*Built for Lifesteal, Skyblock, Survival and economy-driven servers.*

</div>

---

## 🚀 About The Project

**VCompressor** lets players compress massive amounts of raw items and blocks into compact, higher-value forms — automatically and without any lag. Admins can create, edit, rename and delete compression recipes **entirely in-game** through an intuitive GUI dashboard. No config file editing, no server restarts.

Designed from the ground up for heavy network setups:

* ⚡ **Zero-lag compression engine** — runs on configurable tick loops, split by VIP / normal speed tiers.
* 💾 **Data saver system** — all player progress is stored safely and restored after restarts.
* 🔒 **Obfuscated builds** — public releases are fully obfuscated to protect the source.

---

## ✨ Features

### 🎮 Player Experience
* **📂 Personal Compressor GUI** — a paginated menu showing every compressor, its lock status and on/off state.
* **⚡ Auto-Compression** — toggle once, and the plugin compresses your inventory on its own in the background.
* **📜 Voucher Books** — unlock new compressors by right-clicking special in-game books.
* **🏆 Live Stats** — track your total compressed items, unlocked compressors and active compressors in the GUI.
* **👑 VIP Speed Tiers** — players with the VIP permission compress up to **3× faster** (configurable).

### 🛠️ Admin Dashboard
* **✏️ In-Game Recipe Editor** — place an *Input*, *Output* and *Unlock Book* into dedicated slots and save. That's it.
* **🗑️ Safe Deletion** — right-click any compressor to delete it, with a confirmation menu and **automatic backups**.
* **✎ Rename System** — rename any compressor via command without touching YAML files.
* **🎁 Voucher Book Giveaway** — hand out unlock books to any online player instantly.
* **🔄 Hot Reload** — reload configuration and recipes with one command, zero downtime.
* **⌨️ Smart Tab-Completion** — full tab suggestions for subcommands, player names and compressor IDs.

### 🔌 Integrations
* **PlaceholderAPI** — 4 live placeholders ready for your scoreboard, tab, chat or join messages.
* **Automatic Backups** — the last 10 versions of your compressor data are always kept.

---

## 📥 Installation

1. Download the latest `.jar` from the **[Releases](../../releases)** section.
2. Drop it into your server's **`plugins`** folder.
3. Restart the server (or use PlugMan to hot-load it).
4. Optionally install **[PlaceholderAPI](https://www.spigotmc.org/resources/placeholderapi.6245/)** for placeholders.
5. Done! Create your first compressor with `/compressadmin`.

> Requires **Minecraft 1.20+** and **Java 17 or newer**. Works on Paper, Purpur and Spigot.

---

## 📋 Commands

| Command | Description | Permission |
| :--- | :--- | :--- |
| `/compressor` | Opens your personal compressor menu | `compress.use` |
| `/compressadmin` | Opens the admin dashboard (recipe editor) | `compress.admin` |
| `/compressadmin reload` | Reloads config, recipes & speed settings | `compress.admin` |
| `/compressadmin givebook <player> <id>` | Gives a Voucher Book to a player | `compress.admin` |
| `/compressadmin rename <id> <name>` | Renames a compressor | `compress.admin` |

Full tab-completion is supported for all subcommands, online player names and compressor IDs.

## 🔐 Permissions

| Permission | Description | Default |
| :--- | :--- | :--- |
| `compress.use` | Open the compressor GUI | Everyone |
| `compress.vip` | Unlock the faster VIP compression speed | OP |
| `compress.admin` | Full access to the admin dashboard & commands | OP |

## 🏷️ Placeholders (PlaceholderAPI)

| Placeholder | Returns |
| :--- | :--- |
| `%vcompressor_unlocked%` | Number of unlocked compressors |
| `%vcompressor_active%` | Number of currently active compressors |
| `%vcompressor_total_compressed%` | Total items compressed by the player |
| `%vcompressor_toggle%` | Auto-compress status (`ON` / `OFF`) |

---

## ⚙️ Configuration

After the first run, `config.yml` is generated automatically:

```yaml
speeds:
  vip-ticks: 5      # VIP compression interval (20 ticks = 1 second)
  normal-ticks: 15  # Normal compression interval
```

Compressor recipes and player data are stored safely under `plugins/VCompressor/`:

```
plugins/VCompressor/
├── config.yml
└── data/
    ├── compressors.yml    # All recipes (input → output → unlock book)
    ├── playerdata.yml     # Every player's progress & stats
    └── backups/           # Last 10 automatic backups
```

---

## 💡 How It Works

1. **Admin** opens `/compressadmin` and creates a recipe in the GUI — e.g. `64x Cobblestone → 1x Compressed Cobblestone`.
2. **Players** unlock the compressor using its **Voucher Book**, then toggle it ON in `/compressor`.
3. The engine automatically scans their inventory at the configured speed and converts matching items.
4. Progress, stats and unlocks are saved automatically — even after a crash or restart.

---

## 🖼️ Screenshots

> 📸 Coming soon — the GUI, admin dashboard and recipe editor in action.

---

## ❓ FAQ

<details>
<summary><b>Is the source code available?</b></summary>

No — the source code for VCompressor is **private**. Public builds are obfuscated.
</details>

<details>
<summary><b>Can I use this on multiple servers?</b></summary>

Contact us for network / multi-server licensing.
</details>

<details>
<summary><b>Does it work with version X?</b></summary>

Built and tested for **1.20+**. For other versions, reach out via Discord or email.
</details>

<details>
<summary><b>Will it lag my server?</b></summary>

No — compression runs on lightweight scheduled tasks, and all data operations are cached in memory with periodic saves.
</details>

<details>
<summary><b>Where is player data stored?</b></summary>

In `plugins/VCompressor/data/playerdata.yml`. It persists across restarts and is only saved when a player quits or the server shuts down.
</details>

---

## 🛠️ Support & Custom Development

Want a **custom version**, special features for your network, or direct setup assistance?

* **📧 Email:** [mdismohammad6@gmail.com](mailto:mdismohammad6@gmail.com)
* **💬 Discord:** [Join our Discord Server](https://discord.gg/36f6PN6XT)

---

## 📄 License

All rights reserved. Redistribution, resale, decompilation or modification of the plugin is **not permitted** without written permission from the author.

<div align="center">

**Made with ⚡ by Mohammadvirus**

<i>Copyright © VCompressor. All rights reserved.</i>

</div>
