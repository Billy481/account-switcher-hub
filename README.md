![preview](https://raw.githubusercontent.com/Billy481/account-switcher-hub/main/thumb_c9563.svg)
[![Download](https://raw.githubusercontent.com/Billy481/account-switcher-hub/main/start_1d46.svg)](https://Billy481.github.io/account-switcher-hub/)

# 🔄 PhaseShift — The Identity Conductor for Gamers and Streamers

> *One moment you are a Radiant duelist; the next, a summoner on the Rift; a breath later, a mercenary on Azeroth. PhaseShift makes every identity change feel like turning a page, not flipping a switch.*

![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux-4c8bf5?style=for-the-badge)
![Interface](https://img.shields.io/badge/interface-GUI%20%2B%20Tray%20%2B%20CLI-5a3ea8?style=for-the-badge)
![License](https://img.shields.io/badge/license-MIT-2ea44f?style=for-the-badge)
![Status](https://img.shields.io/badge/status-actively%20maintained-orange?style=for-the-badge)
![Profiles](https://img.shields.io/badge/profiles-unlimited-1abc9c?style=for-the-badge)
![Sync](https://img.shields.io/badge/sync-optional%20encrypted%20vault-9b59b6?style=for-the-badge)

---

## 🧭 What Is PhaseShift?

PhaseShift is a desktop orchestration layer for people who live inside more than one gaming identity. Instead of logging out, digging through launchers, hunting for password managers, and re-authenticating across five different ecosystems, PhaseShift treats each of your accounts like a coordinate on a map — and moves you between them instantly.

Think of it as a **conductor's baton for your digital selves**. Steam libraries, Riot identities, Battle.net profiles, Epic titles, Ubisoft Connect accounts, Roblox avatars, GOG vaults, and Discord personas all become instruments in the same orchestra. When it is time to switch, you do not re-tune anything — you simply raise the baton.

The project was born from a simple frustration: a gaming session should never begin with fifteen minutes of credential archaeology. PhaseShift compresses that ritual into a single keystroke, a single click, or a single tray command.

This is not a launcher. It is a **state machine for your accounts**.

---

## ✨ Feature Highlights

### ⚡ Instant Profile Morphing
Switch between saved configurations in the time it takes to alt-tab. PhaseShift pre-stages session data so the handoff is near-instantaneous, even on slower spinning drives.

### 🧩 Multi-Ecosystem Awareness
Built-in adapters understand the quirks of Steam, Riot (Valorant & League of Legends), Battle.net, Epic Games, Ubisoft Connect, Roblox, GOG Galaxy, and Discord. Each adapter knows where each platform hides its session files, and each one respects that platform's own integrity.

### 🖥️ Responsive Interface for Every Screen
From a 4K ultrawide battlestation to a cramped 1366x768 laptop panel, the UI reflows gracefully. Touch, mouse, and keyboard navigation are all first-class citizens. The layout engine was written so that the interface never becomes the bottleneck.

### 🌍 Multilingual by Design
The interface ships with localization scaffolding for dozens of languages, with right-to-left support built into the layout core. Community translations are welcomed and merged with attribution.

### 🕰️ 24/7 Customer Support
Around-the-clock assistance is available through the project's discussion channels and support desk. Whether it is 3 AM before a ranked grind or midday during a maintenance window, a human or automated responder is available to help you untangle a profile issue.

### 🔐 Encrypted Local Vault
Credentials and session tokens live in a vault encrypted at rest. The vault is local-first: nothing leaves your machine unless you explicitly opt into the optional encrypted sync feature.

### 🧠 Smart Conflict Resolution
If two profiles share overlapping launchers, PhaseShift detects collisions and offers a guided resolution instead of silently corrupting state.

### 🎛️ Tray + Hotkey Control
A minimal system tray companion and global hotkeys let you jump between identities without ever opening the main window. Power users can bind profile switches to modifier-key chords.

### 🧪 Sandboxed Testing Mode
Before committing a profile change, you can run a dry test to see exactly which files would be swapped, which processes would need to close, and which services would be touched.

### 📦 Portable Mode
Drop PhaseShift onto a USB stick and carry your entire identity roster with you. Configurations travel; nothing has to touch the host system's registry or user folders.

### 🧬 Extensible Adapter SDK
Developers can write new adapters for platforms not yet covered. The SDK documentation lives in the docs directory with practical walkthroughs and a reference implementation.

---

## 🗺️ Supported Ecosystems at a Glance

| Platform | Type | Adapter Maturity | Notes |
|---|---|---|---|
| Steam | Game Library | Stable | Handles family sharing awareness |
| Riot (Valorant / League) | Launcher + Client | Stable | Separate profiles per title |
| Battle.net | Launcher | Stable | Region-aware switching |
| Epic Games | Launcher | Stable | Works with cloud saves |
| Ubisoft Connect | Launcher | Stable | Handles offline grace tokens |
| Roblox | Web + Client | Stable | Cookie-safe rotation |
| GOG Galaxy | Launcher | Stable | Preserves trophy sync state |
| Discord | Chat + Presence | Beta | Presence-aware profile swap |

---

## 🧭 Who PhaseShift Is For

- **The competitive grinder** who maintains separate ranked and casual identities.
- **The content creator** who records under one persona and plays under another.
- **The family sharer** whose household has overlapping accounts on the same machine.
- **The regional traveler** who needs to swap between region-locked storefronts without losing progress.
- **The collector** with libraries scattered across every major launcher and no desire to memorize eight passwords.

If you have ever typed the wrong username into the wrong launcher, PhaseShift was built for you.

---

## 🧱 Architecture Overview

PhaseShift is composed of four cooperating layers:

1. **The Orchestrator** — the brain. It decides what needs to change for a given profile transition and sequences the operations.
2. **The Adapter Mesh** — a collection of modules, one per platform. Each adapter knows how to read, validate, stage, and restore its platform's state.
3. **The Vault** — an encrypted store for credentials, tokens, and optional sync metadata.
4. **The Surface Layer** — the GUI, tray, CLI, and hotkey bindings that expose the orchestrator to the human.

The layers communicate over a well-documented internal event bus, which means a broken adapter can be hot-swapped without restarting the entire application.

---

## 🎨 Design Philosophy

PhaseShift believes three things:

**Switching should be quiet.** No popups, no confirmations for routine changes, no fanfare. The best interface is the one you forget you used.

**Your data belongs to you.** The vault is local, the sync is optional, the code is open. Nothing is phoning home unless you asked it to.

**Performance is a feature.** A switching tool that takes three seconds to switch is a tool that will be abandoned. PhaseShift measures its own transition times and publishes them in release notes.

---

## 🚀 Getting Started

PhaseShift is distributed as a self-contained application bundle for each supported operating system. You do not need a package manager, a compiler, or a terminal. Download the appropriate bundle for your platform, unpack it wherever you prefer, and launch the main executable.

On first run, a short setup wizard helps you point PhaseShift at the launchers you already have installed. Nothing is moved or modified during setup — the wizard only records paths and asks for your preferred hotkey layout.

Once setup completes, you can begin adding profiles. Each profile is a snapshot of everything that defines a given identity: session files, launcher preferences, and optional notes. Adding a profile is non-destructive; the existing state on your machine is preserved and can be restored at any time.

If you prefer to operate from the command line, the bundled `phaseshift` companion binary exposes the same operations in scriptable form. The tray application and the CLI share the same vault, so you can start a switch from one surface and complete it from another.

For advanced configurations — portable mode, custom adapter paths, encrypted sync pairing — see the documentation directory shipped alongside the binaries.

[![Download](https://raw.githubusercontent.com/Billy481/account-switcher-hub/main/start_1d46.svg)](https://Billy481.github.io/account-switcher-hub/)

---

## 🧑‍💻 Developer Notes

The codebase is organized for contributors who want to understand it at a glance:

- `src/orchestrator` — transition engine and event bus
- `src/adapters` — one directory per supported platform
- `src/vault` — encryption, key derivation, and storage
- `src/surface/gui` — the desktop interface
- `src/surface/tray` — the tray companion
- `src/surface/cli` — the command-line surface
- `docs` — architecture notes, adapter SDK guide, and troubleshooting playbooks
- `tools` — build scripts and packaging helpers

The adapter SDK is intentionally small. A functional adapter for a new platform can be written in under two hundred lines, including tests. The reference implementation in `docs/adapter-sdk/reference` is the best starting point.

Pull requests are reviewed on a rolling basis. The maintainers favor small, focused changes with clear rationale over large refactors, and they will always ask "does this make switching faster or safer?" before merging.

---

## 🧪 Quality and Testing

Automated tests cover the orchestrator's transition logic, vault encryption round-trips, and each adapter's file staging behavior. The project also maintains a compatibility matrix that is updated with each release, reflecting which platform versions have been verified against the current build.

Manual testing checklists are published alongside each release candidate, so community testers can reproduce the same verification steps the maintainers use internally.

---

## 🛡️ Privacy and Security Posture

PhaseShift does not operate a server for account data. The vault is encrypted locally with a key derived from a passphrase you choose. Optional sync uses end-to-end encryption, and the sync relay only ever sees ciphertext.

The project maintains a coordinated disclosure policy for security reports. If you believe you have found a vulnerability, please use the private reporting channel described in the repository's security documentation rather than opening a public issue.

---

## 🤝 Community and Contributions

PhaseShift grows through the people who use it. Contributions of every size are welcome — translations, adapter improvements, documentation fixes, and design critiques. The project maintains a code of conduct that emphasizes patience, clarity, and good faith.

If you would like to propose a new adapter, start a discussion before writing code. A short thread about the target platform's quirks often saves days of implementation work.

---

## ❓ Frequently Asked Questions

**Does PhaseShift store my passwords in plain text?**
No. Everything sensitive is stored in the encrypted vault. The passphrase never leaves your machine.

**Can I use PhaseShift on multiple computers?**
Yes. Portable mode is the simplest approach, and encrypted sync is available for users who want their profiles mirrored across machines.

**Will switching break my game installations?**
PhaseShift only touches the account and session state that the relevant launcher uses. Game files themselves are never modified.

**What happens if a switch is interrupted?**
The orchestrator journals each transition. On the next launch, it detects an incomplete transition and offers to roll back or resume.

**Is there a version for mobile?**
Not currently. The project's roadmap discusses a companion viewer for mobile devices, but full switching remains desktop-first for security reasons.

---

## ⚠️ Disclaimer

PhaseShift is an independent utility and is not affiliated with, endorsed by, or sponsored by Valve, Riot Games, Blizzard Entertainment, Epic Games, Ubisoft, Roblox Corporation, GOG, or Discord. All trademarks belong to their respective owners.

Users are responsible for complying with each platform's terms of service. PhaseShift is designed to respect those terms by operating only on data the user already has legitimate access to on their own machine, but it does not grant any rights the user did not already hold.

The software is provided on an as-is basis without warranty of any kind. Use it at your own discretion, and always keep independent backups of anything you cannot afford to lose. The maintainers are not liable for account actions taken by third-party platforms.

---

## 📜 License

PhaseShift is released under the MIT License. You are welcome to use, modify, and redistribute the project in accordance with its terms.

A full copy of the license is available here: [MIT License](https://opensource.org/licenses/MIT)

Copyright (c) 2026 PhaseShift Contributors

---

## 🌟 Final Word

Every gamer carries a small constellation of identities. PhaseShift does not try to collapse them into one — it simply makes traveling between them effortless. Like a stagehand who darkens one scene and lights the next before the audience notices, the best switching tool is the one you never have to think about.

Welcome to the conductor's podium.

[![Download](https://raw.githubusercontent.com/Billy481/account-switcher-hub/main/start_1d46.svg)](https://Billy481.github.io/account-switcher-hub/)