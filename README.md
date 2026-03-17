# GitHub Actions Debugging Playbook for Humans and Agents

A playbook for debugging CI failures in GitHub Actions.

High-value debugging comes from event awareness, permission clarity, cache discipline, and artifact capture, not random `echo` spam.

## What makes this repo more useful now

- A stronger learning path for self-study and onboarding
- A worked example that shows the migration or debugging move end to end
- A mental-model diagram for fast orientation
- A review checklist for code review or design review
- Portable agent files for Codex, Copilot, Cursor, and Antigravity

## Learning path

- Start with event context and job conditions before debugging commands.
- Check runner environment, shell, filesystem, and toolchain assumptions next.
- Then review permissions, secrets, and cache keys.
- Finish by improving failure forensics with logs, artifacts, and reproducible reruns.

## High-signal traps

- Debugging the script before checking whether the wrong event or ref triggered it.
- Printing too much and still not capturing the exact artifact or context you need.
- Trusting cache hits without validating invalidation logic.
- Assuming `GITHUB_TOKEN` and secrets behave the same on forks and pushes.

## Read this next

- Main portable guide: `AGENTS.md`
- Decision guide: `docs/decision-guide.md`
- Worked example: `examples/worked-example.md`
- Mental-model diagram: `docs/mental-model-map.md`
- Review checklist: `docs/review-checklist.md`
- Official references: `official-references.md`

## Agent formats

- Codex and generic portable guide: `AGENTS.md`
- Copilot repo instructions: `.github/copilot-instructions.md`
- Copilot skill: `.github/skills/github-actions-debugging-playbook/`
- Cursor rule: `.cursor/rules/github-actions-debugging-playbook.mdc`
- Antigravity-style rule: `.agent/rules/github-actions-debugging-playbook.md`
- Antigravity-style skill: `.agent/skills/github-actions-debugging-playbook/`
