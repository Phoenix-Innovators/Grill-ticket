# GitHub + Jira Working Guide

Use this guide for everyday work in:

- **GitHub repository:** [Phoenix-Innovators/Grill-ticket](https://github.com/Phoenix-Innovators/Grill-ticket)
- **Jira project:** `PI`
- **Workflow contact:** Brie

Create the work once, let automation create the matching record, and include the Jira key in your branch, commits, and pull request.

## Quick reference

| I want to… | Do this |
| --- | --- |
| Start in GitHub | Create an issue and wait for the linked Jira task. |
| Start in Jira | Create a `PI` task with the `github` label already included. |
| Find the Jira key | Check the GitHub issue's automation comment or its `Created from Jira:` line. |
| Name a branch | Use `feature/PI-12-login-redirect`. |
| Write a commit | Use `PI-12 Fix login redirect`. |
| Title a pull request | Use `PI-12 Fix login redirect`. |
| Reference the GitHub issue in a PR | Add `Related GitHub issue: #42` to the PR description. |
| Finish work | Meet the team's completion criteria, then close the GitHub issue or move the Jira task to Done. |
| Fix a missing link | Contact Brie before creating another record. |

## How our team's automation works

These rules describe our team's configured automation, not behavior guaranteed by connecting GitHub and Jira alone. If a linked record does not update, contact Brie before creating another. The rules below still need confirmation against the live setup; reopening is explicitly unverified.

- Creating a Jira `PI` task with the `github` label creates a matching GitHub issue.
- Opening an issue directly in GitHub creates a matching Jira task. Issues already created from Jira should not create another task.
- The Jira key and link appear on the GitHub issue.
- GitHub title and description edits update the corresponding Jira fields where that mapping is configured.
- Closing the GitHub issue moves its linked Jira task to **Done**.
- Moving the Jira task to **Done** closes its linked GitHub issue.

> **Reopening is unverified:** reopening a GitHub issue is intended to move its Jira task back to **To Do**. Confirm the current behavior with Brie before relying on it.

GitHub Projects column changes are not covered by these sync rules.

## Everyday workflow

1. Create or choose the work in GitHub or Jira. Do not create the same work separately in both.
2. Wait for the matching record and find the Jira key.
3. Add the uppercase Jira key to your branch name, commit messages, and pull request title.
4. Reference the GitHub issue in the PR description, as explained below.
5. Complete the issue's agreed checks, required review and testing, and any required merge. Non-code tasks follow their agreed completion checks.
6. Close the GitHub issue or move the Jira task to **Done**, or confirm it was closed automatically.
7. Check that the linked record updated. Contact Brie if it did not.

## Finding and using the Jira key

The key may appear in a GitHub issue comment:

`Jira task: PI-12`

For an issue created from Jira, it may appear in the issue body:

`Created from Jira: PI-12`

Use the key exactly as shown, including uppercase letters.

| Item | Example |
| --- | --- |
| Jira task | `PI-12` |
| GitHub issue | `#42` |
| Branch | `feature/PI-12-login-redirect` |
| Commit message | `PI-12 Fix login redirect` |
| Pull request title | `PI-12 Fix login redirect` |

The Jira key and GitHub issue number are different identifiers.

Automation supplies the Jira key, but you still add it to branches, commits, and pull request titles yourself. Edit GitHub-generated branch names if needed.

## Connecting a pull request to the GitHub issue

The Jira key links development activity to Jira. Also reference the GitHub issue in the PR description so teammates can find the original work:

```text
Related GitHub issue: #42
```

When merging the PR should complete the issue, use this instead:

```text
Closes #42
```

GitHub interprets closing keywords when the PR targets the repository's default branch. Merging that PR can automatically close the issue and trigger our Jira status sync. Use `Closes` only when merging satisfies the issue's completion checks; otherwise use the non-closing reference and close the issue after the remaining checks pass.

References: [GitHub PR and issue linking](https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/linking-a-pull-request-to-an-issue), [linking development activity to Jira](https://support.atlassian.com/jira-cloud-administration/docs/use-the-github-for-jira-app/).

## Labels and duplicate prevention

- When starting in Jira, include `github` when creating the task. Adding it later is not the documented team workflow.
- Leave the automatically added Jira label `gh-<number>` intact. It connects the task to its GitHub issue.
- If the matching record or Jira key is missing, contact Brie before creating a replacement.
- Close work only after the team's completion criteria are met, because closure updates the linked record.

## Example

1. A developer opens GitHub issue `#42`: “Fix login redirect.”
2. Automation creates Jira task `PI-12` and adds its key and link to the GitHub issue.
3. The developer creates branch `feature/PI-12-login-redirect`.
4. They commit with `PI-12 Fix login redirect`.
5. They open a pull request titled `PI-12 Fix login redirect` and add `Related GitHub issue: #42` to its description.
6. After the required review, testing, merge, and other completion checks, they close issue `#42`. If a closing keyword was used and GitHub already closed it, they confirm that result instead.
7. They check that the linked Jira task moved to **Done** and contact Brie if it did not.
