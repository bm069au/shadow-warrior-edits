# Shadow Warrior 1997 — Brett's Multiplayer Mod

A Windows 10/11 mod build of the JFSW Shadow Warrior source port, created for chaotic multiplayer (*WangBang*) matches with nuclear grenades, dangerous bunnies, Stalker Mines, and (in the experimental V8 branch) ported *Duke Nukem 3D* weapons and tactical multiplayer map expansions.

---

## ⚠️ Important Notice for Anyone Who Downloaded Between Oct 26 – Nov 2, 2026

**We had a packaging and folder-isolation mistake in our initial V8 pre-release upload and installer. If you downloaded the repo or ran `ShadowWarrior_Setup.exe` during that window and your game looked corrupted, here is what happened and how to fix it:**

1. **What went wrong:**
   - The earlier `ShadowWarrior_Setup.exe` installer placed **V7 (Boss Bunnies + Stalker Mines)** and **V8 Beta (Grapple/Shrink/Freeze)** into the same folder alongside loose V8 map overrides (`$bullet.map`, `$dozer.map`, `$shrine.map`, `$woods.map`) and custom art (`TILES022.ART`).
   - Because the JFSW engine automatically loads any loose `.map` and `.ART` files found in its working directory or in `%APPDATA%\JFShadowWarrior`, running V8 caused V7 (and existing *Shadow Warrior* installs) to load V8's modified maps, mirror textures, and configuration files.
   - In addition, the `main` branch `README` previously described V7 while the V7 source commits were still sitting unmerged on the `stalker-mines-test` branch.
2. **How to fix an affected install in 30 seconds:**
   - **Never mix two versions in one folder.** Keep **V1.0 (Bunny Apocalypse)**, **V7.0 / V7.2_brett (Boss Bunnies + Stalker Mines)**, and **V8.0 Beta** in **separate subdirectories**, each containing its own copy of `SW.GRP`, `sw.cfg`, and an empty file named `user_profiles_disabled` (now included in `jfsw/user_profiles_disabled`, which instructs JFSW to use the local directory instead of `%APPDATA%\JFShadowWarrior`).
   - If your V7 or original *Shadow Warrior* game shows broken mirrors or V8 rooms, delete any loose `$bullet.map`, `$dozer.map`, `$shrine.map`, `$woods.map`, and `TILES022.ART` from your V7 folder and from `C:\Users\<YourName>\AppData\Roaming\JFShadowWarrior`.

---

## 🎮 Distinct Versions, Branches & Tags (Every Iteration Preserved)

To ensure no version ever overwrites an earlier version, every major edition and iteration is preserved on its own Git branch/tag and must be run in its own separate folder:

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
3. **Launch from that folder's working directory** (and ensure the `SWGRP` environment variable is not pointing to another directory).

---

## 📜 Source and Licence

The Shadow Warrior source-port code is provided under the GNU GPL; the licence is in [`jfsw/GPL.TXT`](jfsw/GPL.TXT).
