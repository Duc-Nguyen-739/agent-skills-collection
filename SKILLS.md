# Skills Index

| # | Name | Category | Triggers | Source |
|---|---|---|---|---|
| 1 | `gas-webapp-review` | `gas` | `gas review`, `apps script audit`, `sheets webapp`, `lockservice`, `cacheservice` | `gas-webapp-reviewer` + `review-gas-failure-modes` + `SubAgent/reviewer1` |
| 2 | `webapp-ui-ux-audit` | `web` | `ui audit`, `ux audit`, `wcag`, `performance audit`, `cdp` | `ui-ux-audit` + `reviewer2/3` + `designer` |
| 3 | `systematic-debugging` | `core` | `debug`, `bug fix`, `root cause`, `flaky` | `systematic-debugging` + `debug-systematic` + `scout` |
| 4 | `accessibility-audit` | `web` | `a11y`, `wcag`, `accessibility`, `screen reader` | `accessibility` |
| 5 | `performance-audit` | `web` | `performance`, `lighthouse`, `core web vitals` | `performance` |
| 6 | `design-system` | `web` | `design system`, `tailwind`, `tokens`, `component library` | `tailwind-design-system` + `ui-design-process` |
| 7 | `codebase-explorer` | `core` | `explore codebase`, `find files`, `trace dependencies` | `scout` + `improve-codebase-architecture` |
| 8 | `code-research` | `core` | `research library`, `api docs`, `read source` | `librarian` |
| 9 | `security-review` | `core` | `security review`, `xss`, `injection`, `privilege` | `security-reviewer` |
| 10 | `writing-plans` | `core` | `write plan`, `implementation plan`, `spec to plan` | `writing-plans` |
| 11 | `project-bootstrap` | `gas` | `gas project`, `apps script`, `rollcall`, `bootstrap` | `project-skill` (generalized) |
| 12 | `debate` | `core` | `debate`, `brainstorm`, `critique`, `converge`, `red-team`, `stress-test`, `review`, `audit` | `debate` (three-model deliberation skill) |

## Categories

- `gas` — Google Apps Script + Sheets specific (2 skills)
- `web` — Web UI/UX, a11y, perf, design (4 skills)
- `core` — Debugging, exploration, research, security, planning (5 skills)

## Output Format (shared)

All skills follow `AGENTS.md §8` style if host repo defines it, otherwise: `TL;DR` 1 line (`✅ Approve — 0 P0 · 2 P1` or `🔴 Blocked — 3 P0`) + table `| # | Sev | Issue | Location | Fix |` (+ `Conf` column for review skills) + markers 🔴 P0 (blocker/security) · 🟠 P1 (break) · 🟡 P2 (cosmetic) + Rule check `A/B/C` + `Anti-pattern` (no vague narration, every claim needs `file:line`).

Confidence thresholds (review skills): Blocker/security always reported; Major ≥70; Minor/Nit ≥80.
