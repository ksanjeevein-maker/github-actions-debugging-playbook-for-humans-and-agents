---
name: github-actions-debugging-playbook
description: A playbook for debugging CI failures in GitHub Actions. It focuses on workflow triggers, contexts, permissions, caches, service containers, debug logs, and failure triage patterns that humans and agents can reuse. Use when an agent needs a concise reference, migration guide, or side-by-side pattern library for this topic.
---

# GitHub Actions Debugging

Use this skill to answer the practical question, "what is the target-platform way to do the thing I already know?"

## Quick Start

- Read `references/concepts.md` for conceptual mapping and mindset shifts.
- Read `references/patterns.md` for concrete rewrite or debugging patterns.
- Read `references/official-links.md` when official docs or source repos are needed.

## Workflow

1. Identify the source-side habit or failure mode.
2. Translate the mental model before changing code.
3. Prefer native target-platform patterns.
4. Show a small example or checklist instead of a giant transliteration.
5. Call out the main watchouts clearly.

## Output

- Start with the target-side equivalent in one sentence.
- Explain the mental shift in plain language.
- Show a concise mapping, snippet, or checklist.
- Mention 1-3 watchouts.
- Add official links only when useful.

## Guardrails

- Treat the event payload and job permissions as first-class debugging inputs.
- Do not dump secrets into logs while debugging.
- Make failure artifacts and targeted debug logs easy to enable.
- Prefer reproducible, minimal diagnostics over giant permanent YAML hacks.
