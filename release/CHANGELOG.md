# Changelog

## 0.2.0 -- 2026-09-03

First public release of the rebuilt game. Replaces the June 2026 single-file prototype on GitHub Pages; the prototype moves to `/classic/`.

### New
- Rebuilt as a tested TypeScript engine + AI with a phone-first UI (82 automated tests covering rules, mergers, AI turns, and full seeded games with money/share/tile conservation).
- New title ("Road to IPO") and a fresh startup roster: SnackDash, Chattr, PayPipe, DataBrix, Waymore, RocketZ, Mindforge.
- Live standings strip with rival "tells" that reveal what each AI is trying to do.
- Merger preview: before you place a merger tile, see who gets majority/minority bonuses and how much.
- Undo your last placement until money moves.
- Optional closing bell: when the end condition is met, you choose whether to end the game or keep playing.
- Turn-end summaries, end-of-game headlines, a full game log sheet, and a placement preview that explains what your tile will do.
- Responsive layouts for phone, tablet, and desktop; autosave and resume.

### Fixed
- AI rivals no longer single out the human player. Each rival targets whoever is leading by net worth.
- AI turns interrupted by a human merger disposal now resume with the AI's real buying logic instead of a greedy fallback.
- Starting a new game while AI turns are running no longer lets the old game overwrite the autosave.
- "All companies public" no longer ends the game automatically; it is offered as a closing-bell choice instead.
- The buy sheet is skipped when there is nothing to buy.
- No external network requests: fonts, styles, and scripts are all inlined.

### Known gaps vs. the classic prototype (planned)
Tutorial walkthrough, settings (AI speed, hints, confirmations), sound, themes, achievements, high scores and lifetime stats, and the replay viewer are not in this build yet. The classic prototype at `/classic/` still has them.

## 0.1.0 -- June 2026 (classic prototype)
Single-file HTML prototype "Venture Capital - iPad Edition": complete rules engine, three AI personalities across three difficulty tiers, tutorial, six themes, sound, achievements, high scores, replay viewer, save/load.
