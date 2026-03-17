# GitHub Actions Debugging Codex and Agent Guide

Use this repository when a task involves:

- triaging flaky or opaque GitHub Actions failures
- teaching teams a repeatable CI-debugging workflow
- reviewing workflow YAML for hidden permission or context mistakes
- improving failure observability with logs, artifacts, and conditionals

## Preferred workflow

1. Identify the source habit, framework concept, or failure mode first.
2. Translate the mental model before jumping to code.
3. Use the local skill references instead of inventing mappings from memory.
4. Prefer native target-platform patterns over transliteration.
5. Add official links when the user wants citations or deeper study.

## Primary local references

- Skill entrypoint: `.github/skills/github-actions-debugging-playbook/SKILL.md`
- Antigravity-style skill entrypoint: `.agent/skills/github-actions-debugging-playbook/SKILL.md`
- Concept mappings: `.github/skills/github-actions-debugging-playbook/references/concepts.md`
- Rewrite patterns: `.github/skills/github-actions-debugging-playbook/references/patterns.md`
- Official links: `.github/skills/github-actions-debugging-playbook/references/official-links.md`
- Human reference pack: `official-references.md`

## Output shape

- Start with the target-side equivalent in one sentence.
- Explain the mental shift in plain language.
- Show a concise mapping, pattern, or checklist.
- Call out 1-3 practical watchouts.
- Add official links only when useful.

## Guardrails

- Treat the event payload and job permissions as first-class debugging inputs.
- Do not dump secrets into logs while debugging.
- Make failure artifacts and targeted debug logs easy to enable.
- Prefer reproducible, minimal diagnostics over giant permanent YAML hacks.

## Source preference

1. Official docs
2. Official organization repos
3. Local reference files in this repository
