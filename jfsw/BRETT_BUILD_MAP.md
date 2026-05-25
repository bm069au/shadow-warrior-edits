# Brett Shadow Warrior Build Map

## Current build status

- Build compiles cleanly with:
  `nmake /f Makefile.msvc`
- Main executable output:
  `sw.exe`

---

## weapon.c — player death changes

### Player-death rabbits

Location:
- `src\weapon.c`
- Around line `5822`

Behaviour:
- When a player dies, spawns 2 rabbits.
- Uses:
  `BunnyHatch2(pp->PlayerSprite);`

Notes:
- These are ordinary spawned rabbits unless further tagged elsewhere.
- Current intent: player death creates chaos without requiring nuke event.

### Player-death railgun/rifle drop

Location:
- `src\weapon.c`
- Around line `5832`

Behaviour:
- Rare railgun/rifle drop on player death.
- Current probability:
  `RANDOM_P2(1024) < 200`
- Approx chance:
  `200 / 1024 = 19.5%`

Spawn setup:
```c
SET(User[railgun]->Flags2, SPR2_NEVER_RESPAWN);
IconDefault(railgun);
sprite[railgun].xrepeat = 64;
sprite[railgun].yrepeat = 64;

### Rabbit explosion function check

Search:
`Select-String -Path .\src\*.c -Pattern "SpawnMineExp" -Context 8,24`

Findings:
- Nuke-tagged rabbits call:
  `SpawnMineExp(SpriteNum);`
- This is the same mine explosion function used elsewhere for stuck mines and skull/betty explosions.
- `SpawnMineExp()` is defined in:
  `src\weapon.c` around line `11960`.

Current rabbit proximity logic:
- File: `src\bunny.c`
- Around line `1320`
- Tagged rabbits:
  `sp->hitag == 1977`
- Trigger distance:
  `dist < 1200`
- On trigger:
  `SpawnMineExp(SpriteNum);`
  `SetSuicide(SpriteNum);`

Open question:
- Need to inspect the rest of `SpawnMineExp()` after line `11984` to see damage/radius.
- If mine explosion radius is normal, rabbit weakness may be caused by the trigger distance `1200`, position/height, or ownership.

### Rabbit explosion tuning — paused

Current decision:
- Leave exploding rabbits unchanged for now.
- Darren liked them at the current level.
- They have enough random damage variance to kill occasionally.

Known technical finding:
- Exploding rabbits call `SpawnMineExp(SpriteNum)`.
- `SpawnMineExp()` uses:
  `eu->Radius = DamageData[DMG_MINE_EXP].radius;`
- Therefore rabbits appear to use the normal mine explosion radius/damage data.

Likely reason they feel weaker:
- proximity trigger is only `dist < 1200`
- rabbit sprite position/origin may affect effective blast placement
- gameplay randomness makes damage inconsistent

Current status:
- Not high priority.
- Do not tune unless future playtests show they are clearly too weak.