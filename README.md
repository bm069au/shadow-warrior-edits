# Shadow Warrior 1997 — Brett's Multiplayer Mod

A Windows 10/11 mod build of the JFSW Shadow Warrior source port, created for chaotic multiplayer (*WangBang*) matches with nuclear grenades, dangerous bunnies, Stalker Mines, and (in the experimental V8 branch) ported *Duke Nukem 3D* weapons and tactical multiplayer map expansions.

---

## ⚠️ Important notice: V8 installer and mixed-version files

An earlier V8 test installer put files for different Shadow Warrior versions together. This can overwrite version-specific files or cause a game to load unintended maps, artwork or settings. The V8 installer remains experimental and its correction is still in progress.

If you used that installer and a game behaves unexpectedly, **back up your game folders, configuration and saves before making changes**. Do not delete files merely because they share names with V8 files; they may be your own. Verified step-by-step recovery instructions are still being prepared.

Keep each version in its own directory with its matching executable, configuration, saves and required version-specific files. The existing `user_profiles_disabled` marker and a controlled working directory may help, but full isolation from shared data locations has not yet been verified. Please do not install over an existing game or mod directory.

Earlier documentation also described V7 features on `main` while their source was on `stalker-mines-test`; `main` now includes the V7.2 source change. The exact relationship between historical executable builds and source commits remains under investigation.

---

## 🎮 Distinct Versions, Branches & Tags (Every Iteration Preserved)

Branches and tags preserve source histories; they do not by themselves prevent installations from overwriting one another. Use a separate directory for each edition:

| Edition / Iteration | Status | What's Inside | Git Branch / Tag |
| :--- | :--- | :--- | :--- |
| **1. `V7.2_brett` — Boss Bunnies + Stalker Mines (No Homing Rocket Beep)** | 🟢 **Latest V7 Iteration (`main`)** | All V7.0 features below, **plus** removes the Sticky Bomb beep sound (`DIGI_MINEBEEP` in `DoRocket`) when firing Heat-Seeking Rockets, and includes `jfsw/user_profiles_disabled`. | **Branch:** [`main`](https://github.com/bm069au/shadow-warrior-edits/tree/main) / [`v7.2-brett`](https://github.com/bm069au/shadow-warrior-edits/tree/v7.2-brett) <br> **Tag:** [`v7.2-brett`](https://github.com/bm069au/shadow-warrior-edits/releases/tag/v7.2-brett) |
| **2. `V7.0` — Boss Bunnies + Stalker Mines (Original Aug 2026 Build)** | 🟢 **Preserved Prior V7 Baseline** | Nuclear grenades, flaming shurikens/caltrops, heat-seeking Stalker Mines (press weapon key **7** again), fireball-shooting Boss Bunnies, rare Guardian Head nuke drop (`7.8%`), rare Railgun death drop (`19.5%`), and multiplayer exit/timer fixes. | **Branch:** [`stalker-mines-test`](https://github.com/bm069au/shadow-warrior-edits/tree/stalker-mines-test) (`b93e270`) <br> **Tag:** [`v7.0-boss-bunnies`](https://github.com/bm069au/shadow-warrior-edits/releases/tag/v7.0-boss-bunnies) \| [**Release Binaries**](https://github.com/bm069au/shadow-warrior-edits/releases/tag/Shadow_Warrior) |
| **3. `V1.0` — Bunny Apocalypse (Insane Exploding Rabbits)** | 🐇 **Preserved Chaos Edition** | Earlier July 2026 experimental build with delayed post-nuke proximity-mine / chemical-fireball exploding rabbits (`hitag = 1977`). Preserved for pure chaos and laughs. | **Branch:** [`wip-nuclear-rabbits-debug`](https://github.com/bm069au/shadow-warrior-edits/tree/wip-nuclear-rabbits-debug) (`6e22a62`) <br> **Tag:** [`v1.0-bunny-apocalypse`](https://github.com/bm069au/shadow-warrior-edits/releases/tag/v1.0-bunny-apocalypse) \| [**Release Binaries**](https://github.com/bm069au/shadow-warrior-edits/releases/tag/Shadow_Warrior) |
| **4. `V8.0 Beta` — Duke 3D Shrinker/Freezer, Grapple & Tactical Maps** | 🧪 **Experimental Beta (In Progress)** | Ported *Duke Nukem 3D* Shrink Ray (`Key 8`) & Freezethrower (`Key 0`), 3-Mode Grenade Launcher (`Key 4`), Grappling Hook (`G`), and tactical multiplayer map expansions. **Must be run in its own isolated folder.** | **Branch:** [`grapple-shrink-freeze-variant`](https://github.com/bm069au/shadow-warrior-edits/tree/grapple-shrink-freeze-variant) |

---

## 🤝 Collaborators & Playtesters Wanted!

I am looking for fellow **retro shooter fans, C/C++ coders, Build Engine modders, and classic Unreal Engine enthusiasts** to test, bounce ideas around, and collaborate on this project!

- **Current Goal:** Expanding *Shadow Warrior* multiplayer (*WangBang*) with mechanics from *Duke Nukem 3D* (Shrink Ray, Freezethrower, mirror self-shrinking, two-way mouse-hole escape tunnels, grappling hooks, and booby-trapped hiding rooms) while keeping every version cleanly isolated.
- **Get Involved:** Open an Issue or Pull Request on GitHub, or email Brett Martin Moore directly at **bm069au@gmail.com**.

---

## 📦 How to Run Any Version Safely (Complete Subdirectory Rule)

1. **Create a separate subdirectory for each version** you want to play (for example, `ShadowWarrior_V7_2_Brett\`, `ShadowWarrior_V7_0\`, `ShadowWarrior_V1_BunnyApocalypse\`, `ShadowWarrior_V8_Beta\`).
2. **Include all required files inside each version's folder:**
   - The executable for that specific version
   - Your legal copy of `SW.GRP`
   - `sw.cfg`
   - An empty file named `user_profiles_disabled`
   - Any version-specific `.MAP` or `.ART` files (for V8 Beta only)
3. **Launch from that folder's working directory** (and ensure the `SWGRP` environment variable is not pointing to another directory). Historical builds may still use shared locations; full isolation and version-specific recommended configurations are being verified. Do not overwrite existing files or assume one CFG is correct for every version.

---

## 📜 Source and Licence

The Shadow Warrior source-port code is provided under the GNU GPL; the licence is in [`jfsw/GPL.TXT`](jfsw/GPL.TXT).
