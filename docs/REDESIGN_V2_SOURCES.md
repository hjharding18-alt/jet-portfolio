# Redesign v2: sources for Golf With Jet numbers

All counts from `hjharding18-alt/golfwithjet`, branch `rebuild/off-lovable` at 4c9c727 (Oct 16, 2026).

| Number | What | How computed |
| --- | --- | --- |
| 6 | Visible scoring formats | docs/FEATURES.md `VISIBLE_FORMAT_OPTIONS` (Stroke, Scramble, Texas Scramble, Best Ball, Net Best Ball, Stableford). Match Play hidden, not counted. |
| 1,174 | Tests passing | `bun install --frozen-lockfile && bun run test` (vitest) on Oct 16, 2026: 97 files passed, 3 skipped; 1,174 tests passed, 46 skipped, 0 failed (1,220 defined) |
| 100 | Test files | `git ls-files` matching `\.(test|spec)\.tsx?$` |
| 97 | DB migrations | `ls supabase/migrations | wc -l` |
| 52 | Completed roadmap milestones | data rows in the "Completed" table of docs/ROADMAP.md |
| 33 | App routes | `git ls-files src/routes` `.ts/.tsx`, excluding `__tests__` and README |
| 96 | React components | `git ls-files src/components` `*.tsx` |
| 1,966 | Commits | `git rev-list --count HEAD` (first commit 2026-07-16) |
| 21 | Rebuild PRs merged | `gh pr list --state merged --base rebuild/off-lovable` |
| Phases 1-8 merged, 9 testing | Rebuild progress | `git log origin/main..HEAD` subjects reference Phases 1 to 8; Phase 9 = signed-in testing (in progress), Phase 10 = cutover (planned) |

Screenshots: headless Playwright against the staging build only. Public pages captured signed out; signed-in pages captured with a dedicated demo account in a demo tournament with fictional players. Course geometry from OpenStreetMap (ODbL). Device location was simulated for the live-yardage shot. Join codes are blurred.
