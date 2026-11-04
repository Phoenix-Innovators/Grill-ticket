# Grill Lab product requirements

Version 1 · November 4, 2026 · Team review

## What we are building

Grill Lab is a Jira app for the Gridiron engineering team on one Atlassian site. It helps ticket authors explain what they need and helps developers understand how to build it.

Vague tickets cause rework. Useful information is often spread across Jira, Confluence, and code. Grill Lab brings relevant information together and makes missing decisions visible.

## The two features

**Grill My Ticket** reviews the available context, asks one question at a time, and drafts acceptance criteria: clear checks that show when the work is done. The author can edit the draft and must approve it before it becomes the shared requirement.

**Context Lab** uses the approved criteria and available sources to suggest build steps, explain its reasoning, and provide verification checks. Both features are required for the MVP.

## The user journey

1. Open Grill Lab inside a Jira ticket.
2. See which sources were reviewed and which are missing.
3. Answer up to five questions, skip a question, or choose Draft now.
4. Edit and approve the acceptance criteria.
5. Open Context Lab for source-backed build guidance.
6. Return later to resume work and check whether the guidance is still current.

## Requirements

| ID | The app must… |
| --- | --- |
| FR01 | Read only information the current user can access and show source coverage. |
| FR02 | Review relevant context before asking questions; identify gaps and conflicting information. |
| FR03 | Ask one question at a time, with a five-question maximum including skips and follow-ups. Retries must not count twice. Allow an early draft. |
| FR04 | Let the author add, edit, and remove testable criteria. Keep unknowns and assumptions separate. |
| FR05 | Save the exact approved criteria as a new version. Reject empty criteria and warn about conflicting edits. Repeated submissions must not create duplicate approvals. |
| FR06 | Link build guidance to approved criteria, supporting sources, and verification checks. Clearly label proposed actions and uncertainty. |
| FR07 | Flag guidance when its criteria or sources change. Show when freshness cannot be checked. |
| FR08 | Save progress across reloads and provide clear recovery after errors. Preserve the last good approval. |
| FR09 | Keep private work private. Recheck access before showing saved content, including questions, drafts, guides, and source details. |
| FR10 | Keep AI choices, spending, question limits, validation, and saving rules under backend control. AI output cannot approve itself. |

Facts about existing code or documents need supporting sources. A suggestion must not invent a file, framework, or current behavior. When evidence is missing, show a partial guide and explain what is needed. Partial guidance does not count as a complete release test.

## What is included

One Jira issue panel with both features. Sources include the current ticket, relevant Jira work, agreed Confluence spaces, selected official Forge guidance, and one selected repository.

Approved criteria are saved in the panel and can be copied. Existing Jira titles and descriptions stay intact.

Code editing or execution, automatic description changes, automatic issue creation, pull-request checks, and crawling every connected app are outside the MVP.

## Privacy and saved work

Users review exactly what will be shared before approval. Private source content must not automatically become shared criteria. The team must agree which answers and information may be published.

Recheck access when saved content is opened. Hide dependent private content if access is denied or cannot be confirmed. Keep previous approval versions when a new version is approved; explicit deletion follows the agreed retention policy.

Checking a guide step records user progress. It does not certify that code passed a test.

## What success looks like

- Ten representative tickets complete both features using real sources.
- At least four of five pilot reviewers can identify a useful next step.
- Factual claims have supporting evidence; proposals and uncertainty are clear.
- Release tests find no unresolved access leaks, approval bypasses, duplicate saves, or question-limit failures.
- The complete journey works with keyboard and screen reader, including errors and recovery.
- Measured AI cost and response time fit the team's agreed limits.

These are release targets, not results already achieved.

## Ownership and open decisions

Brie owns product scope and coordinates delivery. Each area owner researches options, chooses an approach, estimates work, and creates concise issues. Decisions affecting other roles, cost, permissions, or product behavior are reviewed together.

The team still needs to confirm pilot sources, permitted AI processing, model choice, spending limits and budget owner, retention, unassigned roles, and release date. OpenRouter is the preferred first AI connection; native Forge AI remains an alternative. Models stay configurable and must be evaluated before selection.

See the [MVP plan](mvp.md), [team responsibilities](team-areas.md), [build recommendations](implementation-decisions.md), and [release checks](acceptance-and-evidence.md).

Keep this PRD current when scope or behavior changes. Link issues to requirement IDs and update the related checks before closing work.

Revision 1 · November 4, 2026: Simplified for team review; both features and FR01–FR10 remain in scope.
