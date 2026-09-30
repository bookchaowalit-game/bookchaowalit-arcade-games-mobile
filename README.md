# bookchaowalit-arcade-games-mobile

Planned mobile edition of **Book Arcade**, the small build-in-public game
collection whose web version lives in
[`bookchaowalit-game/bookchaowalit-game-collection-frontend`](https://github.com/bookchaowalit-game/bookchaowalit-game-collection-frontend).

## Status

**Empty / planning.** This repository has no app code yet. Nothing here is
playable, published, or in an app store.

## Intended scope

- Touch-first versions of the web arcade's short games (twelve exist on the
  web: Neon Harvest, Signal Shift, Gridline, and others).
- Offline play; no account, ads, analytics or network access in the first
  version.
- Game rules shared with the web version rather than re-implemented: the web
  repo keeps each game's rules as pure, unit-tested TypeScript modules
  (`lib/<game>.ts`).

## Related repositories

| Repository | Role |
|---|---|
| `bookchaowalit-game-collection-frontend` | Web arcade; source of the game rules |
| `bookchaowalit-game-engine-mobile` | Planned shared mobile game loop/input layer |
| `bookchaowalit-game-collection-mobile` | Different product: a Flutter tracker for games you own |

## Next step

See [`docs/UPGRADE-PLAN.md`](docs/UPGRADE-PLAN.md) for the proposed
scaffold and the first milestone.
