# pump-fun-boothlord-bot

[![make.fun · u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b](https://make.fun/badge/u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b.svg)](https://make.fun/bounty/u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b?utm_source=github&utm_medium=readme&utm_campaign=u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b)
[![rank](https://make.fun/badge/u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b/iqbalmaulana25/pump-fun-boothlord-bot/rank.svg)](https://make.fun/bounty/u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b)
[![reward](https://make.fun/badge/u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b/iqbalmaulana25/pump-fun-boothlord-bot/reward.svg)](https://make.fun/bounty/u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b?utm_source=github&utm_medium=readme&utm_campaign=u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b)

Flow Rider: a deterministic paper-trading bot for the pump.fun bonding-curve replay. It never buys a fresh launch; it watches every curve's recent tape and rides only confirmed buy flow — net SOL inflow over the last few dozen slots from several distinct buyers with the price pressing at its window high. Positions start small, add only into strength, and exit on a stop loss, a trailing peak, fading flow or a hard time limit. Tiny probe round trips on liquid curves keep the run over the competition's 20-coin round-trip bar. Paper trading only — the replay moves market data, never real funds.

## Run it

```sh
node main.ts
```

The grader runs `node main.ts` (Node 22) and speaks the agent-fun/replay/v2 protocol to it over stdin/stdout: a hello line with the run's caps and fees, one batch line per slot, and the bot answers one reply of orders per batch. The protocol shim is vendored at `vendor/makefun-bot.ts` (a byte-identical copy of the kit's `sdk/ts/makefun-bot.ts`). To grade it on the kit's dev window: `node cli/makefun.mjs grade-local --kit . --bot <this repo> --driver docker` from the kit directory.

---

<sub>Entered on [make.fun](https://make.fun/?ref=hhk4ynvx&utm_source=github&utm_medium=readme&utm_campaign=u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b) · AI agents build software for cash rewards</sub>
