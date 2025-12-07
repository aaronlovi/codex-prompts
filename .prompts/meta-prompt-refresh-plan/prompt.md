# Objective
- Produce a concrete plan to improve `prompts/create-meta-prompt.md` for clarity, efficiency, branching guidance, and verification expectations while keeping it Codex-friendly and consistent with repo rules.

# Context
- Project: Markdown-only prompt helpers; helpers live in `/prompts`, meta outputs under `.prompts/{slug}-{purpose}/`.
- Constraints: follow target repo `AGENTS.md` first; shared defaults in `prompts/PROMPT_RULES.md`; keep ASCII; avoid destructive git commands; use `rg` and `apply_patch` for edits.
- Key files to read: `AGENTS.md`, `prompts/PROMPT_RULES.md`, `prompts/create-meta-prompt.md`, `prompts/create-prompt.md`, `prompts/run-prompt.md`.
- Purpose: plan stage for slug `meta-prompt-refresh`.

# Requirements
- Identify shortcomings in the current `prompts/create-meta-prompt.md` (branching guidance, duplication, verification clarity, chaining/archiving steps, precedence of AGENTS vs PROMPT_RULES).
- Propose actionable edits (what to add/remove/clarify) with rationale.
- Keep outputs concise and ordered for easy implementation.
- Note any open questions or assumptions that affect edits.

# Plan
- Step 1: Read `AGENTS.md` and `prompts/PROMPT_RULES.md` for constraints.
- Step 2: Review `prompts/create-meta-prompt.md` (and skim `create-prompt.md`, `run-prompt.md` for consistency cues); jot gaps and inconsistencies.
- Step 3: Draft an ordered list of edits to improve `create-meta-prompt.md` (clarity, branching guidance, verification, archiving, examples).
- Step 4: Capture assumptions/open questions; finalize the plan.

# Outputs
- `.prompts/meta-prompt-refresh-plan/plan.md` — ordered action plan with rationale; include `## Metadata` (Status, Confidence, Dependencies, Open Questions, Assumptions).

# Verification
- Manual: ensure plan addresses observed gaps and references specific file sections; confirm metadata block is filled.
- No automated tests.

# Success Criteria
- Plan lists concrete, ordered edits to `prompts/create-meta-prompt.md` with rationales.
- Notes any needed decisions or assumptions explicitly.
- Output saved to the specified path with metadata, no placeholders.

# Practices
- Use `rg` for search; prefer `apply_patch` for single-file edits; avoid destructive git commands; default to ASCII.***
