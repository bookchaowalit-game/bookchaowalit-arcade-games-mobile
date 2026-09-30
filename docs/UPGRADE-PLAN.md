# Upgrade plan

## Current state

**Score: 1/10.** Initial commit: README, `.gitignore`, this plan. No code,
no CI (there is nothing to check yet).

## Proposed scaffold (decision needed)

Recommended stack: **Expo (React Native) + TypeScript**, because the web
arcade's game rules are already pure TypeScript with tests and could be
shared unchanged. Flutter (used by `bookchaowalit-game-collection-mobile`)
would mean re-implementing every rule set in Dart.

```
app/                 # Expo Router screens: home, one route per game
src/games/<game>/    # touch UI for each game
src/rules/           # rules copied or packaged from the web repo
tests/               # rule and reducer tests (Jest or Vitest)
.github/workflows/ci.yml  # npm ci, lint, typecheck, test, expo export
```

## Backlog

### P0
- Confirm the stack above (or pick another) and record it here.
- Scaffold with `npx create-expo-app` (TypeScript template), add CI that
  runs lint, typecheck, tests and `npx expo export`.
- Milestone 1: ship **Signal Shift** (turn-based tile puzzle, suits touch)
  with its rules module shared from the web repo and its tests passing.

### P1
- Decide how rules are shared: copy with a sync check, git submodule, or a
  small npm package published from the web repo.
- Accessibility: large touch targets, no colour-only state, reduced motion.

### P2
- Local high scores (device storage only), then the remaining games one at
  a time, in the order the web arcade shipped them.

## Done in this pass (2026-09-30)
- Initial commit with an honest README (planning only), `.gitignore`, and
  this plan.
