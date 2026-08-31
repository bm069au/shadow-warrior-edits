# Shadow Warrior 1997 — Brett's Multiplayer Mod

A Windows 10/11 mod build of the JFSW Shadow Warrior source port, made for chaotic multiplayer games with nuclear grenades, dangerous bunnies, and Stalker Mines.

## Download

Choose one of the Windows executables from the [latest release](https://github.com/bm069au/shadow-warrior-edits/releases/tag/Shadow_Warrior):

- **Boss Bunnies + Stalker Mines V7** — the main, more playable build.
- **Bunny Apocalypse** — an earlier experimental build with extreme bunny density; included for laughs.

## What changed

- Grenades are nuclear weapons.
- Caltrops and shurikens inflict fire damage and can set players on fire.
- **Stalker Mines** are a second Stickybomb mode: press weapon key **7** again to select them. They hide after being thrown, chase an enemy that passes nearby, and detonate after a short fuse.
- Boss Bunnies can appear after deaths. They become larger and more dangerous after nuclear explosions, can fire fireballs, and can bite.
- Rare drops: Guardian Head after a nuke and the Rifle on death.
- Multiplayer exit fix: players can leave cleanly even if the hosting player exits first.
- Stickybomb drops are disabled during the final 60 seconds of a multiplayer match to avoid end-of-level timer issues.

## What you need

This repository and its release files contain the modified engine/source code, not the original game assets.

To play, place the downloaded executable in a folder that contains your own legal copy of `SW.GRP` (for example, from GOG). `SW.GRP` supplies the original graphics, sounds, maps, and other game data; it is **not** included here.

## Source and licence

The Shadow Warrior source-port code is provided under the GNU GPL; the licence is in [`jfsw/GPL.TXT`](jfsw/GPL.TXT). You are welcome to download, study, modify, build, and redistribute the GPL-covered code and compatible builds under that licence.

If you make something funny or useful from this fork, please send it back to Brett so he can share the laughs.

## Notes

This was Brett's first programming project. The edits were made in Notepad++ and built with Microsoft Visual Studio. It is regularly played in multiplayer with Darrin—the reason the practical multiplayer fixes exist.

Questions or feedback: **bm069au@gmail.com**
