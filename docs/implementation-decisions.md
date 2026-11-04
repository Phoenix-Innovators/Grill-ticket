# Grill Lab build recommendations

Version 1 · November 4, 2026 · Recommendations for owner review

These choices answer the main research questions in plain language. They are a starting plan, not proof of a working app or a replacement for owner judgment. The [gap review](gap-review.md) tracks what still needs a decision or demonstration.

## D01 — Connect sources as the user

Start with direct Jira, Confluence, and GitHub connections on the selected site and repository. Check the current user's access before reading or showing information. If access fails, do not fall back to a more powerful app account.

Use Jira as the main Forge app connection and connect Confluence on the same site. A Jira–GitHub connection does not prove that Grill Lab can read source files.

For GitHub, prefer an app limited to the selected repository, with read-only file permission and access tied to each user. Michael must prove sign-in, renewed access, disconnect, and denied access. Forge's general GitHub example does not prove this exact setup.

Keep Teamwork Graph and Rovo MCP out of the first external-AI route. They can be reconsidered after access and data-sharing rules are proved.

References: [Forge app connections](https://developer.atlassian.com/platform/forge/app-compatibility/), [Forge sign-in providers](https://developer.atlassian.com/platform/forge/manifest-reference/providers/), [GitHub user access](https://docs.github.com/en/apps/creating-github-apps/authenticating-with-a-github-app/generating-a-user-access-token-for-a-github-app), [graph restrictions](https://developer.atlassian.com/platform/teamwork-graph/limitations-and-considerations/).

## D02 — Keep private context separate from shared criteria

Private documents, code, related tickets, and interview history must not automatically flow into shared criteria. Generate the shared draft from information suitable for the ticket's audience and answers the author deliberately chooses to share. Restricted comments need separate care, even when the ticket is visible.

Show the author exactly what will be shared before approval. A checkbox or AI filter cannot guarantee that copied text contains no private facts; the team still needs a publication policy.

Leave the optional Jira-property copy off at first. Save approved criteria in the app. Recheck access before showing any private saved work, including questions and source titles.

References: [Jira comment access](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-issue-comments/), [Jira property privacy](https://developer.atlassian.com/cloud/jira/platform/jira-entity-properties/).

## D03 — Show what is known and what is missing

Keep four things distinct: observed facts, conclusions drawn from facts, proposed actions, and unknowns. Facts need supporting sources. Calling something a suggestion does not excuse an invented file or framework.

If the ticket is readable but another source is missing, continue only with the available information and show the gap. A guide can be partial; explain which criteria need more context. A partial guide cannot pass the full-source release check.

If ticket access is denied or cannot be confirmed, hide saved content and offer an appropriate retry or access action.

## D04 — Save once and protect other people's edits

When two people save against the same version, accept one and warn the other. Keep the second person's edits so they can compare and retry. Repeating a successful submission must return its original result, even after a newer approval exists.

Recommended storage: Forge Custom Entity Store, which can check conditions and save related records together. Alan and Michael may choose another design that passes the same tests.

Create operation IDs on the server. An old or missing submitted ID must not start a new save. Keep previous approvals. Mark deleted work so old requests cannot recreate it.

References: [Conditional saving](https://developer.atlassian.com/platform/forge/storage-reference/entities-transactions/), [record creation and expiry](https://developer.atlassian.com/platform/forge/storage-reference/entities-api/).

## D05 — Control long-running AI work and spending

Save a job before starting it, show progress, and make duplicate job messages harmless. Recover a missed start without creating a second paid request.

Before a call, reserve enough of the project and task budget to cover its maximum allowed cost. Record the attempt and reservation together so simultaneous calls cannot spend the same money. Count unresolved calls against the budget. Settle costs against the original budget period, even if a call finishes after a reset; never refund twice.

A timeout does not prove the provider stopped or charged nothing. Hold the reserved amount and investigate before another paid attempt. An app save and an external AI call cannot be guaranteed to happen exactly once together.

Use an approved model/provider, response limits, and explicit fallback rules. Price-per-token limits do not replace total spending limits. Disable paid calls until cost limits and a budget owner are set.

Suggested starting settings: at most two automatic attempts, a two-minute job deadline, and up to ninety seconds for one call. Any retry must fit the remaining time and budget and have a known prior outcome. Owners confirm the final values.

References: [Forge background work](https://developer.atlassian.com/platform/forge/runtime-reference/async-events-api/), [runtime limits](https://developer.atlassian.com/platform/forge/limits-invocation/), [OpenRouter provider controls](https://openrouter.ai/docs/guides/routing/provider-selection).

## D06 — Keep guidance current and honor deletion

Keep the exact code version reviewed and the branch being followed. On reopen and after background work, check current access separately from source changes.

| Status | Meaning |
| --- | --- |
| Current | Access passed and checked sources still match. |
| Outdated | Criteria or sources changed; offer regeneration. |
| Freshness unknown | Access passed, but a source version could not be checked. |
| Hidden | Access was denied or could not be confirmed. |

Access can change after a check; do not promise instant continuous revocation. Preserve approved criteria when guidance changes.

Suggested retention: unfinished drafts seven days, completed private job data one day, private guides thirty days. Owners confirm these values. Keep older approvals until explicit deletion.

Expired content must be hidden immediately even if physical cleanup happens later. Mark deletion first; every job checks that marker when starting and saving, so late work cannot restore deleted content. Keep minimal markers and spending records without deleted text. App deletion does not promise immediate deletion from provider or platform backups.

References: [GitHub file versions](https://docs.github.com/en/rest/repos/contents), [Forge expiry](https://developer.atlassian.com/platform/forge/storage-reference/entities-api/), [platform data lifecycle](https://developer.atlassian.com/platform/forge/storage-reference/hosted-storage-data-lifecycle/).

## D07 — Confirm the real setup

The team needs actual source selections, test users, sign-in access, permitted AI data handling, spending limits, retention choices, role coverage, and a release date. Confirm each before the work that depends on it; release staffing and dates need not block an early connection test.

**Don't forget you can use Shashi's app to check models and prices.** No app link or access was supplied, so the research did not use it. No model has won an evaluation yet.

Use the [release checks](acceptance-and-evidence.md) to prove these choices work. Record adopted choices and test results in the owning issues.
