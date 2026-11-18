# Grill Lab MVP plan

November 18, 2026

## The goal

Deliver one working Grill Lab Jira panel with Grill My Ticket and Context Lab, usable independently or together. Users request AI help when needed. Both functions share authorized ticket context and saved decisions.

The [PRD](prd.md) defines expected product behavior. This plan defines the delivery work and release checks. The team should verify current implementation and access status before starting integration work.

## Start with the essential decisions

Frontend and UX/UI can build interface prototypes while the team tests connections. Resolve the decisions that block real integration before committing to the affected implementation.

1. **Access and roles.** Verify that new teammates can open Jira and the needed repository. Assign Database Management, DevOps, and Testing owners.
2. **Storage.** Decide what must survive reloads and return visits. The storage owner compares Forge-managed storage with other justified options and proves that saving, versioning, and permission checks work.
3. **Development context.** Inspect the development tools already connected to Jira. Check what Grill Lab can read under the user’s access and app permissions. Determine whether source-file review needs direct provider authorization. Prove one authorized development-context path and keep the provider choice open.
4. **AI and sources.** Confirm which source data can be sent to AI, prove a working inference connection, and review model behavior and safe usage limits.
5. **Panel UX.** Product, Frontend, and UX/UI propose the shared panel and results layout. Backend reviews what data the experience needs.

Record open decisions and owners in the [gap review](gap-review.md). Keep research focused on the work it blocks and record findings in the responsible GitHub issue.

## Build in this order

1. **Prove the connections.** Read a permitted Jira ticket and relevant Confluence content. Verify which development information Jira exposes and prove authorized source-file access if the MVP needs it. Make a permitted AI call, save and reload a result, and verify access denial. Record integration gaps before promising code-aware behavior.
2. **Agree on the shared experience.** Define how the panel, both functions, Backend, AI, and storage share information. Agree on the first results layout and the data it needs.
3. **Build flexible ticket work.** Deliver user-triggered reviews, purposeful questions, clarity feedback, editable criteria and explicit approval, and Context Lab help before or after approval.
4. **Test as work progresses.** Test each function separately and together, including permissions, stale guidance, errors, accessibility, and recovery. Release after real-source checks pass.

## Work packages

Use these IDs as planning references and link existing GitHub issues where they cover the work. Check the [team roster](team-areas.md) when assigning work.

| ID | Outcome | Primary areas involved | PRD |
| --- | --- | --- | --- |
| B01 | Prove authorized Jira, Confluence, and development reads. Check whether source-file access is needed, verify AI and save/reload, and verify denied access. | Backend, AI Lead, Database Management (TBD), Security | FR01, FR08–FR10 |
| B02 | Agree on the panel, both functions, shared context, backend responses, and saved records. | Frontend, UX/UI, Backend, AI Lead, Database Management (TBD) | FR01–FR10 |
| B03 | Reuse permitted Jira, Confluence, documentation, and connected development context. If required, implement and verify an authorized route to source files. Show coverage and limitations. | Backend, Security, AI Lead | FR01, FR02, FR07 |
| B04 | Deliver purposeful AI questions, respectful pushback, clarity feedback, and useful guidance within quality and usage safeguards. | AI Lead, Backend, Product Lead for behavior review | FR02–FR04, FR06, FR10 |
| B05 | Deliver flexible, user-triggered clarification with skipping, early drafting, pause/resume, and recovery. Use safe operation limits and let clarification continue as needed. | Frontend, Backend, AI Lead | FR02–FR04, FR08 |
| B06 | Support review, editing, explicit approval, version comparison, and safe saving of acceptance criteria. | Frontend, Backend, Database Management (TBD) | FR04, FR05, FR08, FR09 |
| B07 | Deliver Context Lab guidance before or after approval, with practical steps, source references, and clear uncertainty. | Frontend, UX/UI, Backend, AI Lead | FR02, FR06, FR07 |
| B08 | Protect and restore private work and handle stale results, retention, deletion, and conflicting updates. | Database Management (TBD), Backend, Security | FR05, FR07–FR09 |
| B09 | Test each function alone and the connected experience for access, evidence, errors, usefulness, and accessibility. | Testing (TBD), Security, UX/UI, AI Lead | FR01–FR10 |
| B10 | Review evidence, deploy, and update documentation for handoff. | DevOps (TBD), Product Lead, Documentation, Scrum Master | FR01–FR10 |

## Owner responsibilities and ticket standard

Owners split work packages into small, reviewable GitHub issues and record their research, approach, estimates, and evidence. Bring changes to product behavior to the Product Lead before updating requirements and acceptance checks.

- **Epic** — One product outcome, one accountable lead, relevant contributors, main dependencies, and high-level completion checks. Link the sub-issues in GitHub.
- **Sub-issue** — One technical deliverable, one accountable owner and primary role, dependencies, and two or three observable checks. The owner adds implementation tasks and estimates story points for the issue separately.
- **Every issue** — State the outcome, owner, applicable PRD IDs, dependencies or blockers, and what done looks like. Link existing research and relevant checks. [Reference code legend](../README.md#reference-code-legend)

The [team roster](team-areas.md) lists Kandis (Frontend), Michael (Backend), Gabba (AI Lead), Brie (Product Lead), Shannan (UX/UI), Alex (Documentation), and Shashi (Scrum Master). This draft lists Dan for Security. Confirm that assignment in the roster, which currently marks Security as TBD. Database Management, DevOps, and Testing are also TBD.

## AI and integration choices

Start with one approved AI connection and compare model performance for clarification, technical analysis, and evidence-backed guidance. OpenRouter was an earlier preferred candidate, and native Forge AI is another option. The AI Lead validates providers, output format, quality, permitted data handling, response time, and cost before selection. Shashi’s model and pricing app may help if the team has access.

Test what Jira already exposes from the team’s connected development tools. If the pilot needs source-file content, Backend and Security choose and prove one authorized access path. Verify source-file permissions separately from access to linked commits or pull requests. Additional direct integrations and automatic event monitoring are backlog work.

The relevant owners validate proposed safeguards, including limits on automatic retries or repair and retention of temporary data. An automatic retry requires a known outcome for the previous paid call. Record model, storage, and source decisions in the owning issues and the [gap review](gap-review.md).

## Before release

Run representative tickets covering Grill My Ticket alone, Context Lab alone, and both together. Include early drafting, incomplete requirements, related-work conflicts, restricted sources, edited approvals, resumed sessions, stale evidence, failures and retries, and keyboard and screen reader access.

Verify that private content stays protected, saved approvals persist, factual claims cite real evidence, and users get useful guidance before completing an interview. Confirm that response times and AI spending fit the team’s agreed limits.

Keep the [release checks](acceptance-and-evidence.md) synchronized. Confirm the proposed ten-ticket pilot and model-evaluation counts with the team. Assign pilot tickets across standalone and combined flows.

Record the deployed revision, verified sources, model route, access cases, test results, limitations, and remaining decisions. Use real sources to verify the release after testing with fixtures.
