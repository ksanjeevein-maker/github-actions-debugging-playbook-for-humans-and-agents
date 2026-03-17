# GitHub Actions Debugging Concepts

## Event context first

- Common mistake: debug the command output without checking which event, ref, or payload triggered the workflow.
- Better approach: inspect `github.event_name`, branch refs, matrix values, and job conditionals first.
- Mental shift: the workflow logic often fails before your script even starts.
- Watchouts:
  - `pull_request` and `push` have different ref behavior.
  - Conditionals can silently skip the step you thought was running.

## Runner environment

- Common mistake: assume your local shell and filesystem match the runner.
- Better approach: verify OS, shell, working directory, path resolution, and tool availability.
- Mental shift: a runner is a fresh machine with explicit setup steps.
- Watchouts:
  - PowerShell, bash, and sh differ in quoting and env access.
  - Relative paths often break after `working-directory` changes.

## Caching and dependency state

- Common mistake: trust cache hits blindly.
- Better approach: make cache keys encode the real invalidation inputs.
- Mental shift: cache correctness matters more than cache speed.
- Watchouts:
  - Partial restore keys can mask dependency drift.
  - Cache hits do not guarantee the toolchain or lockfile state is what you expect.
