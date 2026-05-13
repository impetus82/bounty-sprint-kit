# Bounty Sprint Kit

Find small paid GitHub tasks, avoid payout traps, and submit clean work fast.

Version: 1.0
License: Personal use. You may use the templates in your own work. Do not resell this kit unchanged.

## Who This Is For

This kit is for developers and AI-assisted builders who want small, scoped tasks that can be completed without client calls, sales messages, or long negotiations.

It is not a promise of income. It is a workflow for finding better opportunities and avoiding obvious dead ends.

## 10-Minute Bounty Search

Use these GitHub searches first. Sort by recently updated.

```text
label:bounty label:"good first issue" state:open
"$50" "bounty" "good first issue" state:open
"$100" "bounty" "good first issue" state:open
"opire try" "bounty" state:open
"pay on merge" "bounty" state:open
"reward on merge" "bounty" state:open
"wallet" "bounty" "PR" state:open
"USDC" "bounty" "pull request" state:open
"documentation" "bounty" "good first issue" state:open
"typo" "bounty" "good first issue" state:open
"README" "bounty" "good first issue" state:open
"test coverage" "bounty" "good first issue" state:open
"bug bounty marker" "good first issue" state:open
```

Search with GitHub CLI:

```bash
gh search issues "bounty good first issue" --state open --limit 30
gh search issues "\"pay on merge\" bounty" --state open --limit 30
gh search issues "\"USDC\" bounty \"pull request\"" --state open --limit 30
```

## Fast Reject Filters

Skip an issue when any of these are true:

- The issue has dozens of near-identical AI comments and no maintainer replies.
- Payment goes through Stripe, Deel, Upwork, Payoneer, or a platform that may require tax/KYC.
- The repository has no commits in the last 90 days.
- The issue is old, but the owner never comments on submissions.
- The acceptance criteria are vague: "make it better", "improve design", "fix bugs".
- The reward is in an unknown token with no liquidity.
- The task requires private data, account access, production credentials, or social engineering.
- The issue asks contributors to send code only after upfront payment.

## Green Flags

Prioritize issues with:

- Clear acceptance criteria.
- A small reward for a specific file or component.
- Existing tests or a clear way to verify the change.
- Maintainer comments in the last 7 days.
- Existing merged bounty PRs in the repository.
- Payment described as "on merge" or escrowed through a known bot.
- A low number of active PRs for the same task.

## No-KYC Payout Reality Check

No-KYC usually means one of these:

- Direct crypto wallet payment.
- Direct PayPal payment, depending on your region and PayPal account status.
- Gift card payment.
- Platform credit.

Most professional payout platforms can request identity or tax data before release. Before you work, scan the README, issue comments, and linked payment platform docs.

## Comment Template: Claim

Use this when the issue requires a claim comment.

```markdown
/opire try

I can take this. I will keep the change focused on the stated acceptance criteria and submit a PR with verification notes.
```

For non-Opire issues:

```markdown
I can take this. Plan:
- inspect the existing implementation
- make the smallest change that satisfies the acceptance criteria
- include local verification steps in the PR

I will submit a PR rather than discuss payment in the issue thread.
```

## PR Description Template

```markdown
## Summary
- 
- 

## Verification
- [ ] 
- [ ] 

## Notes
This PR is scoped to the bounty acceptance criteria in #ISSUE_NUMBER.
```

## Verification Notes That Maintainers Like

Use concrete commands instead of vague statements.

Good:

```markdown
Verification:
- `npm test -- --runInBand`
- `npm run lint`
- manually checked the empty state and populated state
```

Weak:

```markdown
Tested locally.
```

## 30-Minute Triage Workflow

1. Open 20 candidate issues from searches.
2. Reject anything with obvious KYC/platform risk.
3. Reject anything with more than 5 active competing PRs.
4. Pick one issue where the repo can be installed and tested quickly.
5. Comment only if required by the bounty rules.
6. Fork, branch, solve, verify, submit.
7. Do not post wallet details unless the maintainer requests them or the platform requires it.

## AI Prompt: Issue Triage

```text
Analyze this GitHub issue as a paid bounty candidate.

Return:
1. acceptance criteria
2. likely payout route and KYC risk
3. number of competing PRs/comments
4. estimated implementation size
5. fastest safe verification plan
6. go/no-go decision

Issue:
<paste issue text>
```

## AI Prompt: PR Plan

```text
You are helping me submit a small bounty PR.

Constraints:
- Keep the diff minimal.
- Do not refactor unrelated files.
- Follow existing project style.
- Include verification commands.

Issue acceptance criteria:
<paste criteria>

Repository context:
<paste relevant files or tree>

Produce a step-by-step implementation plan and a PR description.
```

## AI Prompt: Final Review

```text
Review this diff as a maintainer.

Focus on:
- whether it satisfies the bounty acceptance criteria
- hidden regressions
- missing tests
- unclear PR description
- unrelated churn

Diff:
<paste diff>
```

## Tiny Bounty Types Worth Chasing

- README setup fixes.
- CLI help text inconsistencies.
- Missing empty state in UI.
- Broken link checks.
- Test coverage for a known function.
- TypeScript type tightening.
- Dependency-free scripts.
- Documentation examples that no longer compile.
- Small accessibility fixes with obvious verification.

## Tasks To Avoid

- Logo contests with many submissions.
- "Build full MVP" tasks under $100.
- Anything requiring production credentials.
- Vulnerability reports without a proper policy.
- Vague AI-agent tasks with no acceptance tests.
- Token rewards where the token is not listed anywhere credible.

## One-Page Scorecard

Score each issue from 0 to 2.

```text
Clear acceptance criteria: ___ / 2
Maintainer active recently: ___ / 2
Low competition: ___ / 2
No-KYC payout likely: ___ / 2
Small implementation: ___ / 2
Easy verification: ___ / 2

Total: ___ / 12
```

Only work on tasks scoring 9 or higher.

## Minimal Wallet Note

If a maintainer asks for a crypto wallet, reply with only the network and public address.

```markdown
Payment address:
- Network: <network>
- Token: <token>
- Address: `<public address>`
```

Never send seed phrases, private keys, exchange login details, or card numbers.

## Closing Checklist

Before submitting a PR:

- The branch name is specific.
- The diff only touches relevant files.
- Formatting is clean.
- Tests or verification commands are listed.
- The PR links the issue.
- The PR does not ask for payment before review.
- Payment details are not posted unless requested.

Good bounty work is boring in the best way: clear scope, clear proof, clean handoff.

