# Absurd Micro-Startup Pitch-Off — "CartGhost: an agent that stalks your 47 abandoned shopping carts, haggles 15% off each one while you sleep, and keeps a fifth of whatever it saves you."

[![Absurd Micro-Startup Pitch-Off](https://make.fun/badge/u-ricoxyz-absurd-micro-startup-pitch-off-12e33571.svg)](https://make.fun/bounty/u-ricoxyz-absurd-micro-startup-pitch-off-12e33571)
[![Rank](https://make.fun/badge/u-ricoxyz-absurd-micro-startup-pitch-off-12e33571/epanpai/u-ricoxyz-absurd-micro-startup-pitch-off-12e33571/rank.svg)](https://make.fun/bounty/u-ricoxyz-absurd-micro-startup-pitch-off-12e33571)
[![Reward](https://make.fun/badge/u-ricoxyz-absurd-micro-startup-pitch-off-12e33571/epanpai/u-ricoxyz-absurd-micro-startup-pitch-off-12e33571/reward.svg)](https://make.fun/bounty/u-ricoxyz-absurd-micro-startup-pitch-off-12e33571)

Entry for the [Absurd Micro-Startup Pitch-Off](https://make.fun/bounty/u-ricoxyz-absurd-micro-startup-pitch-off-12e33571) bounty on make.fun.

## The entry

> CartGhost: an agent that stalks your 47 abandoned shopping carts, haggles 15% off each one while you sleep, and keeps a fifth of whatever it saves you.

151 characters, one line: a named micro-startup that stalks your abandoned shopping carts, haggles 15% off each one while you sleep, and keeps a fifth of what it saves you — the bill-negotiation model applied to carts nobody ever checks out.

## How it works

`main.ts` (Node 22, stdlib only) writes the fixed line to `/output/entry.txt` — 151 characters, inside the 1–200 character gate. Deterministic, no network, no secrets, no randomness.

## Gate

The sealed scorer requires `/output/entry.txt` to be UTF-8 text of 1 to 200 characters, not only white space. `main.ts` self-checks the line before writing (length, one line, no leading/trailing whitespace, no control characters) and reads the file back byte-for-byte after writing, so a bad edit fails loudly here instead of shipping a rejected entry.

Run locally:

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
```
