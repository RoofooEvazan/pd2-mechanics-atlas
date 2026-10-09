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

## Stream overlay (OBS)

Add a **Browser Source** in OBS with this URL, width 1920, height 1080:

```
https://roofooevazan.github.io/pd2-mechanics-atlas/?stream
```

It shows only the globe, slowly rotating, with labels. Options (add with `&`):

| Option | Effect |
|---|---|
| `speed=60` | Seconds per full turn (default 60) |
| `zoom=1.12` | Globe size; larger number = smaller globe |
| `tilt=0.32` | Tilt toward the viewer, in radians |
| `bg=transparent` | No background, so the globe sits on top of your own scene |
| `labels=0` | No labels |
| `title=Stream%20Starting%20Soon` | Gold title over the globe (Diablo II's Exocet font if installed on the PC, else Cinzel) |
| `subtitle=...` | Smaller line under the title |
| `titlepos=top` | Title position: `top`, `center` (default) or `bottom` |

Example: `?stream&title=Stream%20Starting%20Soon&bg=transparent&speed=45`

The title uses Exocet, the Diablo II font, when it is installed on the streaming PC (OBS's browser uses installed
fonts); after installing it, use **Refresh cache of current page** on the source.
