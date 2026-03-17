# GitHub Actions Debugging Patterns

## Dump safe context on demand

```yaml
- name: Show event context
  if: ${{ runner.debug == '1' }}
  run: |
    echo "event=${{ github.event_name }}"
    echo "ref=${{ github.ref }}"
    echo "sha=${{ github.sha }}"
```

## Capture logs on failure

```yaml
- name: Upload failure logs
  if: failure()
  uses: actions/upload-artifact@v4
  with:
    name: test-logs
    path: artifacts/test-logs/
```

## Cache with real invalidation inputs

```yaml
- uses: actions/cache@v4
  with:
    path: ~/.cache/pip
    key: pip-${{ runner.os }}-${{ hashFiles('requirements.lock') }}
```
