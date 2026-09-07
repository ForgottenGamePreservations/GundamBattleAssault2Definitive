# Gundam Battle Assault 2 - Definitive

A romhack of the PlayStation game Gundam Battle Assault 2 (NTSC-U) that makes the whole roster
playable and adds the two game modes the retail disc has announcer voices for but no menu rows.

Everything is a binary patch to the game's own executable and archives. No source code for the game
exists publicly; the patches are hand-written MIPS assembly injected into the shipped executable,
and the art fixes are rebuilt inside the game's own compressed containers.

![The main menu, now ten rows](assets/img/Gundam%20Battle%20Assault%202%202026-08-22-16-51-51.png)

## Features

**All 34 mechs, unlocked on a fresh boot.** No save file, no unlock grind, no cheat device. Retail
ships 12 mechs and 4 menu rows on a new save; this build gives you everything from the first boot.

**The four cut mechs are selectable.** The-O, Zeta Gundam, Qubeley and Hamma Hamma are complete in
the retail data but were removed from the character select screen. On the select screen, a shoulder
button picks one instantly from any cursor position:

1. In any mode other than Story mode, Press R1 on the mecha select screen (doesn't matter which mech are you highlighting to play as Zeta Gundam! (The announcer will properly say "Zeta Gundam")
2. In any mode other than Story mode, Press R2 on the mecha select screen (doesn't matter which mech are you highlighting to play as Qubeley! (The announcer will properly say "Qubeley")
3. In any mode other than Story mode, Press L1 on the mecha select screen (doesn't matter which mech are you highlighting to play as The-O! (The announcer will properly say "The-O")
4. In any mode other than Story mode, Press L2 on the mecha select screen (doesn't matter which mech are you highlighting to play as Hamma Hamma! (The announcer will properly say "Hamma Hamma")

The press both confirms the pick and selects the mech. Move the cursor or press Triangle to go back
to normal selection. It works in Versus CPU for either fighter, and in Versus 2P each player gets it
on their own controller, independently.

**The announcer says their names.** The disc contains unused character select voice lines for all
four, recorded by the announcer from the first Gundam Battle Assault. They now play on the press.

**Correct name plates and portraits in the fight.** Retail ships placeholder art for three of the
four: Zeta Gundam, Qubeley and Hamma Hamma all carry Domon Kasshu's portrait and a `D-SCYTHE HELL`
name plate, and two of them have a corrupt HUD head. Only The-O was finished. This build replaces
the art with the correct name and a matching pilot.

![Zeta Gundam versus The-O, both with correct plates and portraits](assets/img/Gundam%20Battle%20Assault%202%202026-08-22-16-52-41.png)

**Two new modes**, placed next to the modes they derive from:

- **SHOOTING 2P** - a two player match with unlimited ammunition for both fighters.
- **TRAINING** - a practice match with unlimited ammunition, health, time and special attacks for
  both fighters, against an opponent that **does not act**. It still takes damage, staggers and can
  be knocked down, so combos, ranges and timings can be practised properly. It stays a Versus CPU
  match on the select screens, which is what lets one player choose both mechs.

![A 6 hit combo on the training dummy](assets/img/Gundam%20Battle%20Assault%202%202026-08-22-16-53-22.png)

**A retail bug fixed.** In `OPTION > VOICE TEST`, Trowa's and Treize's clip list pointers are
transposed on the retail disc, so each name plays the other's lines and shows the other's VOICE No.
count. Corrected here with a two byte change.

## How to use

You need an emulator that reads `.chd`. [DuckStation](https://github.com/stenzek/duckstation) is the
usual recommendation and is what this build was tested on; anything based on a reasonably accurate
PlayStation core should work.

1. Add `Gundam Battle Assault 2 (Mod) (NTSC-U).chd` to your emulator's game list, or open it
   directly.
2. Boot it. Everything is already unlocked, so there is nothing to configure.
3. On the character select screen, try R1, R2, L1 or L2 to pick one of the four cut mechs.

Notes:

- The disc keeps its original two track layout including the CD audio track, so music is intact.
- In Versus CPU the shoulder buttons read controller 1 only. Playing that mode on controller 2 alone
  loses the shortcut - there is no reliable way to detect which port a human is actually holding.
- Coming back out of SHOOTING 2P leaves the menu cursor on VERSUS 2P rather than on SHOOTING 2P.
  Cosmetic, and a deliberate trade for making the new modes indistinguishable from ordinary versus
  matches everywhere downstream.
- Save data from this build is not meant to be moved back to a retail disc.

## Credits

- Romhack, disassembly and tooling for this build.
- Gundam Battle Assault 2 is by Natsume and Bandai. All game code, art and audio are theirs; the
  four cut mechs, their voice lines and both unused mode announcements were already on the retail
  disc, and this project only makes them reachable.
- [TCRF](https://tcrf.net/) documented the unused SHOOTING MODE and TRAINING MODE voice samples,
  which is what prompted building the two modes.
- [DuckStation](https://github.com/stenzek/duckstation) by stenzek, used for every play test and for
  the RAM dumps that settled most of the questions in this project.

## License

The patch work in this project is released for free, non-commercial use. Credit is appreciated but
not required.

The game itself is **not** covered by that, and is not included in any redistributable form here.
Gundam Battle Assault 2 remains the copyright of its owners. Use your own legally obtained copy.
