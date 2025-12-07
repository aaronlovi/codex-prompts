# Plan to improve `prompts/create-meta-prompt.md`

## Gaps observed
- Branching/reconciliation: guidance exists but could be more direct on when to split, when to force reconciliation, and how to mark canonical branches.
- Verification clarity: verification steps mention commands in general; could emphasize stating what to run when sandboxed and what to record when blocked.
- Duplication/length: sections are verbose; some points repeat between Usage, Dependency detection, and Execution flow.
- Precedence: target `AGENTS.md` vs `prompts/PROMPT_RULES.md` is noted but could be surfaced earlier in Usage.
- Archiving/cleanup: archiving is mentioned but could be clearer about not auto-archiving and about where to leave failed prompts.
- Examples: only brief examples; could add a short chained example (research → plan → do) and archiving step.

## Proposed edits (ordered)
1) Surface precedence early: in Usage, first bullet should say read target `AGENTS.md` then fall back to `prompts/PROMPT_RULES.md`.
2) Tighten branching guidance: explicitly state when to split (independent concerns or risky parallel research), when to force sequential, and require a reconciliation step naming the canonical branch if multiple research branches exist.
3) Simplify sections: trim repeated instructions between Usage, Dependency detection, and Execution flow; keep a single concise flow for selection, generation, and archiving.
4) Verification clarity: in Verification section, add explicit wording to note commands that cannot be run due to sandbox and to record what to run later.
5) Archiving/failed runs: clarify that on success you move `prompt.md` to `/completed/`, on failure leave it in place and record status; do not auto-archive.
6) Add a chained example: brief example of research → plan → do paths with concrete slug paths and archiving note.
7) Keep style constraints: remind to avoid XML, keep Markdown metadata, ASCII, `rg`/`apply_patch`, non-destructive edits (ensure not duplicated elsewhere).

## Execution notes
- No repo tests; manual verification only.
- Apply edits directly to `prompts/create-meta-prompt.md` using `apply_patch`.

## Metadata
### Status
success
### Confidence
High
### Dependencies
- AGENTS.md
- prompts/PROMPT_RULES.md
- prompts/create-meta-prompt.md
- prompts/create-prompt.md
- prompts/run-prompt.md
### Open Questions
- None
### Assumptions
- Current structure should remain, only streamlined/clarified.***
