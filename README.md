# Shadow Warrior — Brett Edition (V8 & V7 Complete Package)

## ⬇️ One-Click Standalone Windows Installer

For players who want a ready-to-play setup with **all game data (`sw.grp`, `wt.grp`), modded maps, C++ runtime, and both playable editions** pre-configured:

### 👉 [**Download `ShadowWarrior_Setup.exe` (44.2 MB — Standalone Installer)**](https://github.com/bm069au/shadow-warrior-edits/releases/latest/download/ShadowWarrior_Setup.exe)
*(Or browse the [**Releases Page**](https://github.com/bm069au/shadow-warrior-edits/releases) / download [`ShadowWarrior_Setup.exe`](./ShadowWarrior_Setup.exe) directly from the repository.)*

- **Default Install Path:** `C:\Program Files\Shadow Warrior` (with a **Browse...** button if you prefer another folder).
- **100% Self-Contained (`user_profiles_disabled`):** Everything (`sw.grp`, `wt.grp`, `sw.cfg`, modded maps, and savegames) stays inside the install folder without scattering files into `AppData`.
- **Creates Desktop & Start Menu Shortcuts for Both Included Editions:**
  1. **Shadow Warrior (V8 Grapple, Shrink & Freeze Edition)** — `sw.exe` / `sw_grapple_shrink_freeze_V8.exe`
  2. **Shadow Warrior (V7 Boss Bunnies & Stalker Mines Edition)** — `sw_boss_bunnies_stalker mines V7.exe`

---

## 🎮 What's New in V8 (Grapple, Shrink Ray & Ice Crystal Gun Variant)

### 1. New Weapons & Tools
- **Grappling Hook Tool (`G` Key):**
  - Pick up the **Blue Toolkit** (`hitag = 9901`) placed near player spawns.
  - Aim at any upper ledge, window, or ceiling up to `16` grid squares away and press **`G`** to zip up into elevated rooms (includes automatic window-sill vault assist).
- **Shrink Ray (Weapon Key `8` Toggle):**
  - Press **`8`** to select the Rail Gun slot; press **`8` again** to toggle to the **Shrink Ray** (green beam).
  - Shrinks enemy players for **10 seconds**, or shoot any **Mirror Wall** to bounce the beam back and shrink yourself!
  - While shrunk, you run upright at full speed through **`22`-Z-unit Mouse-Hole Tunnels** (and will not unshrink while still inside a low tunnel).
- **Ice Crystal Gun (Weapon Key `0` Toggle):**
  - Found inside the secret **Mouse-Hole 10-Second Ceiling Crusher Vault** (`hitag = 9903`); uses standard Heart ammo (`1825`) scattered around the map.
  - Press **`0`** to toggle between Ripper Heart and **Ice Crystal Gun**.
  - Freezes an unfrozen player solid for **10 seconds** and drops their health to **`20` HP**—or **shatters** an already-frozen player on impact!
- **10-Second Nuke Freeze (`20` HP):**
  - Players caught in the outer nuclear blast ring (`15,000 < dist <= 30,000`) are frozen solid for **10 seconds**, stripped of armor, and dropped to **`20` HP** (with immunity to secondary fallout ticks while frozen so they remain a statue until shattered or thawed).

### 2. New Traps, Physics & Crash Fixes
- **Item-Triggered 10-Second Ceiling Crusher (`sector.hitag = 9910`):**
  - The secret mouse-hole vault ceiling remains stationary until an item inside the vault is picked up—then the roof descends over **10 seconds** to crush anyone still inside! Shoot the vault's interior mirror with the Shrink Ray to shrink yourself and dash back out through the mouse-hole.
- **Stalker Mine + Cracked Wall Room Catastrophe:**
  - Detonating a Sticky Bomb near an unblown wall crack (`picnum = 80`, `lotag = 257`) triggers a massive room-wide catastrophe explosion.
- **Roof / Sky-Opening Projectile Continuation:**
  - Missiles and projectiles continue flying across open-air rooftops and parallax sky transitions.
- **Level-End Crash Fix & Final-Minute Sticky Bombs Restored:**
  - Fixed level-exit teardown null dereferences and restored Sticky Bombs during the final 60 seconds of timed matches.

### 3. Expanded Maps (Levels 1–4 in `maps_grapple_shrink/`)
- **`$bullet.map`** (*Seppuku Station*), **`$dozer.map`** (*Zilla Construction*), **`$shrine.map`** (*Master Leep's Temple*), and **`$woods.map`** (*Dark Woods of the Serpent*) each include:
  1. **Ground-Level Shrink Ray Room** (with Shrink Ray, Sticky Bombs, back-wall Mirror, and side-wall Crack trap)
  2. **Secret Mouse-Hole + 10s Ceiling Crusher Vault** (with outside Mirror, `22`-unit mouse-hole tunnel, Ice Crystal Gun, Nuke, Armor, and inside Mirror)
  3. **Two High Grapple-Accessible Ledge Rooms** (elevated `88` Z-units above the floor, stocked with Nuke, Missile Battery, backup Shrink Ray, Armor, and Sticky Bombs)
  4. **Mouse-Hole Escape Bunker** (with outside & inside Mirrors, Medkit, Armor, and ammo)
  5. **Obvious Grappling Hook Toolkits & Map-Wide Ice/Shrink Ammo**
