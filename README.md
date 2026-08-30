# Agent Skills Collection

Curated, publish-ready **Agent Skills** (`SKILL.md`) for AI coding agents — compatible with [opencode](https://opencode.ai), Claude Code, Cursor, and any tool supporting the [Agent Skills spec](https://opencode.ai/docs/skills).

Focus: **webapp audit, Google Apps Script webapps, debugging & design** — distilled from real-world GAS + Sheets projects (e.g., `van90bg/attendance-portal` RollCall v2, 261 tests, 17 `.gs` + 9 HtmlService modules).

## Skills (11)

| Skill | Category | Use When |
|---|---|---|
| [`gas-webapp-review`](skills/gas-webapp-review/SKILL.md) | `gas` | Review GAS HtmlService webapps (`doGet`, `Sheets`, `LockService`, `CacheService`) — 30+ failure modes, confidence scoring |
| [`webapp-ui-ux-audit`](skills/webapp-ui-ux-audit/SKILL.md) | `web` | Comprehensive UI/UX audit: design language + WCAG 2.2 + perf + CDP verify + 3-layer cross-audit |
| [`systematic-debugging`](skills/systematic-debugging/SKILL.md) | `core` | 4-phase debugging (Iron Law: no fix before Phase 1) — tight loop, Rule of Three |
| [`accessibility-audit`](skills/accessibility-audit/SKILL.md) | `web` | WCAG 2.2 POUR audit — contrast, keyboard, focus, screen reader |
| [`performance-audit`](skills/performance-audit/SKILL.md) | `web` | Core Web Vitals, budgets, caching, runtime — Lighthouse |
| [`design-system`](skills/design-system/SKILL.md) | `web` | Tailwind v4 + tokens (primitive→semantic→component), surface-first, slop blacklist |
| [`codebase-explorer`](skills/codebase-explorer/SKILL.md) | `core` | Fast read-only exploration with parallel `grep`/`glob` + thoroughness levels |
| [`code-research`](skills/code-research/SKILL.md) | `core` | Research libs via source + docs (local first, then clone), verbatim signatures |
| [`security-review`](skills/security-review/SKILL.md) | `core` | Trace source→sink, privilege boundaries, separate root causes |
| [`writing-plans`](skills/writing-plans/SKILL.md) | `core` | Write implementation plans before code — bite-sized tasks, no placeholders |
| [`project-bootstrap`](skills/project-bootstrap/SKILL.md) | `gas` | Bootstrap GAS + Sheets projects — deterministic edit, CRLF, token system |

See [`SKILLS.md`](SKILLS.md) for full index with triggers and categories.

## Quick Start

### opencode

```bash
# Copy a skill to your project
cp -r skills/gas-webapp-review /path/to/your-project/.agents/skills/

# Or add as git submodule
git submodule add https://github.com/van90bg/agent-skills-collection .agents/skills-collection
```

### Claude Code / Cursor

Skills follow the standard `SKILL.md` frontmatter (`name`, `description`, `license`, `metadata`). Drop the `skills/<name>` folder into your project's skills directory.

## Format

Each skill is a single `SKILL.md` with frontmatter:

```yaml
---
name: gas-webapp-review
description: Review GAS webapps ...
license: MIT
metadata:
  author: van90bg
  version: "1.0"
  category: gas
  triggers: ["gas review", "apps script audit"]
---
```

Body: `When to Use` → `Procedure` → `Checklist` → `Output Format` → `References`. Output follows `TL;DR` + `| # | Sev | Issue | Location | Fix |` + markers 🔴🟠🟡 (see `templates/SKILL-TEMPLATE.md`).

## Examples

- `examples/rollcall/` — RollCall v2 real-world details: `AGENTS.md`, deterministic batch runner, architecture gotchas, mockup language (kept as English example, original VI archived).

## Contributing

PRs welcome. Keep skills: **single responsibility, evidence-backed, no speculative features, surgical edits**. Run `npm run lint:skills` (if present) before PR.

## License

MIT — see [LICENSE](LICENSE).
