# AI Code Review Checklist

Price: $10

Use this checklist before submitting AI-assisted code.

## Diff Hygiene

- No unrelated formatting churn.
- No accidental secret files.
- No generated cache folders.
- No broad dependency updates.
- No unexplained snapshots.

## Behavior

- Does the change satisfy the issue?
- What happens on empty input?
- What happens on invalid input?
- What happens on slow network?
- What happens on mobile or narrow screens?

## Tests

- Existing tests still pass.
- New logic has focused coverage.
- Manual verification is documented.
- Known untested areas are named.

## Security

- No logging of secrets.
- No unsafe shell interpolation.
- No trusting client input.
- No widened permissions.
- No new public endpoint without validation.

## PR Note

```markdown
I used AI assistance, then reviewed the diff manually. The change is scoped to the issue and verification steps are listed above.
```

