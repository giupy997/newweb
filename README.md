# $AGI — Amphibian Giga Intelligence

Black & white ASCII-style website for **$AGI**, the pons launchpad token that rewards holders in **NVDA**.

- Live site: https://giupy997.github.io/newweb/
- Token on pons: https://www.ponsfamily.com/launchpad/0x4b516cf6e96f9ac43207462ea389d820bcfd4dc9
- Contract: `0x4B516cf6E96F9AC43207462ea389d820bCfD4dc9`

## How the rewards counter works

The page shows creator-fee rewards (earned, distributed to holders, pot for next distribution) pulled from the pons dashboard API:

1. It first tries the pons API directly (and via a CORS proxy).
2. If that fails, it falls back to `data.json`, which a GitHub Action ([update-rewards.yml](.github/workflows/update-rewards.yml)) refreshes every 15 minutes from the pons API.
3. As a last resort it shows baked-in last-known values.

## Deploy

Plain static site — served with GitHub Pages from the `main` branch root.
