# Objective
- Improve `prompts/run-prompt.md` for clarity and consistency (numbered vs slugged prompts, sequencing rules, sandbox/verification handling) using the established Codex practices.

# Context
- Project: Markdown-only prompt helpers; helpers live in `/prompts`, meta artifacts under `.prompts/{slug}-{purpose}/`.
- Constraints: follow the target repo’s `AGENTS.md` first; fall back to `prompts/PROMPT_RULES.md`; keep ASCII; avoid destructive git commands; use `rg` and `apply_patch`.
- Key files to read: `AGENTS.md`, `prompts/PROMPT_RULES.md`, `prompts/run-prompt.md`, `prompts/create-prompt.md`, `prompts/create-meta-prompt.md`. Check existing metadata if any referenced prompts appear.
- Purpose: do/implementation stage for slug `improve-task-runner`.

# Requirements
- Clarify selection and execution flow in `prompts/run-prompt.md`: numbered prompts vs slugged meta prompts, explicit handling of helpers in `/prompts`, and default sequencing vs allowed parallelism.
- Ensure sandbox/verification instructions tell the operator to note blocked commands/tests and what to run later; keep non-destructive guidance.
- Reduce duplication while preserving step-by-step usability (snapshot, resolve targets, confirmation, execution, wrap-up).
- Align terminology and precedence with `AGENTS.md`/`prompts/PROMPT_RULES.md`.
- Add or adjust examples/notes only if they improve operator clarity; keep the document concise.

# Plan
- Step 1: Read `AGENTS.md`, `prompts/PROMPT_RULES.md`, `prompts/run-prompt.md`, and skim `prompts/create-prompt.md` / `prompts/create-meta-prompt.md` for consistency cues.
- Step 2: List gaps/ambiguities in `prompts/run-prompt.md` (numbering vs slugged prompts, sequencing/parallel rules, sandbox/verification notes, duplication).
- Step 3: Edit `prompts/run-prompt.md` to address the gaps, keeping instructions concise and aligned with repo rules.
- Step 4: Write a brief implementation note summarizing changes and assumptions.

# Outputs
- `prompts/run-prompt.md` — updated runner instructions.
- `.prompts/improve-task-runner-do/implementation-notes.md` — summary of changes, assumptions, and verification; include `## Metadata` with `### Status`, `### Confidence`, `### Dependencies`, `### Open Questions`, `### Assumptions` (use `None` when empty).

# Verification
- Manual: review the updated runner for clarity, consistency with AGENTS/PROMPT_RULES, and correct handling of numbered vs slugged prompts; note any commands/tests that could not be run if sandboxed.
- No automated tests.

# Success Criteria
- Runner instructions are concise, unambiguous on numbered vs slugged prompts, sequencing/parallel rules, and sandbox/verification handling.
- Edits respect AGENTS/PROMPT_RULES and avoid destructive guidance.
- Outputs written to the specified paths with no placeholders and populated metadata.

# Practices
- Use `rg` for search; prefer `apply_patch` for single-file edits; avoid destructive git commands; default to ASCII.***
