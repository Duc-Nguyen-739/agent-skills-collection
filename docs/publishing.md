# Publishing Guide

## Format

Skills follow the [Agent Skills spec](https://opencode.ai/docs/skills) — a single `SKILL.md` per skill with frontmatter `name`, `description`, `license`, `metadata` (author, version, category, triggers). Body uses `When to Use` → `Procedure/Checklist` → `Output Format` → `References`.

Generalization rules applied when extracting from RollCall:

- Replace hardcoded paths like `C:\Users\Van90BG\...` with `{{REPO_ROOT}}` or `examples/rollcall/`.
- Replace RollCall-specific constants (`StaffData 20 cols`, `LOG_COLS`, `ATTENDANCE_TASK`) with generic placeholders + example callout.
- Keep English for publish; Vietnamese notes archived in `examples/rollcall/README_VI.md` if needed.
- Output format is standardized to `AGENTS.md §8` style (`TL;DR` + `| # | Sev | Issue | Location | Fix |` + markers) — host repo's `AGENTS.md` is the SSOT if present.

## Adding a New Skill

1. Copy `templates/SKILL-TEMPLATE.md` to `skills/<new-skill>/SKILL.md`.
2. Fill `name` (kebab-case), `description` (one line, include triggers), `metadata.triggers`.
3. Keep skill **single responsibility**; link related skills via `References`.
4. Add row to `SKILLS.md` index.

## Versioning

- Bump `metadata.version` on breaking checklist changes; patch on wording fixes.
- Tag releases `v1.0.0`, `v1.1.0` etc. Keep `CHANGELOG.md` if needed.

## Testing

- Run the skill on `examples/rollcall/` and verify `file:line` + fix are correct before PR.

## Publishing to Registry (if applicable)

- `opencode` skills are discovered via `skills/` folders or git submodules — no central registry yet. Share via GitHub URL.
- For `npx` distribution, add `package.json` with `bin` if you want CLI.
