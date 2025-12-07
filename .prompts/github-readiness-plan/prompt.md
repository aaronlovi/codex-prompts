# Objective
- Produce a concise plan to ready this prompt repository for publishing/committing to GitHub (repo hygiene, docs, ignore rules, licensing, basic setup).

# Context
- Project type/stack: Markdown-only prompt repository (no build tooling or tests).
- Constraints: follow AGENTS.md; keep ASCII; avoid destructive git commands; use rg for search and apply_patch for single-file edits.
- Key files to read: `AGENTS.md`, `prompts/create-prompt.md`, `prompts/create-meta-prompt.md`, `prompts/run-prompt.md`, root listings.
- References: none existing for this slug.

# Requirements
- Functional: assess current repo state; identify and plan tasks for GitHub readiness (e.g., README completeness, LICENSE choice, .gitignore, repo metadata like description/badges if applicable); call out any missing files or cleanup needed.
- Non-functional: keep plan actionable and minimal; ensure instructions respect sandbox/approval limits noted in AGENTS.md.
- Avoid: placeholders or vague steps; assumptions without noting them; unnecessary new tooling.

# Plan
- Step 1: Read `AGENTS.md` and existing prompts for constraints and conventions.
- Step 2: Inventory repo contents (files/dirs) with rg/ls to spot gaps (README, LICENSE, .gitignore, metadata).
- Step 3: Determine recommended additions/edits for GitHub readiness; note options/assumptions if choices (e.g., license type) are needed.
- Step 4: Draft the plan in the output file with clear tasks, sequencing, and any follow-up questions/assumptions.
- Reflect after each scan before writing the plan.

# Outputs
- `.prompts/github-readiness-plan/plan.md` — the plan with numbered/bulleted tasks and any follow-up notes.
- Append `## Metadata` with `### Status`, `### Confidence`, `### Dependencies`, `### Open Questions`, `### Assumptions` (fill with None if empty).

# Verification
- Manual: ensure the plan is specific to the current repo state and lists concrete file paths/actions; confirm metadata block is filled.
- No automated tests for this repo.

# Success Criteria
- Plan lists clear, ordered tasks to make the repo GitHub-ready (docs, license, ignore rules, metadata).
- Notes any decisions or assumptions explicitly (e.g., license choice).
- Output file and metadata created at the specified path with no placeholders.

# Practices
- Use `rg` for search; prefer `apply_patch` for single-file edits; avoid destructive git commands; keep ASCII.***
