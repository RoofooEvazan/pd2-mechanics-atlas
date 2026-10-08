# Cain

Cain is an interactive 3D map of Project Diablo 2 game mechanics reverse engineered from the game's compiled code, and how
each mechanic feeds the others.

**Open it:** https://roofooevazan.github.io/pd2-mechanics-atlas/

- Each star is a mechanic, coloured by system. Arcs show how one mechanic changes another.
- Every mechanic carries its evidence level:
  - **Verified natively**: the game's own code was run in an emulator and matched a model, and a deliberately wrong model failed.
  - **Partly verified**: some steps are verified natively; the rest were read from the disassembly or game tables. The mechanic's panel says which.
  - **Read from code**: from the disassembly only.
  - **Game tables**: from the live data tables only.
  - **Not yet reverse engineered**: known but not traced yet.
- "Verify in game" findings were found in the code and need in-game verification before they are treated as confirmed bugs.
- **Research to-do** lists what is still open.

Source references in each panel point at the research files they came from. The page is built from that research,
which is not part of this repository.
