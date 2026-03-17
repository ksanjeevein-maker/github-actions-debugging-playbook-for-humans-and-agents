# GitHub Actions Debugging Playbook for Humans and Agents Decision Guide

Use this when you need to choose the next move instead of reading every reference front to back.

## When to use this guide

- Use it when the user is blocked by one of these traps: Debugging the script before checking whether the wrong event or ref triggered it., Printing too much and still not capturing the exact artifact or context you need..
- Use it when you need to decide the order of migration work, not just the target syntax.
- Use it when you need a short review path before shipping or approving code.

## Recommended sequence

### Step 1: Orient

- Focus: Start with event context and job conditions before debugging commands.
- Exit check: Is the workflow being debugged in the correct event context?

### Step 2: Translate

- Focus: Check runner environment, shell, filesystem, and toolchain assumptions next.
- Exit check: Are shell, path, and OS assumptions visible and accurate?

### Step 3: Implement

- Focus: Then review permissions, secrets, and cache keys.
- Exit check: Do cache keys reflect real dependency invalidation inputs?

### Step 4: Harden

- Focus: Finish by improving failure forensics with logs, artifacts, and reproducible reruns.
- Exit check: Are permissions and secrets appropriate for the job?

## If the user is stuck, choose this next move

- If they are porting line by line, redirect to the mental model in `docs/mental-model-map.md` and call out: Assuming `GITHUB_TOKEN` and secrets behave the same on forks and pushes.
- If they need proof, show `examples/worked-example.md` and explain what changed structurally.
- If they are ready to merge or publish, run the checklist in `docs/review-checklist.md`.

## Escalate when

- The implementation still violates this review check: Will the next failure produce better evidence than the current one?
- The chosen approach depends on preserving a source-side habit that keeps causing trouble: Debugging the script before checking whether the wrong event or ref triggered it.
