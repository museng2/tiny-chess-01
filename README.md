# tiny-chess-01 entry

A chess engine in at most 4 KB of Python (`main.py`, a packed form of the
readable source, unpacked at startup with `lzma`). It plays the make.fun
gauntlet through the env: negamax alpha-beta with iterative deepening to a
fixed node budget, quiescence search, a transposition table, null-move
pruning, late-move reductions and MVV-LVA / killer / history ordering,
over an incremental material + piece-square evaluation with a bishop-pair
term. No clock and no randomness: the same position always gets the
same move.

Run it with the env set, as the grader does:

    python3 -P -s main.py
