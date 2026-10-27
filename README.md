# Shadow Warrior 1997 — Brett's Multiplayer Mod

A Windows 10/11 mod build of the JFSW Shadow Warrior source port, made for chaotic multiplayer games with nuclear grenades, dangerous bunnies, Stalker Mines, and (in the experimental pre-release branch) ported *Duke Nukem 3D* weapons and tactical multiplayer map expansions.

---

## 🤝 Collaborators & Playtesters Wanted!

I am actively looking for fellow **retro shooter fans, C/C++ coders, Build Engine modders, and classic Unreal Engine enthusiasts** to test, bounce ideas around, and collaborate on this project!

- **Current Goal:** Expanding *Shadow Warrior* multiplayer (*WangBang*) with the best mechanics from *Duke Nukem 3D* (authentic Shrink Ray, Freezethrower, mirror self-shrinking, two-way mouse-hole escape tunnels, grappling hooks, and booby-trapped hiding rooms).
- **Long-Term Vision:** Creating a fully merged **Shadow Warrior + Duke Nukem 3D** multiplayer sandbox—and ultimately porting the combined arsenal and movement into classic **Unreal Engine**.
- **Get Involved:** Try out the builds below, open an Issue or Pull Request on GitHub, or email Brett directly at **bm069au@gmail.com**.

---

## 🎮 Choose Your Version (Stable vs. Pre-Release for Testing)

| Edition | Status | What's Inside | Where to Get It |
| :--- | :--- | :--- | :--- |
| **1. Boss Bunnies + Stalker Mines (V7)** | 🟢 **Stable & Tested (Recommended)** | The battle-tested multiplayer build played regularly. Nuclear grenades, flaming shurikens/caltrops, heat-seeking Stalker Mines, and fireball-shooting Boss Bunnies. | [**Download V7 Stable Release**](https://github.com/bm069au/shadow-warrior-edits/releases/tag/Shadow_Warrior) *(Code on [`main`](https://github.com/bm069au/shadow-warrior-edits/tree/main))* |
| **2. Bunny Apocalypse** | 🐇 **Tested / For Laughs** | Earlier experimental build with extreme bunny density; included for pure chaos and laughs. | [**Download from Stable Release**](https://github.com/bm069au/shadow-warrior-edits/releases/tag/Shadow_Warrior) |
| **3. V8: Duke 3D Shrinker/Freezer, Grapple & Tactical Maps** | 🧪 **Pre-Release for Testing (Untested / WIP)** | **New Experimental Branch!** Authentic ported *Duke Nukem 3D* Shrink Ray (`Key 8`) & Freezethrower (`Key 0`), 3-Mode Grenade Launcher (`Key 4`: Normal / Red Nuke / Ice Nuke), Grappling Hook (`G`), Linked Booby-Trap Wall Cracks, Spread-Out Secret Rooms, and 2-Way Mouse-Hole Escape Tunnels across Levels 1–4 + **Printable Tactical Map Guide**. | [**View `grapple-shrink-freeze-variant` Branch & Printable Maps**](https://github.com/bm069au/shadow-warrior-edits/tree/grapple-shrink-freeze-variant) \| [**Download V8 Pre-Release**](https://github.com/bm069au/shadow-warrior-edits/releases/tag/v8.0) |

---

## 🟢 Stable Build Details (V7 — `main` Branch)

Choose one of the Windows executables from the [Latest Stable Release (`Shadow_Warrior`)](https://github.com/bm069au/shadow-warrior-edits/releases/tag/Shadow_Warrior):

- **Boss Bunnies + Stalker Mines V7** — the main, tested, playable build.
- **Bunny Apocalypse** — extreme bunny density; included for laughs.

### What changed in V7:
- **Grenades** are nuclear weapons.
- **Caltrops and shurikens** inflict fire damage and can set players on fire.
- **Stalker Mines** are a second Stickybomb mode: press weapon key **7** again to select them. They hide after being thrown, chase an enemy that passes nearby, and detonate after a short fuse.
- **Boss Bunnies** can appear after deaths. They become larger and more dangerous after nuclear explosions, can fire fireballs, and can bite.
- **Rare drops:** Guardian Head after a nuke and the Rifle on death.
- **Multiplayer exit fix:** players can leave cleanly even if the hosting player exits first.
- **Stickybomb drops** are disabled during the final 60 seconds of a multiplayer match to avoid end-of-level timer issues.

---

## 🧪 Pre-Release for Testing Details (V8 — `grapple-shrink-freeze-variant` Branch)

Want to help test the newest features before they are finalized? Check out the [**`grapple-shrink-freeze-variant` branch**](https://github.com/bm069au/shadow-warrior-edits/tree/grapple-shrink-freeze-variant) or grab the [**V8 Pre-Release Installer**](https://github.com/bm069au/shadow-warrior-edits/releases/tag/v8.0):

- **Ported Duke Nukem 3D Shrink Ray (`Key 8`) & Freezethrower (`Key 0`):** Complete with Duke 3D art (`TILES022.ART`), tiny pumping fists when shrunk, foot-stomp squishing, 3x wall-bouncing freeze bolts, and 40 flying ice shards (`GLASSPIECES`).
- **3-Mode Grenade Launcher (`Key 4`):** Cycle between **Normal Grenades**, **Red Nuclear Grenades**, and **Cyan Ice Nuke Grenades** (10-second freeze, strips armor to `0`, drops HP to `20`). Grenades also drop through Room-Over-Room roof holes and arc over outdoor sky walls.
- **Tactical Multiplayer Map Expansions (`$bullet.map`, `$dozer.map`, `$shrine.map`, `$woods.map`):**
  - 5 spread-out rooms/tunnels per Multiplayer (*WangBang*) arena, including **2-Way Mouse-Hole Escape Tunnels** cut between separate rooms (such as inside the Grenade Launcher room in *Master Leep's Temple*), **Mouse-Hole Crusher Vaults**, **High Grapple Sniper Lofts (`G` key)**, and **Booby-Trap Wall Cracks** so campers hiding in secret rooms can be blown up from outside.
  - Includes a [**Printable Tactical Map Guide (`PRINTABLE_MAP_GUIDE.html`)**](https://github.com/bm069au/shadow-warrior-edits/blob/grapple-shrink-freeze-variant/README.md#-printable-tactical-multiplayer-wangbang-maps) showing every new room, mouse-hole tunnel, and weapon spawn.

---

## 📦 What you need

- **For the V7 Stable Executables:** Place the downloaded executable in a folder that contains your own legal copy of `SW.GRP` (for example, from GOG or Steam). `SW.GRP` supplies the original graphics, sounds, maps, and other game data.
- **For the V8 Pre-Release Standalone Installer (`ShadowWarrior_Setup.exe`):** Pre-packages the shareware/modded maps, `TILES022.ART`, Printable Map Guide, and both V7 and V8 executables into a self-contained folder (`C:\Program Files\Shadow Warrior` by default).

## 📜 Source and licence

The Shadow Warrior source-port code is provided under the GNU GPL; the licence is in [`jfsw/GPL.TXT`](jfsw/GPL.TXT). You are welcome to download, study, modify, build, and redistribute the GPL-covered code and compatible builds under that licence.

If you make something funny or useful from this fork, please send it back to Brett so he can share the laughs.

## 📝 Notes

This was Brett's first programming project. The initial edits were made in Notepad++ and built with Microsoft Visual Studio, and it is regularly played in multiplayer with Darrin—the reason the practical multiplayer fixes exist.

Questions, feedback, or interested in collaborating: **bm069au@gmail.com**