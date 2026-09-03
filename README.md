# Road to IPO

A single-player strategy game about funding startups, riding mergers, and cashing out before the market closes. You and three AI rivals place tiles on a city grid, found companies, buy shares, and collect payouts when bigger companies swallow smaller ones. Highest net worth when the closing bell rings wins.

**Play it now:** https://mlpayne1970.github.io/Venture-Cap/

This is the web build of a game headed for iPhone, iPad, and Android. It runs entirely in your browser -- nothing to install, nothing sent anywhere, and your game autosaves locally so you can pick it back up later.

## How it plays

- **Place a tile** each turn. A tile next to nothing sits alone; next to a lone tile it founds a new company (you pick which, and get a free founder's share); next to a company it grows it; between two companies it triggers a merger.
- **Mergers pay out.** The larger company survives and the biggest shareholders in the absorbed company collect majority and minority bonuses. Then everyone holding those shares decides whether to sell, trade two-for-one into the survivor, or hold for a possible comeback.
- **Buy up to three shares** a turn. Bigger companies mean pricier shares. Companies in the premium sector cost more from the start.
- **Going public.** Once a company is big enough it can no longer be absorbed. When every company on the board has gone public, or one company gets large enough, the player on the move may ring the closing bell -- or keep playing if they think they can still catch up.

There is a full rules sheet in the in-game menu.

## Your rivals

Three personalities (the Shark, the Turtle, the Fox) at three funding rounds of difficulty (Angel, Series A, IPO). Each rival goes after whoever is actually winning, not just you, and the standings strip shows you a live read on what each one is up to.

## What's in this build

- Live standings with rival "tells"
- Merger preview showing who gets paid and how much before you commit
- Undo your placement until money changes hands
- Optional closing bell: the game only ends when you say so (or when the board forces it)
- Turn summaries, headlines, and a full game log
- Phone, tablet, and desktop layouts

See [CHANGELOG.md](CHANGELOG.md) for the full history.

## Classic prototype

The original single-file prototype (June 2026) is still playable at https://mlpayne1970.github.io/Venture-Cap/classic/ for anyone who wants to compare.

## Building from source

The game is a pure TypeScript engine and AI (no framework, no DOM dependencies in the engine) with a small vanilla UI, bundled into one self-contained `index.html` by Vite. The source lives in a separate development folder; the file in this repo is the build output.

```sh
npm install
npm test          # vitest: rules, mergers, AI, full seeded games
npm run typecheck # tsc --noEmit
npm run build     # emits dist/index.html
```

## Status

Actively developed. The board layout, company roster, and pricing tables will keep changing as the game finds its own shape ahead of a mobile release.

Made by Matt Payne with AI-assisted development.
