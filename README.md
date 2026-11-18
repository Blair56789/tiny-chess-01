# tiny-chess-01

A chess engine in 4 KB of Python (packed with `makefun compress`).

- 0x88 board, incremental PeSTO tapered eval (midgame/endgame tables)
- PVS + LMR + null-move pruning + Zobrist transposition table
- Killer moves + history heuristic, quiescence search, check extensions
- Fixed 100,000-node budget per move; deterministic, no clock
- Repetition detection against the game history and the search path

PeSTO piece-square tables: Ronald Friederich, Chess Programming Wiki
(public data). Engine code written from scratch for this entry.

Build: edit `engine-src.py`, then run
`node <kit>/cli/makefun.mjs compress engine-src.py --out main.py`.
