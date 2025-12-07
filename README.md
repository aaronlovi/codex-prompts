# Prompts Repository

Markdown-only prompt library for Codex agents. Stores runnable prompts under `prompts/` with zero-padded numbering and slugged meta-prompt artifacts under `.prompts/{slug}-{purpose}/`.

## Contents
- `prompts/create-prompt.md`: create task-specific numbered prompts (NNN-name.md).
- `prompts/create-meta-prompt.md`: create research/plan/do meta-prompt flows saved in `.prompts/{slug}-{purpose}/`.
- `prompts/run-prompt.md`: resolve and execute prompt files (numbered or slugged) sequentially by default.
- `.prompts/`: slugged meta-prompt outputs with `prompt.md`, `plan.md`, `research.md`, etc., plus metadata blocks.
- `prompts/PROMPT_RULES.md`: shared baseline rules for using the helper prompts when copying them to other repos.
- `AGENTS.md`: repository rules and conventions.

## Usage (in this repo)
- Generate a numbered prompt for a task with `prompts/create-prompt.md` (pick next zero-padded number). Ask your AI assistant (e.g., Codex) as shown below to do the generation.
- Create meta-prompt workflows with `prompts/create-meta-prompt.md` using descriptive slugs (no numbers) under `.prompts/`.
- Run prompts via `prompts/run-prompt.md`, selecting targets by number, name fragment, or explicit path (including slugged prompts).

## Quick start (tell your AI)
1) “Read `prompts/create-prompt.md` and write the prompt to `./prompts/NNN-name.md` (use the next zero-padded number) for this task: <one-line task>.”
2) If you need research/plan/do chaining: “Read `prompts/create-meta-prompt.md` and generate a slugged prompt under `.prompts/{topic-slug}-{purpose}/` for this task: <one-line task>.”
3) To run a prompt: “Read `prompts/run-prompt.md` and execute `<target-prompt-path>` following its rules.”

## Using These Helpers in Other Repos (human workflow)
- Copy the helper files in `/prompts` (including `PROMPT_RULES.md`) into the target repo (or reference them); keep helper files unnumbered and place runnable prompts as `./prompts/NNN-name.md`. Do not copy any existing `.prompts/` artifacts—those stay per-repo.
- Check the target repo’s `AGENTS.md` (or equivalent) and follow its rules; do not overwrite it. Use `PROMPT_RULES.md` only as the shared baseline when the target repo lacks prompt-specific guidance.
- To create a new task prompt, tell your AI assistant (e.g., Codex): “Read `prompts/create-prompt.md` and write the prompt to `./prompts/NNN-name.md` (use the next number) for this task: <one-line task description>,” and let it gather repo context per the prompt.
- For research/plan/do chains, tell your AI assistant: “Read `prompts/create-meta-prompt.md` and generate a slugged prompt under `.prompts/{topic-slug}-{purpose}/` (purpose = research/plan/do) for this task: <one-line task description>,” and let it gather repo context per the meta-prompt. The meta workflows include a `## Metadata` block by default.
- To execute prompts, tell your AI assistant: “Read `prompts/run-prompt.md` and execute `<target-prompt-path>` following its rules.” Targets can be numbered prompts (e.g., `./prompts/003-task.md`) or explicit slugged paths (e.g., `./.prompts/topic-plan/prompt.md`). The runner handles sequencing and verification steps.

## Conventions
- Read `AGENTS.md` before edits; keep prompts concise with clear sections and no placeholders; include metadata blocks for meta outputs (`## Metadata` with status/confidence/dependencies/open questions/assumptions).

## Contributing and Testing
- No automated tests; verify changes manually (e.g., `rg --files`, `git status --short`).
- Follow AGENTS guidelines for style, naming, numbering, and sandbox awareness.
