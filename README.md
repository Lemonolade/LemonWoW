# 🍋 LemonWoW

**World of Warcraft 3.3.5a (Wrath of the Lich King) repack for Windows**
Made by **Lemonolade**, with help from Claude AI. Current version: **1.1** ([what's new](../../releases/latest))

LemonWoW is a ready-to-run private server for your own PC, built on [AzerothCore](https://www.azerothcore.org) with [Playerbots](https://github.com/mod-playerbots). The world is full of AI-controlled players (bots) who quest, group with you for dungeons and fill the world.

No Docker, no Linux, no installers: unzip, double-click, play.

## ⬇️ Download

Get **`LemonWoW.zip`** from the [latest release](../../releases/latest).
The source code used to build it (`LemonWoW-source.zip`) is attached to the same release.

You also need your own **WoW 3.3.5a client (build 12340)**. It is not included.

## ✨ Features

- **Playerbots** - 200 AI players by default (adjustable), they join your Dungeon Finder groups
- **Solo LFG** - queue for dungeons alone; after 60 seconds bots fill the group
- **AutoBalance** - dungeons and raids scale to your group size
- **AH Bot** - a stocked auction house
- **Transmog**, **MorphSummon**, **Individual XP** (1x-10x), **AoE Loot**
- **1v1 Arena**, **Top Arena**, **Low Level Random BG** (from level 10), **PvP Titles**, **Duel Reset**
- **Instance Reset**, **Skip DK Starting Area**, **No Hearthstone Cooldown**
- **Weather Vibe**, **Weekend Bonus**, **Boss Announcer**, **Breaking News**
- **Optional AI:** bots that chat with personalities, and your own AI buddy bot (needs [Ollama](https://ollama.com) and a GPU). Since 1.1 the AI chat can also use OpenAI-compatible services or Anthropic (Claude) instead

Special NPCs (Transmogrifier, pet morphs, 1v1 Arena, Instance Reset, Top Arena) stand in both **Orgrimmar** and **Stormwind**.

## 🚀 Quick start

1. Unzip `LemonWoW.zip` anywhere (avoid *Program Files*).
2. Double-click **`Start LemonWoW.bat`**. In the Worldserver window, wait for `ready...` and for the bots to finish logging in (`200/200`), then give it 10-20 seconds.
3. In the Worldserver window, create your account:
   ```
   account create YOURNAME YOURPASSWORD
   account set gmlevel YOURNAME 3 -1
   ```
4. Set `Data\enUS\realmlist.wtf` in your WoW folder to:
   ```
   set realmlist 127.0.0.1
   ```
5. Start WoW and log in.

**To stop:** type `server shutdown 1s` in the Worldserver window, then run **`Stop LemonWoW.bat`**.

If the servers won't start, install the [Microsoft Visual C++ Redistributable (x64)](https://aka.ms/vs/17/release/vc_redist.x64.exe).

The full guide - playing with friends over Radmin VPN, bot counts for your PC, settings, the AI buddy, every command and troubleshooting - is in **`README.txt`** inside the zip.

## 💻 Requirements

| | |
|---|---|
| OS | Windows 10 / 11, 64-bit |
| Disk | about 6 GB |
| Ports | 3306, 3724, 8085 (don't run another WoW server or MySQL at the same time) |
| Bots | 50 for older PCs, 200 for an average gaming PC, 500+ for strong PCs |
| AI modules (optional) | NVIDIA GPU with 8 GB VRAM or more |

## 🛠️ Source and changes

LemonWoW is built from [AzerothCore (Playerbot branch)](https://github.com/mod-playerbots/azerothcore-wotlk) and its modules with a few small changes:

- [`LEMONWOW-CHANGES.txt`](LEMONWOW-CHANGES.txt) - what was changed and why
- [`lemonwow-patches/`](lemonwow-patches) - the exact changes as `.diff` files
- [`BUILDING.txt`](BUILDING.txt) - how the Windows build was made

The complete source is `LemonWoW-source.zip` in the [releases](../../releases/latest).

## 📜 Credits and licenses

Built on [AzerothCore](https://www.azerothcore.org), [mod-playerbots](https://github.com/mod-playerbots) and the work of every module author, plus MySQL, OpenSSL, curl and Boost.
AzerothCore and most modules are free software under the GNU GPL or AGPL; each component keeps its own license file in the source download.

World of Warcraft is a trademark of Blizzard Entertainment. LemonWoW is a fan project, not affiliated with Blizzard, and does not include the game client.
