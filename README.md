# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/vrp2111/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/vrp2111/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

The strongest chess engine in 4 KB of Python. `main.py` (4,071 bytes) is a compressed payload (LZMA + base85) that unpacks and execs the engine: a 0x88 board, negamax alpha-beta with a transposition table, quiescence search, null-move pruning, and iterative deepening to a fixed node budget (60,000 nodes, deterministic — no clock, no randomness). Evaluation is material plus tapered piece-square tables with a tempo bonus. It plays the env protocol (`POST /game`, `/move`, `/resign`) and picks the best move by iterative deepening; on an illegal-move refusal it falls back to the next root move. Trial-0 practice: 3.5/6, Elo ~1,370.

## Run it

```sh
python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=s75rqb78&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
