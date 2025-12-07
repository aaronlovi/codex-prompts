# Prompts Repository

Markdown-only prompt library for Codex agents. Stores runnable prompts under `prompts/` with zero-padded numbering and slugged meta-prompt artifacts under `.prompts/{slug}-{purpose}/`.

## Contents
- `prompts/create-prompt.md`: create task-specific numbered prompts (NNN-name.md).
- `prompts/create-meta-prompt.md`: create research/plan/do meta-prompt flows saved in `.prompts/{slug}-{purpose}/`.
- `prompts/run-prompt.md`: resolve and execute prompt files (numbered or slugged) sequentially by default.
- `.prompts/`: slugged meta-prompt outputs with `prompt.md`, `plan.md`, `research.md`, etc., plus metadata blocks.
- `AGENTS.md`: repository rules and conventions.

## Usage
- Generate a numbered prompt for a task with `prompts/create-prompt.md` (pick next zero-padded number).
- Create meta-prompt workflows with `prompts/create-meta-prompt.md` using descriptive slugs (no numbers) under `.prompts/`.
- Run prompts via `prompts/run-prompt.md`, selecting targets by number, name fragment, or explicit path (including slugged prompts).

## Conventions
- Read `AGENTS.md` before edits; use `rg` for search and `apply_patch` for single-file changes; default to ASCII and avoid destructive git commands.
- Keep prompts concise with clear sections and no placeholders; include metadata blocks for meta outputs (`## Metadata` with status/confidence/dependencies/open questions/assumptions).

## Contributing and Testing
- No automated tests; verify changes manually (e.g., `rg --files`, `git status --short`).
- Follow AGENTS guidelines for style, naming, numbering, and sandbox awareness.***
