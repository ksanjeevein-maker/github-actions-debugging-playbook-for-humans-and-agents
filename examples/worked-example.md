# Worked example: flaky pull request job with hidden permission mismatch

This example shows a CI failure that only appears on pull requests because the workflow assumes permissions and secrets that do not exist in that event context.

## Failing workflow shape

```yaml
on:
  pull_request:

jobs:
  comment:
    runs-on: ubuntu-latest
    steps:
      - run: gh pr comment "$PR_NUMBER" --body "done"
```

## Improved workflow shape

```yaml
jobs:
  comment:
    if: github.event_name == 'pull_request' && github.event.pull_request.head.repo.fork == false
    permissions:
      pull-requests: write
      contents: read
    steps:
      - name: Show safe context when debug is enabled
        if: ${{ runner.debug == '1' }}
        run: |
          echo "event=${{ github.event_name }}"
          echo "fork=${{ github.event.pull_request.head.repo.fork }}"
```

## What to notice

- The fix comes from event and permission awareness, not more shell output.
- Job conditions can prevent unsupported paths from running at all.
- Targeted debug output beats permanent log noise.
