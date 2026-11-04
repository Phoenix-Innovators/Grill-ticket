# Grill Lab release checks

Version 1 · November 4, 2026 · Proposed test plan

This explains what the team needs to demonstrate before release. **All results are pending.** A written plan is not a passing test.

## Prepare the tests

Record the app version, environment, selected sources, AI settings, and spending limits. Use real permitted sources and two users with different access. Keep credentials out of test notes.

Confirm data-sharing rules before private information goes to AI, and spending settings before paid calls. Fill testing, security, design, and documentation roles before their release checks. Release dates and estimates do not block early connection tests.

## Ten workflow checks

| ID | What to try | What should happen |
| --- | --- | --- |
| J01 | Complete both features with real sources, then reload. | Source coverage is accurate; exact approved criteria and useful cited guidance are restored. |
| J02 | Choose Draft now early. | Editable criteria appear; unknowns stay separate; missing context is clear. Approval is still required. |
| J03 | Provide conflicting code and team guidance. | Show the conflict and ask about desired behavior. Do not assume existing code is the requirement. |
| J04 | Reach five questions, skip, repeat a request, and reload. | No sixth question or duplicate progress. Saved question and answer state returns. |
| J05 | Save competing edits; repeat a successful submission later. | One save wins; the other gets a warning and keeps its edits. Retry returns the original result without another approval. |
| J06 | Return broken AI output or an invented, irrelevant, or misleading citation. | Reject unsupported output and preserve good saved work. A real link alone does not prove a claim. |
| J07 | Change criteria, a page, or the selected branch; fail a freshness check. | Mark guidance outdated or freshness unknown. Do not silently rewrite approved criteria. |
| J08 | Try another user's saved work, then revoke source or ticket access. | Hide private content, including questions, drafts, guides, job results, titles, and excerpts. Guessing a record ID must not bypass access. |
| J09 | Fail saving, job startup, or AI; repeat a job; run calls near the budget cap. | Preserve work, prevent duplicate saving/spending, and recover safely. Unknown paid outcomes are not automatically retried. |
| J10 | Complete the journey with keyboard and screen reader, including errors. | Controls are labeled, focus is clear, progress/errors are announced, and recovery preserves entered text. |

A negative test may pass because the app stops safely. That is different from completing a normal ticket.

## Six extra checks

| ID | Check |
| --- | --- |
| C01 | Prove GitHub sign-in, renewed access, disconnect, and denial. Distinguish an unconnected Confluence source from a search with no results. |
| C02 | Confirm private context and restricted comments are kept out of shared-draft AI inputs by default. Review deliberate sharing for indirect disclosure too. |
| C03 | Race first saves, repeat old requests, and delete/restart work. Old operations cannot overwrite or recreate new work. |
| C04 | Test missing/exhausted budgets, simultaneous calls, changed prices, late results, and repeated refunds. Keep costs tied to the original budget period. |
| C05 | Open expired work before cleanup; delete during AI processing. Hide expired content, prevent late restoration, and preserve spending records. |
| C06 | Try missing sources, no useful evidence, and unavailable AI. Show clear next actions and partial results without claiming full completion. |

## Compare AI models

Kandis owns the comparison. The suggested starting set is eighteen fixed examples: six for questions/criteria, six for code analysis, and six for guidance. Use the same source information for each candidate.

Review accuracy, usefulness, supporting evidence, and handling of uncertainty. Count all attempts, including broken responses, refusals, retries, cost, and time. A safe refusal can be correct when information is missing; it is not a useful completion when the question was answerable. A high average cannot cancel a serious privacy or evidence failure.

**Don't forget you can use Shashi's app to check models and prices.** Verify current settings and actual workflow cost before choosing a default. This review did not run that comparison.

## Run the pilot

The PRD calls for **ten representative tickets that complete both features with real sources**. These are separate from the ten workflow checks above and the proposed eighteen model examples. Partial guides cannot replace full-source pilot completion.

At least four of five pilot reviewers must identify a useful next step. Ask independently where possible and record their examples. Also note whether they understand how to check the work; that is a recommended review question, not a new numeric target.

## Check accessibility

Recommended review target: WCAG 2.2 AA for the app-owned screens. Check the full journey, including keyboard use, screen reader, labels, focus, errors, zoom, and contrast. Background progress must not steal focus. A component library alone does not prove accessibility.

References: [WCAG requirements](https://www.w3.org/TR/WCAG22/#cc1), [complete journeys](https://www.w3.org/TR/WCAG22/#cc3), [status announcements](https://www.w3.org/WAI/WCAG22/Understanding/status-messages.html).

## Record the release decision

For each check, record pending/pass/fail, app version, source and AI settings, user access tested, observed result, reviewer, date, and an evidence link. Keep private source content and credentials out of the record.

Release when required checks pass, both features work on the ten pilot tickets, the usefulness target is met, and measured cost/time fit agreed limits. Record limitations and fix unresolved access, approval, evidence, or recovery failures before release.

See the [PRD](prd.md), [MVP](mvp.md), and [build recommendations](implementation-decisions.md).
