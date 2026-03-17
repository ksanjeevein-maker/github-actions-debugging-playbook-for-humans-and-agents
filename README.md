# GitHub Actions Debugging Playbook for Humans and Agents

A playbook for debugging CI failures in GitHub Actions. It focuses on workflow triggers, contexts, permissions, caches, service containers, debug logs, and failure triage patterns that humans and agents can reuse.

CI failures feel random until you make event context, runner environment, permissions, cache design, and artifact capture explicit parts of the workflow.

## Best use

- triaging flaky or opaque GitHub Actions failures
- teaching teams a repeatable CI-debugging workflow
- reviewing workflow YAML for hidden permission or context mistakes
- improving failure observability with logs, artifacts, and conditionals

## Core topics

- event triggers, contexts, and workflow conditionals
- runner environment, shells, and path issues
- caching and dependency invalidation
- permissions, tokens, and secrets troubleshooting
- debug logging, artifacts, and failure forensics

## Questions this pack should answer well

- Why did this workflow run with different values on `pull_request` vs `push`?
- How do I inspect contexts without leaking secrets?
- Why is my cache restoring stale dependencies?
- How should I capture extra logs only when a job fails?

## When not to use this pack

- complete CI/CD platform comparisons
- self-hosted runner fleet management at infrastructure scale
- security policy design beyond GitHub Actions scope

## Agent formats

- Codex and generic portable guide: `AGENTS.md`
- Copilot repo instructions: `.github/copilot-instructions.md`
- Copilot skill: `.github/skills/github-actions-debugging-playbook/`
- Cursor rule: `.cursor/rules/github-actions-debugging-playbook.mdc`
- Antigravity-style rule: `.agent/rules/github-actions-debugging-playbook.md`
- Antigravity-style skill: `.agent/skills/github-actions-debugging-playbook/`

## Source policy

- Prefer official framework and library docs first.
- Prefer official GitHub org repos second.
- Re-check official docs when framework behavior may have changed.
