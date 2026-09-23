# Favorite Skills

A curated set of skills for Codex and compatible AI coding agents.

## Installation

Install the skills into Codex's skills directory, which defaults to `$CODEX_HOME/skills` and usually resolves to `~/.codex/skills`.

```bash
# Recommended
npx skills add https://github.com/igornfaustino/skills
```

```bash
# Copy a single skill
cp -r skills/delivery/create-prd ~/.codex/skills/create-prd

# Or symlink the whole collection
ln -s "$(pwd)/skills" ~/.codex/skills
```

Compatible agents may use a different skills directory, but the repository structure stays the same.

## What Are Skills?

Skills are reusable instruction packs that help an AI coding agent execute specific kinds of work with more consistency and context. Each skill lives in its own directory under `skills/` and is centered around a `SKILL.md` file, with optional supporting assets, templates, and references.

## Structure

- `skills/` contains category folders.
- Each skill should live at `skills/<category>/<skill-name>/`.
- Current skills live under `skills/delivery/` because they support a spec-driven feature delivery workflow.

## Skills Catalog

- [`create-prd`](./skills/delivery/create-prd): Creates a Product Requirements Document from a feature request using a structured clarification and drafting workflow.
- [`create-tasks`](./skills/delivery/create-tasks): Converts an existing PRD and tech spec into a sequenced implementation task list and per-task files.
- [`create-techspec`](./skills/delivery/create-techspec): Creates a technical specification from an existing PRD, covering architecture and implementation guidance.
- [`execute-bugfix`](./skills/delivery/execute-bugfix): Reads documented bugs, implements fixes with regression tests, and updates bug tracking status.
- [`execute-qa`](./skills/delivery/execute-qa): Runs QA against PRD, tech spec, and tasks using E2E, accessibility, and visual validation.
- [`execute-review`](./skills/delivery/execute-review): Performs code review against diffs, project rules, tests, and planned implementation documents.
- [`execute-task`](./skills/delivery/execute-task): Implements a specific planned task with the required context, code changes, and tests.
